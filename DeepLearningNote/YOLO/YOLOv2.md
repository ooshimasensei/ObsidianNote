# 算法流程大致不变，只列出相对V1的变化
## 输出结果的改动，现在每个anchor有自己的20个分类概率，不再像v1版本一样一个grid cell共享20个分类的条件概率
![[Pasted image 20231008145145.png]]
![[Pasted image 20231008145947.png]] 
## 引入了Batch Normalization
![[Pasted image 20231008162643.png]]

![[Pasted image 20231021132805.png]]
## 去掉了yolov1中的全连接层，替换为卷积
## 细粒度特征
## 改进方法和影响
![[Pasted image 20231021132220.png]]