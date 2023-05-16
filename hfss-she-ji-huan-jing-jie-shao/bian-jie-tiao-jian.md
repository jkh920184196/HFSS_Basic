---
description: 用來模擬實際世界中的物理情況
---

# 邊界條件

### Boundary分類

開放型邊界條件：

1. **Radiation**：這種邊界條件模擬了波動從模型邊界自由地傳播出去的情況。這種邊界條件常常被用於模擬天線或其他輻射結構。
2. **FEBI (Finite Element Boundary Integral)**：這種邊界條件是對於輻射邊界條件的一種改進，可以用於處理物體與無窮大區域的相互作用。
3. **PML (Perfectly Matched Layer)**：PML是一種吸收邊界條件，用於模擬波動從模型邊界出去並被完全吸收，不會反射回來的情況。

封閉型邊界條件：

1. **PEC (Perfect Electric Conductor)**：這種邊界條件假定邊界是一個完美的電導體，電場在此處為零。
2. **PMC (Perfect Magnetic Conductor)**：這種邊界條件假定邊界是一個完美的磁導體，磁場在此處為零。
3. **Impedance**：這種邊界條件將邊界視為一個具有特定阻抗的表面，使得電場和磁場的比值為一個固定的值。
4. **Layered Impedance**：這種邊界條件是一種擴展的阻抗邊界條件，可以模擬多層具有不同阻抗的介質。

{% hint style="info" %}
HFSS預設模擬邊界為封閉型，即所有模型接觸背景的面皆默認為PEC。
{% endhint %}

### 開放型邊界
