## 生命週期文件 (LIFECYCLE DOCUMENTS)

### 條款 CK-LP-01

您是否已執行威脅建模 (threat modelling)，以識別、分析並減緩針對設備的威脅？

#### 最低要求 (Minimum Requirements)

* 必須執行**威脅建模**，以識別、分析並減緩針對設備的威脅。

#### 佐證證據 (Supporting Evidence)

* 開發商應提供證據（例如：內部軟體開發生命週期流程文件、流程圖等），顯示威脅建模流程是設備開發生命週期的一部分。
* 威脅建模流程應包含下列事項：
    * 定義安全問題 (Defining the security problem)
    * 執行風險評估 (Conduct risk assessment)
    * 決定安全目標 (Determine the security objectives)
    * 定義安全需求 (Define the security requirements)
    * 設計與實作 (Design and implement)
    * 驗證與確認 (Validate and verify) 設備安全能力是否解決了安全需求
* 或者，開發商亦可提供對設備執行的威脅建模**結果**作為證據。
    * 在此情況下，證據應包含安全問題、安全目標（預期結果），並隨後描述實作的安全能力如何協助減緩威脅建模過程中識別出的風險。

#### 評估 (Assessment)

* 評估人員將檢查開發商執行的威脅建模，並驗證其是否包含最低要求中陳述的關鍵點。
* 評估人員亦將檢查開發商宣告的安全功能，是否足以減緩威脅建模過程中提出的風險。

---

### 開發者深度導讀 (針對 Gateway / App / Cloud 開發商)

#### 本章節核心要求與意涵

從這裡開始，評估重點從「產品功能 (Product Features)」轉向**「開發流程 (Development Process)」**。CK-LP-01 要求證明您在寫第一行程式碼之前，已經想過駭客會怎麼攻擊。

1.  **Security by Design (設計階段的安全性)**：
    * 審查員不想看到「補丁式」的安全（出了 Bug 才修）。他們想看到您在架構設計階段就考慮了資安。
    * **威脅建模不是弱點掃描**：請區分兩者。弱點掃描是針對成品的測試；威脅建模是針對架構的分析。
2.  **結構化分析**：
    * 不能只列出「我們有加防火牆」。必須展示「因為我們識別了 DoS 攻擊風險，所以設計了防火牆」。這是一個 **問題 -> 風險 -> 對策** 的邏輯鏈。

#### 具體落地實現方案建議

* **採用標準方法論**：
    * **STRIDE 模型**：這是業界最通用的標準（由微軟提出）。建議開發團隊針對 Gateway 的每個介面（Wi-Fi, WAN, UART, App API）進行 STRIDE 分析：
        * **S**poofing (假冒身分)
        * **T**ampering (竄改數據)
        * **R**epudiation (抵賴)
        * **I**nformation Disclosure (資訊洩漏)
        * **D**enial of Service (阻斷服務)
        * **E**levation of Privilege (權限提升)
    * **資料流圖 (DFD)**：畫出資料如何在使用者、App、雲端、Gateway 之間流動，並標示出「信任邊界 (Trust Boundaries)」。攻擊通常發生在跨越邊界的地方。

* **證據收集策略**：
    * **威脅建模報告 (Threat Modeling Report)**：
        * 使用 **Microsoft Threat Modeling Tool** (免費工具) 畫出 DFD，它會自動生成一份 HTML 報告，列出潛在威脅。這份報告是完美的佐證證據。
    * **JIRA/Issue Tracker 關聯**：
        * 截取 JIRA 畫面，顯示某個 Security Ticket (例如 "Implement TLS 1.2") 是連結到某個 Threat ID (例如 "Threat #5: Man-in-the-Middle")。這證明了「驗證與確認」環節的落實。
    * **Excel 風險對照表**：
        * 如果不用專用工具，準備一份 Excel：
          | 資產 | 威脅描述 | 風險等級 | 緩解措施 | 驗證狀態 |
          | :--- | :--- | :--- | :--- | :--- |
          | Admin Password | 暴力破解 | High | 實作速率限制 (5.1-5) | Pass |

* **測試與驗證**：
    * **文件一致性檢查**：
        * 確保威脅建模報告中提到的緩解措施（例如「所有 API 都有鑑權」），在實際產品中真的有做，且在前面的章節（如 5.5-5）有提供證據。評估人員會交叉比對。