# LeetCode
文档用于存储平日所练习LeetCode题目的代码和思考方法，记录日常学习~

## 程序设计基本内容

- [C++\Java程序设计基础内容](https://github.com/staer-tan/LeetCode/blob/master/***C%2B%2B%5CJava%E5%9F%BA%E7%A1%80%E5%86%85%E5%AE%B9.md)

## 未来基础进阶

- 数组排序：快速排序、插入排序、堆排序等。非常重要，在对数组进行操作时，对数组首先进行排序，将减少复杂度和运算量。

- 查找（搜索）算法：二分查找、插值查找、红黑树等。

- Hash表的使用：典型的以空间换时间，速度很快。值得深入思考

- 动态规划：0-1背包问题，迪杰斯特拉算法，贪心算法等。

- 图遍历算法：(1) [二叉树的深度优先及广度优先遍历](https://github.com/staer-tan/LeetCode/blob/master/%E4%BA%8C%E5%8F%89%E6%A0%91%E7%9A%84%E6%B7%B1%E5%BA%A6%E4%B8%8E%E5%B9%BF%E5%BA%A6%E4%BC%98%E5%85%88%E6%90%9C%E7%B4%A2.md), (2) 二叉树的前中后序遍历及其扩展, (3) [图的深度优先广度优先搜索算法](https://github.com/staer-tan/LeetCode/blob/master/%E4%B8%AD%E7%BA%A7/*200.%20%E5%B2%9B%E5%B1%BF%E6%95%B0%E9%87%8F.md)。

- 图算法进阶：

(1)最短路径 — 生成节点之间的最短路径

① Dijkstra（单源/有向图）：生成的是某个起始点到图中其他节点的最短距离表（数组）

② Floyd（全源/无向图）：生成图中所有节点到其他节点的最短距离表（数组） 

(2) 最小生成树(无向图/双向图) — 生成一个权值最小的树

① prim：(注意：Prim与Dijkstra算法思想几乎完全相同，区别在于最短距离是顶点针对于“起点”，还是“集合”)

② kruskal：每次选择图中最小边权的边，如果边两端的顶点在不同的连通块种，则把这条边加入最小生成树中。

## 重点题型

#### 1. 数组

##### <基础>
- [28. 实现 strStr() -- 字符串匹配算法(KMP)](https://github.com/staer-tan/LeetCode/blob/master/28.%20%E5%AE%9E%E7%8E%B0%20strStr().md)

- [66. 加一 -- 矢量数组的综合应用](https://github.com/staer-tan/LeetCode/blob/master/66.%20%E5%8A%A0%E4%B8%80.md)

- [125. 验证回文串 -- 字符串的特殊处理](https://github.com/staer-tan/LeetCode/blob/master/125.%E9%AA%8C%E8%AF%81%E5%9B%9E%E6%96%87%E4%B8%B2.md)

- [189. 旋转数组 -- 数组的综合运用](https://github.com/staer-tan/LeetCode/blob/master/189.%20%E6%97%8B%E8%BD%AC%E6%95%B0%E7%BB%84.md)

- [283. 移动零 -- 设置数组指针的计算](https://github.com/staer-tan/LeetCode/blob/master/283.%20%E7%A7%BB%E5%8A%A8%E9%9B%B6.md)

- [350. 两个数组的交集 II -- Hash表的应用](https://github.com/staer-tan/LeetCode/blob/master/*350.%20%E4%B8%A4%E4%B8%AA%E6%95%B0%E7%BB%84%E7%9A%84%E4%BA%A4%E9%9B%86%20II.md)

##### <进阶>
- [5. 最长回文串 -- 字符串匹配提升](https://github.com/staer-tan/LeetCode/blob/master/%E4%B8%AD%E7%BA%A7/*5.%20%E6%9C%80%E9%95%BF%E5%9B%9E%E6%96%87%E5%AD%90%E4%B8%B2.md)

- [15. 三数之和 -- 数组三个元素操作的提升](https://github.com/staer-tan/LeetCode/blob/master/%E4%B8%AD%E7%BA%A7/15.%20%E4%B8%89%E6%95%B0%E4%B9%8B%E5%92%8C.md)

- [33. 搜索旋转排序数组 -- 二分查找的进阶应用](https://github.com/staer-tan/LeetCode/blob/master/%E4%B8%AD%E7%BA%A7/*33.%20%E6%90%9C%E7%B4%A2%E6%97%8B%E8%BD%AC%E6%8E%92%E5%BA%8F%E6%95%B0%E7%BB%84.md)

- [49. 字母异位词分组 -- hash表和二维数组的综合应用(重要)](https://github.com/staer-tan/LeetCode/blob/master/%E4%B8%AD%E7%BA%A7/*49.%20%E5%AD%97%E6%AF%8D%E5%BC%82%E4%BD%8D%E8%AF%8D%E5%88%86%E7%BB%84.md)

- [347. 前K个高频元素 -- 最大堆和map的综合应用（重要）](https://github.com/staer-tan/LeetCode/blob/master/%E4%B8%AD%E7%BA%A7/*347.%20%E5%89%8D%20K%20%E4%B8%AA%E9%AB%98%E9%A2%91%E5%85%83%E7%B4%A0.md)

#### 2. 字符串（链表）
- [19. 删除链表的倒数第N个节点 -- 删除链表节点的重要习题](https://github.com/staer-tan/LeetCode/blob/master/*19.%20%E5%88%A0%E9%99%A4%E9%93%BE%E8%A1%A8%E7%9A%84%E5%80%92%E6%95%B0%E7%AC%ACN%E4%B8%AA%E8%8A%82%E7%82%B9.md)

- [21. 合并两个有序链表 -- 指针的综合运用(offer)](https://github.com/staer-tan/LeetCode/blob/master/*21.%20%E5%90%88%E5%B9%B6%E4%B8%A4%E4%B8%AA%E6%9C%89%E5%BA%8F%E9%93%BE%E8%A1%A8.md)

- [148. 排链表 -- 链表排序重要题型（多种链表操作综合应用）（重要）](https://github.com/staer-tan/LeetCode/blob/master/中级/**148.%20排序链表.md)

- [206. 反转链表 -- 多种方法对字符串的操作(offer)](https://github.com/staer-tan/LeetCode/blob/master/*206.%20%E5%8F%8D%E8%BD%AC%E9%93%BE%E8%A1%A8.md)

#### 3. 二叉树（树）

##### <基础>

- [98. 验证二叉搜索树 -- 中序遍历的深入扩展](https://github.com/staer-tan/LeetCode/blob/master/*98.%20%E9%AA%8C%E8%AF%81%E4%BA%8C%E5%8F%89%E6%90%9C%E7%B4%A2%E6%A0%91.md)

- [101. 验证对称二叉树 -- 二叉树递归、迭代算法使用I(offer)](https://github.com/staer-tan/LeetCode/blob/master/*98.%20%E9%AA%8C%E8%AF%81%E4%BA%8C%E5%8F%89%E6%90%9C%E7%B4%A2%E6%A0%91.md)

- [102. 二叉树的层次遍历 -- 二叉树递归、迭代算法使用II（重要）](https://github.com/staer-tan/LeetCode/blob/master/*102.%20%E4%BA%8C%E5%8F%89%E6%A0%91%E7%9A%84%E5%B1%82%E6%AC%A1%E9%81%8D%E5%8E%86.md)

- [108. 将有序数组转换为二叉搜索树 -- 二叉树递归 + 二分法结合](https://github.com/staer-tan/LeetCode/blob/master/*108.%20%E5%B0%86%E6%9C%89%E5%BA%8F%E6%95%B0%E7%BB%84%E8%BD%AC%E6%8D%A2%E4%B8%BA%E4%BA%8C%E5%8F%89%E6%90%9C%E7%B4%A2%E6%A0%91.md)

##### <进阶>

- [94. 二叉树的中序遍历 -- 二叉树遍历算法应用（重要）](https://github.com/staer-tan/LeetCode/blob/master/%E4%B8%AD%E7%BA%A7/*94.%20%E4%BA%8C%E5%8F%89%E6%A0%91%E7%9A%84%E4%B8%AD%E5%BA%8F%E9%81%8D%E5%8E%86.md)

- [105. 从前序与中序遍历序列构造二叉树 -- 二叉树递归 + 设置双指针结合（重要）](https://github.com/staer-tan/LeetCode/blob/master/%E4%B8%AD%E7%BA%A7/*105.%20%E4%BB%8E%E5%89%8D%E5%BA%8F%E4%B8%8E%E4%B8%AD%E5%BA%8F%E9%81%8D%E5%8E%86%E5%BA%8F%E5%88%97%E6%9E%84%E9%80%A0%E4%BA%8C%E5%8F%89%E6%A0%91.md)

- [116. 填充每个节点的下一个右侧节点指针 -- 双指针构建完美二叉树next指针](https://github.com/staer-tan/LeetCode/blob/master/%E4%B8%AD%E7%BA%A7/*116.%20%E5%A1%AB%E5%85%85%E6%AF%8F%E4%B8%AA%E8%8A%82%E7%82%B9%E7%9A%84%E4%B8%8B%E4%B8%80%E4%B8%AA%E5%8F%B3%E4%BE%A7%E8%8A%82%E7%82%B9%E6%8C%87%E9%92%88.md)

- [208. 实现Trie(前缀树) -- 前缀树的建立和相关指针综合操作](https://github.com/staer-tan/LeetCode/blob/master/%E4%B8%AD%E7%BA%A7/*208.%20%E5%AE%9E%E7%8E%B0%20Trie%20(%E5%89%8D%E7%BC%80%E6%A0%91).md)

- [236. 二叉树的最近公共祖先 -- 二叉树的递归法求解的经典例题](https://github.com/staer-tan/LeetCode/blob/master/%E4%B8%AD%E7%BA%A7/*238.%20%E9%99%A4%E8%87%AA%E8%BA%AB%E4%BB%A5%E5%A4%96%E6%95%B0%E7%BB%84%E7%9A%84%E4%B9%98%E7%A7%AF.md)

#### 4. 哈希与映射（hash表和图）

- [146. LRU缓存机制.md -- hash表和双向链表的结合（非常重要!）](https://github.com/staer-tan/LeetCode/blob/master/%E4%B8%AD%E7%BA%A7/**146.%20LRU%E7%BC%93%E5%AD%98%E6%9C%BA%E5%88%B6.md)

#### 5. 图

图的基本算法知识在上方简介中有提及，本节将推广更多关于图的应用

- [207. 课程表I & 210. 课程表 II -- 拓扑图的广度优先搜索（基于队列迭代方法）](https://github.com/staer-tan/LeetCode/blob/master/%E4%B8%AD%E7%BA%A7/*207.%20%E8%AF%BE%E7%A8%8B%E8%A1%A8%20I%20&%20210.%20%E8%AF%BE%E7%A8%8B%E8%A1%A8%20II.md)

#### 6. 动态规划

定义：采用分治思想，利用它可以实现时间复杂度的优化（也具备以空间换时间的特点）。

动态规划三个最重要的概念：最优子结构、边界、状态转移公式

经典介绍例题：[70. 爬楼梯](https://github.com/staer-tan/LeetCode/blob/master/70.%20%E7%88%AC%E6%A5%BC%E6%A2%AF.md)

- [53. 最大子序和 -- 动态规划的经典应用(offer)](https://github.com/staer-tan/LeetCode/blob/master/*53.%20%E6%9C%80%E5%A4%A7%E5%AD%90%E5%BA%8F%E5%92%8C.md)

- [139. 单词拆分 -- 动态规划的分治分支应用](https://github.com/staer-tan/LeetCode/blob/master/%E4%B8%AD%E7%BA%A7/*139.%20%E5%8D%95%E8%AF%8D%E6%8B%86%E5%88%86.md)

- [152. 乘积最大子序列 -- 动态规划的进阶（注意与53.最大子序和比较）](https://github.com/staer-tan/LeetCode/blob/master/%E4%B8%AD%E7%BA%A7/*152.%20%E4%B9%98%E7%A7%AF%E6%9C%80%E5%A4%A7%E5%AD%90%E5%BA%8F%E5%88%97.md)

- [279. 完全平方数 -- 动态规划的数组（链表法）的应用](https://github.com/staer-tan/LeetCode/blob/master/%E4%B8%AD%E7%BA%A7/*279.%20%E5%AE%8C%E5%85%A8%E5%B9%B3%E6%96%B9%E6%95%B0.md)

- [322. 零钱兑换 -- 动态规划的自底向上的经典试题](https://github.com/staer-tan/LeetCode/blob/master/%E4%B8%AD%E7%BA%A7/*322.%20%E9%9B%B6%E9%92%B1%E5%85%91%E6%8D%A2.md)

- [329. 矩阵中的最长递增路径 -- 动归与DFS算法基于通过额外空间的使用（重要）](https://github.com/staer-tan/LeetCode/blob/master/%E4%B8%AD%E7%BA%A7/**329.%20%E7%9F%A9%E9%98%B5%E4%B8%AD%E7%9A%84%E6%9C%80%E9%95%BF%E9%80%92%E5%A2%9E%E8%B7%AF%E5%BE%84.md)

#### 7. 递归法
##### <回溯法>

- [131. 分割回文串 -- 回溯法在字符串经典应用（分层的思想）](https://github.com/staer-tan/LeetCode/blob/master/%E4%B8%AD%E7%BA%A7/*131.%20%E5%88%86%E5%89%B2%E5%9B%9E%E6%96%87%E4%B8%B2)

#### 数学与其他

- [13. 罗马数字转成整数 -- 一道优秀的技巧题 ](https://github.com/staer-tan/LeetCode/blob/master/13.%20%E7%BD%97%E9%A9%AC%E6%95%B0%E5%AD%97%E8%BD%AC%E6%95%B4%E6%95%B0.md)

- [50. Pow(x,n)](https://github.com/staer-tan/LeetCode/blob/master/%E4%B8%AD%E7%BA%A7/*50.%20Pow(x%2C%20n))，[69. x的平方根 -- 两道关于数学运算递归和二分求解的应用](https://github.com/staer-tan/LeetCode/blob/master/%E4%B8%AD%E7%BA%A7/*69.%20x%20%E7%9A%84%E5%B9%B3%E6%96%B9%E6%A0%B9.md)

- [118. 杨辉三角 -- 二维矢量数组的使用](https://github.com/staer-tan/LeetCode/blob/master/118.%20%E6%9D%A8%E8%BE%89%E4%B8%89%E8%A7%92.md)

- [169. 求众数 -- 标记指针的灵活运用减少时间复杂度(与347可相比较)](https://github.com/staer-tan/LeetCode/blob/master/%E4%B8%AD%E7%BA%A7/*169.%20%E6%B1%82%E4%BC%97%E6%95%B0.md)

- [190|191|461. 二进制算法综合 -- 关于二进制的简单考察](https://github.com/staer-tan/LeetCode/blob/master/190%7C191%7C461.%20%E4%BA%8C%E8%BF%9B%E5%88%B6%E7%AE%97%E6%B3%95%E7%BB%BC%E5%90%88.md)
