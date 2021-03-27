---
title: 'Функция Самплеград:: Самплеград (S, float, float, float, int, float, uint) для Texture1D'
description: Выбор текстуры с помощью градиента, влияющей на способ вычисления расположения выборки, с дополнительным значением для фиксации значений уровня детализации (Лод). Для Texture1D.
ms.assetid: E2B131AC-99E6-493A-91EE-EB0D3EE7FA8B
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
ms.openlocfilehash: 3a5f95a87f46e94c971dd19989ffa670e6993e8f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104000544"
---
# <a name="samplegradsamplegradsfloatfloatfloatintfloatuint-function-for-texture1d"></a><span data-ttu-id="60ea8-105">Функция Самплеград:: Самплеград (S, float, float, float, int, float, uint) для Texture1D</span><span class="sxs-lookup"><span data-stu-id="60ea8-105">SampleGrad::SampleGrad(S,float,float,float,int,float,uint) function for Texture1D</span></span>

<span data-ttu-id="60ea8-106">Выбор текстуры с помощью градиента, влияющей на способ вычисления расположения выборки, с дополнительным значением для фиксации значений уровня детализации (Лод).</span><span class="sxs-lookup"><span data-stu-id="60ea8-106">Samples a texture, using a gradient to influence the way the sample location is calculated, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="60ea8-107">Возвращает состояние операции.</span><span class="sxs-lookup"><span data-stu-id="60ea8-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="60ea8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="60ea8-108">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="60ea8-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="60ea8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60ea8-110">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="60ea8-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60ea8-111">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="60ea8-111">Type: **SamplerState**</span></span>

<span data-ttu-id="60ea8-112">[Состояние образца](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="60ea8-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="60ea8-113">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="60ea8-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="60ea8-114">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="60ea8-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60ea8-115">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="60ea8-115">Type: **float**</span></span>

<span data-ttu-id="60ea8-116">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="60ea8-116">The texture coordinates.</span></span> <span data-ttu-id="60ea8-117">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="60ea8-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="60ea8-118">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="60ea8-118">Texture-Object Type</span></span>                    | <span data-ttu-id="60ea8-119">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="60ea8-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="60ea8-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="60ea8-120">Texture1D</span></span>                              | <span data-ttu-id="60ea8-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="60ea8-121">float</span></span>          |
| <span data-ttu-id="60ea8-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="60ea8-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="60ea8-123">float2</span><span class="sxs-lookup"><span data-stu-id="60ea8-123">float2</span></span>         |
| <span data-ttu-id="60ea8-124">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="60ea8-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="60ea8-125">float3</span><span class="sxs-lookup"><span data-stu-id="60ea8-125">float3</span></span>         |
| <span data-ttu-id="60ea8-126">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="60ea8-126">TextureCubeArray</span></span>                       | <span data-ttu-id="60ea8-127">float4</span><span class="sxs-lookup"><span data-stu-id="60ea8-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="60ea8-128">*DDX* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="60ea8-128">*DDX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60ea8-129">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="60ea8-129">Type: **float**</span></span>

<span data-ttu-id="60ea8-130">Интенсивность изменения геометрии поверхности в направлении x.</span><span class="sxs-lookup"><span data-stu-id="60ea8-130">The rate of change of the surface geometry in the x direction.</span></span> <span data-ttu-id="60ea8-131">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="60ea8-131">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="60ea8-132">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="60ea8-132">Texture-Object Type</span></span>                      | <span data-ttu-id="60ea8-133">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="60ea8-133">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="60ea8-134">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="60ea8-134">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="60ea8-135">FLOAT</span><span class="sxs-lookup"><span data-stu-id="60ea8-135">float</span></span>          |
| <span data-ttu-id="60ea8-136">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="60ea8-136">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="60ea8-137">float2</span><span class="sxs-lookup"><span data-stu-id="60ea8-137">float2</span></span>         |
| <span data-ttu-id="60ea8-138">Texture3D, Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="60ea8-138">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="60ea8-139">float3</span><span class="sxs-lookup"><span data-stu-id="60ea8-139">float3</span></span>         |
| <span data-ttu-id="60ea8-140">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="60ea8-140">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="60ea8-141">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="60ea8-141">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="60ea8-142">*ДДИ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="60ea8-142">*DDY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60ea8-143">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="60ea8-143">Type: **float**</span></span>

<span data-ttu-id="60ea8-144">Интенсивность изменения геометрии поверхности в направлении y.</span><span class="sxs-lookup"><span data-stu-id="60ea8-144">The rate of change of the surface geometry in the y direction.</span></span> <span data-ttu-id="60ea8-145">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="60ea8-145">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="60ea8-146">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="60ea8-146">Texture-Object Type</span></span>                      | <span data-ttu-id="60ea8-147">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="60ea8-147">Parameter Type</span></span> |
|------------------------------------------|----------------|
| <span data-ttu-id="60ea8-148">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="60ea8-148">Texture1D, Texture1DArray</span></span>                | <span data-ttu-id="60ea8-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="60ea8-149">float</span></span>          |
| <span data-ttu-id="60ea8-150">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="60ea8-150">Texture2D, Texture2DArray</span></span>                | <span data-ttu-id="60ea8-151">float2</span><span class="sxs-lookup"><span data-stu-id="60ea8-151">float2</span></span>         |
| <span data-ttu-id="60ea8-152">Texture3D, Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="60ea8-152">Texture3D, TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="60ea8-153">float3</span><span class="sxs-lookup"><span data-stu-id="60ea8-153">float3</span></span>         |
| <span data-ttu-id="60ea8-154">Texture2DMS, Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="60ea8-154">Texture2DMS, Texture2DMSArray</span></span>            | <span data-ttu-id="60ea8-155">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="60ea8-155">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="60ea8-156">*Смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="60ea8-156">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60ea8-157">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="60ea8-157">Type: **int**</span></span>

<span data-ttu-id="60ea8-158">Необязательное Смещение координаты текстуры, которое может использоваться для любого типа объекта текстуры. смещение применяется к расположению перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="60ea8-158">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="60ea8-159">Используйте смещение только с целочисленным миплевел; в противном случае можно получить результаты, которые не могут быть правильно преобразованы в оборудование.</span><span class="sxs-lookup"><span data-stu-id="60ea8-159">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="60ea8-160">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="60ea8-160">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="60ea8-161">Дополнительные сведения см. в разделе [применение целочисленных смещений](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="60ea8-161">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="60ea8-162">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="60ea8-162">Texture-Object Type</span></span>           | <span data-ttu-id="60ea8-163">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="60ea8-163">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="60ea8-164">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="60ea8-164">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="60ea8-165">INT</span><span class="sxs-lookup"><span data-stu-id="60ea8-165">int</span></span>            |
| <span data-ttu-id="60ea8-166">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="60ea8-166">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="60ea8-167">int2</span><span class="sxs-lookup"><span data-stu-id="60ea8-167">int2</span></span>           |
| <span data-ttu-id="60ea8-168">Texture3D</span><span class="sxs-lookup"><span data-stu-id="60ea8-168">Texture3D</span></span>                     | <span data-ttu-id="60ea8-169">int3</span><span class="sxs-lookup"><span data-stu-id="60ea8-169">int3</span></span>           |
| <span data-ttu-id="60ea8-170">Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="60ea8-170">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="60ea8-171">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="60ea8-171">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="60ea8-172">*Срез* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="60ea8-172">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60ea8-173">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="60ea8-173">Type: **float**</span></span>

<span data-ttu-id="60ea8-174">Необязательное значение для примера среза Лод значений.</span><span class="sxs-lookup"><span data-stu-id="60ea8-174">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="60ea8-175">Например, если передать значение среза 2.0 f, вы убедитесь, что ни один из отдельных примеров не имеет доступа к MIP уровню менее 2.0.</span><span class="sxs-lookup"><span data-stu-id="60ea8-175">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="60ea8-176">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="60ea8-176">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60ea8-177">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="60ea8-177">Type: **uint**</span></span>

<span data-ttu-id="60ea8-178">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="60ea8-178">The status of the operation.</span></span> <span data-ttu-id="60ea8-179">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="60ea8-179">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="60ea8-180">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="60ea8-180">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="60ea8-181">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="60ea8-181">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60ea8-182">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="60ea8-182">Return value</span></span>

<span data-ttu-id="60ea8-183">Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="60ea8-183">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="60ea8-184">Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="60ea8-184">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="60ea8-185">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="60ea8-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60ea8-186">Методы Самплеград</span><span class="sxs-lookup"><span data-stu-id="60ea8-186">SampleGrad methods</span></span>](texture1d-samplegrad.md)
</dt> </dl>

 

 
