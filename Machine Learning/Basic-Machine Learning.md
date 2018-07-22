# ML- Basic
- 【机器学习基本理论】详解最大似然估计（MLE）、最大后验概率估计（MAP），以及贝叶斯公式的理解
- 似然与极大似然估计
	- https://zhuanlan.zhihu.com/p/22092462
	- 概率是在特定环境下某件事情发生的可能性
	- 而似然刚好相反，是在确定的结果下去推测产生这个结果的可能环境（参数）
	- ![](https://www.zhihu.com/equation?tex=%5Cmathcal%7BL%7D%28%5Ctheta%7Cx%29+%3DP%28x%7C%5Ctheta%29)
	- 解释了硬币问题的似然估计方法
- 入门 | 什么是最大似然估计、最大后验估计以及贝叶斯参数估计
	- 机器之心

## Evaluate
+ https://www.zhihu.com/question/30643044
+ accuracy
+ P R F1
+ ROC/AUC
	+ https://www.douban.com/note/284051363/

## 判别模型和生成模型
+ Reference
	+ http://www.cnblogs.com/zhangchaoyang/articles/7100083.html
	+ http://www.cnblogs.com/kaituorensheng/p/3379170.html
+ 生成模型：
	+ 直接求联合概率p(x,y)，得到p(x,y)后就可以去生成样本。
	+ HMM、高斯混合模型GMM、LDA、PLSA、Naive Bayes都属于生成模型。
	+ 当我们得到HMM模型后，就可以根据初始状态分布π、状态转移矩阵A和发射矩阵B去生成一个状态序列及相应的观察序列，即拿着生成模型可以去生成样本。
	+ LDA（或PLSA）模型也一样，得到文档下的主题分布p(zk|di)及主题下的词分布p(wj|zk)后，上帝就可以去创作文章了。

+ 判别模型：
	+ 直接求判别（或者是预测）函数y=(f(x)，或者另一种表达：p(y|x)。
	+ 最大熵MaxEnt、人工神经网络ANN、逻辑回归LR、线性判别分析LDA、K-Means、KNN、SVM、决策树都属于判别模型。
	+ 最大熵直接去求p(y|x)，它不会浪费功夫去求p(x,y)
	+ 同样KNN也不关心样本是如何生成的，它只会对样本进行分类。

+ 由生成模型可以得到判别模型，因为p(y|x)=p(x,y)p(x)，但它有2个缺点：
	+ 需要额外地去求p(x)。
	+ 样本量不足的情况下p(x)可能求不准。此时预测p(y|x)没有判别模型准。

+ 生成模型也有它的优点：
	+ 可以生成样本，反应样本本身的相似度
	+ 比如LDA中得到了p(zk|di)就相当于得到了文档向量，可以去计算向量之间的相似度。
+ 当含有隐含变量时，也可以用生成模型，但不能用判别模型。比如HMM、GMM、LDA、PLSA模型都可以用EM算法求解。

## loss function
+ 机器学习部分参照 svm 中得loss
+ PGM 部分参照 PGM 中得推导

## 参数估计
+ MLE
+ EM

## 训练方法
+ 梯度下降
+ 拟牛顿

## 优化方法（数值计算，代替求导）
+ 参考 统计学习方法 P88
+ 对似然函数进行优化
	+ IIS 改进得迭代尺度
	+ 拟牛顿