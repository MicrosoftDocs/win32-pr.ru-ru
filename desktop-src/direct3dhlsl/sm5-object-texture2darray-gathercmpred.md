---
title: 'Функция Texture2DArray:: Гасеркмпред (S, float, float, int)'
description: 'Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, функция возвращает сравнение их красного компонента со значением сравнения. | Функция Texture2DArray:: Гасеркмпред (S, float, float, int)'
ms.assetid: aa7fadf8-fe96-406a-9c93-9ae0c59ef087
keywords:
- Функция Гасеркмпред HLSL
topic_type:
- apiref
api_name:
- GatherCmpRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3cf0f7094c7e535a84e6d8fd6ba7e87bb702dbfd
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998123"
---
# <a name="texture2darraygathercmpredsfloatfloatint-function"></a><span data-ttu-id="2e0be-105">Функция Texture2DArray:: Гасеркмпред (S, float, float, int)</span><span class="sxs-lookup"><span data-stu-id="2e0be-105">Texture2DArray::GatherCmpRed(S,float,float,int) function</span></span>

<span data-ttu-id="2e0be-106">Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, функция возвращает сравнение их красного компонента со значением сравнения.</span><span class="sxs-lookup"><span data-stu-id="2e0be-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e0be-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2e0be-107">Syntax</span></span>

``` syntax
float4 GatherCmpRed(
  in SamplerComparisonState s,
  in float3 location,
  in float compare_value,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="2e0be-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2e0be-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e0be-109">*s* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="2e0be-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e0be-110">Тип: **самплеркомпарисонстате**</span><span class="sxs-lookup"><span data-stu-id="2e0be-110">Type: **SamplerComparisonState**</span></span>

<span data-ttu-id="2e0be-111">Индекс выборки с отсчетом от нуля.</span><span class="sxs-lookup"><span data-stu-id="2e0be-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="2e0be-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2e0be-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e0be-113">Тип: **float3**</span><span class="sxs-lookup"><span data-stu-id="2e0be-113">Type: **float3**</span></span>

<span data-ttu-id="2e0be-114">Образцы координат (u, v).</span><span class="sxs-lookup"><span data-stu-id="2e0be-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="2e0be-115">*сравнить \_ значение* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="2e0be-115">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e0be-116">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="2e0be-116">Type: **float**</span></span>

<span data-ttu-id="2e0be-117">Значение, сравниваемое по каждому значению выборки.</span><span class="sxs-lookup"><span data-stu-id="2e0be-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="2e0be-118">*смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2e0be-118">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e0be-119">Тип: **int2**</span><span class="sxs-lookup"><span data-stu-id="2e0be-119">Type: **int2**</span></span>

<span data-ttu-id="2e0be-120">Смещение, применяемое к координате текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="2e0be-120">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e0be-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2e0be-121">Return value</span></span>

<span data-ttu-id="2e0be-122">Тип: **float4**</span><span class="sxs-lookup"><span data-stu-id="2e0be-122">Type: **float4**</span></span>

<span data-ttu-id="2e0be-123">Значение из четырех компонентов, каждый компонент которого является результатом сравнения каждого компонента.</span><span class="sxs-lookup"><span data-stu-id="2e0be-123">A four-component value, each component is the result of a per-component comparison.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e0be-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="2e0be-124">Remarks</span></span>

<span data-ttu-id="2e0be-125">Примеры текстур можно использовать для интерполяции билинейной.</span><span class="sxs-lookup"><span data-stu-id="2e0be-125">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="2e0be-126">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="2e0be-126">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="2e0be-127">Вершина</span><span class="sxs-lookup"><span data-stu-id="2e0be-127">Vertex</span></span> | <span data-ttu-id="2e0be-128">Поверхности</span><span class="sxs-lookup"><span data-stu-id="2e0be-128">Hull</span></span> | <span data-ttu-id="2e0be-129">Домен</span><span class="sxs-lookup"><span data-stu-id="2e0be-129">Domain</span></span> | <span data-ttu-id="2e0be-130">Геометрия</span><span class="sxs-lookup"><span data-stu-id="2e0be-130">Geometry</span></span> | <span data-ttu-id="2e0be-131">Пиксель</span><span class="sxs-lookup"><span data-stu-id="2e0be-131">Pixel</span></span> | <span data-ttu-id="2e0be-132">Вычисления</span><span class="sxs-lookup"><span data-stu-id="2e0be-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="2e0be-133">x</span><span class="sxs-lookup"><span data-stu-id="2e0be-133">x</span></span>      | <span data-ttu-id="2e0be-134">x</span><span class="sxs-lookup"><span data-stu-id="2e0be-134">x</span></span>    | <span data-ttu-id="2e0be-135">x</span><span class="sxs-lookup"><span data-stu-id="2e0be-135">x</span></span>      | <span data-ttu-id="2e0be-136">x</span><span class="sxs-lookup"><span data-stu-id="2e0be-136">x</span></span>        | <span data-ttu-id="2e0be-137">x</span><span class="sxs-lookup"><span data-stu-id="2e0be-137">x</span></span>     | <span data-ttu-id="2e0be-138">x</span><span class="sxs-lookup"><span data-stu-id="2e0be-138">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="2e0be-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2e0be-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e0be-140">Методы Гасеркмпред</span><span class="sxs-lookup"><span data-stu-id="2e0be-140">GatherCmpRed methods</span></span>](texture2darray-gathercmpred.md)
</dt> <dt>

[<span data-ttu-id="2e0be-141">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="2e0be-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




