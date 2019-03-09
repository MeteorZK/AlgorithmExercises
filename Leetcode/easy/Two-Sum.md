---
layout: post
title: "Two Sum"
date: 2019-3-9 11:04:48
toc: 2
comments: true
tags: 
	- Leetcode easy
---

[Two-Sum](http://pnudcwmmo.bkt.clouddn.com/image/LeetCode/Two-Sum.png)
```
class Solution {
    public int[] twoSum(int[] nums, int target) {
        int[] result = new int[2];
        Map<Integer,Integer> map = new HashMap<>();
        for(int i = 0; i < nums.length; i++){
            if(map.containsKey(target - nums[i])){
                result[0] = map.get(target - nums[i]);
                result[1] = i;
                return result;
            }
            map.put(nums[i],i);
        }
        return result;
    }
}
```