# 德州AI原始碼｜博弈树、训练腳本與评估資料

[简体中文](README.zh-CN.md) · [繁體中文](README.zh-TW.md) · [English](README.en.md) · [产品页面](https://niubideren111.github.io/Texas-Holdem-AI-System/zh-tw/)

面向德州撲克策略研究的 AI 程式碼資料，包含 C++ 博弈树和任務执行類，以及 Python 训练、评估腳本進入點。配套圖片展示训练設定、對局介面和评估工具，便於讨论實驗與工程結构。

**德州AI原始碼 · 德州撲克AI · Poker AI · 德州AI训练**

## 專案重點

### 博弈树結构

GameTree.cpp 與 GameTree.hpp 展示節點、行動歷史和树建置相關程式碼。

### 任務执行組織

Task、TaskQueue 和 TaskExecutor 文件可用於閱讀計算任務調度結构。

### 训练與评估進入點

scriptstrain.py、scriptsevaluate.py 提供命令行進入點資料；實驗結论應配合完整模型與评估資料。

## 資料閱讀與核對方式

1. **先確認產品形態**：依序檢視截圖與圖說，確認產品類型和可見功能流程。
2. **再核對檔案證據**：直接開啟下方列出的原始碼或文件，不只依賴功能描述。
3. **檢查可建置範圍**：確認欲執行的部分是否具備相依套件、資源、設定與啟動腳本。
4. **確認授權**：閱讀儲存庫授權；商業素材及完整工程交付應另行取得書面授權。

## 產品截圖

![德州撲克 AI 训练參數設定截圖](docs/assets/seo/texas-holdem-ai-system-01.jpg)

![德州撲克 AI 專案對局介面展示](docs/assets/seo/texas-holdem-ai-system-02.jpg)

![原儲存庫發布的评估工具與曲線截圖](docs/assets/seo/texas-holdem-ai-system-03.jpg)

## 公開原始碼與資料

| 文件 | 说明 |
|---|---|
| [GameTree.cpp](GameTree.cpp) | 博弈树實作 |
| [GameTree.hpp](GameTree.hpp) | 博弈树與節點定義 |
| [TaskExecutor.cpp](TaskExecutor.cpp) | 任務执行器 |
| [scriptstrain.py](scriptstrain.py) | Python 训练腳本進入點 |
| [scriptsevaluate.py](scriptsevaluate.py) | Python 评估腳本進入點 |

## 開始閱讀

```bash
git clone https://github.com/niubideren111/Texas-Holdem-AI-System.git
cd Texas-Holdem-AI-System
```

## 常見問題

### 公開文件能複現原介绍的胜率吗？

當前缺少部分训练模組與完整评估材料，本頁不重複使用 97% 或最强 AI 等未经複現的結论。

### 從哪里開始閱讀 AI 結构？

建議先閱讀 GameTree.hpp 和 GameTree.cpp，再看任務执行類與 Python 训练參數進入點。

## 後續資料完善方向

补充實驗規則、對手基線、随機种子、样本量、模型版本與收益指標；将可複現實驗程式碼按真實路徑公開。 後續更新還應加入版本化相依清單、經過驗證的建置或匯入步驟、簡明架構／產品流程圖，以及能對應真實檔案變更的版本記錄。大型授權資源可放入 GitHub Releases 並提供校驗值，不能提交密鑰、生產位址或使用者資料。

## 相關專案

- [Texas-Holdem-Game-Source-Code](https://github.com/niubideren111/Texas-Holdem-Game-Source-Code)
- [Texas-Hold-em-Tournament-Source-Code](https://github.com/niubideren111/Texas-Hold-em-Tournament-Source-Code)

## 資料範圍與授權

公開腳本引用的部分 src 训练模組未随儲存庫提供。本頁展示程式碼與實驗資料，不声稱當前公開文件可一鍵複現胜率結果。 公開內容以實際檔案、相依套件與授權為準，不承諾搜尋排名、直接上線或固定效能結果。

- Telegram: [@fox_lovemyself](https://t.me/fox_lovemyself)
- GitHub: [Texas-Holdem-AI-System](https://github.com/niubideren111/Texas-Holdem-AI-System)
