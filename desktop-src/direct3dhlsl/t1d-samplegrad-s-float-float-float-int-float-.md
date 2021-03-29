---
title: 'Функция Самплеград:: Самплеград (S, float, float, float, int, float) для Texture1D'
description: Функция выбирает текстуру с помощью градиента, чтобы повлиять на способ вычисления расположения выборки, с необязательным значением для фиксации примера уровня детализации (Лод).
ms.assetid: 34A79CB6-0C45-40ED-845C-77C08F1DEC57
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
ms.openlocfilehash: 8c6222d8fa9548e3154abf7605fc5032dd67235a
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104987350"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloat-function-for-texture1d"></a><span data-ttu-id="f11c0-104">Функция Самплеград:: Самплеград (S, float, float, float, int, float) для Texture1D</span><span class="sxs-lookup"><span data-stu-id="f11c0-104">SampleGrad::SampleGrad(S,float,float,float,int,float) function for Texture1D</span></span>

<span data-ttu-id="f11c0-105">Выбор текстуры с помощью градиента, влияющей на способ вычисления расположения выборки, с дополнительным значением для фиксации значений уровня детализации (Лод).</span><span class="sxs-lookup"><span data-stu-id="f11c0-105">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="f11c0-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f11c0-106">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="f11c0-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f11c0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f11c0-108">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="f11c0-108">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f11c0-109">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="f11c0-109">Type: **SamplerState**</span></span>

<span data-ttu-id="f11c0-110">[Состояние образца](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="f11c0-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="f11c0-111">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="f11c0-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="f11c0-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f11c0-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f11c0-113">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="f11c0-113">Type: **float**</span></span>

<span data-ttu-id="f11c0-114">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="f11c0-114">The texture coordinates.</span></span> <span data-ttu-id="f11c0-115">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="f11c0-115">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="f11c0-116">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="f11c0-116">Texture-Object Type</span></span>                    | <span data-ttu-id="f11c0-117">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="f11c0-117">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="f11c0-118">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f11c0-118">Texture1D</span></span>                              | <span data-ttu-id="f11c0-119">FLOAT</span><span class="sxs-lookup"><span data-stu-id="f11c0-119">float</span></span>          |
| <span data-ttu-id="f11c0-120">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="f11c0-120">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="f11c0-121">float2</span><span class="sxs-lookup"><span data-stu-id="f11c0-121">float2</span></span>         |
| <span data-ttu-id="f11c0-122">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="f11c0-122">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="f11c0-123">float3</span><span class="sxs-lookup"><span data-stu-id="f11c0-123">float3</span></span>         |
| <span data-ttu-id="f11c0-124">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="f11c0-124">TextureCubeArray</span></span>                       | <span data-ttu-id="f11c0-125">float4</span><span class="sxs-lookup"><span data-stu-id="f11c0-125">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="f11c0-126">*DDX* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="f11c0-126">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f11c0-127">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="f11c0-127">Type: **float**</span></span>

<span data-ttu-id="f11c0-128">Интенсивность изменения геометрии поверхности в направлении x.</span><span class="sxs-lookup"><span data-stu-id="f11c0-128">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="f11c0-129">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="f11c0-129">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="f11c0-130">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="f11c0-130">Texture-Object Type</span></span>                      | <span data-ttu-id="f11c0-131">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="f11c0-131">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="f11c0-132">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="f11c0-132">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="f11c0-133">FLOAT</span><span class="sxs-lookup"><span data-stu-id="f11c0-133">float</span></span>          |
| <span data-ttu-id="f11c0-134">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="f11c0-134">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="f11c0-135">float2</span><span class="sxs-lookup"><span data-stu-id="f11c0-135">float2</span></span>         |
| <span data-ttu-id="f11c0-136">Texture3D, Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="f11c0-136">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="f11c0-137">float3</span><span class="sxs-lookup"><span data-stu-id="f11c0-137">float3</span></span>         |
| <span data-ttu-id="f11c0-138">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="f11c0-138">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="f11c0-139">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f11c0-139">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="f11c0-140">*ДДИ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f11c0-140">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f11c0-141">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="f11c0-141">Type: **float**</span></span>

<span data-ttu-id="f11c0-142">Интенсивность изменения геометрии поверхности в направлении y.</span><span class="sxs-lookup"><span data-stu-id="f11c0-142">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="f11c0-143">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="f11c0-143">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="f11c0-144">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="f11c0-144">Texture-Object Type</span></span>                      | <span data-ttu-id="f11c0-145">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="f11c0-145">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="f11c0-146">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="f11c0-146">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="f11c0-147">FLOAT</span><span class="sxs-lookup"><span data-stu-id="f11c0-147">float</span></span>          |
| <span data-ttu-id="f11c0-148">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="f11c0-148">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="f11c0-149">float2</span><span class="sxs-lookup"><span data-stu-id="f11c0-149">float2</span></span>         |
| <span data-ttu-id="f11c0-150">Texture3D, Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="f11c0-150">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="f11c0-151">float3</span><span class="sxs-lookup"><span data-stu-id="f11c0-151">float3</span></span>         |
| <span data-ttu-id="f11c0-152">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="f11c0-152">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="f11c0-153">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f11c0-153">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="f11c0-154">*Смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f11c0-154">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f11c0-155">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="f11c0-155">Type: **int**</span></span>

<span data-ttu-id="f11c0-156">Необязательное Смещение координаты текстуры, которое может использоваться для любого типа объекта текстуры. смещение применяется к расположению перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="f11c0-156">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="f11c0-157">Используйте смещение только с целочисленным миплевел; в противном случае можно получить результаты, которые не могут быть правильно преобразованы в оборудование.</span><span class="sxs-lookup"><span data-stu-id="f11c0-157">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="f11c0-158">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="f11c0-158">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="f11c0-159">Дополнительные сведения см. в разделе [применение целочисленных смещений](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="f11c0-159">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="f11c0-160">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="f11c0-160">Texture-Object Type</span></span>           | <span data-ttu-id="f11c0-161">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="f11c0-161">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="f11c0-162">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="f11c0-162">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="f11c0-163">INT</span><span class="sxs-lookup"><span data-stu-id="f11c0-163">int</span></span>            |
| <span data-ttu-id="f11c0-164">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="f11c0-164">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="f11c0-165">int2</span><span class="sxs-lookup"><span data-stu-id="f11c0-165">int2</span></span>           |
| <span data-ttu-id="f11c0-166">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f11c0-166">Texture3D</span></span>                     | <span data-ttu-id="f11c0-167">int3</span><span class="sxs-lookup"><span data-stu-id="f11c0-167">int3</span></span>           |
| <span data-ttu-id="f11c0-168">Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="f11c0-168">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="f11c0-169">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f11c0-169">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="f11c0-170">*Срез* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f11c0-170">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f11c0-171">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="f11c0-171">Type: **float**</span></span>

<span data-ttu-id="f11c0-172">Необязательное значение для примера среза Лод значений.</span><span class="sxs-lookup"><span data-stu-id="f11c0-172">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="f11c0-173">Например, если передать значение среза 2.0 f, вы убедитесь, что ни один из отдельных примеров не имеет доступа к MIP уровню менее 2.0.</span><span class="sxs-lookup"><span data-stu-id="f11c0-173">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f11c0-174">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f11c0-174">Return value</span></span>

<span data-ttu-id="f11c0-175">Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="f11c0-175">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="f11c0-176">Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="f11c0-176">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="f11c0-177">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f11c0-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f11c0-178">Методы Самплеград</span><span class="sxs-lookup"><span data-stu-id="f11c0-178">SampleGrad methods</span></span>](texture1d-samplegrad.md)
</dt> </dl>

 

 
