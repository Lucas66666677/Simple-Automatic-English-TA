# 📖 Lecturas — 英文備課助手

這是一個用來幫老師快速備課的 AI 工具，可讀取 **PDF、圖片、貼上文字**，自動生成：

- **板書整理**
- **口語化教學腳本**
- **圖片解析**
- **PDF 文字辨識 / OCR**

目前有兩個版本：

| 版本 | 說明 | 推薦程度 |
|------|------|----------|
| **Groq_API 版** | 使用 Groq API，速度快、較穩定 | ✅ 推薦 |
| **Ollama 版** | 使用本機 Ollama，安裝較麻煩且速度較慢 | 不建議日常使用 |

---

## ✨ 功能特色

- 支援上傳 **PDF**
- 支援上傳 **圖片**
- 支援直接貼上文字
- 自動判斷教材學科類型：
  - 數學 / 物理 / 化學
  - 歷史 / 地理 / 公民
  - 國文 / 英文
- 自動輸出：
  - **結構化板書**
  - **教學腳本**
- 圖片可自動分析題目、圖表、文章內容
- PDF 若無法直接擷取文字，會嘗試 OCR 視覺辨識

---

## 🖥️ 版本一：Groq_API 版（推薦）

### Colab 開啟連結
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Lucas66666677/Simple-Automatic-English-TA/blob/main/%E2%80%9C%E8%8B%B1%E6%96%87%E5%82%99%E8%AA%B2%E5%8A%A9%E6%89%8B%EF%BC%88Groq_API%EF%BC%89%E2%80%9D.ipynb)

### 使用前準備
1. 申請 Groq API Key
2. 在 Google Colab 的 **Secrets** 中新增：
   - 名稱：`Groq`
   - 值：你的 Groq API Key

### 使用方法
1. 點上方 Colab 連結開啟 notebook
2. 依序執行安裝依賴套件的 cell
3. 設定 `Groq` API Key
4. 上傳教材 PDF、圖片，或直接貼上文字
5. 按下 **Generate / 智慧分析**
6. 讀取輸出的：
   - 左側：板書整理
   - 右側：教學腳本

---

## 🖥️ 版本二：Ollama 版

### Colab 開啟連結
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Lucas66666677/Simple-Automatic-English-TA/blob/main/%E8%8B%B1%E6%96%87%E5%82%99%E8%AA%B2%E5%8A%A9%E6%89%8B%EF%BC%88Ollama%EF%BC%89%EF%BC%88Ollama%E7%94%9F%E6%88%90%E5%A4%AA%E6%85%A2%EF%BC%8C%E4%B8%8D%E5%BB%BA%E8%AD%B0%EF%BC%89.ipynb)
### 注意事項
- 這個版本需要在 Colab 中安裝 Ollama
- 啟動時間較長
- 模型下載較慢
- 整體效能通常不如 Groq API 版

### 使用方法
1. 點上方 Colab 連結開啟 notebook
2. 執行安裝環境與套件
3. 啟動 Ollama 服務並下載模型
4. 上傳 PDF / 圖片 / 文字
5. 點擊分析按鈕
6. 查看板書與腳本結果

---

## 📌 輸出說明

### 1. 板書
會依教材內容自動整理成適合上課使用的結構，像是：
- 核心概念
- 公式與變數
- 時間軸
- 因果關係
- 單字與文法
- 易錯點

### 2. 教學腳本
會產生口語化講解內容，方便老師直接拿來授課或微調後使用。

---

## 🛠️ 執行環境需求

### Groq_API 版
- Python 3.10+
- `gradio`
- `langchain-groq`
- `pypdf`
- `pdf2image`
- `markdown`

### Ollama 版
- Python 3.10+
- `gradio`
- `langchain-ollama`
- `pypdf`
- `pdf2image`
- `requests`
- Ollama 本體

---

## 📂 檔案結構建議

```text
.
├── Groq_API.ipynb
├── Ollama.ipynb
└── README.md
