沒問題，這是針對 PDF 文件 **封面、目錄說明與法律聲明（第 1 至 4 頁）** 的重新輸出，已將英文原文與中文翻譯分段對照展示：

**IMDA INFOCOMM MEDIA DEVELOPMENT AUTHORITY**


IMDA 資訊通信媒體發展局

**Internet of Things (IoT) Cyber Security Guide Annex B**


物聯網 (IoT) 網絡安全指南 附錄 B

**Case Study on Home Control System**


家庭控制系統案例研究

**IoT Cyber Security Guide Annex B Version 1, Jan 2019**


物聯網 (IoT) 網絡安全指南 附錄 B 版本 1，2019 年 1 月

**Info-communications Media Development Authority**
**10 Pasir Panjang Road**
**#03-01 Mapletree Business City**
**Singapore 117438**


資訊通信媒體發展局
10 Pasir Panjang Road
#03-01 Mapletree Business City
Singapore 117438

**Copyright of IMDA, 2019**
**This document may be downloaded from the IMDA website at [http://www.imda.gov.sg](http://www.imda.gov.sg) and shall not be distributed without written permission from IMDA**


IMDA 版權所有，2019 年
本文件可從 IMDA 網站 [http://www.imda.gov.sg](http://www.imda.gov.sg) 下載，未經 IMDA 書面許可，不得分發。

***

**IMDA IoT Cyber Security Guide Annex B V1 (Feb 2019)**
**Content**


IMDA IoT 網絡安全指南 附錄 B V1（2019 年 2 月）
目錄

**The following table:**
**"Section (§) Case Study on Home Control System Page"**
**1. Overview 3**
**2. Identify the Target of Protection 4**
**3. Define the security problem 6**
**4. Conduct risk assessment 7**
**5. Determine the security objectives 9**
**6. Define the security requirements 10**


下表：
「章節 (§) 家庭控制系統案例研究 頁碼」
1. 概述 3
2. 識別保護目標 4
3. 定義安全問題 6
4. 進行風險評估 7
5. 確定安全目標 9
6. 定義安全需求 10

**This Guide is a living document which is subject to review and revision periodically.**


本指南是一份活文件，將定期進行審查和修訂。

**Guides are informative documents and voluntary in nature except when it is made mandatory by a regulatory authority.**


指南屬於參考性文件，本質上是自願性的，除非監管機構強制規定。

**It can also be reference in contracts as mandatory requirements.**


它也可以在合約中被引用為強制性要求。

**Users are advised to assess the suitability of this guide for their intended use.**


建議用戶評估本指南是否適合其預期用途。

**Compliance with this guide does not exempt users from any legal obligations.**


遵守本指南並不免除用戶的任何法律義務。

***

**NOTICE**


聲明

**THE INFO-COMMUNICATIONS MEDIA DEVELOPMENT AUTHORITY ("IMDA") MAKES NO WARRANTY OF ANY KIND WITH REGARD TO THE MATERIAL PROVIDED HEREIN AND EXCLUDES ANY EXPRESS OR IMPLIED WARRANTIES OR CONDITIONS OF NON-INFRINGEMENT, MERCHANTABILITY, SATISFACTORY QUALITY AND FITNESS FOR A PARTICULAR PURPOSE.**


資訊通信媒體發展局（「IMDA」）對此處提供的材料不作任何形式的保證，並排除任何明示或暗示的保證或條件，包括不侵權、適銷性、令人滿意的品質以及特定用途的適用性。

**SUBJECT TO THE MAXIMUM EXTENT PERMITTED UNDER LAW. IMDA SHALL NOT BE LIABLE FOR ANY ERRORS AND/OR OMISSIONS CONTAINED HEREIN OR FOR ANY LOSSES OR DAMAGES (INCLUDING ANY LOSS OF PROFITS, BUSINESS, GOODWILL OR REPUTATION, AND/OR ANY SPECIAL, INCIDENTAL OR CONSEQUENTIAL DAMAGES) IN CONNECTION WITH THE USE OF THIS MATERIAL.**


在法律允許的最大範圍內。IMDA 不對此處包含的任何錯誤和/或遺漏負責，也不對因使用本材料而引起的任何損失或損害（包括任何利潤、業務、商譽或聲譽的損失，和/或任何特殊的、附帶的或後果性的損害）負責。

**IMDA DRAWS ATTENTION TO THE POSSIBILITY THAT THE PRACTICE OR IMPLEMENTATION OF THIS GUIDE MAY INVOLVE THE USE OF INTELLECTUAL PROPERTY RIGHTS AND TAKES NO POSITION CONCERNING THE EXISTENCE, VALIDITY AND/OR APPLICABILITY OF ANY SUCH INTELLECTUAL PROPERTY RIGHTS, WHETHER ASSERTED BY CONTRIBUTORS OF THIS DOCUMENT OR ANY THIRD PARTY.**


IMDA 提請注意，本指南的實踐或實施可能涉及知識產權的使用，並且對於任何此類知識產權的存在、有效性和/或適用性不持任何立場，無論是由本文件的貢獻者還是任何第三方主張。

**AS OF THE DATE OF THE ISSUANCE OF THE PUBLIC CONSULTATION OF THIS GUIDE, IMDA HAS NOT RECEIVED WRITTEN NOTICE OF ANY PATENT RIGHTS WHICH MAY BE RELEVANT IN RELATION TO THE IMPLEMENTATION OF THIS GUIDE.**


截至本指南公開諮詢發布之日，IMDA 尚未收到任何可能與本指南實施相關的專利權書面通知。

**HOWEVER, IMPLEMENTERS ARE CAUTIONED THAT THIS MAY NOT REPRESENT THE LATEST INFORMATION AND ARE THEREFORE STRONGLY URGED TO CHECK WITH THE RELEVANT DATABASE IN ITU, ISO, IEC OR THE RELATED STANDARDS DEVELOPMENT ORGANISATION FOR INFORMATION OF PATENT RIGHTS.**


然而，實施者應注意，這可能不代表最新資訊，因此強烈建議向國際電信聯盟 (ITU)、國際標準化組織 (ISO)、國際電工委員會 (IEC) 或相關標準制定組織的相關數據庫查詢專利權資訊。

**IMPLEMENTERS ARE ADVISED TO OBTAIN THEIR OWN LEGAL AND/OR TECHNICAL ADVICE IN RELATION TO THE IMPLEMENTATION OF THE GUIDE IF REQUIRED.**


如有需要，建議實施者就本指南的實施尋求自己的法律和/或技術建議。

***

這是第 1 至 4 頁的內容。請問您是否已理解？若確認無誤，我將繼續處理 **第 1 章：概述 (Overview)**。

好的，接下來處理 **第 1 章：概述 (Overview)** 以及 **表 B-1 (Table B-1)** 的內容。這部分涵蓋了第 5 頁至第 6 頁的上半部分。

***

**Annex B: Case Study on Home Control System (informative)**
**1 Overview**


附錄 B：家庭控制系統案例研究（參考性）
1 概述 

**This annex introduces a case study on Home Control System (HCS) and demonstrates the application of the recommendations in the main document to this case study.**


本附錄介紹了一個關於家庭控制系統 (HCS) 的案例研究，並展示了主文件中的建議如何應用於此案例研究。

**This case study is not meant to be exhaustive and the sample application is not definitive of HCS, but for illustrative purposes only.**


本案例研究並非詳盡無遺，範例應用程式也非 HCS 的權威定義，僅供說明之用。

**Table B-1 depicts the threat modelling checklist, defined in the main document, and its application to the case study on HCS.**


表 B-1 描述了主文件中定義的威脅建模檢查表，及其在 HCS 案例研究中的應用。

**Table B-1: Application of threat modelling checklist**
**The following table:**


表 B-1：威脅建模檢查表的應用 
下表：

**ID: 1**
**Threat modelling checklist: Identify the potential targets to be protected**
**a. Define its boundaries and the external systems (including users) that it needs to interact with**
**b. Decompose the target(s) into its subcomponents**
**c. Identify data flows within the target(s), and inputs and outputs from external systems**
**d. Identify sensitive data and where they are handled (at rest, in transit, in use)**
**e. Identify the security needs (based on potential impacts to Confidentiality, Integrity and Availability (CIA) triad) for subcomponents and data flows**
**f. Identify hardware, software and protocols in use**
**Y/N: Y**
**Please elaborate: Refer to section 2**


ID: 1
威脅建模檢查表：識別需要保護的潛在目標
a. 定義其邊界及需要互動的外部系統（包括用戶）
b. 將目標分解為子組件
c. 識別目標內的數據流，以及來自外部系統的輸入和輸出
d. 識別敏感數據及其處理位置（靜態、傳輸中、使用中）
e. 針對子組件和數據流識別安全需求（基於對機密性、完整性和可用性 (CIA) 三要素的潛在影響）
f. 識別使用中的硬體、軟體和協定
是/否：是
請詳述：參見第 2 節 

**ID: 2**
**Threat modelling checklist: Define the security problem**
**a. Identify system accessibility**
**Identify attack surfaces**
**Determine operating environments**
**Determine system / device lifecycles and supply chain**
**b. Identify system susceptibility (aka vulnerabilities)**
**Determine known vulnerabilities**
**Enumerate threats to attack surfaces (using Spoofing, Tampering, Repudiation, Information disclosure, Denial of service, and Elevation of privilege (STRIDE) as a guide)**
**Enumerate threats to operating environments (using STRIDE as a guide)**
**Enumerate threats to stages of system / device lifecycles and supply chain (using STRIDE as a guide)**
**c. State any assumptions**
**Y/N: Y**
**Please elaborate: Refer to section 3**


ID: 2
威脅建模檢查表：定義安全問題
a. 識別系統可訪問性
識別攻擊面
確定操作環境
確定系統/設備生命週期和供應鏈
b. 識別系統敏感性（即漏洞）
確定已知漏洞
列舉對攻擊面的威脅（使用欺騙、篡改、否認、資訊洩露、拒絕服務和特權提升 (STRIDE) 作為指南）
列舉對操作環境的威脅（使用 STRIDE 作為指南）
列舉對系統/設備生命週期各階段和供應鏈的威脅（使用 STRIDE 作為指南）
c. 說明任何假設
是/否：是
請詳述：參見第 3 節 

**ID: 3**
**Threat modelling checklist: Conduct risk assessment**
**Assess impact of threats and vulnerabilities to CIA triad and match against security needs of assets**
**Assess attacker capabilities required to realise the threats**
**Assess the likelihood of the risk**
**Prioritise the risks for mitigation, including other considerations (e.g. monetary impact)**
**Y/N: Y**
**Please elaborate: Refer to section 4**


ID: 3
威脅建模檢查表：進行風險評估
評估威脅和漏洞對 CIA 三要素的影響，並與資產的安全需求進行匹配
評估實現威脅所需的攻擊者能力
評估風險的可能性
優先考慮風險以進行緩解，包括其他考量因素（例如金錢影響）
是/否：是
請詳述：參見第 4 節 

**ID: 4**
**Threat modelling checklist: Determine the security objectives**
**State the security objectives. For example, OT systems emphasize safety, where system integrity takes precedence over data confidentiality**
**Y/N: Y**
**Please elaborate: Refer to section 5**


ID: 4
威脅建模檢查表：確定安全目標
說明安全目標。例如，OT 系統強調安全性，其中系統完整性優先於數據機密性
是/否：是
請詳述：參見第 5 節 

**ID: 5**
**Threat modelling checklist: Define the security requirements**
**State the necessary requirements to address the identified security objectives without going into their specific implementation**
**Y/N: Y**
**Please elaborate: Refer to section 6**


ID: 5
威脅建模檢查表：定義安全需求
說明解決已識別安全目標所需的必要需求，而不涉及其具體實施
是/否：是
請詳述：參見第 6 節 

**ID: 6**
**Threat modelling checklist: Design and implement the capabilities**
**Y/N: N**
**Please elaborate: Not covered by this document**


ID: 6
威脅建模檢查表：設計並實施功能
是/否：否
請詳述：本文件未涵蓋 

**ID: 7**
**Threat modelling checklist: Validate and verify that the capabilities address the security requirements adequately**
**Y/N: N**
**Please elaborate: Not covered by this document**


ID: 7
威脅建模檢查表：驗證並核實功能是否充分解決了安全需求
是/否：否
請詳述：本文件未涵蓋 

***

這是 **第 1 章：概述** 的內容。請問您是否已理解？若確認無誤，我將繼續處理 **第 2 章：識別保護目標 (Identify the Target of Protection)**。

好的，接下來處理 **第 2 章：識別保護目標 (Identify the Target of Protection)**，內容涵蓋圖表 B-1 的架構描述以及表 B-2 和表 B-3 的資產與數據流分析。

***

**2 Identify the Target of Protection**


2 識別保護目標

**This section illustrates the guidance provided by item-1 of the threat modelling checklist, which helps to identify the Target Of Protection (TOP) for the case study on HCS.**


本節說明威脅建模檢查表第 1 項提供的指導，該指導有助於識別 HCS 案例研究的保護目標 (TOP)。

**Figure B-1 is the system architecture of the defined case study, which demonstrates the guidance provided by the threat modelling checklist.**


圖 B-1 是所定義案例研究的系統架構，展示了威脅建模檢查表提供的指導。

**Figure B-1: System architecture of HCS**
*(Note: Textual representation of the diagram components)*
**Application Layer:** Backend system, Web application, Mobile application
**Service Support Layer:** Sensor network integration platform (SNIP) [Boundary B]
**Network Layer (service):** Service network
**Network Layer (access):** Access network
**Device Layer (gateway):** Home sensor gateway (HSG) [Boundary A starts]
**Network Layer (constrained):** Sensor network
**Device Layer (end node):** Smart socket (Lights, Kettle), Aircon, TV, Washing machine, Smoke detector, Door control


圖 B-1：HCS 的系統架構
*（註：圖表組件的文字表示）*
**應用層：** 後端系統、網頁應用程式、行動應用程式
**服務支援層：** 感測器網絡整合平台 (SNIP) [邊界 B]
**網絡層（服務）：** 服務網絡
**網絡層（接入）：** 接入網絡
**設備層（網關）：** 家庭感測器網關 (HSG) [邊界 A 開始]
**網絡層（受限）：** 感測器網絡
**設備層（終端節點）：** 智慧插座（電燈、水壺）、冷氣機、電視、洗衣機、煙霧探測器、門控裝置

**Two system boundaries for the case study on HCS are defined.**


為 HCS 案例研究定義了兩個系統邊界。

**Boundary A is defined to cover all the subcomponents within the home setting, while Boundary B is defined to contain the Sensor Network Integration Platform (SNIP) hosted on a cloud infrastructure.**


邊界 A 定義為涵蓋家庭環境內的所有子組件，而邊界 B 定義為包含託管在雲端基礎設施上的感測器網絡整合平台 (SNIP)。

**Within boundary A, it is defined that the sensor network is based on WiFi connectivity and Home Sensor Gateway (HSG) mediate between devices on sensor network and SNIP on access network.**


在邊界 A 內，定義感測器網絡基於 WiFi 連接，且家庭感測器網關 (HSG) 在感測器網絡上的設備與接入網絡上的 SNIP 之間進行協調。

**HSG can potentially host sensitive data. HSG aggregates sensing data from the connected devices and can also send commands to devices where control is permissible.**


HSG 可能託管敏感數據。HSG 聚合來自連接設備的感測數據，也可以向允許控制的設備發送指令。

**HSG allows authorised users to access and issue commands for its connected devices, both remotely over the service network (internet or dedicated network) and locally within the home (e.g. using WiFi connectivity).**


HSG 允許授權用戶存取其連接的設備並發出指令，既可以透過服務網絡（網際網路或專用網絡）遠端進行，也可以在家庭內部本地進行（例如使用 WiFi 連接）。

**HSG can also operate in local mode, where access network is not available.**


HSG 也可以在本地模式下運作，此時接入網絡不可用。

**The devices (lights and kettle) connected to the smart socket are not smart devices.**


連接到智慧插座的設備（電燈和水壺）不是智慧設備。

**Lights are enabled for control through a pairing mechanism with the smart socket. We defined kettle as not control permissible.**


電燈透過與智慧插座的配對機制啟用控制。我們將水壺定義為不允許控制。

**SNIP is a digital platform that aggregates sensing data from multiple gateways of multiple homes and probably host sensitive data.**


SNIP 是一個數位平台，聚合來自多個家庭的多個網關的感測數據，並可能託管敏感數據。

**It is connected to the enterprise backend system and may export data in bulk for various purposes, for example, archival.**


它連接到企業後端系統，並可能出於各種目的（例如存檔）批量匯出數據。

**The SNIP supports both web and mobile interfaces for operation and administration purposes.**


SNIP 支援網頁和行動介面，用於操作和管理目的。

**Table B-2 determines the security needs of the assets, with respect to CIA triad.**


表 B-2 確定了資產在 CIA 三要素方面的安全需求。

**It helps in prioritising which assets and which aspects to secure.**


它有助於優先考慮需要保護的資產和方面。

**Table B-2: Security needs of assets**
**Legend: H = high, M = moderate, L = low**


表 B-2：資產的安全需求
圖例：H = 高，M = 中，L = 低

**(Row 1)**
**Assets: Sensor network integration platform (SNIP)**
**Confidentiality: H**
**Integrity: H**
**Availability: H**
**Rationale: Confidentiality is high as SNIP contains sensitive data. Integrity is high to safeguard commands invocation. Availability is important because of the need to support many users.**


（第 1 列）
資產：感測器網絡整合平台 (SNIP)
機密性：H
完整性：H
可用性：H
理由：機密性為高，因為 SNIP 包含敏感數據。完整性為高，以保護指令調用。可用性很重要，因為需要支援許多用戶。

**(Row 2)**
**Assets: Home sensor gateway (HSG)**
**Confidentiality: H**
**Integrity: H**
**Availability: M**
**Rationale: Confidentiality and integrity is the same as SNIP. Availability is moderate as only one household is impacted.**


（第 2 列）
資產：家庭感測器網關 (HSG)
機密性：H
完整性：H
可用性：M
理由：機密性和完整性與 SNIP 相同。可用性為中等，因為僅影響一個家庭。

**(Row 3)**
**Assets: Device: Aircon**
**Confidentiality: L**
**Integrity: M**
**Availability: L**
**Rationale: Integrity is relatively more important because of monetary impact when aircon is on instead of off.**


（第 3 列）
資產：設備：冷氣機
機密性：L
完整性：M
可用性：L
理由：完整性相對更重要，因為當冷氣機應關閉卻開啟時會有金錢影響。

**(Row 4)**
**Assets: Device: TV**
**Confidentiality: M**
**Integrity: H**
**Availability: L**
**Rationale: Integrity is high because compromised TV can participate in DDoS. Confidentiality is moderate because disclosure of watching habits can impact privacy.**


（第 4 列）
資產：設備：電視
機密性：M
完整性：H
可用性：L
理由：完整性為高，因為受損的電視可能參與 DDoS 攻擊。機密性為中等，因為觀看習慣的洩露可能影響隱私。

**(Row 5)**
**Assets: Device: Washing machine**
**Confidentiality: L**
**Integrity: L**
**Availability: L**


（第 5 列）
資產：設備：洗衣機
機密性：L
完整性：L
可用性：L

**(Row 6)**
**Assets: Device: Smoke detector**
**Confidentiality: L**
**Integrity: H**
**Availability: M**
**Rationale: Integrity is high, in order to gain first responder's trust in the system.**


（第 6 列）
資產：設備：煙霧探測器
機密性：L
完整性：H
可用性：M
理由：完整性為高，以獲得急救人員對系統的信任。

**(Row 7)**
**Assets: Device: Door control**
**Confidentiality: M**
**Integrity: H**
**Availability: H**
**Rationale: Integrity and availability is very important for the proper operation for this device. Since this device does not contains sensitive data, confidentiality is moderate as we still want to keep activity information private as far as possible.**


（第 7 列）
資產：設備：門控裝置
機密性：M
完整性：H
可用性：H
理由：完整性和可用性對於此設備的正常運作非常重要。由於此設備不包含敏感數據，機密性為中等，因為我們仍希望儘可能保密活動資訊。

**(Row 8)**
**Assets: Device: Smart socket**
**Confidentiality: L**
**Integrity: H**
**Availability: M**
**Rationale: Integrity is high for safety considerations. Additional restriction might apply. For example, when kettle is connected, remote access is disallowed.**


（第 8 列）
資產：設備：智慧插座
機密性：L
完整性：H
可用性：M
理由：出於安全考量，完整性為高。可能適用額外的限制。例如，當連接水壺時，不允許遠端存取。

**(Row 9)**
**Assets: Device: Lights**
**Confidentiality: L**
**Integrity: M**
**Availability: M**
**Rationale: Integrity and availability is moderate as importance of lighting is contextual. For example, use of lights at night time.**


（第 9 列）
資產：設備：電燈
機密性：L
完整性：M
可用性：M
理由：完整性和可用性為中等，因為照明的重要性取決於情境。例如，夜間使用燈光。

**(Row 10)**
**Assets: Device: Kettle**
**Confidentiality: L**
**Integrity: H**
**Availability: L**
**Rationale: Integrity is high for safety considerations.**


（第 10 列）
資產：設備：水壺
機密性：L
完整性：H
可用性：L
理由：出於安全考量，完整性為高。

**Table B-3 determines the security needs of the data flows between assets, with respect to CIA triad.**


表 B-3 確定了資產之間數據流在 CIA 三要素方面的安全需求。

**It provides information on which data flows required attention and the type of security required.**


它提供了有關哪些數據流需要關注以及所需安全類型的資訊。

**Table B-3: Security needs of data flows**
**Legend: H = high, M = moderate, L = low**


表 B-3：數據流的安全需求
圖例：H = 高，M = 中，L = 低

**(Row 1)**
**Data flows: Devices → HSG**
**Confidentiality: M**
**Integrity: H**
**Availability: H**
**Rationale: The impact to CIA triad for this data flow is determined using high watermark method on the security needs of devices on the same sensor network.**


（第 1 列）
數據流：設備 → HSG
機密性：M
完整性：H
可用性：H
理由：此數據流對 CIA 三要素的影響是使用高水位線法（high watermark method），根據同一感測器網絡上設備的安全需求確定的。

**(Row 2)**
**Data flows: HSG ↔ SNIP**
**Confidentiality: H**
**Integrity: H**
**Availability: H**
**Rationale: The impact to CIA triad for this data flow is determined using high watermark method on the security needs of SNIP and HSG.**


（第 2 列）
數據流：HSG ↔ SNIP
機密性：H
完整性：H
可用性：H
理由：此數據流對 CIA 三要素的影響是使用高水位線法，根據 SNIP 和 HSG 的安全需求確定的。

**(Row 3)**
**Data flows: SNIP → Backend system**
**Confidentiality: H**
**Integrity: H**
**Availability: L**
**Rationale: SNIP exports data for backup at backend system. Safeguarding the confidentiality and integrity of exported data is more important, relative to availability.**


（第 3 列）
數據流：SNIP → 後端系統
機密性：H
完整性：H
可用性：L
理由：SNIP 匯出數據以在後端系統備份。相對於可用性，保護匯出數據的機密性和完整性更為重要。

**(Row 4)**
**Data flows: Web application ↔ SNIP → HSG → Devices**
**Confidentiality: H**
**Integrity: H**
**Availability: H**
**Rationale: Administration of SNIP and devices requires high confidentiality and integrity. Alerts requires high availability.**


（第 4 列）
數據流：網頁應用程式 ↔ SNIP → HSG → 設備
機密性：H
完整性：H
可用性：H
理由：SNIP 和設備的管理需要高度的機密性和完整性。警報需要高可用性。

**(Row 5)**
**Data flows: Mobile application ↔ SNIP → HSG → Device**
**Confidentiality: H**
**Integrity: H**
**Availability: H**
**Rationale: Remote access to devices, through SNIP requires high confidentiality and integrity. Alerts requires high availability.**


（第 5 列）
數據流：行動應用程式 ↔ SNIP → HSG → 設備
機密性：H
完整性：H
可用性：H
理由：透過 SNIP 遠端存取設備需要高度的機密性和完整性。警報需要高可用性。

**(Row 6)**
**Data flows: Mobile application ↔ HSG → Devices**
**Confidentiality: M**
**Integrity: H**
**Availability: M**
**Rationale: Local access to devices, through HSG requires high integrity for safety considerations. Confidentiality is moderate as this data flow is transactional and not sensitive. Alerts requires moderate availability.**


（第 6 列）
數據流：行動應用程式 ↔ HSG → 設備
機密性：M
完整性：H
可用性：M
理由：出於安全考量，透過 HSG 本地存取設備需要高完整性。機密性為中等，因為此數據流屬於交易性質且不敏感。警報需要中等可用性。

***

這是 **第 2 章：識別保護目標** 的內容。請問您是否已理解？若確認無誤，我將繼續處理 **第 3 章：定義安全問題 (Define the security problem)**。

好的，接下來處理 **第 3 章：定義安全問題 (Define the security problem)** 以及 **表 B-4 (Table B-4)** 的內容。這部分涵蓋了第 6 頁的內容。

***

**3 Define the security problem**


3 定義安全問題

**This section illustrates the guidance provided by item-2 of the threat modelling checklist, which helps to define the security problem for the case study on HCS.**


本節說明威脅建模檢查表第 2 項提供的指導，該指導有助於定義 HCS 案例研究的安全問題。

**Table B-4 identifies the concerns that contribute to system accessibility and system susceptibility for assets under TOP.**


表 B-4 識別了導致保護目標 (TOP) 下資產的系統可訪問性和系統敏感性的關注點。

**It provides the information (threats, vulnerabilities, operating environments, assumptions, etc.) required to define the security problem.**


它提供了定義安全問題所需的資訊（威脅、漏洞、操作環境、假設等）。

**Table B-4: System accessibility and susceptibility**
*(Note: Textual representation of the table content)*


表 B-4：系統可訪問性和敏感性
*（註：表格內容的文字表示）*

**(Row 1)**
**Assets: Sensor network integration platform (SNIP)**
**System accessibility (attack surfaces, operating environments, lifecycles):**
The following attack surfaces are relevant for SNIP: bulk API, web API, mobile API, HTTP/IP, storage SW & HW, memory, VM, OS, firmware, server software.
The SNIP is assumed to be hosted in the cloud and accessible from the internet.
All stages of system lifecycle needs to be considered.
**System susceptibility (known vulnerabilities, STRIDE):**
Refer to "OWASP Top 10 Application Security Risks".
Scan for relevant known vulnerabilities from prominent vulnerability repositories. Eg. [https://cve.mitre.org](https://cve.mitre.org)


（第 1 列）
資產：感測器網絡整合平台 (SNIP)
系統可訪問性（攻擊面、操作環境、生命週期）：
以下攻擊面與 SNIP 相關：批量 API、網頁 API、行動 API、HTTP/IP、儲存軟硬體、記憶體、虛擬機 (VM)、作業系統 (OS)、韌體、伺服器軟體。
假設 SNIP 託管在雲端並可從網際網路存取。
需要考慮系統生命週期的所有階段。
系統敏感性（已知漏洞、STRIDE）：
請參閱「OWASP 十大應用程式安全風險」。
從知名的漏洞資料庫掃描相關的已知漏洞。例如：[https://cve.mitre.org](https://cve.mitre.org)

**(Row 2)**
**Assets: Home sensor gateway (HSG)**
**System accessibility:**
The following attack surfaces are relevant for HSG: management API, mobile API, HTTP/IP, WIFI, storage SW & HW, memory, VM, OS, firmware, middleware, communication ports, device ID.
WIFI connectivity is assumed.
The HSG is assumed to operate in the home setting and accessible from the internet.
All stages of device lifecycle needs to be considered.
**System susceptibility:**
Refer to "OWASP IoT Attack Surface Areas" and "OWASP IoT Vulnerabilities".
Scan for relevant known vulnerabilities from prominent vulnerability repositories. Eg. [https://cve.mitre.org](https://cve.mitre.org)


（第 2 列）
資產：家庭感測器網關 (HSG)
系統可訪問性：
以下攻擊面與 HSG 相關：管理 API、行動 API、HTTP/IP、WIFI、儲存軟硬體、記憶體、虛擬機 (VM)、作業系統 (OS)、韌體、中介軟體、通訊埠、設備 ID。
假設使用 WIFI 連接。
假設 HSG 在家庭環境中運作並可從網際網路存取。
需要考慮設備生命週期的所有階段。
系統敏感性：
請參閱「OWASP IoT 攻擊面區域」和「OWASP IoT 漏洞」。
從知名的漏洞資料庫掃描相關的已知漏洞。例如：[https://cve.mitre.org](https://cve.mitre.org)

**(Row 3)**
**Assets: Device: Aircon**
**System accessibility:**
The following attack surfaces are relevant for Aircon: API for sensing/actuating, WiFi, firmware, device ID. WIFI connectivity is assumed.
The Aircon is assumed to operate in the home setting and accessible from HSG only.
All stages of device lifecycle needs to be considered.
**System susceptibility:**
Refer to "OWASP IoT Vulnerabilities".
Scan for relevant known vulnerabilities from prominent vulnerability repositories. Eg. [https://cve.mitre.org](https://cve.mitre.org)


（第 3 列）
資產：設備：冷氣機
系統可訪問性：
以下攻擊面與冷氣機相關：用於感測/致動的 API、WiFi、韌體、設備 ID。假設使用 WIFI 連接。
假設冷氣機在家庭環境中運作，且僅可透過 HSG 存取。
需要考慮設備生命週期的所有階段。
系統敏感性：
請參閱「OWASP IoT 漏洞」。
從知名的漏洞資料庫掃描相關的已知漏洞。例如：[https://cve.mitre.org](https://cve.mitre.org)

**(Row 4)**
**Assets: Device: TV**
**System accessibility / Susceptibility:**
Similar concerns as HSG.
(Note: Often involves web applications, increasing attack surfaces. Operates in home setting with risk of physical access.)
Refer to "OWASP Mobile Top 10 Risks".


（第 4 列）
資產：設備：電視
系統可訪問性 / 敏感性：
與 HSG 有類似的關注點。
（註：通常涉及網頁應用程式，增加攻擊面。在家庭環境中運作，有物理存取風險。）
請參閱「OWASP 行動裝置十大風險」。

**(Row 5)**
**Assets: Device: Washing machine**
**System accessibility / Susceptibility:**
Similar concerns as Aircon.


（第 5 列）
資產：設備：洗衣機
系統可訪問性 / 敏感性：
與冷氣機有類似的關注點。

**(Row 6)**
**Assets: Device: Smoke detector**
**System accessibility / Susceptibility:**
Similar concerns as Aircon.


（第 6 列）
資產：設備：煙霧探測器
系統可訪問性 / 敏感性：
與冷氣機有類似的關注點。

**(Row 7)**
**Assets: Device: Door control**
**System accessibility / Susceptibility:**
Similar concerns as Aircon.


（第 7 列）
資產：設備：門控裝置
系統可訪問性 / 敏感性：
與冷氣機有類似的關注點。

**(Row 8)**
**Assets: Device: Smart socket**
**System accessibility / Susceptibility:**
Similar concerns as Aircon.


（第 8 列）
資產：設備：智慧插座
系統可訪問性 / 敏感性：
與冷氣機有類似的關注點。

**(Row 9)**
**Assets: Device: Lights**
**System accessibility:**
The attack surfaces relevant for Lights are device ID as its "smartness" are provided by the smart socket it is connected to.
**System susceptibility:**
Vulnerability to pairing process between lights and smart socket.


（第 9 列）
資產：設備：電燈
系統可訪問性：
與電燈相關的攻擊面是設備 ID，因為其「智慧功能」是由連接的智慧插座提供的。
系統敏感性：
電燈與智慧插座之間配對過程的漏洞。

**(Row 10)**
**Assets: Device: Kettle**
**System accessibility / Susceptibility:**
Similar concerns as Lights.


（第 10 列）
資產：設備：水壺
系統可訪問性 / 敏感性：
與電燈有類似的關注點。

***

這是 **第 3 章：定義安全問題** 的內容。請問您是否已理解？若確認無誤，我將繼續處理 **第 4 章：進行風險評估 (Conduct risk assessment)**。

好的，接下來處理 **第 4 章：進行風險評估 (Conduct risk assessment)** 以及相關的 **表 B-5、B-6 與 B-7** 的內容。這部分涵蓋了第 9 頁至第 10 頁（PDF 頁碼 7 至 8）的內容。

***

**4 Conduct risk assessment** 

4 進行風險評估

**This section illustrates the guidance provided by item-3 of the threat modelling checklist, which guide how risk assessment is conducted for the case study on HCS.** 

本節說明威脅建模檢查表第 3 項提供的指導，該指導指引如何對 HCS 案例研究進行風險評估。

**Table B-5 demonstrates a risk assessment of system accessibility and system susceptibility for each asset.** 

表 B-5 展示了針對每個資產的系統可訪問性和系統敏感性的風險評估。

**It is useful for illustration purposes only, as risks are context-sensitive to the real world.** 

這僅用於說明目的，因為風險在現實世界中取決於具體情境。

**In the table, risks are classified as high, moderate and low, according to the given rationale.** 

在表中，風險根據給定的理由分為高、中和低。

**Table B-5: Assessment of system accessibility and susceptibility**
**Legend: H = high, M = moderate, L = low** 

表 B-5：系統可訪問性和敏感性評估
圖例：H = 高，M = 中，L = 低

**(Row 1)**
**Assets: Sensor network integration platform (SNIP)**
**System accessibility (attack surfaces, operating environments, lifecycles): H**
**System susceptibility (known vulnerabilities, STRIDE): H**
**Rationale: System accessibility of SNIP is high because it is hosted over the internet. System susceptibility is high because there is many known vulnerabilities. Refer to "OWASP Top 10 Application Security Risks".** 

（第 1 列）
資產：感測器網絡整合平台 (SNIP)
系統可訪問性（攻擊面、操作環境、生命週期）：H
系統敏感性（已知漏洞、STRIDE）：H
理由：SNIP 的系統可訪問性為高，因為它託管在網際網路上。系統敏感性為高，因為存在許多已知漏洞。請參閱「OWASP 十大應用程式安全風險」。

**(Row 2)**
**Assets: Home sensor gateway (HSG)**
**System accessibility: H**
**System susceptibility: H**
**Rationale: System accessibility of HSG is determined to be high. HSG is required to support multiple networks and connectivity from diverse devices increasing the attack surfaces. HSG operates in the home setting with risk of physical access. HSG may transfer ownership during its lifecycle. System susceptibility of HSG is determined to be high because there are many known vulnerabilities. Refer to "OWASP IoT Attack Surface Areas" and "OWASP IoT Vulnerabilities".** 

（第 2 列）
資產：家庭感測器網關 (HSG)
系統可訪問性：H
系統敏感性：H
理由：HSG 的系統可訪問性被確定為高。HSG 需要支援多種網絡和來自不同設備的連接，這增加了攻擊面。HSG 在家庭環境中運作，存在物理存取風險。HSG 在其生命週期中可能會轉移所有權。HSG 的系統敏感性被確定為高，因為存在許多已知漏洞。請參閱「OWASP IoT 攻擊面區域」和「OWASP IoT 漏洞」。

**(Row 3)**
**Assets: Device: Aircon**
**System accessibility: M**
**System susceptibility: M**
**Rationale: System accessibility and susceptibility of aircon is determined to be moderate. The assumption is wireless connectivity is used.** 

（第 3 列）
資產：設備：冷氣機
系統可訪問性：M
系統敏感性：M
理由：冷氣機的系統可訪問性和敏感性被確定為中等。假設使用無線連接。

**(Row 4)**
**Assets: Device: TV**
**System accessibility: H**
**System susceptibility: H**
**Rationale: System accessibility and susceptibility of TV is determined to be high. TV hosts web applications which increases its attack surfaces. It operates in home setting with risk of physical access and may transfer ownership during its lifecycle. Refer to "OWASP Mobile Top 10 Risks".** 

（第 4 列）
資產：設備：電視
系統可訪問性：H
系統敏感性：H
理由：電視的系統可訪問性和敏感性被確定為高。電視託管網頁應用程式，這增加了其攻擊面。它在家庭環境中運作，存在物理存取風險，並且可能在其生命週期中轉移所有權。請參閱「OWASP 行動裝置十大風險」。

**(Row 5)**
**Assets: Device: Washing machine**
**System accessibility: M**
**System susceptibility: M**
**Rationale: System accessibility and susceptibility of washing machine is determined to be moderate. The assumption is wireless connectivity is used.** 

（第 5 列）
資產：設備：洗衣機
系統可訪問性：M
系統敏感性：M
理由：洗衣機的系統可訪問性和敏感性被確定為中等。假設使用無線連接。

**(Row 6)**
**Assets: Device: Smoke detector**
**System accessibility: L**
**System susceptibility: L**
**Rationale: System accessibility and susceptibility of smoke detector is determined to be low, when wired connectivity is used.** 

（第 6 列）
資產：設備：煙霧探測器
系統可訪問性：L
系統敏感性：L
理由：當使用有線連接時，煙霧探測器的系統可訪問性和敏感性被確定為低。

**(Row 7)**
**Assets: Device: Door control**
**System accessibility: M**
**System susceptibility: M**
**Rationale: System accessibility and susceptibility of door control is determined to be moderate. The assumption is wireless connectivity is used.** 

（第 7 列）
資產：設備：門控裝置
系統可訪問性：M
系統敏感性：M
理由：門控裝置的系統可訪問性和敏感性被確定為中等。假設使用無線連接。

**(Row 8)**
**Assets: Device: Smart socket**
**System accessibility: M**
**System susceptibility: M**
**Rationale: System accessibility and susceptibility of smart socket is determined to be moderate. The assumption is wireless connectivity is used.** 

（第 8 列）
資產：設備：智慧插座
系統可訪問性：M
系統敏感性：M
理由：智慧插座的系統可訪問性和敏感性被確定為中等。假設使用無線連接。

**(Row 9)**
**Assets: Device: Lights**
**System accessibility: H**
**System susceptibility: M**
**Rationale: System accessibility of light is determined to be high, because it is removable.** 

（第 9 列）
資產：設備：電燈
系統可訪問性：H
系統敏感性：M
理由：電燈的系統可訪問性被確定為高，因為它是可拆卸的。

**(Row 10)**
**Assets: Device: Kettle**
**System accessibility: H**
**System susceptibility: M**
**Rationale: System accessibility of kettle is determined to be high, because it is removable.** 

（第 10 列）
資產：設備：水壺
系統可訪問性：H
系統敏感性：M
理由：水壺的系統可訪問性被確定為高，因為它是可拆卸的。

**Table B-6 demonstrates a risk assessment of attacker capability for each asset.** 

表 B-6 展示了針對每個資產的攻擊者能力的風險評估。

**It determines a list of attacker types (script kiddies, criminals, hacktivist, terrorists, state sponsored, etc) that have interest in the assets.** 

它確定了對資產感興趣的攻擊者類型列表（腳本小子、罪犯、黑客行動主義者、恐怖分子、國家資助者等）。

**The risks are defined by the capability of the most sophisticated attacker in the list, which can compromise the assets.** 

風險是由列表中能破壞資產的最老練攻擊者的能力所定義的。

**Similarly, risks are classified as high, moderate and low, according to the given rationale.** 

同樣地，根據給定的理由，風險分為高、中和低。

**Table B-6: Assessment of attacker capability**
**Legend: H = high, M = moderate, L = low**
**Attacker capability: L: script kiddies; M: criminals, hacktivist; H: terrorists, state sponsored** 

表 B-6：攻擊者能力評估
圖例：H = 高，M = 中，L = 低
攻擊者能力：L：腳本小子；M：罪犯、黑客行動主義者；H：恐怖分子、國家資助者

**(Row 1)**
**Assets: Sensor network integration platform (SNIP)**
**Attacker capability: H**
**Rationale: The asset is valuable to a range of attackers (script kiddies, criminals, hacktivist, terrorists, state sponsored) including some with high capabilities and resources.** 

（第 1 列）
資產：感測器網絡整合平台 (SNIP)
攻擊者能力：H
理由：該資產對各種攻擊者（腳本小子、罪犯、黑客行動主義者、恐怖分子、國家資助者）都有價值，包括一些具有高能力和資源的攻擊者。

**(Row 2)**
**Assets: Home sensor gateway (HSG)**
**Attacker capability: H**
**Rationale: The asset is valuable to a range of attackers (script kiddies, criminals, hacktivist, terrorists, state sponsored), including some with high capabilities and resources.** 

（第 2 列）
資產：家庭感測器網關 (HSG)
攻擊者能力：H
理由：該資產對各種攻擊者（腳本小子、罪犯、黑客行動主義者、恐怖分子、國家資助者）都有價值，包括一些具有高能力和資源的攻擊者。

**(Row 3)**
**Assets: Device: Aircon**
**Attacker capability: L**
**Rationale: The asset is valuable to script kiddies only.** 

（第 3 列）
資產：設備：冷氣機
攻擊者能力：L
理由：該資產僅對腳本小子有價值。

**(Row 4)**
**Assets: Device: TV**
**Attacker capability: M**
**Rationale: The asset is valuable to a range of attackers (script kiddies, criminals, hacktivist) with moderate capabilities and resources.** 

（第 4 列）
資產：設備：電視
攻擊者能力：M
理由：該資產對具有中等能力和資源的各種攻擊者（腳本小子、罪犯、黑客行動主義者）有價值。

**(Row 5)**
**Assets: Device: Washing machine**
**Attacker capability: L**
**Rationale: The asset is valuable to script kiddies only.** 

（第 5 列）
資產：設備：洗衣機
攻擊者能力：L
理由：該資產僅對腳本小子有價值。

**(Row 6)**
**Assets: Device: Smoke detector**
**Attacker capability: M**
**Rationale: The asset is valuable to script kiddies and criminals with moderate capabilities and resources.** 

（第 6 列）
資產：設備：煙霧探測器
攻擊者能力：M
理由：該資產對具有中等能力和資源的腳本小子和罪犯有價值。

**(Row 7)**
**Assets: Device: Door control**
**Attacker capability: M**
**Rationale: The asset is valuable to script kiddies and criminals with moderate capabilities and resources.** 

（第 7 列）
資產：設備：門控裝置
攻擊者能力：M
理由：該資產對具有中等能力和資源的腳本小子和罪犯有價值。

**(Row 8)**
**Assets: Device: Smart socket**
**Attacker capability: M**
**Rationale: The asset is valuable to script kiddies and criminals with moderate capabilities and resources.** 

（第 8 列）
資產：設備：智慧插座
攻擊者能力：M
理由：該資產對具有中等能力和資源的腳本小子和罪犯有價值。

**(Row 9)**
**Assets: Device: Lights**
**Attacker capability: M**
**Rationale: The asset is valuable to criminals with moderate capabilities and resources.** 

（第 9 列）
資產：設備：電燈
攻擊者能力：M
理由：該資產對具有中等能力和資源的罪犯有價值。

**(Row 10)**
**Assets: Device: Kettle**
**Attacker capability: L**
**Rationale: The asset is not valuable to attacker.** 

（第 10 列）
資產：設備：水壺
攻擊者能力：L
理由：該資產對攻擊者沒有價值。

**Table B-7 determines the priority for mitigation of the threats for each asset, with holistic considerations for risks of system accessibility, system susceptibility and attacker capability.** 

表 B-7 確定了每個資產的威脅緩解優先順序，並綜合考慮了系統可訪問性、系統敏感性和攻擊者能力的風險。

**For illustrative purposes, our case study will only elaborate on the high priority items for mitigation in subsequent sections.** 

為便於說明，本案例研究在後續章節中將僅詳細闡述高優先順序的緩解項目。

**Table B-7: Assessment of priority**
**Legend: H = high, M = moderate, L = low** 

表 B-7：優先順序評估
圖例：H = 高，M = 中，L = 低

**(Row 1)**
**Assets: Sensor network integration platform (SNIP)**
**System accessibility: H**
**System susceptibility: H**
**Attacker capability: H**
**Priority: H** 

（第 1 列）
資產：感測器網絡整合平台 (SNIP)
系統可訪問性：H
系統敏感性：H
攻擊者能力：H
優先順序：H

**(Row 2)**
**Assets: Home sensor gateway (HSG)**
**System accessibility: H**
**System susceptibility: H**
**Attacker capability: H**
**Priority: H** 

（第 2 列）
資產：家庭感測器網關 (HSG)
系統可訪問性：H
系統敏感性：H
攻擊者能力：H
優先順序：H

**(Row 3)**
**Assets: Device: Aircon**
**System accessibility: M**
**System susceptibility: M**
**Attacker capability: L**
**Priority: (Blank)** 

（第 3 列）
資產：設備：冷氣機
系統可訪問性：M
系統敏感性：M
攻擊者能力：L
優先順序：（空白）

**(Row 4)**
**Assets: Device: TV**
**System accessibility: H**
**System susceptibility: H**
**Attacker capability: M**
**Priority: H** 

（第 4 列）
資產：設備：電視
系統可訪問性：H
系統敏感性：H
攻擊者能力：M
優先順序：H

**(Row 5)**
**Assets: Device: Washing machine**
**System accessibility: M**
**System susceptibility: M**
**Attacker capability: L**
**Priority: (Blank)** 

（第 5 列）
資產：設備：洗衣機
系統可訪問性：M
系統敏感性：M
攻擊者能力：L
優先順序：（空白）

**(Row 6)**
**Assets: Device: Smoke detector**
**System accessibility: L**
**System susceptibility: L**
**Attacker capability: M**
**Priority: (Blank)** 

（第 6 列）
資產：設備：煙霧探測器
系統可訪問性：L
系統敏感性：L
攻擊者能力：M
優先順序：（空白）

**(Row 7)**
**Assets: Device: Door control**
**System accessibility: M**
**System susceptibility: M**
**Attacker capability: M**
**Priority: H** 

（第 7 列）
資產：設備：門控裝置
系統可訪問性：M
系統敏感性：M
攻擊者能力：M
優先順序：H

**(Row 8)**
**Assets: Device: Smart socket**
**System accessibility: M**
**System susceptibility: M**
**Attacker capability: M**
**Priority: H** 

（第 8 列）
資產：設備：智慧插座
系統可訪問性：M
系統敏感性：M
攻擊者能力：M
優先順序：H

**(Row 9)**
**Assets: Device: Lights**
**System accessibility: H**
**System susceptibility: M**
**Attacker capability: M**
**Priority: (Blank)** 

（第 9 列）
資產：設備：電燈
系統可訪問性：H
系統敏感性：M
攻擊者能力：M
優先順序：（空白）

**(Row 10)**
**Assets: Device: Kettle**
**System accessibility: H**
**System susceptibility: M**
**Attacker capability: L**
**Priority: (Blank)** 

（第 10 列）
資產：設備：水壺
系統可訪問性：H
系統敏感性：M
攻擊者能力：L
優先順序：（空白）

***

這是 **第 4 章：進行風險評估** 的內容。請問您是否已理解？若確認無誤，我將繼續處理 **第 5 章：確定安全目標 (Determine the security objectives)**。

好的，接下來處理 **第 5 章：確定安全目標 (Determine the security objectives)** 以及 **表 B-8 (Table B-8)** 的內容。這部分涵蓋了第 11 頁（PDF 頁碼 9）的內容。

***

**5 Determine the security objectives** 

5 確定安全目標

**This section illustrates the guidance provided by item-4 of the threat modelling checklist, which guide how security objectives is determined for the case study on HCS.** 

本節說明威脅建模檢查表第 4 項提供的指導，該指導指引如何為 HCS 案例研究確定安全目標。

**Table B-8 demonstrates the definition of security objectives for the threat modelling process.** 

表 B-8 展示了威脅建模過程中的安全目標定義。

**For illustrative purposes, we limit the assets to those identify as high priority in Table B-7.** 

為便於說明，我們將資產限制為在表 B-7 中被識別為高優先順序的資產。

**The needs of CIA triad for the assets are identified in Table B-2 and defined in this table as principle objectives to safeguard.** 

資產對 CIA 三要素的需求已在表 B-2 中識別，並在此表中定義為需要保護的主要目標。

**This table also identified a list of possible security objectives.** 

本表也識別了一系列可能的安全目標。

**Table B-8: Security objectives**
**Legend: H = high, M = moderate, L = low** 

表 B-8：安全目標
圖例：H = 高，M = 中，L = 低

**(Row 1)**
**Assets: Sensor network integration platform (SNIP)**
**Confidentiality: H**
**Integrity: H**
**Availability: H**
**Security objectives:**
1. Ensure confidentiality of sensitive data.
2. Ensure confidentiality and integrity of data and commands.
3. Provide proper access control.
4. Ensure integrity of system.
5. Resilience against DOS.
6. Prevent multitenancy from compromising security. [cite: 362-371]

（第 1 列）
資產：感測器網絡整合平台 (SNIP)
機密性：H
完整性：H
可用性：H
安全目標：
1. 確保敏感數據的機密性。
2. 確保數據和指令的機密性與完整性。
3. 提供適當的存取控制。
4. 確保系統的完整性。
5. 具備對抗阻斷服務 (DOS) 的韌性。
6. 防止多租戶技術危及安全性。

**(Row 2)**
**Assets: Home sensor gateway (HSG)**
**Confidentiality: H**
**Integrity: H**
**Availability: M**
**Security objectives:**
1. Ensure confidentiality of sensitive data.
2. Ensure confidentiality and integrity of data and commands.
3. Provide proper access control.
4. Ensure integrity of HSG.
5. Fail safely.
6. Prevent multitenancy from compromising security. [cite: 372-381]

（第 2 列）
資產：家庭感測器網關 (HSG)
機密性：H
完整性：H
可用性：M
安全目標：
1. 確保敏感數據的機密性。
2. 確保數據和指令的機密性與完整性。
3. 提供適當的存取控制。
4. 確保 HSG 的完整性。
5. 失效安全（Fail safely，指發生故障時能進入安全狀態）。
6. 防止多租戶技術危及安全性。

**(Row 3)**
**Assets: Device: TV**
**Confidentiality: M**
**Integrity: H**
**Availability: L**
**Security objectives:**
1. Ensure confidentiality and integrity of data and commands.
2. Ensure integrity of TV.
3. Prevent multitenancy from compromising security. [cite: 382-388]

（第 3 列）
資產：設備：電視
機密性：M
完整性：H
可用性：L
安全目標：
1. 確保數據和指令的機密性與完整性。
2. 確保電視的完整性。
3. 防止多租戶技術危及安全性。

**(Row 4)**
**Assets: Device: Door control**
**Confidentiality: M**
**Integrity: H**
**Availability: H**
**Security objectives:**
1. Ensure confidentiality and integrity of data and commands.
2. Provide proper access control.
3. Ensure integrity of door control.
4. Ensure availability. [cite: 389-396]

（第 4 列）
資產：設備：門控裝置
機密性：M
完整性：H
可用性：H
安全目標：
1. 確保數據和指令的機密性與完整性。
2. 提供適當的存取控制。
3. 確保門控裝置的完整性。
4. 確保可用性。

**(Row 5)**
**Assets: Device: Smart socket**
**Confidentiality: L**
**Integrity: H**
**Availability: M**
**Security objectives:**
1. Fail safely.
2. Ensure integrity of data and commands.
3. Provide proper access control, including verifying connected devices.
4. Ensure integrity of smart socket. [cite: 397-405]

（第 5 列）
資產：設備：智慧插座
機密性：L
完整性：H
可用性：M
安全目標：
1. 失效安全。
2. 確保數據和指令的完整性。
3. 提供適當的存取控制，包括驗證連接的設備。
4. 確保智慧插座的完整性。

***

這是 **第 5 章：確定安全目標** 的內容。請問您是否已理解？若確認無誤，我將繼續處理 **第 6 章：定義安全需求 (Define the security requirements)**。

好的，接下來處理 **第 6 章：定義安全需求 (Define the security requirements)** 以及 **表 B-9 (Table B-9)** 的內容。這部分涵蓋了第 12 至 17 頁（PDF 頁碼 10 至 15）的內容。

***

**6 Define the security requirements** 

6 定義安全需求

**This section illustrates the guidance provided by item-5 of the threat modelling checklist, which help definition of security requirements for the case study on HCS.** 

本節說明威脅建模檢查表第 5 項提供的指導，該指導有助於定義 HCS 案例研究的安全需求。

**Table B-9 suggests the applicability of vendor disclosure checklist for assets highlighted in Table B-8.** 

表 B-9 建議了供應商揭露檢查表對表 B-8 中強調的資產的適用性。

**In practice, the vendor would have to further elaborate on how they address the security requirements listed.** 

在實務中，供應商必須進一步詳細說明他們如何處理所列出的安全需求。

**Legend: Y=Yes, N=No, NA=Not applicable** 

圖例：Y=是，N=否，NA=不適用

**Table B-9: Usage of Vendor disclosure checklist**
**1. Cryptographic support** 

表 B-9：供應商揭露檢查表的使用
1. 密碼學支援

**ID: CK-CS-01**
**Vendor disclosure checklist:** Do your devices and system employ current and industry accepted cryptographic techniques and best practices? Examples of best practices include: use of approved algorithms, sufficient key length, use of approved random number generator(s), recommended crypto-period. Do you employ proper key management (generation, exchange, storage, use, destruction, replacement, etc.) techniques?
**Please elaborate:** The strength of cryptography is fundamental to safeguard the objectives of confidentiality and integrity. In particular, the cryptography must be approved for the lifetime of the devices. Recommended for: SNIP, HSG, TV, Door control, Smart socket. 

ID: CK-CS-01
供應商揭露檢查表：您的設備和系統是否採用當前且業界認可的密碼學技術和最佳實踐？最佳實踐的範例包括：使用經批准的演算法、足夠的密鑰長度、使用經批准的隨機數生成器、建議的加密週期。您是否採用適當的密鑰管理（生成、交換、存儲、使用、銷毀、更換等）技術？
請詳述：密碼學的強度對於保護機密性和完整性的目標至關重要。特別是，密碼學必須在設備的使用壽命內獲得批准。建議用於：SNIP、HSG、電視、門控裝置、智慧插座。

**ID: CK-CS-02**
**Vendor disclosure checklist:** (Note: Context implies continued focus on key management)
**Please elaborate:** Proper key management is required to prevent the disclosure of keys through the system/device lifecycles. Recommended for: SNIP, HSG, TV, Door control, Smart socket. 

ID: CK-CS-02
供應商揭露檢查表：（註：上下文暗示繼續關注密鑰管理）
請詳述：需要適當的密鑰管理以防止密鑰在系統/設備生命週期中洩露。建議用於：SNIP、HSG、電視、門控裝置、智慧插座。

**2. Security function protection** 

2. 安全功能保護

**ID: CK-FP-01**
**Vendor disclosure checklist:** Do you establish hardware Root-of-Trust?
**Please elaborate:** To safeguard the confidentiality and integrity of sensitive data (e.g. keys) at rest and in use. Recommended for: SNIP, HSG, TV. Optional for: Door control, Smart socket. 

ID: CK-FP-01
供應商揭露檢查表：您是否建立了硬體信任根 (Root-of-Trust)？
請詳述：為了保護靜態和使用中的敏感數據（例如密鑰）的機密性和完整性。建議用於：SNIP、HSG、電視。可選用於：門控裝置、智慧插座。

**ID: CK-FP-02**
**Vendor disclosure checklist:** Do you employ secure boot?
**Please elaborate:** To safeguard integrity of the boot process. Recommended for: SNIP, HSG, TV. 

ID: CK-FP-02
供應商揭露檢查表：您是否採用安全啟動 (secure boot)？
請詳述：為了保護啟動過程的完整性。建議用於：SNIP、HSG、電視。

**3. Identification and authentication** 

3. 識別與驗證

**ID: CK-IA-01**
**Vendor disclosure checklist:** Do you employ unique, non-modifiable and verifiable identities for clients (user, device, gateway, application) and servers?
**Please elaborate:** To safeguard the integrity of identification to mitigate against threats of spoofing. Recommended for: SNIP, HSG, TV, Door control, Smart socket. 

ID: CK-IA-01
供應商揭露檢查表：您是否為客戶端（用戶、設備、網關、應用程式）和伺服器採用唯一、不可修改且可驗證的身份？
請詳述：為了保護識別的完整性，以減輕欺騙威脅。建議用於：SNIP、HSG、電視、門控裝置、智慧插座。

**ID: CK-IA-02**
**Vendor disclosure checklist:** Do you employ mutual authentication? For example, before establishing connections and after pre-defined intervals.
**Please elaborate:** To safeguard the integrity of connections to prevent unauthorised remote access. Recommended for: SNIP, HSG, TV, Door control, Smart socket. 

ID: CK-IA-02
供應商揭露檢查表：您是否採用相互驗證？例如，在建立連接之前和預定義的間隔之後。
請詳述：為了保護連接的完整性，以防止未經授權的遠端存取。建議用於：SNIP、HSG、電視、門控裝置、智慧插座。

**4. Network protection** 

4. 網絡保護

**ID: CK-NP-01**
**Vendor disclosure checklist:** Do you enforce network access control? For example, ensure explicit authorisation to join a new network and/or allow remote access.
**Please elaborate:** Proper access control is required to limit access to the system networks. Recommended for: SNIP, HSG, TV, Door control, Smart socket. 

ID: CK-NP-01
供應商揭露檢查表：您是否強制執行網絡存取控制？例如，確保加入新網絡和/或允許遠端存取的明確授權。
請詳述：需要適當的存取控制來限制對系統網絡的存取。建議用於：SNIP、HSG、電視、門控裝置、智慧插座。

**ID: CK-NP-02**
**Vendor disclosure checklist:** Do you employ proven transport protocols with security controls properly activated? Examples include: Use of TLS for TCP payloads. Use of DTLS for UDP payloads.
**Please elaborate:** To safeguard the confidentiality and integrity of the payloads. Recommended for: SNIP, HSG, TV, Door control, Smart socket. 

ID: CK-NP-02
供應商揭露檢查表：您是否採用已驗證且正確啟用安全控制的傳輸協定？範例包括：對 TCP 有效載荷使用 TLS。對 UDP 有效載荷使用 DTLS。
請詳述：為了保護有效載荷的機密性和完整性。建議用於：SNIP、HSG、電視、門控裝置、智慧插座。

**ID: CK-NP-03**
**Vendor disclosure checklist:** Do you employ industry best practices for secure connectivity? Examples of industry best practices: Use of VPN or leased lines. Use of private mobile APNs from telecommunication operators when using a public mobile carrier network. Use of DNS pinning to prevent DNS spoofing. Use of traffic filtering based on type, port and destination. Use of certificate pinning. Employ TLS when using MQTT. Scan for open network ports.
**Please elaborate:** Applicable to safeguard the data flows highlighted in Table B.3. Recommended for: SNIP, HSG, TV, Door control, Smart socket. 

ID: CK-NP-03
供應商揭露檢查表：您是否採用業界最佳實踐來實現安全連接？業界最佳實踐的範例：使用 VPN 或專線。使用公共移動運營商網絡時，使用來自電信運營商的專用移動 APN。使用 DNS pinning 防止 DNS 欺騙。根據類型、端口和目的地使用流量過濾。使用憑證綁定 (Certificate pinning)。使用 MQTT 時採用 TLS。掃描開放的網絡端口。
請詳述：適用於保護表 B.3 中強調的數據流。建議用於：SNIP、HSG、電視、門控裝置、智慧插座。

**ID: CK-NP-04**
**Vendor disclosure checklist:** Use whitelisting to establish or deny connections from non-trusted sources. Do you segregate communication channels for trusted end points from non-trusted? Examples include: Use of VLAN. Use of firewalls for DMZ. Use of unidirectional security gateway. Physical isolation.
**Please elaborate:** Applicable to safeguard the data flows highlighted in Table B.3. SNIP and HSG can segregate communication channels for administration purposes from normal operations. SNIP should establish DMZ, using firewalls, against remote connections from devices and users. HSG should safeguard the devices within home, from connections outside the home. Recommended for: SNIP, HSG, TV, Door control, Smart socket. 

ID: CK-NP-04
供應商揭露檢查表：使用白名單來建立或拒絕來自不可信來源的連接。您是否將受信任端點的通訊通道與不可信端點隔離？範例包括：使用 VLAN。使用防火牆建立 DMZ。使用單向安全網關。物理隔離。
請詳述：適用於保護表 B.3 中強調的數據流。SNIP 和 HSG 可以將管理用途的通訊通道與正常操作隔離。SNIP 應使用防火牆建立 DMZ，以防範來自設備和用戶的遠端連接。HSG 應保護家庭內的設備免受家庭外部的連接影響。建議用於：SNIP、HSG、電視、門控裝置、智慧插座。

**5. Data protection** 

5. 數據保護

**ID: CK-DP-01**
**Vendor disclosure checklist:** Do you protect the confidentiality and integrity of your sensitive data? in transit, in use, at rest.
**Please elaborate:** To safeguard the confidentiality and integrity of sensitive data. Sensitive data includes cryptographic keys and user credentials. Recommended for: SNIP, HSG, TV, Door control, Smart socket. 

ID: CK-DP-01
供應商揭露檢查表：您是否保護敏感數據的機密性和完整性？（傳輸中、使用中、靜態）
請詳述：為了保護敏感數據的機密性和完整性。敏感數據包括加密密鑰和用戶憑證。建議用於：SNIP、HSG、電視、門控裝置、智慧插座。

**ID: CK-DP-02**
**Vendor disclosure checklist:** Do you protect the authenticity and integrity your codes and firmware? in transit, in use, at rest.
**Please elaborate:** To safeguard the software and firmware in SNIP, HSG and devices, including transportation of updates. Recommended for: SNIP, HSG, TV, Door control, Smart socket. 

ID: CK-DP-02
供應商揭露檢查表：您是否保護代碼和韌體的真實性和完整性？（傳輸中、使用中、靜態）
請詳述：為了保護 SNIP、HSG 和設備中的軟體和韌體，包括更新的傳輸。建議用於：SNIP、HSG、電視、門控裝置、智慧插座。

**ID: CK-DP-03**
**Vendor disclosure checklist:** Do you ensure the authenticity and integrity of your data (e.g. inputs, commands and sensing data)? in transit, in use, at rest. Examples include: Validate incoming content-types. Validate response types. Validate the HTTP methods against authorisation credentials. Whitelist allowable HTTP methods. Define the acceptable character set (e.g. UTF-8). Validate that input characters are acceptable. Encode/escape input and output.
**Please elaborate:** To safeguard the data in SNIP, HSG and devices, including inputs and commands. Recommended for: SNIP, HSG, TV, Door control, Smart socket. 

ID: CK-DP-03
供應商揭露檢查表：您是否確保數據（例如輸入、指令和感測數據）的真實性和完整性？（傳輸中、使用中、靜態）。範例包括：驗證傳入的內容類型。驗證回應類型。根據授權憑證驗證 HTTP 方法。將允許的 HTTP 方法列入白名單。定義可接受的字符集（例如 UTF-8）。驗證輸入字符是否可接受。對輸入和輸出進行編碼/轉義。
請詳述：為了保護 SNIP、HSG 和設備中的數據，包括輸入和指令。建議用於：SNIP、HSG、電視、門控裝置、智慧插座。

**ID: CK-DP-04**
**Vendor disclosure checklist:** Do you enforce access control to detect and prevent unauthorised data access and exfiltration, and filter your outputs?
**Please elaborate:** To safeguard aggregated data in SNIP and HSG from unauthorised access. Recommended for: SNIP, HSG. 

ID: CK-DP-04
供應商揭露檢查表：您是否強制執行存取控制以檢測並防止未經授權的數據存取和外洩，並過濾您的輸出？
請詳述：為了保護 SNIP 和 HSG 中的聚合數據免受未經授權的存取。建議用於：SNIP、HSG。

**6. Access protection** 

6. 存取保護

**ID: CK-AP-01**
**Vendor disclosure checklist:** Do you employ mechanisms to manage and secure local and/or remote access? Example of mechanisms include: auto logoff, screen lock, lock-out for repeated unauthorised attempts, forced re-authorisation.
**Please elaborate:** To safeguard SNIP and HSG from unauthorised access, both locally and remotely, including physical access. Recommended for: SNIP, HSG. 

ID: CK-AP-01
供應商揭露檢查表：您是否採用機制來管理和保護本地和/或遠端存取？機制範例包括：自動登出、螢幕鎖定、重複未授權嘗試後的鎖定、強制重新授權。
請詳述：為了保護 SNIP 和 HSG 免受本地和遠端的未經授權存取，包括物理存取。建議用於：SNIP、HSG。

**ID: CK-AP-02**
**Vendor disclosure checklist:** Do you send out-of-band notifications on impactful operations and/or alerts (eg. credential reset, security update failures)?
**Please elaborate:** To enable users to detect unauthorised attempts from alerts. Recommended for: SNIP, HSG. 

ID: CK-AP-02
供應商揭露檢查表：您是否針對重大操作和/或警報（例如憑證重置、安全更新失敗）發送帶外 (out-of-band) 通知？
請詳述：為了讓用戶能夠透過警報檢測未經授權的嘗試。建議用於：SNIP、HSG。

**ID: CK-AP-03**
**Vendor disclosure checklist:** Do you enforce access control to prevent unauthorised access to system interfaces, system files and removable media?
**Please elaborate:** To safeguard against physical access to system/device interfaces. Recommended for: SNIP, HSG, TV, Door control, Smart socket. 

ID: CK-AP-03
供應商揭露檢查表：您是否強制執行存取控制以防止未經授權存取系統介面、系統文件和可移動媒體？
請詳述：為了防止對系統/設備介面的物理存取。建議用於：SNIP、HSG、電視、門控裝置、智慧插座。

**ID: CK-AP-04**
**Vendor disclosure checklist:** Do you employ anti-tamper mechanisms for resistance, evidence, detection and/or response?
**Please elaborate:** To prevent and detect physical tampering. Recommended for: HSG, TV, Door control, Smart socket. 

ID: CK-AP-04
供應商揭露檢查表：您是否採用防篡改機制來進行抵抗、取證、檢測和/或回應？
請詳述：為了防止和檢測物理篡改。建議用於：HSG、電視、門控裝置、智慧插座。

**ID: CK-AP-05**
**Vendor disclosure checklist:** Do you support multi-factor authentication for impactful operations (eg. credential reset)?
**Please elaborate:** To safeguard impactful operations by requiring higher level of authentication. Recommended for: SNIP, HSG, TV, Door control, Smart socket. 

ID: CK-AP-05
供應商揭露檢查表：您是否支援對重大操作（例如憑證重置）進行多重驗證？
請詳述：透過要求更高級別的驗證來保護重大操作。建議用於：SNIP、HSG、電視、門控裝置、智慧插座。

**7. Security management** 

7. 安全管理

**ID: CK-MT-01**
**Vendor disclosure checklist:** Do you employ proper user and password management? Examples include: Enforce strong password policy. Enforce no default passwords. Ensure that password recovery and reset mechanism are secure.
**Please elaborate:** To safeguard access to SNIP, HSG and TV (device with mobile operating system). Recommended for: SNIP, HSG, TV. 

ID: CK-MT-01
供應商揭露檢查表：您是否採用適當的用戶和密碼管理？範例包括：強制執行強密碼策略。強制不使用預設密碼。確保密碼恢復和重置機制是安全的。
請詳述：為了保護對 SNIP、HSG 和電視（具有行動作業系統的設備）的存取。建議用於：SNIP、HSG、電視。

**ID: CK-MT-02**
**Vendor disclosure checklist:** Do you enforce proper access control to management functions? Examples include: Enforce least privilege policy. Use of attribute-based access control (ABAC) or role-based access control (RBAC). Implement dual control for key management protection to prevent a single bad actor's compromise to the key materials. Implement separation of duties to key management system to prevent a single bad actor/administrator from compromising the system.
**Please elaborate:** To safeguard the administration functions of SNIP and HSG from normal operations. Recommended for: SNIP, HSG. 

ID: CK-MT-02
供應商揭露檢查表：您是否對管理功能強制執行適當的存取控制？範例包括：強制執行最小權限策略。使用基於屬性的存取控制 (ABAC) 或基於角色的存取控制 (RBAC)。對密鑰管理保護實施雙重控制，以防止單一不良行為者破壞密鑰材料。對密鑰管理系統實施職責分離，以防止單一不良行為者/管理員破壞系統。
請詳述：為了保護 SNIP 和 HSG 的管理功能免受正常操作的影響。建議用於：SNIP、HSG。

**ID: CK-MT-03**
**Vendor disclosure checklist:** Do you employ malware mitigation mechanism? Examples include: Ensure file integrity using cryptographic hash. Baseline "normal" behaviour. Detect unauthorised software. Prohibit insecure bootloaders.
**Please elaborate:** To safeguard the integrity of the software. Recommended for: SNIP, HSG, TV. 

ID: CK-MT-03
供應商揭露檢查表：您是否採用惡意軟體緩解機制？範例包括：使用加密雜湊確保文件完整性。建立「正常」行為基準。檢測未經授權的軟體。禁止不安全的引導加載程式 (bootloaders)。
請詳述：為了保護軟體的完整性。建議用於：SNIP、HSG、電視。

**ID: CK-MT-04**
**Vendor disclosure checklist:** Do you secure remote management of devices, including sensor gateways? Examples include: Support secure Over-The-Air (OTA) updates of device applications and configurations. Support software and/or firmware updates using cryptographically secure methods. Support platform integrity checking, such as the measured boot mechanism or verifying the firmware integrity. Restrict remote management to secure networks.
**Please elaborate:** To safeguard the remote management function of HSG and devices, including remote updates. Recommended for: SNIP, HSG, TV. Optional for: Door control, Smart socket. 

ID: CK-MT-04
供應商揭露檢查表：您是否保護設備（包括感測器網關）的遠端管理？範例包括：支援設備應用程式和配置的安全空中下載 (OTA) 更新。使用密碼學安全的方法支援軟體和/或韌體更新。支援平台完整性檢查，例如測量啟動 (measured boot) 機制或驗證韌體完整性。將遠端管理限制在安全網絡中。
請詳述：為了保護 HSG 和設備的遠端管理功能，包括遠端更新。建議用於：SNIP、HSG、電視。可選用於：門控裝置、智慧插座。

**8. Resiliency support** 

8. 韌性支援

**ID: CK-RS-01**
**Vendor disclosure checklist:** Does your device support integrity self-test, error detection and correction for critical functions and return to a safe state?
**Please elaborate:** To safeguard integrity and availability of the system, devices are monitored and attested periodically. Recommended for: HSG, TV, Door control, Smart socket. 

ID: CK-RS-01
供應商揭露檢查表：您的設備是否支援針對關鍵功能的完整性自我測試、錯誤檢測和修正，並能恢復到安全狀態？
請詳述：為了保護系統的完整性和可用性，設備會受到定期監控和證明。建議用於：HSG、電視、門控裝置、智慧插座。

**ID: CK-RS-02**
**Vendor disclosure checklist:** Do you safeguard against a compromised device from compromising the system? Examples include: Use of Perfect Forward Secrecy (PFS) for secure communication. Use of distinct secret keys for individual device.
**Please elaborate:** To safeguard availability of the system, in the event devices are compromised. For example, allowed for compromised devices to be disconnected manually. Recommended for: HSG, TV, Door control, Smart socket. 

ID: CK-RS-02
供應商揭露檢查表：您是否防止受損設備危及系統？範例包括：使用完全前向保密 (PFS) 進行安全通訊。為個別設備使用不同的密鑰。
請詳述：為了在設備受損時保護系統的可用性。例如，允許手動斷開受損設備的連接。建議用於：HSG、電視、門控裝置、智慧插座。

**ID: CK-RS-03**
**Vendor disclosure checklist:** Do you employ mechanisms against failures from resource exhaustion and/or malicious attacks such as DDOS? Examples include: Monitor to ensure that cloud resources are sufficient to sustain services. Detect resource exhaustion, for early preventive or corrective actions. Control the execution of resource-intensive software. Enforce power thresholds. Limit the number of concurrent sessions. Operate with excess capacity.
**Please elaborate:** To safeguard availability of the system by detecting and preventing resource exhaustion. Recommended for: SNIP. 

ID: CK-RS-03
供應商揭露檢查表：您是否採用機制來對抗因資源耗盡和/或惡意攻擊（如 DDoS）導致的故障？範例包括：監控以確保雲端資源足以維持服務。檢測資源耗盡，以便採取早期預防或糾正措施。控制資源密集型軟體的執行。強制執行功率閾值。限制並發會話的數量。以超額容量運作。
請詳述：透過檢測和防止資源耗盡來保護系統的可用性。建議用於：SNIP。

**ID: CK-RS-04**
**Vendor disclosure checklist:** Do you conduct regular backups of system data (including settings)?
**Please elaborate:** To safeguard availability of the system ensuring the ability to recover from a compromised state. Recommended for: SNIP, HSG. 

ID: CK-RS-04
供應商揭露檢查表：您是否定期備份系統數據（包括設定）？
請詳述：為了保護系統的可用性，確保能夠從受損狀態恢復。建議用於：SNIP、HSG。

**9. Security audit** 

9. 安全稽核

**ID: CK-AU-01**
**Vendor disclosure checklist:** Do your devices and system record enough information (e.g. who does what and when) in audit logs and flag significant events? Example of events include: User logins, logouts and unsuccessful authentication attempts. Connection, disconnection attempts and unsuccessful connection attempts. Unsuccessful authorisation attempts. Access to sensitive data. Import and export of data from removable media. Any change in access privileges. Creation, modification and deletion of data by user. Impactful operations. Remote operations. Security update failures. Physical access attempts where possible. Emergency access where possible.
**Please elaborate:** To safeguard the system by having the ability to detect and analyse when attacks are realised. Recommended for: SNIP, HSG, TV. 

ID: CK-AU-01
供應商揭露檢查表：您的設備和系統是否在稽核日誌中記錄足夠的資訊（例如誰在何時做了什麼）並標記重大事件？事件範例包括：用戶登入、登出和不成功的驗證嘗試。連接、斷開連接嘗試和不成功的連接嘗試。不成功的授權嘗試。存取敏感數據。從可移動媒體匯入和匯出數據。存取權限的任何更改。用戶創建、修改和刪除數據。重大操作。遠端操作。安全更新失敗。可能的物理存取嘗試。可能的緊急存取。
請詳述：透過具備檢測和分析攻擊何時實現的能力來保護系統。建議用於：SNIP、HSG、電視。

**ID: CK-AU-02**
**Vendor disclosure checklist:** Are your audit logs protected from modification, deletion, physical tampering and sensitive data disclosure?
**Please elaborate:** To safeguard the confidentiality and integrity of audit logs. Recommended for: SNIP, HSG. 

ID: CK-AU-02
供應商揭露檢查表：您的稽核日誌是否受到保護，免受修改、刪除、物理篡改和敏感數據洩露？
請詳述：為了保護稽核日誌的機密性和完整性。建議用於：SNIP、HSG。

**10. Lifecycle protection** 

10. 生命週期保護

**ID: CK-LP-01**
**Vendor disclosure checklist:** Have you conducted threat modelling to identify, analyse and mitigate threats to the system?
**Please elaborate:** To understand and focus limited resources to what needs protection. Recommended for: SNIP, HSG, TV, Door control, Smart socket. 

ID: CK-LP-01
供應商揭露檢查表：您是否進行了威脅建模以識別、分析和緩解系統威脅？
請詳述：為了了解並將有限的資源集中在需要保護的地方。建議用於：SNIP、HSG、電視、門控裝置、智慧插座。

**ID: CK-LP-02**
**Vendor disclosure checklist:** Did you design and develop the system using a secure systems engineering approach?
**Please elaborate:** To employ "security by design" principle and develop system/design using secure best practices. Recommended for: SNIP, HSG, TV, Door control, Smart socket. 

ID: CK-LP-02
供應商揭露檢查表：您是否使用安全系統工程方法設計和開發系統？
請詳述：為了採用「設計安全」原則並使用安全最佳實踐開發系統/設計。建議用於：SNIP、HSG、電視、門控裝置、智慧插座。

**ID: CK-LP-03**
**Vendor disclosure checklist:** Do you implement and maintain the system with components from a secure supply chain, with no known vulnerabilities?
**Please elaborate:** To safeguard the supply chain of system components. In this case, maintain a list of suppliers for the components. Recommended for: SNIP, HSG, TV, Door control, Smart socket. 

ID: CK-LP-03
供應商揭露檢查表：您是否使用來自安全供應鏈且沒有已知漏洞的組件來實施和維護系統？
請詳述：為了保護系統組件的供應鏈。在此情況下，維護組件供應商列表。建議用於：SNIP、HSG、電視、門控裝置、智慧插座。

**ID: CK-LP-04**
**Vendor disclosure checklist:** Do you communicate, provide and update security information (terms of service, features, guidelines, instructions and notifications, etc.), in simple language and timely manner? Examples of security information include: security polices, security updates, instructions for device/media sanitisation, end-of-life notifications.
**Please elaborate:** To ensure that there is a ownership and commitment to provide security information in a timely manner so that known vulnerabilities can be mitigated. Recommended for: SNIP, HSG, TV, Door control, Smart socket. 

ID: CK-LP-04
供應商揭露檢查表：您是否以簡單的語言和及時的方式傳達、提供和更新安全資訊（服務條款、功能、指南、說明和通知等）？安全資訊的範例包括：安全策略、安全更新、設備/媒體清理說明、終止支援通知。
請詳述：為了確保有歸屬權和承諾及時提供安全資訊，以便可以緩解已知漏洞。建議用於：SNIP、HSG、電視、門控裝置、智慧插座。

**ID: CK-LP-05**
**Vendor disclosure checklist:** Do you ensure that the system is hardened before the "Operational" lifecycle phase? Examples of system hardening include: Remove all backdoors. Remove all debug codes from the released version. Change default configuration and disable unnecessary services. Remove or tamper-covered JTAG, unneeded serial and ports before deployment. Harden VM host properly, including disabling memory sharing between VM. Remove default and hardcoded passwords.
**Please elaborate:** Employ "security by defaults" principle and ensure the system is configure securely before operation. Recommended for: SNIP, HSG, TV, Door control, Smart socket. 

ID: CK-LP-05
供應商揭露檢查表：您是否確保在「操作」生命週期階段之前對系統進行加固？系統加固的範例包括：移除所有後門。從發布版本中移除所有調試代碼。更改預設配置並禁用不必要的服務。部署前移除 JTAG、不需要的串行端口和端口，或對其進行防篡改覆蓋。適當加固虛擬機主機，包括禁用虛擬機之間的記憶體共享。移除預設和硬編碼密碼。
請詳述：採用「預設安全」原則，並確保系統在操作前配置安全。建議用於：SNIP、HSG、電視、門控裝置、智慧插座。

**ID: CK-LP-06**
**Vendor disclosure checklist:** Do you maintain an inventory of connected devices, software and firmware versions, applied patches and updates throughout the "Operational" lifecycle stage?
**Please elaborate:** Employ the "accountability" principle to keep track that only authorised and patched devices are in use. Recommended for: SNIP, HSG, TV, Door control, Smart socket. 

ID: CK-LP-06
供應商揭露檢查表：您是否在整個「操作」生命週期階段維護連接設備、軟體和韌體版本、已應用的修補程式和更新的清單？
請詳述：採用「問責制」原則，以追蹤僅使用經過授權和修補的設備。建議用於：SNIP、HSG、電視、門控裝置、智慧插座。

**ID: CK-LP-07**
**Vendor disclosure checklist:** Do you conduct penetration testing and/or vulnerability assessment periodically, and before each major release?
**Please elaborate:** Conduct periodic testing on the integrated system to detect vulnerabilities due to improper integration. Recommended for: SNIP, HSG, TV, Door control, Smart socket. 

ID: CK-LP-07
供應商揭露檢查表：您是否定期以及在每次主要發布之前進行滲透測試和/或漏洞評估？
請詳述：對整合系統進行定期測試，以檢測因整合不當而產生的漏洞。建議用於：SNIP、HSG、電視、門控裝置、智慧插座。

**ID: CK-LP-08**
**Vendor disclosure checklist:** Do you establish proper vulnerability disclosure and management? Examples include: Ensure the supply chain's capability to provide upgrades and patches. Provide vulnerability disclosure and processes to track and response promptly. Provide firmware and software patches/updates for vulnerabilities discovered, in a timely manner. Employ proper change management processes to manage security patches or updates. Notify and/or allow user to approve/reject updates, patches and changes to user settings, where appropriate. Disclose minimum support period.
**Please elaborate:** Build resilience by establishing ownership and standard operating procedures (SOPs) to disclosure, manage and resolve vulnerability. Recommended for: SNIP, HSG, TV, Door control, Smart socket. 

ID: CK-LP-08
供應商揭露檢查表：您是否建立了適當的漏洞揭露和管理？範例包括：確保供應鏈提供升級和修補程式的能力。提供漏洞揭露和流程以進行追蹤和及時回應。及時為發現的漏洞提供韌體和軟體修補程式/更新。採用適當的變更管理流程來管理安全修補程式或更新。在適當的情況下，通知和/或允許用戶批准/拒絕更新、修補程式和用戶設定的更改。揭露最短支援期限。
請詳述：透過建立所有權和標準作業程序 (SOP) 來揭露、管理和解決漏洞，從而建立韌性。建議用於：SNIP、HSG、電視、門控裝置、智慧插座。

**ID: CK-LP-09**
**Vendor disclosure checklist:** Do you ensure that identities, certificates and secrets are secured throughout the lifecycle (e.g. creation, provisioning, renewal and revocation)?
**Please elaborate:** By the "accountability" principle, the identities and secrets should be safeguard throughout their lifecycles. Recommended for: SNIP, HSG, TV, Door control, Smart socket. 

ID: CK-LP-09
供應商揭露檢查表：您是否確保身份、憑證和秘密在整個生命週期（例如創建、配置、更新和撤銷）中都是安全的？
請詳述：根據「問責制」原則，身份和秘密應在其整個生命週期中受到保護。建議用於：SNIP、HSG、電視、門控裝置、智慧插座。

**ID: CK-LP-10**
**Vendor disclosure checklist:** Do you sanitise devices and systems of security data and sensitive user data, before the "Reuse or Dispose" lifecycle stages?
**Please elaborate:** By the "accountability" principle, the sensitive data should be safeguard throughout the system/device's lifecycles. Recommended for: SNIP, HSG, TV, Door control, Smart socket. 

ID: CK-LP-10
供應商揭露檢查表：在「再利用或處置」生命週期階段之前，您是否對設備和系統的安全數據和敏感用戶數據進行清理？
請詳述：根據「問責制」原則，敏感數據應在系統/設備的整個生命週期中受到保護。建議用於：SNIP、HSG、電視、門控裝置、智慧插座。

***

這是 **第 6 章：定義安全需求** 的內容。這也是文件的最後一部分。請問您是否還有其他問題或需要進一步的協助？