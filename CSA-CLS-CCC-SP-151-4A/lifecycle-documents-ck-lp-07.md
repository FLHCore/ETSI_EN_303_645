## 生命週期文件 (LIFECYCLE DOCUMENTS)

### 條款 CK-LP-07

您是否定期以及在每次主要版本發布前，執行滲透測試 (penetration testing) 和/或弱點評估 (vulnerability assessment)？

#### 最低要求 (Minimum Requirements)

* 必須**定期 (periodically)** 以及在**發布重大更新 (major updates)** 之前，執行滲透測試和/或弱點評估。

#### 佐證證據 (Supporting Evidence)

* 開發商應宣告是否在內部定期以及在重大更新發布前，執行滲透測試和/或弱點評估。
* 開發商應提供證據（例如：內部文件、VA/PT 報告等），顯示這些測試是**如何執行的**、**由誰執行**、**頻率為何**，以及**使用的工具**。

#### 評估 (Assessment)

* 評估人員將檢查提供的證據，以確認這些測試與評估已在設備上定期執行，並在重大更新前執行。
* 評估人員將檢查開發商列出的工具是否能執行有效的滲透測試和/或弱點評估。

---

### 開發者深度導讀 (針對 Gateway / App / Cloud 開發商)

#### 本章節核心要求與意涵

本條款是關於**「驗證 (Validation)」**。如果 CK-LP-01 是「想」，CK-LP-02 是「做」，那 CK-LP-07 就是「測」。

1.  **VA 與 PT 的區別**：
    * **弱點評估 (Vulnerability Assessment, VA)**：通常指使用自動化工具（如 Nessus, OpenVAS, OWASP ZAP）進行掃描，找出已知漏洞。速度快，廣度高，但深度淺。
    * **滲透測試 (Penetration Testing, PT)**：通常指由真人（紅隊或外部資安公司）模擬駭客攻擊，嘗試利用漏洞串接 (Chaining) 來取得控制權。深度高，但成本昂貴。
    * **合規策略**：條款寫 "and/or"，意味著最低限度下只做 VA 可能過關，但建議針對重大版本做 PT，日常版本做 VA。
2.  **「重大更新」的定義**：
    * 您必須在內部政策中定義什麼是「重大更新 (Major Update)」。
    * 通常指：版本號第一碼變更 (v1.0 -> v2.0)、更換底層 OS/Kernel、新增網路服務 (如新增 VPN 功能)、或變更認證機制。



#### 具體落地實現方案建議

* **流程整合 (DevSecOps)**：
    * **自動化 VA**：
        * 在 CI/CD Pipeline 中整合 **DAST (Dynamic Application Security Testing)** 工具。
        * 例如：每次 Release Build 完成後，自動觸發 OWASP ZAP 針對 Web GUI 進行掃描。
    * **週期性 PT**：
        * 設定行事曆，例如「每半年」或「每年」聘請外部廠商進行一次完整的滲透測試。

* **工具鏈建議**：
    * **VA 工具**：Nessus, OpenVAS, Qualys, OWASP ZAP (針對 Web), Burp Suite Pro.
    * **PT 工具**：Metasploit, Hydra (暴力破解), Nmap, Wireshark, SQLMap.

* **證據收集策略**：
    * **報告封面與摘要**：
        * 不需要提交幾百頁的完整漏洞報告（這可能包含過多敏感細節）。
        * **關鍵證據**：提交報告的「封面 (Cover Page)」與「執行摘要 (Executive Summary)」。
        * 封面需包含：**日期** (證明是新的)、**目標版本** (證明針對特定版本)、**測試單位** (證明是誰測的)。
    * **工具使用紀錄**：
        * 提供自動化掃描工具的 Log 或 Dashboard 截圖，證明掃描確實有在跑。

* **測試與驗證**：
    * **漏洞修復追蹤 (Remediation Tracking)**：
        * 如果 VA/PT 報告中發現了 High/Critical 漏洞，您必須同時提供「修復證明」或「緩解計畫」。
        * 評估人員可能會問：「這份報告顯示有 SQL Injection，請問你們修了嗎？」您需要出示對應的 JIRA Ticket 和修復後的複測報告 (Re-test Report)。

---
[回到 Lifecycle Documents](./lifecycle-documents.md)