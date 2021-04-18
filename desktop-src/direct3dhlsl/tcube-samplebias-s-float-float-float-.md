---
title: 'Функция Самплебиас:: Самплебиас (S, float, float, float) для Текстурекубе'
description: 'Функция Самплебиас:: Самплебиас (S, float, float, float) для Текстурекубе выбирает текстуру после применения значения смещения к уровню mipmap.'
ms.assetid: BCDDADD9-D8B0-47C9-A312-5E6AF9C3C07B
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
ms.openlocfilehash: 55404f2e32f45e5b19e7b0cd4c109a6d5a8bcc13
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187689"
---
# <a name="samplebiassamplebiassfloatfloatfloat-function-for-texturecube"></a><span data-ttu-id="43e91-104">Функция Самплебиас:: Самплебиас (S, float, float, float) для Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="43e91-104">SampleBias::SampleBias(S,float,float,float) function for TextureCube</span></span>

<span data-ttu-id="43e91-105">Демонстрирует выбор текстуры после применения значения смещения к уровню mipmap с дополнительным значением для создания среза образцов значений уровня детализации (Лод).</span><span class="sxs-lookup"><span data-stu-id="43e91-105">Samples a texture, after applying the bias value to the mipmap level, with an optional value to clamp sample level-of-detail (LOD) values to.</span></span>

## <a name="syntax"></a><span data-ttu-id="43e91-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43e91-106">Syntax</span></span>


``` syntax
DXGI_FORMAT SampleBias(
  in SamplerState S,
  in float        Location,
  in float        Bias,
  in float        Clamp
);
```



## <a name="parameters"></a><span data-ttu-id="43e91-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="43e91-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43e91-108">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="43e91-108">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43e91-109">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="43e91-109">Type: **SamplerState**</span></span>

<span data-ttu-id="43e91-110">[Состояние образца](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="43e91-110">A [Sampler state](dx-graphics-hlsl-sampler.md).</span></span> <span data-ttu-id="43e91-111">Это объект, объявленный в файле эффектов, который содержит назначения состояний.</span><span class="sxs-lookup"><span data-stu-id="43e91-111">This is an object declared in an effect file that contains state assignments.</span></span>

</dd> <dt>

<span data-ttu-id="43e91-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43e91-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43e91-113">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="43e91-113">Type: **float**</span></span>

<span data-ttu-id="43e91-114">Координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="43e91-114">The texture coordinates.</span></span> <span data-ttu-id="43e91-115">Тип аргумента зависит от типа объекта текстуры.</span><span class="sxs-lookup"><span data-stu-id="43e91-115">The argument type is dependent on the texture-object type.</span></span>



| <span data-ttu-id="43e91-116">Тип Texture-Object</span><span class="sxs-lookup"><span data-stu-id="43e91-116">Texture-Object Type</span></span>                    | <span data-ttu-id="43e91-117">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="43e91-117">Parameter Type</span></span> |
|----------------------------------------|----------------|
| <span data-ttu-id="43e91-118">Texture1D</span><span class="sxs-lookup"><span data-stu-id="43e91-118">Texture1D</span></span>                              | <span data-ttu-id="43e91-119">FLOAT</span><span class="sxs-lookup"><span data-stu-id="43e91-119">float</span></span>          |
| <span data-ttu-id="43e91-120">Texture1DArray, Texture2D</span><span class="sxs-lookup"><span data-stu-id="43e91-120">Texture1DArray, Texture2D</span></span>              | <span data-ttu-id="43e91-121">float2</span><span class="sxs-lookup"><span data-stu-id="43e91-121">float2</span></span>         |
| <span data-ttu-id="43e91-122">Texture2DArray, Texture3D, Текстурекубе</span><span class="sxs-lookup"><span data-stu-id="43e91-122">Texture2DArray, Texture3D, TextureCube</span></span> | <span data-ttu-id="43e91-123">float3</span><span class="sxs-lookup"><span data-stu-id="43e91-123">float3</span></span>         |
| <span data-ttu-id="43e91-124">текстурекубеаррай</span><span class="sxs-lookup"><span data-stu-id="43e91-124">TextureCubeArray</span></span>                       | <span data-ttu-id="43e91-125">float4</span><span class="sxs-lookup"><span data-stu-id="43e91-125">float4</span></span>         |



 

</dd> <dt>

<span data-ttu-id="43e91-126">*Уровень защиты* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43e91-126">*Bias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43e91-127">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="43e91-127">Type: **float**</span></span>

<span data-ttu-id="43e91-128">Значение смещения, которое является числом с плавающей запятой от 0,0 до 1,0 включительно, применяется к MIP уровню перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="43e91-128">The bias value, which is a floating-point number between 0.0 and 1.0 inclusive, is applied to a mip level before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="43e91-129">*Срез* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43e91-129">*Clamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43e91-130">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="43e91-130">Type: **float**</span></span>

<span data-ttu-id="43e91-131">Необязательное значение для примера среза Лод значений.</span><span class="sxs-lookup"><span data-stu-id="43e91-131">An optional value to clamp sample LOD values to.</span></span> <span data-ttu-id="43e91-132">Например, если передать значение среза 2.0 f, вы убедитесь, что ни один из отдельных примеров не имеет доступа к MIP уровню менее 2.0.</span><span class="sxs-lookup"><span data-stu-id="43e91-132">For example, if you pass 2.0f for the clamp value, you ensure that no individual sample accesses a mip level less than 2.0f.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43e91-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="43e91-133">Return value</span></span>

<span data-ttu-id="43e91-134">Тип: **[ **\_ Формат DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span><span class="sxs-lookup"><span data-stu-id="43e91-134">Type: **[**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**</span></span>

<span data-ttu-id="43e91-135">Формат текстуры, который является одним из типизированных значений, перечисленных в [**\_ формате DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="43e91-135">The texture format, which is one of the typed values listed in [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span>

## <a name="see-also"></a><span data-ttu-id="43e91-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="43e91-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43e91-137">Методы Самплебиас</span><span class="sxs-lookup"><span data-stu-id="43e91-137">SampleBias methods</span></span>](texturecube-samplebias.md)
</dt> <dt>

[<span data-ttu-id="43e91-138">**текстурекубе**</span><span class="sxs-lookup"><span data-stu-id="43e91-138">**TextureCube**</span></span>](texturecube.md)
</dt> </dl>

 

 
