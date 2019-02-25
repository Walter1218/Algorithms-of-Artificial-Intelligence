# View of DL4NLP
- https://zhuanlan.zhihu.com/p/28710886
	- 信息抽取
	- NER
		- 命名实体识别（NER）的主要任务是将诸如Guido van Rossum，Microsoft，London等的命名实体分类为人员，组织，地点，时间，日期等预定类别。许多NER系统已经创建，其中最好系统采用的是神经网络。
		- 在《Neural Architectures for Named Entity Recognition》文章中，提出了两种用于NER模型。这些模型采用有监督的语料学习字符的表示，或者从无标记的语料库中学习无监督的词汇表达[4]。使用英语，荷兰语，德语和西班牙语等不同数据集，如CoNLL-2002和CoNLL-2003进行了大量测试。该小组最终得出结论，如果没有任何特定语言的知识或资源（如地名词典），他们的模型在NER中取得最好的成绩。
	- POS
		- 在《Part-of-Speech Tagging with Bidirectional Long Short-Term Memory Recurrent Neural Network》工作中，提出了一个采用RNN进行词性标注的系统[5]。该模型采用《Wall Street Journal data from Penn Treebank III》数据集进行了测试，并获得了97.40％的标记准确性。
	- CLF
		- Siwei Lai, Liheng Xu, Kang Liu, and Jun Zhao在论文《Recurrent Convolutional Neural Networks for Text Classification》中，提出了一种用于文本分类的循环卷积神经网络，该模型没有人为设计的特征。该团队在四个数据集测试了他们模型的效果，四个数据集包括：20Newsgroup（有四类，计算机，政治，娱乐和宗教），复旦大学集（中国的文档分类集合，包括20类，如艺术，教育和能源），ACL选集网（有五种语言：英文，日文，德文，中文和法文）和Sentiment Treebank数据集（包含非常负面，负面，中性，正面和非常正面的标签的数据集）。测试后，将模型与现有的文本分类方法进行比较，如Bag of Words，Bigrams + LR，SVM，LDA，Tree Kernels，RecursiveNN和CNN。最后发现，在所有四个数据集中，神经网络方法优于传统方法，他们所提出的模型效果优于CNN和循环神经网络。
	- 语义分析和问题回答
		- 问题回答系统可以自动回答通过自然语言描述的不同类型的问题，包括定义问题，传记问题，多语言问题等。神经网络可以用于开发高性能的问答系统。
		- 在《Semantic Parsing via Staged Query Graph Generation Question Answering with Knowledge Base》文章中，Wen-tau Yih, Ming-Wei Chang, Xiaodong He, and Jianfeng Gao描述了基于知识库来开发问答语义解析系统的框架框架。作者说他们的方法早期使用知识库来修剪搜索空间，从而简化了语义匹配问题[6]。他们还应用高级实体链接系统和一个用于匹配问题和预测序列的深卷积神经网络模型。该模型在WebQuestions数据集上进行了测试，其性能优于以前的方法。
	- 释义检测:  释义检测确定两个句子是否具有相同的含义。
		-  《Detecting Semantically Equivalent Questions in Online User Forums》文中提出了一种采用卷积神经网络来识别语义等效性问题的方法
		-  《 Paraphrase Detection Using Recursive Autoencoder》文中提出了使用递归自动编码器的进行释义检测的一种新型的递归自动编码器架构。
	- 语言生成和多文档总结
		- 《 Natural Language Generation, Paraphrasing and Summarization of User Reviews with Recurrent Neural Networks》中，描述了基于循环神经网络（RNN）模型，能够生成新句子和文档摘要的。
	- 机器翻译
	- 语音识别
		- 在《Convolutional Neural Networks for Speech Recognition》文章中，科学家以新颖的方式解释了如何将CNN应用于语音识别，使CNN的结构直接适应了一些类型的语音变化，如变化的语速
	- 字符识别
		- 字符识别系统具有许多应用，如收据字符识别，发票字符识别，检查字符识别，合法开票凭证字符识别等。文章《Character Recognition Using Neural Network》提出了一种具有85％精度的手写字符的方法
	- 拼写检查
		- 大多数文本编辑器可以让用户检查其文本是否包含拼写错误。神经网络现在也被并入拼写检查工具中。
		- 在《Personalized Spell Checking using Neural Networks》，作者提出了一种用于检测拼写错误的单词的新系统。
