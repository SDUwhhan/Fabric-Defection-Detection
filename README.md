# Fabric-Defection-Detection
山东大学（威海）2022年机器学习项目———布匹缺陷检测
# 结果预览
# ![Image text](ScreenShots/image20230207121843.png)
# ![Image text](ScreenShots/image20230207121909.png)
### 测试环境： 
### CPU : 12th Gen Intel(R) Core(TM) i7-12700H   2.70 GHz
### GPU : NVIDIA RTX3070Ti
### RAM : 32GB
### Matlab R2020a (Deep Learning Tools)
### 注 ：Data文件过大 未上传
# 一.神经网络概述
## 1. 卷积神经网络概念
人工神经网络（Artificial Neural Networks，ANN）是一种模拟生物神经系统的结构和行为，进行分布式并行信息处理的算法数学模型。ANN通过调整内部神经元与神经元之间的权重关系，从而达到处理信息的目的。而卷积神经网络（Convolutional Neural Network，CNN）是一种前馈神经网络，它由若干卷积层和池化层组成，尤其在图像处理方面CNN的表现十分出色。

CNN的基本结构由输入层、卷积层（convolutional layer）、池化层（pooling layer，也称为取样层）、全连接层及输出层构成。卷积层和池化层一般会取若干个，采用卷积层和池化层交替设置，即一个卷积层连接一个池化层，池化层后再连接一个卷积层，依此类推。由于卷积层中输出特征图的每个神经元与其输入进行局部连接，并通过对应的连接权值与局部输入进行加权求和再加上偏置值，得到该神经元输入值，该过程等同于卷积过程，CNN也由此而得名
## 2. 卷积神经网络的特点
卷积神经网络由多层感知机（MLP）演变而来，由于其具有局部区域连接、权值共享、降采样的结构特点，使得卷积神经网络在图像处理领域表现出色。卷积神经网络相比于其他神经网络的特殊性主要在于权值共享与局部连接两个方面。权值共享使得卷积神经网络的网络结构更加类似于生物神经网络。局部连接不像传统神经网络那样，第n-1层的每一神经元都与第n层的所有神经元连接，而是第n-1层的神经元与第n层的部分神经元之间连接。这两个特点的作用在于降低了网络模型的复杂度，减少了权值的数目。
# 二.图像数据预处理
## 2.1处理步骤
1.加载数据集

2.显示类别数量

3.图像的维度大小

4.为了使各类样本数量平衡选取数量最少的基准抽取样本

5.图像预处理，将图像转换

6.样本分割,随机抽取样本分割7:3的训练集和验证集

### 2.1.1加载数据集
imageDatastore()函数用于读取指定路径下的所有文件
使用语法：
ImageDatastore(path,Name,Value)
输入参数为文件（夹）路径，以及一些键值对，输出为一个ImageDatastore对象。


### 2.1.2显示类别数量
tbl = countEachLabel(imds) ⇒ 见名知意，创建一个表格，某一label图像，及其对应的图像个数；


### 2.1.3图像的维度大小

imread函数
用法： A = imread(filename.fmt)     
根据文件名filename读取灰度获彩色图像。返回的数组A包含图像数据。
若文件包含灰色图像，A是M*N的数组；若文件名包含真彩图像，A是M*N*3的数组。

### 2.1.4为了使各类样本数量平衡选取数量最少的基准抽取样本



### 2.1.5图像预处理，将图像转换



### 2.1.6样本分割,随机抽取样本分割为7:3的训练集和验证集


# 三.缺陷检测
## 3.1可视化工具Deep Learning Tools（matlab工具）
# 四.训练与测试
# 五.总结
## 5.1过拟合和欠拟合问题
## 5.2数据特征维度的选取
## 5.3参数的选取
