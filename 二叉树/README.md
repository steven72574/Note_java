## 基础知识
子树：一个节点以及其下面所有节点加起来  
叶子节点也算一个子树  
有几个节点就有几个子树  
前中后序说的是根的位置  
![WeChat Screenshot_20221002200423](https://user-images.githubusercontent.com/83968454/193469031-a8f3f02d-d047-48e0-894c-b11e68776fce.png)

![WeChat Screenshot_20221002201004](https://user-images.githubusercontent.com/83968454/193469265-9e8bfc18-c490-4aa6-9a4a-5ad8447e1442.png)
![WeChat Screenshot_20221002201132](https://user-images.githubusercontent.com/83968454/193469329-b7071ab9-8e41-42a7-8180-cbcbdd6d51e8.png)

## 二叉树考点
1.二叉树上求值，求路径  
2.二叉树结构变化  
3.二叉查找树  
以上三种都是dfs

## 经典题目
LCA最近公共祖先
lintcode.com/problem/474

## BST(BinarySearchTree)二叉搜索树
左节点值<根节点值<右节点值
二叉搜索树的中序遍历是一个不下降序列链表
值相等的情况一般不考虑，也可能相等值在左边也可能在右边，得看题目要求
### 练习  
![WeChat Screenshot_20221003225746](https://user-images.githubusercontent.com/83968454/193681178-e0fd8673-bfc5-4632-9d8a-e759fc9457d6.png)

### 二叉树序列化
使用场景  
1.把内存中数据存储到硬盘中  
2.网络传输时  
例子  
![WeChat Screenshot_20221013234435](https://user-images.githubusercontent.com/83968454/195716801-a7e25cdd-31e5-4a43-826e-2347f5272eb5.png)

## 红黑树
红黑树是一个平衡的BST
java 里面是treemap/treeset
### 应用  
在logN 时间内执行下面操作：  
1.增删查改数据
2.寻找最大最小
3.查找比某个数小的最大值和比某个数大的最小值

