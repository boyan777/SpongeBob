# SpongeBob-Pro

> 一个从零实现的大语言模型训练框架，完整覆盖 Tokenizer 训练、预训练（Pretrain）、监督微调（SFT）以及 GRPO 强化学习对齐等核心流程。

---

# 项目简介

SpongeBob-Pro 是一个端到端的大语言模型（LLM）训练项目，旨在以清晰的工程结构复现现代大语言模型训练的完整流程。

本项目实现了从 **文本数据 → Tokenizer → 预训练 → 指令微调 → 强化学习对齐** 的完整 pipeline。

适合作为：

* 大模型原理学习项目
* LLM 工程实践项目
* AI / 软件工程面试项目
* Transformer 结构学习项目

---

# 项目特性

* 完整的大模型训练 Pipeline
* Decoder-only Transformer 实现
* 支持 Tokenizer 训练
* 支持语言模型预训练
* 支持 SFT（Supervised Fine-tuning）
* 支持 GRPO 强化学习对齐
* 模块化代码结构

---

# 项目结构

```
SpongeBob-Pro/
├── benchmark/          # benchmark评测
├── data/               # 训练数据
├── dataset/            # 数据处理
├── model/              # Transformer模型实现
├── train/              # 训练脚本
├── tokenizer_15k/      # tokenizer文件
├── out_grpo/           # GRPO训练输出
├── eval.py             # 模型评测
└── README.md
```

---

# 技术亮点

## 完整的大模型训练流程

本项目复现了现代 LLM 训练的完整流程：

```
原始文本
   ↓
Tokenizer训练
   ↓
Tokenized Dataset
   ↓
Transformer预训练
   ↓
SFT指令微调
   ↓
GRPO强化学习对齐
   ↓
最终对齐语言模型
```

---

## 主流模型结构

模型实现参考当前主流大模型架构，包括：

* **RoPE（旋转位置编码）**
* **RMSNorm**
* **SwiGLU**
* **Causal Self-Attention**

这些结构被广泛应用于现代大模型中。

---

# 环境配置

推荐环境：

* Python 3.10+
* PyTorch 2.x
* CUDA 11.7+

安装依赖：

```
pip install torch transformers datasets sentencepiece tiktoken swanlab
```

---

# 快速开始

## 克隆项目

```
git clone https://github.com/boyan777/SpongeBob-Pro.git
cd SpongeBob-Pro
```

---

## 训练 Tokenizer

```
python train/train_tokenizer.py
```

---

## 运行预训练

```
python train/pretrain.py
```

---

## 监督微调 SFT

```
python train/train_sft.py
```

---

## GRPO 强化学习训练

```
python train/train_grpo.py
```

---

# 项目用途

本项目适合：

* 学习 Transformer / LLM 原理
* 理解大模型训练流程
* AI / 软件工程面试项目
* 大模型工程实践

---

# 简历项目描述

可以在简历中描述为：

> 从零实现一个大语言模型训练框架，完整复现 Tokenizer 训练、Transformer 自回归预训练、SFT 指令微调以及 GRPO 强化学习对齐流程。模型结构包含 RoPE、RMSNorm 和 SwiGLU 等主流组件，并实现模块化训练流程。
