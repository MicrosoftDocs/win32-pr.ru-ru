---
title: dcl_sampler (SM4-ASM)
description: дклный \_ образец (SM4-ASM)
ms.assetid: 285a47fa-2d47-4ba9-90b9-3f4c61d5dce1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 86e0e04558c9ca1c10f89e924605c8999a7f7346d2278850d7cd6449968fd13c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118515543"
---
# <a name="dcl_sampler-sm4---asm"></a>дклный \_ образец (SM4-ASM)

Объявляет регистр образца.



| дклный \_ образец, режим |
|-----------------------|



 



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
<td><span id="sN"></span><span id="sn"></span><span id="SN"></span>с<em>N</em><br/></td>
<td>окне Регистр образцов, где <em>N</em> — это целое число, которое обозначает номер регистра.<br/></td>
</tr>
<tr class="even">
<td><span id="mode"></span><span id="MODE"></span><em>режима</em><br/></td>
<td>окне Режим выборки, который ограничивает количество состояний образца (перечисленных в элементах <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_sampler_desc"><strong>D3D10_SAMPLER_DESC</strong></a>). Режимы и состояния перечислены в следующей таблице.<br/> 
<table>
<thead>
<tr class="header">
<th>Режим</th>
<th>Принятые состояния образца</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>default</td>
<td><em>Filter</em> (может не использовать значения _COMPARISON или _TEXT), <em>аддрессу/V/W</em>, <em>минлод/макслод</em>, <em>миплодбиас</em>, <em>максанисотропи</em>, <em>BorderColor [4]</em></td>
</tr>
<tr class="even">
<td>сравнение</td>
<td><em>Filter</em>, <em>компарисонфунктион</em>, <em>аддрессу/V/W</em>, <em>минлод, макслод</em>, <em>миплодбиас</em>, <em>максанисотропи</em>, <em>BorderColor [4]</em></td>
</tr>
<tr class="odd">
<td>одним</td>
<td><em>Фильтр</em> (должен быть одним из значений _TEXT), <em>монофилтервидс</em>, <em>монофилтерхеигхт</em> (эти два состояния имеют глобальное состояние устройства), <em>минлод</em>, <em>миплодбиас</em>, <em>максанисотропи</em></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

Режим позволяет ограничивать примеры инструкций, которые можно использовать. в этой таблице перечислены методы объекта-текстуры, которые поддерживаются для каждого режима.



| Образец работы с образцом в этом режиме | Может использовать эти Texture-Object методы                                                                                                           |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| default                          | [Sample](dx-graphics-hlsl-to-sample.md), [самплелевел](dx-graphics-hlsl-to-samplelevel.md), [самплеград](dx-graphics-hlsl-to-samplegrad.md) |
| сравнение                       | [Самплекмп](dx-graphics-hlsl-to-samplecmp.md), [самплекмплевелзеро](dx-graphics-hlsl-to-samplecmplevelzero.md)                               |
| одним                             | [SampleLevel](dx-graphics-hlsl-to-samplelevel.md)                                                                                             |



 

Эта инструкция применяется к следующим этапам шейдера:



| Вершинный построитель текстуры | Шейдер геометрии | Построитель текстуры |
|---------------|-----------------|--------------|
| x             | x               | x\*          |



 

\* — Использование образца в режиме Mono поддерживается только в шейдере пикселей.

Эта инструкция включена для облегчения отладки шейдера в сборке; нельзя создать шейдер на языке ассемблера с использованием модели шейдеров 4.

## <a name="example"></a>Пример

Ниже приведен пример.


```
dcl_sampler s3, default
```



## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| Модель шейдера                                              | Поддерживается |
|-----------------------------------------------------------|-----------|
| [Модель шейдера 5](d3d11-graphics-reference-sm5.md)        | Да       |
| [Модель шейдера 4,1](dx-graphics-hlsl-sm4.md)              | Да       |
| [Модель шейдера 4](dx-graphics-hlsl-sm4.md)                | Да       |
| [Модель шейдера 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Нет        |
| [Модель шейдера 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Нет        |
| [Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Нет        |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Сборка Shader Model 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

