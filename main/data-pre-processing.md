# data pre-processing 数据预处理

在训练模型之前对数据进行清洗、转换和归一化的过程。

## 方法

### 最小-最大缩放（Min-Max Scaling）

它将特征的值缩放到0-1之间。

公式 (x - min) / (max - min)。

实例 (x - 2) / (8 - 2) = 0.5。

选择 包含异常值时

### 标准化（Standardization）

它将特征的值缩放到均值为0，标准差为1的范围内。

公式 (x - mean) / std。

实例 (x - 5) / 2 = 0.5。

选择 不包含异常值时

### 归一化（Normalization）

归一化是指将特征的值缩放到单位范数（向量的长度为1）。

公式 x / ||x||。

实例 (3, 4) / sqrt(3^2 + 4^2) = (0.6, 0.8)。

选择 不包含异常值时

### 分位数转换（Quantile Transformation）

它将特征的值转换为一个均匀分布。

### 离散化（Discretization）

它将连续值转换为离散值。
