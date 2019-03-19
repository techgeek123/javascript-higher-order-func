# The Fibonacci Sequence

### Summary
In this challenge we'll again look at implementing the same behavior in two different ways:  iteratively and recursively.

The behavior we're after in this challenge is calculating a number in the Fibonacci sequence.  We'll write two methods, each of which will accept an integer as an argument and return the number at that position in the Fibonacci sequence.  If our methods are called with the argument `7`, they return the seventh number in the sequence.  If called with `23`, they return the twenty-third number in the sequence.


### The Fibonacci Sequence
The [Fibonacci sequence](http://en.wikipedia.org/wiki/Fibonacci_number) is a specific sequence of numbers.  The numbers in the sequence are observable in nature (if interested, see video [Parts 1](http://www.youtube.com/watch?v=ahXIMUkSXX0), [2](http://www.youtube.com/watch?v=lOIP_Z_-0Hs), and [3](http://www.youtube.com/watch?v=14-NdQwKz9w)), and the ratio between the numbers approximates the [Golden Ratio](https://en.wikipedia.org/wiki/Golden_ratio) which has been [used in the arts](https://en.wikipedia.org/wiki/List_of_works_designed_with_the_golden_ratio) for its aesthetic properties.

Why are we interested in calculating numbers in the sequence?  Not for the numbers themselves, but because the sequence represents a real-world system of rules that we can model in code.

The sequence is built by following simple rules:

- The sequence starts with 0 and 1.
- The next number in the sequence is the sum of the last two numbers in the sequence.

![building the Fibonacci sequence](assets/build_fibonacci_sequence.gif)

*Figure 1*. Building the Fibonacci sequence.

Following these rules we can build the Fibonacci sequence:  0, 1, 1, 2, 3, 5, 8, 13 ... (see Figure 1).


## Releases
### Release 0: Iteratively Calculate the nth Fibonacci Number
As described in the *Summary*, we're going to write a method that returns the nth number in the Fibonacci sequence.  For this release, we need to implement this behavior through an iterative algorithm.  Tests have been provided, which we can use to drive our development of this method.

*Note:* We'll use zero-based numbering to reference positions in the sequence.  So, the sequence starts with the zeroth number—like indexes in an array.


### Release 1: Recursively Calculate the nth Fibonacci Number
Now we'll implement the same behavior using a recursive algorithm.  We'll need to supply our own tests.


## Conclusion
This challenge presented us with another opportunity to create behavior with using different implementations:  iterative and recursive.  We want to continue to practice each, so that we can employ whichever is appropriate for a given situation.


# Algorithm Drill: Calculating Count of Subsets

## Summary
If we had five pens, how many unique groups of three could we make?  If we had ten letters, how many unique combinations of four could we make?  If we had twelve players, how many unique teams of seven could we make?

More generically, given a set of *n* options, how many unique *k*-sized subsets could we make?


### A Function for Calculating the Number of Subsets
We're going to define a function that we'll later translate into a JavaScript method.  We'll represent our function as `f(n, k)`.  `n` represents the number of options we have, and `k` represents the size of each subset.  To determine how many unique groups of three we could make from five crayons, we'd have `f(5, 3)`.  Given ten letters, to determine how many unique combinations of four we could make, we'd have `f(10, 4)`.  Do we see how this could translate to a method definition?

```
f(n, k)  = f(n - 1, k - 1) + f(n - 1, k)

f(5, 3)  = f(4, 2) + f(4, 3)
f(10, 4) = f(9, 3) + f(9, 4)
```
*Figure 1*. Generic formula for `f(n, k)` with two examples.

We know that our function needs two inputs:  `n` and `k`.  But what do we do with those inputs?  Figure 1 shows the calculations that we do with them.  Let's take a minute to review both the general formula and how it would be applied to the specific situations we've been discussing.  What type of algorithm does this look like?


### Known Numbers of Subsets
```
f(0, 5) = 0
f(3, 0) = 1
f(7, 1) = 7
```
*Figure 2*. Known values for specific input conditions.

There are some conditions where we know how many subsets we can calculate based on the inputs.  These conditions are shown in Figure 2 and detailed in the following points.

- If there are zero options, we can make zero subsets.
- We can always make one subset of size zero, the empty set.
- If we're trying to make subsets of size one, then we can make as many subsets as there are options.


## Releases
### Release 0: Translate the Function to JavaScript
```js
subset_count(0, 5)
# => 0
subset_count(6, 2)
# => 15
subset_count(6, 3)
# => 20
subset_count(24, 4)
# => 10626
```

Write a `subset_count` method that implements the function we defined in the *Summary*.  Our method should accept two arguments, the number of options and the subset size, and it should return the number of unique combinations of the subset size that can be made from the number of options (see Figure 3).  Tests have been written to describe the known conditions (e.g., when there are zero options).  We'll need to write tests for other use cases.


## Conclusion
Given a real-world function, we were required to translate it into JavaScript.  When developing an algorithm, it's sometimes helpful to understand how we would solve the problem in the real world and then translate our process into JavaScript.


