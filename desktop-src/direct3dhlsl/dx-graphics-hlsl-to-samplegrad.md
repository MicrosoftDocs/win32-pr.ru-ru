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
# <a name="samplegrad-directx-hlsl-texture-object"></a><span data-ttu-id="e646e-104">Самплеград (объект текстуры DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e646e-104">SampleGrad (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="e646e-105">Выбор текстуры с помощью градиента, чтобы повлиять на способ вычисления расположения образца.</span><span class="sxs-lookup"><span data-stu-id="e646e-105">Samples a texture using a gradient to influence the way the sample location is calculated.</span></span>



|                                                                                                            |
|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e646e-106">&lt;Тип шаблона &gt; Object. самплеград (выборка \_ состояния, расположение с плавающей точкой, Обмен плавающей запятой, ДДИ с плавающей запятой, \[ смещение int \] );</span><span class="sxs-lookup"><span data-stu-id="e646e-106">&lt;Template Type&gt; Object.SampleGrad( sampler\_state S, float Location, float DDX, float DDY \[, int Offset\] );</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="e646e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e646e-107">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e646e-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="e646e-108">Item</span></span></th>
<th><span data-ttu-id="e646e-109">Описание</span><span class="sxs-lookup"><span data-stu-id="e646e-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e646e-110"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Объектами</em></span><span class="sxs-lookup"><span data-stu-id="e646e-110"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="e646e-111">Любой тип <a href="dx-graphics-hlsl-to-type.md">объекта текстуры</a> (кроме Texture2DMS и Texture2DMSArray).</span><span class="sxs-lookup"><span data-stu-id="e646e-111">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e646e-112"><span id="S"></span><span id="s"></span><em>#D0</em></span><span class="sxs-lookup"><span data-stu-id="e646e-112"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="e646e-113">окне <a href="dx-graphics-hlsl-sampler.md">Состояние образца</a>.</span><span class="sxs-lookup"><span data-stu-id="e646e-113">[in] A <a href="dx-graphics-hlsl-sampler.md">Sampler state</a>.</span></span> <span data-ttu-id="e646e-114">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="e646e-114">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e646e-115"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Места</em></span><span class="sxs-lookup"><span data-stu-id="e646e-115"><span id="Location"></span><span id="location"></span><span id="LOCATION"></span><em>Location</em></span></span><br/></td>
<td><span data-ttu-id="e646e-116">окне Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="e646e-116">[in] The Texture coordinates.</span></span> <span data-ttu-id="e646e-117">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="e646e-117">The argument type is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e646e-118">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="e646e-118">Texture-Object Type</span></span></th>
<th><span data-ttu-id="e646e-119">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="e646e-119">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e646e-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e646e-120">Texture1D</span></span></td>
<td><span data-ttu-id="e646e-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="e646e-121">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e646e-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="e646e-122">Texture1DArray, Texture2D</span></span></td>
<td><span data-ttu-id="e646e-123">float2</span><span class="sxs-lookup"><span data-stu-id="e646e-123">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e646e-124">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="e646e-124">Texture2DArray, Texture3D, TextureCube</span></span></td>
<td><span data-ttu-id="e646e-125">float3</span><span class="sxs-lookup"><span data-stu-id="e646e-125">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e646e-126">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="e646e-126">TextureCubeArray</span></span> </td>
<td><span data-ttu-id="e646e-127">float4</span><span class="sxs-lookup"><span data-stu-id="e646e-127">float4</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e646e-128">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="e646e-128">Texture2DMS, Texture2DMSArray</span></span></td>
<td><span data-ttu-id="e646e-129">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e646e-129">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e646e-130"><span id="DDX"></span><span id="ddx"></span><em>DDX</em></span><span class="sxs-lookup"><span data-stu-id="e646e-130"><span id="DDX"></span><span id="ddx"></span><em>DDX</em></span></span></p></td>
<td><p><span data-ttu-id="e646e-131">окне Интенсивность изменения геометрии поверхности в направлении x.</span><span class="sxs-lookup"><span data-stu-id="e646e-131">[in] The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="e646e-132">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="e646e-132">The argument type is dependent on the texture-object type.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e646e-133">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="e646e-133">Texture-Object Type</span></span></th>
<th><span data-ttu-id="e646e-134">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="e646e-134">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e646e-135">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="e646e-135">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="e646e-136">FLOAT</span><span class="sxs-lookup"><span data-stu-id="e646e-136">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e646e-137">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="e646e-137">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="e646e-138">float2</span><span class="sxs-lookup"><span data-stu-id="e646e-138">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e646e-139">Texture3D, Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="e646e-139">Texture3D, TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="e646e-140">float3</span><span class="sxs-lookup"><span data-stu-id="e646e-140">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e646e-141">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="e646e-141">Texture2DMS, Texture2DMSArray</span></span></td>
<td><span data-ttu-id="e646e-142">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e646e-142">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e646e-143"><span id="DDY"></span><span id="ddy"></span><em>дди</em></span><span class="sxs-lookup"><span data-stu-id="e646e-143"><span id="DDY"></span><span id="ddy"></span><em>DDY</em></span></span></p></td>
<td><p><span data-ttu-id="e646e-144">окне Интенсивность изменения геометрии поверхности в направлении y.</span><span class="sxs-lookup"><span data-stu-id="e646e-144">[in] The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="e646e-145">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="e646e-145">The argument type is dependent on the texture-object type.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e646e-146">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="e646e-146">Texture-Object Type</span></span></th>
<th><span data-ttu-id="e646e-147">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="e646e-147">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e646e-148">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="e646e-148">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="e646e-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="e646e-149">float</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e646e-150">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="e646e-150">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="e646e-151">float2</span><span class="sxs-lookup"><span data-stu-id="e646e-151">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e646e-152">Texture3D, Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="e646e-152">Texture3D, TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="e646e-153">float3</span><span class="sxs-lookup"><span data-stu-id="e646e-153">float3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e646e-154">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="e646e-154">Texture2DMS, Texture2DMSArray</span></span></td>
<td><span data-ttu-id="e646e-155">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e646e-155">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e646e-156"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Собой</em></span><span class="sxs-lookup"><span data-stu-id="e646e-156"><span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="e646e-157">окне Необязательное Смещение координаты текстуры, которое может использоваться для любых типов объектов текстуры.</span><span class="sxs-lookup"><span data-stu-id="e646e-157">[in] An optional texture coordinate offset, which can be used for any texture-object types.</span></span> <span data-ttu-id="e646e-158">Смещение применяется к расположению перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="e646e-158">The offset is applied to the location before sampling.</span></span> <span data-ttu-id="e646e-159">Используйте смещение только с целочисленным миплевел; в противном случае можно получить результаты, которые не могут быть правильно преобразованы в оборудование.</span><span class="sxs-lookup"><span data-stu-id="e646e-159">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="e646e-160">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="e646e-160">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="e646e-161">Дополнительные сведения см. в разделе<a href="dx-graphics-hlsl-to-sample.md">применение целочисленных смещений</a>.</span><span class="sxs-lookup"><span data-stu-id="e646e-161">For more info, see<a href="dx-graphics-hlsl-to-sample.md">Applying Integer Offsets</a>.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e646e-162">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="e646e-162">Texture-Object Type</span></span></th>
<th><span data-ttu-id="e646e-163">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="e646e-163">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e646e-164">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="e646e-164">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="e646e-165">INT</span><span class="sxs-lookup"><span data-stu-id="e646e-165">int</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e646e-166">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="e646e-166">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="e646e-167">int2</span><span class="sxs-lookup"><span data-stu-id="e646e-167">int2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e646e-168">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e646e-168">Texture3D</span></span></td>
<td><span data-ttu-id="e646e-169">int3</span><span class="sxs-lookup"><span data-stu-id="e646e-169">int3</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e646e-170">Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="e646e-170">TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="e646e-171">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e646e-171">not supported</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e646e-172">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="e646e-172">Texture2DMS, Texture2DMSArray</span></span></td>
<td><span data-ttu-id="e646e-173">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e646e-173">not supported</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="e646e-174">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e646e-174">Return Value</span></span>

<span data-ttu-id="e646e-175">Тип шаблона текстуры, который может быть вектором с одним или несколькими компонентами.</span><span class="sxs-lookup"><span data-stu-id="e646e-175">The texture's template type, which may be a single- or multi-component vector.</span></span> <span data-ttu-id="e646e-176">Формат основан на [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)в текстуре.</span><span class="sxs-lookup"><span data-stu-id="e646e-176">The format is based on the texture's [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="e646e-177">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="e646e-177">Minimum Shader Model</span></span>

<span data-ttu-id="e646e-178">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="e646e-178">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e646e-179">VS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e646e-179">vs\_4\_0</span></span> | <span data-ttu-id="e646e-180">VS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="e646e-180">vs\_4\_1</span></span>  | <span data-ttu-id="e646e-181">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e646e-181">ps\_4\_0</span></span> | <span data-ttu-id="e646e-182">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="e646e-182">ps\_4\_1</span></span>  | <span data-ttu-id="e646e-183">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e646e-183">gs\_4\_0</span></span> | <span data-ttu-id="e646e-184">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="e646e-184">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
| <span data-ttu-id="e646e-185">x</span><span class="sxs-lookup"><span data-stu-id="e646e-185">x</span></span>        | <span data-ttu-id="e646e-186">x</span><span class="sxs-lookup"><span data-stu-id="e646e-186">x</span></span>         | <span data-ttu-id="e646e-187">x</span><span class="sxs-lookup"><span data-stu-id="e646e-187">x</span></span>        | <span data-ttu-id="e646e-188">x</span><span class="sxs-lookup"><span data-stu-id="e646e-188">x</span></span>         | <span data-ttu-id="e646e-189">x</span><span class="sxs-lookup"><span data-stu-id="e646e-189">x</span></span>        | <span data-ttu-id="e646e-190">x</span><span class="sxs-lookup"><span data-stu-id="e646e-190">x</span></span>         |



 

1.  <span data-ttu-id="e646e-191">Текстурекубеаррай доступен в модели шейдеров 4,1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="e646e-191">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="e646e-192">Модель шейдеров 4,1 доступна в Direct3D 10,1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="e646e-192">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="example"></a><span data-ttu-id="e646e-193">Например, .</span><span class="sxs-lookup"><span data-stu-id="e646e-193">Example</span></span>

<span data-ttu-id="e646e-194">Этот частичный пример кода относится к файлу Мотионблур. FX в [примере MotionBlur10](https://msdn.microsoft.com/library/Ee416417(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="e646e-194">This partial code example is from the MotionBlur.fx file in the [MotionBlur10 Sample](https://msdn.microsoft.com/library/Ee416417(v=VS.85).aspx).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="e646e-195">См. также</span><span class="sxs-lookup"><span data-stu-id="e646e-195">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e646e-196">Текстура-объект</span><span class="sxs-lookup"><span data-stu-id="e646e-196">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

