---
title: 'Функция Самплеград:: Самплеград (S, float, float, float, float, uint) для Текстурекубе'
description: Выбор текстуры с помощью градиента, влияющей на способ вычисления расположения выборки, с дополнительным значением для фиксации значений уровня детализации (Лод). Для Текстурекубе.
ms.assetid: 36DF7846-416A-4F2F-A7F8-44EE768CDEE1
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
ms.openlocfilehash: 3e75bccaeac28aefc50620a5dea31fa62b880332
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104548151"
---
# <a name="samplegradsamplegradsfloatfloatfloatfloatuint-function-for-texturecube"></a><span data-ttu-id="a5e76-105">Функция Самплеград:: Самплеград (S, float, float, float, float, uint) для Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="a5e76-105">SampleGrad::SampleGrad(S,float,float,float,float,uint) function for TextureCube</span></span>

<span data-ttu-id="a5e76-106">Выбор текстуры с помощью градиента, влияющей на способ вычисления расположения выборки, с дополнительным значением для фиксации значений уровня детализации (Лод).</span><span class="sxs-lookup"><span data-stu-id="a5e76-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="a5e76-107">Возвращает состояние операции.</span><span class="sxs-lookup"><span data-stu-id="a5e76-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5e76-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a5e76-108">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="a5e76-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a5e76-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5e76-110">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="a5e76-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5e76-111">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="a5e76-111">Type: **SamplerState**</span></span>

<span data-ttu-id="a5e76-112">[Состояние образца](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="a5e76-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="a5e76-113">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="a5e76-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="a5e76-114">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a5e76-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5e76-115">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="a5e76-115">Type: **float**</span></span>

<span data-ttu-id="a5e76-116">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="a5e76-116">The texture coordinates.</span></span> <span data-ttu-id="a5e76-117">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="a5e76-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="a5e76-118">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="a5e76-118">Texture-Object Type</span></span>                    | <span data-ttu-id="a5e76-119">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="a5e76-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="a5e76-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a5e76-120">Texture1D</span></span>                              | <span data-ttu-id="a5e76-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="a5e76-121">float</span></span>          |
| <span data-ttu-id="a5e76-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="a5e76-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="a5e76-123">float2</span><span class="sxs-lookup"><span data-stu-id="a5e76-123">float2</span></span>         |
| <span data-ttu-id="a5e76-124">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="a5e76-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="a5e76-125">float3</span><span class="sxs-lookup"><span data-stu-id="a5e76-125">float3</span></span>         |
| <span data-ttu-id="a5e76-126">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="a5e76-126">TextureCubeArray</span></span>                       | <span data-ttu-id="a5e76-127">float4</span><span class="sxs-lookup"><span data-stu-id="a5e76-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="a5e76-128">*DDX* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="a5e76-128">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5e76-129">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="a5e76-129">Type: **float**</span></span>

<span data-ttu-id="a5e76-130">Интенсивность изменения геометрии поверхности в направлении x.</span><span class="sxs-lookup"><span data-stu-id="a5e76-130">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="a5e76-131">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="a5e76-131">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="a5e76-132">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="a5e76-132">Texture-Object Type</span></span>                      | <span data-ttu-id="a5e76-133">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="a5e76-133">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="a5e76-134">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="a5e76-134">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="a5e76-135">FLOAT</span><span class="sxs-lookup"><span data-stu-id="a5e76-135">float</span></span>          |
| <span data-ttu-id="a5e76-136">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="a5e76-136">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="a5e76-137">float2</span><span class="sxs-lookup"><span data-stu-id="a5e76-137">float2</span></span>         |
| <span data-ttu-id="a5e76-138">Texture3D, Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="a5e76-138">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="a5e76-139">float3</span><span class="sxs-lookup"><span data-stu-id="a5e76-139">float3</span></span>         |
| <span data-ttu-id="a5e76-140">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="a5e76-140">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="a5e76-141">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a5e76-141">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="a5e76-142">*ДДИ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a5e76-142">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5e76-143">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="a5e76-143">Type: **float**</span></span>

<span data-ttu-id="a5e76-144">Интенсивность изменения геометрии поверхности в направлении y.</span><span class="sxs-lookup"><span data-stu-id="a5e76-144">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="a5e76-145">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="a5e76-145">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="a5e76-146">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="a5e76-146">Texture-Object Type</span></span>                      | <span data-ttu-id="a5e76-147">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="a5e76-147">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="a5e76-148">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="a5e76-148">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="a5e76-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="a5e76-149">float</span></span>          |
| <span data-ttu-id="a5e76-150">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="a5e76-150">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="a5e76-151">float2</span><span class="sxs-lookup"><span data-stu-id="a5e76-151">float2</span></span>         |
| <span data-ttu-id="a5e76-152">Texture3D, Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="a5e76-152">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="a5e76-153">float3</span><span class="sxs-lookup"><span data-stu-id="a5e76-153">float3</span></span>         |
| <span data-ttu-id="a5e76-154">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="a5e76-154">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="a5e76-155">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a5e76-155">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="a5e76-156">*Срез* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a5e76-156">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5e76-157">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="a5e76-157">Type: **float**</span></span>

<span data-ttu-id="a5e76-158">Необязательное значение для примера среза Лод значений.</span><span class="sxs-lookup"><span data-stu-id="a5e76-158">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="a5e76-159">Например, если передать значение среза 2.0 f, вы убедитесь, что ни один из отдельных примеров не имеет доступа к MIP уровню менее 2.0.</span><span class="sxs-lookup"><span data-stu-id="a5e76-159">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="a5e76-160">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a5e76-160">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5e76-161">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="a5e76-161">Type: **uint**</span></span>

<span data-ttu-id="a5e76-162">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="a5e76-162">The status of the operation.</span></span> <span data-ttu-id="a5e76-163">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="a5e76-163">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="a5e76-164">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="a5e76-164">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="a5e76-165">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="a5e76-165">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5e76-166">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a5e76-166">Return value</span></span>

<span data-ttu-id="a5e76-167">Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="a5e76-167">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="a5e76-168">Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="a5e76-168">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="a5e76-169">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a5e76-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5e76-170">Методы Самплеград</span><span class="sxs-lookup"><span data-stu-id="a5e76-170">SampleGrad methods</span></span>](texturecube-samplegrad.md)
</dt> <dt>

[<span data-ttu-id="a5e76-171">**текстурекубе**</span><span class="sxs-lookup"><span data-stu-id="a5e76-171">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
