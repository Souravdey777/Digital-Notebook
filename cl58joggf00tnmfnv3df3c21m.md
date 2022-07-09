## LeetCode Question - 135. Candy 🍭

### About the Series

Problem-solving is a key skill set for any tech-related stuff you might be working on.

When it comes to developers it's one of the most crucial skills which is needed in almost any day-to-day code you might be writing.

So, this series of blogs is all about practicing Daily LeetCode Challenges & Problem-solving. 🚀

### Problem Statement 

[**Candy 🍭**](https://leetcode.com/problems/candy/)

> There are `n` children standing in a line. Each child is assigned a rating value given in the integer array `ratings`.
> 
> You are giving candies to these children subjected to the following requirements:
> 
> - Each child must have at least one candy.
> - Children with a higher rating get more candies than their neighbors.
>
> Return the minimum number of candies you need to have to distribute the candies to the children.

**Example 1:**
```
Input: ratings = [1,0,2]
Output: 5
Explanation: You can allocate to the first, second, and third child with 2, 1, 2 candies respectively.
```

**Example 2:**
```
Input: ratings = [1,2,2]
Output: 4
Explanation: You can allocate to the first, second, and third child with 1, 2, 1 candies respectively.
The third child gets 1 candy because it satisfies the above two conditions.
```

**Constraints:**
- `n == ratings.length`
- `1 <= n <= 2 * 10^4`
- `0 <= ratings[i] <= 2 * 10^4`


### Video Explanation

%[https://youtu.be/OxN9ZklMQcY]
![Sketch-annotation-element-stroke-line-arrow-spiral-up.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1656783229902/L2fEwmCDd.png align="right")


### Solution

**Algorithm**

1. Create a new array of `candies` with all initial values as at least one candy will be given to all the children.
2. Now, traverse from the left of the array to the right of the array and increase the count of the candies to be given based on the rating of the neighbor child. In this iteration, we are incrementing candies count only based on the left neighbor.
3. Now, repeat the above from right to left and also store the sum.
4. Finally return the total sum of candies. 🍭 

**Code in JS 🧑‍💻 **

```
/**
 * @param {number[]} ratings
 * @return {number}
 */
var candy = function (ratings) {
  var candies = Array(ratings.length).fill(1);
  for (var i = 1; i < ratings.length; i++) {
    if (ratings[i] > ratings[i - 1]) {
      candies[i] = candies[i - 1] + 1;
    }
  }
  var sum = candies[ratings.length - 1];
  for (var i = ratings.length - 2; i >= 0; i--) {
    if (ratings[i] > ratings[i + 1]) {
      candies[i] = Math.max(candies[i], candies[i + 1] + 1);
    }
    sum += candies[i];
  }
  return sum;
};

``` 

**Time Complexity : `O(n)` **

**Space Complexity: `O(n)`**


### You can find me on the web 🌍

- [Github](https://github.com/Souravdey777)
- [LinkedIn](https://www.linkedin.com/in/souravdey777)
- [Twitter](https://twitter.com/Souravdey777)


Add your solution or approach in the comments below. Also, show your love by Sharing the blog. 🤗 

> “Life is like riding a bicycle. To keep your balance, you must keep moving.”

> – Albert Einstein

