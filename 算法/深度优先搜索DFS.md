## DFS
注意是任意点到任意点的路径  
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
https://leetcode.cn/problems/permutations-ii/

