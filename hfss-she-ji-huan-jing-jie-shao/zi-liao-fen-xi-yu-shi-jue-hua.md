# 模擬報告輸出

### Report種類

在創建報告時，可用的報告類型會依據你的模擬設定而有所不同。報告中的資訊可以用幾種格式來顯示。當你在功能區選擇 "Results"（結果）標籤時，你將會看到一系列的報告類型分組，這取決於給定設計與解決方案類型可用的報告。例如，"Modal Solution Data"（模態解決方案數據），"Fields Report"（場報告），"Emission Test"（輻射測試），"Antenna Parameters"（天線參數），"Near Fields"（近場），"Terminal Solution Report"（終端解決方案報告），"Far Fields Report"（遠場報告），"Characteristic Mode Data"（特性模式數據）等等，這些都會有下拉選單，顯示該組中對該設計可用的報告類型。

<figure><img src="../.gitbook/assets/image (1) (4) (1).png" alt=""><figcaption></figcaption></figure>

### 圖表種類

資料可以用不同的圖表來呈現，如下圖

<figure><img src="../.gitbook/assets/image (3) (3).png" alt=""><figcaption></figcaption></figure>

* 矩形圖： 一個2D的矩形（x-y）圖表。
* 堆疊矩形圖： 這個選項將每個跡線放入其自己的2D矩形圖中，並堆疊每個圖，而不是在同一個圖上疊加跡線。
* 3D矩形圖： 一個3D的矩形（x-y-z）圖表。
* 3D矩形條狀圖： 一個3D的矩形條狀圖。
* 矩形輪廓圖： 一個矩形（x-y-z）圖表。輪廓圖對於視覺化表面（例如，phi/theta的直射性功能）非常有用。
* 極座標圖： 一個由球面座標劃分的2D圓形圖表。
* 3D極座標圖： 一個由球面座標劃分的3D圓形圖表。
* 3D球面圖： 一個3D的圓形圖，其中圖的半徑（rho）在所有點上都是均勻的，並且等於每個（theta, phi）點的所有rho的最大值。
* Smith圖： 一個繪有S參數的2D極座標圖，在其上叠加了標準化阻抗網格。
* Smith輪廓圖： 一個極座標圖。輪廓圖對於視覺化表面非常有用。
* 數據表： 一個以數字形式顯示選定量與掃描變量或其他量對照的行和列的網格。
* 輻射模式： 一個輻射場的2D極座標圖。

### Traces

選定Report及圖表之後，接下來就是要在圖表當中加入要檢視的資料。資料依照類別(Category)選擇對應之物理量(Quantity)，接著用函數(Function)處理該物理量。

<figure><img src="../.gitbook/assets/image (6) (3).png" alt=""><figcaption></figcaption></figure>

### 圖表格式

<figure><img src="../.gitbook/assets/image (20).png" alt=""><figcaption></figcaption></figure>

### 資料匯出

圖表可以輸出圖片檔(PNG、JPG)或資料檔(CSV、TSV)檔等。資料檔可以用EXCEL或程式加以處理。以下為匯出檔案格式：

<figure><img src="../.gitbook/assets/image (2) (3).png" alt=""><figcaption></figcaption></figure>

