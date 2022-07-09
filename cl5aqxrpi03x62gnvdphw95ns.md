## LeetCode Question - 509. Fibonacci Number 🤪

### About the Series

Problem-solving is a key skill set for any tech-related stuff you might be working on.

When it comes to developers it's one of the most crucial skills which is needed in almost any day-to-day code you might be writing.

So, this series of blogs is all about practicing Daily LeetCode Challenges & Problem-solving. 🚀

### Problem Statement 

[**Fibonacci Number**](https://leetcode.com/problems/fibonacci-number/)

> The Fibonacci numbers, commonly denoted `F(n)` form a sequence, called the Fibonacci sequence, such that each number is the sum of the two preceding ones, starting from 0 and 1. That is,
> 
> - `F(0) = 0, F(1) = 1`
> - `F(n) = F(n - 1) + F(n - 2), for n > 1.`

> Given n, calculate F(n).
 

**Example 1:**
```
Input: n = 2
Output: 1
Explanation: F(2) = F(1) + F(0) = 1 + 0 = 1.
```

**Example 2:**
```
Input: n = 3
Output: 2
Explanation: F(3) = F(2) + F(1) = 1 + 1 = 2.
```

**Example 3:**
```
Input: n = 4
Output: 3
Explanation: F(4) = F(3) + F(2) = 2 + 1 = 3.
```

### Video Explanation

%[https://youtu.be/a87elJk3ztU]
![Sketch-annotation-element-stroke-line-arrow-spiral-up.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1656783229902/L2fEwmCDd.png align="right")


### Solution 1: Recursive Approach

**Algorithm**

1. This is the recursive solution where If `n` is `0` it will return `0` or if `n` is `1` it will return `1`. This is the base case for recursion 
2. Recursively call the `f(n-1)` and `f(n-2)` to return the final value of `f(n)`
3. Finally we get out `f(n)`.


**Code in JS 🧑‍💻 **

```
/**
 * @param {number} n
 * @return {number}
 */
var fib = function (n) {
  if (n < 2) return n;
  return fib(n - 1) + fib(n - 2);
};
``` 

**Time Complexity : `O(n)` **

**Space Complexity: `O(n)`**


### Solution 2: Iterative approach with an array 

**Algorithm**

1. First of all, `n = 0` return `0` and for `n = 1` return `1`
2. Create an array and store the first two values of the Fibonacci sequence in the array
3. Now update the `ith` value of the array with the `i-1` value + the `i-2` value of the array.
4. Repeat the same for n iterations and then the array will have the `nth` value too.
6. Return the `nth` value from the array


**Code in JS 🧑‍💻 **

```
/**
 * @param {number} n
 * @return {number}
 */
var fib = function (n) {
  if (n < 2) return n;
  var fibArray = [];
  fibArray[0] = 0;
  fibArray[1] = 1;
  for (var i = 2; i <= n; i++) {
    fibArray[i] = fibArray[i - 1] + fibArray[i - 2];
  }
  return fibArray[n];
};
``` 

**Time Complexity : `O(n)` **

**Space Complexity: `O(n)`**

### Solution 3: Iterative approach without an array 

**Algorithm**

The approach is similar to the 2nd solution but it is done without using a new array.
1. First of all, `n = 0` return `0` and for `n = 1` return `1`
2. Store the last two values of the Fibonacci series in `f1` and `f2`.
3. Update `f1` with `f2`
4. Update `f2` with the current sum of `f1` and `f2`.
5. Steps 2 and 3 will be repeated till we get the final value after n iterations.
6. Return `f2`.



**Code in JS 🧑‍💻 **

```
/**
 * @param {number} n
 * @return {number}
 */
var fib = function (n) {
  if (n < 2) return n;
  var f1 = 0;
  var f2 = 1;
  for (var i = 2; i <=n; i++) {
    var currentSum = f1 + f2;
    f1 = f2;
    f2 = currentSum;
  }
  return f2;
};
``` 

**Time Complexity : `O(n)` **

**Space Complexity: `O(1)`**

### Similar Questions for practice

Now it is time to try some similar questions
- [Climbing Stairs](https://leetcode.com/problems/climbing-stairs/)
- [Split Array into Fibonacci Sequence](https://leetcode.com/problems/split-array-into-fibonacci-sequence/)
- [Length of Longest Fibonacci Subsequence](https://leetcode.com/problems/length-of-longest-fibonacci-subsequence/)
- [N-th Tribonacci Number](https://leetcode.com/problems/n-th-tribonacci-number/)


### You can find me on the web 🌍

- [Github](https://github.com/Souravdey777)
- [LinkedIn](https://www.linkedin.com/in/souravdey777)
- [Twitter](https://twitter.com/Souravdey777)


Add your solution or approach in the comments below. Also, show your love by Sharing the blog. 🤗 

> “Belief creates the actual fact.”

> ~ William James


