---
title: 'Функция Самплебиас:: Самплебиас (S, float, float, float)'
description: 'Демонстрирует выбор текстуры после применения значения смещения к уровню mipmap с дополнительным значением для создания среза образцов значений уровня детализации (Лод). | Функция Самплебиас:: Самплебиас (S, float, float, float)'
ms.assetid: 6683F115-4F81-4C24-B735-67DB4B52455B
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
ms.openlocfilehash: 8d95a1b0341e61853a20d313a04d1cde64dde66d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104157075"
---
# <a name="samplebiassamplebiassfloatfloatfloat-function"></a><span data-ttu-id="9860f-105">Функция Самплебиас:: Самплебиас (S, float, float, float)</span><span class="sxs-lookup"><span data-stu-id="9860f-105">SampleBias::SampleBias(S,float,float,float) function</span></span>

<span data-ttu-id="9860f-106">Демонстрирует выбор текстуры после применения значения смещения к уровню mipmap с дополнительным значением для создания среза образцов значений уровня детализации (Лод).</span><span class="sxs-lookup"><span data-stu-id="9860f-106">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="9860f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9860f-107">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="9860f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9860f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9860f-109">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="9860f-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9860f-110">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="9860f-110">Type: **SamplerState**</span></span>

<span data-ttu-id="9860f-111">[Состояние образца](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="9860f-111">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="9860f-112">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="9860f-112">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="9860f-113">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9860f-113">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9860f-114">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="9860f-114">Type: **float**</span></span>

<span data-ttu-id="9860f-115">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="9860f-115">The texture coordinates.</span></span> <span data-ttu-id="9860f-116">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="9860f-116">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="9860f-117">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="9860f-117">Texture-Object Type</span></span>                    | <span data-ttu-id="9860f-118">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="9860f-118">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="9860f-119">Texture1D</span><span class="sxs-lookup"><span data-stu-id="9860f-119">Texture1D</span></span>                              | <span data-ttu-id="9860f-120">FLOAT</span><span class="sxs-lookup"><span data-stu-id="9860f-120">float</span></span>          |
| <span data-ttu-id="9860f-121">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="9860f-121">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="9860f-122">float2</span><span class="sxs-lookup"><span data-stu-id="9860f-122">float2</span></span>         |
| <span data-ttu-id="9860f-123">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="9860f-123">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="9860f-124">float3</span><span class="sxs-lookup"><span data-stu-id="9860f-124">float3</span></span>         |
| <span data-ttu-id="9860f-125">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="9860f-125">TextureCubeArray</span></span>                       | <span data-ttu-id="9860f-126">float4</span><span class="sxs-lookup"><span data-stu-id="9860f-126">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="9860f-127">*Уровень защиты* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9860f-127">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9860f-128">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="9860f-128">Type: **float**</span></span>

<span data-ttu-id="9860f-129">Значение смещения, которое является числом с плавающей запятой от 0,0 до 1,0 включительно, применяется к MIP уровню перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="9860f-129">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="9860f-130">*Срез* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9860f-130">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9860f-131">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="9860f-131">Type: **float**</span></span>

<span data-ttu-id="9860f-132">Необязательное значение для примера среза Лод значений.</span><span class="sxs-lookup"><span data-stu-id="9860f-132">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="9860f-133">Например, если передать значение среза 2.0 f, вы убедитесь, что ни один из отдельных примеров не имеет доступа к MIP уровню менее 2.0.</span><span class="sxs-lookup"><span data-stu-id="9860f-133">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9860f-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9860f-134">Return value</span></span>

<span data-ttu-id="9860f-135">Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="9860f-135">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="9860f-136">Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="9860f-136">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="9860f-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9860f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9860f-138">Методы Самплебиас</span><span class="sxs-lookup"><span data-stu-id="9860f-138">SampleBias methods</span></span>](texturecubearray-samplebias.md)
</dt> <dt>

[<span data-ttu-id="9860f-139">**текстурекубеаррай**</span><span class="sxs-lookup"><span data-stu-id="9860f-139">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
