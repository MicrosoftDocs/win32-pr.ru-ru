---
title: 'Функция Самплеград:: Самплеград (S, float, float, float, int, float) для Texture1DArray'
description: Выбор текстуры с помощью градиента, влияющей на способ вычисления расположения выборки, с дополнительным значением для фиксации значений уровня детализации (Лод). Для Texture1DArray.
ms.assetid: 328EEC75-1E0A-4196-AD82-A48F3C66D65B
keywords:
- Функция Самплеград HLSL
topic_type:
- apiref
api_name:
- SampleGrad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e4af761ab82492fd49a4f6f048c74016a19aa872
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104987344"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloat-function-for-texture1darray"></a><span data-ttu-id="68beb-105">Функция Самплеград:: Самплеград (S, float, float, float, int, float) для Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="68beb-105">SampleGrad::SampleGrad(S,float,float,float,int,float) function for Texture1DArray</span></span>

<span data-ttu-id="68beb-106">Выбор текстуры с помощью градиента, влияющей на способ вычисления расположения выборки, с дополнительным значением для фиксации значений уровня детализации (Лод).</span><span class="sxs-lookup"><span data-stu-id="68beb-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="68beb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="68beb-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleGrad(
  in SamplerState S,
  in float        Location,
  in float        DDX,
  in float        DDY,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="68beb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="68beb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68beb-109">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="68beb-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68beb-110">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="68beb-110">Type: **SamplerState**</span></span>

<span data-ttu-id="68beb-111">[Состояние образца](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="68beb-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="68beb-112">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="68beb-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="68beb-113">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="68beb-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68beb-114">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="68beb-114">Type: **float**</span></span>

<span data-ttu-id="68beb-115">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="68beb-115">The texture coordinates.</span></span> <span data-ttu-id="68beb-116">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="68beb-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="68beb-117">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="68beb-117">Texture-Object Type</span></span>                    | <span data-ttu-id="68beb-118">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="68beb-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="68beb-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="68beb-119">Texture1D</span></span>                              | <span data-ttu-id="68beb-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="68beb-120">float</span></span>          |
| <span data-ttu-id="68beb-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="68beb-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="68beb-122">float2</span><span class="sxs-lookup"><span data-stu-id="68beb-122">float2</span></span>         |
| <span data-ttu-id="68beb-123">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="68beb-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="68beb-124">float3</span><span class="sxs-lookup"><span data-stu-id="68beb-124">float3</span></span>         |
| <span data-ttu-id="68beb-125">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="68beb-125">TextureCubeArray</span></span>                       | <span data-ttu-id="68beb-126">float4</span><span class="sxs-lookup"><span data-stu-id="68beb-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="68beb-127">*DDX* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="68beb-127">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68beb-128">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="68beb-128">Type: **float**</span></span>

<span data-ttu-id="68beb-129">Интенсивность изменения геометрии поверхности в направлении x.</span><span class="sxs-lookup"><span data-stu-id="68beb-129">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="68beb-130">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="68beb-130">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="68beb-131">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="68beb-131">Texture-Object Type</span></span>                      | <span data-ttu-id="68beb-132">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="68beb-132">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="68beb-133">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="68beb-133">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="68beb-134">FLOAT</span><span class="sxs-lookup"><span data-stu-id="68beb-134">float</span></span>          |
| <span data-ttu-id="68beb-135">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="68beb-135">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="68beb-136">float2</span><span class="sxs-lookup"><span data-stu-id="68beb-136">float2</span></span>         |
| <span data-ttu-id="68beb-137">Texture3D, Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="68beb-137">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="68beb-138">float3</span><span class="sxs-lookup"><span data-stu-id="68beb-138">float3</span></span>         |
| <span data-ttu-id="68beb-139">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="68beb-139">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="68beb-140">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="68beb-140">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="68beb-141">*ДДИ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="68beb-141">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68beb-142">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="68beb-142">Type: **float**</span></span>

<span data-ttu-id="68beb-143">Интенсивность изменения геометрии поверхности в направлении y.</span><span class="sxs-lookup"><span data-stu-id="68beb-143">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="68beb-144">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="68beb-144">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="68beb-145">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="68beb-145">Texture-Object Type</span></span>                      | <span data-ttu-id="68beb-146">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="68beb-146">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="68beb-147">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="68beb-147">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="68beb-148">FLOAT</span><span class="sxs-lookup"><span data-stu-id="68beb-148">float</span></span>          |
| <span data-ttu-id="68beb-149">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="68beb-149">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="68beb-150">float2</span><span class="sxs-lookup"><span data-stu-id="68beb-150">float2</span></span>         |
| <span data-ttu-id="68beb-151">Texture3D, Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="68beb-151">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="68beb-152">float3</span><span class="sxs-lookup"><span data-stu-id="68beb-152">float3</span></span>         |
| <span data-ttu-id="68beb-153">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="68beb-153">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="68beb-154">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="68beb-154">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="68beb-155">*Смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="68beb-155">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68beb-156">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="68beb-156">Type: **int**</span></span>

<span data-ttu-id="68beb-157">Необязательное Смещение координаты текстуры, которое может использоваться для любого типа объекта текстуры. смещение применяется к расположению перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="68beb-157">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="68beb-158">Используйте смещение только с целочисленным миплевел; в противном случае можно получить результаты, которые не могут быть правильно преобразованы в оборудование.</span><span class="sxs-lookup"><span data-stu-id="68beb-158">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="68beb-159">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="68beb-159">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="68beb-160">Дополнительные сведения см. в разделе [применение целочисленных смещений](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="68beb-160">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="68beb-161">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="68beb-161">Texture-Object Type</span></span>           | <span data-ttu-id="68beb-162">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="68beb-162">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="68beb-163">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="68beb-163">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="68beb-164">INT</span><span class="sxs-lookup"><span data-stu-id="68beb-164">int</span></span>            |
| <span data-ttu-id="68beb-165">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="68beb-165">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="68beb-166">int2</span><span class="sxs-lookup"><span data-stu-id="68beb-166">int2</span></span>           |
| <span data-ttu-id="68beb-167">Texture3D</span><span class="sxs-lookup"><span data-stu-id="68beb-167">Texture3D</span></span>                     | <span data-ttu-id="68beb-168">int3</span><span class="sxs-lookup"><span data-stu-id="68beb-168">int3</span></span>           |
| <span data-ttu-id="68beb-169">Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="68beb-169">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="68beb-170">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="68beb-170">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="68beb-171">*Срез* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="68beb-171">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68beb-172">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="68beb-172">Type: **float**</span></span>

<span data-ttu-id="68beb-173">Необязательное значение для примера среза Лод значений.</span><span class="sxs-lookup"><span data-stu-id="68beb-173">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="68beb-174">Например, если передать значение среза 2.0 f, вы убедитесь, что ни один из отдельных примеров не имеет доступа к MIP уровню менее 2.0.</span><span class="sxs-lookup"><span data-stu-id="68beb-174">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68beb-175">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="68beb-175">Return value</span></span>

<span data-ttu-id="68beb-176">Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="68beb-176">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="68beb-177">Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="68beb-177">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="68beb-178">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="68beb-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68beb-179">Методы Самплеград</span><span class="sxs-lookup"><span data-stu-id="68beb-179">SampleGrad methods</span></span>](texture1darray-samplegrad.md)
</dt> </dl>

 

 
