---
title: 'Функция Texture2DArray:: собрать (S, float, int)'
description: 'Возвращает четыре значения шаг текселя, которые будут использоваться в операции линейной фильтрации. | Функция Texture2DArray:: собрать (S, float, int)'
ms.assetid: b0355158-01c8-45a1-bb5d-29a8c43b1685
keywords:
- Собрать функцию HLSL
topic_type:
- apiref
api_name:
- Gather
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 46866df18a0836b311443a3dd411d74dfa7fb126
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998031"
---
# <a name="texture2darraygathersfloatint-function"></a><span data-ttu-id="84c57-105">Функция Texture2DArray:: собрать (S, float, int)</span><span class="sxs-lookup"><span data-stu-id="84c57-105">Texture2DArray::Gather(S,float,int) function</span></span>

<span data-ttu-id="84c57-106">Возвращает четыре значения шаг текселя, которые будут использоваться в операции линейной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="84c57-106">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="84c57-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="84c57-107">Syntax</span></span>

``` syntax
TemplateType Gather(
  in sampler s,
  in float3 location,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="84c57-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="84c57-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84c57-109">*s* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="84c57-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84c57-110">Тип: **образец**</span><span class="sxs-lookup"><span data-stu-id="84c57-110">Type: **sampler**</span></span>

<span data-ttu-id="84c57-111">Индекс выборки с отсчетом от нуля.</span><span class="sxs-lookup"><span data-stu-id="84c57-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="84c57-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="84c57-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84c57-113">Тип: **float3**</span><span class="sxs-lookup"><span data-stu-id="84c57-113">Type: **float3**</span></span>

<span data-ttu-id="84c57-114">Образцы координат (u, v).</span><span class="sxs-lookup"><span data-stu-id="84c57-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="84c57-115">*смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="84c57-115">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84c57-116">Тип: **int2**</span><span class="sxs-lookup"><span data-stu-id="84c57-116">Type: **int2**</span></span>

<span data-ttu-id="84c57-117">Смещение, применяемое к координатам текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="84c57-117">The offset applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84c57-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="84c57-118">Return value</span></span>

<span data-ttu-id="84c57-119">Тип: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="84c57-119">Type: **TemplateType**</span></span>

<span data-ttu-id="84c57-120">Значение из четырех компонентов, тип которого совпадает с типом шаблона.</span><span class="sxs-lookup"><span data-stu-id="84c57-120">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="84c57-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="84c57-121">Remarks</span></span>

<span data-ttu-id="84c57-122">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="84c57-122">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="84c57-123">Вершина</span><span class="sxs-lookup"><span data-stu-id="84c57-123">Vertex</span></span> | <span data-ttu-id="84c57-124">Поверхности</span><span class="sxs-lookup"><span data-stu-id="84c57-124">Hull</span></span> | <span data-ttu-id="84c57-125">Домен</span><span class="sxs-lookup"><span data-stu-id="84c57-125">Domain</span></span> | <span data-ttu-id="84c57-126">Геометрия</span><span class="sxs-lookup"><span data-stu-id="84c57-126">Geometry</span></span> | <span data-ttu-id="84c57-127">Пиксель</span><span class="sxs-lookup"><span data-stu-id="84c57-127">Pixel</span></span> | <span data-ttu-id="84c57-128">Вычисления</span><span class="sxs-lookup"><span data-stu-id="84c57-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="84c57-129">x</span><span class="sxs-lookup"><span data-stu-id="84c57-129">x</span></span>      | <span data-ttu-id="84c57-130">x</span><span class="sxs-lookup"><span data-stu-id="84c57-130">x</span></span>    | <span data-ttu-id="84c57-131">x</span><span class="sxs-lookup"><span data-stu-id="84c57-131">x</span></span>      | <span data-ttu-id="84c57-132">x</span><span class="sxs-lookup"><span data-stu-id="84c57-132">x</span></span>        | <span data-ttu-id="84c57-133">x</span><span class="sxs-lookup"><span data-stu-id="84c57-133">x</span></span>     | <span data-ttu-id="84c57-134">x</span><span class="sxs-lookup"><span data-stu-id="84c57-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="84c57-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="84c57-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84c57-136">Собрать методы</span><span class="sxs-lookup"><span data-stu-id="84c57-136">Gather methods</span></span>](texture2darray-gather.md)
</dt> <dt>

[<span data-ttu-id="84c57-137">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="84c57-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




