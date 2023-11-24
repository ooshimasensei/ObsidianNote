# 一个RNN的例子
## 得到第一个输出
![[Pasted image 20231118153528.png]]
## 存储中间层结果
![[Pasted image 20231118160351.png]]
## 存储的中间层结果参与新的计算
![[Pasted image 20231118160634.png]]
## 再对新的输入2 2计算
![[Pasted image 20231118160710.png]]
# 有两种RNN，一种记忆上次的中间结果，一种记忆上次的输出结果
![[Pasted image 20231118161114.png]]
# 还有双向的RNN
![[Pasted image 20231118164630.png]]
# LSTM 模型
## 简图
![[Pasted image 20231118165227.png]]
## 流程
![[Pasted image 20231118172019.png]]
流程举例
![[Pasted image 20231118200638.png]]
### 第一个输入的运作情况
![[Pasted image 20231118205243.png]]
### 第二个输入，流程跟上图一样
![[Pasted image 20231118205808.png]]
## LSTM因为多了3个输入端，参数量是普通网络的四倍
![[Pasted image 20231118212608.png]]
## LSTM不同时刻的信息传递
![[Pasted image 20231119091407.png]]
接上图，cell里存的内容也会参与到下一时刻的输出
![[Pasted image 20231119091917.png]]
 上面的结构还可以叠很多层
![[Pasted image 20231119092843.png]]

# 模型训练
## 训练的目标怎么表示
![[Pasted image 20231120114421.png]]
## 对于RNN怎么算梯度
![[Pasted image 20231120114922.png]]
## RNN训练的时候有没有自己的问题
### Loss 在训练的时候会出现剧烈的震荡
![[Pasted image 20231120115501.png]]
### 是什么导致了上面的问题
![[Pasted image 20231120131756.png]]
# 各种各样的任务
## 评价类
![[Pasted image 20231120132420.png]]
## 输入比较多 输出比较少
![[Pasted image 20231120132703.png]]
上面的例子没办法 区分好棒和好棒棒
![[Pasted image 20231120132843.png]]![[Pasted image 20231120134809.png]]
对于英文的识别例子
![[Pasted image 20231120134904.png]]

![[Pasted image 20231120155824.png]]


