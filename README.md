# paper

## 1. Anti-aliasing Semantic Reconstruction for Few-Shot Semantic Segmentation
- 将小样本分割重新表述为语义重建的问题
- 提出了anti-aliasing semantic reconstruction (ASR)
- 将基类特征转成基向量，张成一个语义空间，即semantic span
- 在训练期间，ASR利用语义空间，最大化基向量的正交性，最小化基类semantic aliasing ，帮助reconstruct新类
- 在推理期间，ASR利用semantic filtering 抑制语义干扰，精确激活目标物体区域

