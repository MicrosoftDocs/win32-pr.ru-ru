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
ms.openlocfilehash: bc3a074641ce5b15a3d837e8bd91dfdae09fe627
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826688"
---
# <a name="samplelevel-directx-hlsl-texture-object"></a><span data-ttu-id="b2306-103">Самплелевел (объект текстуры DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b2306-103">SampleLevel (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="b2306-104">Выбор текстуры с помощью смещения на уровне mipmap.</span><span class="sxs-lookup"><span data-stu-id="b2306-104">Samples a texture using a mipmap-level offset.</span></span>

<span data-ttu-id="b2306-105">&lt;Тип шаблона &gt; Object. самплелевел (образец \_ состояния, расположение с плавающей запятой, Лод float \[ , смещение int \] );</span><span class="sxs-lookup"><span data-stu-id="b2306-105">&lt;Template Type&gt; Object.SampleLevel( sampler\_state S, float Location, float LOD \[, int Offset\] );</span></span>



 

<span data-ttu-id="b2306-106">Эта функция аналогична [образцу](dx-graphics-hlsl-to-sample.md) , за исключением того, что она использует уровень Лод (в последнем компоненте параметра location) для выбора уровня mipmap.</span><span class="sxs-lookup"><span data-stu-id="b2306-106">This function is similar to [Sample](dx-graphics-hlsl-to-sample.md) except that it uses the LOD level (in the last component of the location parameter) to choose the mipmap level.</span></span> <span data-ttu-id="b2306-107">Например, двухмерная текстура использует первые два компонента для UV-координат и третий компонент для уровня mipmap.</span><span class="sxs-lookup"><span data-stu-id="b2306-107">For example, a 2D texture uses the first two components for uv coordinates and the third component for the mipmap level.</span></span>

## <a name="parameters"></a><span data-ttu-id="b2306-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b2306-108">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b2306-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="b2306-109">Item</span></span></th>
<th><span data-ttu-id="b2306-110">Описание</span><span class="sxs-lookup"><span data-stu-id="b2306-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b2306-111"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Объектами</em></span><span class="sxs-lookup"><span data-stu-id="b2306-111"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="b2306-112">Любой тип <a href="dx-graphics-hlsl-to-type.md">объекта текстуры</a> (кроме Texture2DMS и Texture2DMSArray).</span><span class="sxs-lookup"><span data-stu-id="b2306-112">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b2306-113"><span id="S"></span><span id="s"></span><em>#D0</em></span><span class="sxs-lookup"><span data-stu-id="b2306-113"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="b2306-114">окне <a href="dx-graphics-hlsl-sampler.md">Состояние образца</a>.</span><span class="sxs-lookup"><span data-stu-id="b2306-114">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="b2306-115">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="b2306-115">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b2306-116"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Места</em></span><span class="sxs-lookup"><span data-stu-id="b2306-116"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="b2306-117">окне Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="b2306-117">[in] The texture coordinates.</span></span> <span data-ttu-id="b2306-118">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="b2306-118">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b2306-119">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="b2306-119">Texture-Object Type</span></span></th>
<th><span data-ttu-id="b2306-120">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="b2306-120">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b2306-121">Texture1D</span><span class="sxs-lookup"><span data-stu-id="b2306-121">Texture1D</span></span></td>
<td><span data-ttu-id="b2306-122">FLOAT</span><span class="sxs-lookup"><span data-stu-id="b2306-122">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b2306-123">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="b2306-123">Texture1DArray, Texture2D</span></span></td>
<td><span data-ttu-id="b2306-124">float2</span><span class="sxs-lookup"><span data-stu-id="b2306-124">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b2306-125">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="b2306-125">Texture2DArray, Texture3D, TextureCube</span></span></td>
<td><span data-ttu-id="b2306-126">float3</span><span class="sxs-lookup"><span data-stu-id="b2306-126">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b2306-127">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="b2306-127">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="b2306-128">float4</span><span class="sxs-lookup"><span data-stu-id="b2306-128">float4</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="b2306-129">Если объект текстуры является массивом, последний компонент является индексом массива.</span><span class="sxs-lookup"><span data-stu-id="b2306-129">If the texture object is an array, the last component is the array index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2306-130"><span id="LOD"></span><span id="lod"></span><em>лод</em></span><span class="sxs-lookup"><span data-stu-id="b2306-130"><span id="LOD"></span><span id="lod"></span><em>LOD</em></span></span></p></td>
<td><p><span data-ttu-id="b2306-131">окне Число, указывающее уровень mipmap.</span><span class="sxs-lookup"><span data-stu-id="b2306-131">[in] A number that specifies the mipmap level.</span></span> <span data-ttu-id="b2306-132">Если значение равно 0, используется зеро'с (самая большая схема).</span><span class="sxs-lookup"><span data-stu-id="b2306-132">If the value is = 0, the zero'th (biggest map) is used.</span></span> <span data-ttu-id="b2306-133">Дробное значение (если оно указано) используется для интерполяции между двумя уровнями mipmap.</span><span class="sxs-lookup"><span data-stu-id="b2306-133">The fractional value (if supplied) is used to interpolate between two mipmap levels.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2306-134"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Собой</em></span><span class="sxs-lookup"><span data-stu-id="b2306-134"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="b2306-135">окне Необязательное Смещение координаты текстуры, которое может использоваться для любого типа объекта текстуры. смещение применяется к расположению перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="b2306-135">[in] An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="b2306-136">Смещение текстуры должно быть статическим.</span><span class="sxs-lookup"><span data-stu-id="b2306-136">The texture offsets need to be static.</span></span> <span data-ttu-id="b2306-137">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="b2306-137">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="b2306-138">Дополнительные сведения см. в разделе <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">применение смещения координат текстуры</a>.</span><span class="sxs-lookup"><span data-stu-id="b2306-138">For more info, see <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Applying texture coordinate offsets</a>.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b2306-139">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="b2306-139">Texture-Object Type</span></span></th>
<th><span data-ttu-id="b2306-140">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="b2306-140">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b2306-141">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="b2306-141">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="b2306-142">INT</span><span class="sxs-lookup"><span data-stu-id="b2306-142">int</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b2306-143">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="b2306-143">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="b2306-144">int2</span><span class="sxs-lookup"><span data-stu-id="b2306-144">int2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b2306-145">Texture3D</span><span class="sxs-lookup"><span data-stu-id="b2306-145">Texture3D</span></span></td>
<td><span data-ttu-id="b2306-146">int3</span><span class="sxs-lookup"><span data-stu-id="b2306-146">int3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b2306-147">Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="b2306-147">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="b2306-148">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b2306-148">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="b2306-149">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b2306-149">Return Value</span></span>

<span data-ttu-id="b2306-150">Тип шаблона текстуры, который может быть вектором с одним или несколькими компонентами.</span><span class="sxs-lookup"><span data-stu-id="b2306-150">The texture's template type, which may be a single- or multi-component vector.</span></span> <span data-ttu-id="b2306-151">Формат основан на [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)в текстуре.</span><span class="sxs-lookup"><span data-stu-id="b2306-151">The format is based on the texture's [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="b2306-152">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="b2306-152">Minimum Shader Model</span></span>

<span data-ttu-id="b2306-153">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="b2306-153">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b2306-154">VS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b2306-154">vs\_4\_0</span></span> | <span data-ttu-id="b2306-155">VS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="b2306-155">vs\_4\_1</span></span>  | <span data-ttu-id="b2306-156">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b2306-156">ps\_4\_0</span></span> | <span data-ttu-id="b2306-157">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="b2306-157">ps\_4\_1</span></span>  | <span data-ttu-id="b2306-158">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b2306-158">gs\_4\_0</span></span> | <span data-ttu-id="b2306-159">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="b2306-159">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
| <span data-ttu-id="b2306-160">x</span><span class="sxs-lookup"><span data-stu-id="b2306-160">x</span></span>        | <span data-ttu-id="b2306-161">x</span><span class="sxs-lookup"><span data-stu-id="b2306-161">x</span></span>         | <span data-ttu-id="b2306-162">x</span><span class="sxs-lookup"><span data-stu-id="b2306-162">x</span></span>        | <span data-ttu-id="b2306-163">x</span><span class="sxs-lookup"><span data-stu-id="b2306-163">x</span></span>         | <span data-ttu-id="b2306-164">x</span><span class="sxs-lookup"><span data-stu-id="b2306-164">x</span></span>        | <span data-ttu-id="b2306-165">x</span><span class="sxs-lookup"><span data-stu-id="b2306-165">x</span></span>         |



 

1.  <span data-ttu-id="b2306-166">Текстурекубеаррай доступен в модели шейдеров 4,1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="b2306-166">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="b2306-167">Модель шейдеров 4,1 доступна в Direct3D 10,1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="b2306-167">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="example"></a><span data-ttu-id="b2306-168">Пример</span><span class="sxs-lookup"><span data-stu-id="b2306-168">Example</span></span>

<span data-ttu-id="b2306-169">Этот частичный пример кода находится в файле с расширением. FX в [образце Instancing10](https://msdn.microsoft.com/library/Ee416415(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="b2306-169">This partial code example is from the Instancing.fx file in the [Instancing10 Sample](https://msdn.microsoft.com/library/Ee416415(v=VS.85).aspx).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="b2306-170">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="b2306-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2306-171">Текстура-объект</span><span class="sxs-lookup"><span data-stu-id="b2306-171">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

