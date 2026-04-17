# 第六章 基于 transformers 的 LLM 训练  AMD ROCm 版本

<div align='center'>

[![AMD](https://img.shields.io/badge/AMD-ROCm-ED1C24)](https://rocm.docs.amd.com/)

</div>

注：本章的核心内容是，基于 transformers 框架实现 LLM 预训练和微调

1. 框架简述：
   1. transformers
   2. deepspeed
   3. peft
   4. wandb
   5. tokenizers
2. 基于 transformers 的 LLM 预训练
   1. 分词器训练
   2. 数据集构建
   3. 模型搭建/继承预训练模型
   4. 构造 Trainer 进行训练
3. 基于 transformers 的 LLM SFT/下游任务微调
   1. 分词器训练
   2. 数据集构建
   3. LoRA 配置
   4. 继承预训练模型
   5. 构造 Trainer 进行训练