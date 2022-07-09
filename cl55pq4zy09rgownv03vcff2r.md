## LeetCode Question - 1465. Maximum Area of a Piece of Cake After Horizontal and Vertical Cuts 🍰

### About the Series

Problem-solving is a key skill set for any tech-related stuff you might be working on.

When it comes to developers it's one of the most crucial skills which is needed in almost any day-to-day code you might be writing.

So, this series of blogs is all about practicing Daily LeetCode Challenges & Problem-solving. 🚀

### Problem Statement 

[**Maximum Area of a Piece of Cake After Horizontal and Vertical Cuts 🍰**](https://leetcode.com/problems/maximum-area-of-a-piece-of-cake-after-horizontal-and-vertical-cuts/)

> You are given a rectangular cake of size ``h x w`` and two arrays of integers ``horizontalCuts`` and ``verticalCuts`` where:
> 
> - ``horizontalCuts[i]`` is the distance from the top of the rectangular cake to the ``ith`` horizontal cut and similarly, and
> - ``verticalCuts[j]`` is the distance from the left of the rectangular cake to the ``jth`` vertical cut.

> Return the maximum area of a piece of cake after you cut at each horizontal and vertical position provided in the arrays ``horizontalCuts`` and ``verticalCuts``. Since the answer can be a large number, return this ``modulo 109 + 7``

### Video Explanation

%[https://youtu.be/gErjVSkoKDA]
![Sketch-annotation-element-stroke-line-arrow-spiral-up.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1656783229902/L2fEwmCDd.png align="right")


### Solution

**Algorithm**

1. Push `0` and `h` in the `horizontalCuts`.
2. Sort the `horizontalCuts` array in Ascending Order.
3. Take the maximum difference between the cuts by iterating on the list of `horizontalCuts`
4. Push `0` and `h` in the `horizontalCuts`.
5. Sort the `horizontalCuts` array in Ascending Order.
6. Take the maximum difference between the cuts by iterating on the list of `horizontalCuts`
7. Multiply both the max values and return the modulo `10^9 + 7`
8. Now, we got the largest piece of Cake 🍰 

**Code in JS 🧑‍💻 **

```
/**
 * @param {number} h
 * @param {number} w
 * @param {number[]} horizontalCuts
 * @param {number[]} verticalCuts
 * @return {number}
 */
var maxArea = function (h, w, horizontalCuts, verticalCuts) {
  horizontalCuts.push(0, h);
  horizontalCuts.sort((a, b) => a - b);
  var maxH = 0;
  verticalCuts.push(0, w);
  verticalCuts.sort((a, b) => a - b);
  var maxW = 0;

  for (var i = 1; i < horizontalCuts.length; i++) {
    maxH = Math.max(maxH, horizontalCuts[i] - horizontalCuts[i - 1]);
  }

  for (var j = 1; j < verticalCuts.length; j++) {
    maxW = Math.max(maxW, verticalCuts[j] - verticalCuts[j - 1]);
  }

  return (BigInt(maxH) * BigInt(maxW)) % BigInt(1e9 + 7);
};

``` 

**Time Complexity : `O(nlogn)` **

**Space Complexity: `O(1)`**


### You can find me on the web 🌍

- [Github](https://github.com/Souravdey777)
- [LinkedIn](https://www.linkedin.com/in/souravdey777)
- [Twitter](https://twitter.com/Souravdey777)


Add your solution or approach in the comments below.

Show your love by Sharing the blog. 🤗 


> “The best way to predict the future is to create it.”
> 
> ~ Peter Drucker


