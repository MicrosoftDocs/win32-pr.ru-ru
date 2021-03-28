---
title: 'Функция Texture1D:: Sample (S, float, int, float)'
description: 'Выберет текстуру с необязательным значением, чтобы зафрагментировать образцы значений уровня детализации (Лод) в. | Функция Texture1D:: Sample (S, float, int, float)'
ms.assetid: D2E2E143-8240-43AA-AD70-BD793B3CFD19
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
ms.openlocfilehash: f119955a66f7aec336ce52d730d54a5f11756527
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104081802"
---
# <a name="texture1dsamplesfloatintfloat-function"></a><span data-ttu-id="89134-105">Функция Texture1D:: Sample (S, float, int, float)</span><span class="sxs-lookup"><span data-stu-id="89134-105">Texture1D::Sample(S,float,int,float) function</span></span>

<span data-ttu-id="89134-106">Выберет текстуру с необязательным значением, чтобы зафрагментировать образцы значений уровня детализации (Лод) в.</span><span class="sxs-lookup"><span data-stu-id="89134-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="89134-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="89134-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in SamplerState S,
  in float        Location,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="89134-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="89134-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89134-109">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="89134-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89134-110">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="89134-110">Type: **SamplerState**</span></span>

<span data-ttu-id="89134-111">[Состояние образца](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="89134-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="89134-112">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="89134-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="89134-113">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="89134-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89134-114">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="89134-114">Type: **float**</span></span>

<span data-ttu-id="89134-115">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="89134-115">The texture coordinates.</span></span> <span data-ttu-id="89134-116">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="89134-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="89134-117">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="89134-117">Texture-Object Type</span></span>                    | <span data-ttu-id="89134-118">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="89134-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="89134-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="89134-119">Texture1D</span></span>                              | <span data-ttu-id="89134-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="89134-120">float</span></span>          |
| <span data-ttu-id="89134-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="89134-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="89134-122">float2</span><span class="sxs-lookup"><span data-stu-id="89134-122">float2</span></span>         |
| <span data-ttu-id="89134-123">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="89134-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="89134-124">float3</span><span class="sxs-lookup"><span data-stu-id="89134-124">float3</span></span>         |
| <span data-ttu-id="89134-125">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="89134-125">TextureCubeArray</span></span>                       | <span data-ttu-id="89134-126">float4</span><span class="sxs-lookup"><span data-stu-id="89134-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="89134-127">*Смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="89134-127">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89134-128">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="89134-128">Type: **int**</span></span>

<span data-ttu-id="89134-129">Необязательное Смещение координаты текстуры, которое может использоваться для любого типа объекта текстуры. смещение применяется к расположению перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="89134-129">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="89134-130">Используйте смещение только с целочисленным миплевел; в противном случае можно получить результаты, которые не могут быть правильно преобразованы в оборудование.</span><span class="sxs-lookup"><span data-stu-id="89134-130">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="89134-131">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="89134-131">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="89134-132">Дополнительные сведения см. в разделе [применение целочисленных смещений](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="89134-132">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="89134-133">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="89134-133">Texture-Object Type</span></span>           | <span data-ttu-id="89134-134">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="89134-134">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="89134-135">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="89134-135">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="89134-136">INT</span><span class="sxs-lookup"><span data-stu-id="89134-136">int</span></span>            |
| <span data-ttu-id="89134-137">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="89134-137">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="89134-138">int2</span><span class="sxs-lookup"><span data-stu-id="89134-138">int2</span></span>           |
| <span data-ttu-id="89134-139">Texture3D</span><span class="sxs-lookup"><span data-stu-id="89134-139">Texture3D</span></span>                     | <span data-ttu-id="89134-140">int3</span><span class="sxs-lookup"><span data-stu-id="89134-140">int3</span></span>           |
| <span data-ttu-id="89134-141">Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="89134-141">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="89134-142">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="89134-142">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="89134-143">*Срез* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="89134-143">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89134-144">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="89134-144">Type: **float**</span></span>

<span data-ttu-id="89134-145">Необязательное значение для примера среза Лод значений.</span><span class="sxs-lookup"><span data-stu-id="89134-145">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="89134-146">Например, если передать значение среза 2.0 f, вы убедитесь, что ни один из отдельных примеров не имеет доступа к MIP уровню менее 2.0.</span><span class="sxs-lookup"><span data-stu-id="89134-146">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89134-147">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="89134-147">Return value</span></span>

<span data-ttu-id="89134-148">Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="89134-148">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="89134-149">Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="89134-149">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="89134-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="89134-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89134-151">Примеры методов</span><span class="sxs-lookup"><span data-stu-id="89134-151">Sample methods</span></span>](texture1d-sample.md)
</dt> </dl>

 

 
