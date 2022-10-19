# Note_java
java刷题笔记
![WeChat Screenshot_20221010112117](https://user-images.githubusercontent.com/83968454/194834895-9dc0fa7e-c85b-4bf7-8261-5d35f1da6f61.png)
![image](https://user-images.githubusercontent.com/83968454/194835360-8300f58e-881a-4028-b073-541947e3c9d1.png)
## 编程好习惯
访问数组之前进行下标检测，如  
```java
if( i>=2 && nums[i-2]>0)
```
## 做题小技巧
通过题目要求的时间复杂度反推使用的算法。如果有给数据范围。  
则可以通过数据范围来得知时间复杂度。面试时可以问面试官。  
如：  
10^-6 < val < 10^6 时间复杂度 O(NlogN)  
10^-8 < val < 10^8 时间复杂度应为O(N)  
### O(N)有哪些算法
双指针、单调栈、枚举  
## 考点排名
拓扑算法/BFS  
二分法  
哈希表  
双指针  
二叉查找树  
链表  
DFS  
分治法  
动态规划  
## 做的题以及日期
### 2022
### 10.10  
98.验证二叉搜索树  
https://leetcode.cn/problems/validate-binary-search-tree/  
450.删除二叉搜索树的节点（未完全理解）  
https://leetcode.cn/problems/delete-node-in-a-bst/solution/shan-chu-er-cha-sou-suo-shu-zhong-de-jie-n6vo/  
173.二叉搜索树迭代器  
https://leetcode.cn/problems/binary-search-tree-iterator/submissions/  
### 10.11  
5.最长回文子串  
https://leetcode.cn/problems/longest-palindromic-substring/submissions/   
9.回文数  
https://leetcode.cn/problems/palindrome-number/submissions/  
20.有效的括号  
https://leetcode.cn/problems/valid-parentheses/  
102.二叉树层序遍历  
https://leetcode.cn/problems/binary-tree-level-order-traversal/  
103.二叉树的锯齿行层序遍历  
https://leetcode.cn/problems/binary-tree-zigzag-level-order-traversal/submissions/  
15.三数之和  
https://leetcode.cn/problems/3sum/  
18.四数之和  
https://leetcode.cn/problems/4sum/  
976.四数之和变形LintCode（四个数在不同数组中，求四数之和为0的方案数量）
### 10.12  
看了动态规划视频  
(未做：数字三角形用动态规划实现一下)  
114.不同路径(lintcode)  
lintcode.com/problem/114  
### 10.13
新信息：华为面试中，动态规划考的比较少。可以暂时跳过  
双指针：三角形个数，没太明白。   
复习了下面的题目  
77.组合  
https://leetcode.cn/problems/combinations/  
46.全排列  
https://leetcode.cn/problems/permutations/  
47.全排列II  
https://leetcode.cn/problems/permutations-ii/  
新题  
39.组合总和  
https://leetcode.cn/problems/combination-sum/  
78.子集  
https://leetcode.cn/problems/subsets/  
90.子集II  
https://leetcode.cn/problems/subsets-ii/  
去重心得：去重前先排序。常用去重方法  
```java
if(i>0 && nums[i] == nums[i-1] && !visited[i-1]) continue;  
```  
看了N皇后问题的视频。没做题  
### 10.14  
112.路径总和  
https://leetcode.cn/problems/path-sum/  
104.二叉树最大深度  
https://leetcode.cn/problems/maximum-depth-of-binary-tree/  
### 10.15  
314.二叉树的垂序遍历(bug_free,一遍写出，大约30min)  
https://leetcode.cn/problems/binary-tree-vertical-order-traversal/  
490.迷宫（没做，早上做一下）  
https://leetcode.cn/problems/the-maze/  
### 10.16  
200.岛屿数量(dfs，bfs都做了)  
https://leetcode.cn/problems/number-of-islands/  
处理二维数组小技巧，把（x * maze[0].length + y) 将二维数组转换为integer整数，这样就能存放在Hashmap中。(其中maze是二维数组，x是row索引，从0开始,y是colum索引)  
133.克隆图（差点细节,要再做一遍） 
https://leetcode.cn/problems/clone-graph/  
752.打开转盘锁（看了题，答案看不太懂，先放着）
https://leetcode.cn/problems/open-the-lock/  
1469.lincode树上最长路径  
https://www.lintcode.com/problem/1469/  
417.太平洋大西洋水流问题（自己做，正向dfs时间185ms，击败5%。看了题解，自己做，逆向dfs，时间3ms，击败98%）  
https://leetcode.cn/problems/pacific-atlantic-water-flow/  
