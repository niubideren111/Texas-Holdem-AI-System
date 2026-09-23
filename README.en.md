# Texas Holdem AI Source Code | Game Trees, Training and Evaluation

[简体中文](README.zh-CN.md) · [繁體中文](README.zh-TW.md) · [English](README.en.md) · [Product page](https://niubideren111.github.io/Texas-Holdem-AI-System/en/)

Poker AI research materials with C++ game-tree and task execution code plus Python training and evaluation entry scripts, supported by experiment and interface previews.

**Texas Holdem AI source code · poker AI source code · poker game tree · poker AI training**

## Introduction

This repository contains code references for Texas Holdem AI research, poker-bot match testing and strategy experiments. Public material includes a C++ game tree, Agent and Trainer interfaces, a task queue/executor, Python training and evaluation entry points, and a simplified CFR example. Any “poker assistant” use here means development, offline analysis, simulation and quality assurance, not unauthorized real-time advice in human games.

## Features

| Feature | Public material |
|---|---|
| Game-tree modeling | `GameTree.cpp/.hpp` for nodes, action history and tree structure |
| Agent interface | `Agent.hpp` as an agent abstraction reference |
| Trainer interface | `Trainer.hpp` for training-task organization |
| Task execution | `Task`, `TaskQueue` and `TaskExecutor` computation structure |
| Training entry point | `scriptstrain.py` exposes CFR, PPO and DQN parameters; referenced modules require verification |
| Evaluation entry point | `scriptsevaluate.py` accepts model, opponent type and game count |
| Minimal CFR example | `examples/scriptsminimal_train.py` contains readable demonstration logic |
| Model evaluation example | Minimal script demonstrates random opponents, game counts and return statistics |
| Project configuration | CMake, Python package metadata, requirements, Docker examples and tests |

## Architecture

```text
Game state / action history
          |
          v
GameTree + Agent/Trainer
          |
          v
TaskQueue -> TaskExecutor
          |
          v
Training script -> model -> evaluation script
          |
          v
Baselines, game count, returns and logs
```

| Layer | Components |
|---|---|
| Core | C++ game tree, Agent, Trainer and task-execution classes |
| Experiment | Python training, evaluation and minimal CFR scripts |
| Configuration | `pyproject.toml`, `setup.py`, `requirements.txt` |
| Build | `CMakeLists.txt`, `Makefile.mk` and Docker examples |
| Validation | Examples, sample tests and evaluation-output entry points |

## Advantages

- **C++ and Python separation:** core structures and experiment entry points are easy to study independently.
- **Separate training and evaluation:** model generation and opponent evaluation use distinct workflows.
- **Minimal example included:** the CFR demonstration introduces strategy accumulation and action selection.
- **Explicit evaluation parameters:** model, opponent and game-count inputs support better benchmark design.
- **Bot testing use cases:** useful for offline simulation, room-filling bot research and server QA.

## Performance and evaluation

The public repository does not include enough complete models, fixed hardware details, raw evaluation logs and training modules to establish a universal win rate or throughput claim. Do not treat claims such as “97% win rate” or “strongest AI” as verified benchmarks.

Record training duration, decision latency (mean/P95/P99), hands per second, opponent type, seed, sample size, win rate, average return, variance, confidence intervals, peak memory and CPU/GPU utilization. Every result should identify the code revision, configuration, model, hardware and raw logs. The minimal CFR example is for education and workflow validation; it is not a performance claim for a full no-limit Texas Holdem solver.

## What this repository presents

### Game-tree structure

Read GameTree.hpp and GameTree.cpp to study nodes, action histories and tree construction.

### Task execution

Review Task, TaskQueue and TaskExecutor files for computation scheduling structure.

### Training and evaluation

Use the Python entry scripts as references and validate claims against complete models and experiment data.

## How to evaluate the material

1. **Confirm the product:** review the screenshots and captions to identify the product type and visible workflow.
2. **Inspect the evidence:** open the listed source files or documents instead of relying on feature claims alone.
3. **Check buildability:** verify that required dependencies, assets, configuration and startup scripts are present for the part you intend to run.
4. **Confirm licensing:** read the repository license and obtain written permission for any commercial assets or complete-project delivery.

## Product screenshots

![Texas Holdem AI training parameters](docs/assets/seo/texas-holdem-ai-system-01.jpg)

![Poker AI project table interface](docs/assets/seo/texas-holdem-ai-system-02.jpg)

![Published evaluation tool and curve preview](docs/assets/seo/texas-holdem-ai-system-03.jpg)

## Public source and documents

| File | Description |
|---|---|
| [GameTree.cpp](GameTree.cpp) | Public CPP file: GameTree.cpp. |
| [GameTree.hpp](GameTree.hpp) | Public HPP file: GameTree.hpp. |
| [TaskExecutor.cpp](TaskExecutor.cpp) | Public CPP file: TaskExecutor.cpp. |
| [scriptstrain.py](scriptstrain.py) | Public PY file: scriptstrain.py. |
| [scriptsevaluate.py](scriptsevaluate.py) | Public PY file: scriptsevaluate.py. |

## Start reading

```bash
git clone https://github.com/niubideren111/Texas-Holdem-AI-System.git
cd Texas-Holdem-AI-System
```

## Questions

### Can the public files reproduce a claimed win rate?

The repository lacks some training modules and complete evaluation data, so no fixed win-rate claim is made.

### Where should I begin?

Read GameTree.hpp and GameTree.cpp first, followed by the task executor and Python parameter entry points.

## Documentation roadmap

Future updates should add a versioned dependency list, a verified setup or import procedure, a concise architecture or product-flow diagram, and release notes tied to real file changes. Large authorized assets belong in GitHub Releases with checksums; secrets, production endpoints and user data must never be committed.

## Related repositories

- [Texas-Holdem-Game-Source-Code](https://github.com/niubideren111/Texas-Holdem-Game-Source-Code)
- [Texas-Hold-em-Tournament-Source-Code](https://github.com/niubideren111/Texas-Hold-em-Tournament-Source-Code)

## Scope and license

Some training modules referenced by the public scripts are not included. The page documents available research material and does not promise one-command reproduction of win-rate claims. Public files should be evaluated against their actual paths, dependencies and license. No search ranking, production readiness or performance result is guaranteed.

- Telegram: [@fox_lovemyself](https://t.me/fox_lovemyself)
- GitHub: [Texas-Holdem-AI-System](https://github.com/niubideren111/Texas-Holdem-AI-System)
