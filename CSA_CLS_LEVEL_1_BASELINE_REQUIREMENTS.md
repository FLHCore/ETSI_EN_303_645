CSA_CLS_LEVEL_1_BASELINE_REQUIREMENTS
===

CSA（Cyber Security Agency of Singapore）提出 Cybersecurity Labelling Scheme（CLS）旨在改善物聯網（IoT）設備的網路安全水準。

CLS 基於 ETSI EN 303 645 標準，設計了四個層級（Tier），每個層級要求不同，其中的 Tier 1 基礎安全要求 IOT 設備必須符合基準安全需求，例如防止使用通用預設密碼等等，依據 ETSI EN 303 645 條規文件中的內容，基準安全要求（Baseline Requirements）主要在文件的第 5 節「消費者物聯網的網路安全條款」和第 6 節「消費者物聯網的資料保護條款」中詳細列出 。

以下是該文件目錄中列出的所有基準要求項目 ：

### 5. 消費者物聯網的網路安全條款 (Cyber security provisions for consumer IoT)

**5.0 報告實施情況 (Reporting implementation)**
* **Provision 5.0-1:** 對於本文件中被認為不適用或消費者物聯網設備未滿足的每項建議，**均應**（shall）記錄其理由 。

**5.1 禁止通用預設密碼 (No universal default passwords)**

* **Provision 5.1-1:** ...在出廠預設以外的任何狀態下，所有消費者物聯網設備的密碼**均應**（shall）為每台設備唯一或由使用者定義 。
* **Provision 5.1-2:** ...這些密碼**應**（shall）透過一種機制生成，以降低針對某一類別或類型的消費者物聯網設備進行自動化攻擊的風險 。
* **Provision 5.1-3:** 用於驗證消費者物聯網設備使用者或用於機器對機器驗證的驗證機制**應**（shall）使用最佳實踐的密碼學... 。
* **Provision 5.1-4:** ...消費者物聯網設備**應**（shall）向使用者或管理員提供一種簡單的機制來更改所使用的驗證值 。
* **Provision 5.1-5:** 消費者物聯網設備**應**（shall）具有一種可用機制，使透過網路介面對驗證機制進行的暴力破解攻擊變得不可行... 。

詳細規範說明請參考：[5.1 No universal default passwords](docs/5.1_no_universal_default_passwords.md)

**5.2 實施管理漏洞報告的方法 (Implement a means to manage reports of vulnerabilities)**

* **Provision 5.2-1:** 製造商**應**（shall）公開提供漏洞揭露政策 。此政策**應**（shall）至少包括：
    * 用於報告問題的聯絡資訊 ；以及
    * 初步確認收到漏洞報告的時間表 ；以及
    * 報告問題者將在何時收到狀態更新的時間表，直到報告的問題得到解決 。

詳細規範說明請參考：[5.2 Implement a means to manage reports of vulnerabilities](docs/5.2_vulnerability_management_system_design.md)

**5.3 保持軟體更新 (Keep software updated)**

* **Provision 5.3-2:** 消費者物聯網設備**應**（shall）具有安全的更新機制，除非設備因使用案例而有資源限制，導致無法實施 。
* **Provision 5.3-3:** 更新**應**（shall）讓使用者易於套用 。
* **Provision 5.3-7:** 消費者物聯網設備**應**（shall）使用最佳實踐的密碼學以促進安全的更新機制 。
* **Provision 5.3-8:** 安全更新**應**（shall）及時 。
* **Provision 5.3-10:** ...消費者物聯網設備**應**（shall）透過信任關係驗證每次更新的真實性和完整性 。
* **Provision 5.3-13:** 製造商**應**（shall）以使用者可存取、清晰且透明的方式，發布明確的支援期限 。
* **Provision 5.3-16:** 消費者物聯網設備的型號名稱**應**（shall）清晰可辨，可透過消費者物聯網設備上的標籤或使用者介面識別 。

詳細規範說明請參考：[5.3 Keep software updated](docs/5.3_software_update_system_design_cm5.md)

**5.4 安全儲存敏感的安全參數 (Securely store sensitive security parameters)**

* **Provision 5.4-1:** 儲存在持久性儲存中的敏感安全參數**應**（shall）由消費者物聯網設備安全地儲存 。
* **Provision 5.4-2:** ...**應**（shall）以能抵抗實體、電氣或軟體等竄改的方式實現 。
* **Provision 5.4-3:** **不得**（shall not）在消費者物聯網設備軟體原始碼中使用硬編碼（Hard-coded）的關鍵安全參數 。
* **Provision 5.4-4:** ...**應**（shall）為每台設備唯一，並**應**（shall）透過一種機制產生，以降低針對多類消費者物聯網設備進行自動化攻擊的風險 。

詳細規範說明請參考：[5.4 Securely store sensitive security parameters](docs/5.4_secure_parameter_storage_design_cm5.md)

**5.5 安全通訊 (Communicate securely)**

* **Provision 5.5-1:** 消費者物聯網設備**應**（shall）使用最佳實踐的密碼學進行安全通訊 。
* **Provision 5.5-5:** 允許透過網路介面進行安全相關設定變更的消費者物聯網設備功能，**應**（shall）僅在驗證後才能存取 。
* **Provision 5.5-7:** 消費者物聯網設備**應**（shall）保護透過遠端可存取網路介面傳輸的關鍵安全參數的機密性 。
* **Provision 5.5-8:** 製造商**應**（shall）遵循與消費者物聯網設備相關的關鍵安全參數的安全管理流程，並貫穿關鍵安全參數的整個生命週期 。

詳細規範說明請參考：[5.5 Communicate securely](docs/5.5_secure_communication_example.md)

**5.6 最小化暴露的攻擊面 (Minimize exposed attack surfaces)**
* **Provision 5.6-1:** 所有未使用的網路介面和所有透過網路介面可存取的未使用邏輯介面**均應**（shall）被禁用 。

* **Provision 5.6-2:** 在初始化狀態下，消費者物聯網設備的網路介面**應**（shall）最小化未經身分驗證的安全相關資訊揭露 。
* **Provision 5.6-4A:** 偵錯介面**應**（shall）被禁用或透過最佳實踐的驗證或存取控制機制進行保護 。

詳細規範說明請參考：[5.6 Minimize exposed attack surfaces](docs/5.6_minimize_exposed_attack_surfaces_example.md)

**5.7 確保軟體完整性 (Ensure software integrity)**
* （本節中的 Provision 5.7-1 和 5.7-2 均使用 "should"（應該），沒有 "shall"（必須）的規範。）

詳細規範說明請參考：[5.7 Ensure software integrity](docs/5.7_ensure_software_integrity_example.md)

**5.8 確保個人資料安全 (Ensure that personal data is secure)**

* **Provision 5.8-2:** 在消費者物聯網設備和關聯服務之間傳輸的敏感個人資料的機密性**應**（shall）使用最佳實踐的密碼學加以保護... 。
* **Provision 5.8-3:** 消費者物聯網設備的所有外部感測功能**應**（shall）以使用者可存取、清晰且透明的方式加以記錄 。

詳細規範說明請參考：[5.8 Ensure that personal data is secure](docs/5.8_ensure_personal_data_is_secure_design.md)

**5.9 使系統能夠彈性應對服務中斷 (Make systems resilient to outages)**

* （本節中的 Provision 5.9-1 至 5.9-3 均使用 "should"（應該），沒有 "shall"（必須）的規範。）

詳細規範說明請參考：[5.9 Make systems resilient to outages](docs/5.9_make_systems_resilient_to_outages_example.md)

**5.10 檢查系統遙測資料 (Examine system telemetry data)**

* （本節中的 Provision 5.10-1 使用 "should"（應該），沒有 "shall"（必須）的規範。）

詳細規範說明請參考：[5.10 Examine system telemetry data](docs/5.10_examine_system_telemetry_data_example.md)

**5.11 讓使用者能輕鬆刪除使用者資料 (Make it easy for users to delete user data)**

* **Provision 5.11-1:** **應**（shall）向使用者提供功能，使其能夠以簡單的方式從消費者物聯網設備中清除所有使用者資料 。

詳細規範說明請參考：[5.11 Make it easy for users to delete user data](docs/5.11_make_it_easy_for_users_to_delete_user_data_example.md)

**5.12 讓設備的安裝和維護變得簡單 (Make installation and maintenance of devices easy)**

* （本節中的 Provision 5.12-1 至 5.12-3 均使用 "should"（應該），沒有 "shall"（必須）的規範。）

**5.13 驗證輸入資料 (Validate input data)**
詳細規範說明請參考：[5.13 Validate input data](docs/5.13_validate_input_data_example.md)

* **Provision 5.13-1A:** 透過使用者介面輸入到設備應用層的資料**應**（shall）由設備驗證，以防止意外的資料輸入導致系統被操縱和發生故障 。
* **Provision 5.13-1B:** 透過網路介面輸入到設備應用層的資料**應**（shall）由設備驗證，以防止意外的資料輸入導致系統被操縱和發生故障 。

詳細規範說明請參考：[5.12 Make installation and maintenance of devices easy](docs/5.12_make_installation_and_maintenance_easy_example.md)

---

### 6. 消費者物聯網的資料保護條款 (Data protection provisions for consumer IoT)

* **Provision 6-1:** 製造商**應**（shall）向消費者提供清晰透明的資訊，說明每個消費者物聯網設備和關聯服務處理哪些個人資料、出於何種目的、由誰處理以及處理多長時間 。
* **Provision 6-2:** 如果將基於消費者的同意來處理個人資料，消費者物聯網設備**應**（shall）提供一種以有效方式獲取此同意的方法 。
* **Provision 6-3A:** 如果將基於消費者的同意來處理個人資料，消費者物聯網設備**應**（shall）提供一種隨時撤回此同意的方法 。
* **Provision 6-3B:** 如果將基於消費者的同意來處理個人資料，消費者物聯網設備**應**（shall）提供一種儲存有關此同意資訊的方法 。
* **Provision 6-5:** 如果從消費者物聯網產品收集遙測資料，**應**（shall）向消費者提供有關收集了哪些遙測資料、如何使用、由誰使用以及出於何種目的的資訊 。
* **Provision 6-6:** 在消費者物聯網設備上儲存和處理的資料，或由消費者物聯網設備提供給關聯服務的資料...**應**（shall）僅限於為其收集或處理目的所必需的資料，並且一旦不再需要用於任何已識別的目的，則**應**（shall）將其刪除 。

詳細規範說明請參考：[6 Data protection provisions for consumer IoT](docs/6_data_protection_provisions_example.md)

---

ETSI EN 303 645 文件翻譯導讀 [cyber_security_for_consumer_internet_of_things_baseline_requirements](docs/0_cyber_security_for_consumer_internet_of_things_baseline_requirements.md)
