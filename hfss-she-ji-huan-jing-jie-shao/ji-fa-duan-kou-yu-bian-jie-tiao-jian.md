# 激發與端口

### Excitation(激發)

大致上可以分成以下三類

* Port:可以用來計算網路模型(S, Y, Z)
* Field:近場或遠場或磁偏
* Source:電壓源/電流源

### Port(端口)

|              | Modal | Terminal |
| ------------ | :---: | :------: |
| Wave Port    |   V   |     V    |
| Lumped Port  |   V   |     V    |
| Circuit Port |   V   |     V    |
| FLoquet Port |   V   |          |

### Wave Port設定

計算輸入面當中的穩定電磁場分佈並以此電磁場作為激發，主要用在傳輸線截面上面，另一端必須為PEC邊界或PEC金屬塊。可以做deembed來移除或增加特定傳輸線長度。

### Lumped Port設定

直接以電壓激發結構，主要用在電阻，電容或電感等元件上面，會激發多個模態，正負端不可以穿越其他金屬結構。

### Circuit Port設定

類似Lumped Port，直接點選正負端邊緣即可設置，正負端之間可以穿過其他金屬結構。

### FLoquet Port

主要用於無限週期結構計算，如FSS等。
