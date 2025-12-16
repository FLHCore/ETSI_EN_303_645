## 生命週期文件 (LIFECYCLE DOCUMENTS)

### 條款 CK-LP-08

您是否建立了適當的漏洞揭露與管理機制 (vulnerability disclosure and management)？

#### 最低要求 (Minimum Requirements)

* 必須執行適當的漏洞分類，使用 **CVSS v3** (或更高版本) 系統將漏洞分類為不同的嚴重等級 (嚴重 critical、高 high、中 medium、低 low)。
* 開發商必須具備充足的**供應鏈能力 (supply chain capability)**，以確保其設備中使用的組件（包含硬體與軟體）在必要時能獲得更新。

#### 佐證證據 (Supporting Evidence)

* 開發商應描述當收到漏洞報告時，管理設備修補程式與更新的**內部流程**（例如：如何報告設備漏洞、確保這些漏洞得到解決的計畫）。
* 開發商隨後應提供證據（例如：上述漏洞的 **CVSS 評分截圖**等），顯示在漏洞嚴重等級分類中使用了 CVSS v3 (或更高版本)。
* 開發商亦應提供**內部文件**，描述其供應鏈能力，確保設備使用的組件能持續獲得修補程式與更新。

#### 評估 (Assessment)

* 評估人員將檢查當漏洞被報告時，是否有管理設備修補程式與更新的內部流程。
* 評估人員將檢查是否使用 CVSS v3 (或更高版本) 系統進行設備漏洞分類。
* 評估人員將檢查描述開發商供應鏈能力的內部文件是否準確。

---

### 開發者深度導讀 (針對 Gateway / App / Cloud 開發商)

#### 本章節核心要求與意涵

本條款關注的是**「漏洞量化標準 (Standardization)」**與**「上游維護能力 (Upstream Maintenance)」**。

1.  **CVSS 的強制性**：
    * 過去許多廠商對漏洞嚴重度的定義很主觀（例如：「我覺得這個還好，算 Low 吧」）。
    * **合規要求**：必須採用 **CVSS (Common Vulnerability Scoring System)** 標準。這是一個客觀的計算公式，根據攻擊向量 (AV)、攻擊複雜度 (AC)、權限需求 (PR) 等因子算出 0.0~10.0 的分數。
    * **意義**：這讓開發團隊與外部資安研究員有了「共同語言」。當研究員說這是 CVSS 9.8 的漏洞時，您就不能把它當作 Low 來處理。
2.  **供應鏈的「課責性」**：
    * 這是針對 OEM/ODM 模式的痛點。如果您是貼牌廠商，或者使用 MediaTek/Realtek/Qualcomm 的 Turnkey 方案，您必須證明**當晶片原廠的 SDK 出包時，您叫得動原廠修**。
    * 如果您的晶片供應商已經停止支援該型號（EoL），那您的「供應鏈能力」就會被判定不足，無法通過此條款。

#### 具體落地實現方案建議

* **流程建立 (SOP)**：
    * **漏洞分級標準書**：
        * 制定內部規範：
            * Critical: CVSS 9.0 - 10.0 (需 24hr 內回應)
            * High: CVSS 7.0 - 8.9 (需 7 天內修復)
            * Medium: CVSS 4.0 - 6.9
            * Low: CVSS 0.1 - 3.9
    * **CVSS 計算器整合**：
        * 在內部的 Bug Tracking System (如 JIRA) 中，安裝 CVSS Calculator Plugin，或者提供連結到 [NVD CVSS Calculator](https://nvd.nist.gov/vuln-metrics/cvss/v3-calculator)。

* **證據收集策略**：
    * **JIRA 欄位截圖**：
        * 截取一張 Security Ticket 的畫面，顯示有一個欄位叫 "CVSS Score"，填寫數值為 "7.5"，並且 Priority 自動對應到 "High"。這是證明您有落實 CVSS 分類的鐵證。
    * **供應商合約/郵件**：
        * 針對「供應鏈能力」，提供與晶片廠或軟體供應商的**維護合約 (SLA)** 摘要，證明在產品生命週期內，供應商有義務提供 Security Patch。
        * 或者提供最近一次供應商釋出 SDK Patch 的 Release Note，證明上游還是活的。

* **測試與驗證**：
    * **評分演練**：
        * 拿一個已知的歷史漏洞（例如 Log4j），請安全團隊成員試算 CVSS 分數。
        * 確認算出來的分數與 NVD 官方分數接近，證明團隊懂得如何使用 CVSS 標準。

---
[回到 Lifecycle Documents](./lifecycle-documents.md)