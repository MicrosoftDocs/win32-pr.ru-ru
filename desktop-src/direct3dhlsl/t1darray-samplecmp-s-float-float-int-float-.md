---
title: 'Функция Самплекмп:: Самплекмп (S, float, float, int, float) для Texture1DArray'
description: 'Эта функция выбирает текстуру, используя значение сравнения для отклонения выборок, с необязательным значением для фиксации образцов значений уровня детализации (Лод) до. | Функция Самплекмп:: Самплекмп (S, float, float, int, float) для Texture1DArray'
ms.assetid: D4EF2ADB-202A-4258-BCCD-524567A42A90
keywords:
- Функция Самплекмп HLSL
topic_type:
- apiref
api_name:
- SampleCmp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3c703c971bfddcda5dbd28978f5743e07b2e6be7
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104998813"
---
# <a name="samplecmpsamplecmpsfloatfloatintfloat-function-for-texture1darray"></a><span data-ttu-id="bb36d-105">Функция Самплекмп:: Самплекмп (S, float, float, int, float) для Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="bb36d-105">SampleCmp::SampleCmp(S,float,float,int,float) function for Texture1DArray</span></span>

<span data-ttu-id="bb36d-106">Выбор текстуры с использованием значения сравнения для отклонения выборок с необязательным значением для фиксации значений уровня детализации (Лод) в.</span><span class="sxs-lookup"><span data-stu-id="bb36d-106">Samples a texture, using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb36d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bb36d-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmp(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="bb36d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="bb36d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb36d-109">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="bb36d-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb36d-110">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="bb36d-110">Type: **SamplerState**</span></span>

<span data-ttu-id="bb36d-111">[Состояние образца](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="bb36d-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="bb36d-112">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="bb36d-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="bb36d-113">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bb36d-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb36d-114">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="bb36d-114">Type: **float**</span></span>

<span data-ttu-id="bb36d-115">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="bb36d-115">The texture coordinates.</span></span> <span data-ttu-id="bb36d-116">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="bb36d-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="bb36d-117">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="bb36d-117">Texture-Object Type</span></span>                    | <span data-ttu-id="bb36d-118">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="bb36d-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="bb36d-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="bb36d-119">Texture1D</span></span>                              | <span data-ttu-id="bb36d-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="bb36d-120">float</span></span>          |
| <span data-ttu-id="bb36d-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="bb36d-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="bb36d-122">float2</span><span class="sxs-lookup"><span data-stu-id="bb36d-122">float2</span></span>         |
| <span data-ttu-id="bb36d-123">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="bb36d-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="bb36d-124">float3</span><span class="sxs-lookup"><span data-stu-id="bb36d-124">float3</span></span>         |
| <span data-ttu-id="bb36d-125">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="bb36d-125">TextureCubeArray</span></span>                       | <span data-ttu-id="bb36d-126">float4</span><span class="sxs-lookup"><span data-stu-id="bb36d-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="bb36d-127">*Компаревалуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bb36d-127">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb36d-128">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="bb36d-128">Type: **float**</span></span>

<span data-ttu-id="bb36d-129">Значение с плавающей запятой, используемое в качестве значения сравнения.</span><span class="sxs-lookup"><span data-stu-id="bb36d-129">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="bb36d-130">*Смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bb36d-130">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb36d-131">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="bb36d-131">Type: **int**</span></span>

<span data-ttu-id="bb36d-132">Необязательное Смещение координаты текстуры, которое может использоваться для любого типа объекта текстуры. смещение применяется к расположению перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="bb36d-132">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="bb36d-133">Используйте смещение только с целочисленным миплевел; в противном случае можно получить результаты, которые не могут быть правильно преобразованы в оборудование.</span><span class="sxs-lookup"><span data-stu-id="bb36d-133">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="bb36d-134">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="bb36d-134">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="bb36d-135">Дополнительные сведения см. в разделе [применение целочисленных смещений](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="bb36d-135">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="bb36d-136">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="bb36d-136">Texture-Object Type</span></span>           | <span data-ttu-id="bb36d-137">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="bb36d-137">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="bb36d-138">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="bb36d-138">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="bb36d-139">INT</span><span class="sxs-lookup"><span data-stu-id="bb36d-139">int</span></span>            |
| <span data-ttu-id="bb36d-140">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="bb36d-140">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="bb36d-141">int2</span><span class="sxs-lookup"><span data-stu-id="bb36d-141">int2</span></span>           |
| <span data-ttu-id="bb36d-142">Texture3D</span><span class="sxs-lookup"><span data-stu-id="bb36d-142">Texture3D</span></span>                     | <span data-ttu-id="bb36d-143">int3</span><span class="sxs-lookup"><span data-stu-id="bb36d-143">int3</span></span>           |
| <span data-ttu-id="bb36d-144">Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="bb36d-144">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="bb36d-145">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="bb36d-145">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="bb36d-146">*Срез* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bb36d-146">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb36d-147">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="bb36d-147">Type: **float**</span></span>

<span data-ttu-id="bb36d-148">Необязательное значение для примера среза Лод значений.</span><span class="sxs-lookup"><span data-stu-id="bb36d-148">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="bb36d-149">Например, если передать значение среза 2.0 f, вы убедитесь, что ни один из отдельных примеров не имеет доступа к MIP уровню менее 2.0.</span><span class="sxs-lookup"><span data-stu-id="bb36d-149">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb36d-150">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bb36d-150">Return value</span></span>

<span data-ttu-id="bb36d-151">Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="bb36d-151">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="bb36d-152">Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="bb36d-152">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="bb36d-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bb36d-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb36d-154">Методы Самплекмп</span><span class="sxs-lookup"><span data-stu-id="bb36d-154">SampleCmp methods</span></span>](texture1darray-samplecmp.md)
</dt> </dl>

 

 
