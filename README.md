# SDD - Specification-Driven Development

一個基於規格驅動開發的工作流程框架，透過 GitHub Copilot slash 指令實現從規格制定到實作的完整開發流程。

## 專案簡介

SDD（Specification-Driven Development）提供一套標準化的開發流程，透過三個核心指令來管理專案：

### 核心指令

- **`/speckit.constitution`** - 制定專案基本規則與原則
- **`/speckit.specify`** - 撰寫功能規格文件和任務清單
- **`/speckit.implement`** - 根據規格實作功能並追蹤進度

## 快速開始

1. 確保已安裝 GitHub Copilot
2. 使用 `/speckit.specify` 建立專案規格
3. 使用 `/speckit.implement` 開始實作

## 文件結構

```
/workspaces/SDD/
├── README.md                    # 專案說明（本檔案）
├── SPEC.md                      # 詳細規格文件
├── tasks.md                     # 任務追蹤清單
├── .github/
│   ├── copilot-instructions.md  # Copilot 基本設定
│   └── prompts/                 # Slash 指令定義目錄
│       ├── constitution.md
│       ├── specify.md
│       └── implement.md
```

## 開發原則

- 使用繁體中文撰寫所有文件
- 不過度設計，保持簡潔
- 確保 git 在每個階段都正確運作
- 實作時使用 tasks.md 追蹤進度
- 網站專案以靜態前端為主（可部署至 GitHub Pages）

## 詳細規格

請參閱 [SPEC.md](./SPEC.md) 了解完整的功能需求與技術規格。

## 授權

MIT License