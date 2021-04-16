---
title: 'Функция Самплебиас:: Самплебиас (S, float, float, int, float) для Texture3D'
description: 'Функция Самплебиас:: Самплебиас (S, float, float, int, float) для Texture3D выбирает текстуру после применения значения смещения к уровню mipmap.'
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
ms.openlocfilehash: c7ef038a3faa4cb0a208e9a9d05de230d2b87231
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187921"
---
# <a name="samplebiassamplebiassfloatfloatintfloat-function-for-texture3d"></a><span data-ttu-id="3acff-104">Функция Самплебиас:: Самплебиас (S, float, float, int, float) для Texture3D</span><span class="sxs-lookup"><span data-stu-id="3acff-104">SampleBias::SampleBias(S,float,float,int,float) function for Texture3D</span></span>

<span data-ttu-id="3acff-105">Демонстрирует выбор текстуры после применения значения смещения к уровню mipmap с дополнительным значением для создания среза образцов значений уровня детализации (Лод).</span><span class="sxs-lookup"><span data-stu-id="3acff-105">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="3acff-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3acff-106">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="3acff-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3acff-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3acff-108">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="3acff-108">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3acff-109">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="3acff-109">Type: **SamplerState**</span></span>

<span data-ttu-id="3acff-110">[Состояние образца](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="3acff-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="3acff-111">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="3acff-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="3acff-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3acff-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3acff-113">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="3acff-113">Type: **float**</span></span>

<span data-ttu-id="3acff-114">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="3acff-114">The texture coordinates.</span></span> <span data-ttu-id="3acff-115">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="3acff-115">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="3acff-116">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="3acff-116">Texture-Object Type</span></span>                    | <span data-ttu-id="3acff-117">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="3acff-117">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="3acff-118">Texture1D</span><span class="sxs-lookup"><span data-stu-id="3acff-118">Texture1D</span></span>                              | <span data-ttu-id="3acff-119">FLOAT</span><span class="sxs-lookup"><span data-stu-id="3acff-119">float</span></span>          |
| <span data-ttu-id="3acff-120">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="3acff-120">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="3acff-121">float2</span><span class="sxs-lookup"><span data-stu-id="3acff-121">float2</span></span>         |
| <span data-ttu-id="3acff-122">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="3acff-122">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="3acff-123">float3</span><span class="sxs-lookup"><span data-stu-id="3acff-123">float3</span></span>         |
| <span data-ttu-id="3acff-124">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="3acff-124">TextureCubeArray</span></span>                       | <span data-ttu-id="3acff-125">float4</span><span class="sxs-lookup"><span data-stu-id="3acff-125">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="3acff-126">*Уровень защиты* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3acff-126">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3acff-127">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="3acff-127">Type: **float**</span></span>

<span data-ttu-id="3acff-128">Значение смещения, которое является числом с плавающей запятой от 0,0 до 1,0 включительно, применяется к MIP уровню перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="3acff-128">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="3acff-129">*Смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3acff-129">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3acff-130">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="3acff-130">Type: **int**</span></span>

<span data-ttu-id="3acff-131">Необязательное Смещение координаты текстуры, которое может использоваться для любого типа объекта текстуры. смещение применяется к расположению перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="3acff-131">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="3acff-132">Используйте смещение только с целочисленным миплевел; в противном случае можно получить результаты, которые не могут быть правильно преобразованы в оборудование.</span><span class="sxs-lookup"><span data-stu-id="3acff-132">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="3acff-133">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="3acff-133">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="3acff-134">Дополнительные сведения см. в разделе [применение целочисленных смещений](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="3acff-134">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="3acff-135">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="3acff-135">Texture-Object Type</span></span>           | <span data-ttu-id="3acff-136">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="3acff-136">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="3acff-137">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="3acff-137">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="3acff-138">INT</span><span class="sxs-lookup"><span data-stu-id="3acff-138">int</span></span>            |
| <span data-ttu-id="3acff-139">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="3acff-139">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="3acff-140">int2</span><span class="sxs-lookup"><span data-stu-id="3acff-140">int2</span></span>           |
| <span data-ttu-id="3acff-141">Texture3D</span><span class="sxs-lookup"><span data-stu-id="3acff-141">Texture3D</span></span>                     | <span data-ttu-id="3acff-142">int3</span><span class="sxs-lookup"><span data-stu-id="3acff-142">int3</span></span>           |
| <span data-ttu-id="3acff-143">Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="3acff-143">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="3acff-144">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3acff-144">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="3acff-145">*Срез* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3acff-145">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3acff-146">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="3acff-146">Type: **float**</span></span>

<span data-ttu-id="3acff-147">Необязательное значение для примера среза Лод значений.</span><span class="sxs-lookup"><span data-stu-id="3acff-147">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="3acff-148">Например, если передать значение среза 2.0 f, вы убедитесь, что ни один из отдельных примеров не имеет доступа к MIP уровню менее 2.0.</span><span class="sxs-lookup"><span data-stu-id="3acff-148">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3acff-149">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3acff-149">Return value</span></span>

<span data-ttu-id="3acff-150">Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="3acff-150">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="3acff-151">Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="3acff-151">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="3acff-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3acff-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3acff-153">Методы Самплебиас</span><span class="sxs-lookup"><span data-stu-id="3acff-153">SampleBias methods</span></span>](texture3d-samplebias.md)
</dt> <dt>

[<span data-ttu-id="3acff-154">**Texture3D**</span><span class="sxs-lookup"><span data-stu-id="3acff-154">**Texture3D**</span></span>](sm5-object-texture3d.md)
</dt> </dl>

 

 
