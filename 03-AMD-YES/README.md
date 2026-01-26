<div align=center>
  <h1>03-AMD-YES</h1>
  <strong>✨ AMD 实践案例集合</strong>
</div>

<div align="center">

*社区驱动的 AMD GPU 项目实践*

[返回主页](../README.md)

</div>

## 简介

&emsp;&emsp;本模块收集了社区成员在 AMD GPU 上完成的精彩项目案例。这些案例涵盖了不同领域的大模型应用，展示了 AMD GPU 在 AI 领域的实际应用能力。

&emsp;&emsp;**AMD YES!** 不仅是一句口号，更是对 AMD GPU 在 AI 领域潜力的认可。我们希望通过这些案例，激发更多开发者在 AMD 平台上创造出色的 AI 应用。

## 案例列表

### AMchat - 高等数学助手

&emsp;&emsp;AMchat（Advanced Mathematics Chat）是一个集成了数学知识和高等数学习题及其解答的大语言模型。该模型使用 Math 和高等数学习题数据集，基于 InternLM2-Math-7B 模型微调，专门设计用于解答高等数学问题。

- **应用领域**：教育、数学辅导
- **基础模型**：InternLM2-Math-7B
- **微调方法**：LoRA

**项目亮点：**
- 专注高等数学领域
- 支持公式推导与解题步骤展示
- 可作为学习助手使用

📖 [查看 AMchat 项目详情](./AMchat/README.md)

---

### Chat-嬛嬛

&emsp;&emsp;Chat-嬛嬛是利用《甄嬛传》剧本中所有关于甄嬛的台词和语句，基于 LLM 进行 LoRA 微调得到的模仿甄嬛语气的聊天语言模型。

- **应用领域**：娱乐、角色扮演
- **基础模型**：多种 LLM 支持
- **微调方法**：LoRA

**项目亮点：**
- 独特的角色扮演体验
- 展示了数据驱动的人格定制
- 完整的数据处理流程

📖 [查看 Chat-嬛嬛 项目详情](./Chat-Huanhuan/README.md)

---

### Tianji - 天机

&emsp;&emsp;天机是一款基于人情世故社交场景的大语言模型系统应用教程。涵盖提示词工程、智能体制作、数据获取与模型微调、RAG 数据清洗与使用等全流程。

- **应用领域**：社交助手、情商培养
- **技术栈**：Prompt Engineering、Agent、RAG、Fine-tuning
- **难度等级**：⭐⭐⭐

**项目亮点：**
- 完整的 LLM 应用开发流程
- 多技术栈综合运用
- 实用的社交场景应用

📖 [查看 Tianji 项目详情](./Tianji/README.md)

---

### 数字生命

&emsp;&emsp;本项目致力于创造一个能够真正反映个人特征的 AI 数字人——包括语气、表达方式和思维模式等。整个流程是可迁移复制的，亮点是数据集的制作方法。

- **应用领域**：数字人、个人 AI 助手
- **基础模型**：多种 LLM 支持
- **微调方法**：自定义数据集 + LoRA

**项目亮点：**
- 可复制的数字人制作流程
- 创新的数据集制作方法
- 个性化 AI 的探索实践

📖 [查看数字生命项目详情](./Digital-Life/README.md)

---

### happy-llm

&emsp;&emsp;Happy-LLM 是一个从零开始的大语言模型原理与实践教程，带你深入探索大模型的底层机制，掌握完整的训练流程。

- **应用领域**：教育、大模型原理学习
- **内容范围**：模型架构、训练流程、优化技巧
- **难度等级**：⭐⭐⭐⭐

**项目亮点：**
- 从零理解大模型原理
- 完整的动手实践流程
- 适合进阶学习者

📖 [查看 happy-llm 项目详情](./happy-llm/README.md)

---

## 如何贡献你的项目

&emsp;&emsp;我们欢迎所有在 AMD GPU 上完成的 AI 项目！如果你有精彩的项目想要分享，请按照以下步骤提交：

### 提交步骤

1. **Fork 本仓库**
2. **在 `03-AMD-YES` 目录下创建你的项目文件夹**
3. **编写项目 README.md**，包含以下内容：
   - 项目简介
   - 环境要求
   - 使用方法
   - 效果展示
   - 参考资源
4. **提交 Pull Request**

### 项目要求

- 项目必须在 AMD GPU 上成功运行
- 提供完整的环境配置说明
- 代码可复现、文档清晰
- 遵循开源协议

## 案例展示墙

> 以下是社区成员在 AMD GPU 上完成的更多精彩项目（持续更新中）：

| 项目名称 | 描述 | 贡献者 |
|----------|------|--------|
| AMchat | 高等数学助手 | @contributor1 |
| Chat-嬛嬛 | 角色扮演聊天机器人 | @contributor2 |
| Tianji | 人情世故社交助手 | @contributor3 |
| 数字生命 | 个人 AI 数字人 | @contributor4 |
| happy-llm | 大模型原理教程 | @contributor5 |

---

<div align="center">

**AMD YES! 期待你的精彩项目！** 🎉

[提交你的项目](https://github.com/datawhalechina/hello-rocm/pulls)

</div>
