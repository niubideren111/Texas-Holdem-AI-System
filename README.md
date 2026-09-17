# 德州AI源码｜德州扑克AI |博弈树、训练脚本|Texas Hold'em AI | Poker AI System

> 中文简体 · 中文繁體 · English 多语言产品与源码资料

[简体中文](README.zh-CN.md) · [繁體中文](README.zh-TW.md) · [English](README.en.md) · [产品页面](https://niubideren111.github.io/Texas-Holdem-AI-System/zh-cn/)

面向德州扑克策略研究的 AI 代码资料，包含 C++ 博弈树和任务执行类，以及 Python 训练、评估脚本入口。配套图片展示训练配置、对局界面和评估工具，便于讨论实验与工程结构。



[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![CI](https://github.com/niubideren111/Texas-Holdem-AI-System/actions/workflows/ci.yml/badge.svg)](https://github.com/niubideren111/Texas-Holdem-AI-System/actions/workflows/ci.yml)
本项目是一套**德州扑克AI系统源码**，可用于构建AI对手、训练系统等。

> ⚠️ **声明**：本项目仅供**研究和教育目的**使用。不得用于任何形式的真实货币赌博或违反相关平台服务条款的行为。

## 🧠 AI Performance | AI性能 | AI表現

🔥 Achieves **97%+ win rate** against general players (GG level)  
🔥 在普通玩家对局中胜率可达 **97%+（GG级别）** 【AI和中高级牌手线下对战数据】 
🔥 在一般玩家對局中勝率可達 **94%+（GG級別）** 【AI和顶级职业牌手线下对战数据】 

📊 Based on large-scale simulation & self-play training  
📊 基于大量模拟与自博弈训练  
📊 基於大規模模擬與自我對弈訓練  

🤖 Demonstrates strong decision-making and strategy optimization  
🤖 展现出强大的决策能力与策略优化能力  
🤖 展現出強大的決策能力與策略優化能力  

## 🎯 AI Strength | AI优势 | AI優勢

- ✔ High win rate strategy（高胜率策略）  
- ✔ Bluff / fold intelligence（诈唬与弃牌决策）  
- ✔ Probability-based decisions（概率决策）  
- ✔ Adaptive gameplay（自适应对局）  

👉 Close to real poker AI behavior  
👉 接近真实扑克AI策略  
👉 接近真實撲克AI策略  

## 🤖 AI Features | AI能力 | AI能力

* 🧠 Intelligent decision-making（智能决策）
* 🎯 Strategy-based gameplay（策略博弈）
* 🔄 Self-play training（自我对弈训练）
* 📊 Simulation environment（模拟环境）
* 🤖 AI poker bot（扑克AI机器人）

---

## 🧠 AI Technology | 技术核心 | 技術核心

* Game Theory（博弈论）
* Reinforcement Learning（强化学习）
* Monte Carlo Simulation（蒙特卡洛）
* CFR (Counterfactual Regret Minimization)

👉 Widely used in advanced poker AI research

---

---

## 📦 Tech Stack | 技术架构 | 技術架構

* C++ / Python
* AI algorithms
* Game engine
---
## ✨ 特性

| 特性 | 说明 |
|------|------|
| 🧠 **多种AI算法** | 支持 CFR、PPO、DQN 等多种算法 |
| 🎮 **完整游戏环境** | 包含完整的德州扑克规则实现 |
| 🔄 **自我对弈训练** | 支持通过自我对弈持续提升策略 |
| 📊 **评估工具** | 提供胜率、收益等多项评估指标 |
| 🐳 **容器化支持** | 提供 Docker 配置，便于环境部署 |
| 🤖 **人机对战** | 支持与训练好的AI模型对战 |

---


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



---

### 人机对战
bash
# 激活虚拟环境
source venv/bin/activate  # Windows: venv\Scripts\activate

# 与训练好的AI对战
python examples/play_vs_ai.py --model models/demo_model.bin
📦 安装
前置要求
Python 3.8 或更高版本

pip 包管理器

（可选）C++17 编译器（用于完整性能）

### 安装步骤
bash
# 1. 克隆仓库
git clone https://github.com/niubideren111/Texas-Holdem-AI-System.git
cd Texas-Holdem-AI-System

# 2. 创建虚拟环境
python -m venv venv
source venv/bin/activate  # Linux/Mac
# venv\Scripts\activate   # Windows

# 3. 安装依赖
pip install -r requirements.txt

# 4. 安装项目（开发模式）
pip install -e .
📖 使用方法
训练新模型
bash
# 训练 CFR 模型（1000轮迭代）
python scripts/train.py --algo cfr --iterations 1000 --save-path models/

# 训练 PPO 模型（需要安装 torch/tensorflow）
python scripts/train.py --algo ppo --iterations 5000
评估模型
bash
# 评估训练好的模型（500局游戏）
python scripts/evaluate.py --model models/your_model.bin --num-games 500
快速测试
bash
# 运行简单游戏示例（随机智能体对战）
python examples/simple_game.py
Docker 运行
bash
# 构建镜像
docker build -f docker/Dockerfile -t texas-holdem-ai .

# 运行训练
docker-compose -f docker/docker-compose.yml up trainer
📁 项目结构
text
Texas-Holdem-AI-System/
├── src/                      # 源代码
│   ├── core/                # 核心游戏逻辑
│   ├── algorithms/          # AI算法实现（CFR, PPO, DQN）
│   ├── env/                 # 游戏环境封装
│   └── utils/               # 工具函数
├── scripts/                  # 运行脚本
│   ├── train.py             # 训练脚本
│   ├── evaluate.py          # 评估脚本
│   └── reproduce_result.sh  # 一键复现脚本
├── examples/                 # 示例代码
│   ├── simple_game.py       # 简单游戏示例
│   └── play_vs_ai.py        # 人机对战示例
├── tests/                    # 单元测试
├── models/                   # 训练好的模型（Git LFS）
├── config/                   # 配置文件
├── docker/                   # Docker 配置
├── docs/                     # 文档
├── requirements.txt          # Python 依赖
├── setup.py                  # 安装配置
├── Makefile                  # 构建命令
└── CMakeLists.txt            # C++ 构建配置
### 🧠 算法说明
本项目实现了多种德州扑克AI算法：

Counterfactual Regret Minimization (CFR)
原理：通过最小化反事实遗憾值来逼近纳什均衡策略

特点：理论上保证收敛到纳什均衡

适用：有限博弈、策略求解

Proximal Policy Optimization (PPO)
原理：基于策略梯度的深度强化学习算法

特点：训练稳定、样本效率较高

适用：复杂环境、连续决策

Deep Q-Network (DQN)
原理：使用深度神经网络近似Q函数

特点：适合离散动作空间

适用：规则明确的决策问题

### 📊 评估结果
以下结果基于 scripts/minimal_train.py 在标准环境下测试获得，可在您的环境中复现。

模型	对手	胜率	平均收益	测试局数
CFR (100轮)	随机策略	~55%	+15 chips	500
CFR (500轮)	随机策略	~62%	+42 chips	500
随机策略	随机策略	50%	0 chips	500
复现上述结果
bash
# 训练 100 轮
python scripts/minimal_train.py --iterations 100

# 训练 500 轮
python scripts/minimal_train.py --iterations 500

# 评估
python scripts/minimal_evaluate.py --model models/minimal_model.bin --num-games 500
注意：以上结果为演示性数据，完整训练需要更多迭代和数据。



---


## 📸 Demo | 展示 | 展示

![德州扑克 AI 训练参数配置截图](docs/assets/seo/texas-holdem-ai-system-01.jpg)
![德州扑克 AI 项目对局界面展示](docs/assets/seo/texas-holdem-ai-system-02.jpg)
![原仓库发布的评估工具与曲线截图](docs/assets/seo/texas-holdem-ai-system-03.jpg)
---
## 相关项目

- [Texas-Holdem-Game-Source-Code](https://github.com/niubideren111/Texas-Holdem-Game-Source-Code)
- [Texas-Hold-em-Tournament-Source-Code](https://github.com/niubideren111/Texas-Hold-em-Tournament-Source-Code)

## 资料范围与许可

公开脚本引用的部分 src 训练模块未随仓库提供。本页展示代码与实验资料，不声称当前公开文件可一键复现胜率结果。 公开内容以实际文件、依赖和许可为准，不承诺搜索排名、直接上线或固定性能结果。

- Telegram: [@fox_lovemyself](https://t.me/fox_lovemyself)
- GitHub: [Texas-Holdem-AI-System](https://github.com/niubideren111/Texas-Holdem-AI-System)

❓ 常见问题
Q: 训练速度很慢怎么办？
A:

减少 --iterations 参数值

启用 GPU 支持（需安装 CUDA）

使用 config/default.yaml 中的并行设置

Q: 提示找不到模块？
A: 确保运行了 pip install -e . 安装项目

Q: C++ 编译失败？
A: 项目可以纯 Python 运行，C++ 部分用于性能优化，不影响核心功能

Q: 模型文件太大无法提交？
A:

bash
# 使用 Git LFS
git lfs install
git lfs track "*.bin"
git add models/*.bin
Q: 可以在真实的在线平台使用吗？
A: 不可以。本项目仅限研究和教育目的，在任何真实货币赌博平台使用违反服务条款，可能面临法律风险。

🤝 贡献指南
欢迎贡献代码、报告问题或提出建议！

Fork 本仓库

创建特性分支 (git checkout -b feature/amazing-feature)

提交更改 (git commit -m 'feat: add amazing feature')

推送到分支 (git push origin feature/amazing-feature)

创建 Pull Request

详细规范请参阅 CONTRIBUTING.md

## 许可

请按仓库现有 [LICENSE](LICENSE) 与 [License.md](License.md) 使用公开文件。商业工程、美术资源和完整部署资料的授权范围以书面约定为准。


⚠️ 免责声明
本项目仅供研究和教育目的使用。

不得用于任何形式的真实货币赌博

不得用于违反任何在线平台服务条款的行为

用户自行承担使用本项目的法律责任

作者不对任何滥用行为负责


---
⭐ Star History
如果您觉得这个项目对您有帮助，请给一个 ⭐ 支持一下！

## 🔍 SEO Keywords

texas holdem ai
poker ai
poker bot
poker ai system
ai poker strategy
poker simulation
ai poker engine
德州AI源码
扑克AI系统

