---
description: HFSS 提供兩種網格生成器來生成初始網格：Tau 和 Classic 網格生成器。
---

# 初始化網格

Classic 網格生成器使用 Bowyer 算法創建具有非常大長度尺度的模型的緊湊網格。它能非常準確地表示模型。

Tau 網格生成器生成的網格品質非常高。它使用體積分解方法創建初始網格並使其粗化以達到小元素數量。它具有適應性放鬆公差以克服輸入模型中的不準確性和不對齊。這種運行模式被稱為 Tau 寬容。另一種版本被稱為 Tau 嚴格。

兩種網格生成器都被設計成可以處理所有幾何體。然而，如果您選擇 Auto，HFSS 將根據對幾何形狀的分析選擇 Classic 或 Tau 網格生成器。您可以覆蓋此選擇，選擇 Classic 或 Tau 來創建初始網格。根據模型的不同，有時 Classic 可以使用更少的資源收斂，而 Tau 可能會更快收斂。

無論選擇哪種網格，收斂的結果都是準確的。Ansys 建議選擇 Auto，因為 HFSS 會自動確定給定幾何形狀的網格生成器的正確選擇。

<figure><img src="../.gitbook/assets/image (2) (3) (1) (1).png" alt=""><figcaption></figcaption></figure>

### 物件網格

如果使用者事先知道哪一部分的網格需要較密集，可以在模擬之前手動針對該處設定較密集的網格，如此可以縮短網格迭代進一步降低模擬時間。
