# 连续子序列的最大和

## 题目

这个题目说的是，给你一个非空整数数组，你要找到和最大的连续子序列，然后返回它的和。

```
比如说，给你的数组 a 是：

2, -8, 3, -2, 4, -10

和最大的连续子序列是 3, -2, 4,  他们的和是 5。
```

## 解答

### 方法1

#### 思路

很容易发现，当前面的连续和为负数的时候应该舍弃。所以在一次遍历中不断的加上当前值，舍弃后面的值就行。


#### 复杂度

时间复杂度：O(n)

空间复杂度：O(1)
