## Stretch Blocks

In this challenge,You will be learning about Closures

## Release 0:

Write a function called `createCounter`. This function should contain a variable `count` that is initialized to `0`. This function should return another function that when invoked, increments the counter by 1 and returns the count variable. You should be able to create multiple counters with the `createCounter` function and they should all have their own private variable called `count`.

```js
var firstCounter = createCounter();

firstCounter(); // 1
firstCounter(); // 2
firstCounter(); // 3
firstCounter(); // 4

var secondCounter = createCounter();

secondCounter(); // 1
secondCounter(); // 2
secondCounter(); // 3

firstCounter(); // 5
firstCounter(); // 6

secondCounter(); // 4
```
## Release 1:

What is the result of the following code? Explain your answer.
  ```
  var fullname = 'John Doe';
  var obj = {
     fullname: 'Colin Ihrig',
     prop: {
        fullname: 'Aurelio De Rosa',
        getFullname: function() {
           return this.fullname;
        }
     }
  };
  
  console.log(obj.prop.getFullname());

  var test = obj.prop.getFullname;
  
  console.log(test());
  ```

## Release 2:

What will you see in the console for the following example?
  ```
  var a = 1; 
  function b() { 
      a = 10; 
      return; 
      function a() {} 
  } 
  b(); 
  console.log(a);    
  ```


