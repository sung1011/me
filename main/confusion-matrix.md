# confusion matrix 混淆矩阵

混淆矩阵是用于评估分类模型性能的一种方法, 通过统计模型预测结果与真实标签之间的关系, 可以计算出准确率, 精确率, 召回率, F1值等指标.

## 混淆矩阵结构

|        | 预测正例 | 预测负例 |
| ------ | -------- | -------- |
| 真正例 | TP       | FN       |
| 真负例 | FP       | TN       |

真正例（True Positive，TP）：实际为正例且模型预测为正例的实例数量。

假负例（False Negative，FN）：实际为正例但模型预测为负例的实例数量。这也被称为“漏报”。

假正例（False Positive，FP）：实际为负例但模型预测为正例的实例数量。这也被称为“误报”。

真负例（True Negative，TN）：实际为负例且模型预测为负例的实例数量。

> 正例（Positive）：这是我们关注的类别，通常被标记为1。例如，在垃圾邮件检测中，所有垃圾邮件都被视为正例；在疾病检测中，所有疾病的病例都被视为正例。

> 负例（Negative）：这是我们不关注的类别，通常被标记为0。例如，在垃圾邮件检测中，所有非垃圾邮件都被视为负例；在疾病检测中，所有健康的病例都被视为负例。

## 混淆矩阵指标

### 准确率 Accuracy

准确率是分类模型预测正确的样本数量占总样本数量的比例:

    Accuracy = (TP + TN)/(TP + TN + FP + FN)

### 精确率 Precision

精确率是分类模型预测为正例的样本中真正例的比例:

    Precision = TP/(TP + FP)

### 召回率 Recall

召回率是分类模型预测出的正例占总正例的比例:

    Recall = TP/(TP + FN)

### F1值 F1 Score

F1值是精确率和召回率的调和平均:

    F1 = 2 * Precision * Recall / (Precision + Recall)

### 特定情况下的混淆矩阵指标

- 假正例率 FPR(False Positive Rate, false alarm): FP/(FP + TN)
- 假负例率 FNR(False Negative Rate, missed alarm): FN/(TP + FN)
- 真正例率 TPR(True Positive Rate, sensitivity): TP/(TP + FN)
- 真负例率 TNR(True Negative Rate, specificity): TN/(FP + TN)
- 特异度 Specificity: 真负例率 TNR
- 命中率 Hit Rate: 真正例率 TPR
- 假发现率 False Discovery Rate: 假正例率 FPR
- 假遗漏率 False Omission Rate: 假负例率 FNR

## 实例

|        | 预测正例 | 预测负例 |
| ------ | -------- | -------- |
| 真正例 | 1000     | 100      |
| 真负例 | 200      | 700      |

- TP = 1000
- FP = 100
- FN = 200
- TN = 700

计算准确率:

    Accuracy = (1000 + 700)/(1000 + 700 + 100 + 200) = 0.85

计算精确率:

    Precision = 1000/(1000 + 100) = 0.91

计算召回率:

    Recall = 1000/(1000 + 200) = 0.83

计算F1值:

    F1 = 2 * 0.91 * 0.83 / (0.91 + 0.83) = 0.87