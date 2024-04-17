# Naive Bayes classifier 朴素贝叶斯

朴素贝叶斯分类器是一种基于贝叶斯定理的简化概率分类器。
它是一种快速的、简单的、基于概率的分类器，适用于大规模的数据集。
朴素贝叶斯分类器假设特征之间相互独立。

## 表达

P(C|X) = P(X|C) * P(C) / P(X)

## 实例

- 流行病分析

| type    | fever(√) | fever(×) | sneezing(√) | sneezing(×) | runny nose(√) | runny nose(×) | sick total |
| ------- | -------- | -------- | ----------- | ----------- | ------------- | ------------- | ---------- |
| flu     | 400      | 100      | 350         | 150         | 450           | 50            | 500        |
| allergy | 0        | 300      | 150         | 150         | 300           | 0             | 300        |
| cold    | 100      | 100      | 150         | 50          | 50            | 150           | 200        |
| total   | 500      | 500      | 650         | 350         | 800           | 200           | 1000       |

Q:

    新来一个病人 √发烧、×不打喷嚏、√流鼻涕，患flu的概率是多少？

A:

    通过过往数据得到 发烧*不打喷嚏*流鼻涕*流感 连乘就是这些独立事件同事发生的概率

    flu:
    P(flu|X) = P(X|flu) * P(flu) / P(X) = P(fever|flu) * P(no sneezing|flu) * P(runny nose|flu) * P(flu) / P(X)

    P(fever|flu) = 400 / 500 = 0.8
    P(no sneezing|flu) = 150 / 500 = 0.3
    P(runny nose|flu) = 450 / 500 = 0.9
    P(flu) = 500 / 1000 = 0.5
    = 0.8 * 0.3 * 0.9 * 0.5 = 0.108 = 10.8%

    allergy:
    P(allergy|X) = P(X|allergy) * P(allergy) / P(X) = P(fever|allergy) * P(no sneezing|allergy) * P(runny nose|allergy) * P(allergy) / P(X)

    P(fever|allergy) = 0 / 300 = 0
    P(no sneezing|allergy) = 150 / 300 = 0.5
    P(runny nose|allergy) = 300 / 300 = 1
    P(allergy) = 300 / 1000 = 0.3
    = 0 * 0.5 * 1 * 0.3 = 0 = 0%

    cold:
    P(cold|X) = P(X|cold) * P(cold) / P(X) = P(fever|cold) * P(no sneezing|cold) * P(runny nose|cold) * P(cold) / P(X)

    P(fever|cold) = 100 / 200 = 0.5
    P(no sneezing|cold) = 50 / 200 = 0.25
    P(runny nose|cold) = 50 / 200 = 0.25
    P(cold) = 200 / 1000 = 0.2
    = 0.5 * 0.25 * 0.25 * 0.2 = 0.00625 = 0.625%

    流感概率最大10.8%

- 垃圾邮件分类