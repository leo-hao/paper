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

