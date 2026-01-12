# hello-rocm

<div align="center">

**AMD YES! 🚀**

*开源 · 社区驱动 · 让 AMD AI 生态更易用*

</div>


## News

- *2025.12.11:* [*ROCm 7.10.0 Release Notes*](https://rocm.docs.amd.com/en/7.10.0-preview/about/release-notes.html)


## About

自 **ROCm 7.10.0** (2025年12月11日发布) 以来，ROCm 已支持像 CUDA 一样在 Python 虚拟环境中无缝安装，并正式支持 **Linux 和 Windows** 双系统。这标志着 AMD 在 AI 领域的重大突破——学习者与大模型爱好者在硬件选择上不再局限于 NVIDIA，AMD GPU 正成为一个强有力的竞争选择。

苏妈在发布会上宣布 ROCm 将保持 **每 6 周一个新版本** 的迭代节奏，并全力转向 AI 领域。前景令人振奋！

然而，目前全球范围内缺乏系统的 ROCm 大模型推理、部署、训练、微调及 Infra 的学习教程。**hello-rocm** 应运而生，旨在填补这一空白。


## Mission

构建一个开源、社区驱动的 AMD ROCm AI 学习平台，让每个人都能轻松上手 AMD GPU 进行大模型开发。


## Project Structure

```
hello-rocm/
├── 01-Deploy/              # ROCm 大模型部署实践
├── 02-Fine-tune/           # ROCm 大模型微调实践
├── 03-AMD-YES/             # AMD 实践案例集合
└── 04-Infra/               # Rocm 算子优化实践
└── 05-References/          # Rocm 优质参考资料
```


## Modules

### 01. Deploy - ROCm 大模型部署
<table align="center">
  <tr>
    <td valign="top" width="50%">
      <b>核心内容</b><br>
      • LM Studio 零基础大模型部署<br>
      • Vllm 零基础大模型部署<br>
      • SGLong 零基础大模型部署<br>
      • ATOM 零基础大模型部署<br>
    </td>
  </tr>
</table>

**入门教程** → [Getting Started with ROCm Deploy](./01-Deploy/README.md)

### 02. Fine-tune - ROCm 大模型微调实践
<table align="center">
  <tr>
    <td valign="top" width="50%">
      <b>核心内容</b><br>
      • 大模型零基础微调教程<br>
      • 大模型单机微调脚本<br>
      • 大模型多机多卡微调教程<br>
    </td>
  </tr>
</table>

**入门教程** → [Getting Started with ROCm Fine-tune](./02-Fine-tune/README.md)

### 03. AMD-YES - AMD 实践案例集合
<table align="center">
  <tr>
    <td valign="top" width="50%">
      <b>核心内容</b><br>
      • AMchat-高等数学<br>
      • Chat-嬛嬛<br>
      • Tianji-天机<br>
      • 数字生命<br>
      • happy-llm<br>
    </td>
  </tr>
</table>

**入门教程** → [Getting Started with ROCm AMD-YES](./03-AMD-YES/README.md)

### 04. Infra - Rocm 算子优化实践
<table align="center">
  <tr>
    <td valign="top" width="50%">
      <b>核心内容</b><br>
      • HIPify 自动化迁移实战<br>
      • BLAS 与 DNN 的无缝切换<br>
      • NCCL 到 RCCL 的迁移<br>
      • Nsight 到 Rocprof 的映射
    </td>
  </tr>
</table>

**查看项目** → [Getting Started with ROCm Infra](.04-Infra/README.md)


### 05. References - Rocm 优质参考资料
<table align="center">
  <tr>
    <td valign="top" width="50%">
      <b>核心内容</b><br>
      • AMD 参考资料<br>
      • 相关新闻<br>
    </td>
  </tr>
</table>

**查看项目** → [ROCm References](./05-References/README.md)


## Contributing

我们欢迎所有形式的贡献！无论是：

- 完善或新增教程
- 修复错误与 Bug
- 分享你的 AMD 项目
- 提出建议与想法

请参阅 [CONTRIBUTING.md](./CONTRIBUTING.md) 了解详情。


## Resources

- [ROCm 官方文档](https://rocm.docs.amd.com/)
- [AMD GitHub](https://github.com/amd)
- [ROCm Release Notes](https://rocm.docs.amd.com/en/latest/about/release-notes.html)


## License

[MIT License](./LICENSE)

---

<div align="center">

**让我们一起构建 AMD AI 的未来！** 💪

Made with ❤️ by the hello-rocm community

</div>
