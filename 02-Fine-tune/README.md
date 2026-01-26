<div align=center>
  <h1>02-Fine-tune</h1>
  <strong>🔧 ROCm 大模型微调实践</strong>
</div>

<div align="center">

*在 AMD GPU 上进行高效模型微调*

[返回主页](../README.md)

</div>

## 简介

&emsp;&emsp;本模块提供在 AMD GPU 上微调大语言模型的完整教程。通过本教程，你将学习如何使用 ROCm 平台对开源大模型进行微调，打造专属于你的领域模型。

&emsp;&emsp;微调（Fine-tuning）是将预训练大模型适配到特定任务或领域的重要技术。在 AMD GPU 上，你可以使用 LoRA、QLoRA 等高效微调方法，以较低的成本完成模型定制。

## 教程列表

### 大模型零基础微调教程

&emsp;&emsp;本教程从零开始介绍大模型微调的基本概念和实践方法，适合初次接触微调的学习者。

- **适合人群**：零基础用户、希望了解微调原理的学习者
- **难度等级**：⭐⭐
- **预计时间**：2 小时

**核心内容：**
- 微调基础概念（Full Fine-tuning、LoRA、QLoRA）
- 数据集准备与格式化
- 训练参数配置
- 模型评估与导出

📖 [开始学习零基础微调教程](./Basic-Finetune/README.md)

---

### 大模型单机微调脚本

&emsp;&emsp;本教程提供可直接使用的单机微调脚本，帮助你快速在 AMD GPU 上启动微调任务。

- **适合人群**：有一定基础、希望快速实践的开发者
- **难度等级**：⭐⭐⭐
- **预计时间**：1.5 小时

**核心内容：**
- 单卡 LoRA 微调脚本
- 单卡 QLoRA 微调脚本
- 常用模型微调配置示例
- 训练监控与日志分析

📖 [开始学习单机微调教程](./Single-GPU-Finetune/README.md)

---

### 大模型多机多卡微调教程

&emsp;&emsp;本教程介绍如何在多台机器、多张 AMD GPU 上进行分布式微调，适用于大规模模型训练场景。

- **适合人群**：有分布式训练需求的高级用户
- **难度等级**：⭐⭐⭐⭐
- **预计时间**：3 小时

**核心内容：**
- RCCL 分布式通信配置
- DeepSpeed 集成与配置
- 多节点训练启动脚本
- 分布式训练调优技巧

📖 [开始学习多机多卡微调教程](./Multi-GPU-Finetune/README.md)

---

## 环境要求

### 硬件要求

- AMD GPU（支持 ROCm，建议 MI250/MI300 或 RX 7900 系列）
- 单卡微调建议显存 16GB+
- 多卡微调建议每卡显存 24GB+

### 软件要求

- 操作系统：Linux (Ubuntu 22.04+)
- ROCm 7.10.0 或更高版本
- Python 3.10+
- PyTorch 2.0+（ROCm 版本）

## 快速开始

```bash
# 1. 安装依赖
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/rocm6.2
pip install transformers datasets peft accelerate bitsandbytes

# 2. 验证 GPU 可用
python -c "import torch; print(f'GPU: {torch.cuda.get_device_name(0)}')"

# 3. 运行示例微调脚本
python train.py --model_name Qwen/Qwen2.5-7B --lora_rank 8
```

## 支持的微调方法

| 方法 | 显存需求 | 训练速度 | 适用场景 |
|------|----------|----------|----------|
| Full Fine-tuning | 高 | 慢 | 充足资源、追求最佳效果 |
| LoRA | 中 | 中 | 平衡效果与资源 |
| QLoRA | 低 | 中 | 显存有限、成本敏感 |

## 常见问题

<details>
<summary>Q: AMD GPU 上使用 bitsandbytes 量化吗？</summary>

ROCm 版本的 bitsandbytes 支持有限，建议使用 GPTQ 或 AWQ 等量化方案。具体兼容性请参考各工具的官方文档。

</details>

<details>
<summary>Q: 微调时 OOM（显存不足）怎么办？</summary>

1. 降低 batch_size
2. 使用 gradient_checkpointing
3. 减小 LoRA rank
4. 使用 QLoRA 进行量化微调

</details>

## 参考资源

- [PEFT 官方文档](https://huggingface.co/docs/peft)
- [Transformers 微调指南](https://huggingface.co/docs/transformers/training)
- [DeepSpeed 官方文档](https://www.deepspeed.ai/)

---

<div align="center">

**欢迎贡献更多微调教程！** 🎉

[提交 Issue](https://github.com/datawhalechina/hello-rocm/issues) | [提交 PR](https://github.com/datawhalechina/hello-rocm/pulls)

</div>
