---
title: dcl_input_sv (SM4-ASM)
description: дкл \_ входной \_ ОКП (SM4-ASM)
ms.assetid: 59270148-e2eb-4525-a888-ad7e843d62a5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 650196dff224259f48d1471f3005f95ec0de9c8b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103785022"
---
# <a name="dcl_input_sv-sm4---asm"></a>дкл \_ входной \_ ОКП (SM4-ASM)

Объявляет входной регистр шейдера, который ждет, что [системное значение](dx-graphics-hlsl-semantics.md) должно быть предоставлено из предыдущего этапа.



| дкл \_ входной \_ ОКП v *N \[ . Mask \]*, *системвалуенаме \[ , интерполатионмоде \]* |
|------------------------------------------------------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Элемент</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="vN_.mask_"></span><span id="vn_.mask_"></span><span id="VN_.MASK_"></span>v<em>N [. Маска]</em><br/></td>
<td>окне Регистр данных вершин. <br/>
<ul>
<li><em>N</em> — это целое число, определяющее номер регистра.</li>
<li><em>[. Mask]</em> — это необязательная маска компонента (. ксизв), указывающая, какие компоненты регистров следует использовать.</li>
</ul></td>
</tr>
<tr class="even">
<td><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span><em>системвалуенаме</em><br/></td>
<td>окне Имя системного значения, являющееся строкой (см. раздел <a href="dx-graphics-hlsl-semantics.md">семантика системного значения</a>) без &quot; &quot; префикса SV_.<br/></td>
</tr>
<tr class="odd">
<td><span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>интерполатионмоде</em><br/></td>
<td>[в] Необязательно. Режим интерполяции, который влияет на способ вычисления значений во время растрирования; режим используется только в шейдере пикселей. Может иметь одно из следующих значений. <br/>
<ul>
<li>Константа — не выполнять интерполяцию между значениями регистров.</li>
<li>линейная — линейная интерполяция между значениями регистра.</li>
<li>Линеарцентроид — то же, что и линейный, но центроид при множественной выборке.</li>
<li>Линеарноперспективе — то же, что и линейная, но без исправления перспективы.</li>
<li>Линеарноперспективецентроид — то же, что и линейная, но без изменений перспективы и центроид при множественной выборки.</li>
</ul></td>
</tr>
</tbody>
</table>



 

Маска компонента для объявления системного значения может быть любым подмножеством \[ ксизв \] ; объявления не могут перекрываться (каждое объявление должно следовать за последовательностью ксизв). При объявлении скалярных системных значений (например, расстояния обрезки и расстояния для отбора) можно объявить несколько системных значений в одном регистре. В этом случае убедитесь, что другие модификаторы, такие как режимы интерполяции, совпадают.

Эта инструкция применяется к следующим этапам шейдера:



| Вершинный построитель текстуры | Шейдер геометрии | Построитель текстуры |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Эта инструкция включена для облегчения отладки шейдера в сборке; нельзя создать шейдер на языке ассемблера с использованием модели шейдеров 4.

## <a name="example"></a>Например, .

Ниже приводится несколько примеров.


```
// valid
dcl_input v0.y, linear
dcl_input_sv v0.w, clipDistance
dcl_input_sv v0.z, cullDistance
```




```
// invalid declarations
dcl_input v0.y, linear
dcl_input_sv v0.x, clipDistance  // the y component was previously declared, this declaration must use 
                                 // either the z or w component

dcl_input v0.y, linearNoPerspective                  // the interpolation mode is linear-no-perspective
dcl_input_sv v0.z, renderTargetArrayIndex, constant  // the interpolation modes is constant
                                                     // the interpolation modes must match
```



## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| Модель шейдера                                              | Поддерживается |
|-----------------------------------------------------------|-----------|
| [Модель шейдера 5](d3d11-graphics-reference-sm5.md)        | да       |
| [Модель шейдера 4,1](dx-graphics-hlsl-sm4.md)              | да       |
| [Модель шейдера 4](dx-graphics-hlsl-sm4.md)                | да       |
| [Модель шейдера 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Нет        |
| [Модель шейдера 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Нет        |
| [Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Нет        |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Сборка Shader Model 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





