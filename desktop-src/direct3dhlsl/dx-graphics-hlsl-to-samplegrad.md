---
title: Самплеград (объект текстуры DirectX HLSL)
description: Выбор текстуры с помощью градиента, чтобы повлиять на способ вычисления расположения образца. | Самплеград (объект текстуры DirectX HLSL)
ms.assetid: f3d73296-23c4-4178-b89e-6f84cfcb48a5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 236c453f3636452cbba8ed6000b2416e5187898d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273444"
---
# <a name="samplegrad-directx-hlsl-texture-object"></a>Самплеград (объект текстуры DirectX HLSL)

Выбор текстуры с помощью градиента, чтобы повлиять на способ вычисления расположения образца.



|                                                                                                            |
|------------------------------------------------------------------------------------------------------------|
| &lt;Тип шаблона &gt; Object. самплеград (выборка \_ состояния, расположение с плавающей точкой, Обмен плавающей запятой, ДДИ с плавающей запятой, \[ смещение int \] ); |



 

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
<tr class="odd">
<td>Texture2DMS, Texture2DMSArray</td>
<td>не поддерживается</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span id="DDX"></span><span id="ddx"></span><em>DDX</em></p></td>
<td><p>окне Интенсивность изменения геометрии поверхности в направлении x. Тип аргумента зависит от типа объекта текстуры.</p>

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
<td>FLOAT</td>
</tr>
<tr class="even">
<td>Texture2D, Texture2DArray</td>
<td>float2</td>
</tr>
<tr class="odd">
<td>Texture3D, Текстурекубе, Текстурекубеаррай </td>
<td>float3</td>
</tr>
<tr class="even">
<td>Texture2DMS, Texture2DMSArray</td>
<td>не поддерживается</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><p><span id="DDY"></span><span id="ddy"></span><em>дди</em></p></td>
<td><p>окне Интенсивность изменения геометрии поверхности в направлении y. Тип аргумента зависит от типа объекта текстуры.</p>

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
<td>FLOAT</td>
</tr>
<tr class="even">
<td>Texture2D, Texture2DArray</td>
<td>float2</td>
</tr>
<tr class="odd">
<td>Texture3D, Текстурекубе, Текстурекубеаррай </td>
<td>float3</td>
</tr>
<tr class="even">
<td>Texture2DMS, Texture2DMSArray</td>
<td>не поддерживается</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Собой</em></p></td>
<td><p>окне Необязательное Смещение координаты текстуры, которое может использоваться для любых типов объектов текстуры. Смещение применяется к расположению перед выборкой. Используйте смещение только с целочисленным миплевел; в противном случае можно получить результаты, которые не могут быть правильно преобразованы в оборудование. Тип аргумента зависит от типа объекта текстуры. Дополнительные сведения см. в разделе<a href="dx-graphics-hlsl-to-sample.md">применение целочисленных смещений</a>.</p>

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
<tr class="odd">
<td>Texture2DMS, Texture2DMSArray</td>
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
| x        | x         | x        | x         | x        | x         |



 

1.  Текстурекубеаррай доступен в модели шейдеров 4,1 или более поздней версии.
2.  Модель шейдеров 4,1 доступна в Direct3D 10,1 или более поздней версии.

## <a name="example"></a>Например, .

Этот частичный пример кода относится к файлу Мотионблур. FX в [примере MotionBlur10](https://msdn.microsoft.com/library/Ee416417(v=VS.85).aspx).


```
// Object Declarations
Texture2D g_txDiffuse;

SamplerState g_samLinear
{
    Filter = ANISOTROPIC;
    MaxAnisotropy = 8;
    AddressU = Wrap;
    AddressV = Wrap;
};

struct VSSceneOut
{
    float4 Pos : SV_POSITION;
    float4 Color : COLOR0;
    float2 Tex : TEXCOORD;
    float2 Aniso : ANISOTROPY;
};

float4 PSSceneMain( VSSceneOut Input ) : SV_TARGET
{
    float2 ddx = Input.Aniso;
    float2 ddy = Input.Aniso;
    
    // Shader body calling the intrinsic function
    float4 diff = g_txDiffuse.SampleGrad( g_samLinear, Input.Tex, ddx, ddy);
    
    ...
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Текстура-объект](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

