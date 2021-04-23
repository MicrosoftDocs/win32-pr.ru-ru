---
title: 'Функция Texture2DArray:: Гасерред (S, float, int)'
description: 'Возвращает красные компоненты четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации. | Функция Texture2DArray:: Гасерред (S, float, int)'
ms.assetid: cb9c21ef-87f4-4c32-b41a-9fc7478713a6
keywords:
- Функция Гасерред HLSL
topic_type:
- apiref
api_name:
- GatherRed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 431d08b77d13540bb48621a6d5ec76f4c775f796
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998142"
---
# <a name="texture2darraygatherredsfloatint-function"></a><span data-ttu-id="917a9-105">Функция Texture2DArray:: Гасерред (S, float, int)</span><span class="sxs-lookup"><span data-stu-id="917a9-105">Texture2DArray::GatherRed(S,float,int) function</span></span>

<span data-ttu-id="917a9-106">Возвращает красные компоненты четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="917a9-106">Returns the red components of the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="917a9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="917a9-107">Syntax</span></span>

``` syntax
TemplateType GatherRed(
  in sampler s,
  in float3 location,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="917a9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="917a9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="917a9-109">*s* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="917a9-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="917a9-110">Тип: **образец**</span><span class="sxs-lookup"><span data-stu-id="917a9-110">Type: **sampler**</span></span>

<span data-ttu-id="917a9-111">Индекс выборки с отсчетом от нуля.</span><span class="sxs-lookup"><span data-stu-id="917a9-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="917a9-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="917a9-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="917a9-113">Тип: **float3**</span><span class="sxs-lookup"><span data-stu-id="917a9-113">Type: **float3**</span></span>

<span data-ttu-id="917a9-114">Образцы координат (u, v).</span><span class="sxs-lookup"><span data-stu-id="917a9-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="917a9-115">*смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="917a9-115">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="917a9-116">Тип: **int2**</span><span class="sxs-lookup"><span data-stu-id="917a9-116">Type: **int2**</span></span>

<span data-ttu-id="917a9-117">Смещение, применяемое к координате текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="917a9-117">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="917a9-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="917a9-118">Return value</span></span>

<span data-ttu-id="917a9-119">Тип: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="917a9-119">Type: **TemplateType**</span></span>

<span data-ttu-id="917a9-120">Значение из четырех компонентов, тип которого совпадает с типом шаблона.</span><span class="sxs-lookup"><span data-stu-id="917a9-120">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="917a9-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="917a9-121">Remarks</span></span>

<span data-ttu-id="917a9-122">Примеры текстур можно использовать для интерполяции билинейной.</span><span class="sxs-lookup"><span data-stu-id="917a9-122">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="917a9-123">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="917a9-123">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="917a9-124">Вершина</span><span class="sxs-lookup"><span data-stu-id="917a9-124">Vertex</span></span> | <span data-ttu-id="917a9-125">Поверхности</span><span class="sxs-lookup"><span data-stu-id="917a9-125">Hull</span></span> | <span data-ttu-id="917a9-126">Домен</span><span class="sxs-lookup"><span data-stu-id="917a9-126">Domain</span></span> | <span data-ttu-id="917a9-127">Геометрия</span><span class="sxs-lookup"><span data-stu-id="917a9-127">Geometry</span></span> | <span data-ttu-id="917a9-128">Пиксель</span><span class="sxs-lookup"><span data-stu-id="917a9-128">Pixel</span></span> | <span data-ttu-id="917a9-129">Вычисления</span><span class="sxs-lookup"><span data-stu-id="917a9-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="917a9-130">x</span><span class="sxs-lookup"><span data-stu-id="917a9-130">x</span></span>      | <span data-ttu-id="917a9-131">x</span><span class="sxs-lookup"><span data-stu-id="917a9-131">x</span></span>    | <span data-ttu-id="917a9-132">x</span><span class="sxs-lookup"><span data-stu-id="917a9-132">x</span></span>      | <span data-ttu-id="917a9-133">x</span><span class="sxs-lookup"><span data-stu-id="917a9-133">x</span></span>        | <span data-ttu-id="917a9-134">x</span><span class="sxs-lookup"><span data-stu-id="917a9-134">x</span></span>     | <span data-ttu-id="917a9-135">x</span><span class="sxs-lookup"><span data-stu-id="917a9-135">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="917a9-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="917a9-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="917a9-137">Методы Гасерред</span><span class="sxs-lookup"><span data-stu-id="917a9-137">GatherRed methods</span></span>](texture2darray-gatherred.md)
</dt> <dt>

[<span data-ttu-id="917a9-138">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="917a9-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




