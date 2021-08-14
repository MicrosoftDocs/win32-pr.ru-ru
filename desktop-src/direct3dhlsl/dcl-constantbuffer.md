---
title: dcl_constantBuffer (SM4-ASM)
description: дкл \_ константбуффер (SM4-ASM)
ms.assetid: 164fb2a4-8782-42f0-b4ba-1f87d9c7255d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 437266c5a37f266a4f8847f09719380f436b6d9d38e8dee21b3258c79adb32b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117727268"
---
# <a name="dcl_constantbuffer-sm4---asm"></a>дкл \_ константбуффер (SM4-ASM)

Объявляет константный буфер шейдера.



| дкл \_ константбуффер *КБН \[ size \]*, *акцесспаттерн* |
|----------------------------------------------------|



 



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
<td><span id="cbN_size_"></span><span id="cbn_size_"></span><span id="CBN_SIZE_"></span>CB<em>N [размер]</em><br/></td>
<td>окне Буфер констант шейдера, где N — это целое число, которое обозначает номер регистра константы и размер — целое число, которое обозначает количество элементов в буфере.<br/></td>
</tr>
<tr class="even">
<td><span id="AccessPattern"></span><span id="accesspattern"></span><span id="ACCESSPATTERN"></span><em>акцесспаттерн</em><br/></td>
<td>окне Способ доступа к буферу по коду шейдера может быть одним из следующих: <br/> 
<table>
<thead>
<tr class="header">
<th>Имя</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>иммедиатеиндексед</td>
<td>Индексировать буфер с литеральным значением.</td>
</tr>
<tr class="even">
<td>dynamic_indexed</td>
<td>Индексировать буфер с результатом вычисленного выражения.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

Эта инструкция применяется к следующим этапам шейдера:



| Вершинный построитель текстуры | Шейдер геометрии | Построитель текстуры |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Эта инструкция включена для облегчения отладки шейдера в сборке; нельзя создать шейдер на языке ассемблера с использованием модели шейдеров 4.

## <a name="example"></a>Пример

В этом примере объявляется константный буфер для Register cB0, который содержит 19 элементов. Доступ к этим элементам осуществляется с помощью литерального индекса.


```
dcl_constantbuffer  cb0[19], immediateIndexed
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

 

 





