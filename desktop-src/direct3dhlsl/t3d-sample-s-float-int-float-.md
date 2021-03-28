---
title: 'Функция Texture3D:: Sample (S, float, int, float)'
description: 'Выберет текстуру с необязательным значением, чтобы зафрагментировать образцы значений уровня детализации (Лод) в. | Функция Texture3D:: Sample (S, float, int, float)'
ms.assetid: A1114A4A-16B9-4A5D-9A9D-262D6BAA9F2E
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
ms.openlocfilehash: 11577e6151d2353477a70e6ef2873d287eb71a87
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998039"
---
# <a name="texture3dsamplesfloatintfloat-function"></a><span data-ttu-id="a4465-105">Функция Texture3D:: Sample (S, float, int, float)</span><span class="sxs-lookup"><span data-stu-id="a4465-105">Texture3D::Sample(S,float,int,float) function</span></span>

<span data-ttu-id="a4465-106">Выберет текстуру с необязательным значением, чтобы зафрагментировать образцы значений уровня детализации (Лод) в.</span><span class="sxs-lookup"><span data-stu-id="a4465-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4465-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a4465-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in SamplerState S,
  in float        Location,
  in int          Offset,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="a4465-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a4465-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4465-109">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="a4465-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4465-110">[Состояние образца](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="a4465-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="a4465-111">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="a4465-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="a4465-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a4465-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4465-113">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="a4465-113">The texture coordinates.</span></span> <span data-ttu-id="a4465-114">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="a4465-114">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="a4465-115">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="a4465-115">Texture-Object Type</span></span>                    | <span data-ttu-id="a4465-116">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="a4465-116">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="a4465-117">Texture1D</span><span class="sxs-lookup"><span data-stu-id="a4465-117">Texture1D</span></span>                              | <span data-ttu-id="a4465-118">FLOAT</span><span class="sxs-lookup"><span data-stu-id="a4465-118">float</span></span>          |
| <span data-ttu-id="a4465-119">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="a4465-119">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="a4465-120">float2</span><span class="sxs-lookup"><span data-stu-id="a4465-120">float2</span></span>         |
| <span data-ttu-id="a4465-121">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="a4465-121">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="a4465-122">float3</span><span class="sxs-lookup"><span data-stu-id="a4465-122">float3</span></span>         |
| <span data-ttu-id="a4465-123">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="a4465-123">TextureCubeArray</span></span>                       | <span data-ttu-id="a4465-124">float4</span><span class="sxs-lookup"><span data-stu-id="a4465-124">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="a4465-125">*Смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a4465-125">*Offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4465-126">Необязательное Смещение координаты текстуры, которое может использоваться для любого типа объекта текстуры. смещение применяется к расположению перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="a4465-126">An optional texture coordinate offset, which can be used for any texture-object type; the offset is applied to the location before sampling.</span></span> <span data-ttu-id="a4465-127">Используйте смещение только с целочисленным миплевел; в противном случае можно получить результаты, которые не могут быть правильно преобразованы в оборудование.</span><span class="sxs-lookup"><span data-stu-id="a4465-127">Use an offset only at an integer miplevel; otherwise, you may get results that do not translate well to hardware.</span></span> <span data-ttu-id="a4465-128">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="a4465-128">The argument type is dependent on the texture-object type.</span></span> <span data-ttu-id="a4465-129">Дополнительные сведения см. в разделе [применение целочисленных смещений](dx-graphics-hlsl-to-sample.md).</span><span class="sxs-lookup"><span data-stu-id="a4465-129">For more info, see [Applying Integer Offsets](dx-graphics-hlsl-to-sample.md).</span></span>



| <span data-ttu-id="a4465-130">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="a4465-130">Texture-Object Type</span></span>           | <span data-ttu-id="a4465-131">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="a4465-131">Parameter Type</span></span> |
|-------------------------------|----------------|
| <span data-ttu-id="a4465-132">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="a4465-132">Texture1D, Texture1DArray</span></span>     | <span data-ttu-id="a4465-133">INT</span><span class="sxs-lookup"><span data-stu-id="a4465-133">int</span></span>            |
| <span data-ttu-id="a4465-134">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="a4465-134">Texture2D, Texture2DArray</span></span>     | <span data-ttu-id="a4465-135">int2</span><span class="sxs-lookup"><span data-stu-id="a4465-135">int2</span></span>           |
| <span data-ttu-id="a4465-136">Texture3D</span><span class="sxs-lookup"><span data-stu-id="a4465-136">Texture3D</span></span>                     | <span data-ttu-id="a4465-137">int3</span><span class="sxs-lookup"><span data-stu-id="a4465-137">int3</span></span>           |
| <span data-ttu-id="a4465-138">Текстурекубе, Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="a4465-138">TextureCube, TextureCubeArray</span></span> | <span data-ttu-id="a4465-139">не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a4465-139">not supported</span></span>  |



 

</dd> <dt>

<span data-ttu-id="a4465-140">*Срез* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a4465-140">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4465-141">Необязательное значение для примера среза Лод значений.</span><span class="sxs-lookup"><span data-stu-id="a4465-141">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="a4465-142">Например, если передать значение среза 2.0 f, вы убедитесь, что ни один из отдельных примеров не имеет доступа к MIP уровню менее 2.0.</span><span class="sxs-lookup"><span data-stu-id="a4465-142">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4465-143">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a4465-143">Return value</span></span>

<span data-ttu-id="a4465-144">Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="a4465-144">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="a4465-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a4465-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4465-146">Примеры методов</span><span class="sxs-lookup"><span data-stu-id="a4465-146">Sample methods</span></span>](texture3d-sample.md)
</dt> <dt>

[<span data-ttu-id="a4465-147">**Texture3D**</span><span class="sxs-lookup"><span data-stu-id="a4465-147">**Texture3D**</span></span>](sm5-object-texture3d.md)
</dt> </dl>

 

 
