# 德州撲克 AI 源碼｜機器人、博弈樹、訓練與評估系統

[簡體中文](README.zh-CN.md) · [繁體中文](README.zh-TW.md) · [English](README.en.md) · [產品頁面](https://niubideren111.github.io/Texas-Holdem-AI-System/zh-tw/)

面向德州撲克策略研究的 AI 程式碼資料，包含 C++ 博弈樹和任務執行類別，以及 Python 訓練、評估腳本入口。配套圖片展示訓練設定、對局介面和評估工具，便於討論實驗與工程結構。

**德州AI · 德州AI源碼 · 德州源碼 · 德州機器人 · 德州輔助軟體 · Poker AI**

## 簡介

這是一個面向德州撲克 AI 研究、機器人對局測試和策略實驗的程式碼資料庫。公開內容包括 C++ 博弈樹、Agent/Trainer 介面、任務佇列與執行器，以及 Python 訓練、評估和簡化 CFR 示例。這裡的「德州輔助軟體」指開發除錯、離線分析、模擬和品質測試工具，不用於在真人牌局中提供未經允許的即時決策。

## 特性

| 特性 | 公開資料 |
|---|---|
| 博弈樹建模 | `GameTree.cpp/.hpp` 展示節點、行動歷史和樹狀結構 |
| AI Agent 介面 | `Agent.hpp` 提供智慧代理抽象資料 |
| 訓練器介面 | `Trainer.hpp` 展示訓練任務組織方式 |
| 並行任務結構 | `Task`、`TaskQueue`、`TaskExecutor` 組成任務執行框架 |
| 訓練入口 | `scriptstrain.py` 提供 CFR、PPO、DQN 參數入口，但引用模組需另行核對 |
| 評估入口 | `scriptsevaluate.py` 提供模型、對手類型和局數參數 |
| 簡化 CFR 示例 | `examples/scriptsminimal_train.py` 包含可閱讀的最小訓練邏輯 |
| 模型評估示例 | 最小評估腳本展示隨機對手、局數及收益統計思路 |
| 工程設定 | CMake、Python 套件設定、requirements、Docker 示例和測試檔案 |

## 架構

```text
牌局狀態 / 行動歷史
        |
        v
GameTree + Agent/Trainer
        |
        v
TaskQueue -> TaskExecutor
        |
        v
訓練腳本 -> 模型檔案 -> 評估腳本
        |
        v
隨機/CFR等基準、局數、收益與日誌
```

| 層級 | 技術組成 |
|---|---|
| 核心結構 | C++ 博弈樹、Agent、Trainer 和任務執行類別 |
| 實驗層 | Python 訓練、評估及最小 CFR 展示腳本 |
| 設定層 | `pyproject.toml`、`setup.py`、`requirements.txt` |
| 建置層 | `CMakeLists.txt`、`Makefile.mk`、Docker 示例 |
| 驗證層 | 示例腳本、測試樣例和評估結果輸出入口 |

## 優勢

- **C++ 與 Python 分層**：核心結構和實驗入口分開，方便研究工程組織。
- **訓練與評估分離**：模型產生和對手評估使用不同入口，方便重現實驗流程。
- **包含最小示例**：簡化 CFR 檔案可作為理解策略累計和行動選擇的入口。
- **評估參數明確**：評估入口包含模型、對手和局數參數，適合補充標準化基準。
- **適合機器人測試**：可用於離線對局模擬、房間填充機器人研究和伺服器 QA。

## 效能與評估

儲存庫沒有足夠的完整模型、固定硬體環境、原始評估日誌和全部訓練模組來證明統一勝率或吞吐量，因此不採用「97% 勝率」「最強 AI」等結論。建議記錄訓練耗時、推理延遲、對局吞吐、對手類型、隨機種子、樣本量、平均收益、變異和資源使用。

效能結論必須綁定具體程式碼版本、設定、模型、硬體和原始日誌。最小 CFR 示例適合教學和流程驗證，不代表完整無限注德州撲克求解器的效能。

## 專案重點

### 博弈樹結構

GameTree.cpp 與 GameTree.hpp 展示節點、行動歷史和樹狀建置相關程式碼。

### 任務執行組織

Task、TaskQueue 和 TaskExecutor 檔案可用於閱讀計算任務調度結構。

### 訓練與評估入口

scriptstrain.py、scriptsevaluate.py 提供命令列入口資料；實驗結論應配合完整模型與評估資料。

## 資料閱讀與核對方式

1. **先確認產品形態**：依序檢視截圖與圖說，確認產品類型和可見功能流程。
2. **再核對檔案證據**：直接開啟下方列出的原始碼或文件，不只依賴功能描述。
3. **檢查可建置範圍**：確認欲執行的部分是否具備相依套件、資源、設定與啟動腳本。
4. **確認授權**：閱讀儲存庫授權；商業素材及完整工程交付應另行取得書面授權。

## 產品截圖

![德州撲克 AI 訓練參數設定截圖](docs/assets/seo/texas-holdem-ai-system-01.jpg)

![德州撲克 AI 專案對局介面展示](docs/assets/seo/texas-holdem-ai-system-02.jpg)

![原儲存庫發布的評估工具與曲線截圖](docs/assets/seo/texas-holdem-ai-system-03.jpg)

## 公開原始碼與資料

| 檔案 | 說明 |
|---|---|
| [GameTree.cpp](GameTree.cpp) | 博弈樹實作 |
| [GameTree.hpp](GameTree.hpp) | 博弈樹與節點定義 |
| [TaskExecutor.cpp](TaskExecutor.cpp) | 任務執行器 |
| [scriptstrain.py](scriptstrain.py) | Python 訓練腳本入口 |
| [scriptsevaluate.py](scriptsevaluate.py) | Python 評估腳本入口 |

## 開始閱讀

```bash
git clone https://github.com/niubideren111/Texas-Holdem-AI-System.git
cd Texas-Holdem-AI-System
```

## 常見問題

### 公開檔案能重現原介紹的勝率嗎？

目前缺少部分訓練模組與完整評估材料，本頁不重複使用 97% 或最強 AI 等未經重現的結論。

### 從哪里開始閱讀 AI 結构？

建議先閱讀 GameTree.hpp 和 GameTree.cpp，再看任務執行類別與 Python 訓練參數入口。

## 後續資料完善方向

补充實驗規則、對手基線、随機种子、样本量、模型版本與收益指標；将可複現實驗程式碼按真實路徑公開。 後續更新還應加入版本化相依清單、經過驗證的建置或匯入步驟、簡明架構／產品流程圖，以及能對應真實檔案變更的版本記錄。大型授權資源可放入 GitHub Releases 並提供校驗值，不能提交密鑰、生產位址或使用者資料。

## 相關專案

- [Texas-Holdem-Game-Source-Code](https://github.com/niubideren111/Texas-Holdem-Game-Source-Code)
- [Texas-Hold-em-Tournament-Source-Code](https://github.com/niubideren111/Texas-Hold-em-Tournament-Source-Code)

## 資料範圍與授權

公開腳本引用的部分 src 訓練模組未隨儲存庫提供。本頁展示程式碼與實驗資料，不聲稱目前公開檔案可一鍵重現勝率結果。公開內容以實際檔案、相依套件與授權為準，不承諾搜尋排名、直接上線或固定效能結果。

- Telegram: [@fox_lovemyself](https://t.me/fox_lovemyself)
- GitHub: [Texas-Holdem-AI-System](https://github.com/niubideren111/Texas-Holdem-AI-System)
