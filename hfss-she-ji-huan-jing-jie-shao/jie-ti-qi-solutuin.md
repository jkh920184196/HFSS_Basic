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

* 模擬電磁場時域傳播
* 支援GPU加速

### SBR+

* 模擬電磁場空間傳播行為(反射、繞射、折射等等)

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
