Annex B: Case Study on Home Control System (informative) 
===

### 節次 1：Overview (概覽)

**📌 原文翻譯**

> [35] 本附件介紹了一個關於家庭控制系統 (HCS) 的案例研究，並示範了如何將主文件中的建議應用於此案例研究。
> [36] 本案例研究並非詳盡無遺，其範例應用也不是 HCS 的最終定義，僅供說明之用。
> [37] 表 B-1 描述了主文件中定義的威脅建模檢查清單，及其在 HCS 案例研究中的應用。

**💡 智慧家庭網關 (HSG) 開發人員重點提醒**

* [cite_start]**學習方法，而非複製範例：** 這份文件提供的不只是一個 HCS 範例，更重要的是它展示了一套完整的「威脅建模流程」(Threat Modelling Checklist) [cite: 37, 38]。您開發的網關功能可能與此案例不同，但您**必須**學習並應用這套「方法論」來分析您自己的產品。
* [cite_start]**範例的用途：** 這個 HCS 案例是為了「說明」安全建議如何落地 [cite: 36]。在後續章節中，當您看到 HCS 範例時，應思考：「**如果將這個威脅或安全需求，套用在我開發的網關上，會是什麼樣子？**」
* [cite_start]**掌握核心清單：** 「表 B-1」[cite: 37, 38] 是本附件的靈魂。它預告了接下來所有章節的內容：從識別保護目標、定義安全問題、風險評估，一路到最後的安全需求。這就是您在產品開發週期中應遵循的安全分析藍圖。

---

### 條文 1：Identify the potential targets to be protected (識別要保護的潛在目標)

[cite_start]本節的目標是完整拆解您的系統，為後續的威脅分析建立一個清晰的藍圖 [cite: 38]。

#### 1a. [cite_start]Define its boundaries and the external systems (including users) that it needs to interact with (定義其邊界及其需要互動的外部系統 (包括使用者)) [cite: 38]

**📌 案例內容 (參照 Section 2)**
[cite_start]文件明確定義了兩個系統邊界 [cite: 110]：
* [cite_start]**邊界 A (Boundary A):** 涵蓋家庭環境內的所有子組件 [cite: 111][cite_start]，包括 HSG (網關)、智慧設備 (如門鎖、電視) 和受限的感測器網路 [cite: 83-105]。
* [cite_start]**邊界 B (Boundary B):** 包含託管在雲端基礎設施上的感測器網路整合平台 (SNIP) [cite: 111, 76-80]。
* **外部系統/使用者:** 包括:
    * [cite_start]Web 應用 (Web application) [cite: 68]
    * [cite_start]行動應用 (Mobile application) [cite: 88]
    * [cite_start]後端系統 (Backend system) [cite: 66]

**💡 智慧家庭網關 (HSG) 開發人員重點提醒**
* **您是「邊界 A」的守門員：** 您的 HSG 設備是家庭內部網路 (LAN/Sensor Network) 和外部網路 (WAN/Access Network) 之間最關鍵的關卡。
* **邊界本身就是攻擊面：** 任何跨越「邊界 A」的資料流 (例如 HSG 連到 SNIP，或 App 本地連線到 HSG)，都是最高風險的攻擊點，必須受到嚴格審查。

**🛠️ 網關 (HSG) 工程實作建議**
* **建立防火牆規則：** 在您的 HSG 軟體中 (例如使用 `iptables` 或 `nftables`)，嚴格區分 `LAN_if` (對內) 和 `WAN_if` (對外) 的網路介面。
* **預設拒絕 (Default-Deny)：** 除非明確允許 (例如連線到 SNIP 的 8883 埠)，否則應阻擋所有來自內網設備主動連線到外部網路的流量。

---

#### 1b. [cite_start]Decompose the target(s) into its subcomponents (將目標分解為其子組件) [cite: 38]

**📌 案例內容 (參照 Section 2)**
[cite_start]**圖 B-1** 清楚地將 HCS 分解為以下主要組件 [cite: 64, 109]：
* [cite_start]**雲端 (邊界 B):** SNIP (感測器網路整合平台) [cite: 79][cite_start]、後端系統 [cite: 66][cite_start]、Web 應用 [cite: 68][cite_start]、行動應用 (遠端) [cite: 88]。
* **家庭 (邊界 A):**
    * [cite_start]**閘道 (Gateway):** HSG (家庭感測器閘道) [cite: 85]。
    * [cite_start]**終端節點 (End Node):** 智慧插座 [cite: 100][cite_start]、冷氣 [cite: 101][cite_start]、電視 [cite: 102][cite_start]、洗衣機 [cite: 103][cite_start]、煙霧偵測器 [cite: 104][cite_start]、門鎖控制 [cite: 105]。
    * [cite_start]**非智慧設備:** 燈 [cite: 107][cite_start]、水壺 [cite: 108]。

**💡 智慧家庭網關 (HSG) 開發人員重點提醒**
* **HSG 內部的子組件：** 這個案例只將 HSG 視為一個「黑盒子」。身為開發者，您必須進一步將 **您的 HSG** 分解為更小的子組件。
* **您的分解清單：** 您的清單應包含：Web 伺服器 (管理介面)、OTA 更新代理程式、MQTT 客戶端 (連雲端)、Zigbee/BLE 協定堆疊、憑證儲存庫、本地資料庫 (存日誌)、硬體加解密引擎 (TPM/TEE) 等。

**🛠️ 網關 (HSG) 工程實作建議**
* **繪製內部架構圖：** 針對您的 HSG，繪製一張詳細的「軟體組件圖」。
* **最小權限原則：** 確保每個組件 (例如 Web 伺服器) 僅以執行其功能所需的「最低權限」使用者 (例如 `www-data` 而非 `root`) 運行。

---

#### 1c. [cite_start]Identify data flows within the target(s), and inputs and outputs from external systems (識別目標內部的資料流，以及來自外部系統的輸入和輸出) [cite: 38]

**📌 案例內容 (參照 Section 2)**
[cite_start]圖 B-1 和表 B-3 標示了關鍵資料流 [cite: 109, 226]：
* [cite_start]**上行資料流:** 設備 → HSG [cite: 193][cite_start]、HSG ↔ SNIP [cite: 198][cite_start]、SNIP → 後端系統 [cite: 203]。
* [cite_start]**下行/控制流 (遠端):** Web 應用 → SNIP ↔ HSG ↔ 設備 [cite: 208-213][cite_start]；行動應用 → SNIP ↔ HSG ↔ 設備 [cite: 214-219]。
* [cite_start]**下行/控制流 (本地):** 行動應用 → HSG ↔ 設備 [cite: 220]。
* [cite_start]**輸入/輸出:** 警報 (Alerts)、管理存取 (Admin access)、本地存取 (Local access)、遠端存取 (Remote access)、開/關 (On/off)、鎖/解鎖 (Lock/unlock) [cite: 69, 71, 89, 91, 96, 97, 98]。

**💡 智慧家庭網關 (HSG) 開發人員重點提醒**
* [cite_start]**本地 vs. 遠端：** 文件明確區分了「遠端存取」和「本地存取」 [cite: 215, 224]。這兩條路徑的安全需求和信任等級完全不同。
* [cite_start]**HSG 的責任：** 您的 HSG 是所有這些資料流的「中介者」 [cite: 115]。您必須處理每條資料流的認證 (Authentication) 和授權 (Authorization)。

**🛠️ 網關 (HSG) 工程實作建議**
* **繪製資料流圖 (DFD)：** 針對您的 HSG 畫出詳細的資料流圖。
* **API 端點盤點：** 列出您的 HSG 提供的「所有」 API 端點 (RESTful API, MQTT topics, WebSockets)，並標記它們是「本地存取」還是「遠端存取」。

---

#### 1d. [cite_start]Identify sensitive data and where they are handled (at rest, in transit, in use) (識別敏感資料及其處理位置 (靜態、傳輸中、使用中)) [cite: 38]

**📌 案例內容 (參照 Section 2)**
文件指出了幾個敏感資料的儲存點：
* [cite_start]**HSG:** 「可能儲存敏感資料」 (potentially host sensitive data) [cite: 115]。
* [cite_start]**SNIP:** 「可能儲存敏感資料」 (probably host sensitive data) [cite: 120]。
* [cite_start]**資料流:** 圖 B-1 將 HSG 和 SNIP 之間的資料標記為「敏感資料」 (Sensitive data) [cite: 79, 86]。
* [cite_start]**表 B-3** 強調了 `HSG ↔ SNIP` 和遠端存取資料流需要「高機密性 (H)」 [cite: 199, 216]，這暗示了這些是敏感資料流。

**💡 智慧家庭網關 (HSG) 開發人員重點提醒**
* **HSG 的敏感資料：** 對您 (HSG 開發者) 而言，敏感資料包括 (但不限於)：
    * **靜態 (At rest / 儲存時):** Wi-Fi 密碼、雲端 (SNIP) 的金鑰或憑證、本地管理員密碼、設備配對金鑰 (如 Zigbee network key)、儲存的使用者隱私資料 (如門鎖日誌)。
    * **傳輸中 (In transit / 傳輸時):** 傳遞給雲端的控制命令 (如「開鎖」)、使用者登入憑證、韌體更新包。
    * **使用中 (In use / 記憶體中):** 上述資料在 RAM 中解密後的狀態、暫存的 session token。

**🛠️ 網關 (HSG) 工程實作建議**
* **靜態資料加密：** 使用檔案系統層級加密 (如 `dm-crypt`) 或至少對儲存憑證的檔案進行加密。金鑰「必須」儲存在硬體安全模組 (如 TPM, TEE) 中。
* **傳輸中資料加密：** 見下一節 (1e) 的高機C密性要求。
* **使用中資料保護：** 最小化敏感資料在記憶體中停留的時間。在處理完畢後立即清除 (zero-fill) 該記憶體區塊。

---

#### 1e. [cite_start]Identify the security needs (based on potential impacts to CIA triad) for subcomponents and data flows (識別子組件和資料流的安全需求 (基於對 CIA 三元組的潛在影響)) [cite: 38]

**📌 案例內容 (參照 Section 2)**
這是本節的核心，由 **表 B-2 (資產)** 和 **表 B-3 (資料流)** 完整定義。
* [cite_start]**表 B-2 (資產安全需求):** [cite: 183]
    * [cite_start]**HSG (您的設備):** 機密性 (H)、完整性 (H)、可用性 (M) [cite: 138-140][cite_start]。理由：與 SNIP 同樣需要高機密性和完整性；可用性為中，因僅影響單一家庭 [cite: 141]。
    * [cite_start]**門鎖控制 (Door control):** 機密性 (M)、完整性 (H)、可用性 (H) [cite: 163-165][cite_start]。理由：完整性和可用性對正常運作至關重要 [cite: 174]。
* [cite_start]**表 B-3 (資料流安全需求):** [cite: 226]
    * [cite_start]**HSG ↔ SNIP (遠端):** 機密性 (H)、完整性 (H)、可用性 (H) [cite: 199-201]。
    * [cite_start]**行動應用 → HSG (本地):** 機密性 (M)、完整性 (H)、可用性 (M) [cite: 221-223]。

**💡 智慧家庭網關 (HSG) 開發人員重點提醒**
* [cite_start]**「完整性 (H)」是您的第一要務：** 對於 HSG、門鎖、煙霧偵測器 [cite: 159, 164, 139]，「高完整性」是最高共識。這意味著「**防止命令被竄改**」比「防止命令被竊聽」更重要。一個加密但可被竄改的「開鎖」命令是災難性的。
* [cite_start]**本地 vs. 遠端 (CIA 差異)：** 注意本地存取的機密性僅為「M」 [cite: 221][cite_start]，而遠端為「H」 [cite: 216][cite_start]。這暗示文件假設「本地網路 (家中 Wi-Fi)」相對「網際網路」更可信，但「高完整性 (H)」 [cite: 222] 依然是必須的 (防止家中其他被駭的設備，如電視，來偽造命令)。

**🛠️ 網關 (HSG) 工程實作建議**
* **實作高完整性 (H)：**
    * [cite_start]**傳輸層：** 使用 **TLS 1.2/1.3** (提供基礎完整性) [cite: 414] (參照 Section 6)。
    * **應用層：** 在 TLS 之上，所有 API 請求應包含「訊息鑑別碼 (HMAC)」或「數位簽章」，以確保命令未被 (例如惡意的雲端管理員或中間人) 竄改。
* **實作高機密性 (H)：**
    * [cite_start]**傳輸層：** 必須使用 **TLS** 進行點對點加密 [cite: 414] (參照 Section 6)。
    * **應用層 (可選)：** 對於極度敏感的資料 (如韌體更新金鑰)，可考慮在 TLS 內部再進行一次「酬載加密 (Payload Encryption)」。

---

#### 1f. [cite_start]Identify hardware, software and protocols in use (識別使用中的硬體、軟體和協定) [cite: 38]

**📌 案例內容 (參照 Section 2)**
文件提供了高層級的協定資訊：
* [cite_start]**網路協定:** 感測器網路 (邊界 A 內部) 基於 **WiFi** 連線 [cite: 114]。
* [cite_start]**存取方式:** 透過服務網路 (網際網路) 進行遠端存取 [cite: 116][cite_start]，或使用 WiFi 進行本地存取 [cite: 116]。
* [cite_start]**應用介面:** SNIP 支援 **Web** 和 **行動介面** [cite: 122]。

**💡 智慧家庭網關 (HSG) 開發人員重點提醒**
* **製作您的「SBOM」：** 這裡的「軟體」不只指您寫的程式，更重要的是您使用的「**所有第三方套件**」。您必須建立一份軟體物料清單 (SBOM - Software Bill of Materials)。
* **盤點協定：** 您的 HSG 使用了哪些協定？
    * **硬體層：** UART, JTAG, SPI...
    * **網路層：** WiFi, BLE, Zigbee...
    * **應用層：** HTTP, HTTPS, MQTT, mDNS, UPnP, SSH, FTP...

**🛠️ 網關 (HSG) 工程實作建議**
* **硬體：**
    * 在生產階段，「**必須**」燒斷 (Disable) JTAG/UART 等除錯介面的 FUSE，或設定安全存取 (如使用加密金鑰才能啟用)。
* **軟體 (SBOM)：**
    * 使用工具 (如 `Yocto` build history, `OpenWrt` package lists) 產生完整的 SBOM。
    * 定期使用漏洞掃描工具 (如 `Trivy`, `Nessus`) 掃描您的韌體映像檔 (firmware image)，檢查 SBOM 中是否存在已知的 CVE 漏洞。
* **協定：**
    * **停用不安全的協定：** 預設「**必須**」停用 `telnet`, `ftp` 等明文協定。
    * **加固必要的協定：** `SSH` 應使用金鑰登入而非密碼。`HTTPS` 應使用 TLS 1.2+ 並停用老舊的加密套件 (ciphersuites)。

---

我們已經依序完成了 Table B-1 中 ID 1 (a-f) 的所有子項分析。

我是否可以繼續處理 Table B-1 的第二個條文：「**ID 2: Define the security problem (定義安全問題)**」，也就是 **Section 3**？