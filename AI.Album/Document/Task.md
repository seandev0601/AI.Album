# Task Breakdown – Photo Story Metadata PBI

> Revision **v1.1** · 2025-05-22
> Engineer: iOS Dev (solo)

---

## 0. Preparation – 定義開發規格（Specification）

| #   | Task                           | DoD（完成標準）                         | Est. (SP) |
| --- | ------------------------------ | --------------------------------- | --------- |
| 0.1 | **Tech Spec 撰寫** – API、架構、資料模型 | `TechSpec.md` 已 push，PO Review 完成 | **1**     |
| 0.2 | **UI Spec 撰寫** – Flow、版面、互動    | `UISpec.pdf` 附檔並獲 PO 核准           | **1**     |
| 0.3 | **Spec Review & Sign‑off**     | Meeting note 確認無開放議題              | **1**     |

## 1. Requirement Alignment

| #   | Task        | DoD                         | Est. (SP) |
| --- | ----------- | --------------------------- | --------- |
| 1.1 | 需求確認 & 風險盤點 | Checklist 完成，列出 HEIC / 權限風險 | **1**     |

## 2. Core Development

| #   | Task                                              | DoD                                      | Est. (SP) |
| --- | ------------------------------------------------- | ---------------------------------------- | --------- |
| 2.1 | 相簿權限流程（PhotoKit）                                  | 首次啟動彈窗、生效否決流程                            | **1**     |
| 2.2 | **Localization 建置 (zh‑Hant / en)**                | `Localizable.strings` 兩語系切換通過            | **1**     |
| 2.3 | 建立 `PhotoStory` Domain Model 及常數 `ai.album.story` | Struct + 單元測試                            | **1**     |
| 2.4 | Metadata **讀取** Utility                           | 支援 JPG/PNG/HEIC；讀取 `ai.album.story`；錯誤回傳 | **2**     |
| 2.5 | Metadata **寫入** Utility                           | ≤300 字寫入 `ai.album.story`；三格式測試          | **2**     |
| 2.6 | 故事輸入 UI (TextEditor + Counter)                    | 300 字動態提示；覆蓋警告彈窗                         | **2**     |
| 2.7 | 儲存流程整合                                            | Save→寫入→成功回載；錯誤 Toast                    | **1**     |
| 2.8 | 錯誤處理 & i18n 訊息                                    | 權限/讀取/寫入/格式/未知 5 類 error 字串完成            | **1**     |

## 3. Quality Assurance

| #   | Task                | DoD                                    | Est. (SP) |
| --- | ------------------- | -------------------------------------- | --------- |
| 3.1 | E2E 實機測試腳本 (iOS 17) | Happy path + 4 negative 情境通過           | **1**     |
| 3.2 | PR & Code Review    | CI 綠燈、0 Warning、Review Checklist all ✅ | **1**     |

## 4. Documentation & Handoff

| #   | Task                | DoD        | Est. (SP) |
| --- | ------------------- | ---------- | --------- |
| 4.1 | 更新 Task.md / README | 檔案合併至 main | **1**     |

---

### 總 Story Point

**18 SP**
（以 1 SP ≈ 1 小時 為本 Sprint 估算基準）

---

### 全域 Definition of Done

* 遵循 Xcode 16.2，最低 iOS 17。
* Story 成功寫入/讀取於 JPG、PNG、HEIC。
* zh‑Hant / English 文案正確顯示。
* Unit & E2E 測試全部通過。
* PO Demo 確認並簽核。

---

> 備註：Accessibility 與高階動畫將於後續迭代評估。

