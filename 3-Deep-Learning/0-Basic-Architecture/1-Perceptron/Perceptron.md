# Perceptron
### 多层感知机为何具有非线性能力？
+ 推到
+ 例子：异或问题
	+ 一层不可分，多层可以

### 浅层模型
+ 浅层模型：含有一个隐层的叫做多层感知机，又叫BP神经网络。
+ 20世纪90年代，出现了各种浅层学习模型，包括：SVM、Boosting、最大熵方法（LR）。它们都可以看做只有一层隐层或没有隐层的神经网络。
+ 浅层模型的问题是：
	1.特征的提取与选择。
	2.表达能力差。
+ 因为只有底层的特征，很难识别出不同目标，高层的特征依靠手工设计很难得到。而根据经验来说，一般网络神经元和层数越多，表达能力越强。