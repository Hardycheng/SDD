# SDD (Specification-Driven Development) 專案規格

## 專案概述

SDD 是一個基於規格驅動開發（Specification-Driven Development）的工作流程框架，透過 GitHub Copilot 的 slash 指令來實現從規格制定到實作的完整開發流程。

## 核心概念

### Speckit 工作流程

本專案實作一套標準化的開發流程，包含以下階段：

1. **Constitution（制定憲法）** - `/speckit.constitution`
   - 建立專案的基本原則和規範
   - 定義開發流程的基礎規則

2. **Specify（撰寫規格）** - `/speckit.specify`
   - 撰寫功能規格文件
   - 定義需求和驗收標準

3. **Implement（實作）** - `/speckit.implement`
   - 根據規格文件進行開發
   - 使用 tasks.md 追蹤進度
   - 每完成一項任務就打勾

## 功能需求

### 1. GitHub Copilot Slash 指令

在 `.github/prompts/` 目錄下建立以下 slash 指令：

#### 1.1 `/speckit.constitution`
- **用途**：設定專案基本規則
- **行為**：
  - 使用繁體中文
  - 不過度設計
  - 不自動建立 Markdown 總結文件
  - 確保 git 正確運作
  - 網站專案以靜態前端為主（可部署到 GitHub Pages）

#### 1.2 `/speckit.specify`
- **用途**：撰寫規格文件
- **行為**：
  - 建立或更新 `SPEC.md` 檔案
  - 包含專案概述、功能需求、技術規格
  - 建立 `tasks.md` 任務清單
  - 使用繁體中文撰寫

#### 1.3 `/speckit.implement`
- **用途**：根據規格實作功能
- **行為**：
  - 讀取 `SPEC.md` 和 `tasks.md`
  - 確認已完成的任務並打勾
  - 實作下一個未完成的任務
  - 不刪除或覆蓋規格文件
  - 每階段確保 git 正確提交

### 2. 文件結構

```
/workspaces/SDD/
├── README.md                    # 專案說明
├── SPEC.md                      # 規格文件
├── tasks.md                     # 任務清單
├── .github/
│   ├── copilot-instructions.md  # Copilot 基本設定
│   └── prompts/                 # Slash 指令定義
│       ├── constitution.md
│       ├── specify.md
│       └── implement.md
```

### 3. 任務追蹤機制

- 使用 `tasks.md` 作為待辦清單
- 格式：Markdown checklist
- 實作階段要確認並打勾已完成項目
- 按順序執行未完成的任務

## 技術規格

### 開發環境
- GitHub Codespaces / VS Code
- Git 版本控制
- GitHub Copilot

### 語言要求
- 所有文件使用繁體中文
- 程式碼註解使用繁體中文（必要時）

### Git 工作流程
- 每個實作階段都要提交
- 提交訊息使用繁體中文
- 確保 `.github/` 目錄被追蹤

## 驗收標準

### Phase 1: 基礎設施
- [ ] 建立 `.github/prompts/` 目錄結構
- [ ] 建立三個 slash 指令檔案
- [ ] 更新 README.md 說明專案用途
- [ ] git 提交所有檔案

### Phase 2: 指令功能
- [ ] `/speckit.constitution` 指令可正常運作
- [ ] `/speckit.specify` 指令可建立規格文件
- [ ] `/speckit.implement` 指令可讀取並實作任務

### Phase 3: 驗證
- [ ] 使用指令完成一個簡單範例專案
- [ ] 確認任務追蹤機制正常運作
- [ ] 確認 git 提交流程順暢

## 非功能需求

- **簡潔性**：不過度設計，保持簡單
- **可維護性**：文件清楚，易於理解
- **可用性**：指令直觀，容易使用
- **相容性**：可在 GitHub Codespaces 和本地環境運作

## 限制與假設

- 假設使用者已安裝 GitHub Copilot
- 假設使用者熟悉基本的 Git 操作
- 網站專案限制為靜態前端（HTML/CSS/JS）
- 不包含後端服務或資料庫

## 未來擴展方向

- 支援更多專案類型（後端、全端等）
- 整合 CI/CD 流程
- 提供專案範本
- 自動化測試整合
