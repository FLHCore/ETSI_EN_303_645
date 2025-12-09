## 生命週期文件 (LIFECYCLE DOCUMENTS)

### 條款 CK-LP-05

您是否確保設備在發布前已進行強化 (hardened)？

#### 最低要求 (Minimum Requirements)

* 設備在發布前必須進行**強化 (hardened)**。設備強化措施的範例包括但不限於：
    * 關閉未使用 (unused) 的連接埠與服務。
    * 移除所有後門 (backdoors)。
    * 從發布版本中移除所有除錯程式碼 (debug codes)。
    * 必須移除不必要的帳號。
    * 必須停用不必要的網路介面。
    * 啟用作業系統的安全功能。
    * 阻擋未授權的網路流量，或阻擋來自未在網路存取控制策略中註冊設備的流量。

#### 佐證證據 (Supporting Evidence)

* 開發商應描述設備強化是如何執行的，並提供其開發團隊所遵循的指示/流程文件。
* 開發商應執行 **nmap 掃描**並提供輸出結果作為證據（例如：截圖、nmap 輸出檔等），以顯示所有未使用的連接埠皆已關閉。
    * 通訊埠掃描可使用以下指令執行：`nmap -sT -sU -A -p- <ip address>`
* 如適用，開發商應提供證據（例如：截圖、掃描結果等），顯示已使用掃描工具檢查並確認除錯/後門程式碼或硬編碼安全憑證已從設備的生產版本中移除。
* 如適用，開發商應提供證據（例如：截圖、文件、照片等），顯示所有實體除錯連接埠（如 **UART**）在實體上已被停用且無法存取。
    * (我們建議使用 **PuTTY** 來獲取此證據)。

#### 評估 (Assessment)

* 評估人員將檢查設備強化是否已依照開發商提供的指示/流程執行。
* 評估人員將檢查 nmap 報告，確認所有未使用的連接埠皆已關閉。
* 如適用，評估人員將檢查證據，以判斷除錯/後門程式碼或硬編碼安全憑證是否已從設備的生產版本中移除。
* 如適用，評估人員將檢查證據，以判斷實體除錯連接埠（如 UART）是否在實體上已被停用且無法存取。

---

### 開發者深度導讀 (針對 Gateway / App / Cloud 開發商)

#### 本章節核心要求與意涵

本條款是產品上市前的**最後一道防線**，也就是所謂的 **Gold Master (GM) 驗收標準**。

1.  **不僅僅是關 Port**：
    * 雖然 Nmap 掃描是重點，但「強化 (Hardening)」的範圍更廣。它包含了 OS 層級的設定（如 Linux Kernel Hardening）、檔案系統權限（移除 `chmod 777`）、以及二進位檔案的淨化（Stripping Symbols）。
2.  **明確的反後門 (Anti-Backdoor) 要求**：
    * 過去許多設備因為RD為了方便維修而留下的「萬用密碼」或「隱藏指令」而被詬病。此條款明確要求**「移除所有後門」**。這意味著您不能在程式碼裡寫 `if (password == "super_secret_backdoor") allow_login()`。
3.  **作業系統安全功能**：
    * 對於嵌入式 Linux，這通常指啟用 **ASLR (Address Space Layout Randomization)**、**DEP/NX**，或是使用 **AppArmor / SELinux** 來限制 Process 權限。

#### 具體落地實現方案建議

* **系統設計與 Build 腳本**：
    * **Binary Stripping**：
        * 在編譯 Release 版本時，務必對所有執行檔與函式庫執行 `strip` 指令，移除 Symbol Table。這能增加逆向工程的難度，並移除可能洩漏路徑資訊的字串。
    * **檔案權限檢查**：
        * 執行腳本掃描 Root Filesystem，確保沒有檔案是 World-Writable (`o+w`) 的，特別是 `/etc/shadow`, `/etc/passwd`, 和啟動腳本。
    * **移除不必要的使用者**：
        * 檢查 `/etc/passwd`，移除如 `ftp`, `news`, `uucp` 等嵌入式設備用不到的預設帳號。

* **證據收集策略**：
    * **強化檢查表 (Hardening Checklist)**：
        * 這是最關鍵的文件證據。提供一份內部簽核的 Excel 表，列出如："SSH Disabled: Pass", "UART Disabled: Pass", "Root Password Changed: Pass"。
    * **PuTTY「黑畫面」截圖**：
        * 這是 **Provision 5.6-4/7.6-1** 的再確認。接上 UART，打開 PuTTY，截取那個「什麼都沒顯示」的黑畫面，證明實體除錯口已死。
    * **靜態掃描報告**：
        * 使用工具掃描原始碼中的 "TODO", "FIXME", "HACK" 等關鍵字，證明沒有遺留臨時程式碼。

* **測試與驗證**：
    * **滲透測試工具掃描**：
        * 使用 **Firmwalker** 或類似工具掃描解包後的 Firmware，尋找是否有被遺忘的憑證檔案 (如 `.pem`, `.key`) 或敏感字串。
    * **權限提權測試**：
        * 假設駭客取得了一個低權限 Shell (如 `nobody` 或 `www-data`)，測試他是否能讀取 `/etc/shadow` 或寫入 `/etc/config/`。強化的系統應能阻止這類橫向移動。