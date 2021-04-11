---
title: 'Функция Texture2DArray:: Sample (S, float, int, float)'
description: 'Выберет текстуру с необязательным значением, чтобы зафрагментировать образцы значений уровня детализации (Лод) в. | Функция Texture2DArray:: Sample (S, float, int, float)'
ms.assetid: F6638224-0993-4F55-A8C0-7EC4140204D5
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
ms.openlocfilehash: 8d85e4d7e5662d76c011b1c5684f3fd36e4191ba
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273452"
---
# <a name="texture2darraysamplesfloatintfloat-function"></a><span data-ttu-id="83be0-105">Функция Texture2DArray:: Sample (S, float, int, float)</span><span class="sxs-lookup"><span data-stu-id="83be0-105">Texture2DArray::Sample(S,float,int,float) function</span></span>

<span data-ttu-id="83be0-106">Выберет текстуру с необязательным значением, чтобы зафрагментировать образцы значений уровня детализации (Лод) в.</span><span class="sxs-lookup"><span data-stu-id="83be0-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="83be0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="83be0-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in SamplerState S,
  in float        Location,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="83be0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="83be0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83be0-109">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="83be0-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83be0-110">[Состояние образца](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="83be0-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="83be0-111">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="83be0-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="83be0-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="83be0-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83be0-113">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="83be0-113">The texture coordinates.</span></span> <span data-ttu-id="83be0-114">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="83be0-114">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="83be0-115">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="83be0-115">Texture-Object Type</span></span>                    | <span data-ttu-id="83be0-116">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="83be0-116">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="83be0-117">Texture1D</span><span class="sxs-lookup"><span data-stu-id="83be0-117">Texture1D</span></span>                              | <span data-ttu-id="83be0-118">FLOAT</span><span class="sxs-lookup"><span data-stu-id="83be0-118">float</span></span>          |
| <span data-ttu-id="83be0-119">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="83be0-119">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="83be0-120">float2</span><span class="sxs-lookup"><span data-stu-id="83be0-120">float2</span></span>         |
| <span data-ttu-id="83be0-121">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="83be0-121">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="83be0-122">float3</span><span class="sxs-lookup"><span data-stu-id="83be0-122">float3</span></span>         |
| <span data-ttu-id="83be0-123">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="83be0-123">TextureCubeArray</span></span>                       | <span data-ttu-id="83be0-124">float4</span><span class="sxs-lookup"><span data-stu-id="83be0-124">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="83be0-125">*Смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="83be0-125">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83be0-126">Необязательное Смещение координаты текстуры, которое может использоваться для любого типа объекта текстуры. смещение применяется к расположению перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="83be0-126">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="83be0-127">Используйте смещение только с целочисленным миплевел; в противном случае можно получить результаты, которые не могут быть правильно преобразованы в оборудование.</span><span class="sxs-lookup"><span data-stu-id="83be0-127">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="83be0-128">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="83be0-128">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="83be0-129">Дополнительные сведения см. в разделе [применение целочисленных смещений](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="83be0-129">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="83be0-130">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="83be0-130">Texture-Object Type</span></span>           | <span data-ttu-id="83be0-131">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="83be0-131">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="83be0-132">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="83be0-132">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="83be0-133">INT</span><span class="sxs-lookup"><span data-stu-id="83be0-133">int</span></span>            |
| <span data-ttu-id="83be0-134">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="83be0-134">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="83be0-135">int2</span><span class="sxs-lookup"><span data-stu-id="83be0-135">int2</span></span>           |
| <span data-ttu-id="83be0-136">Texture3D</span><span class="sxs-lookup"><span data-stu-id="83be0-136">Texture3D</span></span>                     | <span data-ttu-id="83be0-137">int3</span><span class="sxs-lookup"><span data-stu-id="83be0-137">int3</span></span>           |
| <span data-ttu-id="83be0-138">Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="83be0-138">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="83be0-139">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="83be0-139">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="83be0-140">*Срез* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="83be0-140">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83be0-141">Необязательное значение для примера среза Лод значений.</span><span class="sxs-lookup"><span data-stu-id="83be0-141">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="83be0-142">Например, если передать значение среза 2.0 f, вы убедитесь, что ни один из отдельных примеров не имеет доступа к MIP уровню менее 2.0.</span><span class="sxs-lookup"><span data-stu-id="83be0-142">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83be0-143">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="83be0-143">Return value</span></span>

<span data-ttu-id="83be0-144">Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="83be0-144">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="83be0-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="83be0-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83be0-146">Примеры методов</span><span class="sxs-lookup"><span data-stu-id="83be0-146">Sample methods</span></span>](texture2darray-sample.md)
</dt> </dl>

 

 
