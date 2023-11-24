# 期刊名
![[Pasted image 20231122150634.png]]
# 创新点
加了一个局部注意力模块
加了一个迁移学习
# 实验部分
## 数据准备
coco数据集 330000张
自用数据集 631张
## 实验环境设置
预训练集：imageNet
基准模型：D-DETR
指标：box loss, label loss ,GIOU loss
最终指标：上面三个指标加权
优化器：Adam
LR:0.0002
Epoch:200 **(感觉有点太多了，微调5-6个就够了)**
## 模型性能对比
![[Pasted image 20231122152744.png]]
第一排是基准模型
第二排加了局部注意力
第三批用了迁移学习
**他这里性能的比较是在coco数据集上的，可能原作者只在coco数据集上做了**
## 消融实验
![[Pasted image 20231122152928.png]]
**消融实验只做了$AP_s$**
## 分析和讨论
在自己数据集上挑了几个图，证明可以识别小的目标
![[Pasted image 20231122153230.png]]
# 相关文章的线索
## muda
目前，光伏组件表面异物阴影检测的研究主要采用基于图像的分析方法。三种最常用的基于图像的研究方法是电致发光成像、红外成像和可见光成像。Abdelilah Et-taleby 等人提出了一个结合了两种机器学习算法——卷积神经网络(CNN)和支持向量机(SVM)的模型，用于检测和分类 PV 模块故障，并达到了很高的准确率。所使用的数据库是 PV 模块的电致发光图像[27]**他这个是做分类的，近距离判断光伏板是裂痕还是破损等具体的伤损**。
## A novel detection method for hot spots of photovoltaic (PV) panels using improved anchors and prediction heads of YOLOv5 network
针对 YOLOv5网络，提出了一种基于改进的锚和预测头的光伏组件故障检测方法。对于红外光谱中的光伏组件图像，研究了在实际操作中光伏组件上热点形成的机制，并对热点目标进行分类，以便于识别和检测光伏组件热点[28]**在热相机上定位热斑**。
## Image based surface damage detection of renewable energy installations using a unified deep learning approach
Fadhel 等人应用最先进的改进的基于 YOLOv5的目标检测图像分析方法来检测风力涡轮机和光伏组件的表面损伤。此外，他们还实现了对不同分辨率的可见图像数据(从光伏组件到风力涡轮机)的极佳识别精度[29]。**在可见光相机上做的光伏板污损**
## Automatic soiling and partial shading assessment on PV modules through RGB images analysis.
Robinson Cavieres 等人开发了一个模型，该模型利用光伏组件的可见光图像来识别图像中存在的每个组件，将每个光伏组件从图像中分离出来，评估其操作，并使用神经网络的分割、同质化和回归操作来确定由于损坏或部分着色引起的功率损失。这对于确保发电光伏系统的最佳运行和维护非常重要[30]。**识别可见光相机拍摄的**

