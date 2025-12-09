## 生命週期文件 (LIFECYCLE DOCUMENTS)

### 條款 CK-LP-06

您是否維護一份包含組件版本、已應用修補程式與更新的組件清單 (inventory of components)？

#### 最低要求 (Minimum Requirements)

* 必須有一份維護良好的組件清單，其中包含版本、已應用的修補程式與更新。
* 可接受的設備組件清單範例包括但不限於：
    * **軟體物料清單 (SBOM)**
    * **硬體物料清單 (HBOM)**
    * **行動應用程式物料清單 (Mobile application BOM)**
    * **版本控制系統 (Version control system)**

#### 佐證證據 (Supporting Evidence)

* 開發商應提供設備的物料清單，至少需標示出**使用的組件**、**組件版本**以及其**授權 (license)**。
* 如適用，開發商應提供行動應用程式 BOM 與版本控制系統（例如：subversion, git 等）。

#### 評估 (Assessment)

* 評估人員將檢查是否有一份維護良好的組件清單被追蹤，並以合適的格式呈現，該清單至少需標示出使用的組件，連同其版本號碼與對應的授權。

---

### 開發者深度導讀 (針對 Gateway / App / Cloud 開發商)

#### 本章節核心要求與意涵

本條款與 **CK-LP-03 (安全供應鏈)** 相輔相成，但 CK-LP-03 重在「選擇與評估」，而 CK-LP-06 重在**「記錄與追蹤」**。

1.  **資產盤點 (Asset Inventory)**：
    * 在發生 Log4j 這樣的重大漏洞時，資安團隊的第一個問題通常是：「我們有哪些產品用了 Log4j？版本是多少？」
    * 如果沒有維護良好的 SBOM，您就無法回答這個問題，只能盲目地去掃描所有程式碼。CK-LP-06 要求您必須隨時能回答這個問題。
2.  **授權合規 (License Compliance)**：
    * 雖然 CLS 是資安標準，但這裡特別要求列出 **License**（如 GPL, MIT, Apache）。這是因為開源授權衝突可能導致法律風險，進而影響產品的維護與更新能力。

#### 具體落地實現方案建議

* **系統設計與自動化生成**：
    * **嵌入式系統 (Yocto/Buildroot)**：
        * 這些構建系統通常內建 SBOM 生成功能。
        * **Yocto**: 設定 `INHERIT += "create-spdx"`，編譯時會自動吐出 SPDX 格式的清單。
    * **行動應用程式 (Android/iOS)**：
        * **Gradle (Android)**: 使用 `CycloneDX Gradle Plugin`。
        * **CocoaPods/SwiftPM (iOS)**: 匯出 `Podfile.lock` 或 `Package.resolved` 並轉換為標準 BOM 格式。

* **證據收集策略**：
    * **SBOM 匯出檔**：
        * 提供一份 Excel 或 PDF，欄位包含：`Component Name`, `Version`, `License`, `Source URL`。
        * 範例：
            * `OpenSSL` | `1.1.1t` | `Apache-2.0` | `https://openssl.org`
            * `cJSON` | `1.7.15` | `MIT` | `https://github.com/DaveGamble/cJSON`
    * **Git 截圖**：
        * 雖然條款接受 VCS，但建議作為輔助。截取 GitLab/GitHub 的 Repository 首頁，顯示 `tags` 列表，證明每個發布版本都有明確的 Tag (如 `v1.0.0_release`)。

* **測試與驗證**：
    * **一致性檢查**：
        * QA 隨機檢查 SBOM 上列出的某個套件版本（例如 `curl 7.68.0`）。
        * 登入設備執行 `curl --version`。
        * **預期結果**：版本號必須完全一致。如果設備上跑的是 7.80.0 但 SBOM 寫 7.68.0，代表清單未維護，這是不合規的。