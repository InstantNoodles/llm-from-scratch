# 十二周计划

完成一项就把 `[ ]` 改成 `[x]`，然后提交。每周最后一条是完成标准。

> **9/7 调整**：首个周末只完成了装环境和线代 1 到 2 集。W0 剩余部分并入 9/7 到 9/9，W1 顺延 3 天到 9/10 到 9/15，W2 压缩为 9/16 到 9/20 五天，W3 起日期不变。如果本周末再次落空，整体顺延一周，不再压缩。

## W0 · 准备（9/5 周六 – 9/9 周三，顺延 3 天）

- [x] 上周末：装环境，Python 3.11+、VS Code，`pip install torch numpy jupyter matplotlib`
- [x] 上周末：建好本仓库，之后所有代码都放这里
- [x] 上周末：看 3Blue1Brown《线性代数的本质》第 1 到 2 集
- [ ] 周一 9/7：看《线性代数的本质》第 3 到 5 集，线性变换、矩阵乘法即复合、三维变换
- [ ] 周一 9/7：NumPy 上手 30 分钟，创建数组、索引切片，每次都打印 `shape`
- [ ] 周二 9/8：看第 7 到 9 集，逆矩阵与列空间、非方阵、点积。第 6 集行列式跳过
- [ ] 周二 9/8：看 3Blue1Brown《神经网络》第 1 到 2 集
- [ ] 周三 9/9：NumPy 练习 1 小时，broadcasting、reshape、sum(axis=…)，每个先预测 shape 再运行
- [ ] 周三 9/9：跑通 `torch.randn(3,4) @ torch.randn(4,5)`，把自测答案写进 `notes.md` 并提交
- [ ] **完成标准**：不运行就能写出 `(32,10) @ (10,5)` 的结果形状，并用一句话解释矩阵乘法在做什么

## W1 · micrograd：手写反向传播（9/10 周四 – 9/15 周二，顺延 3 天）

- [ ] 周四到周五：跟《building micrograd》视频前半，到手动算 backward 那段为止，边看边敲
- [ ] 周六：把视频后半敲完，拓扑排序的 `backward()`、tanh、Neuron / Layer / MLP 类
- [ ] 周六：看 3Blue1Brown《神经网络》第 3 到 4 集，和自己的代码对照
- [ ] 周日：关掉视频，从空文件重写 `Value` 类和 `backward()`，对比原版
- [ ] 周日：开始用自己的 micrograd 训练两层 MLP 做二分类
- [ ] 下周一到周二 9/14 到 9/15：完成 MLP 二分类，画出决策边界，代码提交到 `week01-micrograd/`
- [ ] **完成标准**：能默写 `__add__` 和 `__mul__` 的 backward，并说清链式法则在 `backward()` 里怎么体现

## W2 · bigram 与 MLP 语言模型（9/16 周三 – 9/20 周日，压缩为 5 天）

- [ ] 周三：makemore Part 1，bigram 模型
- [ ] 周四到周五：makemore Part 2，MLP。重点理解 embedding、隐藏层、softmax、交叉熵
- [ ] 周末：换一份自己找的数据集跑 MLP
- [ ] 周末：调 embedding 维度和隐藏层大小，记录 loss 变化
- [ ] **完成标准**：能解释交叉熵为什么是负对数似然，以及 train loss 与 val loss 分开看的意义

## W3 · 训练的内部细节（9/21 – 9/27）

- [ ] 周一到周三：makemore Part 3，激活值分布、梯度、BatchNorm
- [ ] 周四到周日：makemore Part 4《Becoming a Backprop Ninja》，手推每一步梯度。全程最难的一周，允许卡住
- [ ] **完成标准**：手写 softmax + 交叉熵的反向传播，与 PyTorch autograd 的结果对上

## W4 · 巩固与缓冲（9/28 – 10/4，含国庆）

- [ ] 周一到周二：makemore Part 5，WaveNet，把模型模块化成 `nn.Module` 风格
- [ ] 国庆：补前三周没完成的内容
- [ ] 国庆（都完成的话）：PyTorch 官方 60 分钟教程，把手写部分换成 `torch.nn` 版本
- [ ] **完成标准**：不看资料写出标准 PyTorch 训练循环：模型、优化器、前向、loss、zero_grad、backward、step

## W5 · 手写 GPT 上：attention（10/5 – 10/11）

- [ ] 周一到周二：《Let's build GPT》前半，数据加载、字符级 tokenizer、bigram baseline
- [ ] 周三到周五：self-attention 推导，下三角 mask、Q/K/V、为什么除以 sqrt(d_k)
- [ ] 周末：关视频，从零写出单头 attention，验证输出 shape
- [ ] **完成标准**：能画出一次 attention 的数据流，并标出每个中间张量的 shape

## W6 · 手写 GPT 下：拼装与训练（10/12 – 10/18）

- [ ] 周一到周三：多头注意力、前馈层、残差连接、LayerNorm、Dropout
- [ ] 周四到周五：拼装成完整 GPT，在莎士比亚数据集上训练
- [ ] 周末：换成中文文本训练，生成样本
- [ ] 周末：写一篇 500 字笔记，解释 Transformer 每一层在做什么
- [ ] **完成标准 · 核心里程碑**：合上所有资料，从空文件写出可运行的 GPT，并训练出能生成通顺片段的结果

## W7 · Tokenizer：手写 BPE（10/19 – 10/25）

- [ ] 周一到周四：《Let's build the GPT Tokenizer》，手写 BPE
- [ ] 周五到周日：把 GPT 从字符级换成 BPE 分词，对比效果
- [ ] **完成标准**：能解释 BPE 的 merge 过程，并说出词表大小对模型的影响

## W8 · 真正训练一个模型（10/26 – 11/1）

- [ ] 读 nanoGPT 源码，列出与自己版本的差异
- [ ] 学会用 GPU 训练，本地没有显卡就用 Colab 或 Kaggle
- [ ] 加上学习率 warmup、cosine decay、混合精度、checkpoint 保存
- [ ] 训练一个 10M 参数级别的模型，跑 30 分钟以上，保存后能加载并生成文本
- [ ] **完成标准**：本仓库 README 里有训练出的模型的生成样例

## W9–12 · 加深（11/2 – 11/29）

- [ ] 读《Attention Is All You Need》原文
- [ ] 读 GPT-2 论文，列出它和自己模型的差别
- [ ] 三选一：KV cache / RoPE / 用 HuggingFace 微调开源小模型
- [ ] 写一篇完整博客，讲清楚从零写出 GPT 的全过程
- [ ] **完成标准**：博客发布，别人照着能复现
