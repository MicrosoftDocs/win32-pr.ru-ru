---
title: Самплелевел (объект текстуры DirectX HLSL)
description: Выбор текстуры с помощью смещения на уровне mipmap.
ms.assetid: d61426c8-e09f-4e88-99f6-fa96c4a2b58d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4249d094f142af8a9015f4e8a3b32d4e39cd42fb
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122629557"
---
# <a name="samplelevel-directx-hlsl-texture-object"></a>Самплелевел (объект текстуры DirectX HLSL)

Выбор текстуры с помощью смещения на уровне mipmap.

&lt;Тип шаблона &gt; Object. самплелевел (образец \_ состояния, расположение с плавающей запятой, Лод float \[ , смещение int \] );



 

Эта функция аналогична [образцу](dx-graphics-hlsl-to-sample.md) , за исключением того, что она использует уровень Лод (в последнем компоненте параметра location) для выбора уровня mipmap. Например, двухмерная текстура использует первые два компонента для UV-координат и третий компонент для уровня mipmap.

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

<p> </p>
<p>Если объект текстуры является массивом, последний компонент является индексом массива.</p></td>
</tr>
<tr class="even">
<td><p><span id="LOD"></span><span id="lod"></span><em>лод</em></p></td>
<td><p>окне Число, указывающее уровень mipmap. Если значение равно 0, используется зеро'с (самая большая схема). Дробное значение (если оно указано) используется для интерполяции между двумя уровнями mipmap.</p></td>
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
<td>Не поддерживается</td>
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
| x        | x         | x        | x         | x        | x         |



 

1.  Текстурекубеаррай доступен в модели шейдеров 4,1 или более поздней версии.
2.  Модель шейдеров 4,1 доступна в Direct3D 10,1 или более поздней версии.

## <a name="example"></a>Пример

Этот частичный пример кода находится в файле с расширением. FX в [образце Instancing10](https://msdn.microsoft.com/library/Ee416415(v=VS.85).aspx).


```
// Object Declarations
Texture1D g_txRandom;

SamplerState g_samPoint
{
    Filter = MIN_MAG_MIP_POINT;
    AddressU = Wrap;
    AddressV = Wrap;
};

    
// Shader body calling the intrinsic function
float3 RandomDir(float fOffset)
{   
    float tCoord = (fOffset) / 300.0;
    return g_txRandom.SampleLevel( g_samPoint, tCoord, 0 );
   ...

```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Текстура-объект](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

