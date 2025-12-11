## 前言

物聯網網路安全標籤計畫 [CLS(IoT)] 是新加坡網路安全局（CSA）為加強新加坡網路空間安全和提升網路衛生水平所做努力的一部分。其目的是透過使安全措施對消費者更加透明，提高安全意識，並賦予消費者利用網路安全標籤上的資訊，為具有更好安全性的產品做出明智的購買決策。

在 CLS(IoT) 計畫下，網路安全標籤提供了網路連接智慧裝置的安全等級指示。

CLS(IoT) 旨在激勵開發商/製造商開發和提供具有增強網路安全措施的產品。這些標籤也有助於在市場上區分具有更好網路安全保障措施的智慧裝置與其競爭對手。

同時，CSA 有意與其他志同道合的夥伴合作，互相認可 CLS(IoT)，目標是消除跨國界的重複評估。

CLS(IoT) 是更安全網路空間總體規劃下的一項倡議，旨在創建一個更安全的網路空間，保護公眾和企業免受網路威脅，推動新加坡邁向數位經濟和智慧國家。

CLS(IoT) 由網路安全認證中心（CCC）擁有和管理，該中心隸屬於新加坡網路安全局（CSA）。

## 簡介 (INTRODUCTION)

本文件規定了物聯網網路安全標籤計畫 [CLS(IoT)] 下家用閘道器（Home Gateway）的評估方法。

## 預期用途 (INTENDED USAGE)

本評估方法旨在提供澄清說明，以更好地協調各項安全條款的期望和要求，從而促進 CLS(IoT) 的更容易採用。

這是透過為每個安全條款指定三個主要組成部分來實現的：

1. **最低要求** – 規定物聯網裝置為滿足該條款所需達成的要求。

2. **支持證據** – 提供開發商應提供的預期證據的範例和/或建議，以便評估員確定特定條款是否得到滿足。

3. **評估** – 規定評估員將從所提供的支持證據中檢查/審查的內容，以確定每個條款所規定的最低要求是否得到滿足。

### 免責聲明：

雖然本文件為每個安全條款提供了可接受的支持證據範例，但這絕非詳盡無遺，所需的支持證據可能會偏離所述內容。

CCC 保留要求進一步澄清、更多支持證據的權利，並且如果所提供的證據被認為不足以滿足安全條款的要求，CCC 有權拒絕任何證據。

開發商為滿足安全條款的最低要求而提供的證據不得包含個人可識別資訊（PII）。

當前版本： Version 1.1
發布日期： April 2025（2025年4月）

---

- [5.1 – 禁用通用預設密碼 (NO UNIVERSAL DEFAULT PASSWORDS)](./5.1-no-universal-default-passwords.md)
- [5.2 – 實施一種管理漏洞報告的機制 (IMPLEMENT A MEANS TO MANAGE REPORTS OF VULNERABILITIES)](./5.2-implement-a-means-to-manage-reports-of-vulnerabilities.md)
- [5.3 – 保持軟體更新 (KEEP SOFTWARE UPDATED)](./5.3-keep-software-updated.md)
- [5.4 – 安全儲存安全參數 (SECURELY STORE SECURITY PARAMETERS)](./5.4-securely-store-security-parameters.md)
- [5.5 – 安全通訊 (COMMUNICATE SECURELY)](./5.5-communicate-securely.md)
- [5.6 – 最小化暴露的攻擊面 (MINIMISE EXPOSED ATTACK SURFACES)](./5.6-minimise-exposed-attack-surfaces.md)

---

### Table 1 - 各 CLS(IoT) 家庭閘道器等級的強制性條款 (Mandatory Provisions for each CLS(IoT) Home Gateway Level)

| CLS(IoT) Home Gateway Levels | 評估活動 (Assessment Activities) | 格式 (Format) | 強制性條款 (Mandatory Provisions) |
| :--- | :--- | :--- | :--- |
| **Level 1** | 安全基準 (Security Baseline) | 開發商的符合性聲明 (Developer's declaration of conformity)。 | 5.1-1, 5.1-2, 5.1-3, 5.1-4, 5.1-5, 5.2-1, 5.3-1, 7.3-1, 5.3-2, 5.3-3, 7.3-4, 5.3-6, 5.3-7, 7.3-7, 5.3-8, 5.3-9, 5.3-10, 5.3-13, 5.3-16 |
| **Level 2** | 遵守國際標準 (Adherence to International Standards) | 遵守 Level 1 條款。 | **Level 1 條款**，以及：<br>5.4-1, 7.4-1, 5.4-2, 7.4-2, 5.4-3, 7.4-3, 5.4-4, 5.5-1, 5.5-5, 7.5-6, 5.5-7, 7.5-7, 5.5-8, 5.6-1, 7.6-1, 5.6-2, 7.6-2, 7.6-3, 5.6-4, 7.6-4, 5.6-5, 7.6-9, 5.8-2, 5.8-3, 5.9-2, 5.11-1 |
| **Level 3** | 生命週期要求與軟體二進位分析 (Lifecycle Requirements and Software Binary Analysis) | 基於開發商符合性聲明的生命週期要求。<br>基於測試實驗室獨立評估的軟體二進位分析。 | 5.13-1, 6.1, 6.2, 6.3, 6.5<br>**Level 1 條款**<br>**Level 2 條款**<br>**CK-LP** (生命週期文件) |
| **Level 4** | 滲透測試 (Penetration Testing) | 測試實驗室總結測試執行與結果的報告。 | **Level 1 條款**<br>**Level 2 條款**<br>**CK-LP** (生命週期文件)<br>*(包含上述所有條款範圍的滲透測試)* |

---
