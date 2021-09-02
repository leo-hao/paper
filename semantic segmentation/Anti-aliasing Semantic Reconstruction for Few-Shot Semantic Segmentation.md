# Anti-aliasing Semantic Reconstruction for Few-Shot Semantic Segmentation

## Abstract

### 现状

- 经过充分训练数据的特征学习，用少量样本去表示新类，少样本的语义分割取得了令人鼓舞的进展

### 问题

- 特征共享机制，不可避免的在具有相似语义组成理论的新类之间造成语义混淆

### 创新

- 本文里，我们提出了将少样本的分割问题视为语义重建问题，将基本类的特征转化成一系列的基本向量，并张成类级别的语义空间，用于新类重建

### 方法

- 引入对比损失，最大化向量之间的正交性的同时最小化类间语义混叠
- 在重建表示空间内，我们通过查询特征投影到支持向量进行精确的语义激活，来进一步抑制其他类的干扰

### 总结

- 我们的方法为少量样本学习提供了系统、可解释的方法。大量实验，在PASCAL VOC、 MS COCO进行，与之前的工作相比取得了良好的结果

## 1. Introduction

### 动机

- 打标签很贵，并且在一些场景（计算机辅助诊断系统）也不可行。

### 意义

- 少样本分割目的可以概括为：将在充足基类数据上预训练的模型推广到只有几个例子的新类。是一种很有前景的技术

### Fig1

- 我们的模型和传统方法相比。传统方法在基类指定特征空间内表示新类的时，没有考虑语义混叠；我们方法通过构建类级语义空间来实现语义重构，其中基向量正交并减少语义干扰

### 贡献

- 我们提出了一种系统的可解释的抗混叠语义重建方法（ASR）用于少样本语义分割，通过将类特征转成基向量用于语义重建
- 我们提出语义跨度，减少基类和新类的语义混叠。基于语义跨度，进一步提出了语义滤波，消除查询图像的干扰语义
- 当应用于常用数据集时，ASR 以显着的余量改进了先前的方法。 它在two-way少镜头分割设置下也取得了良好的性能。

## 2. Related work

### Semantic Segmentation

- multi-scale feature aggregation：Pyramid scene parsing network.
- atrous spatial pyramid pooling(ASPP): Deeplab: Semantic image segmentation with deep convolutional nets, atrous convolution, and fully connected crfs.
- 问题：这些方法需要大量像素级别的标注，阻碍了他们在真实场景里应用

### Few-shot Learning

- meta learning：贡献了优化方法和数据增强
- metric learning：使用原型模型代表了大部分少样本学习方法，原型模型转换空间语义信息成卷积通道。旨在相似的样本对有高的相似分数。
- 问题：由特征共享机制造成的语义混叠被忽略

### Few-shot Segmentation

- 早期的方法使用参数模型，通过support图片学习特征来分割query图片

	-  Conditional networks for fewshot semantic segmentation: 将 support 特征和 query 图片连接来激活特征对象区域的特征，从而进行分割
	- PGNet 和 DAN 使用图解决语义分割问题，并使用图推理将标签信息传播到查询图像

- 下列少样本分类方法，将prototype向量用作跨通道的语义表示

	-  Similarity guidance network for one-shot semantic segmentation: 使用掩码平均池化将 support 图像里前景信息压缩到原型向量
	- CANet: 由两个分支模型组成，该模型在 support 图像和原型引导的 query 图像之间执行特征比较 
	- PANet: 为每个语义类提供了极具代表性的原型类型，并基于像素匹配对查询图像执行分割
	- CRNet: 提出了一种交叉引用机制，可以同时对支持图像和查询图像进行预测，强制对象的共现，从而改善语义传递
	- PMMs  和 PPNet  建议将对象分解为多个部分，并用混合原型向量表示这些部分以对抗语义mixing。

- 尽管取得了上述进展，但现有方法仍然忽视了语义aliasing 问题，这会导致对象部分的错误（或丢失）分割 

	- SST  和 SimProp  分别引入了自监督微调和相似性传播，它们利用特定类别的语义约束来减少语义aliasing。 然而，没考虑基类特征的正交性，它们仍然受到语义aliasing问题的挑战。

## 3. The Proposed Method

### 3.1. Problem Definition

- 子主题 1

$$
D_{base} D_{novel}
$$

