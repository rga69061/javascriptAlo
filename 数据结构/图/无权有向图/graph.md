# 图

## 什么是图

边和顶点的集合

## 图应该有哪些操作

1. 添加边
2. 删除边
3. 深度优先遍历
4. 广度优先遍历
5. 查找最短路径
6. 最小生成树
7. 拓扑排序

图的顶点和边上都可以扩展很多的数据信息。写算法需要实现大的框架，在实际中再灵活发挥。


## 图的表示有邻接表和邻接矩阵。应该怎么选择？

> 邻接矩阵是一个二位数组。从数学上来看，邻接矩阵的x轴y轴都是节点。假设用a标准邻接矩阵，那么`a[vi][vj] == 1`表示这两个节点相连。为0表示不相连。


### 邻接矩阵的优缺点

1. 缺点

    1. 浪费空间—— 存稀疏图（点很多而边很少）有大量无效元素
    2. 对稠密图（特别是完全图）还是很合算的
    3. 浪费时间—— 统计稀疏图中一共有多少条边
    
2. 优点  

    1. 方便计算任一顶点的“度”（从该点发出的边数为“出度”，指向该点的边数为“入度”）无向图：对应行（或列）非0元素的个数。有向图：对应行非0元素的个数是“出度”；对应列非0元素的个数是“入度”


> 邻接表是一个对象，对象的key存储着每一个节点。对应的value是与节点相连的节点。

1. 优点

    1. 节约稀疏图的空间
    2. 方便计算任一顶点的“度”？：对无向图：是的，对有向图只能计算出度，
    
2. 缺点    

    1. 对有向图，需要构造“逆邻接表”计算入度。


## 深度优先搜索和广度优先搜索

深度优先和广度优先的本质就体现在名称上。从实现上来说都是递推，只是**递归的时机不同**。

## 最小生成树

1. https://www.cnblogs.com/biyeymyhjob/archive/2012/07/30/2615542.html

