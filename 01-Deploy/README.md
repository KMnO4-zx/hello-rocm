<div align=center>
  <h1>01-Deploy</h1>
  <strong>🚀 ROCm 大模型部署实践</strong>
</div>

<div align="center">

*零基础快速上手 AMD GPU 大模型部署*

[返回主页](../README.md)

</div>

## 简介

&emsp;&emsp;本模块提供在 AMD GPU 上部署大语言模型的完整教程。无论你是初学者还是有经验的开发者，都可以通过本教程快速掌握在 ROCm 平台上部署和运行大模型的方法。

&emsp;&emsp;自 ROCm 7.10.0 起，ROCm 已支持像 CUDA 一样在 Python 虚拟环境中无缝安装，这大大降低了 AMD GPU 大模型部署的门槛。

## 教程列表

### Ubuntu 24.04 + ROCm 7 环境准备教程

&emsp;&emsp;本教程将手把手带你在 Ubuntu 24.04 上完成 ROCm 7.1.0 的安装与验证，包括卸载旧 ROCm 环境、运行官方脚本安装 ROCm、以及使用 `rocminfo` / `rocm-smi` / `amd-smi` 等工具确认 GPU 与驱动状态。建议在开始任何部署教程之前先完成本篇。

- **适合人群**：首次在 AMD GPU 上搭建 ROCm 环境的用户
- **难度等级**：⭐⭐
- **预计时间**：1 小时

📖 [开始学习环境准备教程](./env-prepare-ubuntu24-rocm7.md)

---
### LM Studio 零基础大模型部署

&emsp;&emsp;LM Studio 是一款用户友好的桌面应用，支持在本地运行大语言模型。本教程将指导你如何在 AMD GPU 上使用 LM Studio 部署和运行大模型。

- **适合人群**：零基础用户、希望快速体验大模型的用户
- **难度等级**：⭐
- **预计时间**：30 分钟

📖 [开始学习 LM Studio 部署教程](./lm-studio-rocm7-deploy.md)

---

### vLLM 零基础大模型部署

&emsp;&emsp;vLLM 是一个高性能的大模型推理和服务框架，支持高效的 PagedAttention 和连续批处理。本教程将指导你如何在 AMD GPU 上使用 vLLM 部署大模型服务。

- **适合人群**：需要搭建推理服务的开发者
- **难度等级**：⭐⭐
- **预计时间**：1 小时

📖 [开始学习 vLLM 部署教程](./vllm-rocm7-deploy.md)

---

### Ollama 零基础大模型部署

&emsp;&emsp;Ollama 是一个快速服务大语言模型和视觉语言模型的框架，具有高效的后端运行时。本教程将指导你如何在 AMD GPU 上使用 Ollama 部署大模型。

- **适合人群**：需要高性能推理服务的开发者
- **难度等级**：⭐⭐
- **预计时间**：1 小时

📖 [开始学习 Ollama 部署教程](./ollama-rocm7-deploy.md)

---

### ATOM 零基础大模型部署

&emsp;&emsp;ATOM 是一个针对 AMD GPU 优化的推理框架。本教程将指导你如何使用 ATOM 在 AMD GPU 上高效运行大模型。

- **适合人群**：追求极致性能的开发者
- **难度等级**：⭐⭐⭐
- **预计时间**：1.5 小时

📖 [开始学习 ATOM 部署教程](./ATOM/README.md)

---

### llama.cpp 零基础大模型部署

&emsp;&emsp;llama.cpp 是一个轻量且高性能的推理后端，支持 GGUF 等多种模型格式，并已提供针对 ROCm 的优化版本。本教程将介绍如何在 Ubuntu 24.04 + ROCm 7+ 环境下使用预编译二进制与 Docker 两种方式部署 Qwen3 等主流模型。

- **适合人群**：希望用命令行 / REST API 自由编排推理流程的开发者
- **难度等级**：⭐⭐⭐
- **预计时间**：1.5 小时

📖 [开始学习 llama.cpp 部署教程](./llamacpp-rocm7-deploy.md)

---


## 环境要求

### 硬件要求

- AMD GPU（支持 ROCm 的显卡，如 RX 7000 系列、MI 系列等）
- 建议显存 8GB 以上

### 软件要求

- 操作系统：Linux (Ubuntu 22.04+) 或 Windows 11
- ROCm 7.10.0 或更高版本
- Python 3.10+

## 常见问题

<details>
<summary>Q: 如何确认我的 AMD GPU 是否支持 ROCm？</summary>

请参考 [ROCm 官方支持列表](https://rocm.docs.amd.com/projects/install-on-linux/en/latest/reference/system-requirements.html) 查看支持的 GPU 型号。

</details>

<details>
<summary>Q: 部署时遇到 "HIP error" 怎么办？</summary>

1. 确认 ROCm 已正确安装
2. 检查环境变量是否正确设置
3. 尝试重启系统后再次运行

</details>

## 参考资源

- [ROCm 官方文档](https://rocm.docs.amd.com/)
- [vLLM 官方文档](https://docs.vllm.ai/)
- [Ollama GitHub](https://github.com/sgl-project/Ollama)

---

<div align="center">

**欢迎贡献更多部署教程！** 🎉

[提交 Issue](https://github.com/datawhalechina/hello-rocm/issues) | [提交 PR](https://github.com/datawhalechina/hello-rocm/pulls)

</div>
