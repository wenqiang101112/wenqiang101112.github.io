---
layout: post
title: 算法知识总结
category: algorithm
tags: [algorithm]
---

算法资料收集、知识总结

## 参考资料
- [Leetcode算法](http://www.leetcodecn.com/)  
- [LeetCode Cookbook](https://books.halfrost.com/leetcode/)
- [https://github.com/halfrost/LeetCode-Go](https://github.com/halfrost/LeetCode-Go)    

## 一、算法复杂度：
指算法在编写成可执行程序后，运行时所需要的资源，资源包括时间资源和内存资源；

### 1.1.时间复杂度
（1）时间频度
- 一个算法执行所耗费的时间，从理论上是不能算出来的，必须上机运行测试才能知道。
- 一个算法花费的时间与算法中语句的执行次数成正比例。
- 一个算法中的语句执行次数称为语句频度或时间频度。记为T(n)。

算法的时间复杂度是指执行算法所需要的计算工作量。
    
（2）时间复杂度  
在刚才提到的时间频度中，n称为问题的规模，当n不断变化时，时间频度T(n)也会不断变化。  
但有时我们想知道它变化时呈现什么规律。为此，我们引入时间复杂度概念。
    
一般情况下，算法中基本操作重复执行的次数是问题规模n的某个函数，用T(n)表示  ，  
若有某个辅助函数f(n),存在一个正常数c使得fn*c>=T(n)恒成立。记作T(n)=O(f(n)),  
称O(f(n)) 为算法的渐进时间复杂度，简称时间复杂度。
    
在各种不同算法中，若算法中语句执行次数为一个常数，则时间复杂度为O(1),  
在时间频度不相同时，时间复杂度有可能相同，如T(n)=n^2+3n+4与T(n)=4n^2+2n+1它们的频度不同，但时间复杂度相同，都为O(n^2)。
    
按数量级递增排列，常见的时间复杂度有：
- 常数阶O(1),
- 对数阶O(log2n)(以2为底n的对数，下同)
- 线性阶O(n),
- 线性对数阶O(nlog2n),
- 平方阶O(n^2)，立方阶O(n^3),...，
- k次方阶O(n^k),
- 指数阶O(2^n)

随着问题规模n的不断增大，上述时间复杂度不断增大，算法的执行效率越低

### 1.2.空间复杂度
与时间复杂度类似，空间复杂度是指算法在计算机内执行时所需存储空间的度量。记作:S(n)=O(f(n))  
算法执行期间所需要的存储空间包括3个部分：
- 算法程序所占的空间；
- 输入的初始数据所占的存储空间；
- 算法执行过程中所需要的额外空间。  

在许多实际问题中，为了减少算法所占的存储空间，通常采用压缩存储技术。

![](https://wdsheng0i.github.io/assets/images/2021/alg/1.png)

![](https://wdsheng0i.github.io/assets/images/2021/alg/2.png)  

## 二、常见算法
### 2.1 搜索算法
#### 顺序查找

#### 二分查找

#### 哈希(HASH)查找

#### 深度优先遍历查找(图)

### 2.2 排序算法
#### 插入排序(直接插入排序、希尔排序)

#### 选择排序(直接选择排序、堆排序)

#### 交换排序(冒泡排序、快速排序)

#### 归并排序

### 2.3 递归算法

### 2.4 递推算法

### 2.5 暴力求解算法(穷举法)

### 2.6 分治算法

### 2.7 动态规划算法

### 2.8 贪心算法

### 2.9 分支界定

### 2.10 回溯法：
八皇后问题
    

### 2.11 图论模型与算法
最小生成树 
 
最短路径问题