## 常用数据结构的操作的时间复杂度
### 数组
查询O(1),插入O(n)  
### 链表
查询O(n),插入O(1)  
### 堆(Heap)

### 红黑树
红黑树是平衡有序二叉树，中序遍历为有序数组  
插入O(logn),删除O(logn),输出有序数组O(n)
## Java
两字符串相加时间复杂度是O(m+n),m n 分别为两个字符串的长度，他是两个字符串逐个字符加起来(即enumeration枚举)，然后形成一个新的字符串  
最好使用StringBuider来拼接，在字符串很大的时候时间复杂度不会很高  
![2](https://user-images.githubusercontent.com/83968454/192902620-d949a2a2-b5a4-4be2-9b79-c61ecb107970.png)
![image](https://user-images.githubusercontent.com/83968454/192903145-8ed28348-de47-4a65-9eac-319fb0ed6f11.png)


