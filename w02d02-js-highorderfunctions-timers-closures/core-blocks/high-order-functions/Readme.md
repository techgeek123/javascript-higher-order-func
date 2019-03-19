## Core-Blocks

In this challenge you will learn about High Order Functions

## Release 0:

Create a function called `sendMessage` that accepts a string and a function. The `sendMessage` function will return the result of the function being passed to it with the message as a parameter

## Release 1:

- Write a function called `each` which accepts two parameters: an array and a callback function. The `each` function should loop over the array passed to it and run the callback function on each element in it.
```js
// this function should accept 2 parameters, put them in!
function each(){
    // put your code inside here!
}


each([1,2,3,4], function(val){
    console.log(val);
});
// Here is what should be output if you wrote the function correctly

// 1
// 2
// 3
// 4

each([1,2,3,4], function(val){
    console.log(val*2);
});

// Here is what should be output if you wrote the function correctly

// 2
// 4
// 6
// 8
```

## Release 2:

- Write a function called `map` which accepts two parameters: an array and a callback. The `map` function should return a new array with the result of each value being passed to the callback function. Here's an example:
```js
map([1,2,3,4], function(val){
    return val * 2;
}); // [2,4,6,8]
```
