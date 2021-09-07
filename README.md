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

- 作者 | Seungho Lee, Minhyun Lee, Jongwuk Lee, Hyunjung Shim
- 单位 | 延世大学；成均馆大学
- 论文 | <https://link.zhihu.com/?target=https%3A//arxiv.org/abs/2105.08965>
- 代码 | <https://link.zhihu.com/?target=https%3A//github.com/halbielee/EPS>
