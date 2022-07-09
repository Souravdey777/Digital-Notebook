## LeetCode Question - 128. Longest Consecutive Sequence 🏃🏻

### About the Series

Problem-solving is a key skill set for any tech-related stuff you might be working on.

When it comes to developers it's one of the most crucial skills which is needed in almost any day-to-day code you might be writing.

So, this series of blogs is all about practicing Daily LeetCode Challenges & Problem-solving. 🚀

### Problem Statement 

[**Longest Consecutive Sequence**](https://leetcode.com/problems/longest-consecutive-sequence/)

> Given an unsorted array of integers `nums`, return the length of the longest consecutive elements sequence.
> 
> You must write an algorithm that runs in `O(n)` time.

**Example 1:**
```
Input: nums = [100,4,200,1,3,2]
Output: 4
Explanation: The longest consecutive elements sequence is [1, 2, 3, 4]. Therefore its length is 4.
```

**Example 2:**
```
Input: nums = [0,3,7,2,5,8,4,6,0,1]
Output: 9
```

### Video Explanation

%[https://youtu.be/IWmw5xkJd9s]
![Sketch-annotation-element-stroke-line-arrow-spiral-up.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1656783229902/L2fEwmCDd.png align="right")


### Solution

**Algorithm**

1. we create a `numsMap` and store all the values in the map.
2. Now Iterate through the `nums` array and check if it is the starting point of a consecutive sequence of values or not. ie. `num-1` exists or not. If it doesn’t exist that means it can be starting value of the sequence.
3. Now check whether the next consecutive value exists or not in a while loop and increment the value of the current sequence length.
4. Compare the longest sequence length with the current sequence length whichever is maximum will be stored in longest sequence length
5. Finally return the longest sequence length.


**Code in JS 🧑‍💻 **

```
/**
 * @param {number[]} nums
 * @return {number}
 */
var longestConsecutive = function (nums) {
  var numsMap = new Map();
  for (const num of nums) {
    numsMap.set(num);
  }

  var longestSequence = 0;
  for (const num of nums) {
    if (!numsMap.has(num - 1)) {
      var currentSequence = 1;
      var currentNum = num;
      while (numsMap.has(currentNum + 1)) {
        currentNum++;
        currentSequence++;
      }
      longestSequence = Math.max(longestSequence, currentSequence);
    }
  }
  return longestSequence;
};
``` 

**Time Complexity : `O(n)` **

**Space Complexity: `O(1)`**

### Similar Questions for practice

Now it is time to try some similar questions
- [Binary Tree Longest Consecutive Sequence](https://leetcode.com/problems/binary-tree-longest-consecutive-sequence/)
- [Find Three Consecutive Integers That Sum to a Given Number](https://leetcode.com/problems/find-three-consecutive-integers-that-sum-to-a-given-number/)
- [Maximum Consecutive Floors Without Special Floors](https://leetcode.com/problems/maximum-consecutive-floors-without-special-floors/)


### You can find me on the web 🌍

- [Github](https://github.com/Souravdey777)
- [LinkedIn](https://www.linkedin.com/in/souravdey777)
- [Twitter](https://twitter.com/Souravdey777)


Add your solution or approach in the comments below. Also, show your love by Sharing the blog. 🤗 

> “Believe you can and you’re halfway there.”

> ~ Theodore Roosevelt


