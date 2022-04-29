---
layout: post
title: 数据结构知识总结
category: data-struct
tags: [data-struct]
---

数据结构资料收集、知识总结

## 参考资料
- [这里分享一个数据可视化的网站](https://www.cs.usfca.edu/~galles/visualization/Algorithms.html)  
- [TreeMap详解可以参考](https://www.jianshu.com/p/2dcff3634326)    

## 一、概述
- 逻辑结构：
是对操作对像的数学描述，描述的是数据元素之间的逻辑关系。如，"线性结构，树形结构，图状结构"。
    - 线性结构：数据元素之间仅有线性关系，每个数据元素只有一个直接前驱和一个直接后继
    - 树形结构：数据元素之间有明显的层次关系，并且每一层上的数据元素可能和下一层中多个元素（即其孩子结点）相关，但只能和上一层中一个元素（即其父亲结点）相关
    - 图形结构：结点之间的关系可以是任意的，图中任意两个数据元素之间都可能相关 
- 物理结构(存储结构)：
又称存储结构，是数据结构在计算机中的表示（又称映像）。例如，"数组，指针"  
![](https://note.youdao.com/yws/public/resource/e219b21c411784c8d8bf1bec5bb6f26d/xmlnote/WEBRESOURCE19b204b26c2218c8c5b5ded49d91a4b9/46730)

## 二、常见数据结构
### 1.数组(Arrays)：
数组就是相同数据类型的元素按一定顺序排列的集合。  
一句话：就是物理上存储在一组连续的地址上。也称为数据结构中的物理结构。

#### 1.1.有序数组：

#### 1.2.静态数组：

#### 1.3.动态数组(Vector)：

### 2.线性表(ArrayList)：
线性表中数据元素之间的关系是一对一的关系，即除了第一个和最后一个数据元素之外，其它数据元素都是首尾相接的。  
一句话：线性表是数据结构中的逻辑结构。可以存储在数组上，也可以存储在链表上。  
![](https://note.youdao.com/yws/public/resource/e219b21c411784c8d8bf1bec5bb6f26d/xmlnote/WEBRESOURCE4a5edbd659a1f8c85328f305112f497a/46530)

#### 2.1.顺序表： 
线性表的结点按逻辑次序依次存放在一组地址连续的存储单元里的方法。用顺序存储方法存储的线性表简称为顺序表。   
![](https://note.youdao.com/yws/public/resource/e219b21c411784c8d8bf1bec5bb6f26d/xmlnote/WEBRESOURCEb5d98f885e9b504b4a73ee11d745d4b6/46525)

#### 2.2.链表(物理结构指针)(LinkedList)：
链表是一种物理存储单元上非连续、非顺序的存储结构，数据元素的逻辑顺序是通过链表中的指针链接次序实现的

#### 2.3.单链表：
在每个结点中除包含数据域外，只设置一个指针域用以指向其直接后继结点，这种构成的链接表称为线性单向链接表，简称单链表  
![](https://note.youdao.com/yws/public/resource/e219b21c411784c8d8bf1bec5bb6f26d/xmlnote/WEBRESOURCEc1cd53f269e105717f680d0b2d087e91/46527)

#### 2.4.双链表：
在每个结点中除包含数值域外，设置两个指针域，分别用以指向直接前驱结点和直接后继结点，这样构成的链接表称为线性双向链接表，简称双链表。  
![](https://note.youdao.com/yws/public/resource/e219b21c411784c8d8bf1bec5bb6f26d/xmlnote/WEBRESOURCE54709cba06332c93a493de134ff2a28a/46526)

#### 2.5.循环链表：
![](https://note.youdao.com/yws/public/resource/e219b21c411784c8d8bf1bec5bb6f26d/xmlnote/WEBRESOURCE2a046d89191fbd78df1db2566e470ab5/46734)

### 4.哈希表Hash：
HashMap 是一个散列表，它存储的内容是键值对(key-value)映射  
存储结构（简单说来就是 数组(hash桶)+链表+红黑树）  
![](https://note.youdao.com/yws/public/resource/e219b21c411784c8d8bf1bec5bb6f26d/xmlnote/WEBRESOURCEdf08b555d28b58cee02b7dd7af9064f6/46529)

### 5.栈(Stack)：也称为堆栈，是一种线性表
栈（stack）——后进先出LIFO(Last-In/First-Out)，删除与加入均在栈顶操作   
- PUSH：在堆栈的顶部加入一 个元素。  
- POP：在堆栈顶部移去一个元素， 并将堆栈的大小减一。
    
![](https://note.youdao.com/yws/public/resource/e219b21c411784c8d8bf1bec5bb6f26d/xmlnote/WEBRESOURCEea4b7a514ed590fa856fd8c37daf82df/46528)  

使用：方法执行时，局部变量、参数值以及返回地址都被压入栈  
栈溢出：递归，不断执行方法并入栈，没有涉及条件跳出递归，就会造成栈溢出；  

**递归函数：** 一个直接用自己或通过一系列的调用语句间接地调用自己的函数，称作递归函数  
- 在前行阶段：对于每一层递归，函数的局部变量、参数值以及返回地址都被压入栈中。  
- 在退回阶段：位于栈顶的局部变量、参数值和返回地址被弹出，用于返回调用层次中执行代码的其余部分，也就是恢复了调用的状态。  

PS：递归函数必须至少有一个条件，满足时递归不再执行，即不再引用自身而是返回值退出。  

### 6.堆：是一种经过排序的树形数据结构(二叉树)  
![](https://note.youdao.com/yws/public/resource/e219b21c411784c8d8bf1bec5bb6f26d/xmlnote/WEBRESOURCE9583fba173d4118481affe8868adb214/46531)  
- 堆是在程序运行时，而不是在程序编译时，申请某个大小的内存空间。即动态分配内存，对其访问和对一般内存的访问没有区别  
- 堆是一种经过排序的树形数据结构，每个节点都有一个值，通常我们所说的堆的数据结构是指二叉树。所以堆在数据结构中通常可以被看做是一棵树的数组对象。而且堆需要满足一下两个性质：  
（1）堆中某个节点的值总是不大于或不小于其父节点的值；  
（2）堆总是一棵完全二叉树。  
- 堆分为两种情况，有最大堆和最小堆。将根节点最大的堆叫做最大堆或大根堆，根节点最小的堆叫做最小堆或小根堆  

> 堆和栈区别：  
- 申请方式的不同：栈是系统自动分配空间的，而堆则是程序员根据需要自己申请的空间。  
栈上的空间是自动分配自动回收的，所以栈上的数据的生存周期只是在函数的运行过程中，运行后就释放掉，不可以再访问。   
- 申请效率的比较：栈由系统自动分配，速度较快。但程序员是无法控制的。  
堆是由new分配的内存，一般速度比较慢，而且容易产生内存碎片，不过用起来最方便。   

### 7.队列(Queue)： 先进先出FIFO，队列也是一种特殊的线性表。
队列的原则是先进先出。 队列在队头做删除操作, 在队尾做插入操作：  
![](https://note.youdao.com/yws/public/resource/e219b21c411784c8d8bf1bec5bb6f26d/xmlnote/WEBRESOURCEc184deb242da2827d893ee3ba3500598/46532)
- 双端队列 ：Deque。
- 优先队列：PriorityQueue
- 循环队列  
![](https://note.youdao.com/yws/public/resource/e219b21c411784c8d8bf1bec5bb6f26d/xmlnote/WEBRESOURCEd6cc9f6b14cf3da3cdf579bde80abf0c/46738)

### 8.树 
树的基本概念  
![](https://note.youdao.com/yws/public/resource/e219b21c411784c8d8bf1bec5bb6f26d/xmlnote/WEBRESOURCE524f03d7aec65bf5de739e625e9232b9/46768)
  
- 节点的度：节点度 == 节点的子节点数
- 树的度：树的度 == 节点中度最大的
- 叶子节点：度为0的节点，即无子节点的节点
- 分支节点：有子节点，有分支的节点
- 内部节点：除根节点、叶子节点外的，称为分支节点
- 父节点：
- 子节点：
- 兄弟节点：
- 层：

#### 8.1 二叉树：
每个结点最多有两个子树的树结构。    
二叉树常被用于实现二叉查找树和二叉堆。   

![](https://note.youdao.com/yws/public/resource/e219b21c411784c8d8bf1bec5bb6f26d/xmlnote/WEBRESOURCEdd7608c30ad56efc3312cc38988db2f5/46784)

#### 8.2 满二叉树：
一棵深度为k，且有2^k-1个节点的二叉树，称为满二叉树。  
这种树的特点是每一层上的节点数都是最大节点数，每一层都是满的  

#### 8.3 完全二叉树：
除最后一层外，若其余层都是满的，并且最后一层或者是满的，或者是在右边缺少连续若干节点，则此二叉树为完全二叉树     
深度为k的完全二叉树，至少有2k-1个叶子节点，至多有2k-1个节点。  

#### 8.4 二叉查找树（Binary Search Tree）：
性质：左子节点<根节点<右子节点  
优点：解决链表、数组：查找/插入 速度问题  
缺点：极端情况下，退化成链表(斜树)    

#### 8.5 平衡二叉查找树（AVL）：
性质：左右子树深度差不超过1，通过左旋、右旋来平衡    

#### 8.6 红黑树(自平衡二叉查找树))
是一种自平衡二叉查找树

#### 8.7 B树（英语：Balanced-tree）：
是一种平衡的多叉查找树，能够保持数据有序。这种数据结构能够让查找数据、顺序访问、插入数据及删除的动作，都在对数时间内完成  

**性质**  
- 1.根结点至少有两个子女(特殊情况：没有孩子的根结点，即根结点为叶子结点，整棵树只有一个根节点)
- 2.每个中间节点都包含k-1个关键字和k个孩子，其中 m/2 <= k <= m
- 3.每一个叶子节点都包含k-1个关键字，其中 m/2 <= k <= m
- 4.所有的叶子结点都位于同一层
- 5.每个节点中的关键字从小到大排列；中间节点的k关键字，左边子树的所有值都必须小于k关键字，右边子树的所有值都必须大于k关键字

**性质解析**    
![](https://note.youdao.com/yws/public/resource/e219b21c411784c8d8bf1bec5bb6f26d/xmlnote/WEBRESOURCE8f4d8a0495daebd44e8f0972f5b88777/46578)  
性质五保证了树的顺序性，才能作为搜索树，达到这一点只需要在插入删除做结构变换时比较下大小就可以了  
性质二、三、四保证了树的平衡性和磁盘空间利用率；  
达到性质二、三需要插入删除时注意保持结构一致就可以；  
达到性质四这里比较巧妙，它是向上分裂的，自然而然的保证了叶子节点都在同一层  
性质一避免树的单肢

#### 8.8 B+树：加强版的多路平衡查找树
B+树是B树的一种变形形式，B+树上的叶子结点存储关键字以及相应记录的地址，叶子结点以上各层作为索引使用

与B树差异  
- 1.所有关键字都可以在叶子节点中找到，叶子结点本身依关键字的大小自小而大顺序链接。
- 2.data只存在叶子节点  
![](https://note.youdao.com/yws/public/resource/e219b21c411784c8d8bf1bec5bb6f26d/xmlnote/WEBRESOURCE15318bf993523b9b42831b576ae9e022/46580)  

相比B树优点
- 1.单一节点存储更多元素，减少io次数；因为没有data
- 2.更好的范围查找；叶子节点形成了有序链表
 
操作系统读磁盘，一次io读一页数据，8扇区*512b=4kb

#### 8.9 字典树：

#### 8.10 排序树：

#### 8.11 R树：

#### 8.12 多路(叉)树：一个节点有多个子节点  

#### 8.13 二叉树遍历
![](https://note.youdao.com/yws/public/resource/e219b21c411784c8d8bf1bec5bb6f26d/xmlnote/WEBRESOURCE8ffb76d59f5b17fbf4b961a690e403b1/46579)  

**1.1 深度优先遍历：**     
- 前序遍历： 根 左子树 右子树， 结果为ABDGHECKFIJ  
- 中序遍历： 左子树 根 右子树 ，结果为GDHBEAKCIJF  
- 后序遍历：左子树 右子树 根 ，结果为GHDEBKJIFCA  
- 层次遍历：从上往下，从左往右，结果为A BC DEKF GHI J

**1.2 广度优先遍历**：访问根，访问子女，再访问子女的子女    
即按照层次访问，通常用队列来做。（越往后的层次越低）（两个子女的级别相同）s

### 9.图
- 图的遍历
- 最小生成树
- 最短路径

## 三、java中常用的数据结构 

### 3.1 散列表(HashMap)：
- HashMap是什么：HashMap 是一个散列表，它存储的内容是键值对(key-value)映射
- 为什么需要它：HaspMap是O(1)的 ，写代码时，查找元素更简洁的写法(haspMap.get(key))
- 优点：查找O(1)效率高，缺点：线程不安全

#### HashMap存储结构
简单说来就是： 数组(hash桶)+链表+红黑树  
![](https://wdsheng0i.github.io/assets/images/2021/datastruct/hm2.png)  

若桶中链表元素个数>=8，链表转成树结构；若桶中链表元素个数<=6，树结构还原成链表  
![](https://wdsheng0i.github.io/assets/images/2021/datastruct/hm1.png)  

#### 查找元素 
使用哈希函数将被查找的键转换为数组的索引。
- 获取object hashcode
- 通过hashcode计算位置
- hashcode与hashcode的前16位与取值
- 用前面hashcode计算的值与(数组长度-1)与计算得到所在hash桶下标

hash冲突
- 理想情况下，不同键会被转换为不同索引值，但有些情况我们需要处理多个键被哈希到同一索引值的情况。即hash冲突
- 而且在创建hash表和查找hash表都有可能会遇到冲突。        
- 因为作为一种可用的hash算法，其位数一定是有限的，但是它所能记录的文件又是无限的。所以碰到碰撞的概率永远不会是零。

#### 处理哈希碰撞冲突方法
通过构造性能良好的hash算法，可以减少冲突，但不能完全避免冲突。 其中MD5和SHA-1是应用最为广泛的Hash算法。  
常见的Hash算法:  
- MD4：MD4是MIT的Rivest在1990年设计，MD是信息摘要 Message Digest 的缩写。它是基于32位操作数的位操作来实现的。
- MD5：  MD5是Rivest在1991年对MD4的改进，MD5比MD4复杂，因此速度慢一些，但安全性更好。
- SHA-1：SHA-1是由NIST NSA设计的，它对长度小于264位的输入，产生长度位160位的散列值。因此抗穷举性更好。SHA-1模仿了MD4的算法    

    
解决碰撞的方法: 
- 开放寻址法： 主要是通过key转出hash值h1，如果遇到冲突，那在h1的基础上，再次进行hash操作得到h2，直到不产生冲突为止。
- 再哈希法： 主要是同时构造多个hash函数，当第一个hash函数计算出来的遇到冲突时，调用第二个hash函数计算出来的hash值。以此类推，直到不产生冲突为止。
- 链地址法： 主要将所有hash值（比如都为i）相同的元素构成一个称谓同义词链的单链表，将单链表的头指针存放在hash表的第i个单元中。
- 建立公共溢出区：  主要将hash表分为基本表和溢出表，凡是和基本表相冲突的，都放在溢出表中。

#### 扩容
HashMap的长度是改变的,长度改变即扩容与两个参数有关 ：“初始容量” 和 “加载因子”。
- 容量（初始容量16 ）： 是哈希表中桶的数量，只是哈希表在创建时的容量。
- 加载因子（默认0.75）： 是哈希表在其容量自动增加之前可以达到多满的一种尺度。时间和空间成本上计算出的一种折衷

当哈希表中的条目数超出了加载因子与当前容量的乘积时，则要对该哈希表进行 rehash 操作（即重建内部数据结构），从而哈希表将具有大约两倍的桶数。

#### 问题记录
1.HashMap在多线程下可能会导致死循环
``` 
jdk1.7.0_79源码
死循环是因为jdk7插入元素是前插法，在resize时会进行反转链表，多线程下就造成了死循环；网上很多用3,5,7演示死循环示例，看jdk1.7.0_79的源码发现，不管怎么样都不可能造成死循环，因为
1在resize后才把元素加进去，
2resize判断的2个条件，要size大于阀值，并且放的元素的index里面已经有值

jdk1.8.0_201源码
死循环是多线程情况下在红黑树里面造成的死循环
```

### 3.2 concurentHsahMap
	细化分段锁

### 3.3 LinkedHashMap
结构 和HashMap 相同，区别是维护一个根据插入顺序保持的双向链表
![](https://wdsheng0i.github.io/assets/images/2021/datastruct/lhm.png)  

### 3.4 LinkList
	基于链表实现，查找O(n)

### 3.5 ArrayList
	底层数据结构就是一个数组，数组元素的类型为Object类型
	初始size：10
	扩容1.5倍后拷贝旧数组元素

### 3.6 TreeMap
存储结构: 红黑树  
TreeMap详解可以参考：https://www.jianshu.com/p/2dcff3634326  
![](https://wdsheng0i.github.io/assets/images/2021/datastruct/treemap.png)  

 







