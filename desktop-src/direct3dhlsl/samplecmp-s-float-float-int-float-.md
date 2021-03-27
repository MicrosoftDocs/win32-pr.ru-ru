---
title: 'Функция Самплекмп:: Самплекмп (S, float, float, int, float) для Texture2D'
description: Эта функция выбирает Texture2D, используя значение сравнения для отклонения выборок, с необязательным значением для фиксации значений уровня детализации (Лод) в.
ms.assetid: 1B5E6559-2524-4557-8F43-7AF258C39FB2
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
ms.openlocfilehash: 9df6a84fff7c6988ed9333584a7196fa06ad30ec
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104987377"
---
# <a name="samplecmpsamplecmpsfloatfloatintfloat-function-for-texture2d"></a><span data-ttu-id="f2825-104">Функция Самплекмп:: Самплекмп (S, float, float, int, float) для Texture2D</span><span class="sxs-lookup"><span data-stu-id="f2825-104">SampleCmp::SampleCmp(S,float,float,int,float) function for Texture2D</span></span>

<span data-ttu-id="f2825-105">Примеры [**Texture2D**](sm5-object-texture2d.md)с использованием значения сравнения для отклонения выборок с необязательным значением для фиксации значений уровня детализации (Лод) в.</span><span class="sxs-lookup"><span data-stu-id="f2825-105">Samples a [**Texture2D**](sm5-object-texture2d.md), using a comparison value to reject samples, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2825-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f2825-106">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleCmp(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="f2825-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f2825-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2825-108">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="f2825-108">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2825-109">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="f2825-109">Type: **SamplerState**</span></span>

<span data-ttu-id="f2825-110">[Состояние образца](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="f2825-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="f2825-111">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="f2825-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="f2825-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f2825-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2825-113">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="f2825-113">Type: **float**</span></span>

<span data-ttu-id="f2825-114">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="f2825-114">The texture coordinates.</span></span> <span data-ttu-id="f2825-115">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="f2825-115">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="f2825-116">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="f2825-116">Texture-Object Type</span></span>                    | <span data-ttu-id="f2825-117">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="f2825-117">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="f2825-118">Texture1D</span><span class="sxs-lookup"><span data-stu-id="f2825-118">Texture1D</span></span>                              | <span data-ttu-id="f2825-119">FLOAT</span><span class="sxs-lookup"><span data-stu-id="f2825-119">float</span></span>          |
| <span data-ttu-id="f2825-120">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="f2825-120">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="f2825-121">float2</span><span class="sxs-lookup"><span data-stu-id="f2825-121">float2</span></span>         |
| <span data-ttu-id="f2825-122">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="f2825-122">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="f2825-123">float3</span><span class="sxs-lookup"><span data-stu-id="f2825-123">float3</span></span>         |
| <span data-ttu-id="f2825-124">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="f2825-124">TextureCubeArray</span></span>                       | <span data-ttu-id="f2825-125">float4</span><span class="sxs-lookup"><span data-stu-id="f2825-125">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="f2825-126">*Компаревалуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f2825-126">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2825-127">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="f2825-127">Type: **float**</span></span>

<span data-ttu-id="f2825-128">Значение с плавающей запятой, используемое в качестве значения сравнения.</span><span class="sxs-lookup"><span data-stu-id="f2825-128">A floating-point value to use as a comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="f2825-129">*Смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f2825-129">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2825-130">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="f2825-130">Type: **int**</span></span>

<span data-ttu-id="f2825-131">Необязательное Смещение координаты текстуры, которое может использоваться для любого типа объекта текстуры. смещение применяется к расположению перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="f2825-131">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="f2825-132">Используйте смещение только с целочисленным миплевел; в противном случае можно получить результаты, которые не могут быть правильно преобразованы в оборудование.</span><span class="sxs-lookup"><span data-stu-id="f2825-132">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="f2825-133">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="f2825-133">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="f2825-134">Дополнительные сведения см. в разделе [применение целочисленных смещений](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="f2825-134">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="f2825-135">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="f2825-135">Texture-Object Type</span></span>           | <span data-ttu-id="f2825-136">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="f2825-136">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="f2825-137">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="f2825-137">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="f2825-138">INT</span><span class="sxs-lookup"><span data-stu-id="f2825-138">int</span></span>            |
| <span data-ttu-id="f2825-139">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="f2825-139">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="f2825-140">int2</span><span class="sxs-lookup"><span data-stu-id="f2825-140">int2</span></span>           |
| <span data-ttu-id="f2825-141">Texture3D</span><span class="sxs-lookup"><span data-stu-id="f2825-141">Texture3D</span></span>                     | <span data-ttu-id="f2825-142">int3</span><span class="sxs-lookup"><span data-stu-id="f2825-142">int3</span></span>           |
| <span data-ttu-id="f2825-143">Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="f2825-143">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="f2825-144">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f2825-144">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="f2825-145">*Срез* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f2825-145">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2825-146">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="f2825-146">Type: **float**</span></span>

<span data-ttu-id="f2825-147">Необязательное значение для примера среза Лод значений.</span><span class="sxs-lookup"><span data-stu-id="f2825-147">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="f2825-148">Например, если передать значение среза 2.0 f, вы убедитесь, что ни один из отдельных примеров не имеет доступа к MIP уровню менее 2.0.</span><span class="sxs-lookup"><span data-stu-id="f2825-148">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2825-149">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f2825-149">Return value</span></span>

<span data-ttu-id="f2825-150">Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="f2825-150">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="f2825-151">Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="f2825-151">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="f2825-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f2825-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2825-153">Методы Самплекмп</span><span class="sxs-lookup"><span data-stu-id="f2825-153">SampleCmp methods</span></span>](texture2d-samplecmp.md)
</dt> </dl>

 

 
