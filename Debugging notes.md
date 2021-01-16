### Debugging

> Fix the Problem, Not the Blame

Solve the bug, no matter who introduced it.

> Don't panic

Relax, no matter, do not panic. Dont think thats impossible, coz it happend.

Do not solve the symptopm rather try to find the root cause.

Bug reported does not necessarily be clear enough. Interview the user who reported and if possible sit with and reporoduce the same bug.

> Write breaking test (especially when it takes 10s of steps to reproduce it, one command for reproducing the bug is what we need) and then make it pass.

> Read the error message

Error message and stack trace will give detail.

tip - set the log level to error in production.

> Binary chop

can be applied if there are many releases/stack traces to isolate the root cause.

Try to go into the middle of stack trace, keep chopping untill you get to the cause.

Say after a week we found the issue coming, bianry chop the releases during that time and find the release who is criminal.


> Rubber Ducking

Try to explain the bug to colleauge or talk to yourself, jot down the series of incindent helps in understading the root cause.

> Don't blame OS/Framework

First, eliminate application code.
Read the lib/framework document properly.
If its a data issue, which I miss testing, try to find other part of the codebase which also may fail due to that.


> Debugging and Tracing

Use Debugger to find current state.

Use tracing to find the whole flow ho I got here. (series of steps.)

Have tracing statement with consistent messagage so that it can be automated.




