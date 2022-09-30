## BFS vs  DFS
DFS采用递归时，使用的是栈空间，如果树或图的深度很深，则可能出现栈溢出，而BFS采用的是队列，使用堆空间，则不会出现这种情况

BFS缺点，当树的结构是矮胖时（即深度不深，但是子节点非常多），此时BFS遍历则会占用大量空间。

## BFS模板
### 注意点：在遍历时要创建一个hashset，记录已经访问过的节点，避免死循环
![image](https://user-images.githubusercontent.com/83968454/193339423-1da6ed0a-2a9b-49f2-865d-3c6ab0320d8b.png)
![image](https://user-images.githubusercontent.com/83968454/193338110-e51b1190-d3a5-4508-a72c-389b92f542bd.png)
![image](https://user-images.githubusercontent.com/83968454/193338313-b45a48cb-54f4-4776-98ed-971b1cfa9f24.png)
## BFS不分层（左）与分层（右）
区别，看题目要求，当题目有以下要求时，分层
1.最短路径
2.输出每一层的节点
![image](https://user-images.githubusercontent.com/83968454/193357994-37a5452d-80b5-4054-a2b5-e1edae10c466.png)




