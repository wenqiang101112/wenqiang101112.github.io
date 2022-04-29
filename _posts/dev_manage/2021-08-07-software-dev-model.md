---
layout: post
title:  软件开发模型介绍
category: dev-manage
tags: [dev-manage]
---

## 参考资料 
《系统架构设计师教程》  
《敏捷软件开发(原则模式与实践)》

## 一、软件开发生命周期
传统的软件生命周期是指软件产品从形成概念开始，经过定义、开发、使用和维护，直到最后被废弃（不能再使用）为止的全过程。

## 二、软件开发模型
- 软件生存周期模型又称软件开发模型（software develop model）或软件过程模型（software process model），它是从某一个特定角度提出的软件过程的简化描述。
- 软件过程模型的基本概念：软件过程是制作软件产品的一组活动以及结果，这些活动主要由软件人员来完成，软件活动主要如下：
    - 软件描述
    - 软件开发
    - 软件有效性验证
    - 软件进化  
    
软件过程模型是软件工程重要内容，为软件工程管理提供里程碑，为软件开发过程提供原则和方法。

### 2.1 瀑布模型
瀑布模型（waterfall model）可以说是最早使用的软件生命周期模型之一。该模型描述的活动从一个阶段到另一个阶段逐次下降，它的工作流程形式上又很想瀑布，该模型如下图所示：  
![](https://wdsheng0i.github.io/assets/images/2021/dev-manage/pb.png)    

特点:
- 阶段间具有顺序性和依赖性:  
因果关系紧密相连：前一阶段完成后，才能开始后一阶段。
前一个阶段工作的结果是后一个阶段工作的输入
- 质量保证:  
每个阶段必须交付出合格的文档
对文档进行审核

缺点：
- 软件需求分析的准确性很难确定
- 初始版本周期长
- 如果改变需求，代价巨大

各阶段关注内容： 
- 1）可靠性研究与计划：做还是不做
- 2）需求分析：都有什么功能
- 3）概要设计：共有多少子功能
- 4）详细设计：子功能怎么实现
- 5）编码：子功能实现了吗？
- 6）测试：功能完备吗？
- 7）部署：需要多少设备和软件

#### 1). 产品需求定义
产品需求定义的目标是：“清楚地描述要做的产品是什么样的？不涉及具体实现方法。”，其定义过程如下图所示。  
![](https://wdsheng0i.github.io/assets/images/2021/dev-manage/pb-1.png)  

 此产品需求定义包括：软件+硬件
 
#### 2).需求调研分析

#### 3).架构/概要设计/系统模块设计
架构设计或概要设计的目标是：“为系统需求或产品需求提供解决方案”。   
概要设计：把软件按照一定的原则分解为模块、层次，赋予每个模块一定的任务，并确定模块间调用关系和接口。通常输出的为：“软件结构图”。   
在架构设计或概要设计，设计者会大致考虑并照顾模块的内部实现，但不过多纠缠于此。主要集中于：
- （1）划分模块
- （2）分配任务
- （3）定义调用关系

模块间的接口与传参在这个阶段要定得十分细致明确，应编写严谨的数据字典，避免后续设计产生不解或误解。概要设计一般不是一次就能做到位，而是反复地进行结构调整。典型的调整是合并功能重复的模块，或者进一步分解出可以复用的模块。在概要设计阶段，应最大限度地提取可以重用的模块，建立合理的结构体系，节省后续环节的工作量。  
概要设计文档最重要的部分是：
- （1）分层数据流图
- （2）结构图
- （3）数据字典
- （4）相应的文字说明

以概要设计文档为依据，各个模块的详细设计就可以并行展开了。
包括系统的基本处理流程、系统的组织结构、模块划分、功能分配、接口设计、运行设计、数据结构设计和出错处理设计等，为软件的详细设计提供基础。

#### 4).详细设计
详细设计的目标是：“提供编码的依据（数据结构+流程）”。  
详细设计：依据概要设计阶段的分解，设计每个模块内的算法、流程等。通常采用“流程图”进行描述。   
在详细设计阶段，各个模块可以分给不同的人去并行设计。在详细设计阶段，设计者的工作对象是一个模块，根据概要设计赋予的局部任务和对外接口，设计并表达出模块的以下内容：  
- （1）算法
- （2）流程
- （3）状态转换（状态机）

注意：如果发现有结构调整（如分解出子模块等）的必要，必须返回到概要设计阶段，将调整反应到概要设计文档中，而不能就地解决，不打招呼。  

详细设计文档最重要的部分是模块的以下内容：
- （1）流程图
- （2）状态图
- （3）局部变量及相应的文字说明。
 
一个模块一篇详细设计文档。

在概要设计的基础上，开发者需要进行软件系统的详细设计。  
在详细设计中，描述实现具体模块所涉及到的主要算法、数据结构、类的层次结构及调用关系，需要说明软件系统各个层次中的每一个程序(每个模块或子程序)的设计考虑，以便进行编码和测试。  
应当保证软件的需求完全分配给整个软件。详细设计应当足够详细，能够根据详细设计报告进行编码。

#### 5).编码实现

#### 6).测试

#### 7).运行维护

### 2.2 原型模型
原型模型（prototype model）又称快速原型。由于瀑布模型的缺点，人们借助建筑师、工程师建造原型的经验，提出了原型模型。原型模型主要有两个阶段，如下图所示：  
![](https://wdsheng0i.github.io/assets/images/2021/dev-manage/yx.png)    

- 原型开发阶段：根据用户提出的软件系统定义，快速地开发一个原型。
利用模拟软件系统的人机界面和人机交互方式。
真正开发一个原型。
找一个或多个正在运行的类似软件进行比较。
- 目标软件开发阶段。

使用原型模型应该注意：
- 要有一定的开发环境和工具支持。
- 经过对原型的若干次修改，应收敛到目标范围内，否则可能会失败。
- 用户对系统模糊不清，无法准确回答目标系统的需求。
- 对大型软件来说，原型可能非常复杂而难以快速形成，如没有现成的，就不应考虑原型法。

### 2.3 螺旋模型
螺旋模型（Spiral Model）是在快速原型的基础上扩展而成，实际上，它是软件生命周期模型与原型模型的一个结合，如下图所示：  
![](https://wdsheng0i.github.io/assets/images/2021/dev-manage/lx.png)    

该模型将整个软件开发流程分为多个阶段，每个阶段都由4部分组成：
- 目标设定
- 风险分析
- 开发和有效性验证
- 评审

螺旋模型的软件开发过程实际上是上述4个部分的迭代过程，每迭代一次，螺旋线就增加一周，代表软件的一个新版本。经过若干次迭代后，系统应尽快收敛到用户允许或可以接受的目标范围。

优点:
- 设计上的灵活性,可以在项目的各个阶段进行变更。
- 以小的分段来构建大型系统，使成本计算变得简单容易。
- 客户始终参为保证了项目不偏离正确方向以及项目的可控性。
- 客户始终掌握项目的最新信息，从而他或她能够和管理层有效地交互。
- 客户认可这种公司内部的开发方式带来的良好的沟通和高质量的产品。

缺点:
- 很难让用户确信这种演化方法的结果是可以控制的。
- 建设周期长，而软件技术发展比较快，所以经常出现软件开发完毕后，和当前的技术水平有了较大的差距，无法满足当前用户需求。

### 2.4 增量模型
增量模型（Incremental Model）把待开发的软件系统模块化，将每个模块作为一个增量组件，从而分批次地分析、设计、编码和测试这些增量组件，如下图所示：  
![](https://wdsheng0i.github.io/assets/images/2021/dev-manage/zl.jpeg)    

困难:
每个新的构件集成到现有的软件结构中必须破坏原来以开发的产品，所以必须定义很好的接口。

优点:
- 短时间内向用户提供可完成部分工作的产品。
- 逐步增加产品功能可以使用户有时间了解和适应新产品。
- 开放结构的软件拥有的维护性明显好于封闭结构的软件。

缺点：
- 容易退化为边做边改模型，从而使软件过程的控制失去整体性。
- 如果增量包之间存在相交的情况且未很好处理，则必须做全盘系统分析。

### 2.5 喷泉模型
喷泉模型（fountain model）是一种以用户需求为动力，以对象为驱动的模型，主要用于描述面向对象的软件开发过程。该模型认为软件开发过程自下而上周期的各阶段是相互迭代和无间隙的特性，该模型如下图所示：  
![](https://wdsheng0i.github.io/assets/images/2021/dev-manage/pq.png)  
  
优点:
- 喷泉模型不像瀑布模型那样，需要分析活动结束后才开始设计活动，设计活动结束后才开始编码活动。
- 该模型的各个阶段没有明显的界限，开发人员可以同步进行开发。
- 可以提高软件项目开发效率，节省开发时间，适应于面向对象的软件开发过程。

缺点:
- 由于喷泉模型在各个开发阶段是重叠的，因此在开发过程中需要大量的开发人员，因此不利于项目的管理。
- 这种模型要求严格管理文档，使得审核的难度加大，尤其是面对可能随时加入各种信息、需求与资料的情况。

### 2.6 敏捷开发
敏捷开发以用户的需求进化为核心，采用迭代、循序渐进的方法进行软件开发，其核心思想主要有以下三点：
- 适应型，而非可预测型。
- 以人为本，而非已过程为本。
- 迭代增量式的开发过程。

敏捷开发知识体系整体框架  
![](https://wdsheng0i.github.io/assets/images/2021/dev-manage/mj.png)    

敏捷软件开发宣言
- 个体和交互胜过过程和工具。
以人为本，强调个体及个体间的沟通与协作在软件开发过程中的重要性。
- 可以工作的软件胜过面面俱到的文档。
目标导向，自解释的友好的代码和架构。
- 客户合作胜过合同谈判。
客户为先，理解客户的需求，懂得如何与客户合作。
- 响应变化胜过遵循计划。
拥抱变化，在客户断变化的需求中了解其真正的需要。

敏捷宣言遵循的原则
- 我们最优先要做的是通过尽早的、持续的交付有价值的软件来使客户满意。
- 即使到了开发的后期，也欢迎改变需求。敏捷过程利用变化来为客户创造竞争优势。
- 经常性地交付可以工作的软件，交付的间隔可以从几个星期到几个月，交付的时间间隔越短越好。
- 在整个项目开发期间，业务人员和开发人员必须天天都在一起工作。
- 围绕被激励起来的个体来构建项目。给他们提供所需的环境和支持，并且信任他们能够完成工作。
- 在团队内部，最具有效果并且富有效率的传递信息的方法，就是面对面的交谈。
- 工作的软件是首要的进度度量标准。
- 敏捷过程提倡可持续的开发速度。责任人、开发者和用户应该能够保持一个长期的、恒定的开发速度。
- 不断地关注优秀的技能和好的设计会增强敏捷能力。
- 简单——使未完成的工作最大化的艺术——是根本的。
- 最好的构架、需求和设计是出自于自组织的团队。
- 每隔一定时间，团队会在如何才能更有效地工作方面进行反省，然后相应地对自己的行为进行调整。

敏捷设计  
拙劣设计的症状
- 僵化性：设计难以改变。
- 脆弱性：设计易于遭到破坏。
- 牢固性：设计难以重用。
- 粘滞性：难以做正确的事情。
- 不必要的复杂性：过分设计。
- 不必要的重复：复制黏贴。
- 晦涩性：混乱的表达。

这些症状在本质上和代码的臭味相似，但是它们所处的层次稍高一些。它们是遍及整个软件结构的臭味，而不仅仅是一小段代码。


 