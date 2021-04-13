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
ms.openlocfilehash: e710b8a6c7dd2983c6d0c635d16356f95d0b4fe7
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/17/2020
ms.locfileid: "104414276"
---
# <a name="samplebias-directx-hlsl-texture-object"></a><span data-ttu-id="bf3b0-103">Самплебиас (объект текстуры DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bf3b0-103">SampleBias (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="bf3b0-104">Демонстрирует выбор текстуры после применения смещения входных данных к уровню mipmap.</span><span class="sxs-lookup"><span data-stu-id="bf3b0-104">Samples a texture, after applying the input bias to the mipmap level.</span></span>



|                                                                                                  |
|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf3b0-105">&lt;Тип шаблона &gt; Object. самплебиас (выборка \_ состояния, расположение с плавающей точкой, смещение с плавающей запятой \[ , смещения int \] );</span><span class="sxs-lookup"><span data-stu-id="bf3b0-105">&lt;Template Type&gt; Object.SampleBias( sampler\_state S, float Location, float Bias \[, int Offset\] );</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="bf3b0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf3b0-106">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bf3b0-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="bf3b0-107">Item</span></span></th>
<th><span data-ttu-id="bf3b0-108">Описание</span><span class="sxs-lookup"><span data-stu-id="bf3b0-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bf3b0-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Объектами</em></span><span class="sxs-lookup"><span data-stu-id="bf3b0-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="bf3b0-110">Любой тип <a href="dx-graphics-hlsl-to-type.md">объекта текстуры</a> (кроме Texture2DMS и Texture2DMSArray).</span><span class="sxs-lookup"><span data-stu-id="bf3b0-110">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf3b0-111"><span id="S"></span><span id="s"></span><em>#D0</em></span><span class="sxs-lookup"><span data-stu-id="bf3b0-111"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="bf3b0-112">окне <a href="dx-graphics-hlsl-sampler.md">Состояние образца</a>.</span><span class="sxs-lookup"><span data-stu-id="bf3b0-112">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="bf3b0-113">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="bf3b0-113">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bf3b0-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Места</em></span><span class="sxs-lookup"><span data-stu-id="bf3b0-114"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="bf3b0-115">окне Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="bf3b0-115">[in] The texture coordinates.</span></span> <span data-ttu-id="bf3b0-116">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="bf3b0-116">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="bf3b0-117">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="bf3b0-117">Texture-Object Type</span></span></th>
<th><span data-ttu-id="bf3b0-118">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="bf3b0-118">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bf3b0-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bf3b0-119">Texture1D</span></span></td>
<td><span data-ttu-id="bf3b0-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bf3b0-120">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf3b0-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="bf3b0-121">Texture1DArray, Texture2D</span></span></td>
<td><span data-ttu-id="bf3b0-122">float2</span><span class="sxs-lookup"><span data-stu-id="bf3b0-122">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bf3b0-123">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="bf3b0-123">Texture2DArray, Texture3D, TextureCube</span></span></td>
<td><span data-ttu-id="bf3b0-124">float3</span><span class="sxs-lookup"><span data-stu-id="bf3b0-124">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf3b0-125">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="bf3b0-125">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="bf3b0-126">float4</span><span class="sxs-lookup"><span data-stu-id="bf3b0-126">float4</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf3b0-127"><span id="Bias"></span><span id="bias"></span><span id="BIAS"></span><em>Часов</em></span><span class="sxs-lookup"><span data-stu-id="bf3b0-127"><span id="Bias"></span><span id="bias"></span><span id="BIAS"></span><em>Bias</em></span></span></p></td>
<td><p><span data-ttu-id="bf3b0-128">окне Значение смещения, которое является числом с плавающей запятой от-16,0 до 15,99, применяется к MIP уровню перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="bf3b0-128">[in] The bias value, which is a floating-point number between -16.0 and 15.99, is applied to a mip level before sampling.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf3b0-129"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Собой</em></span><span class="sxs-lookup"><span data-stu-id="bf3b0-129"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="bf3b0-130">окне Необязательное Смещение координаты текстуры, которое может использоваться для любого типа объекта текстуры. смещение применяется к расположению перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="bf3b0-130">[in] An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="bf3b0-131">Смещение текстуры должно быть статическим.</span><span class="sxs-lookup"><span data-stu-id="bf3b0-131">The texture offsets need to be static.</span></span> <span data-ttu-id="bf3b0-132">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="bf3b0-132">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="bf3b0-133">Дополнительные сведения см. в разделе <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">применение смещения координат текстуры</a>.</span><span class="sxs-lookup"><span data-stu-id="bf3b0-133">For more info, see <a href="/windows/win32/direct3dhlsl/dx-graphics-hlsl-to-sample#applying-texture-coordinate-offsets">Applying texture coordinate offsets</a>.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="bf3b0-134">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="bf3b0-134">Texture-Object Type</span></span></th>
<th><span data-ttu-id="bf3b0-135">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="bf3b0-135">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bf3b0-136">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="bf3b0-136">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="bf3b0-137">INT</span><span class="sxs-lookup"><span data-stu-id="bf3b0-137">int</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf3b0-138">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="bf3b0-138">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="bf3b0-139">int2</span><span class="sxs-lookup"><span data-stu-id="bf3b0-139">int2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bf3b0-140">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bf3b0-140">Texture3D</span></span></td>
<td><span data-ttu-id="bf3b0-141">int3</span><span class="sxs-lookup"><span data-stu-id="bf3b0-141">int3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf3b0-142">Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="bf3b0-142">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="bf3b0-143">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="bf3b0-143">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="bf3b0-144">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bf3b0-144">Return Value</span></span>

<span data-ttu-id="bf3b0-145">Тип шаблона текстуры, который может быть вектором с одним или несколькими компонентами.</span><span class="sxs-lookup"><span data-stu-id="bf3b0-145">The texture's template type, which may be a single- or multi-component vector.</span></span> <span data-ttu-id="bf3b0-146">Формат основан на [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)в текстуре.</span><span class="sxs-lookup"><span data-stu-id="bf3b0-146">The format is based on the texture's [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="bf3b0-147">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="bf3b0-147">Minimum Shader Model</span></span>

<span data-ttu-id="bf3b0-148">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="bf3b0-148">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="bf3b0-149">VS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bf3b0-149">vs\_4\_0</span></span> | <span data-ttu-id="bf3b0-150">VS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="bf3b0-150">vs\_4\_1</span></span>  | <span data-ttu-id="bf3b0-151">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bf3b0-151">ps\_4\_0</span></span> | <span data-ttu-id="bf3b0-152">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="bf3b0-152">ps\_4\_1</span></span>  | <span data-ttu-id="bf3b0-153">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bf3b0-153">gs\_4\_0</span></span> | <span data-ttu-id="bf3b0-154">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="bf3b0-154">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          |           | <span data-ttu-id="bf3b0-155">x</span><span class="sxs-lookup"><span data-stu-id="bf3b0-155">x</span></span>        | <span data-ttu-id="bf3b0-156">x</span><span class="sxs-lookup"><span data-stu-id="bf3b0-156">x</span></span>         |          |           |



 

1.  <span data-ttu-id="bf3b0-157">Текстурекубеаррай доступен в модели шейдеров 4,1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="bf3b0-157">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="bf3b0-158">Модель шейдеров 4,1 доступна в Direct3D 10,1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="bf3b0-158">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf3b0-159">См. также</span><span class="sxs-lookup"><span data-stu-id="bf3b0-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf3b0-160">Текстура-объект</span><span class="sxs-lookup"><span data-stu-id="bf3b0-160">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

