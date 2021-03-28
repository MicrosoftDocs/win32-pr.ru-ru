---
title: 'Функция Текстурекубеаррай:: Sample (S, float, float)'
description: 'Выберет текстуру с необязательным значением, чтобы зафрагментировать образцы значений уровня детализации (Лод) в. | Функция Текстурекубеаррай:: Sample (S, float, float)'
ms.assetid: E3BACA5E-18FC-4BD7-A8D8-C2808BDF1517
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
ms.openlocfilehash: 0f3f822ee334262dc50950064c6b4257aca3dd1f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986401"
---
# <a name="texturecubearraysamplesfloatfloat-function"></a><span data-ttu-id="d6783-105">Функция Текстурекубеаррай:: Sample (S, float, float)</span><span class="sxs-lookup"><span data-stu-id="d6783-105">TextureCubeArray::Sample(S,float,float) function</span></span>

<span data-ttu-id="d6783-106">Выберет текстуру с необязательным значением, чтобы зафрагментировать образцы значений уровня детализации (Лод) в.</span><span class="sxs-lookup"><span data-stu-id="d6783-106">Samples a texture with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6783-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d6783-107">Syntax</span></span>


``` syntax
DXGI_FORMAT Sample(
  in SamplerState S,
  in float        Location,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="d6783-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d6783-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6783-109">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="d6783-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6783-110">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="d6783-110">Type: **SamplerState**</span></span>

<span data-ttu-id="d6783-111">[Состояние образца](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="d6783-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="d6783-112">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="d6783-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="d6783-113">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d6783-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6783-114">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="d6783-114">Type: **float**</span></span>

<span data-ttu-id="d6783-115">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="d6783-115">The texture coordinates.</span></span> <span data-ttu-id="d6783-116">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="d6783-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="d6783-117">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="d6783-117">Texture-Object Type</span></span>                    | <span data-ttu-id="d6783-118">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="d6783-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="d6783-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="d6783-119">Texture1D</span></span>                              | <span data-ttu-id="d6783-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="d6783-120">float</span></span>          |
| <span data-ttu-id="d6783-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="d6783-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="d6783-122">float2</span><span class="sxs-lookup"><span data-stu-id="d6783-122">float2</span></span>         |
| <span data-ttu-id="d6783-123">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="d6783-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="d6783-124">float3</span><span class="sxs-lookup"><span data-stu-id="d6783-124">float3</span></span>         |
| <span data-ttu-id="d6783-125">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="d6783-125">TextureCubeArray</span></span>                       | <span data-ttu-id="d6783-126">float4</span><span class="sxs-lookup"><span data-stu-id="d6783-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="d6783-127">*Срез* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d6783-127">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6783-128">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="d6783-128">Type: **float**</span></span>

<span data-ttu-id="d6783-129">Необязательное значение для примера среза Лод значений.</span><span class="sxs-lookup"><span data-stu-id="d6783-129">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="d6783-130">Например, если передать значение среза 2.0 f, вы убедитесь, что ни один из отдельных примеров не имеет доступа к MIP уровню менее 2.0.</span><span class="sxs-lookup"><span data-stu-id="d6783-130">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6783-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d6783-131">Return value</span></span>

<span data-ttu-id="d6783-132">Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="d6783-132">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="d6783-133">Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="d6783-133">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="d6783-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d6783-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6783-135">Примеры методов</span><span class="sxs-lookup"><span data-stu-id="d6783-135">Sample methods</span></span>](texturecubearray-sample.md)
</dt> <dt>

[<span data-ttu-id="d6783-136">**текстурекубеаррай**</span><span class="sxs-lookup"><span data-stu-id="d6783-136">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
