---
layout: post
title:  "[筆記/Leetcode in Python] 1, 7, 9"
date:   2019-07-18
description: 看Leetcode解題教學影片之學習筆記。
tags: [Leetcode]
---

* 教學影片來源：
[Michelle小梦想家- LeetCode in Python](https://www.youtube.com/playlist?list=PL2rWx9cCzU84eBz9Xfp9Rah5Fexq5yrh8)


### LeetCode in Python 1. Two Sum

#### 【法1】較慢

```python
class Solution:
	def twoSum(self, nums, target):
		
		for i in nums:
			j = target - i
			start_index = nums.index(i)
			next_index = start_index + 1
			temp_nums = nums[next_index: ]
			if j in temp_nums:
				return(nums.index(i), next_index + temp_nums.index(j))
```

#### 【法2】較快

```python
class Solution:
	def twoSum(self, nums, target):
	
	dict = {}
	
	for i in range(len(nums)):
		if target - nums[i] not in dict:
			dict[nums[i]] = i
		else:
			return [dict[target-nums[i]], i]
```


### LeetCode in Python 7. Reverse Integer

* Note:
1. 拿掉註解可以跑比較快。
2. `a//10` 比 `int(a/10)` 快。 

```python
class Solution:
	def reverse(self, x):
		num = 0
		
		a = abs(x) #取絕對值
		
		while(a != 0):
			temp = a % 10
			num = num * 10 + temp
			a = a // 10
		
		if x > 0 and num < 2147483647:
			return num
		elif x < 0 and num <= 2147483647:
			return -num
		else:
			return 0
```


### LeetCode in Python 9. Palindrome Number

```python
class Solution:
	def isPalindrom(self, x):
		num = 0
		a = abs(x)
		
		while(a != 0):
			temp = a % 10
			num = num * 10 + temp
			a = a // 10
			
		if x >= 0 and x == num:
			return True
		else:
			return False
```
