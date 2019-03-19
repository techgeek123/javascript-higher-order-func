## Stretch Blocks

In this challenge,You will be learning about HighOrderFunctions

## Release 0:


- Write a function called `reject` which accepts two parameters an array and a callback. The function should return a new array with all of the values that do not return true to the callback. Here are two examples:
```js
reject([1,2,3,4], function(val){
    return val > 2;
}); // [1,2]

reject([2,3,4,5], function(val){
    return val % 2 === 0;
}); // [3,5]
```

