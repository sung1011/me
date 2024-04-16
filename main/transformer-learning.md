# transformer learning

    由 Vaswani 等人于 2017 年提出, 用于自然语言处理
    由多个 encoder 和 decoder 组成, 用于处理序列数据
    属于自然语言处理(NLP)领域的模型

## 相关模型

- `GPT` 通过单向语言模型预训练, 用于生成文本
- [BERT](ai-bert.md) 通过双向语言模型预训练, 用于理解文本
- `T5`  通过encoder-decoder模型预训练, 用于生成和理解文本

## 相关算法

## 组成

input_embedding -> positional_encoding -> encoder

output_embedding -> positional_encoding -> decoder -> linear -> softmax

### input embedding

    词意信息
    将输入的词句分割成token. 如 "women" -> ["women", "and", "man"]
    每个token传入 embedding (嵌入)层转换成词向量. 如 "women" -> [0.1, 0.4, 0.3, 0.5, ...]
    向量的每个维度代表一个特征, 通过训练学习到的, 用于表示词的语义
    可以通过向量空间中的距离, 得到其与其他词的相关性

    e.g.: women 的向量与 queen, girl 相关性更高, 与 king 相关性更低, 与 apple 相关性非常低

### positional encoding

    顺序信息
    由于 transformer 没有循环结构, 无法处理序列的顺序
    通过添加位置编码, 使模型能够学习到序列的顺序信息
    位置编码是一个与词向量相加的向量, 用于表示词的位置信息

### encoder

    捕捉特征
    由多个 self-attention 层组成, 用于提取输入序列的特征

    self-attention
    通过计算输入序列中每个词与其他词的相关性, 来提取特征
    通过 QKV 矩阵计算, 得到每个词的注意力分布(相关性)

    e.g.: the animal didn't cross the street because [it] was too tired
    it可以指animal, street, cross, tired, 通过计算得到it与其他词的相关性, 从而确定it指向animal

> `多个 self-attention 层` 关注侧重不同, 可以并行计算.如 情感, 动词, 修饰词...

> `BERT` 的预训练阶段就是通过 encoder 来学习文本的双向表示

### decoder

    由多个 self-attention 层和 encoder-decoder attention 层组成, 用于生成输出序列
    与encoder不同的是 decoder 是单向的, 只能看到一句话中已生成的词

> `GPT` 的预训练阶段就是通过 decoder 来学习文本的单向表示

### linear

    将 decoder 的输出通过线性变换, 使其维度与词表大小相同

### softmax

    将线性变换的结果通过 softmax 函数, 得到每个词的概率

### output embedding

    将 softmax 的结果通过 embedding 层, 得到输出词的词向量

> `预训练 pre-train`

    捕获数据中的一般特征，便于在特定任务上进行微调(fine-tune)
    主要优点是可以利用大量的无标签数据来学习有用的特征
    为后续任务提供更好的初始化参数
