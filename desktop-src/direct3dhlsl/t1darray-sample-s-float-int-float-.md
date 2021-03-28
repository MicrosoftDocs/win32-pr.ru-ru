---
title: 'Функция Texture1DArray:: Sample (S, float, int, float)'
description: 'Выберет текстуру с необязательным значением, чтобы зафрагментировать образцы значений уровня детализации (Лод) в. | Функция Texture1DArray:: Sample (S, float, int, float)'
ms.assetid: 3A965EEE-FCA3-4DD8-87D2-56679DFF5D3A
keywords:
- Пример функции HLSL
topic_type:
- apiref
api_name:
- Sample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16d0a651d70aa618b9791fb760c51dfa05945752
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998198"
---
# <a name="texture1darraysamplesfloatintfloat-function"></a><span data-ttu-id="e6e4b-105">Функция Texture1DArray:: Sample (S, float, int, float)</span><span class="sxs-lookup"><span data-stu-id="e6e4b-105">Texture1DArray::Sample(S,float,int,float) function</span></span>

<span data-ttu-id="e6e4b-106">Выберет текстуру с необязательным значением, чтобы зафрагментировать образцы значений уровня детализации (Лод) в.</span><span class="sxs-lookup"><span data-stu-id="e6e4b-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6e4b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e6e4b-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in SamplerState S,
  in float        Location,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="e6e4b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e6e4b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6e4b-109">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="e6e4b-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6e4b-110">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="e6e4b-110">Type: **SamplerState**</span></span>

<span data-ttu-id="e6e4b-111">[Состояние образца](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="e6e4b-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="e6e4b-112">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="e6e4b-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="e6e4b-113">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e6e4b-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6e4b-114">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="e6e4b-114">Type: **float**</span></span>

<span data-ttu-id="e6e4b-115">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="e6e4b-115">The texture coordinates.</span></span> <span data-ttu-id="e6e4b-116">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="e6e4b-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="e6e4b-117">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="e6e4b-117">Texture-Object Type</span></span>                    | <span data-ttu-id="e6e4b-118">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="e6e4b-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="e6e4b-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="e6e4b-119">Texture1D</span></span>                              | <span data-ttu-id="e6e4b-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="e6e4b-120">float</span></span>          |
| <span data-ttu-id="e6e4b-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="e6e4b-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="e6e4b-122">float2</span><span class="sxs-lookup"><span data-stu-id="e6e4b-122">float2</span></span>         |
| <span data-ttu-id="e6e4b-123">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="e6e4b-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="e6e4b-124">float3</span><span class="sxs-lookup"><span data-stu-id="e6e4b-124">float3</span></span>         |
| <span data-ttu-id="e6e4b-125">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="e6e4b-125">TextureCubeArray</span></span>                       | <span data-ttu-id="e6e4b-126">float4</span><span class="sxs-lookup"><span data-stu-id="e6e4b-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="e6e4b-127">*Смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e6e4b-127">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6e4b-128">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="e6e4b-128">Type: **int**</span></span>

<span data-ttu-id="e6e4b-129">Необязательное Смещение координаты текстуры, которое может использоваться для любого типа объекта текстуры. смещение применяется к расположению перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="e6e4b-129">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="e6e4b-130">Используйте смещение только с целочисленным миплевел; в противном случае можно получить результаты, которые не могут быть правильно преобразованы в оборудование.</span><span class="sxs-lookup"><span data-stu-id="e6e4b-130">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="e6e4b-131">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="e6e4b-131">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="e6e4b-132">Дополнительные сведения см. в разделе [применение целочисленных смещений](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="e6e4b-132">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="e6e4b-133">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="e6e4b-133">Texture-Object Type</span></span>           | <span data-ttu-id="e6e4b-134">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="e6e4b-134">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="e6e4b-135">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="e6e4b-135">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="e6e4b-136">INT</span><span class="sxs-lookup"><span data-stu-id="e6e4b-136">int</span></span>            |
| <span data-ttu-id="e6e4b-137">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="e6e4b-137">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="e6e4b-138">int2</span><span class="sxs-lookup"><span data-stu-id="e6e4b-138">int2</span></span>           |
| <span data-ttu-id="e6e4b-139">Texture3D</span><span class="sxs-lookup"><span data-stu-id="e6e4b-139">Texture3D</span></span>                     | <span data-ttu-id="e6e4b-140">int3</span><span class="sxs-lookup"><span data-stu-id="e6e4b-140">int3</span></span>           |
| <span data-ttu-id="e6e4b-141">Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="e6e4b-141">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="e6e4b-142">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e6e4b-142">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="e6e4b-143">*Срез* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e6e4b-143">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6e4b-144">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="e6e4b-144">Type: **float**</span></span>

<span data-ttu-id="e6e4b-145">Необязательное значение для примера среза Лод значений.</span><span class="sxs-lookup"><span data-stu-id="e6e4b-145">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="e6e4b-146">Например, если передать значение среза 2.0 f, вы убедитесь, что ни один из отдельных примеров не имеет доступа к MIP уровню менее 2.0.</span><span class="sxs-lookup"><span data-stu-id="e6e4b-146">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6e4b-147">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e6e4b-147">Return value</span></span>

<span data-ttu-id="e6e4b-148">Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="e6e4b-148">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="e6e4b-149">Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="e6e4b-149">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="e6e4b-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e6e4b-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6e4b-151">Примеры методов</span><span class="sxs-lookup"><span data-stu-id="e6e4b-151">Sample methods</span></span>](texture1darray-sample.md)
</dt> </dl>

 

 
