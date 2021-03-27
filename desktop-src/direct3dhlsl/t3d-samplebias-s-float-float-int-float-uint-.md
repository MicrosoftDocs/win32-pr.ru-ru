---
title: 'Функция Самплебиас:: Самплебиас (S, float, float, int, float, uint) для Texture3D'
description: 'Демонстрирует выбор текстуры после применения значения смещения к уровню mipmap с дополнительным значением для создания среза образцов значений уровня детализации (Лод). | Функция Самплебиас:: Самплебиас (S, float, float, int, float, uint) для Texture3D'
ms.assetid: 87B06414-F1A3-4BC8-B7DE-137B2156CFA7
keywords:
- Функция Самплебиас HLSL
topic_type:
- apiref
api_name:
- SampleBias
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e6155bbd4a3b21b86add57d13bc14a1185c76b73
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104987293"
---
# <a name="samplebiassamplebiassfloatfloatintfloatuint-function-for-texture3d"></a><span data-ttu-id="d238d-105">Функция Самплебиас:: Самплебиас (S, float, float, int, float, uint) для Texture3D</span><span class="sxs-lookup"><span data-stu-id="d238d-105">SampleBias::SampleBias(S,float,float,int,float,uint) function for Texture3D</span></span>

<span data-ttu-id="d238d-106">Демонстрирует выбор текстуры после применения значения смещения к уровню mipmap с дополнительным значением для создания среза образцов значений уровня детализации (Лод).</span><span class="sxs-lookup"><span data-stu-id="d238d-106">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span> <span data-ttu-id="d238d-107">Возвращает состояние операции.</span><span class="sxs-lookup"><span data-stu-id="d238d-107">Returns status about the operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="d238d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d238d-108">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in  SamplerState S,
  in  float        Location,
  in  float        Bias,
  in  int          Offset,
  in  float        Clamp,
  out uint         Status
);
```



## <a name="parameters"></a><span data-ttu-id="d238d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d238d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d238d-110">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="d238d-110">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d238d-111">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="d238d-111">Type: **SamplerState**</span></span>

<span data-ttu-id="d238d-112">[Состояние образца](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="d238d-112">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="d238d-113">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="d238d-113">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="d238d-114">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d238d-114">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d238d-115">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="d238d-115">Type: **float**</span></span>

<span data-ttu-id="d238d-116">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="d238d-116">The texture coordinates.</span></span> <span data-ttu-id="d238d-117">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="d238d-117">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="d238d-118">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="d238d-118">Texture-Object Type</span></span>                    | <span data-ttu-id="d238d-119">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="d238d-119">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="d238d-120">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d238d-120">Texture1D</span></span>                              | <span data-ttu-id="d238d-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="d238d-121">float</span></span>          |
| <span data-ttu-id="d238d-122">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="d238d-122">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="d238d-123">float2</span><span class="sxs-lookup"><span data-stu-id="d238d-123">float2</span></span>         |
| <span data-ttu-id="d238d-124">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="d238d-124">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="d238d-125">float3</span><span class="sxs-lookup"><span data-stu-id="d238d-125">float3</span></span>         |
| <span data-ttu-id="d238d-126">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="d238d-126">TextureCubeArray</span></span>                       | <span data-ttu-id="d238d-127">float4</span><span class="sxs-lookup"><span data-stu-id="d238d-127">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="d238d-128">*Уровень защиты* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d238d-128">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d238d-129">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="d238d-129">Type: **float**</span></span>

<span data-ttu-id="d238d-130">Значение смещения, которое является числом с плавающей запятой от 0,0 до 1,0 включительно, применяется к MIP уровню перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="d238d-130">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="d238d-131">*Смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d238d-131">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d238d-132">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="d238d-132">Type: **int**</span></span>

<span data-ttu-id="d238d-133">Необязательное Смещение координаты текстуры, которое может использоваться для любого типа объекта текстуры. смещение применяется к расположению перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="d238d-133">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="d238d-134">Используйте смещение только с целочисленным миплевел; в противном случае можно получить результаты, которые не могут быть правильно преобразованы в оборудование.</span><span class="sxs-lookup"><span data-stu-id="d238d-134">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="d238d-135">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="d238d-135">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="d238d-136">Дополнительные сведения см. в разделе [применение целочисленных смещений](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="d238d-136">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="d238d-137">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="d238d-137">Texture-Object Type</span></span>           | <span data-ttu-id="d238d-138">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="d238d-138">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="d238d-139">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="d238d-139">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="d238d-140">INT</span><span class="sxs-lookup"><span data-stu-id="d238d-140">int</span></span>            |
| <span data-ttu-id="d238d-141">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="d238d-141">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="d238d-142">int2</span><span class="sxs-lookup"><span data-stu-id="d238d-142">int2</span></span>           |
| <span data-ttu-id="d238d-143">Texture3D</span><span class="sxs-lookup"><span data-stu-id="d238d-143">Texture3D</span></span>                     | <span data-ttu-id="d238d-144">int3</span><span class="sxs-lookup"><span data-stu-id="d238d-144">int3</span></span>           |
| <span data-ttu-id="d238d-145">Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="d238d-145">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="d238d-146">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d238d-146">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="d238d-147">*Срез* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d238d-147">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d238d-148">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="d238d-148">Type: **float**</span></span>

<span data-ttu-id="d238d-149">Необязательное значение для примера среза Лод значений.</span><span class="sxs-lookup"><span data-stu-id="d238d-149">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="d238d-150">Например, если передать значение среза 2.0 f, вы убедитесь, что ни один из отдельных примеров не имеет доступа к MIP уровню менее 2.0.</span><span class="sxs-lookup"><span data-stu-id="d238d-150">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> <dt>

<span data-ttu-id="d238d-151">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d238d-151">*Status* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d238d-152">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="d238d-152">Type: **uint**</span></span>

<span data-ttu-id="d238d-153">Состояние операции.</span><span class="sxs-lookup"><span data-stu-id="d238d-153">The status of the operation.</span></span> <span data-ttu-id="d238d-154">Вы не можете получить доступ к состоянию напрямую; Вместо этого передайте состояние в подставляемую функцию [**чеккакцессфуллимаппед**](checkaccessfullymapped.md) .</span><span class="sxs-lookup"><span data-stu-id="d238d-154">You can't access the status directly; instead, pass the status to the [**CheckAccessFullyMapped**](checkaccessfullymapped.md) intrinsic function.</span></span> <span data-ttu-id="d238d-155">**Чеккакцессфуллимаппед** возвращает **значение true** , если все значения из соответствующего **образца**, **сбора** или операции **загрузки** обращались к сопоставленным плиткам в [мозаичном ресурсе](/windows/desktop/direct3d11/direct3d-11-2-features).</span><span class="sxs-lookup"><span data-stu-id="d238d-155">**CheckAccessFullyMapped** returns **TRUE** if all values from the corresponding **Sample**, **Gather**, or **Load** operation accessed mapped tiles in a [tiled resource](/windows/desktop/direct3d11/direct3d-11-2-features).</span></span> <span data-ttu-id="d238d-156">Если какие бы то ни было значения были взяты из несопоставленной плитки, **чеккакцессфуллимаппед** возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="d238d-156">If any values were taken from an unmapped tile, **CheckAccessFullyMapped** returns **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d238d-157">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d238d-157">Return value</span></span>

<span data-ttu-id="d238d-158">Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="d238d-158">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="d238d-159">Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="d238d-159">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="d238d-160">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d238d-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d238d-161">Методы Самплебиас</span><span class="sxs-lookup"><span data-stu-id="d238d-161">SampleBias methods</span></span>](texture3d-samplebias.md)
</dt> <dt>

[<span data-ttu-id="d238d-162">**Texture3D**</span><span class="sxs-lookup"><span data-stu-id="d238d-162">**Texture3D**</span></span>](sm5-object-texture3d.md)
</dt> </dl>

 

 
