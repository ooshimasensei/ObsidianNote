# Transformer 架构
## Enoder
### Encoder结构，输入一排向量，输出一排向量
![[Pasted image 20231101203915.png]]
### Encoder内部结构，由若干个Block组成（下图右侧仅便于理解并不是原本transformer的结构）
![[Pasted image 20231101204504.png]]
### 原本的transformer中一个Block实际的结构如下图
![[Pasted image 20231102132431.png]]
## Autoregressive Decoder
### Decoder的输入包含了自己先前的输出
![[Pasted image 20231102141138.png]] 
### 稍微对比一下,Encoder和Decoder在结构上的差别(灰色覆盖的部分后面再讲,其他部分差别不大) 
![[Pasted image 20231102143847.png]]
### 上图中Decoder里masked讲解
#### masked考虑的输入的示意图,不能像encoder一样考虑全部的输出
![[Pasted image 20231102144222.png]]
#### 比如b2作为例子
![[Pasted image 20231102144625.png]]
### Decoder也可以输出结尾,用来表示不用再生成新的输出
![[Pasted image 20231102145253.png]]
## Decoder -Non-autoregressive(NAT)和AT的比较
![[Pasted image 20231102150530.png]]
## 上面Decoder里灰色遮挡的一部分
### 结构, 这部分称为Cross attention
![[Pasted image 20231102151229.png]]
### Cross attention的计算方法
![[Pasted image 20231102152117.png]]
### 一个语音识别的例子
![[Pasted image 20231102153404.png]]
### Cross Attention 计算的时候, Decoder的输入不一定非要来自Encoder的最后一层
![[Pasted image 20231102153802.png]]
## Transformer的训练
### 输出的格式和分类是类似的
![[Pasted image 20231102154254.png]]
### 输出的样子,输出的loss是用cross entropy
![[Pasted image 20231102154537.png]]
### 复制机制
![[Pasted image 20231102154904.png]]

![[Pasted image 20231102154946.png]]
### Guided Attention  (对于语音合成有用)
![[Pasted image 20231102211854.png]]
### Beam Search(感觉讲的有点少,用不上, 只适合答案固定的任务)
![[Pasted image 20231102212453.png]]
### Scheduled Sampling
![[Pasted image 20231102213041.png]]