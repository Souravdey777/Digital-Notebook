## LeetCode Question - 376. Wiggle Subsequence 🧠

### About the Series

Problem-solving is a key skill set for any tech-related stuff you might be working on.

When it comes to developers it's one of the most crucial skills which is needed in almost any day-to-day code you might be writing.

So, this series of blogs is all about practicing Daily LeetCode Challenges & Problem-solving. 🚀

### Problem Statement 

[**Wiggle Subsequence**](https://leetcode.com/problems/wiggle-subsequence/)

> A **wiggle sequence** is a sequence where the differences between successive numbers strictly alternate between positive and negative. The first difference (if one exists) may be either positive or negative. A sequence with one element and a sequence with two non-equal elements are trivially wiggle sequences.
> 
> - For example, `[1, 7, 4, 9, 2, 5]` is a wiggle sequence because the differences `(6, -3, 5, -7, 3)` alternate between positive and negative.
> - In contrast, `[1, 4, 7, 2, 5]` and `[1, 7, 4, 5, 5]` are not wiggle sequences. The first is not because its first two differences are positive, and the second is not because its last difference is zero.
> A **subsequence** is obtained by deleting some elements (possibly zero) from the original sequence, leaving the remaining elements in their original order.
> 
> Given an integer array `nums`, return the length of the longest wiggle subsequence of `nums`.


### Video Explanation

%[https://www.youtube.com/watch?v=mp5-uz6W8MA]
![Sketch-annotation-element-stroke-line-arrow-spiral-up.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1656783229902/L2fEwmCDd.png align="right")


### Solution

**Algorithm**

1. First check if the length of the `nums` array is smaller than two or not. If yes, we will simply return the length of the array ie. `0` for `[]` and `1` for `[x]` (where x can be any value)
2. We check the first difference between the `1st` from the `0th` value in the `nums` array and store it in the `previousdiff`
3. If the values are not equal we will count both the no. for the wiggle sequence thus our counter will be `2` and if equal we take our counter to be `1`
4. Now, While iterating the `nums` array we will compare the compare current difference and previous difference. If one is positive the other should be negative or vice versa. Now, we will increment the count if the conditions are satisfied and update the previous difference with the current difference. 
5. Finally return the count of the wiggle sequence.


**Code in JS 🧑‍💻 **

```
/**
 * @param {number[]} nums
 * @return {number}
 */
var wiggleMaxLength = function (nums) {
  if (nums.length < 2) {
    return nums.length;
  }
  var previousdiff = nums[1] - nums[0];
  var counter = previousdiff != 0 ? 2 : 1;

  for (var i = 1; i < nums.length; i++) {
    const currentDiff = nums[i] - nums[i - 1];
    if (
      (currentDiff > 0 && previousdiff <= 0) ||
      (currentDiff < 0 && previousdiff >= 0)
    ) {
      counter++;
      previousdiff = currentDiff;
    }
  }
  return counter;
};


``` 

**Time Complexity : `O(n)` **

**Space Complexity: `O(1)`**

### Similar Questions for practice

Now it is time to try more similar questions
- [Rearrange Array Elements by Sign](https://leetcode.com/problems/rearrange-array-elements-by-sign/)


### You can find me on the web 🌍

- [Github](https://github.com/Souravdey777)
- [LinkedIn](https://www.linkedin.com/in/souravdey777)
- [Twitter](https://twitter.com/Souravdey777)


Add your solution or approach in the comments below. Also, show your love by Sharing the blog. 🤗 


> "Dream big. Start small. But most of all, start."
> 
> ~ Simon Sinek


