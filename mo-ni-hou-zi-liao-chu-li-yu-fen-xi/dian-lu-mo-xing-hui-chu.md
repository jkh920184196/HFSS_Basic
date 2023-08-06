---
description: >-
  在 HFSS 中，可以將模擬結果，如 S 參數、Z 參數或 Y
  參數等矩陣數據或是SPICE等效電路導出到檔案中，這些檔案可以用於後續的分析或與其他軟體進行交互。
---

# 電路模型匯出

### Export Matrix Data

在 HFSS 中，您可以將矩陣數據（如S-矩陣，Y-矩陣，Z-矩陣，Gamma，或Zo）輸出到各種格式，包括 _.tab 數據表格式、_.sNp Touchstone S參數格式、_.nmf 中立模型格式、_.m MATLAB格式和\*.cit Citifile格式。

對於 Touchstone 格式，您可以選擇是否覆寫解決方案重整，也可以指定是否包含 Gamma 和 Impedance 的註釋，以及設置數字精確度位數。

請注意，輸出的數據默認是按照波形端口在激勵樹中的字母和數字順序列出的。您可以在 HFSS 選項對話框中將此順序更改為創建順序，而不會使解決方案無效。如果您選擇 Touchstone 格式，系統會首先顯示一個對話框，讓您指定數字精度，以及是否覆寫解決方案重整。如果是這樣，您可以指定輸出重整阻抗（一個整數值）。在這裡，您還可以指定是否包含 Gamma 和 Impedance 的註釋，以及數字精確度位數（預設值為15）。

另外，如果您在 Matrix Data 標籤下修改了插值或 Fast 掃描中解決頻率的顯示（通過點擊 Edit Freqs 然後在 Edit Sweep 對話框中修改值），則只有列出的頻率會被輸出到檔案中。

### Equivalent Circuit Export

您可以將驅動終端解的 S 參數數據導出到 PSpice、HSPICE、Spectre 或 Maxwell Spice 格式。將新的數據文件導入到 PSpice、HSPICE、Spectre 或 Maxwell Spice 將使您能夠在電路模擬中包含波效應。您也可以導出端口的 WElement 模型。

注意事項：您必須有一個頻率掃描解和五個或更多的頻率點才能成功導出等效電路數據文件。看看幫助主題中關於全波 SPICE 的頻率範圍選擇的建議。GUI 可讓您導出包含差分對的模型的全波 Spice，但它將在原始的單端形式中靜默導出數據。全波 Spice 模型是一種 "寬帶" 等效電路（也就是說，其 S 參數與解的整個頻率掃描範圍相匹配。）

某些離散掃描允許全波 SPICE 導出。如果離散數據均勻分佈，包含直流，並且至少有 500 個頻率點，則允許進行。

在 HFSS 中，您可以選擇導出到以下格式：PSpice (_.lib)、Nexxim State Space (.sss)、Spectre (_.cir)、Star HSpice (\*.sp)、Twin Builder (.sml)。當請求 Twin Builder 格式時，將創建 \*.sml 和 \*.png。後者包含 GIF 格式的圖像。

您可以選擇是否啟用全波 Spice 導出，還可以編輯期望的擬合誤差（百分比）和最大階數的默認值。

另外，HFSS 支持從驅動模態設計中導出全波 Spice，只要所有端口都只有一種模式。但是，HFSS 不支持在驅動模態設計中定義差分對。

您還可以選擇是否強制通道，選擇是否導出低頻帶寬的集總元件模型，選擇是否為 Matlab 擴展部分分數，以及選擇是否將可用的掃描結合到單個輸出文件中。

最後，點擊 OK，S 參數將會被寫入到你在等效電路數據格式中指定的數據文件。

<figure><img src="../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>
