---
title: Дадд (SM5-ASM)
description: Добавление двойной точности с привязкум к компоненту.
ms.assetid: 416F1103-E27B-4AFC-9ED1-492FF8A93492
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e217a03a5ba9e4da0d365bbfd15e4283f1a69cb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412140"
---
# <a name="dadd-sm5---asm"></a>Дадд (SM5-ASM)

Добавление двойной точности с привязкум к компоненту.



| Дадд \[ \_ \] \[ . Маска \] , \[ - \] src0 \[ \_ ABS \] \[ . свиззле \] , \[ - \] src1 \[ \_ ABS \] \[ . свиззле\] |
|---------------------------------------------------------------------------------------------|



 



| Элемент                                                            | Описание                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[в \] адресе результата операции.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[в \] компонентах, добавляемых с помощью *src1*.<br/>          |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[в \] компонентах, добавляемых с помощью *src0*<br/>           |



 

## <a name="remarks"></a>Примечания

Допустимыми свиззлес для параметров источника являются. ксизв,. ксикси,. звкси,. звзв. Допустимые маски *приемников* : XY, ZW и. ксизв. Следующие сопоставления являются свиззле.

-   *dest* — это двойное vec2 в (x 32LSB, y 32MSB) и (z 32LSB, w 32MSB).
-   *src0* — это двойное vec2 в (x 32LSB, y 32MSB) и (z 32LSB, w 32MSB).
-   *src1* — это двойное vec2 в (x 32LSB, y 32MSB) и (z 32LSB, w 32MSB).

В следующей таблице показаны результаты, полученные при выполнении инструкции с различными классами чисел, предполагая, что ни переполнение, ни потеря точности не происходит.

F означает ограничение по настоящему вещественному числу.



<table>
<tbody>
<tr class="odd">
<td><dl> <strong>src0</strong><br />
<strong>src1 — ></strong><br />
</dl></td>
<td><strong>-INF</strong></td>
<td><strong>-F</strong></td>
<td><strong>-0</strong></td>
<td><strong>+0</strong></td>
<td><strong>+ F</strong></td>
<td><strong>+ INF</strong></td>
<td><strong>Не число</strong></td>
</tr>
<tr class="even">
<td><strong>-INF</strong></td>
<td>-inf</td>
<td>-inf</td>
<td>-inf</td>
<td>-inf</td>
<td>-inf</td>
<td>Не число</td>
<td>Не число</td>
</tr>
<tr class="odd">
<td><strong>-F</strong></td>
<td>-inf</td>
<td>-F</td>
<td>src0</td>
<td>src0</td>
<td>+-F или +-0</td>
<td>+inf</td>
<td>Не число</td>
</tr>
<tr class="even">
<td><strong>-0</strong></td>
<td>-inf</td>
<td>src1</td>
<td>-0</td>
<td>+0</td>
<td>src1</td>
<td>+inf</td>
<td>Не число</td>
</tr>
<tr class="odd">
<td><strong>+0</strong></td>
<td>-inf</td>
<td>src1</td>
<td>+0</td>
<td>+0</td>
<td>src1</td>
<td>+inf</td>
<td>не число</td>
</tr>
<tr class="even">
<td><strong>+ F</strong></td>
<td>-inf</td>
<td>+-F или +-0</td>
<td>src0</td>
<td>src0</td>
<td>+ F</td>
<td>+inf</td>
<td>не число</td>
</tr>
<tr class="odd">
<td><strong>+ INF</strong></td>
<td>не число</td>
<td>+inf</td>
<td>+inf</td>
<td>+inf</td>
<td>+inf</td>
<td>+inf</td>
<td>Не число</td>
</tr>
<tr class="even">
<td><strong>Не число</strong></td>
<td>Не число</td>
<td>Не число</td>
<td>Не число</td>
<td>Не число</td>
<td>Не число</td>
<td>Не число</td>
<td>Не число</td>
</tr>
</tbody>
</table>



 

Эта инструкция применяется к следующим этапам шейдера:



| Вершина | Поверхности | Домен | Геометрия | Пиксель | Вычисления |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта инструкция поддерживается в следующих моделях шейдеров:



| Модель шейдера                                              | Поддерживается |
|-----------------------------------------------------------|-----------|
| [Модель шейдера 5](d3d11-graphics-reference-sm5.md)        | да       |
| [Модель шейдера 4,1](dx-graphics-hlsl-sm4.md)              | Нет        |
| [Модель шейдера 4](dx-graphics-hlsl-sm4.md)                | Нет        |
| [Модель шейдера 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Нет        |
| [Модель шейдера 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Нет        |
| [Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Нет        |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Сборка Shader Model 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





