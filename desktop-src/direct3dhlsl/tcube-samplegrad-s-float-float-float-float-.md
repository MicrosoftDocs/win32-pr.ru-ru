---
title: 'Функция Самплеград:: Самплеград (S, float, float, float, float) для Текстурекубе'
description: Выбор текстуры с помощью градиента, влияющей на способ вычисления расположения выборки, с дополнительным значением для фиксации значений уровня детализации (Лод). Для Текстурекубе
ms.assetid: C5BC71FA-63E3-4DE2-9202-B9C79789AE8E
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
ms.openlocfilehash: e4a51c49d9373dc210cbf216089e4c82835bf2c4
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104548186"
---
# <a name="samplegradsamplegradsfloatfloatfloatfloat-function-for-texturecube"></a><span data-ttu-id="170e2-105">Функция Самплеград:: Самплеград (S, float, float, float, float) для Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="170e2-105">SampleGrad::SampleGrad(S,float,float,float,float) function for TextureCube</span></span>

<span data-ttu-id="170e2-106">Выбор текстуры с помощью градиента, влияющей на способ вычисления расположения выборки, с дополнительным значением для фиксации значений уровня детализации (Лод).</span><span class="sxs-lookup"><span data-stu-id="170e2-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="170e2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="170e2-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleGrad(
  in SamplerState S,
  in float        Location,
  in float        DDX,
  in float        DDY,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="170e2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="170e2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="170e2-109">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="170e2-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="170e2-110">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="170e2-110">Type: **SamplerState**</span></span>

<span data-ttu-id="170e2-111">[Состояние образца](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="170e2-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="170e2-112">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="170e2-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="170e2-113">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="170e2-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="170e2-114">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="170e2-114">Type: **float**</span></span>

<span data-ttu-id="170e2-115">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="170e2-115">The texture coordinates.</span></span> <span data-ttu-id="170e2-116">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="170e2-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="170e2-117">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="170e2-117">Texture-Object Type</span></span>                    | <span data-ttu-id="170e2-118">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="170e2-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="170e2-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="170e2-119">Texture1D</span></span>                              | <span data-ttu-id="170e2-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="170e2-120">float</span></span>          |
| <span data-ttu-id="170e2-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="170e2-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="170e2-122">float2</span><span class="sxs-lookup"><span data-stu-id="170e2-122">float2</span></span>         |
| <span data-ttu-id="170e2-123">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="170e2-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="170e2-124">float3</span><span class="sxs-lookup"><span data-stu-id="170e2-124">float3</span></span>         |
| <span data-ttu-id="170e2-125">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="170e2-125">TextureCubeArray</span></span>                       | <span data-ttu-id="170e2-126">float4</span><span class="sxs-lookup"><span data-stu-id="170e2-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="170e2-127">*DDX* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="170e2-127">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="170e2-128">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="170e2-128">Type: **float**</span></span>

<span data-ttu-id="170e2-129">Интенсивность изменения геометрии поверхности в направлении x.</span><span class="sxs-lookup"><span data-stu-id="170e2-129">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="170e2-130">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="170e2-130">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="170e2-131">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="170e2-131">Texture-Object Type</span></span>                      | <span data-ttu-id="170e2-132">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="170e2-132">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="170e2-133">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="170e2-133">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="170e2-134">FLOAT</span><span class="sxs-lookup"><span data-stu-id="170e2-134">float</span></span>          |
| <span data-ttu-id="170e2-135">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="170e2-135">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="170e2-136">float2</span><span class="sxs-lookup"><span data-stu-id="170e2-136">float2</span></span>         |
| <span data-ttu-id="170e2-137">Texture3D, Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="170e2-137">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="170e2-138">float3</span><span class="sxs-lookup"><span data-stu-id="170e2-138">float3</span></span>         |
| <span data-ttu-id="170e2-139">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="170e2-139">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="170e2-140">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="170e2-140">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="170e2-141">*ДДИ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="170e2-141">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="170e2-142">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="170e2-142">Type: **float**</span></span>

<span data-ttu-id="170e2-143">Интенсивность изменения геометрии поверхности в направлении y.</span><span class="sxs-lookup"><span data-stu-id="170e2-143">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="170e2-144">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="170e2-144">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="170e2-145">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="170e2-145">Texture-Object Type</span></span>                      | <span data-ttu-id="170e2-146">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="170e2-146">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="170e2-147">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="170e2-147">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="170e2-148">FLOAT</span><span class="sxs-lookup"><span data-stu-id="170e2-148">float</span></span>          |
| <span data-ttu-id="170e2-149">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="170e2-149">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="170e2-150">float2</span><span class="sxs-lookup"><span data-stu-id="170e2-150">float2</span></span>         |
| <span data-ttu-id="170e2-151">Texture3D, Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="170e2-151">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="170e2-152">float3</span><span class="sxs-lookup"><span data-stu-id="170e2-152">float3</span></span>         |
| <span data-ttu-id="170e2-153">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="170e2-153">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="170e2-154">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="170e2-154">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="170e2-155">*Срез* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="170e2-155">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="170e2-156">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="170e2-156">Type: **float**</span></span>

<span data-ttu-id="170e2-157">Необязательное значение для примера среза Лод значений.</span><span class="sxs-lookup"><span data-stu-id="170e2-157">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="170e2-158">Например, если передать значение среза 2.0 f, вы убедитесь, что ни один из отдельных примеров не имеет доступа к MIP уровню менее 2.0.</span><span class="sxs-lookup"><span data-stu-id="170e2-158">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="170e2-159">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="170e2-159">Return value</span></span>

<span data-ttu-id="170e2-160">Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="170e2-160">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="170e2-161">Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="170e2-161">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="170e2-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="170e2-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="170e2-163">Методы Самплеград</span><span class="sxs-lookup"><span data-stu-id="170e2-163">SampleGrad methods</span></span>](texturecube-samplegrad.md)
</dt> <dt>

[<span data-ttu-id="170e2-164">**текстурекубе**</span><span class="sxs-lookup"><span data-stu-id="170e2-164">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
