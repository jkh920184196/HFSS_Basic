---
description: 根據應用選擇適當的解題及設定，最常用的是HFSS + Network Analysis + Terminal + Radiation
---

# 解題器 (Solution)

<figure><img src="../.gitbook/assets/image (7) (2).png" alt=""><figcaption></figcaption></figure>

## 解題類型

### HFSS

* 適合天線、連結器、封裝、射頻微波元件(濾波器、分波器、電感、電容等)設計
* 支援Modal及Terminal兩大類端口模式

### HFSS with Hybrid and Arrays

* 適合陣列天線或空間電磁場傳播等大空間模擬計算
* 支援FEBI、SBR+、IE等不同區域混和計算

### Transient

* 基於不連續Galerkin方法（DGTD）的3D全波瞬態或時域電磁場求解器。這種四面體有限元技術利用了與HFSS相同的自動適應精度網格技術，使HFSS成為電磁學精度的金標準。您可以在具有脈衝激勵的應用中調查、提取和可視化場，例如時域反射測量（TDR）、地面穿透雷達、靜電放電、電磁干擾和閃電。這種技術補充了HFSS中的頻域解決方案技術，使您能夠詳細了解設計的電磁特性。支援GPU加速。

### SBR+

* SBR+能夠快速且準確地預測在電氣大型平台上安裝的天線輻射模式、近場和天線間的耦合。HFSS SBR+利用了加強版的漸近射擊和反射射線（SBR+）技術，能夠有效地計算準確的電磁波路徑解，並且具有驚人的運算速度和可擴展性。此外，HFSS SBR+還包括了一些先進的物理模型，如蠕行波和UTD繞射射線。HFSS SBR+能夠計算安裝的天線輻射模式、Tx/Rx天線對之間的耦合、空間E和H場分佈（近場）、入射、散射和總場，以及共振和交叉振輻射和散射。此外，透過視覺射線跟蹤（VRT）功能，使用者可以在分析前後查看SBR、蠕行波和UTD邊緣射線，這對於理解射線反彈機制、模式零點或峰值的來源、幾何光學（GO）阻擋和特定目標照明角度的射線密度等問題提供了有用的信息。

### Eigenmode

* 封閉金屬腔體共振模態計算

### Characteristic Mode

* 開放空間金屬結構共振模態計算

## 選項

### Network vs. Composite Excitation

Network可以在模擬之後調整Ports激發強度及相位，模擬所需時間及記憶體較多。可以輸出S參數，輻射場等，為主要使用模式。

Composite Excitation則必須在模擬之前先行設定，模擬完成之後無法修改，模擬所需時間及記憶體較少。另外還具備以下限制：

* 不支持差分對。
* 不支持衍生。
* 報告器無法顯示 S 參數或基於它們的任何數據（Y、Z、…）。
* Gamma、終端（和模式）端口阻抗將可用。
* 矩陣顯示面板將僅限於 Gamma 和端口阻抗。
* 不會有 Touchstone 導出。
* 報告器可以繪製場以及 Active S（和 Active Y 等）。但是，Active S 由求解器提供，而非後處理。Active Y、Z 和 VSWR 是 Active S 和端口 Zo 的函數。
* 支持輻射場。

### Modal vs Terminal

Modal可以支援高階模態計算，適用於導波管設計。Terminal只支援基礎模態，SI/PI模型抽取主要使用Terminal。

### Auto-Open Region

* Radiation
* FE-BI
* PML
