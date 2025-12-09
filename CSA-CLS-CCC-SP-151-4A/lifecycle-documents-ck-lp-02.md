## 生命週期文件 (LIFECYCLE DOCUMENTS)

### 條款 CK-LP-02

您是否使用安全工程方法 (secure engineering approach) 來設計與開發設備？

#### 最低要求 (Minimum Requirements)

* 在開發設備（包括其配套應用程式及其他相關服務，如適用）時，必須在**「開發實務 (Development Practices)」**與**「測試 (Testing)」**這兩個類別中，各採用至少一種安全工程方法。

**類別一：開發實務 (Development Practices) - 範例（非詳盡列表）：**

1.  **安全編碼實務 (Secure coding practices)**：
    * 驗證所有輸入、輸出並進行適當編碼。
    * 偵測並處理錯誤。
    * 避免使用不安全的函數與呼叫。
    * 遵循安全編碼標準與指引。
    * 原始碼混淆 (Source code obfuscation)。
2.  **重複使用既有的安全軟體函式庫**：
    * 已部署的軟體組件如何進行更新。
    * 使用程式碼儲存庫 (Code repository) 來儲存與維護安全軟體，以便在適當時重複使用。
3.  **使用非預設、組織良好的編譯器、直譯器與建置流程**：
    * 使用提供如記憶體位址隨機化 (randomisation of memory location) 等功能的編譯器、直譯器與建置工具，以提升執行檔的安全性。
4.  **其他**：
    * 輸入的密碼字元被特殊字元遮蔽，不以明文顯示。
    * 在一段時間後鎖定或終止閒置連線 (inactive session)，並防止在重新連線時重複使用連線資訊。

**類別二：測試 (Testing) - 範例（非詳盡列表）：**

1.  **針對安全功能的實用測試**：
    * 靜態應用程式安全測試 (SAST)。
    * 動態應用程式安全測試 (DAST)。
    * API 測試。
    * 模糊測試 (Fuzz testing)。
2.  **開發者和/或同儕程式碼審查 (Peer code review) 系統**：
    * 使用追蹤系統進行程式碼審查、回饋，並提供發現問題的修補狀態。
3.  **軟體預設部署於安全設定**：
    * 文件反映每個設備設定的目的、選項、預設值、安全關聯性、操作影響，以及與其他設定的關係。
4.  **其他**

#### 佐證證據 (Supporting Evidence)

* 開發商應宣告在開發設備（包括其配套應用程式及其他相關服務，如適用）時，採用了哪些安全工程方法。
* 為了證明已採用安全工程方法，開發商應提供證據，形式包括但不限於：
    * 顯示開發商內部為提升設備安全性所執行的步驟/流程的流程/指引文件。
    * 開發商用於內部追蹤問題與程式碼審查的工具截圖（例如：JIRA 等）。
    * 提供滲透測試、靜態/動態分析報告等，或這些報告相關部分的截圖。

#### 評估 (Assessment)

* 評估人員將檢查開發商是否在開發設備（包括其配套應用程式及其他相關服務，如適用）時，從「開發實務」與「測試」類別中各採用了至少一種安全工程方法。
* 評估人員將檢查是否使用了適當的測試方法與工具，以判斷所執行測試的適用性。

---

### 開發者深度導讀 (針對 Gateway / App / Cloud 開發商)

#### 本章節核心要求與意涵

本條款要求建立**SSDLC (Secure Software Development Life Cycle)**。這意味著安全性不能只是最後一關的「滲透測試報告」，而是必須內建在 CI/CD 流程與開發習慣中。

1.  **二選一的強制性**：
    * 您必須從「開發」選一項，從「測試」選一項。
    * **最推薦組合**：
        * **開發**：使用編譯器強化 (Compiler Hardening) 或 安全編碼標準。
        * **測試**：實作 SAST (靜態分析) 或 同儕審查 (Code Review)。
        * 這兩項通常最容易整合進現有的 DevOps 流程中。
2.  **編譯器強化 (Compiler Hardening)**：
    * 對於 Gateway (通常是 Linux/OpenWrt) 開發者來說，這是 CP 值最高的加分項。只要在 Makefile 加入幾個 Flag，就能大幅提升 Binary 的抗攻擊能力（防 Buffer Overflow, ROP）。

#### 具體落地實現方案建議

* **技術實作：編譯器選項 (GCC/Clang)**：
    * 確保您的 Build System (如 Buildroot, Yocto) 全域開啟以下 Flags：
        * **Stack Canary**: `-fstack-protector-strong` (偵測 Stack Overflow)。
        * **NX / DEP**: `-z noexecstack` (防止在 Stack 上執行程式碼)。
        * **RELRO**: `-z relro -z now` (防止 Global Offset Table 被覆寫)。
        * **PIE**: `-fPIE -pie` (位置無關執行檔，配合 ASLR)。
        * **Fortify Source**: `-D_FORTIFY_SOURCE=2`。

* **技術實作：自動化測試 (SAST/DAST)**：
    * **SAST (Static Application Security Testing)**：
        * 在 Git Push 時自動觸發掃描。
        * **免費工具推薦**：SonarQube (支援多語言), Bandit (Python), Cppcheck (C/C++), Trivy (Container/Filesystem)。
    * **Code Review 流程**：
        * 在 GitLab/GitHub 設定 "Branch Protection" 規則：主分支 (Master/Main) 不允許直接 Push，必須透過 Merge Request (MR/PR)，且至少需要一人核准 (Approve)。

* **證據收集策略**：
    * **編譯 Log**：
        * 截取編譯過程的 Log，用螢光筆標示出上述的 GCC Flags (如 `-fstack-protector`)。這是證明「開發實務 #3」的最有力證據。
    * **SAST 報告截圖**：
        * 截取 SonarQube 或 Trivy 的 Dashboard，顯示掃描了多少行程式碼、發現了多少漏洞（以及已修復的狀態）。
    * **Pull Request 截圖**：
        * 截取一張 Git PR 的畫面，顯示有同事的 "Review Comments" 以及 "Approved" 標記，證明有落實「同儕審查」。

* **測試與驗證**：
    * **Binary 檢查 (Checksec)**：
        * QA 或資安人員可以使用 `checksec.sh` 腳本來檢查編譯出來的韌體執行檔。
        * **預期結果**：RELRO, Canary, NX, PIE 欄位應顯示為綠色的 "Enabled"。