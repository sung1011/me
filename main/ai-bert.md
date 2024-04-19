# BERT

    Bidirectional Encoder Representations from Transformers
    通过预训练学习文本的双向表示, 用于下游任务

## model

### BERT MLM

    Masked Language Model, 自我填空, 通过上下文预测中间词
    如通过训练 "树上掉下来的[苹果]可以做成好喝的果汁". 今后遇到 树, 果汁, 好喝 就会提高推断出[mask]为苹果的概率.

1. 输入句子：

         "The cat sat on the [MASK]."

2. BERT 模型：

         +-------------------+
         |                   |
         |     BERT Model    |
         |                   |
         +-------------------+

3. 预测的单词：

         "mat"

4. 上下文信息：

         "The cat sat on the"

### BERT NSP

    Next Sentence Prediction, 通过上下文预测两个句子是否有关联

1. 输入句子对：

         Sentence A: "The cat sat on the mat."
         Sentence B: "It was comfortable."

2. BERT 模型：

         +-------------------+
         |                   |
         |     BERT Model    |
         |                   |
         +-------------------+

3. 预测结果：

         "Is Sentence B the next sentence of Sentence A? Yes"

## 预训练任务 微调阶段

### case 1 情感分析

    判断一句话是积极还是消极

1. 输入句子：

         "I love this product! It's amazing!"

2. BERT 模型：

         +-------------------+
         |                   |
         |     BERT Model    |
         |                   |
         +-------------------+

3. 预测结果：

         Positive

### case 2 分析句中单词的词性

    判断一句话中每个词的词性

1. 输入句子：

         "The cat sat on the mat."

2. BERT 模型：

         +-------------------+
         |                   |
         |     BERT Model    |
         |                   |
         +-------------------+

3. 预测结果：

         The (Det), cat (Noun), sat (Verb), on (Prep), the (Det), mat (Noun)

### case 3 输入2个句子 输出1个类别

    判断两句话是有有关联

### case 4 输入文档和问题 输出答案

    输入文档和问题, 输出答案, 答案是文档中的一个词或一句话

1. 输入文档：

         "Albert Einstein was a German-born theoretical physicist. He developed the theory of relativity."

2. 输入问题：

         "Who developed the theory of relativity?"

3. BERT 模型：

         +-------------------+
         |                   |
         |     BERT Model    |
         |                   |
         +-------------------+

4. 预测结果：

         "Albert Einstein"