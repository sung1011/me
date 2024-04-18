# supervised learning

## 相关模型

## 相关算法

### Regression

"Regression"（回归）是一种监督学习方法，其目标是预测一个连续的目标变量。回归模型试图理解目标变量与一个或多个特征之间的关系。

- [linear regression](algo-linear-regression.md) 线性回归

      假设目标值与特征之间存在线性关系, 通过最小化平方误差来拟合参数

- [logistic regression](algo-logistic-regression.md) 逻辑回归

      适用于二分类问题, 通过sigmoid函数将线性回归的输出映射到0-1之间

- [regression trees](algo-regression_trees.md) 回归树

      用于处理连续值的预测问题, 通过递归地分割数据集来构建一棵树

- [support vector regression] 支持向量回归

### Classification

"Classification"（分类）是一种监督学习方法，其目标是从已标记的训练数据中学习一个模型，然后用这个模型预测新数据的类别。

- [Decision trees] 决策树

- [K Nearest Neighbor (kNN)](algo-knn.md) k最临近

      通过计算输入样本与训练集中所有样本的距离, 选择距离最近的k个样本中出现最多的类别作为预测结果

- [Naive Bayes classifier](algo-naive-bayes.md) 朴素贝叶斯分类器

      输入给定特征的条件下, 计算每个类别的概率, 选择概率最大的类别作为预测结果

- [Support Vector Machine (SVM)]

- [Neural networks]

### Performance

模型的预测性能，即模型对新数据进行预测的能力。评估模型性能的指标取决于问题的类型（例如，分类、回归、聚类等）和特定的业务需求。

- [overfitting and underfitting](overfitting-underfitting.md) 过拟合和欠拟合

      通过调整模型复杂度来解决过拟合和欠拟合问题

- [confusion matrix](confusion-matrix.md) 混淆矩阵

      用于评估分类模型的性能, 包括准确率, 精确率, 召回率, F1值等

- [unbalanced data] 不平衡数据

      处理不平衡数据的方法, 如过采样, 欠采样, SMOTE等

### Linear Algebra 线性代数

- [L1 norm](l1-norm.md) L1范数

      其元素的绝对值之和

- [L2 norm](l2-norm.md) L2范数

      其元素的平方和的平方根

### data pre-processing 数据预处理

改善数据质量：数据预处理可以帮助我们处理缺失值、异常值和噪声，从而提高数据的质量。
使数据适应模型：许多机器学习模型对输入数据有特定的要求。例如，一些模型需要输入特征具有相同的尺度，一些模型需要数据是正态分布的，等等。数据预处理可以帮助我们将数据转换为模型可以接受的形式。
提高模型性能：通过降维和特征选择，我们可以减少数据的维度，从而减少计算需求。

- [data pre-processing](data-pre-processing.md) 数据预处理

      在训练模型之前对数据进行清洗、转换和归一化的过程