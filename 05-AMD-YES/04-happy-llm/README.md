# 🚀 Happy-LLM - 从零训练大模型 AMD ROCm 版本

<div align='center'>

[![AMD](https://img.shields.io/badge/AMD-ROCm-ED1C24)](https://rocm.docs.amd.com/)

</div>

**Happy-LLM** 是一套完整的大语言模型（LLM）学习与实践教程，从零开始讲解大模型的核心原理和实现方法，包含模型结构设计、预训练、微调等全流程。本版本已适配 AMD ROCm 7.2.0+ 平台，支持 Linux 环境的多卡分布式训练。

> Happy-LLM 原始项目地址：[*Link*](https://github.com/datawhalechina/happy-llm.git)

***本教程将从零开始，带领你手把手实现一个完整的大语言模型，深入理解 LLM 的原理与实践！***

## 简介

&emsp;&emsp;本模块基于 Happy-LLM 教程，针对 AMD GPU 和 ROCm 平台进行了优化和适配。它包含两个核心章节：

- **第五章：动手搭建大模型** - 从零开始实现 LLaMA2 模型的完整结构，包括 RMSNorm、Attention、FFN 等核心组件
- **第六章：大模型训练流程实践** - 使用主流框架（Transformers、DeepSpeed）实现预训练和微调的完整流程

&emsp;&emsp;通过本教程，你将深入理解大模型的工作原理，掌握在 AMD GPU 上高效训练 LLM 的技能。

## 核心内容

### 📚 第五章：动手搭建大模型

深入讲解大语言模型的核心原理和实现细节。

#### 学习目标
- ✅ 理解 Transformer 架构和注意力机制
- ✅ 从零实现 LLaMA2 模型的完整结构
- ✅ 掌握模型预训练的全流程
- ✅ 实现参数高效的微调方法（LoRA）

#### 主要内容
- **5.1 - 动手实现 LLaMA2 大模型**
  - 超参数定义与 ModelConfig 类设计
  - RMSNorm 归一化层实现
  - Attention 多头注意力机制
  - 前馈网络（FFN）实现
  - 完整 LLaMA2 模型架构

- **5.2 - 预训练与微调**
  - 数据加载与预处理
  - 模型预训练流程
  - 监督微调（SFT）实现
  - 模型保存与导出

📖 [进入第五章](./chapter5/README.md)

---

### 🔧 第六章：大模型训练流程实践

使用主流框架实现工业级的大模型训练。

#### 学习目标
- ✅ 掌握 Transformers 框架的使用方法
- ✅ 实现多卡分布式训练（DDP、DeepSpeed）
- ✅ 学习参数高效微调技术（LoRA、QLoRA）
- ✅ 优化训练性能与显存使用

#### 主要内容
- **6.1 - 框架介绍与基础**
  - Transformers 框架概述
  - Trainer API 讲解
  - 配置文件与超参数设置

- **6.2 - 预训练实践**
  - 模型下载与初始化
  - 数据集加载与处理
  - 分布式预训练脚本
  - 检查点保存与恢复

- **6.3 - 微调实践**
  - 监督微调（SFT）
  - 参数高效微调（PEFT）
  - DeepSpeed 零阶段优化
  - 模型量化与推理优化

- **6.4 - 偏好对齐**
  - 强化学习微调（RLHF）
  - DPO、IPO 等对齐方法

📖 [进入第六章](./chapter6/README.md)

---

## 环境要求

### 硬件要求

- **GPU**：AMD RDNA 2/3 系列（如 RX 6700 XT、RX 7900 XTX）或 MI 系列（如 MI300X）
- **显存**：建议 64GB+ 以上
- **系统内存**：128GB+ 推荐
- **存储空间**：300GB+（用于模型和数据集）

### 软件要求

- **操作系统**：Linux (Ubuntu 22.04 LTS / 24.04 LTS 推荐)
- **ROCm 版本**：7.12.0 或更高版本
- **Python 版本**：3.10~3.12

---

## 快速开始

### 第一步：环境准备

```bash
cd 04-happy-llm

# 升级pip
python -m pip install --upgrade pip

# 安装 rocm 以及 rocm 版本的 torch torchvision torchaudio
# 本次测试使用的是 4*AMD Radeon™ AI PRO R9700 架构为 gfx1201 如果为其他架构请自行下载
pip install --index-url https://repo.amd.com/rocm/whl/gfx120X-all/ "rocm[libraries,devel]"
pip install --index-url https://repo.amd.com/rocm/whl/gfx120X-all/ torch torchvision torchaudio

# 安装项目依赖
pip install -r ./chapter5/code/requirements.txt
pip install -r ./chapter6/code/requirements.txt
```

> 本项目使用 4*AMD Radeon™ AI PRO R9700 运行测试，其他 Instinct/Radeon PRO/Radeon/Ryzen 系列适配情况请查看 https://rocm.docs.amd.com/en/7.12.0-preview/compatibility/compatibility-matrix.html

### 第二步：选择学习路径

**初学者推荐路线：**
1. 先完成第五章第一节，理解 LLaMA2 的完整结构
2. 按顺序完成第五章，掌握从零实现大模型
3. 进入第六章，学习使用主流框架训练模型

**进阶开发者路线：**
1. 跳过第五章基础部分，从第五章第二节开始
2. 重点学习第六章的分布式训练和优化技术
3. 完成性能基准测试和优化案例

### 第三步：运行示例

```bash
# 运行第五章模型实现示例
cd chapter5/code

# 运行第六章预训练脚本
cd chapter6/code
```

---

## 关键技术点

### 模型架构
| 组件 | 说明 |
|------|------|
| **Token Embedding** | 词嵌入层 |
| **RMSNorm** | 根均方范数归一化 |
| **Attention** | 多头自注意力机制，支持 FlashAttention2 |
| **FFN** | 前馈网络 (MLP) |
| **Rotary Embedding** | 旋转位置编码 |

### 训练优化
| 技术 | 用途 |
|------|------|
| **DDP** | 数据并行分布式训练 |
| **DeepSpeed ZeRO** | 内存优化与参数分片 |
| **FlashAttention** | 降低注意力计算复杂度 |
| **PEFT/LoRA** | 参数高效微调 |
| **梯度累积** | 增大有效批大小 |
| **混合精度训练** | 降低显存占用 |


## 常见问题

<details>
<summary>Q: ROCm 找不到 GPU 怎么办？</summary>

**A:** 按以下步骤排查：

1. 验证 GPU 和驱动：
   ```bash
   rocminfo
   rocm-smi
   ```

2. 检查环境变量：
   ```bash
   echo $LD_LIBRARY_PATH
   export HSA_OVERRIDE_GFX_VERSION=gfx90a  # 对某些 GPU 可能需要
   ```

3. 重新安装 PyTorch ROCm 版本，注意 gpu 对应架构：
   ```bash
   pip install torch torchvision torchaudio --index-url https://repo.amd.com/rocm/whl/gfx120X-all/
   ```

4. 如果问题仍存在，请查看 [ROCm 官方指南](https://rocm.docs.amd.com/en/7.12.0-preview/compatibility/compatibility-matrix.html)

</details>

<details>
<summary>Q: 显存不足（OOM）如何解决？</summary>

**A:** 尝试以下方法（优先级从高到低）：

1. **减小批大小** - 在配置文件中设置 `per_device_train_batch_size = 1`
2. **启用梯度累积** - 设置 `gradient_accumulation_steps = 8`
3. **使用混合精度** - 设置 `fp16 = true` 或 `bf16 = true`
4. **启用 DeepSpeed ZeRO-3** - 完整参数分片
5. **使用 LoRA 微调** - 而不是全量微调
6. **启用 FlashAttention** - 降低注意力显存占用

</details>

<details>
<summary>Q: 多卡训练速度不理想怎么办？</summary>

**A:** 检查和优化：

1. 验证多卡识别：
   ```bash
   rocm-smi  # 查看所有 GPU
   ```

2. 检查通信带宽：
   ```bash
   rocm-bandwidth-test
   ```

3. 在训练脚本中启用 distributed debug：
   ```bash
   export NCCL_DEBUG=INFO
   # 或 HIP 的等价环境变量
   ```

4. 尝试增加 `num_train_epochs` 和 `logging_steps` 以平衡通信开销

</details>

<details>
<summary>Q: 如何在服务器上实际运行这些项目？</summary>

**A:** 推荐流程：

1. **环境准备**（第一次运行）
   - 运行 `code/install_rocm_deps.sh` 安装所有依赖
   - 运行 `code/setup_environment.sh` 配置环境变量

2. **验证环境**
   - 运行 `code/performance_benchmark.py` 进行性能测试
   - 查看输出的 GPU 利用率和吞吐量

3. **选择模型**
   - 根据硬件显存选择合适的模型大小
   - 参考"性能参考"表格调整超参数

4. **开始训练**
   - 从 chapter5 开始学习基础概念
   - 按 chapter6 的脚本进行实际训练

5. **监控和优化**
   - 使用 `rocm-smi` 实时监控 GPU 状态
   - 根据训练日志调整超参数

详细的运行指南见各章节文档。

</details>

<details>
<summary>Q: 第五章和第六章有什么区别？</summary>

**A:** 
- **第五章**：纯 PyTorch 实现，从零搭建 LLaMA2，适合理解模型原理
- **第六章**：使用 Transformers 框架，重点在于工业级训练和优化，适合实际应用

如果想快速上手训练，可以直接进入第六章。如果想深入理解模型原理，建议先完成第五章。

</details>

---

## 项目结构

```

```

---

## 参考资源

- 📚 [Happy-LLM 原始项目](https://github.com/datawhalechina/happy-llm)
- 📖 [ROCm 官方文档](https://rocm.docs.amd.com/)
- 📖 [ROCm 官方 preview 文档](https://rocm.docs.amd.com/en/7.12.0-preview/index.html)
- 🤗 [Hugging Face Transformers](https://huggingface.co/docs/transformers)
- ⚡ [DeepSpeed 官方文档](https://www.deepspeed.ai/)
- 🔧 [PyTorch 官方文档](https://pytorch.org/docs/)

---

## 贡献与反馈

欢迎提交 Issue 和 Pull Request！

- 📝 改进文档和教程
- 🐛 报告 Bug
- 💡 分享优化技巧
- 📊 补充性能测试结果

[提交 Issue](https://github.com/datawhalechina/hello-rocm/issues) | [提交 PR](https://github.com/datawhalechina/hello-rocm/pulls)

---

<div align="center">

**开始学习大模型，从零构建 LLM！** 🎓

Made with ❤️ by the hello-rocm community

</div>
