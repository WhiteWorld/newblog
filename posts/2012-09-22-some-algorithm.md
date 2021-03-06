date: 2012-09-22
layout: post
title: "算法记录"
description: 
category: "学习"
tags: [Algorithm]
published: true

图算法
------
### 最短路径
- Dijkstra  
	+ 单源最短路径算法,算法解决了有向图中单个源点到其他顶点的最短路径问题   
	+ 适用条件，有向图（无向图），所有边的权为非负  
	+ 时间复杂度O( N^2 ) 
- SPFA  
	+ Shortest Path Faster Algorithm,单源最短路径算法
	+ 代码简单，可计算负权
	+ 本质是Bellman-Ford算法的优化
	+ ....
- Bellman-Ford  
	+ 求含负权图的单源最短路径算法,主要思想是“松弛”
	+ 实现时可以把边为单位考虑，外层循环是v-1次，内层是E次
	+ 时间复杂度O(VE)

* Floyd-Warshall  
	+ 解决任意两点间的最短路径的一种算法
	+ 可以正确处理有向图或负权的最短路径问题
	+ 原理是动态规划
	+ 时间复杂度O( N^3 ) 空间复杂度O( N^2 ),编码时注意三重循环的次序
	+ 空间压缩为2维后的代码可以这样理解：内层的i、j从k=1开始，计算i和j点中间经过最多k个点（这k个点是从1开始递加到k的）的最短路径，dis[][]数组保存了当前k结束后的最短路径直，可供下次（第k+1次）直接使用。
	
