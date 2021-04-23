---
title: 'Функция Самплеград:: Самплеград (S, float, float, float, int, float, uint) для Texture2DArray'
description: Узнайте, как эта функция выбирает текстуру с помощью градиента, влияющей на способ вычисления расположения образца. Для Texture2DArray.
ms.assetid: 71CC8747-8684-4ABD-8B7A-E02889048261
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
ms.openlocfilehash: 3d6c46deb14c3a2c3554052ecc3e6625b13b2848
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104998837"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloatuint-function-for-texture2darray"></a><span data-ttu-id="4f683-105">Функция Самплеград:: Самплеград (S, float, float, float, int, float, uint) для Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="4f683-105">SampleGrad::SampleGrad(S,float,float,float,int,float,uint) function for Texture2DArray</span></span>

<span data-ttu-id="4f683-106">Выбор текстуры с помощью градиента, влияющей на способ вычисления расположения выборки, с дополнительным значением для фиксации значений уровня детализации (Лод).</span><span class="sxs-lookup"><span data-stu-id="4f683-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="4f683-107">Возвращает состояние операции.</span><span class="sxs-lookup"><span data-stu-id="4f683-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f683-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4f683-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleGrad(
  in  SamplerState S,
  in  float        Location,
  in  float        DDX,
  in  float        DDY,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="4f683-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4f683-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f683-110">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="4f683-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f683-111">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="4f683-111">Type: **SamplerState**</span></span>

<span data-ttu-id="4f683-112">[Состояние образца](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="4f683-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="4f683-113">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="4f683-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="4f683-114">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4f683-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f683-115">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="4f683-115">Type: **float**</span></span>

<span data-ttu-id="4f683-116">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="4f683-116">The texture coordinates.</span></span> <span data-ttu-id="4f683-117">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="4f683-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="4f683-118">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="4f683-118">Texture-Object Type</span></span>                    | <span data-ttu-id="4f683-119">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="4f683-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="4f683-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="4f683-120">Texture1D</span></span>                              | <span data-ttu-id="4f683-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4f683-121">float</span></span>          |
| <span data-ttu-id="4f683-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="4f683-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="4f683-123">float2</span><span class="sxs-lookup"><span data-stu-id="4f683-123">float2</span></span>         |
| <span data-ttu-id="4f683-124">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="4f683-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="4f683-125">float3</span><span class="sxs-lookup"><span data-stu-id="4f683-125">float3</span></span>         |
| <span data-ttu-id="4f683-126">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="4f683-126">TextureCubeArray</span></span>                       | <span data-ttu-id="4f683-127">float4</span><span class="sxs-lookup"><span data-stu-id="4f683-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="4f683-128">*DDX* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="4f683-128">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f683-129">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="4f683-129">Type: **float**</span></span>

<span data-ttu-id="4f683-130">Интенсивность изменения геометрии поверхности в направлении x.</span><span class="sxs-lookup"><span data-stu-id="4f683-130">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="4f683-131">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="4f683-131">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="4f683-132">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="4f683-132">Texture-Object Type</span></span>                      | <span data-ttu-id="4f683-133">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="4f683-133">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="4f683-134">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="4f683-134">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="4f683-135">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4f683-135">float</span></span>          |
| <span data-ttu-id="4f683-136">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="4f683-136">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="4f683-137">float2</span><span class="sxs-lookup"><span data-stu-id="4f683-137">float2</span></span>         |
| <span data-ttu-id="4f683-138">Texture3D, Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="4f683-138">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="4f683-139">float3</span><span class="sxs-lookup"><span data-stu-id="4f683-139">float3</span></span>         |
| <span data-ttu-id="4f683-140">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="4f683-140">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="4f683-141">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4f683-141">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="4f683-142">*ДДИ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4f683-142">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f683-143">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="4f683-143">Type: **float**</span></span>

<span data-ttu-id="4f683-144">Интенсивность изменения геометрии поверхности в направлении y.</span><span class="sxs-lookup"><span data-stu-id="4f683-144">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="4f683-145">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="4f683-145">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="4f683-146">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="4f683-146">Texture-Object Type</span></span>                      | <span data-ttu-id="4f683-147">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="4f683-147">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="4f683-148">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="4f683-148">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="4f683-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4f683-149">float</span></span>          |
| <span data-ttu-id="4f683-150">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="4f683-150">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="4f683-151">float2</span><span class="sxs-lookup"><span data-stu-id="4f683-151">float2</span></span>         |
| <span data-ttu-id="4f683-152">Texture3D, Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="4f683-152">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="4f683-153">float3</span><span class="sxs-lookup"><span data-stu-id="4f683-153">float3</span></span>         |
| <span data-ttu-id="4f683-154">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="4f683-154">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="4f683-155">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4f683-155">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="4f683-156">*Смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4f683-156">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f683-157">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="4f683-157">Type: **int**</span></span>

<span data-ttu-id="4f683-158">Необязательное Смещение координаты текстуры, которое может использоваться для любого типа объекта текстуры. смещение применяется к расположению перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="4f683-158">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="4f683-159">Используйте смещение только с целочисленным миплевел; в противном случае можно получить результаты, которые не могут быть правильно преобразованы в оборудование.</span><span class="sxs-lookup"><span data-stu-id="4f683-159">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="4f683-160">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="4f683-160">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="4f683-161">Дополнительные сведения см. в разделе [применение целочисленных смещений](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="4f683-161">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="4f683-162">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="4f683-162">Texture-Object Type</span></span>           | <span data-ttu-id="4f683-163">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="4f683-163">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="4f683-164">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="4f683-164">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="4f683-165">INT</span><span class="sxs-lookup"><span data-stu-id="4f683-165">int</span></span>            |
| <span data-ttu-id="4f683-166">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="4f683-166">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="4f683-167">int2</span><span class="sxs-lookup"><span data-stu-id="4f683-167">int2</span></span>           |
| <span data-ttu-id="4f683-168">Texture3D</span><span class="sxs-lookup"><span data-stu-id="4f683-168">Texture3D</span></span>                     | <span data-ttu-id="4f683-169">int3</span><span class="sxs-lookup"><span data-stu-id="4f683-169">int3</span></span>           |
| <span data-ttu-id="4f683-170">Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="4f683-170">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="4f683-171">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4f683-171">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="4f683-172">*Срез* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4f683-172">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f683-173">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="4f683-173">Type: **float**</span></span>

<span data-ttu-id="4f683-174">Необязательное значение для примера среза Лод значений.</span><span class="sxs-lookup"><span data-stu-id="4f683-174">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="4f683-175">Например, если передать значение среза 2.0 f, вы убедитесь, что ни один из отдельных примеров не имеет доступа к MIP уровню менее 2.0.</span><span class="sxs-lookup"><span data-stu-id="4f683-175">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="4f683-176">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4f683-176">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f683-177">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="4f683-177">Type: **uint**</span></span>

<span data-ttu-id="4f683-178">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="4f683-178">The status of the operation.</span></span> <span data-ttu-id="4f683-179">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="4f683-179">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="4f683-180">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="4f683-180">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="4f683-181">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="4f683-181">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f683-182">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4f683-182">Return value</span></span>

<span data-ttu-id="4f683-183">Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="4f683-183">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="4f683-184">Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="4f683-184">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="4f683-185">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4f683-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f683-186">Методы Самплеград</span><span class="sxs-lookup"><span data-stu-id="4f683-186">SampleGrad methods</span></span>](texture2darray-samplegrad.md)
</dt> <dt>

[<span data-ttu-id="4f683-187">**Texture2DArray**</span><span class="sxs-lookup"><span data-stu-id="4f683-187">**Texture2DArray**</span></span>](sm5-object-texture2darray.md)
</dt> </dl>

 

 
