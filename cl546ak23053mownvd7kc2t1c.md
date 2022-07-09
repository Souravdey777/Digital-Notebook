## LeetCode Question - 1710. Maximum Units on a Truck 🚛

### About the Series

Problem-solving is a key skill set for any tech-related stuff you might be working on.

When it comes to developers it's one of the most crucial skills which is needed in almost any day-to-day code you might be writing.

So, this series of blogs is all about practicing Daily LeetCode Challenges & Problem-solving. 🚀

### Problem Statement 

[**Maximum Units on a Truck 🚛**](https://leetcode.com/problems/maximum-units-on-a-truck)


> You are assigned to put some amount of boxes onto one truck. You are given a 2D array ``boxTypes``, where ``boxTypes[i] = [numberOfBoxesi, numberOfUnitsPerBoxi]``:
> 
> - ``numberOfBoxes`` is the number of boxes of type i.
> - ``numberOfUnitsPerBox`` is the number of units in each box of type i.
> You are also given an integer ``truckSize``, which is the maximum number of boxes that can be put on the truck. You can choose any boxes to put on the truck as long as the number of boxes does not exceed ``truckSize``.
> 
> Return the maximum total number of units that can be put on the truck.
>

### Video Explanation


%[https://youtu.be/mx1Z7PszOkU]
![Sketch-annotation-element-stroke-line-arrow-spiral-up.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1656783229902/L2fEwmCDd.png align="right")



### Solution

**Algorithm**

1. Sorting the array in descending order based on the no. of units in each box. 📦 
2. Iterate through the sorted array elements and check the remaining ``truckSize``.
    - If not enough size for all boxes take as many boxes as you can and calculate the total units
    - Else take all the boxes and calculate the total units.
3. Return the total units 



**Code 🧑‍💻 **

```
var maximumUnits = function (boxTypes, truckSize) {
  boxTypes.sort((a, b) => b[1] - a[1]);

  var maxTotal = 0;
  var i = 0;

  while (truckSize > 0 && i < boxTypes.length) {
    const numOfBoxes = boxTypes[i][0];
    const numOfUnits = boxTypes[i][1];

    if (truckSize <= numOfBoxes) {
      maxTotal += truckSize * numOfUnits;
      truckSize = 0;
    } else {
      maxTotal += numOfBoxes * numOfUnits;
      truckSize -= numOfBoxes;
    }

    i++;
  }
  return maxTotal;
};
``` 

**Time Complexity : O(nlogn)+O(n) = O(nlogn) **

**Space Complexity: O(1)**



### Similar Questions for practice

Now it is time to try more similar questions

- [Maximum Bags With Full Capacity of Rocks](https://leetcode.com/problems/maximum-bags-with-full-capacity-of-rocks/)


### You can find me on the web 🌍

- [Github](https://github.com/Souravdey777)
- [LinkedIn](https://www.linkedin.com/in/souravdey777)
- [Twitter](https://twitter.com/Souravdey777)


Add your solutions or approaches to the comments. 

Show your love by Sharing the blog. 🤗 


> "I didn't fail 1000 times. The light bulb was an invention with 1000 steps."

> ~Thomas A. Edison


