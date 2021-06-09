---
title: Самплебиас (объект текстуры DirectX HLSL)
description: Демонстрирует выбор текстуры после применения смещения входных данных к уровню mipmap.
ms.assetid: 1bc03ad8-7b69-4001-81c7-64d8c631d68d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 01087ab36bdbe90ff73643899229c7ec6ccfbdbe
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826799"
---
# <a name="samplebias-directx-hlsl-texture-object"></a>Самплебиас (объект текстуры DirectX HLSL)

Демонстрирует выбор текстуры после применения смещения входных данных к уровню mipmap.

&lt;Тип шаблона &gt; Object. самплебиас (выборка \_ состояния, расположение с плавающей точкой, смещение с плавающей запятой \[ , смещения int \] );



 

## <a name="parameters"></a>Параметры



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
<td><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Объектами</em><br/></td>
<td>Любой тип <a href="dx-graphics-hlsl-to-type.md">объекта текстуры</a> (кроме Texture2DMS и Texture2DMSArray).<br/></td>
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
<td>Texture1D</td>
<td>FLOAT</td>
</tr>
<tr class="even">
<td>Texture1DArray, Texture2D</td>
<td>float2</td>
</tr>
<tr class="odd">
<td>Texture2DArray, Texture3D, Текстурекубе</td>
<td>float3</td>
</tr>
<tr class="even">
<td>текстурекубеаррай </td>
<td>float4</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span id="Bias"></span><span id="bias"></span><span id="BIAS"></span><em>Часов</em></p></td>
<td><p>окне Значение смещения, которое является числом с плавающей запятой от-16,0 до 15,99, применяется к MIP уровню перед выборкой.</p></td>
</tr>
<tr class="odd">
<td><p><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Собой</em></p></td>
<td><p>окне Необязательное Смещение координаты текстуры, которое может использоваться для любого типа объекта текстуры. смещение применяется к расположению перед выборкой. Смещение текстуры должно быть статическим. Тип аргумента зависит от типа объекта текстуры. Дополнительные сведения см. в разделе <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">применение смещения координат текстуры</a>.</p>

<table>
<thead>
<tr class="header">
<th>Тип Texture-Object</th>
<th>Тип параметра</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Texture1D, Texture1DArray</td>
<td>INT</td>
</tr>
<tr class="even">
<td>Texture2D, Texture2DArray</td>
<td>int2</td>
</tr>
<tr class="odd">
<td>Texture3D</td>
<td>int3</td>
</tr>
<tr class="even">
<td>Текстурекубе, Текстурекубеаррай </td>
<td>не поддерживается</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a>Возвращаемое значение

Тип шаблона текстуры, который может быть вектором с одним или несколькими компонентами. Формат основан на [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)в текстуре.

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| VS \_ 4 \_ 0 | VS \_ 4 \_ 1  | PS \_ 4 \_ 0 | PS \_ 4 \_ 1  | GS \_ 4 \_ 0 | GS \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
|          |           | x        | x         |          |           |



 

1.  Текстурекубеаррай доступен в модели шейдеров 4,1 или более поздней версии.
2.  Модель шейдеров 4,1 доступна в Direct3D 10,1 или более поздней версии.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Текстура-объект](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

