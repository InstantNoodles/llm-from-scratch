# llm-from-scratch

十二周自学计划：从 100 行的 micrograd 到能在 GPU 上训练 10M 参数模型的 nanoGPT。

- 起止：2026-09-05（周六）到 2026-11-29（周日）
- 投入：工作日每天 1.5 小时，周末每天 3 小时，每周约 13.5 小时
- 主线教材：Andrej Karpathy《Neural Networks: Zero to Hero》
- 在线进度清单：<https://claude.ai/code/artifact/80314e5d-f5af-408f-98ee-d216fbe97bb3>
- 本仓库内的清单副本：[docs/index.html](docs/index.html)（可开 GitHub Pages）

## 仓库结构

```
PLAN.md              十二周计划的 Markdown 勾选清单，完成一项改成 [x] 后提交
notes.md             每日学习日志，每天 3 到 5 行
docs/index.html      网页版清单
week00-setup/        环境、线代补课、NumPy 练习
week01-micrograd/    手写自动求导
week02-makemore-1/   bigram 与 MLP 语言模型
week03-makemore-2/   BatchNorm 与手推反向传播
week04-buffer/       WaveNet、PyTorch 巩固、国庆缓冲
week05-gpt-1/        self-attention
week06-gpt-2/        完整 GPT 拼装与训练
week07-tokenizer/    手写 BPE
week08-train/        nanoGPT、GPU 训练
week09-12-deepen/    论文、进阶实现、博客
```

每周文件夹里有一份 `README.md`，写着那周的任务和完成标准。当周的代码、笔记、训练日志都放进对应文件夹。

## 每天的固定流程

1. 前 10 分钟：不看视频，凭记忆重写昨天的核心代码。
2. 中间：跟视频敲代码，每讲一段就暂停，自己先写。
3. 后 10 分钟：在 `notes.md` 写 3 到 5 行，然后 `git commit`。

## 三条规则

1. 允许落后，不允许跳过。
2. 卡住超过 30 分钟就换方式。
3. 每周日晚回顾 15 分钟，完成标准没达到的下周先补。

## 环境

```bash
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
```
