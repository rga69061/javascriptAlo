# 没有重复字符的最长子串

## 题目

这个题目说的是，给你一个字符串，你要找到没有重复字符的最长子串，然后返回它的长度。

```
比如说给你的字符串 s 是：

abcabcbb

没有重复字符的最长子串是 abc，这里再往下的字符是 a，和前面这个 a 重复了。

后面满足条件的子串还有 bca，cab，abc 等，不过它们的长度都是 3 ，因此返回的长度为 3。

再比如说 ddd，没有重复字符的最长子串就是一个 d，因此你要返回的长度是 1。
```

## 方法

### 方法1

#### 思路

暴力找到所有的子字符串。然后判断

#### 复杂度

时间复杂度: 两层循环O(n^2)

空间复杂度: 需要存储所有的子字符串O(n^2)

### 方法2

#### 思路

滑动窗口。用两个小标作为窗口,滑动。遇到重复则后面的下标前进，否则前面的下标前进。
（这个方法的优化就是在遇到重复的时候将下标移动到重复的字符串的后一位，需要保存每一个字符串的出现位置）

#### 复杂度

时间复杂度：O(n), 遍历一次

空间复杂度：最坏O(n)


