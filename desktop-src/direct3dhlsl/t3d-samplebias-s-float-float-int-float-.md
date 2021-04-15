---
title: 'Функция Самплебиас:: Самплебиас (S, float, float, int, float)'
description: 'Демонстрирует выбор текстуры после применения значения смещения к уровню mipmap с дополнительным значением для создания среза образцов значений уровня детализации (Лод). | Функция Самплебиас:: Самплебиас (S, float, float, int, float)'
ms.assetid: C252F1D1-51F9-48E3-BD74-3B050E0E16E0
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
ms.openlocfilehash: 16cc939de3bffe32dd26380b05eb65afac05114d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986253"
---
# <a name="samplebiassamplebiassfloatfloatintfloat-function"></a><span data-ttu-id="2fa6c-105">Функция Самплебиас:: Самплебиас (S, float, float, int, float)</span><span class="sxs-lookup"><span data-stu-id="2fa6c-105">SampleBias::SampleBias(S,float,float,int,float) function</span></span>

<span data-ttu-id="2fa6c-106">Демонстрирует выбор текстуры после применения значения смещения к уровню mipmap с дополнительным значением для создания среза образцов значений уровня детализации (Лод).</span><span class="sxs-lookup"><span data-stu-id="2fa6c-106">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fa6c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2fa6c-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="2fa6c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2fa6c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fa6c-109">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="2fa6c-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fa6c-110">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="2fa6c-110">Type: **SamplerState**</span></span>

<span data-ttu-id="2fa6c-111">[Состояние образца](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="2fa6c-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="2fa6c-112">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="2fa6c-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="2fa6c-113">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2fa6c-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fa6c-114">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="2fa6c-114">Type: **float**</span></span>

<span data-ttu-id="2fa6c-115">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="2fa6c-115">The texture coordinates.</span></span> <span data-ttu-id="2fa6c-116">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="2fa6c-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="2fa6c-117">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="2fa6c-117">Texture-Object Type</span></span>                    | <span data-ttu-id="2fa6c-118">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="2fa6c-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="2fa6c-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="2fa6c-119">Texture1D</span></span>                              | <span data-ttu-id="2fa6c-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="2fa6c-120">float</span></span>          |
| <span data-ttu-id="2fa6c-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="2fa6c-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="2fa6c-122">float2</span><span class="sxs-lookup"><span data-stu-id="2fa6c-122">float2</span></span>         |
| <span data-ttu-id="2fa6c-123">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="2fa6c-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="2fa6c-124">float3</span><span class="sxs-lookup"><span data-stu-id="2fa6c-124">float3</span></span>         |
| <span data-ttu-id="2fa6c-125">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="2fa6c-125">TextureCubeArray</span></span>                       | <span data-ttu-id="2fa6c-126">float4</span><span class="sxs-lookup"><span data-stu-id="2fa6c-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="2fa6c-127">*Уровень защиты* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2fa6c-127">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fa6c-128">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="2fa6c-128">Type: **float**</span></span>

<span data-ttu-id="2fa6c-129">Значение смещения, которое является числом с плавающей запятой от 0,0 до 1,0 включительно, применяется к MIP уровню перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="2fa6c-129">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="2fa6c-130">*Смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2fa6c-130">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fa6c-131">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="2fa6c-131">Type: **int**</span></span>

<span data-ttu-id="2fa6c-132">Необязательное Смещение координаты текстуры, которое может использоваться для любого типа объекта текстуры. смещение применяется к расположению перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="2fa6c-132">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="2fa6c-133">Используйте смещение только с целочисленным миплевел; в противном случае можно получить результаты, которые не могут быть правильно преобразованы в оборудование.</span><span class="sxs-lookup"><span data-stu-id="2fa6c-133">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="2fa6c-134">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="2fa6c-134">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="2fa6c-135">Дополнительные сведения см. в разделе [применение целочисленных смещений](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="2fa6c-135">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="2fa6c-136">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="2fa6c-136">Texture-Object Type</span></span>           | <span data-ttu-id="2fa6c-137">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="2fa6c-137">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="2fa6c-138">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="2fa6c-138">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="2fa6c-139">INT</span><span class="sxs-lookup"><span data-stu-id="2fa6c-139">int</span></span>            |
| <span data-ttu-id="2fa6c-140">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="2fa6c-140">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="2fa6c-141">int2</span><span class="sxs-lookup"><span data-stu-id="2fa6c-141">int2</span></span>           |
| <span data-ttu-id="2fa6c-142">Texture3D</span><span class="sxs-lookup"><span data-stu-id="2fa6c-142">Texture3D</span></span>                     | <span data-ttu-id="2fa6c-143">int3</span><span class="sxs-lookup"><span data-stu-id="2fa6c-143">int3</span></span>           |
| <span data-ttu-id="2fa6c-144">Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="2fa6c-144">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="2fa6c-145">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="2fa6c-145">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="2fa6c-146">*Срез* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2fa6c-146">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fa6c-147">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="2fa6c-147">Type: **float**</span></span>

<span data-ttu-id="2fa6c-148">Необязательное значение для примера среза Лод значений.</span><span class="sxs-lookup"><span data-stu-id="2fa6c-148">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="2fa6c-149">Например, если передать значение среза 2.0 f, вы убедитесь, что ни один из отдельных примеров не имеет доступа к MIP уровню менее 2.0.</span><span class="sxs-lookup"><span data-stu-id="2fa6c-149">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fa6c-150">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2fa6c-150">Return value</span></span>

<span data-ttu-id="2fa6c-151">Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="2fa6c-151">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="2fa6c-152">Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="2fa6c-152">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="2fa6c-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2fa6c-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fa6c-154">Методы Самплебиас</span><span class="sxs-lookup"><span data-stu-id="2fa6c-154">SampleBias methods</span></span>](texture3d-samplebias.md)
</dt> <dt>

[<span data-ttu-id="2fa6c-155">**Texture3D**</span><span class="sxs-lookup"><span data-stu-id="2fa6c-155">**Texture3D**</span></span>](sm5-object-texture3d.md)
</dt> </dl>

 

 
