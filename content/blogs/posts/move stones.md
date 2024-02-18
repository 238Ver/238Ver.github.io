+++
title = '移除石子使总数最小'
date = 2024-02-12T17:33:05+08:00
draft = false
+++
<h1><center>移除石子</center></h1>

```python
	class Solution:

	    def minStoneSum(self, piles: List[int], k: int) -> int:
	        for i in range(k):
	            piles.sort(reverse=True)
	            piles[0] = (piles[0] + 1) // 2
	        return sum(piles)
```


## 上面的代码是对的，但是TLE
### 需要建立一个大根堆【学习堆的建立方法】
*你好 *【python解法】
**好**

$1+2 = 3$
$$
\frac {1} {2} x + 2
$$




```python
	class Solution: 
		def minStoneSum(self, piles: List[int], k: int) -> int: 
			for i in range(len(piles)): piles[i] *= -1 # 变成相反数，这样堆化后就是最大堆了 
				heapify(piles)                 # 原地堆化 
				while k and piles[0]: 
					heapreplace(piles, piles[0] // 2)  # 负数下取整等于正数上取整 
					k -= 1 
			return -sum(piles) 
		
		链接：https://leetcode.cn/problems/remove-stones-to-minimize-the-total/
```




