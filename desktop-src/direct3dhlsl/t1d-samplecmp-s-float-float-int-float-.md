---
title: 'Функция Самплекмп:: Самплекмп (S, float, float, int, float) для Texture1D'
description: 'Выбор текстуры с использованием значения сравнения для отклонения выборок с необязательным значением для фиксации значений уровня детализации (Лод) в. | Функция Самплекмп:: Самплекмп (S, float, float, int, float) для Texture1D'
ms.assetid: 91AD0B59-D3F0-4A0D-8825-17282815D64B
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
ms.openlocfilehash: 811636e7e7002afedf026d4e3955f08f647c2c5d
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104998828"
---
# <a name="samplecmpsamplecmpsfloatfloatintfloat-function-for-texture1d"></a><span data-ttu-id="85a5c-105">Функция Самплекмп:: Самплекмп (S, float, float, int, float) для Texture1D</span><span class="sxs-lookup"><span data-stu-id="85a5c-105">SampleCmp::SampleCmp(S,float,float,int,float) function for Texture1D</span></span>

<span data-ttu-id="85a5c-106">Выбор текстуры с использованием значения сравнения для отклонения выборок с необязательным значением для фиксации значений уровня детализации (Лод) в.</span><span class="sxs-lookup"><span data-stu-id="85a5c-106">Samples a texture, using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="85a5c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="85a5c-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmp(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="85a5c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="85a5c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85a5c-109">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="85a5c-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85a5c-110">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="85a5c-110">Type: **SamplerState**</span></span>

<span data-ttu-id="85a5c-111">[Состояние образца](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="85a5c-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="85a5c-112">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="85a5c-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="85a5c-113">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="85a5c-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85a5c-114">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="85a5c-114">Type: **float**</span></span>

<span data-ttu-id="85a5c-115">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="85a5c-115">The texture coordinates.</span></span> <span data-ttu-id="85a5c-116">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="85a5c-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="85a5c-117">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="85a5c-117">Texture-Object Type</span></span>                    | <span data-ttu-id="85a5c-118">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="85a5c-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="85a5c-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="85a5c-119">Texture1D</span></span>                              | <span data-ttu-id="85a5c-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="85a5c-120">float</span></span>          |
| <span data-ttu-id="85a5c-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="85a5c-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="85a5c-122">float2</span><span class="sxs-lookup"><span data-stu-id="85a5c-122">float2</span></span>         |
| <span data-ttu-id="85a5c-123">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="85a5c-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="85a5c-124">float3</span><span class="sxs-lookup"><span data-stu-id="85a5c-124">float3</span></span>         |
| <span data-ttu-id="85a5c-125">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="85a5c-125">TextureCubeArray</span></span>                       | <span data-ttu-id="85a5c-126">float4</span><span class="sxs-lookup"><span data-stu-id="85a5c-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="85a5c-127">*Компаревалуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="85a5c-127">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85a5c-128">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="85a5c-128">Type: **float**</span></span>

<span data-ttu-id="85a5c-129">Значение с плавающей запятой, используемое в качестве значения сравнения.</span><span class="sxs-lookup"><span data-stu-id="85a5c-129">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="85a5c-130">*Смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="85a5c-130">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85a5c-131">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="85a5c-131">Type: **int**</span></span>

<span data-ttu-id="85a5c-132">Необязательное Смещение координаты текстуры, которое может использоваться для любого типа объекта текстуры. смещение применяется к расположению перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="85a5c-132">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="85a5c-133">Используйте смещение только с целочисленным миплевел; в противном случае можно получить результаты, которые не могут быть правильно преобразованы в оборудование.</span><span class="sxs-lookup"><span data-stu-id="85a5c-133">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="85a5c-134">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="85a5c-134">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="85a5c-135">Дополнительные сведения см. в разделе [применение целочисленных смещений](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="85a5c-135">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="85a5c-136">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="85a5c-136">Texture-Object Type</span></span>           | <span data-ttu-id="85a5c-137">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="85a5c-137">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="85a5c-138">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="85a5c-138">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="85a5c-139">INT</span><span class="sxs-lookup"><span data-stu-id="85a5c-139">int</span></span>            |
| <span data-ttu-id="85a5c-140">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="85a5c-140">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="85a5c-141">int2</span><span class="sxs-lookup"><span data-stu-id="85a5c-141">int2</span></span>           |
| <span data-ttu-id="85a5c-142">Texture3D</span><span class="sxs-lookup"><span data-stu-id="85a5c-142">Texture3D</span></span>                     | <span data-ttu-id="85a5c-143">int3</span><span class="sxs-lookup"><span data-stu-id="85a5c-143">int3</span></span>           |
| <span data-ttu-id="85a5c-144">Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="85a5c-144">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="85a5c-145">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="85a5c-145">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="85a5c-146">*Срез* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="85a5c-146">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85a5c-147">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="85a5c-147">Type: **float**</span></span>

<span data-ttu-id="85a5c-148">Необязательное значение для примера среза Лод значений.</span><span class="sxs-lookup"><span data-stu-id="85a5c-148">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="85a5c-149">Например, если передать значение среза 2.0 f, вы убедитесь, что ни один из отдельных примеров не имеет доступа к MIP уровню менее 2.0.</span><span class="sxs-lookup"><span data-stu-id="85a5c-149">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85a5c-150">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="85a5c-150">Return value</span></span>

<span data-ttu-id="85a5c-151">Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="85a5c-151">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="85a5c-152">Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="85a5c-152">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="85a5c-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="85a5c-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85a5c-154">Методы Самплекмп</span><span class="sxs-lookup"><span data-stu-id="85a5c-154">SampleCmp methods</span></span>](texture1d-samplecmp.md)
</dt> </dl>

 

 
