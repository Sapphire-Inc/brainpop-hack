## Brainpop-hack
- Simple brainpop hack that skips any review/quiz with a 10/10.

**Notice**: This does not skip your full assignments that include doing additional activities or watching a movie, this simply submits a graded quiz or a review as a 10/10 but you will still have to manually submit it to your teacher to fully complete it.

## Instructions: 
- 1. Open a review or a graded quiz.
- 2. Open console and paste this code in.
```
fetch(`https://api.brainpop.com/api/students/${Core.options.settings.user_info.id}/activities`,{method:"POST",credentials:"include",headers:{accept:"*/*","accept-language":"en-US,en;q=0.9","content-type":"application/json"},body:JSON.stringify({product:quiz_obj.options.product,language:quiz_obj.player.options.language,resource_type:quiz_obj.player.options.resource_type,resource_id:quiz_obj.player.options.content.category.unit.topic.feature.EntryID,topic_id:quiz_obj.player.options.content.category.unit.topic.EntryID,lesson_id:null,timestamp:"0",content:quiz_obj.player.options.quiz_content.quizFeature.questions.map(((t,e)=>({q_id:t.id,sa:["a","b","c","d"][t.correctAnswer],timestamp:Math.trunc(Date.now()/1e3)+e+1}))),quiz_id:quiz_obj.player.options.quiz_content.quizFeature.id,mode:quiz_obj.player.options.quiz_type})});
```
- 3. You can now close the console and go to your activities and see that your assignment has been completed with a score of 10/10 and you can submit this to your teacher.
