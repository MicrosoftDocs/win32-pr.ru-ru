---
title: 'Функция Texture2D:: Гасеркмпблуе (S, float, float, int)'
description: 'Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, функция возвращает сравнение их синего компонента со значением сравнения. | Функция Texture2D:: Гасеркмпблуе (S, float, float, int)'
ms.assetid: d8e03c55-18f1-4598-a700-9ba3a680d78a
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
ms.openlocfilehash: eedeb21141c1e694effe4eb8c7be70c828aa0a3c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998074"
---
# <a name="texture2dgathercmpbluesfloatfloatint-function"></a><span data-ttu-id="83e3c-105">Функция Texture2D:: Гасеркмпблуе (S, float, float, int)</span><span class="sxs-lookup"><span data-stu-id="83e3c-105">Texture2D::GatherCmpBlue(S,float,float,int) function</span></span>

<span data-ttu-id="83e3c-106">Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, функция возвращает сравнение их синего компонента со значением сравнения.</span><span class="sxs-lookup"><span data-stu-id="83e3c-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their blue component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="83e3c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="83e3c-107">Syntax</span></span>

``` syntax
float4 GatherCmpBlue(
  in SamplerComparisonState s,
  in float2 location,
  in float compare_value,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="83e3c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="83e3c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83e3c-109">*s* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="83e3c-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83e3c-110">Тип: **самплеркомпарисонстате**</span><span class="sxs-lookup"><span data-stu-id="83e3c-110">Type: **SamplerComparisonState**</span></span>

<span data-ttu-id="83e3c-111">Индекс выборки с отсчетом от нуля.</span><span class="sxs-lookup"><span data-stu-id="83e3c-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="83e3c-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="83e3c-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83e3c-113">Тип: **float2**</span><span class="sxs-lookup"><span data-stu-id="83e3c-113">Type: **float2**</span></span>

<span data-ttu-id="83e3c-114">Образцы координат (u, v).</span><span class="sxs-lookup"><span data-stu-id="83e3c-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="83e3c-115">*сравнить \_ значение* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="83e3c-115">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83e3c-116">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="83e3c-116">Type: **float**</span></span>

<span data-ttu-id="83e3c-117">Значение, сравниваемое по каждому значению выборки.</span><span class="sxs-lookup"><span data-stu-id="83e3c-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="83e3c-118">*смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="83e3c-118">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83e3c-119">Тип: **int2**</span><span class="sxs-lookup"><span data-stu-id="83e3c-119">Type: **int2**</span></span>

<span data-ttu-id="83e3c-120">Смещение, применяемое к координате текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="83e3c-120">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83e3c-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="83e3c-121">Return value</span></span>

<span data-ttu-id="83e3c-122">Тип: **float4**</span><span class="sxs-lookup"><span data-stu-id="83e3c-122">Type: **float4**</span></span>

<span data-ttu-id="83e3c-123">Значение из четырех компонентов, каждый компонент которого является результатом сравнения каждого компонента.</span><span class="sxs-lookup"><span data-stu-id="83e3c-123">A four-component value, each component is the result of a per-component comparison.</span></span>

## <a name="remarks"></a><span data-ttu-id="83e3c-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="83e3c-124">Remarks</span></span>

<span data-ttu-id="83e3c-125">Примеры текстур можно использовать для интерполяции билинейной.</span><span class="sxs-lookup"><span data-stu-id="83e3c-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="83e3c-126">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="83e3c-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="83e3c-127">Вершина</span><span class="sxs-lookup"><span data-stu-id="83e3c-127">Vertex</span></span> | <span data-ttu-id="83e3c-128">Поверхности</span><span class="sxs-lookup"><span data-stu-id="83e3c-128">Hull</span></span> | <span data-ttu-id="83e3c-129">Домен</span><span class="sxs-lookup"><span data-stu-id="83e3c-129">Domain</span></span> | <span data-ttu-id="83e3c-130">Геометрия</span><span class="sxs-lookup"><span data-stu-id="83e3c-130">Geometry</span></span> | <span data-ttu-id="83e3c-131">Пиксель</span><span class="sxs-lookup"><span data-stu-id="83e3c-131">Pixel</span></span> | <span data-ttu-id="83e3c-132">Вычисления</span><span class="sxs-lookup"><span data-stu-id="83e3c-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="83e3c-133">x</span><span class="sxs-lookup"><span data-stu-id="83e3c-133">x</span></span>      | <span data-ttu-id="83e3c-134">x</span><span class="sxs-lookup"><span data-stu-id="83e3c-134">x</span></span>    | <span data-ttu-id="83e3c-135">x</span><span class="sxs-lookup"><span data-stu-id="83e3c-135">x</span></span>      | <span data-ttu-id="83e3c-136">x</span><span class="sxs-lookup"><span data-stu-id="83e3c-136">x</span></span>        | <span data-ttu-id="83e3c-137">x</span><span class="sxs-lookup"><span data-stu-id="83e3c-137">x</span></span>     | <span data-ttu-id="83e3c-138">x</span><span class="sxs-lookup"><span data-stu-id="83e3c-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="83e3c-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="83e3c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83e3c-140">Методы Гасеркмпблуе</span><span class="sxs-lookup"><span data-stu-id="83e3c-140">GatherCmpBlue methods</span></span>](texture2d-gathercmpblue.md)
</dt> <dt>

[<span data-ttu-id="83e3c-141">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="83e3c-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




