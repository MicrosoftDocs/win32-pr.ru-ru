---
title: 'Функция Самплеград:: Самплеград (S, float, float, float, int, float) для Texture2D'
description: Примеры Texture2D с использованием градиента, влияющего на способ вычисления расположения выборки, с необязательным значением для фиксации примера уровня детализации (Лод) до значения. Для Texture2D.
ms.assetid: 1216B02A-4F70-4804-9B04-37E83DFC1CE8
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
ms.openlocfilehash: 0b309eb9bc0ce7cbd968be81fa05eee91ee577b4
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104998852"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloat-function-for-texture2d"></a><span data-ttu-id="83def-105">Функция Самплеград:: Самплеград (S, float, float, float, int, float) для Texture2D</span><span class="sxs-lookup"><span data-stu-id="83def-105">SampleGrad::SampleGrad(S,float,float,float,int,float) function for Texture2D</span></span>

<span data-ttu-id="83def-106">Примеры [**Texture2D**](sm5-object-texture2d.md)с использованием градиента, влияющего на способ вычисления расположения выборки, с необязательным значением для фиксации примера уровня детализации (Лод) до значения.</span><span class="sxs-lookup"><span data-stu-id="83def-106">Samples a [**Texture2D**](sm5-object-texture2d.md), using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="83def-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="83def-107">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="83def-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="83def-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83def-109">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="83def-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83def-110">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="83def-110">Type: **SamplerState**</span></span>

<span data-ttu-id="83def-111">[Состояние образца](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="83def-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="83def-112">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="83def-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="83def-113">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="83def-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83def-114">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="83def-114">Type: **float**</span></span>

<span data-ttu-id="83def-115">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="83def-115">The texture coordinates.</span></span> <span data-ttu-id="83def-116">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="83def-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="83def-117">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="83def-117">Texture-Object Type</span></span>                    | <span data-ttu-id="83def-118">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="83def-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="83def-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="83def-119">Texture1D</span></span>                              | <span data-ttu-id="83def-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="83def-120">float</span></span>          |
| <span data-ttu-id="83def-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="83def-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="83def-122">float2</span><span class="sxs-lookup"><span data-stu-id="83def-122">float2</span></span>         |
| <span data-ttu-id="83def-123">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="83def-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="83def-124">float3</span><span class="sxs-lookup"><span data-stu-id="83def-124">float3</span></span>         |
| <span data-ttu-id="83def-125">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="83def-125">TextureCubeArray</span></span>                       | <span data-ttu-id="83def-126">float4</span><span class="sxs-lookup"><span data-stu-id="83def-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="83def-127">*DDX* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="83def-127">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83def-128">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="83def-128">Type: **float**</span></span>

<span data-ttu-id="83def-129">Интенсивность изменения геометрии поверхности в направлении x.</span><span class="sxs-lookup"><span data-stu-id="83def-129">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="83def-130">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="83def-130">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="83def-131">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="83def-131">Texture-Object Type</span></span>                      | <span data-ttu-id="83def-132">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="83def-132">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="83def-133">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="83def-133">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="83def-134">FLOAT</span><span class="sxs-lookup"><span data-stu-id="83def-134">float</span></span>          |
| <span data-ttu-id="83def-135">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="83def-135">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="83def-136">float2</span><span class="sxs-lookup"><span data-stu-id="83def-136">float2</span></span>         |
| <span data-ttu-id="83def-137">Texture3D, Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="83def-137">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="83def-138">float3</span><span class="sxs-lookup"><span data-stu-id="83def-138">float3</span></span>         |
| <span data-ttu-id="83def-139">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="83def-139">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="83def-140">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="83def-140">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="83def-141">*ДДИ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="83def-141">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83def-142">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="83def-142">Type: **float**</span></span>

<span data-ttu-id="83def-143">Интенсивность изменения геометрии поверхности в направлении y.</span><span class="sxs-lookup"><span data-stu-id="83def-143">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="83def-144">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="83def-144">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="83def-145">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="83def-145">Texture-Object Type</span></span>                      | <span data-ttu-id="83def-146">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="83def-146">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="83def-147">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="83def-147">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="83def-148">FLOAT</span><span class="sxs-lookup"><span data-stu-id="83def-148">float</span></span>          |
| <span data-ttu-id="83def-149">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="83def-149">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="83def-150">float2</span><span class="sxs-lookup"><span data-stu-id="83def-150">float2</span></span>         |
| <span data-ttu-id="83def-151">Texture3D, Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="83def-151">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="83def-152">float3</span><span class="sxs-lookup"><span data-stu-id="83def-152">float3</span></span>         |
| <span data-ttu-id="83def-153">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="83def-153">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="83def-154">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="83def-154">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="83def-155">*Смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="83def-155">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83def-156">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="83def-156">Type: **int**</span></span>

<span data-ttu-id="83def-157">Необязательное Смещение координаты текстуры, которое может использоваться для любого типа объекта текстуры. смещение применяется к расположению перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="83def-157">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="83def-158">Используйте смещение только с целочисленным миплевел; в противном случае можно получить результаты, которые не могут быть правильно преобразованы в оборудование.</span><span class="sxs-lookup"><span data-stu-id="83def-158">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="83def-159">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="83def-159">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="83def-160">Дополнительные сведения см. в разделе [применение целочисленных смещений](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="83def-160">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="83def-161">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="83def-161">Texture-Object Type</span></span>           | <span data-ttu-id="83def-162">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="83def-162">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="83def-163">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="83def-163">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="83def-164">INT</span><span class="sxs-lookup"><span data-stu-id="83def-164">int</span></span>            |
| <span data-ttu-id="83def-165">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="83def-165">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="83def-166">int2</span><span class="sxs-lookup"><span data-stu-id="83def-166">int2</span></span>           |
| <span data-ttu-id="83def-167">Texture3D</span><span class="sxs-lookup"><span data-stu-id="83def-167">Texture3D</span></span>                     | <span data-ttu-id="83def-168">int3</span><span class="sxs-lookup"><span data-stu-id="83def-168">int3</span></span>           |
| <span data-ttu-id="83def-169">Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="83def-169">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="83def-170">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="83def-170">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="83def-171">*Срез* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="83def-171">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83def-172">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="83def-172">Type: **float**</span></span>

<span data-ttu-id="83def-173">Необязательное значение для примера среза Лод значений.</span><span class="sxs-lookup"><span data-stu-id="83def-173">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="83def-174">Например, если передать значение среза 2.0 f, вы убедитесь, что ни один из отдельных примеров не имеет доступа к MIP уровню менее 2.0.</span><span class="sxs-lookup"><span data-stu-id="83def-174">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83def-175">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="83def-175">Return value</span></span>

<span data-ttu-id="83def-176">Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="83def-176">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="83def-177">Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="83def-177">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="83def-178">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="83def-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83def-179">Методы Самплеград</span><span class="sxs-lookup"><span data-stu-id="83def-179">SampleGrad methods</span></span>](texture2d-samplegrad.md)
</dt> </dl>

 

 
