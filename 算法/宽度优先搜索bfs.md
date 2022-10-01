## BFS vs  DFS
DFS采用递归时，使用的是栈空间，如果树或图的深度很深，则可能出现栈溢出，而BFS采用的是队列，使用堆空间，则不会出现这种情况

BFS缺点，当树的结构是矮胖时（即深度不深，但是子节点非常多），此时BFS遍历则会占用大量空间。

Java 建议使用ArrayDeque 不建议 LinkedList 作为Queue。

DFS是找路径，bfs是找点.而找路径的时间复杂度就达到指数级别，高很多。

对于一个n*n的矩阵来说，DFS的空间复杂度可能到达O(n^2)级别（下图左），而BFS则是O(n^1/2)（下图右），即对角线
![image](https://user-images.githubusercontent.com/83968454/193414193-6599d2b3-0685-4eae-ad03-eb44ac88c257.png)

### 时间复杂度
![image](https://user-images.githubusercontent.com/83968454/193415555-30fd619f-514c-4c82-b5c4-4fc764142c12.png)



## 题目
https://leetcode.cn/problems/max-area-of-island/
## BFS模板
### 注意点：在遍历时要创建一个hashset，记录已经访问过的节点，避免死循环
![image](https://user-images.githubusercontent.com/83968454/193339423-1da6ed0a-2a9b-49f2-865d-3c6ab0320d8b.png)
### 要注意的是
在构建哈希集合hashset来记录访问过的节点时，对于数组或者类这些数据结构，哈希集合是不能有效去重，即使放进去的数组的值是相等的。因为这个时候哈希集合存放的是内存的地址。如下图，返回的值是false
![image](https://user-images.githubusercontent.com/83968454/193410941-2a8fc0a1-1bee-41d5-a8be-edb795f10daf.png)
![image](https://user-images.githubusercontent.com/83968454/193338110-e51b1190-d3a5-4508-a72c-389b92f542bd.png)
![image](https://user-images.githubusercontent.com/83968454/193338313-b45a48cb-54f4-4776-98ed-971b1cfa9f24.png)


## BFS不分层（左）与分层（右）
区别，看题目要求，当题目有以下要求时，分层
1.最短路径
2.输出每一层的节点
![image](https://user-images.githubusercontent.com/83968454/193357994-37a5452d-80b5-4054-a2b5-e1edae10c466.png)

## 练习题
![image](https://user-images.githubusercontent.com/83968454/193360842-d90f1b45-a807-44e7-97e7-c3ac3f10a5d2.png)
## 代码
![image](https://user-images.githubusercontent.com/83968454/193360935-6cfcc309-b344-4b9c-ae65-d6676be56609.png)





