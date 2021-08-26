---
title: Сбор данных (объект текстуры DirectX HLSL)
description: Получает четыре образца (только красный компонент), которые будут использоваться для интерполяции билинейной при выборке текстуры.
ms.assetid: a394d8c2-99cc-4a38-9ac9-34afc666ebe0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bf364bc9d8feac199235319639ab5be8b851de4b
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626960"
---
# <a name="gather-directx-hlsl-texture-object"></a>Сбор данных (объект текстуры DirectX HLSL)

Получает четыре образца (только красный компонент), которые будут использоваться для интерполяции билинейной при выборке текстуры.

&lt;Тип шаблона &gt; 4 Object. сбор данных (образец \_ состояния, \| Расположение float2 3 \| 4 \[ , смещение int2 \] );



 

## <a name="parameters"></a>Параметры



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Элемент</th>
<th>Описание:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Объектами</em><br/></td>
<td>Поддерживаются следующие типы <a href="dx-graphics-hlsl-to-type.md">объектов текстуры</a> : Texture2D, Texture2DArray, Текстурекубе, текстурекубеаррай.<br/></td>
</tr>
<tr class="even">
<td><span id="S"></span><span id="s"></span><em>#D0</em><br/></td>
<td>окне <a href="dx-graphics-hlsl-sampler.md">Состояние образца</a>. Это объект, объявленный в файле эффектов, который содержит назначения состояний.<br/></td>
</tr>
<tr class="odd">
<td><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Места</em><br/></td>
<td>окне Координаты текстуры. Тип аргумента зависит от типа объекта текстуры. <br/> 
<table>
<thead>
<tr class="header">
<th>Тип Texture-Object</th>
<th>Тип параметра</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Texture2D</td>
<td>float2</td>
</tr>
<tr class="even">
<td>Texture2DArray, Текстурекубе</td>
<td>float3</td>
</tr>
<tr class="odd">
<td>текстурекубеаррай </td>
<td>float4</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Собой</em></p></td>
<td><p>окне Необязательное Смещение координаты текстуры, которое может использоваться для любого типа объекта текстуры. смещение применяется к расположению перед выборкой. Тип аргумента зависит от типа объекта текстуры. Для шейдеров, предназначенных для Shader Model 5,0 и более поздних версий, 6 наименее значимых битов каждого значения смещения учитываются как значение со знаком, а возвращает диапазон [-32.. 31]. Для предыдущих шейдеров модели шейдера смещения должны быть прямыми целыми числами от-8 до 7.</p>

<table>
<thead>
<tr class="header">
<th>Тип Texture-Object</th>
<th>Тип параметра</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Texture2D, Texture2DArray</td>
<td>int2</td>
</tr>
<tr class="even">
<td>Текстурекубе, Текстурекубеаррай </td>
<td>Не поддерживается</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a>Возвращаемое значение

Вектор из четырех компонентов с четырьмя компонентами Красного типа данных, тип которых совпадает с типом шаблона текстуры.

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| VS \_ 4 \_ 0 | VS \_ 4 \_ 1  | PS \_ 4 \_ 0 | PS \_ 4 \_ 1  | GS \_ 4 \_ 0 | GS \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
|          | x         |          | x         |          | x         |



 

1.  Текстурекубеаррай доступен в модели шейдеров 4,1 или более поздней версии.
2.  Модель шейдеров 4,1 доступна в Direct3D 10,1 или более поздней версии.

## <a name="example"></a>Пример


```
Texture2D<int1> Tex2d;
Texture2DArray<int2> Tex2dArray;
TextureCube<int3> TexCube;
TextureCubeArray<float2> TexCubeArray;

SamplerState s;

int4 main (float4 f : SV_Position) : SV_Target
{
    int2 iOffset = int2(2,3);

    int4 i1 = Tex2d.Gather(s, f.xy);
    int4 i2 = Tex2d.Gather(s, f.xy, iOffset);

    int4 i3 = Tex2dArray.Gather(s, f.xyz);
    int4 i4 = Tex2dArray.Gather(s, f.xyz, iOffset);

    int4 i5 = TexCube.Gather(s, f.xyzw);

    float4 f6 = TexCubeArray.Gather(s, f.xyzw);

    return i1+i2+i3+i4+i5+int4(i6);
}
  
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Текстура-объект](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





