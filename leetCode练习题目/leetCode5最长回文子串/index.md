# 最长回文子串

## 题目

这个题目说的是，给你一个字符串，你要在它所有的回文子串中，找到长度最长的子串，并返回它。

```
比如说，给你的字符串是：

abcbab

你要返回的最长回文子串是：

abcba
```

## 方法

### 方法1

#### 思路

暴力方法。找到所有的子串。判断是否回文，然后找到最长的回文子串

#### 复杂度

时间复杂度：O(n^3)。找到所有的子串，然后找回文。就是n^3。

空间复杂度：最坏O(n^2)。所有的子串都是回文字符串

### 方法2

#### 思路

动态规划：

假设s(i,j)表示从下标i到下标j是否回文。

1. 当i=j的时候肯定回文
2. 当i=j-1的时候charAt(i) = charAt(j)则回文
3. 当i<j-1的时候s(i,j) = s(i-1,j-1) && (charAt(i)===charAt(j))

#### 复杂度

时间复杂度：O(n^2) 需要两层循环

空间复杂度：O(n^2) 需要一个二维数组

### 方法3

#### 思路

用字符串"ababa"为例。

以第二个字符a。为中心向两边扩展。如果两边相等，那么就是回文子字符串。利用这种方法。可以找到所有的回文子字符串。

其中需要注意的是字符长度是奇数还是偶数的区别

#### 复杂度

时间复杂度：O(n^2)。还是需要两层循环

空间复杂度：O(1)。不需要多余的数据结构


### 方法4

#### 思路

Manacher算法

#### 复杂度

时间复杂度：O(n)
