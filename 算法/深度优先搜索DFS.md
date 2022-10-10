## DFS 
### 包含剪枝，回溯，记忆化(算一种特殊的剪枝)
90%的问题是二叉树问题，10%是排列(permutation/arrangement)与组合(combination)的问题  
排列的问题：根节点下面n个分支，其中n是元素个数，每个节点下面又是n-1个分支（除了自己这个元素）以此类推，时间复杂度是O(n!)  
组合问题：每个元素有选与不选两种可能，第一层是第一个元素选或不选，第二层是第二个元素选与不选，可以形成二叉树（如下图）。  
![image](https://user-images.githubusercontent.com/83968454/193422399-b0966243-5488-4eca-a4a7-e7c3afa31927.png)

注意是任意点到任意点的路径  
一般使用递归，是比较好实现的方法。也可用迭代，但是实现难度较大。  
### 递归三要素
1.递归的定义（这个递归是实现什么目的的一个递归）  
2.递归的拆解  
3.递归的出口  
![image](https://user-images.githubusercontent.com/83968454/193412735-c126c6cb-cdc8-40a0-9984-f1aaeb50962a.png)

## 注意点
使用递归实现dfs时避免使用全局的变量path ,visited，确保函数的封装性，避免bug。

## 去重
搜索和去重基本上是同时出现的，最好的去重办法是在构造树的时候就把重复的方案去掉，减少后续遍历的时候的时间花费（可行性剪枝）。
剪枝分为两种  
1.可行性剪枝：答案不对，砍掉  
2.最优性剪枝：不是最优化答案，砍掉，一般出现在求最优结果的题目中  
![image](https://user-images.githubusercontent.com/83968454/193417979-d801d707-363d-4094-b091-49de59aa5716.png)
![image](https://user-images.githubusercontent.com/83968454/193418084-a2a86abc-546c-4a34-ab04-46f7c88ce12a.png)

## 题目
单词搜索  （推荐）
https://www.lintcode.com/problem/123/  
单词搜索II
https://www.lintcode.com/problem/132/  


### 组合题
### 排列题
https://lintcode.com/problrm/15
电话号码的数字组合 leetcode17  
![WeChat Screenshot_20221001202847](https://user-images.githubusercontent.com/83968454/193423219-9342d5c4-466c-43ca-b009-d615d9f77e42.png)
https://leetcode.cn/problems/max-area-of-island/  
https://leetcode.cn/problems/permutations-ii/  
### K数和
https://lintcode.com/problem/90  

### 帮助理解的
![WeChat Screenshot_20221001201332](https://user-images.githubusercontent.com/83968454/193422692-faa53387-bea7-4bfd-9980-43efa335f816.png)
