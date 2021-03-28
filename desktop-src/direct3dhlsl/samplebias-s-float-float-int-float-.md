---
title: 'Функция Самплебиас:: Самплебиас (S, float, float, int, float)'
description: Пример Texture2D. После применения значения смещения к уровню mipmap с необязательным значением для создания среза образца уровня детализации (Лод) до значения.
ms.assetid: 4E4A1188-DE45-4A43-B54D-4CA2E66707E3
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
ms.openlocfilehash: d91ce53da6dbf2c1e39f23967d1c1dc36085e764
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104070922"
---
# <a name="samplebiassamplebiassfloatfloatintfloat-function"></a><span data-ttu-id="835d5-104">Функция Самплебиас:: Самплебиас (S, float, float, int, float)</span><span class="sxs-lookup"><span data-stu-id="835d5-104">SampleBias::SampleBias(S,float,float,int,float) function</span></span>

<span data-ttu-id="835d5-105">Пример [**Texture2D**](sm5-object-texture2d.md). После применения значения смещения к уровню mipmap с необязательным значением для создания среза образца уровня детализации (Лод) до значения.</span><span class="sxs-lookup"><span data-stu-id="835d5-105">Samples a [**Texture2D**](sm5-object-texture2d.md), after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="835d5-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="835d5-106">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="835d5-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="835d5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="835d5-108">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="835d5-108">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="835d5-109">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="835d5-109">Type: **SamplerState**</span></span>

<span data-ttu-id="835d5-110">[Состояние образца](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="835d5-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="835d5-111">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="835d5-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="835d5-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="835d5-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="835d5-113">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="835d5-113">Type: **float**</span></span>

<span data-ttu-id="835d5-114">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="835d5-114">The texture coordinates.</span></span> <span data-ttu-id="835d5-115">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="835d5-115">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="835d5-116">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="835d5-116">Texture-Object Type</span></span>                    | <span data-ttu-id="835d5-117">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="835d5-117">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="835d5-118">Texture1D</span><span class="sxs-lookup"><span data-stu-id="835d5-118">Texture1D</span></span>                              | <span data-ttu-id="835d5-119">FLOAT</span><span class="sxs-lookup"><span data-stu-id="835d5-119">float</span></span>          |
| <span data-ttu-id="835d5-120">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="835d5-120">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="835d5-121">float2</span><span class="sxs-lookup"><span data-stu-id="835d5-121">float2</span></span>         |
| <span data-ttu-id="835d5-122">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="835d5-122">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="835d5-123">float3</span><span class="sxs-lookup"><span data-stu-id="835d5-123">float3</span></span>         |
| <span data-ttu-id="835d5-124">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="835d5-124">TextureCubeArray</span></span>                       | <span data-ttu-id="835d5-125">float4</span><span class="sxs-lookup"><span data-stu-id="835d5-125">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="835d5-126">*Уровень защиты* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="835d5-126">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="835d5-127">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="835d5-127">Type: **float**</span></span>

<span data-ttu-id="835d5-128">Значение смещения, которое является числом с плавающей запятой от 0,0 до 1,0 включительно, применяется к MIP уровню перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="835d5-128">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="835d5-129">*Смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="835d5-129">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="835d5-130">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="835d5-130">Type: **int**</span></span>

<span data-ttu-id="835d5-131">Необязательное Смещение координаты текстуры, которое может использоваться для любого типа объекта текстуры. смещение применяется к расположению перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="835d5-131">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="835d5-132">Используйте смещение только с целочисленным миплевел; в противном случае можно получить результаты, которые не могут быть правильно преобразованы в оборудование.</span><span class="sxs-lookup"><span data-stu-id="835d5-132">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="835d5-133">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="835d5-133">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="835d5-134">Дополнительные сведения см. в разделе [применение целочисленных смещений](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="835d5-134">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="835d5-135">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="835d5-135">Texture-Object Type</span></span>           | <span data-ttu-id="835d5-136">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="835d5-136">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="835d5-137">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="835d5-137">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="835d5-138">INT</span><span class="sxs-lookup"><span data-stu-id="835d5-138">int</span></span>            |
| <span data-ttu-id="835d5-139">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="835d5-139">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="835d5-140">int2</span><span class="sxs-lookup"><span data-stu-id="835d5-140">int2</span></span>           |
| <span data-ttu-id="835d5-141">Texture3D</span><span class="sxs-lookup"><span data-stu-id="835d5-141">Texture3D</span></span>                     | <span data-ttu-id="835d5-142">int3</span><span class="sxs-lookup"><span data-stu-id="835d5-142">int3</span></span>           |
| <span data-ttu-id="835d5-143">Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="835d5-143">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="835d5-144">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="835d5-144">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="835d5-145">*Срез* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="835d5-145">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="835d5-146">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="835d5-146">Type: **float**</span></span>

<span data-ttu-id="835d5-147">Необязательное значение для примера среза Лод значений.</span><span class="sxs-lookup"><span data-stu-id="835d5-147">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="835d5-148">Например, если передать значение среза 2.0 f, вы убедитесь, что ни один из отдельных примеров не имеет доступа к MIP уровню менее 2.0.</span><span class="sxs-lookup"><span data-stu-id="835d5-148">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="835d5-149">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="835d5-149">Return value</span></span>

<span data-ttu-id="835d5-150">Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="835d5-150">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="835d5-151">Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="835d5-151">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="835d5-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="835d5-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="835d5-153">Методы Самплебиас</span><span class="sxs-lookup"><span data-stu-id="835d5-153">SampleBias methods</span></span>](texture2d-samplebias.md)
</dt> </dl>

 

 
