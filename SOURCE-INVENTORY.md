# 公开源码与资料索引

## C++ 核心结构

- `GameTree.cpp` / `GameTree.hpp`：博弈树实现与定义
- `Agent.hpp`：AI Agent 接口资料
- `Trainer.hpp`：训练器接口资料
- `Task.cpp/.hpp`：任务对象
- `TaskQueue.cpp/.hpp`：任务队列
- `TaskExecutor.cpp/.hpp`：任务执行器

## Python 实验入口

- `scriptstrain.py`：训练参数入口，引用的 `src` 模块需按实际仓库核对
- `scriptsevaluate.py`：模型评估参数入口
- `examples/scriptsminimal_train.py`：简化 CFR 训练示例
- `examples/scriptsminimal_evaluate.py`：最小模型评估示例
- `examplessimple_game.py`：对局调用示例，引用模块需核对

## 工程文件

- `CMakeLists.txt`、`Makefile.mk`
- `pyproject.toml`、`setup.py`、`requirements.txt`
- `docker.dockerfile`、`dockerdocker-compose.yaml`
- `teststest_sample.py`

公开文件适合结构阅读和最小实验。完整训练入口引用的模块、模型及数据如果不在仓库中，不应描述为可一键复现。
