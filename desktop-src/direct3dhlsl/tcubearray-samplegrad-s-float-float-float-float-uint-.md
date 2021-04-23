---
title: 'Функция Самплеград:: Самплеград (S, float, float, float, float, uint) для Текстурекубеаррай'
description: Узнайте, как эта функция выбирает текстуру с помощью градиента, влияющей на способ вычисления расположения выборки, с необязательным значением для фиксации значения уровня детализации (Лод) в. Для Текстурекубеаррай.
ms.assetid: 849FAF04-A133-4E5B-967E-0679AE335CCC
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
ms.openlocfilehash: 00adfb5c7a1a95e5462b1bc524a6c7d86f71c2e8
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104987275"
---
# <a name="samplegradsamplegradsfloatfloatfloatfloatuint-function-for-texturecubearray"></a><span data-ttu-id="2ae7c-105">Функция Самплеград:: Самплеград (S, float, float, float, float, uint) для Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="2ae7c-105">SampleGrad::SampleGrad(S,float,float,float,float,uint) function for TextureCubeArray</span></span>

<span data-ttu-id="2ae7c-106">Выбор текстуры с помощью градиента, влияющей на способ вычисления расположения выборки, с дополнительным значением для фиксации значений уровня детализации (Лод).</span><span class="sxs-lookup"><span data-stu-id="2ae7c-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="2ae7c-107">Возвращает состояние операции.</span><span class="sxs-lookup"><span data-stu-id="2ae7c-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ae7c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2ae7c-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleGrad(
  in  SamplerState S,
  in  float        Location,
  in  float        DDX,
  in  float        DDY,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="2ae7c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="2ae7c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ae7c-110">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="2ae7c-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ae7c-111">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="2ae7c-111">Type: **SamplerState**</span></span>

<span data-ttu-id="2ae7c-112">[Состояние образца](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="2ae7c-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="2ae7c-113">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="2ae7c-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="2ae7c-114">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2ae7c-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ae7c-115">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="2ae7c-115">Type: **float**</span></span>

<span data-ttu-id="2ae7c-116">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="2ae7c-116">The texture coordinates.</span></span> <span data-ttu-id="2ae7c-117">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="2ae7c-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="2ae7c-118">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="2ae7c-118">Texture-Object Type</span></span>                    | <span data-ttu-id="2ae7c-119">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="2ae7c-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="2ae7c-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2ae7c-120">Texture1D</span></span>                              | <span data-ttu-id="2ae7c-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="2ae7c-121">float</span></span>          |
| <span data-ttu-id="2ae7c-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="2ae7c-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="2ae7c-123">float2</span><span class="sxs-lookup"><span data-stu-id="2ae7c-123">float2</span></span>         |
| <span data-ttu-id="2ae7c-124">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="2ae7c-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="2ae7c-125">float3</span><span class="sxs-lookup"><span data-stu-id="2ae7c-125">float3</span></span>         |
| <span data-ttu-id="2ae7c-126">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="2ae7c-126">TextureCubeArray</span></span>                       | <span data-ttu-id="2ae7c-127">float4</span><span class="sxs-lookup"><span data-stu-id="2ae7c-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="2ae7c-128">*DDX* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="2ae7c-128">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ae7c-129">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="2ae7c-129">Type: **float**</span></span>

<span data-ttu-id="2ae7c-130">Интенсивность изменения геометрии поверхности в направлении x.</span><span class="sxs-lookup"><span data-stu-id="2ae7c-130">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="2ae7c-131">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="2ae7c-131">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="2ae7c-132">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="2ae7c-132">Texture-Object Type</span></span>                      | <span data-ttu-id="2ae7c-133">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="2ae7c-133">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="2ae7c-134">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="2ae7c-134">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="2ae7c-135">FLOAT</span><span class="sxs-lookup"><span data-stu-id="2ae7c-135">float</span></span>          |
| <span data-ttu-id="2ae7c-136">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="2ae7c-136">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="2ae7c-137">float2</span><span class="sxs-lookup"><span data-stu-id="2ae7c-137">float2</span></span>         |
| <span data-ttu-id="2ae7c-138">Texture3D, Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="2ae7c-138">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="2ae7c-139">float3</span><span class="sxs-lookup"><span data-stu-id="2ae7c-139">float3</span></span>         |
| <span data-ttu-id="2ae7c-140">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="2ae7c-140">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="2ae7c-141">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="2ae7c-141">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="2ae7c-142">*ДДИ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2ae7c-142">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ae7c-143">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="2ae7c-143">Type: **float**</span></span>

<span data-ttu-id="2ae7c-144">Интенсивность изменения геометрии поверхности в направлении y.</span><span class="sxs-lookup"><span data-stu-id="2ae7c-144">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="2ae7c-145">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="2ae7c-145">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="2ae7c-146">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="2ae7c-146">Texture-Object Type</span></span>                      | <span data-ttu-id="2ae7c-147">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="2ae7c-147">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="2ae7c-148">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="2ae7c-148">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="2ae7c-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="2ae7c-149">float</span></span>          |
| <span data-ttu-id="2ae7c-150">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="2ae7c-150">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="2ae7c-151">float2</span><span class="sxs-lookup"><span data-stu-id="2ae7c-151">float2</span></span>         |
| <span data-ttu-id="2ae7c-152">Texture3D, Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="2ae7c-152">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="2ae7c-153">float3</span><span class="sxs-lookup"><span data-stu-id="2ae7c-153">float3</span></span>         |
| <span data-ttu-id="2ae7c-154">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="2ae7c-154">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="2ae7c-155">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="2ae7c-155">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="2ae7c-156">*Срез* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2ae7c-156">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ae7c-157">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="2ae7c-157">Type: **float**</span></span>

<span data-ttu-id="2ae7c-158">Необязательное значение для примера среза Лод значений.</span><span class="sxs-lookup"><span data-stu-id="2ae7c-158">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="2ae7c-159">Например, если передать значение среза 2.0 f, вы убедитесь, что ни один из отдельных примеров не имеет доступа к MIP уровню менее 2.0.</span><span class="sxs-lookup"><span data-stu-id="2ae7c-159">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="2ae7c-160">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2ae7c-160">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ae7c-161">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="2ae7c-161">Type: **uint**</span></span>

<span data-ttu-id="2ae7c-162">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="2ae7c-162">The status of the operation.</span></span> <span data-ttu-id="2ae7c-163">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="2ae7c-163">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="2ae7c-164">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="2ae7c-164">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="2ae7c-165">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="2ae7c-165">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ae7c-166">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2ae7c-166">Return value</span></span>

<span data-ttu-id="2ae7c-167">Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="2ae7c-167">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="2ae7c-168">Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="2ae7c-168">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="2ae7c-169">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2ae7c-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ae7c-170">Методы Самплеград</span><span class="sxs-lookup"><span data-stu-id="2ae7c-170">SampleGrad methods</span></span>](texturecubearray-samplegrad.md)
</dt> <dt>

[<span data-ttu-id="2ae7c-171">**текстурекубеаррай**</span><span class="sxs-lookup"><span data-stu-id="2ae7c-171">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
