## 本章任务：

+ [x] 了解AI相关概念，ML分类
+ [ ] 运行Python/Jupyter Notebook相关示例代码

观感：还可以，详略得当，AI讲的不深

---

面向网络安全专业人员的AI简介

将AI应用于网络安全

> 迄今为止AI取得的成果时令人振奋的，而其分析方法将来会成为网络安全从业者的常识
>
> 迫在眉睫的问题是将机器的自动分析与操作人员的技能结合，使得操作人员和机器间不会产生冲突；AI处理繁琐的低级工作，选择潜在的可疑案件，安全分析人员处理最应收到关注的威胁案件

[**专家系统**](https://zh.wikipedia.org/wiki/%E4%B8%93%E5%AE%B6%E7%B3%BB%E7%BB%9F)是早期[人工智能](https://zh.wikipedia.org/wiki/人工智能)的一个重要分支，它可以看作是一类具有专门知识和经验的计算机智能程序系统，一般采用人工智能中的[知识表示](https://zh.wikipedia.org/wiki/知识表示)和[知识推理](https://zh.wikipedia.org/w/index.php?title=知识推理&action=edit&redlink=1)技术来模拟通常由领域专家才能解决的复杂问题。

一般来说，专家系统=[知识库](https://zh.wikipedia.org/wiki/知识库)+[推理机](https://zh.wikipedia.org/wiki/推理机)，因此专家系统也被称为基于知识的系统。一个专家系统必须具备三要素：

1. 领域专家级知识
2. 模拟专家思维
3. 达到专家级的水准

局限：决策简化为布尔值，限制在一个知识库中，无法解决未解决的新问题

[数据挖掘](https://zh.wikipedia.org/wiki/%E6%95%B0%E6%8D%AE%E6%8C%96%E6%8E%98)

**数据挖掘**（英语：**data mining**）是一个跨学科的[计算机科学](https://zh.wikipedia.org/wiki/计算机科学)分支[[1\]](https://zh.wikipedia.org/wiki/数据挖掘#cite_note-acm-1)[[2\]](https://zh.wikipedia.org/wiki/数据挖掘#cite_note-brittanica-2)[[3\]](https://zh.wikipedia.org/wiki/数据挖掘#cite_note-elements-3) 。它是用[人工智能](https://zh.wikipedia.org/wiki/人工智能)、[机器学习](https://zh.wikipedia.org/wiki/机器学习)、[统计学](https://zh.wikipedia.org/wiki/统计学)和[数据库](https://zh.wikipedia.org/wiki/数据库)的交叉方法在相对较大型的[数据集](https://zh.wikipedia.org/wiki/数据集)中发现模式的计算过程[[1\]](https://zh.wikipedia.org/wiki/数据挖掘#cite_note-acm-1)。

数据挖掘过程的总体目标是从一个数据集中提取信息，并将其转换成可理解的结构，以进一步使用[[1\]](https://zh.wikipedia.org/wiki/数据挖掘#cite_note-acm-1)。除了原始分析步骤，它还涉及到数据库和[数据管理](https://zh.wikipedia.org/wiki/数据管理)方面、[数据预处理](https://zh.wikipedia.org/w/index.php?title=数据预处理&action=edit&redlink=1)、[模型](https://zh.wikipedia.org/wiki/概率模型)与[推断](https://zh.wikipedia.org/wiki/推論統計學)方面考量、兴趣度度量、[复杂度](https://zh.wikipedia.org/wiki/計算複雜性理論)的考虑，以及发现结构、[可视化](https://zh.wikipedia.org/wiki/数据可视化)及[在线更新](https://zh.wikipedia.org/wiki/線上演算法)等后处理[[1\]](https://zh.wikipedia.org/wiki/数据挖掘#cite_note-acm-1)。数据挖掘是“数据库知识发现”（Knowledge-Discovery in Databases, KDD）的分析步骤[[4\]](https://zh.wikipedia.org/wiki/数据挖掘#cite_note-Fayyad-4) ，本质上属于机器学习的范畴。

## ML:

### 监督学习

利用输入数据集对算法训练，样本的输出类型已知

示例：垃圾邮件过滤器（已分类好垃圾邮件和正常邮件）

几种监督学习：

+ 回归 线性 逻辑
+ K近邻
+ 支持向量机SVM
+ 决策树和随机森林
+ 神经网络NN

### 无监督学习

必须尝试独立地对数据分类，而无需借助分析人员之前标注的类别

用途：识别新的恶意软件攻击、欺诈和电子邮件活动

示例：

+ 降维
  + 主成分分析PCA
  + 核化PCA
+ 聚类
  + K均值k-means
  + 层次聚类分析HCA

### 强化学习

从学习路径获取的反馈中汲取信息，根据所选算法的正确决策数量，使最终的激励最大化

示例：

+ 马尔可夫过程
+ Q学习
+ 时序差分法
+ 蒙特卡洛方法

隐马尔可夫模型HMM在检测多态恶意软件至关重要

## 算法的训练和优化

+ 误报处理
+ 正确告警数量控制

## Python实操

监督学习示例——线性回归

无监督学习示例——聚类

简单的人工神经网络示例——感知机

## 网安背景下的人工智能

初级分析阶段，分流triage，威胁初步筛选

对网络安全人员的能力要求：理解算法的逻辑，根据目标，在算法的学习阶段微调

+ 分类：区分恶意软件
+ 聚类：无监督，当事先无法获取有关类别的信息时，聚类能自动识别样本所属的类比；恶意软件分析和取证分析
+ 预测分析：NN和DL，威胁发生时识别，高度动态，自动优化

AI在Sec的可能应用：

+ 网络保护：使用ML实现高度复杂的入侵检测系统IDS，用于网络边界保护领域
+ 终端保护：针对勒索病毒，检测威胁
+ 应用安全：SSRF、SQL注入、XSS、DDoS
+ 可疑用户行为：及时识别恶意用户欺诈或破坏应用程序的企图

