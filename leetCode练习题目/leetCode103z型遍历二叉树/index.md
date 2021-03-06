# z型遍历二叉树

给定一个二叉树，返回其节点值的锯齿形层次遍历。（即先从左往右，再从右往左进行下一层遍历，以此类推，层与层之间交替进行）。

例如：
给定二叉树 [3,9,20,null,null,15,7],

```
    3
   / \
  9  20
    /  \
   15   7
```

返回锯齿形层次遍历如下：

```
[
  [3],
  [20,9],
  [15,7]
]
```

## 方案1

利用广度优先遍历。将每一层分隔在不同的数组里。在遍历的同时，根据二叉树的层数，来决定是反向还是正向的将这一层数据加到结果中去。

时间复杂度：O(2n)，因为在遍历的同时，还需要将结果放到数组中去。

空间复杂度：O(n)，很广度优先遍历相同




