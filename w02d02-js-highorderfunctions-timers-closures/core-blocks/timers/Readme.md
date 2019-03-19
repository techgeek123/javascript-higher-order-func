## Core Blocks

In this challenge,You will be learning about Timers

## Release 0:

- Write a code that will log out `Hello!` after one second

## Release 1:

- Write a code if we want to stop the timer of one second of the above problem?

## Release 2:

What is the following code doing?
```js
var timerId = setInterval(function(){
    console.log("HI!");
},1000);

setTimeout(function(){
   clearTimeout(timerId);
},3000);
```

## Release 3:

Examine the following code

```js
console.log("first");
setTimeout(function(){
    console.log("second");
},0);
console.log("third");
```

- What are you expecting the function to log out
- Run the following code.
- Compare your results and Explain why this event might have occure
