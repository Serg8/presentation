Hello everyone! Today I am going to tell you about event loop.
And first I need to say, that JS is a single-threaded non-blocking asynchronous concurrent language.
What is the call stack? The call stack means one thread, one call stack, one thing at a time.
Let's take an example. We have two functions. Function printSum calls function sum. What will happen in the stack? 
First, the stack will get the function printSum. Then will get the function sum. 
Remove function sum. And at the end remove function printSum.
Blocking. Let's imagine that js is not asynchronous language. In this situation, we would have a problem - blocking.
Blocking is when the stack occupied by very long time functions. In this case, the browser is frozen. For example. 
We have a network request. But the network request is slow. So we need to wait when it will be finished. 
While waiting for the browser is blocked.
Let's take an example. The console will output in the following order. 
First we'll see 'I', then 'am' and then 'happy'. Why is that?
In addition to the stack, we have webapis and task queue. 
Therefore, setTimeout move to the webapis from the stack, 
and is executed there. console.log('am') doesn't need to wait for setTimeout to execute. 
And it will move to the stack and executed. When setTimeout is executed callback will move to the task queue. 
And if the stack is empty callback move to the stack.
Thanks for attention :)		
