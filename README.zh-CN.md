# 德州AI源码｜博弈树、训练脚本与评估资料

[简体中文](README.zh-CN.md) · [繁體中文](README.zh-TW.md) · [English](README.en.md) · [产品页面](https://niubideren111.github.io/Texas-Holdem-AI-System/zh-cn/)

面向德州扑克策略研究的 AI 代码资料，包含 C++ 博弈树和任务执行类，以及 Python 训练、评估脚本入口。配套图片展示训练配置、对局界面和评估工具，便于讨论实验与工程结构。

**德州AI源码 · 德州扑克AI · Poker AI · 德州AI训练**

## 项目重点

### 博弈树结构

GameTree.cpp 与 GameTree.hpp 展示节点、行动历史和树构建相关代码。

### 任务执行组织

Task、TaskQueue 和 TaskExecutor 文件可用于阅读计算任务调度结构。

### 训练与评估入口

scriptstrain.py、scriptsevaluate.py 提供命令行入口资料；实验结论应配合完整模型与评估数据。

## 资料阅读与核对方式

1. **先确认产品形态**：依次查看截图和图注，确认产品类型与可见功能流程。
2. **再核对文件证据**：直接打开下方列出的源码或文档，不只依赖功能描述。
3. **检查可构建范围**：确认准备运行的部分是否具备依赖、资源、配置和启动脚本。
4. **确认授权**：阅读仓库许可；商业素材及完整工程交付应另行取得书面授权。

## 产品截图

![德州扑克 AI 训练参数配置截图](docs/assets/seo/texas-holdem-ai-system-01.jpg)

![德州扑克 AI 项目对局界面展示](docs/assets/seo/texas-holdem-ai-system-02.jpg)

![原仓库发布的评估工具与曲线截图](docs/assets/seo/texas-holdem-ai-system-03.jpg)

## 公开源码与资料

| 文件 | 说明 |
|---|---|
| [GameTree.cpp](GameTree.cpp) | 博弈树实现 |
| [GameTree.hpp](GameTree.hpp) | 博弈树与节点定义 |
| [TaskExecutor.cpp](TaskExecutor.cpp) | 任务执行器 |
| [scriptstrain.py](scriptstrain.py) | Python 训练脚本入口 |
| [scriptsevaluate.py](scriptsevaluate.py) | Python 评估脚本入口 |

## 开始阅读

```bash
git clone https://github.com/niubideren111/Texas-Holdem-AI-System.git
cd Texas-Holdem-AI-System
```

## 常见问题



### 从哪里开始阅读 AI 结构？

建议先阅读 GameTree.hpp 和 GameTree.cpp，再看任务执行类与 Python 训练参数入口。

## 后续资料完善方向

补充实验规则、对手基线、随机种子、样本量、模型版本与收益指标；将可复现实验代码按真实路径公开。 后续更新还应加入版本化依赖清单、经过验证的构建或导入步骤、简明架构/产品流程图，以及能对应真实文件变化的版本记录。大型授权资源可放入 GitHub Releases 并提供校验值，不能提交密钥、生产地址或用户数据。

## 相关项目

- [Texas-Holdem-Game-Source-Code](https://github.com/niubideren111/Texas-Holdem-Game-Source-Code)
- [Texas-Hold-em-Tournament-Source-Code](https://github.com/niubideren111/Texas-Hold-em-Tournament-Source-Code)

## 资料范围与许可

公开脚本引用的部分 src 训练模块未随仓库提供。本页展示代码与实验资料，不声称当前公开文件可一键复现胜率结果。 公开内容以实际文件、依赖和许可为准，不承诺搜索排名、直接上线或固定性能结果。

- Telegram: [@fox_lovemyself](https://t.me/fox_lovemyself)
- GitHub: [Texas-Holdem-AI-System](https://github.com/niubideren111/Texas-Holdem-AI-System)
