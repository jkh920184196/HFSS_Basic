---
description: HFSS 3D建模有特定的邏輯與規則
---

# 3D建模

### 單位

![](<../.gitbook/assets/image (2) (1) (2).png>)

### XY/YZ/ZX面

在HFSS或任何其他3D建模軟體中，這些平面可以用來定義對象的形狀和位置，並且可以用來創建2D的截面視圖。

![](<../.gitbook/assets/image (24).png>)

### 模型結構特性

可以分成Solids, Sheets, Lines及Point四大類

![](<../.gitbook/assets/image (1) (1) (1) (1).png>)

每一種結構包含不同幾何特性

| Type   | Object | Face | Edge | Vertex |
| ------ | :----: | :--: | :--: | :----: |
| Solids |    V   |   V  |   V  |    V   |
| Sheets |        |   V  |   V  |    V   |
| Lines  |        |      |   V  |    V   |
| Points |        |      |      |    V   |

### 鎖點

![](<../.gitbook/assets/image (5) (3).png>)

### 基礎模型建立及編輯

#### 模型移動與複製

![](<../.gitbook/assets/image (16).png>)

#### 布林運算

![](<../.gitbook/assets/image (22).png>)

**掃描**

![](<../.gitbook/assets/image (23).png>)

**導角**

![](<../.gitbook/assets/image (1).png>)

**線面運算**

### ![](<../.gitbook/assets/image (13).png>)

### 常用熱鍵

* 設計視圖最大化：Ctrl+D
* 放大縮小圖面：滾輪
* 旋轉圖面：按住滾輪移動滑鼠
* 切換視角：Alt+點選
* 框選：由左至右與由右至左不同
* 沿X(Y, Z)方向移動：按住X(Y, Z)鍵

