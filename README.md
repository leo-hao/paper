# paper

## 1. Anti-aliasing Semantic Reconstruction for Few-Shot Semantic Segmentation

- 将小样本分割重新表述为语义重建的问题
- 提出了anti-aliasing semantic reconstruction (ASR)
- 将基类特征转成基向量，张成一个语义空间，即semantic span
- 在训练期间，ASR利用语义空间，最大化基向量的正交性，最小化基类semantic aliasing ，帮助reconstruct新类
- 在推理期间，ASR利用semantic filtering 抑制语义干扰，精确激活目标物体区域
- 作者 | Binghao Liu, Yao Ding, Jianbin Jiao, Xiangyang Ji, Qixiang Ye
- 单位 | 国科大；清华
- 论文 | <https://link.zhihu.com/?target=https%3A//arxiv.org/abs/2106.00184>
- 代码 | <https://link.zhihu.com/?target=https%3A//github.com/Bibkiller/ASR>

## 2. Semantic Segmentation with Generative Models: Semi-Supervised Learning and Strong Out-of-Domain Generalization

- 提出一个完全生成性方法进行语义分割，基于SyleGAN2，允许半监督训练，并且展示了强大的泛化性
- 作者 | Daiqing Li, Junlin Yang, Karsten Kreis, Antonio Torralba, Sanja Fidler
- 单位 | 英伟达；多伦多大学；耶鲁大学；麻省理工学院；Vector Institute
- 论文 | <https://link.zhihu.com/?target=https%3A//arxiv.org/abs/2104.05833>
- 主页 | <https://link.zhihu.com/?target=https%3A//nv-tlabs.github.io/semanticGAN/>

## 3. Railroad is not a Train: Saliency as Pseudo-pixel Supervision for Weakly Supervised Semantic Segmentation

- 弱监督
- 作者 | Seungho Lee, Minhyun Lee, Jongwuk Lee, Hyunjung Shim
- 单位 | 延世大学；成均馆大学
- 论文 | <https://link.zhihu.com/?target=https%3A//arxiv.org/abs/2105.08965>
- 代码 | <https://link.zhihu.com/?target=https%3A//github.com/halbielee/EPS>


## 4. HyperSeg: Patch-wise Hypernetwork for Real-time Semantic Segmentation

- 实时
- 作者 | Yuval Nirkin, Lior Wolf, Tal Hassner
- 单位 | Facebook；巴-伊兰大学；以色列特拉维夫大学
- 论文 | <https://link.zhihu.com/?target=https%3A//arxiv.org/abs/2012.11582>
- 代码 | <https://link.zhihu.com/?target=https%3A//github.com/YuvalNirkin/hyperseg>

## 5. Self-supervised Augmentation Consistency for Adapting Semantic Segmentation

- 本次工作提出一种既实用又高度准确的语义分割域适应方法。与以前的工作相比，放弃了使用涉及计算的对抗性目标、网络集成和风格迁移。而是采用标准的数据增强技术：光度噪声、翻转和缩放，并确保语义预测在这些图像转换中的一致性。通过简单的增强技术和 momentum 更新，显著提高了最先进的分割精度。
- 作者 | Nikita Araslanov, Stefan Roth
- 单位 | 达姆施塔特工业大学；hessian.AI
- 论文 | <https://link.zhihu.com/?target=https%3A//arxiv.org/abs/2105.00097>
- 代码 | <https://link.zhihu.com/?target=https%3A//github.com/visinf/da-sac>


## 6. Learning Calibrated Medical Image Segmentation via Multi-rater Agreement Modeling

- 在医学图像分析中，典型的做法是收集多个标注，每个标注都来自不同的临床专家或评分者，减少可能出现的诊断误差。同时，从计算机视觉从业者的角度来看，通常的做法是采用通过多数票或简单地从首选评分者那里获得的基础ground-truth 标签。但这一过程往往忽略了原始的多评判员标注中所蕴含丰富的一致或分歧信息。
- 针对此，提出一个新的模型，MRNet。首先，设计一个expertiseaware inferring 模块或 EIM，将各个评分者的专业水平作为先验知识嵌入其中，以形成高层次的语义特征。其次，该方法能够从粗略的预测中重建多评判者的等级，并进一步利用多评判者（不）一致的线索来提高分割的性能。
- 作者称这是首个在不同专业水平下为医学图像分割产生校准预测的工作。并在不同成像模式的五个医学分割任务中进行了广泛的经验性实验。结果表明，MRNet 与最先进的技术相比，性能卓越，也验证了 MRNet 在广泛的医学分割任务中的有效性和适用性。
- 作者 | Wei Ji、Shuang Yu、Junde Wu、Kai Ma、Cheng Bian、 Qi Bi、Jingjing Li、Hanruo Liu、Li Cheng、 Yefeng Zheng
- 单位 | 腾讯天衍实验室；阿尔伯塔大学；首都医科大学
- 论文 | <https://link.zhihu.com/?target=https%3A//openaccess.thecvf.com/content/CVPR2021/papers/Ji_Learning_Calibrated_Medical_Image_Segmentation_via_Multi-Rater_Agreement_Modeling_CVPR_2021_paper.pdf>
- 代码 | <https://link.zhihu.com/?target=https%3A//github.com/jiwei0921/MRNet/>

# Domain Adaptive Semantic Segmentation

## 1.Prototypical Pseudo Label Denoising and Target Structure Learning for Domain Adaptive Semantic Segmentation

- 固定prototypical 特征，通过距离计算伪标签，在线训练更新权重；
- 同时根据同一个目标的两个不同的视图相对于原型对齐距离，来产生紧凑的特征空间
- Synthetic-to-Real Translation on GTAV-to-Cityscapes Labels数据集上排名第二2021-11-17
- 作者 | Pan Zhang *, Bo Zhang, Ting Zhang, Dong Chen, Yong Wang, Fang Wen
- 单位 | University of Science and Technology of China, Microsoft Research Asia
- 论文 | https://arxiv.org/abs/2101.10979
- 代码 | https://github.com/microsoft/ProDA

## 2.DSP: Dual Soft-Paste for Unsupervised Domain Adaptive Semantic Segmentation

- 提出了一种新颖的双软粘贴 (DSP)创建具有较小域的新中间域的方法差距。 基于平均教师框架，进行DSP诱导的输出级对齐和特征级对齐，其中有助于学习域不变特征。
- 此外，长尾类DSP 中使用的第一个采样策略显示了它在解决类不平衡问题方面的有效性。 
- Synthetic-to-Real Translation on GTAV-to-Cityscapes Labels数据集上排名第二2021-11-17
- 作者 | Li Gao, Jing Zhang, Lefei Zhang, and Dacheng Tao
- 单位 | Wuhan University, The University of Sydney, JD Explore Academy
- 论文 | https://arxiv.org/pdf/2107.09600v3.pdf
- 代码 | https://github.com/GaoLii/DSP

## 3.DACS: Domain Adaptation via Cross-domain Mixed Sampling

- 提出了一种用于语义分割无监督自适应的新算法，跨域混合的域自适应，用于解决朴素混合强制一致性造成的混淆问题。进一步提升了域适应的表现。
- 作者 | Wilhelm Tranheden1,2*, Viktor Olsson1,2*, Juliano Pinto1, Lennart Svensson1
- 单位 | 1Chalmers University of Technology, Gothenburg, Sweden 2Volvo Cars, Gothenburg, Sweden
- 论文 | https://arxiv.org/abs/2007.08702
- 代码 | https://github.com/vikolss/DACS

## 4.Domain Adaptive Semantic Segmentation with Self-Supervised Depth Estimation

- ICCV21，用辅助任务深度估计弥合领域差异，提出的自监督学习目标域的深度，自注意力显示学习语义和深度的关系，将源域知识共享到目标域，最后整合到一个现有的自训练框架DACS
- 作者 | Qin Wang1 Dengxin Dai1,2*Lukas Hoyer1 Luc Van Gool1,3 Olga Fink
- 单位 | 1ETH Zurich, Switzerland 2MPI for Informatics, Germany 3KU Lueven, Belgium
- 论文 | http://arxiv.org/abs/2104.13613
- 代码 | https://qin.ee/corda

## 5. Dual Path Learning for Domain Adaptation of Semantic Segmentation
- DPL包含两个分别互补和交互的源域、目标域适应管道。DPL的推理非常简单，只采用目标域中的一种分割模型。新技术：提出的双路图像迁移、双路适应分割，使两条路径以一种交互的方式提出对方。
- 作者 | Yiting Cheng1 Fangyun Wei* 2Jianmin Bao2 Dong Chen2 Fang Wen2 Wenqiang Zhang*1
- 单位 | 1Fudan University 2Microsoft Research Asia
- 论文 | https://arxiv.org/pdf/2108.06337.pdf
- 代码 |  https://github.com/royee182/DPL

## 6.PixMatch: Unsupervised Domain Adaptation via Pixelwise Consistency Training

- 我们引入一种一致性损失项，模型预测目标图像和预测相同带扰动的图片之间的差距，并且研究比较了四种不同扰动的影响：强数据增强、风格迁移、CutMix、傅里叶变换，相比下对于流行的对抗性适应方法，我们的方法更简单、更容易实现、内存效率更高在训练中
- 作者 | Luke Melas-Kyriazi, Arjun K. Manrai
- 单位 | Harvard University...
- 论文 | https://arxiv.org/abs/2105.08128
- 代码 | https://github.com/lukemelas/pixmatch

## 7.SegFormer: Simple and Efficient Design for Semantic Segmentation with Transformers

- Transformers与轻量级多层感知器（MLP）统一起来；1. 分层结构的transformers编码器，并且不需要位置编码:MixFFN；2.避免使用复杂的解码器，MLP聚合了不同层的信息
- 网络更小，效果也佳
- 作者 | Enze Xie1, Wenhai Wang2, Zhiding Yu3, Anima Anandkumar3,4, Jose M. Alvarez3, Ping Luo1
- 单位 | The University of Hong Kong 2Nanjing University 3NVIDIA 4Caltech
- 论文 | https://arxiv.org/abs/2105.15203
- 代码 | https://github.com/NVlabs/SegFormer
