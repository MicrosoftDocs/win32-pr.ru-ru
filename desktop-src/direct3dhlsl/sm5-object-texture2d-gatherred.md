---
title: 'Функция Texture2D:: Гасерред (S, float, int)'
description: 'Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, функция возвращает сравнение их красного компонента со значением сравнения. | Функция Texture2D:: Гасерред (S, float, int)'
ms.assetid: 6d2d1556-d52f-4625-93ca-34da399f9a8b
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
ms.openlocfilehash: f05196063f6a17cc34865157c17a92bc2bb116bf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986513"
---
# <a name="texture2dgatherredsfloatint-function"></a><span data-ttu-id="b4460-105">Функция Texture2D:: Гасерред (S, float, int)</span><span class="sxs-lookup"><span data-stu-id="b4460-105">Texture2D::GatherRed(S,float,int) function</span></span>

<span data-ttu-id="b4460-106">Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, функция возвращает сравнение их красного компонента со значением сравнения.</span><span class="sxs-lookup"><span data-stu-id="b4460-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their red component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4460-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4460-107">Syntax</span></span>

``` syntax
TemplateType GatherRed(
  in sampler s,
  in float2 location,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="b4460-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b4460-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4460-109">*s* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="b4460-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4460-110">Тип: **образец**</span><span class="sxs-lookup"><span data-stu-id="b4460-110">Type: **sampler**</span></span>

<span data-ttu-id="b4460-111">Индекс выборки с отсчетом от нуля.</span><span class="sxs-lookup"><span data-stu-id="b4460-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="b4460-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b4460-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4460-113">Тип: **float2**</span><span class="sxs-lookup"><span data-stu-id="b4460-113">Type: **float2**</span></span>

<span data-ttu-id="b4460-114">Образцы координат (u, v).</span><span class="sxs-lookup"><span data-stu-id="b4460-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="b4460-115">*смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b4460-115">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4460-116">Тип: **int2**</span><span class="sxs-lookup"><span data-stu-id="b4460-116">Type: **int2**</span></span>

<span data-ttu-id="b4460-117">Смещение, применяемое к координате текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="b4460-117">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4460-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b4460-118">Return value</span></span>

<span data-ttu-id="b4460-119">Тип: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="b4460-119">Type: **TemplateType**</span></span>

<span data-ttu-id="b4460-120">Значение из четырех компонентов, тип которого совпадает с типом шаблона.</span><span class="sxs-lookup"><span data-stu-id="b4460-120">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4460-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="b4460-121">Remarks</span></span>

<span data-ttu-id="b4460-122">Примеры текстур можно использовать для интерполяции билинейной.</span><span class="sxs-lookup"><span data-stu-id="b4460-122">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="b4460-123">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="b4460-123">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="b4460-124">Вершина</span><span class="sxs-lookup"><span data-stu-id="b4460-124">Vertex</span></span> | <span data-ttu-id="b4460-125">Поверхности</span><span class="sxs-lookup"><span data-stu-id="b4460-125">Hull</span></span> | <span data-ttu-id="b4460-126">Домен</span><span class="sxs-lookup"><span data-stu-id="b4460-126">Domain</span></span> | <span data-ttu-id="b4460-127">Геометрия</span><span class="sxs-lookup"><span data-stu-id="b4460-127">Geometry</span></span> | <span data-ttu-id="b4460-128">Пиксель</span><span class="sxs-lookup"><span data-stu-id="b4460-128">Pixel</span></span> | <span data-ttu-id="b4460-129">Вычисления</span><span class="sxs-lookup"><span data-stu-id="b4460-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="b4460-130">x</span><span class="sxs-lookup"><span data-stu-id="b4460-130">x</span></span>      | <span data-ttu-id="b4460-131">x</span><span class="sxs-lookup"><span data-stu-id="b4460-131">x</span></span>    | <span data-ttu-id="b4460-132">x</span><span class="sxs-lookup"><span data-stu-id="b4460-132">x</span></span>      | <span data-ttu-id="b4460-133">x</span><span class="sxs-lookup"><span data-stu-id="b4460-133">x</span></span>        | <span data-ttu-id="b4460-134">x</span><span class="sxs-lookup"><span data-stu-id="b4460-134">x</span></span>     | <span data-ttu-id="b4460-135">x</span><span class="sxs-lookup"><span data-stu-id="b4460-135">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b4460-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b4460-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4460-137">Методы Гасерред</span><span class="sxs-lookup"><span data-stu-id="b4460-137">GatherRed methods</span></span>](texture2d-gatherred.md)
</dt> <dt>

[<span data-ttu-id="b4460-138">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="b4460-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




