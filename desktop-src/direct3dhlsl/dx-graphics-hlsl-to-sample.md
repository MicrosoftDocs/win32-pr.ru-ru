---
title: Пример (объект текстуры HLSL DirectX)
description: Выбор текстуры. | Образец (объект текстуры DirectX HLSL)
ms.assetid: 788ba4b4-8013-411f-9a19-fb9983386fa0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2374063d222d06576f720fed2aa7fb714bcccf04
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/09/2021
ms.locfileid: "111825751"
---
# <a name="sample-directx-hlsl-texture-object"></a>Пример (объект текстуры HLSL DirectX)

Выбор текстуры.

&lt;Тип шаблона &gt; Object. Sample ( \_ состояние образца, расположение float \[ , смещение int \] );

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

## <a name="example"></a>Пример

Этот частичный пример кода основан на файле BasicHLSL11. FX в [примере BasicHLSL11](https://github.com/microsoftarchive/msdn-code-gallery-community-a-c/tree/master/Basic%20DXUT%20Win32%20Samples/%5BC%2B%2B%5D-Basic%20DXUT%20Win32%20Samples/C%2B%2B/BasicHLSL11).

```
// Object Declarations
Texture2D g_MeshTexture;            // Color texture for mesh

SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};

struct VS_OUTPUT
{
    float4 Position   : SV_POSITION; // vertex position 
    float4 Diffuse    : COLOR0;      // vertex diffuse color (note that COLOR0 is clamped from 0..1)
    float2 TextureUV  : TEXCOORD0;   // vertex texture coords 
};

VS_OUTPUT In;

// Shader body calling the intrinsic function
   ...
        Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) * In.Diffuse;
```

## <a name="remarks"></a>Remarks

Выбор текстуры использует расположение шаг текселя для поиска значения шаг текселя. Смещение можно применить к положению перед подстановкой. Состояние образца содержит параметры выборки и фильтрации. Этот метод может быть вызван в шейдере пикселей, но не поддерживается в шейдере вершин или шейдере Geometry.

Используйте смещение только с целочисленным миплевел; в противном случае вы можете получить разные результаты в зависимости от аппаратной реализации или параметров драйверов.

### <a name="calculating-texel-positions"></a>Вычисление позиций шаг текселя

Координаты текстуры — это значения с плавающей запятой, которые ссылаются на данные текстуры, которые также называются нормализованной областью текстуры. Режимы переноса адреса применяются в этом порядке (координаты текстуры + смещения + режим переноса) для изменения координат текстуры за пределами \[ диапазона 0... 1 \] .

Для массивов текстуры дополнительное значение параметра Location указывает индекс в массиве текстуры. Этот индекс рассматривается как масштабированное значение с плавающей запятой (вместо нормализованного пространства для стандартных координат текстуры). Преобразование в целочисленный индекс выполняется в следующем порядке (float + Round-To-ближайшего-четного целое число + срез в диапазон массива).

### <a name="applying-texture-coordinate-offsets"></a>Применение смещений для координат текстуры

Параметр offset изменяет координаты текстуры в шаг текселя пространстве. Несмотря на то, что координаты текстуры являются нормализованными числами с плавающей запятой, смещение применяет целочисленное смещение. Также обратите внимание, что смещение текстуры должно быть статическим.

Возвращаемый формат данных определяется форматом текстуры. Например, если ресурс текстуры был определен в \_ \_ формате DXGI A8B8G8R8 \_ UNORM \_ sRGB, операция выборки преобразует пример пикселей текстуры из гаммы 2,0 в 1,0, отфильтрует и записывает результат в виде значения с плавающей запятой в диапазоне \[ 0.. 1 \] .

## <a name="related-topics"></a>Связанные темы

[Текстура-объект](dx-graphics-hlsl-to-type.md)
