# Two Sum

Given an array of integers, return **indices** of the two numbers such that they add up to a specific target.

You may assume that each input would have **exactly** one solution, and you may not use the same element twice.

**Example:**

Given nums = [2, 7, 11, 15], target = 9,

Because nums[0] + nums[1] = 2 + 7 = 9,
return [0, 1].

# 两数之和

给定一个整数数组和一个目标值，找出数组中和为目标值的两个数。

你可以假设每个输入只对应一种答案，且同样的元素不能被重复利用。

**示例**

给定 nums = [2, 7, 11, 15], target = 9

因为 nums[0] + nums[1] = 2 + 7 = 9
所以返回 [0, 1]

## JavaScript
```
/**
 * @param {number[]} nums
 * @param {number} target
 * @return {number[]}
 */
var twoSum = function(nums, target) {
    for(var i=0;i<nums.length;i++) {
        for(var j= i+1; j<nums.length; j++) {
            if(nums[i] + nums[j] == target) {
                return [i,j]
            } 
        }
    }
};
```

## Java
```
class Solution {
    public int[] twoSum(int[] nums, int target) {
        int[] sum = new int[2];
        for(int i=0;i<nums.length;i++) {
            for(int j= i+1; j<nums.length; j++) {
                if(nums[i] + nums[j] == target) {
                    sum[0] = i;
                    sum[1] = j;
                } 
            }
        }
        return sum;
    }
}
```

## 思路
暴力循环数组，n*(n-1)的方式进行遍历。一旦找到后返回。