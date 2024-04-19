# unsupervised learning 非监督学习

## 相关模型

## 相关算法

### clustering 聚类

将数据集划分为几个组或"集群"，使得同一集群内的数据点之间的相似度尽可能高，而不同集群的数据点之间的相似度尽可能低。

- [K-means](algo-kmeans.md) K均值

      通过迭代的方式将数据集划分为K个簇, 使得每个样本点到簇中心的距离最小

- [hierarchical connectivity](algo-hierarchical-connectivity.md) 层次聚类

      通过计算样本之间的相似度, 逐步合并相似度最高的样本, 构建一棵树

- [bayesian clustering](algo-bayesian-clustering.md) 贝叶斯聚类

      通过贝叶斯方法对数据进行聚类, 通过后验概率来判断样本属于哪个簇

### dimensionality reduction

将高维数据映射到低维空间，以便更好地可视化和理解数据。

- [PCA](algo-pca.md) 主成分分析 principal component analysis

      通过线性变换将数据投影到低维空间, 保留最大方差的方向作为主成分

- [MDS](algo-mds.md) 多维缩放 multi-dimensional scaling

      通过保留高维数据点之间的距离关系, 将数据映射到低维空间

- [t-SNE] t分布邻域嵌入 t-Distributed Stochastic Neighbor Embedding

      通过保留高维数据点之间的相似度关系, 将数据映射到低维空间

- [LDA] 线性判别分析

      通过最大化类间距离和最小化类内距离, 将数据映射到低维空间

- [autoencoder] 自编码器

      通过神经网络将数据映射到低维空间, 通过重构误差来学习数据的表示

- [SVD] 奇异值分解

      通过分解数据矩阵, 将数据映射到低维空间
