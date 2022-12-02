## 怎么刷题
1.讲义-打卡-讲义
如果做题困难，看讲义
刷题顺序
![image](https://user-images.githubusercontent.com/83968454/203429864-26bd215a-e71a-4688-9ed9-dea9c89506a4.png)

# Note_java
java刷题笔记
![WeChat Screenshot_20221010112117](https://user-images.githubusercontent.com/83968454/194834895-9dc0fa7e-c85b-4bf7-8261-5d35f1da6f61.png)
![image](https://user-images.githubusercontent.com/83968454/194835360-8300f58e-881a-4028-b073-541947e3c9d1.png)
![image](https://user-images.githubusercontent.com/83968454/197073453-0c234cf8-3cea-4e7a-a691-634c82f3deda.png)
![image](https://user-images.githubusercontent.com/83968454/197073905-0da34a7b-b9ae-4339-a8fa-ff0e25f2a70f.png)
![image](https://user-images.githubusercontent.com/83968454/197191388-6212393f-c336-4b22-8ec9-daa52eb086a5.png)


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
### 10.20
207.课程表（拓扑排序）  
https://leetcode.cn/problems/course-schedule/  
297.二叉树的序列化与反序列化
https://leetcode.cn/problems/serialize-and-deserialize-binary-tree/  
小知识点：
方法1最快，然后是方法3，方法2最慢
```java
//方法1
StringBuilder sb = new StringBuilder();
sb.append("string");
sb.append("another string");
//方法2
String s = "string" + "another string";
//方法3
StringJoiner sj = new StringJoiner(",");//方法参数StringJoiner(分隔符，前缀符号，后缀符号);
sj.add(string);
sj.add("another string");
sj.toString();// "string,another string"
```

### 前缀和（只要题目中出现子数组，大概率可以用前缀和）  
preFix[i]  定义：前i个数的和（index为i-1），preFix[0] = 0;  
降维思想：用哈希表将两个for循环降为一个，如两数之和  
560.和为k的子数组  
https://leetcode.cn/problems/subarray-sum-equals-k/  
https://leetcode.cn/problems/QTMn0o/  
53.最大子数组和  
https://leetcode.cn/problems/maximum-subarray/  
### 10.23
复习了
297.二叉树的序列化与反序列化(BFS和DFS)  
53.最大子数组和  
207.课程表  
15.三数之和  
新题  
16.最接近的三数之和  
https://leetcode.cn/problems/3sum-closest/  
### 10.24  
277.搜寻名人（暴力解出来了，对这种题的逻辑很不擅长，要多练习）    
https://leetcode.cn/problems/find-the-celebrity/  
26.删除有序数组中的重复项  （做了1小时做出，时间复杂度O(n),1ms，双指针，核心是左右指针的移动条件）  
https://leetcode.cn/problems/remove-duplicates-from-sorted-array/     
3.无重复字符的最长子串（1h做出，一开始用集合，有特殊用例过不了，改hashmap,76ms击败10%）  
https://leetcode.cn/problems/longest-substring-without-repeating-characters/  
170.两数之和III（数据结构设计）  
https://leetcode.cn/problems/two-sum-iii-data-structure-design/  
lintcode604.滑动窗口之和  
https://www.lintcode.com/problem/604/  
11.盛最多水的容器（回忆了一下做出来了）  
https://leetcode.cn/problems/container-with-most-water/  
165.比较版本修订号(题目比较难读，编码难度不难，注意字符串split("\\."))方法若是“.”的话要转义  
https://leetcode.cn/problems/compare-version-numbers/  
### 10.26
19.删除链表的倒数第N个节点(不到20min做出)  
https://leetcode.cn/problems/remove-nth-node-from-end-of-list/  
75.颜色分类(30min，题目要求一次遍历，答案太特殊，没太钻研)  
https://leetcode.cn/problems/sort-colors/  
82.删除排序链表中的重复元素（一开始差点被绕晕，后面自己画一下清晰很多）  
https://leetcode.cn/problems/remove-duplicates-from-sorted-list-ii/  
567.字符串的排序（做的比较烦，找时间再做一下）  
https://leetcode.cn/problems/permutation-in-string/  
121买卖股票最佳时机(另一种解法，非动态规划)  
https://leetcode.cn/problems/best-time-to-buy-and-sell-stock/  
123.买卖股票最佳时机III(隔板法,力扣超时，lincode通过)  
https://www.lintcode.com/problem/151/  

### 11.03
394.字符串解码(做了一小时，解法有点忘了,还有优化空间)  
https://leetcode.cn/problems/decode-string/submissions/

### 11.22
复习了下面的题目  
77.组合  
https://leetcode.cn/problems/combinations/  
46.全排列  
https://leetcode.cn/problems/permutations/  
47.全排列II  
https://leetcode.cn/problems/permutations-ii/  
39.组合总和  
https://leetcode.cn/problems/combination-sum/  
78.子集  
https://leetcode.cn/problems/subsets/  
90.子集II  
https://leetcode.cn/problems/subsets-ii/  
112.路径总和  
https://leetcode.cn/problems/path-sum/  

### 11.23
104.二叉树最大深度  
https://leetcode.cn/problems/maximum-depth-of-binary-tree/  
695.岛屿最大面积   
https://leetcode.cn/problems/max-area-of-island/  
00.岛屿数量(dfs，bfs都做了)  
https://leetcode.cn/problems/number-of-islands/  
463.岛屿的周长  
https://leetcode.cn/problems/island-perimeter/  
133.克隆图  
https://leetcode.cn/problems/clone-graph/  
100.相同的树  
https://leetcode.cn/problems/same-tree/  
101.对称二叉树  
https://leetcode.cn/problems/symmetric-tree/  
207.课程表  
https://leetcode.cn/problems/course-schedule/  

### 11.24  
297.二叉树的序列化与反序列化（DFS做的）  
https://leetcode.cn/problems/serialize-and-deserialize-binary-tree/  
129.求根节点到叶子节点的数字之和    
https://leetcode.cn/problems/sum-root-to-leaf-numbers/  
543.二叉树的直径（答案代码看不是很懂）  
https://leetcode.cn/problems/diameter-of-binary-tree/  
662.二叉树的最大宽度（答案看不是很懂）  
https://leetcode.cn/problems/maximum-width-of-binary-tree/  
113.路径总和II  
https://leetcode.cn/problems/path-sum-ii/  
小笔记:关于二叉树的dfs搜索，判断非空有两种方法，第一个是在去往左节点之前就进行非空判断，如下所示，第二种是，去左节点之后进行非空判断，这两种方法的path的位置不一样.方法二对于二叉树dfs来说更好，简洁，也更好书写  
```java
class Solution {
    public List<List<Integer>> pathSum(TreeNode root, int targetSum) {
        
        Deque<Integer> path = new ArrayDeque<>();
        List<List<Integer>> paths = new ArrayList<>();
        if(root == null) return paths;

        path.offer(root.val);
        dfs(root ,targetSum, root.val, path , paths);

        return paths;
    }

    public void dfs(TreeNode root ,int targetSum, int curSum , Deque<Integer> path , List<List<Integer>> paths){

        if(root.left == null && root.right == null && curSum == targetSum){
            paths.add(new ArrayList<Integer>(path));
            return;
        }

        if(root.left != null){
            path.addLast(root.left.val);
            dfs(root.left , targetSum ,curSum + root.left.val , path , paths);
            path.removeLast();
        }

        if(root.right != null){
            path.addLast(root.right.val);
            dfs(root.right , targetSum ,curSum + root.right.val , path , paths);
            path.removeLast();
        }

    }
}
```
```java
class Solution {
    public List<List<Integer>> pathSum(TreeNode root, int targetSum) {
        
        Deque<Integer> path = new ArrayDeque<>();
        List<List<Integer>> paths = new ArrayList<>();
        if(root == null) return paths;
        dfs(root ,targetSum, 0, path , paths);
        return paths;
    }

    public void dfs(TreeNode root ,int targetSum, int curSum , Deque<Integer> path , List<List<Integer>> paths){

        if(root == null) return;

        curSum += root.val;
        path.offerLast(root.val);//加入路径
        if(root.left == null && root.right ==null && curSum == targetSum){
            paths.add(new ArrayList<Integer>(path));
        }

        dfs(root.left , targetSum , curSum , path , paths);
        dfs(root.right , targetSum , curSum , path , paths);

        path.removeLast();//弹出路径； 相当于当前节点左右节点遍历完之后，移除自己的值。做到了遍历与路径同步
    }
}
```
110.平衡二叉树（难度为简单）  
https://leetcode.cn/problems/balanced-binary-tree/  
98.验证二叉搜索树  
https://leetcode.cn/problems/validate-binary-search-tree/  
108.将有序数组转换为二叉搜索树（一遍过） 
https://leetcode.cn/problems/convert-sorted-array-to-binary-search-tree/  
### 11.25
111.二叉树的最小深度（难度为简单，dfs和bfs自己解出来的，bfs快很多）  
https://leetcode.cn/problems/minimum-depth-of-binary-tree/  
130.被围绕的区域  
https://leetcode.cn/problems/surrounded-regions/  
279.完全平方数（做了半个多小时，想用dfs，超时，看了解法 发现是dp或数学定理做，跳过）  
https://leetcode.cn/problems/perfect-squares/  
上午做的：9.15开始，复习1h，10：15-12：00 做三题  
下午看cs144课+做笔记，15:30开始-19：30
### 11-26
上午复习一小时后下午打球，晚上聚餐吃饭  
### 11-27
上午复习一小时，下午14.30开始到19：30，5h学习b站c++，并做笔记，把面向对象之前的都看完，记录了c++与java的区别，收获颇丰。  
晚上22：30-23：41，结构体案例。  

### 12.01
到下午晚上19：30，学完c++面向对象，做了案例，功能没实现完，也有些bug，对虚函数，父类数组创建子类对象，c++的内存操作（稍微增进了解，知道了这个部分的麻烦程度，动不动就内存被占用），以及小系统开发，有进一步的了解。  
笔记：https://github.com/steven72574/c-  
34. 在排序数组中查找元素的第一个和最后一个位置  
https://leetcode.cn/problems/find-first-and-last-position-of-element-in-sorted-array/  
心得：  
![image](https://user-images.githubusercontent.com/83968454/205183714-42f7e69e-eb93-4c36-ac83-733fe093c984.png)  
33. 搜索旋转排序数组  
https://leetcode.cn/problems/search-in-rotated-sorted-array/submissions/  
思路图解：  
![image](https://user-images.githubusercontent.com/83968454/205183657-584a9cdf-f659-44f2-97dd-0e652cc550f7.png)  
162. 寻找峰值  
https://leetcode.cn/problems/find-peak-element/  
### 12.02  
209. 长度最小的子数组(调试后一遍过)  
https://leetcode.cn/problems/minimum-size-subarray-sum/  
思路：  
![image](https://user-images.githubusercontent.com/83968454/205254618-0010e3d5-b8eb-42ea-bc46-78b53abb4a9b.png)  
剑指 Offer 04. 二维数组中的查找  
https://leetcode.cn/problems/er-wei-shu-zu-zhong-de-cha-zhao-lcof/  
35. 搜索插入位置（调试后一遍过，比较理解了，边界条件很多，注意考虑到）  
https://leetcode.cn/problems/search-insert-position/  
349.两个数组的交集（看了思路，没做）  
https://leetcode.cn/problems/intersection-of-two-arrays/  
875.875. 爱吃香蕉的珂珂（看不懂，没做）  
https://leetcode.cn/problems/koko-eating-bananas/   
611.有效三角形个数（1h，一次提交通过。排序+二分。时间使用很高，双指针没太看懂。找时间看看）  
https://leetcode.cn/problems/valid-triangle-number/submissions/   
### 双指针用同向还是双向，关键看表达式，最终目的是，双指针一个使值变大一个使值变小，才有操作空间
```java
//假设i j k 代表数组索引且i < j < k,现求
nums[k] + nums[j] > nums[i]
//则用相向双指针，因为这样的话nums[k] 和nums[i]能一个控制增加，一个控制减少.
//相向可以用while,使两双指针靠近
nums[k] - nums[j] > nums[i]
//则用同向双指针
//同向则最好用for循环，遍历j，然后用while循环移动k
```
3.无重复字符的最长子串  
https://leetcode.cn/problems/longest-substring-without-repeating-characters/  
15.三数之和（自己写的模板很不错，多复习）  
https://leetcode.cn/problems/3sum/  
