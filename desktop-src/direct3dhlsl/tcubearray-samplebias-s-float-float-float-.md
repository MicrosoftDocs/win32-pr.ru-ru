---
title: 'Функция Самплебиас:: Самплебиас (S, float, float, float) для Текстурекубеаррай'
description: 'Функция Самплебиас:: Самплебиас (S, float, float, float) для Текстурекубеаррай выбирает текстуру после применения значения смещения к уровню mipmap.'
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
ms.openlocfilehash: 0c57eec224ca92b2584ba7262488530ea7080939
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187809"
---
# <a name="samplebiassamplebiassfloatfloatfloat-function-for-texturecubearray"></a><span data-ttu-id="44592-104">Функция Самплебиас:: Самплебиас (S, float, float, float) для Текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="44592-104">SampleBias::SampleBias(S,float,float,float) function for TextureCubeArray</span></span>

<span data-ttu-id="44592-105">Демонстрирует выбор текстуры после применения значения смещения к уровню mipmap с дополнительным значением для создания среза образцов значений уровня детализации (Лод).</span><span class="sxs-lookup"><span data-stu-id="44592-105">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="44592-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="44592-106">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="44592-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="44592-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44592-108">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="44592-108">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44592-109">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="44592-109">Type: **SamplerState**</span></span>

<span data-ttu-id="44592-110">[Состояние образца](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="44592-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="44592-111">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="44592-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="44592-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="44592-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44592-113">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="44592-113">Type: **float**</span></span>

<span data-ttu-id="44592-114">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="44592-114">The texture coordinates.</span></span> <span data-ttu-id="44592-115">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="44592-115">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="44592-116">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="44592-116">Texture-Object Type</span></span>                    | <span data-ttu-id="44592-117">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="44592-117">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="44592-118">Texture1D</span><span class="sxs-lookup"><span data-stu-id="44592-118">Texture1D</span></span>                              | <span data-ttu-id="44592-119">FLOAT</span><span class="sxs-lookup"><span data-stu-id="44592-119">float</span></span>          |
| <span data-ttu-id="44592-120">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="44592-120">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="44592-121">float2</span><span class="sxs-lookup"><span data-stu-id="44592-121">float2</span></span>         |
| <span data-ttu-id="44592-122">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="44592-122">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="44592-123">float3</span><span class="sxs-lookup"><span data-stu-id="44592-123">float3</span></span>         |
| <span data-ttu-id="44592-124">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="44592-124">TextureCubeArray</span></span>                       | <span data-ttu-id="44592-125">float4</span><span class="sxs-lookup"><span data-stu-id="44592-125">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="44592-126">*Уровень защиты* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="44592-126">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44592-127">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="44592-127">Type: **float**</span></span>

<span data-ttu-id="44592-128">Значение смещения, которое является числом с плавающей запятой от 0,0 до 1,0 включительно, применяется к MIP уровню перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="44592-128">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="44592-129">*Срез* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="44592-129">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44592-130">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="44592-130">Type: **float**</span></span>

<span data-ttu-id="44592-131">Необязательное значение для примера среза Лод значений.</span><span class="sxs-lookup"><span data-stu-id="44592-131">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="44592-132">Например, если передать значение среза 2.0 f, вы убедитесь, что ни один из отдельных примеров не имеет доступа к MIP уровню менее 2.0.</span><span class="sxs-lookup"><span data-stu-id="44592-132">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44592-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="44592-133">Return value</span></span>

<span data-ttu-id="44592-134">Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="44592-134">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="44592-135">Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="44592-135">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="44592-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="44592-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44592-137">Методы Самплебиас</span><span class="sxs-lookup"><span data-stu-id="44592-137">SampleBias methods</span></span>](texturecubearray-samplebias.md)
</dt> <dt>

[<span data-ttu-id="44592-138">**текстурекубеаррай**</span><span class="sxs-lookup"><span data-stu-id="44592-138">**TextureCubeArray**</span></span>](texturecubearray.md)
</dt> </dl>

 

 
