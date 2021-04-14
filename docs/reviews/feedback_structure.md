## Recommendation on feedback

### General recommendations:
1) Highlight how well were implemented areas of the task like requirements, design of the code base, activity in git, and during the task review.
2) Specify what was good and what could be improved.
3) Use a person's name in the feedback text.
4) Use English as the main language.
5) Use tools to fix possible grammatical errors. I can recommend extensions like [grammarly](https://chrome.google.com/webstore/detail/grammarly-for-chrome/kbfnbcaeplbcioakkpcpgfkobkghlhen)
6) Remember that person will see this feedback on a portal so it should be constructive and informative

### Example of a feedback
Every required item of the task was implemented in time and even sooner. Everything, including database, publish and integration tests run, works as it should be.
Dave fixed all requested changes in the span of a day or convincingly renegotiated via reply comments under the merge request. 
Pretty well-organized code: 
- properly divided into private methods_
- all the required abstractions (interfaces, generics, and patterns) are correctly implemented and used 
- usage of constants instead of literals
- dependency injection with using reflection and name conventions
- usage of lambda-expressions and parameters of methods for filtering logic

Dave sometimes tends to exploitation of the task clauses: time zone setup has been implemented but not used for displaying dates, as the latest wasn’t mentioned in the task.
But as soon as the request to implement missing functionality was made, logic was promptly and neatly implemented.
