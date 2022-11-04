---
description: 讓設計更彈性
---

# 設計變數

### 變數的目的

1. 透過變數來設定模型的尺寸、角度、位移等。之後修改會容易許多。
2. 多個物件屬性可以透過變數一次完成修改。
3. 變數可以搭配Sweep、Optimization來優化設計。

### 專案變數與設計變數

AEDT的變數分成兩大類，Project層級的變數在project當中所有的設計都可以參考到，以$開頭，比方說$dx。design層級的變數只有該design可以參考到，不影響其他design。兩者設定方式類似。一旦設定完成之後，便可以在屬性視窗加以修改。

![](<../.gitbook/assets/image (5).png>)

![](<../.gitbook/assets/image (1) (1).png>)

{% hint style="warning" %}
使用中的變數無法刪除，需先找到使用該變數的欄位，將該變數移除之後才能刪除該變數。
{% endhint %}

### 變數型態

變數數值可以是數值、數值陣列或是由其他變數組成的表示式

### 將物件屬性改為變數

如果該變數已存在，物件會立即更改該屬性。如果輸入的為新變數，則會跳出Add Variable視窗讓使用者可以即時加入所需的變數。

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>
