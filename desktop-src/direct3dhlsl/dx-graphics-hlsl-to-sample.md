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
ms.openlocfilehash: ec80d296025684c1bb67642661a31d8cdc119a53
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998015"
---
# <a name="sample-directx-hlsl-texture-object"></a><span data-ttu-id="ef70e-104">Пример (объект текстуры HLSL DirectX)</span><span class="sxs-lookup"><span data-stu-id="ef70e-104">Sample (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="ef70e-105">Выбор текстуры.</span><span class="sxs-lookup"><span data-stu-id="ef70e-105">Samples a texture.</span></span>

|                                                                                  |
|----------------------------------------------------------------------------------|
| <span data-ttu-id="ef70e-106">&lt;Тип шаблона &gt; Object. Sample ( \_ состояние образца, расположение float \[ , смещение int \] );</span><span class="sxs-lookup"><span data-stu-id="ef70e-106">&lt;Template Type&gt; Object.Sample( sampler\_state S, float Location \[, int Offset\] );</span></span> |

## <a name="parameters"></a><span data-ttu-id="ef70e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ef70e-107">Parameters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ef70e-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="ef70e-108">Item</span></span></th>
<th><span data-ttu-id="ef70e-109">Описание</span><span class="sxs-lookup"><span data-stu-id="ef70e-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ef70e-110"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Объектами</em></span><span class="sxs-lookup"><span data-stu-id="ef70e-110"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="ef70e-111">Любой тип <a href="dx-graphics-hlsl-to-type.md">объекта текстуры</a> (кроме Texture2DMS и Texture2DMSArray).</span><span class="sxs-lookup"><span data-stu-id="ef70e-111">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ef70e-112"><span id="S"></span><span id="s"></span><em>#D0</em></span><span class="sxs-lookup"><span data-stu-id="ef70e-112"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="ef70e-113">окне <a href="dx-graphics-hlsl-sampler.md">Состояние образца</a>.</span><span class="sxs-lookup"><span data-stu-id="ef70e-113">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="ef70e-114">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="ef70e-114">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ef70e-115"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Места</em></span><span class="sxs-lookup"><span data-stu-id="ef70e-115"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="ef70e-116">окне Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="ef70e-116">[in] The texture coordinates.</span></span> <span data-ttu-id="ef70e-117">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="ef70e-117">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ef70e-118">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="ef70e-118">Texture-Object Type</span></span></th>
<th><span data-ttu-id="ef70e-119">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="ef70e-119">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ef70e-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="ef70e-120">Texture1D</span></span></td>
<td><span data-ttu-id="ef70e-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ef70e-121">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ef70e-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="ef70e-122">Texture1DArray, Texture2D</span></span></td>
<td><span data-ttu-id="ef70e-123">float2</span><span class="sxs-lookup"><span data-stu-id="ef70e-123">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ef70e-124">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="ef70e-124">Texture2DArray, Texture3D, TextureCube</span></span></td>
<td><span data-ttu-id="ef70e-125">float3</span><span class="sxs-lookup"><span data-stu-id="ef70e-125">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ef70e-126">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="ef70e-126">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="ef70e-127">float4</span><span class="sxs-lookup"><span data-stu-id="ef70e-127">float4</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ef70e-128"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Собой</em></span><span class="sxs-lookup"><span data-stu-id="ef70e-128"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="ef70e-129">окне Необязательное Смещение координаты текстуры, которое может использоваться для любого типа объекта текстуры. смещение применяется к расположению перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="ef70e-129">[in] An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="ef70e-130">Смещение текстуры должно быть статическим.</span><span class="sxs-lookup"><span data-stu-id="ef70e-130">The texture offsets need to be static.</span></span> <span data-ttu-id="ef70e-131">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="ef70e-131">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="ef70e-132">Дополнительные сведения см. в разделе <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">применение смещения координат текстуры</a>.</span><span class="sxs-lookup"><span data-stu-id="ef70e-132">For more info, see <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Applying texture coordinate offsets</a>.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ef70e-133">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="ef70e-133">Texture-Object Type</span></span></th>
<th><span data-ttu-id="ef70e-134">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="ef70e-134">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ef70e-135">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="ef70e-135">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="ef70e-136">INT</span><span class="sxs-lookup"><span data-stu-id="ef70e-136">int</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ef70e-137">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="ef70e-137">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="ef70e-138">int2</span><span class="sxs-lookup"><span data-stu-id="ef70e-138">int2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ef70e-139">Texture3D</span><span class="sxs-lookup"><span data-stu-id="ef70e-139">Texture3D</span></span></td>
<td><span data-ttu-id="ef70e-140">int3</span><span class="sxs-lookup"><span data-stu-id="ef70e-140">int3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ef70e-141">Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="ef70e-141">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="ef70e-142">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ef70e-142">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>

## <a name="return-value"></a><span data-ttu-id="ef70e-143">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ef70e-143">Return value</span></span>

<span data-ttu-id="ef70e-144">Тип шаблона текстуры, который может быть вектором с одним или несколькими компонентами.</span><span class="sxs-lookup"><span data-stu-id="ef70e-144">The texture's template type, which may be a single- or multi-component vector.</span></span> <span data-ttu-id="ef70e-145">Формат основан на [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)в текстуре.</span><span class="sxs-lookup"><span data-stu-id="ef70e-145">The format is based on the texture's [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="ef70e-146">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ef70e-146">Minimum Shader Model</span></span>

<span data-ttu-id="ef70e-147">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="ef70e-147">This function is supported in the following shader models.</span></span>

| <span data-ttu-id="ef70e-148">VS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ef70e-148">vs\_4\_0</span></span> | <span data-ttu-id="ef70e-149">VS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="ef70e-149">vs\_4\_1</span></span>  | <span data-ttu-id="ef70e-150">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ef70e-150">ps\_4\_0</span></span> | <span data-ttu-id="ef70e-151">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="ef70e-151">ps\_4\_1</span></span>  | <span data-ttu-id="ef70e-152">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ef70e-152">gs\_4\_0</span></span> | <span data-ttu-id="ef70e-153">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="ef70e-153">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          |           | <span data-ttu-id="ef70e-154">x</span><span class="sxs-lookup"><span data-stu-id="ef70e-154">x</span></span>        | <span data-ttu-id="ef70e-155">x</span><span class="sxs-lookup"><span data-stu-id="ef70e-155">x</span></span>         |          |           |

1.  <span data-ttu-id="ef70e-156">Текстурекубеаррай доступен в модели шейдеров 4,1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="ef70e-156">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="ef70e-157">Модель шейдеров 4,1 доступна в Direct3D 10,1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="ef70e-157">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="example"></a><span data-ttu-id="ef70e-158">Например, .</span><span class="sxs-lookup"><span data-stu-id="ef70e-158">Example</span></span>

<span data-ttu-id="ef70e-159">Этот частичный пример кода основан на файле BasicHLSL11. FX в [примере BasicHLSL11](https://github.com/microsoftarchive/msdn-code-gallery-community-a-c/tree/master/Basic%20DXUT%20Win32%20Samples/%5BC%2B%2B%5D-Basic%20DXUT%20Win32%20Samples/C%2B%2B/BasicHLSL11).</span><span class="sxs-lookup"><span data-stu-id="ef70e-159">This partial code example is based on the BasicHLSL11.fx file in the [BasicHLSL11 Sample](https://github.com/microsoftarchive/msdn-code-gallery-community-a-c/tree/master/Basic%20DXUT%20Win32%20Samples/%5BC%2B%2B%5D-Basic%20DXUT%20Win32%20Samples/C%2B%2B/BasicHLSL11).</span></span>

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

## <a name="remarks"></a><span data-ttu-id="ef70e-160">Примечания</span><span class="sxs-lookup"><span data-stu-id="ef70e-160">Remarks</span></span>

<span data-ttu-id="ef70e-161">Выбор текстуры использует расположение шаг текселя для поиска значения шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="ef70e-161">Texture sampling uses the texel position to look up a texel value.</span></span> <span data-ttu-id="ef70e-162">Смещение можно применить к положению перед подстановкой.</span><span class="sxs-lookup"><span data-stu-id="ef70e-162">An offset can be applied to the position before lookup.</span></span> <span data-ttu-id="ef70e-163">Состояние образца содержит параметры выборки и фильтрации.</span><span class="sxs-lookup"><span data-stu-id="ef70e-163">The sampler state contains the sampling and filtering options.</span></span> <span data-ttu-id="ef70e-164">Этот метод может быть вызван в шейдере пикселей, но не поддерживается в шейдере вершин или шейдере Geometry.</span><span class="sxs-lookup"><span data-stu-id="ef70e-164">This method can be invoked within a pixel shader, but it is not supported in a vertex shader or a geometry shader.</span></span>

<span data-ttu-id="ef70e-165">Используйте смещение только с целочисленным миплевел; в противном случае вы можете получить разные результаты в зависимости от аппаратной реализации или параметров драйверов.</span><span class="sxs-lookup"><span data-stu-id="ef70e-165">Use an offset only at an integer miplevel; otherwise, you may get different results depending on hardware implementation or driver settings.</span></span>

### <a name="calculating-texel-positions"></a><span data-ttu-id="ef70e-166">Вычисление позиций шаг текселя</span><span class="sxs-lookup"><span data-stu-id="ef70e-166">Calculating texel positions</span></span>

<span data-ttu-id="ef70e-167">Координаты текстуры — это значения с плавающей запятой, которые ссылаются на данные текстуры, которые также называются нормализованной областью текстуры.</span><span class="sxs-lookup"><span data-stu-id="ef70e-167">Texture coordinates are floating-point values that reference texture data, which is also known as normalized texture space.</span></span> <span data-ttu-id="ef70e-168">Режимы переноса адреса применяются в этом порядке (координаты текстуры + смещения + режим переноса) для изменения координат текстуры за пределами \[ диапазона 0... 1 \] .</span><span class="sxs-lookup"><span data-stu-id="ef70e-168">Address wrapping modes are applied in this order (texture coordinates + offsets + wrap mode) to modify texture coordinates outside the \[0...1\] range.</span></span>

<span data-ttu-id="ef70e-169">Для массивов текстуры дополнительное значение параметра Location указывает индекс в массиве текстуры.</span><span class="sxs-lookup"><span data-stu-id="ef70e-169">For texture arrays, an additional value in the location parameter specifies an index into a texture array.</span></span> <span data-ttu-id="ef70e-170">Этот индекс рассматривается как масштабированное значение с плавающей запятой (вместо нормализованного пространства для стандартных координат текстуры).</span><span class="sxs-lookup"><span data-stu-id="ef70e-170">This index is treated as a scaled float value (instead of the normalized space for standard texture coordinates).</span></span> <span data-ttu-id="ef70e-171">Преобразование в целочисленный индекс выполняется в следующем порядке (float + Round-To-ближайшего-четного целое число + срез в диапазон массива).</span><span class="sxs-lookup"><span data-stu-id="ef70e-171">The conversion to an integer index is done in the following order (float + round-to-nearest-even integer + clamp to the array range).</span></span>

### <a name="applying-texture-coordinate-offsets"></a><span data-ttu-id="ef70e-172">Применение смещений для координат текстуры</span><span class="sxs-lookup"><span data-stu-id="ef70e-172">Applying texture coordinate offsets</span></span>

<span data-ttu-id="ef70e-173">Параметр offset изменяет координаты текстуры в шаг текселя пространстве.</span><span class="sxs-lookup"><span data-stu-id="ef70e-173">The offset parameter modifies the texture coordinates, in texel space.</span></span> <span data-ttu-id="ef70e-174">Несмотря на то, что координаты текстуры являются нормализованными числами с плавающей запятой, смещение применяет целочисленное смещение.</span><span class="sxs-lookup"><span data-stu-id="ef70e-174">Even though texture coordinates are normalized floating-point numbers, the offset applies an integer offset.</span></span> <span data-ttu-id="ef70e-175">Также обратите внимание, что смещение текстуры должно быть статическим.</span><span class="sxs-lookup"><span data-stu-id="ef70e-175">Also note that the texture offsets need to be static.</span></span>

<span data-ttu-id="ef70e-176">Возвращаемый формат данных определяется форматом текстуры.</span><span class="sxs-lookup"><span data-stu-id="ef70e-176">The data format returned is determined by the texture format.</span></span> <span data-ttu-id="ef70e-177">Например, если ресурс текстуры был определен в \_ \_ формате DXGI A8B8G8R8 \_ UNORM \_ sRGB, операция выборки преобразует пример пикселей текстуры из гаммы 2,0 в 1,0, отфильтрует и записывает результат в виде значения с плавающей запятой в диапазоне \[ 0.. 1 \] .</span><span class="sxs-lookup"><span data-stu-id="ef70e-177">For example, if the texture resource was defined with the DXGI\_FORMAT\_A8B8G8R8\_UNORM\_SRGB format, the sampling operation converts sampled texels from gamma 2.0 to 1.0, filter, and writes the result as a floating-point value in the range \[0..1\].</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef70e-178">См. также</span><span class="sxs-lookup"><span data-stu-id="ef70e-178">Related topics</span></span>

[<span data-ttu-id="ef70e-179">Текстура-объект</span><span class="sxs-lookup"><span data-stu-id="ef70e-179">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
