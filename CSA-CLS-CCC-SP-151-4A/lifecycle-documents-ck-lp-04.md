## 生命週期文件 (LIFECYCLE DOCUMENTS)

### 條款 CK-LP-04

您是否以簡單的語言且及時的方式，提供、溝通並更新安全資訊（服務條款、功能、指引、說明與通知等）？

#### 最低要求 (Minimum Requirements)

* 必須向設備使用者提供**安全資訊**（例如：發布給使用者關於更新的資訊、提供給使用者關於更新所減緩風險的資訊等）。

#### 佐證證據 (Supporting Evidence)

* 開發商應提供證據（例如：截圖、文件、網頁等），顯示安全資訊已傳達給使用者。
* 可能的範例包括但不限於：
    * 發布在開發商網站上的官方聲明。
    * 張貼在開發商社群媒體帳號上的公告 (Advisories)。
    * 設備介面上的通知。
    * 設備更新日誌 (Device changelogs)。
    * 修補說明 (Patch notes)。

#### 評估 (Assessment)

* 評估人員將檢查安全資訊是否已傳達給使用者。

---

### 開發者深度導讀 (針對 Gateway / App / Cloud 開發商)

#### 本章節核心要求與意涵

本條款關注的是**「安全溝通 (Security Communication)」**的品質與時效性。

1.  **不僅僅是 "Bug Fixes"**：
    * 開發者在撰寫 Release Notes 時，常習慣只寫一行 "Bug fixes and performance improvements"。
    * **合規要求**：如果該次更新修補了安全性漏洞，必須明確告知使用者。這有助於使用者判斷更新的急迫性。
2.  **簡單語言 (Simple Language)**：
    * 條款標題特別強調「簡單語言」。這意味著您不應該直接貼上 `Fixed heap overflow in libxyz.so at address 0x1234`。
    * **正確範例**：「修復了一個可能允許未授權使用者存取您設備的安全問題 (Fixed a security issue that could allow unauthorized access)。」
3.  **多管道通知**：
    * 不要指望使用者會主動去逛官網。訊息應該推送到使用者面前（如 App 推播、設備 UI 彈窗）。

#### 具體落地實現方案建議

* **系統設計與發布流程**：
    * **Release Note 欄位規劃**：
        * 在後端 Update Server 的 API 回應中，除了 `version` 和 `download_url`，應增加 `release_notes` 與 `severity` 欄位。
        * 當 `severity == Critical` 時，App 端應顯示紅色警示圖示，並將 Release Note 放在顯眼位置。
    * **安全公告頁面 (Security Advisories)**：
        * 在官網建立一個 `/security/advisories` 頁面，按年份列出所有已修補的 CVE 與對應的韌體版本。這是展現負責態度的最佳方式。

* **證據收集策略**：
    * **App Store 更新日誌**：
        * 截取 iOS App Store 或 Google Play 的 "What's New" 區塊，其中包含 "Security Updates" 的字樣。
    * **韌體更新彈窗**：
        * 截取 App 或 Web GUI 偵測到新韌體時的彈窗，內容需包含修補說明的文字。
    * **社群媒體貼文**：
        * 如果曾發生重大漏洞（如 KRACK, Log4j），截取公司 Facebook/Twitter 當時發布的「請用戶儘速更新」貼文。

* **測試與驗證**：
    * **UI 檢查**：
        * QA 在測試 OTA 時，需確認後端設定的 Release Note 文字能完整顯示在前端 UI 上，且沒有亂碼或被截斷。

---
[回到 Lifecycle Documents](./lifecycle-documents.md)