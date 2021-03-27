---
title: 'Функция Texture2DArray:: Гасеркмпблуе (S, float, float, int)'
description: 'Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, функция возвращает сравнение их синего компонента со значением сравнения. | Функция Texture2DArray:: Гасеркмпблуе (S, float, float, int)'
ms.assetid: 5fa23e27-368a-4c55-b6d6-33506c932a43
keywords:
- Функция Гасеркмпблуе HLSL
topic_type:
- apiref
api_name:
- GatherCmpBlue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 42c645333cc45c6de55a609439445936f65b85f4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "103820636"
---
# <a name="texture2darraygathercmpbluesfloatfloatint-function"></a><span data-ttu-id="5c5d8-105">Функция Texture2DArray:: Гасеркмпблуе (S, float, float, int)</span><span class="sxs-lookup"><span data-stu-id="5c5d8-105">Texture2DArray::GatherCmpBlue(S,float,float,int) function</span></span>

<span data-ttu-id="5c5d8-106">Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, функция возвращает сравнение их синего компонента со значением сравнения.</span><span class="sxs-lookup"><span data-stu-id="5c5d8-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their blue component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c5d8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5c5d8-107">Syntax</span></span>

``` syntax
float4 GatherCmpBlue(
  in SamplerComparisonState s,
  in float3 location,
  in float compare_value,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="5c5d8-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5c5d8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c5d8-109">*s* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="5c5d8-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c5d8-110">Тип: **самплеркомпарисонстате**</span><span class="sxs-lookup"><span data-stu-id="5c5d8-110">Type: **SamplerComparisonState**</span></span>

<span data-ttu-id="5c5d8-111">Индекс выборки с отсчетом от нуля.</span><span class="sxs-lookup"><span data-stu-id="5c5d8-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="5c5d8-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5c5d8-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c5d8-113">Тип: **float3**</span><span class="sxs-lookup"><span data-stu-id="5c5d8-113">Type: **float3**</span></span>

<span data-ttu-id="5c5d8-114">Образцы координат (u, v).</span><span class="sxs-lookup"><span data-stu-id="5c5d8-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="5c5d8-115">*сравнить \_ значение* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="5c5d8-115">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c5d8-116">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="5c5d8-116">Type: **float**</span></span>

<span data-ttu-id="5c5d8-117">Значение, сравниваемое по каждому значению выборки.</span><span class="sxs-lookup"><span data-stu-id="5c5d8-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="5c5d8-118">*смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5c5d8-118">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c5d8-119">Тип: **int2**</span><span class="sxs-lookup"><span data-stu-id="5c5d8-119">Type: **int2**</span></span>

<span data-ttu-id="5c5d8-120">Смещение, применяемое к координате текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="5c5d8-120">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c5d8-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5c5d8-121">Return value</span></span>

<span data-ttu-id="5c5d8-122">Тип: **float4**</span><span class="sxs-lookup"><span data-stu-id="5c5d8-122">Type: **float4**</span></span>

<span data-ttu-id="5c5d8-123">Значение из четырех компонентов, каждый компонент которого является результатом сравнения каждого компонента.</span><span class="sxs-lookup"><span data-stu-id="5c5d8-123">A four-component value, each component is the result of a per-component comparison.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c5d8-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="5c5d8-124">Remarks</span></span>

<span data-ttu-id="5c5d8-125">Примеры текстур можно использовать для интерполяции билинейной.</span><span class="sxs-lookup"><span data-stu-id="5c5d8-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="5c5d8-126">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="5c5d8-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="5c5d8-127">Вершина</span><span class="sxs-lookup"><span data-stu-id="5c5d8-127">Vertex</span></span> | <span data-ttu-id="5c5d8-128">Поверхности</span><span class="sxs-lookup"><span data-stu-id="5c5d8-128">Hull</span></span> | <span data-ttu-id="5c5d8-129">Домен</span><span class="sxs-lookup"><span data-stu-id="5c5d8-129">Domain</span></span> | <span data-ttu-id="5c5d8-130">Геометрия</span><span class="sxs-lookup"><span data-stu-id="5c5d8-130">Geometry</span></span> | <span data-ttu-id="5c5d8-131">Пиксель</span><span class="sxs-lookup"><span data-stu-id="5c5d8-131">Pixel</span></span> | <span data-ttu-id="5c5d8-132">Вычисления</span><span class="sxs-lookup"><span data-stu-id="5c5d8-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="5c5d8-133">x</span><span class="sxs-lookup"><span data-stu-id="5c5d8-133">x</span></span>      | <span data-ttu-id="5c5d8-134">x</span><span class="sxs-lookup"><span data-stu-id="5c5d8-134">x</span></span>    | <span data-ttu-id="5c5d8-135">x</span><span class="sxs-lookup"><span data-stu-id="5c5d8-135">x</span></span>      | <span data-ttu-id="5c5d8-136">x</span><span class="sxs-lookup"><span data-stu-id="5c5d8-136">x</span></span>        | <span data-ttu-id="5c5d8-137">x</span><span class="sxs-lookup"><span data-stu-id="5c5d8-137">x</span></span>     | <span data-ttu-id="5c5d8-138">x</span><span class="sxs-lookup"><span data-stu-id="5c5d8-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="5c5d8-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5c5d8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c5d8-140">Методы Гасеркмпблуе</span><span class="sxs-lookup"><span data-stu-id="5c5d8-140">GatherCmpBlue methods</span></span>](texture2darray-gathercmpblue.md)
</dt> <dt>

[<span data-ttu-id="5c5d8-141">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="5c5d8-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




