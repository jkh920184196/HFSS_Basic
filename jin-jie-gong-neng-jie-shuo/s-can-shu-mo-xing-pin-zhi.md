---
description: 當S參數要用在Transient模擬當中時，除了頻寬必須足夠，還需要注意到S參數品質
---

# 被動元件S參數模型品質

S參數（Scattering Parameters）是高頻電路設計和分析中的核心概念，能夠描述電路元件在不同頻率下的反應。為確保S參數模型的品質和準確性，我們需要確認模型滿足以下的物理特性：

1. 被動性（Passivity）：被動性意味著系統無法生成能量，只能消耗或儲存能量。
2. 因果性（Causality）：因果性代表系統的反應只能由過去或現在的輸入所引發，不會被未來的輸入所引發。在S參數模型中，我們可以透過檢查S參數是否符合Kramers-Kronig關係來驗證其因果性。
3. 對稱性（Reciprocity）：對稱性代表系統的反應並不會因為輸入和輸出的交換而改變。在電路中，這意味著電路是雙向的，且在任何方向上的信號傳輸都是相同的。在S參數模型中，我們可以透過檢查S參數矩陣是否為對稱矩陣（也就是Sij = Sji）來驗證其對稱性。

{% hint style="info" %}
對於信號完整性的模擬，我們需要確保描述的模型是因果的，並使用適當的模型來描述導體的高頻行為。Djordjevic-Sarkar模型就是這樣的一種模型，它能夠提供對於導體在高頻情況下行為的準確描述，從而有助於對信號完整性的模擬和分析。
{% endhint %}

### 因果性問題解決

HFSS模擬出來的S參數較常會遇到的是因果性問題，基本上注意以下設定便可以消除此問題

* Automatically use causal materials打勾(圖一)

<figure><img src="../.gitbook/assets/image (26).png" alt=""><figcaption></figcaption></figure>

* 採用三段掃頻方式([https://www.oldfriend.url.tw/SIwave/ansys\_ch\_divergent.html](https://www.oldfriend.url.tw/SIwave/ansys\_ch\_divergent.html))

<figure><img src="../.gitbook/assets/image (27).png" alt=""><figcaption></figcaption></figure>
