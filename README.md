# Tensorflow Study - By Yang
## 系统及相关硬件：Windows10 AMD-2GB显卡 
## 开发环境：python3.7.12 tensorflow2.11
## 前言
本人才疏学浅，精力有限，于2024年4月起，目前截止2024年7月，仅仅学习了tensorflow的2.0版本，且目前仅仅在cpu上运行尝试。 
这台电脑配置较低，显卡为AMD，无法使用Nvidia显卡的cuda加速，故浅尝辄止。本篇文章意在查漏补缺、巩固知识、温故知新。 
## 总览
### 2024年4月-2024年5月1日
学习python相关函数和内部构造。 
### 2024年5月-2024年7月1日
学习神经网络相关知识。 
### 2024年7月至今
进行测试
### 注：本篇文章并未涉及python脚本相关操作，仅仅进行本地构造运行
## 基础知识
本人学习过C++，初步使用过QT，MySQL，了解了计算机组成原理的基础，玩过一段时间的Ubuntu，玩过51单片机和32单片机，故python基础操作部分省略。 
### 神经网络基础
目前常用的神经网络有线性神经网络——以线性回归(linear regression)为基础构建的神经网络、卷积神经网络(convolutional neural network，CNN)，其旨在处理图像数据、 
循环神经网络(recurrent neural network，RNN)旨在处理序列数据，重点在于语言模型，基于过去的数据和现在的问题给出现在的回答。 
## 线性神经网络(LNN)
### 线性模型
线性假设公式如下所示: 

![image](https://github.com/user-attachments/assets/2fb1d234-1896-47eb-9129-9d01f0f4eda0) 

式中的![image](https://github.com/user-attachments/assets/efe7a4ab-993a-488a-ae85-dda6c407e5a9)和![image](https://github.com/user-attachments/assets/614c9089-1c0d-41e2-86ff-177f4fa04352)我们称为权重，权重决定了每个特征对我们预测值的影响程度。 
b称为偏置(bias)，为数学中所称的截距(intercept)。 
但是这仅仅是数学上的思维，机器学习需要更加直观的高维数据进行处理。于是我们将所有特征放入向量x中，将所有权重放入向量w中，得到了这个式子: 

![image](https://github.com/user-attachments/assets/46ce6a53-2215-4b57-afec-eaa0a88e6c46) 
 
对于x来说，X是n个x的特征集合向量，于是，可得这个式子: 
![image](https://github.com/user-attachments/assets/5457cdbb-fa37-41d4-923c-5ca90d9a6f1b)
### 损失函数
对样本i的预测值为![image](https://github.com/user-attachments/assets/43c28a78-8571-41a9-a357-44dc1540816d)，样本i的真实值为![image](https://github.com/user-attachments/assets/b4c6baf9-9b06-4788-95d2-dfc05c4dae20)，那么平方损失函数如下所示: 

![image](https://github.com/user-attachments/assets/07781323-101a-47ec-ba97-dcb377e094b4) 

其中取1/2这个值并不会影响最终的损失判定，但是便于我们求导。 
具体到计算n个样本产生的损失值，可得下式: 

![image](https://github.com/user-attachments/assets/90c9b359-e225-4279-9bd5-d4fc744d0c9b) 



### 实践-波士顿房价模型
[点击这个链接，查看相关信息](https://github.com/happyeveday/Boston_price)
