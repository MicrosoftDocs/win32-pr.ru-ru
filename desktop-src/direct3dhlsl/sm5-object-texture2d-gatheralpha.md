---
title: 'Функция Texture2D:: Гасералфа (S, float, int)'
description: 'Возвращает альфа-компоненты четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации. | Функция Texture2D:: Гасералфа (S, float, int)'
ms.assetid: 4c980e06-d768-479e-bee3-1b2541c23038
keywords:
- Функция Гасералфа HLSL
topic_type:
- apiref
api_name:
- GatherAlpha
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 36561e6bc16a84e0a377292ededf58df3c15f800
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986568"
---
# <a name="texture2dgatheralphasfloatint-function"></a><span data-ttu-id="edd5c-105">Функция Texture2D:: Гасералфа (S, float, int)</span><span class="sxs-lookup"><span data-stu-id="edd5c-105">Texture2D::GatherAlpha(S,float,int) function</span></span>

<span data-ttu-id="edd5c-106">Возвращает альфа-компоненты четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="edd5c-106">Returns the alpha components of the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="edd5c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="edd5c-107">Syntax</span></span>

``` syntax
TemplateType GatherAlpha(
  in sampler s,
  in float2 location,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="edd5c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="edd5c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edd5c-109">*s* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="edd5c-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edd5c-110">Тип: **образец**</span><span class="sxs-lookup"><span data-stu-id="edd5c-110">Type: **sampler**</span></span>

<span data-ttu-id="edd5c-111">Индекс выборки с отсчетом от нуля.</span><span class="sxs-lookup"><span data-stu-id="edd5c-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="edd5c-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="edd5c-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edd5c-113">Тип: **float2**</span><span class="sxs-lookup"><span data-stu-id="edd5c-113">Type: **float2**</span></span>

<span data-ttu-id="edd5c-114">Образцы координат (u, v).</span><span class="sxs-lookup"><span data-stu-id="edd5c-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="edd5c-115">*смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="edd5c-115">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edd5c-116">Тип: **int2**</span><span class="sxs-lookup"><span data-stu-id="edd5c-116">Type: **int2**</span></span>

<span data-ttu-id="edd5c-117">Смещение, применяемое к координате текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="edd5c-117">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edd5c-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="edd5c-118">Return value</span></span>

<span data-ttu-id="edd5c-119">Тип: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="edd5c-119">Type: **TemplateType**</span></span>

<span data-ttu-id="edd5c-120">Значение из четырех компонентов, тип которого совпадает с типом шаблона.</span><span class="sxs-lookup"><span data-stu-id="edd5c-120">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="edd5c-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="edd5c-121">Remarks</span></span>

<span data-ttu-id="edd5c-122">Примеры текстур можно использовать для интерполяции билинейной.</span><span class="sxs-lookup"><span data-stu-id="edd5c-122">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="edd5c-123">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="edd5c-123">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="edd5c-124">Вершина</span><span class="sxs-lookup"><span data-stu-id="edd5c-124">Vertex</span></span> | <span data-ttu-id="edd5c-125">Поверхности</span><span class="sxs-lookup"><span data-stu-id="edd5c-125">Hull</span></span> | <span data-ttu-id="edd5c-126">Домен</span><span class="sxs-lookup"><span data-stu-id="edd5c-126">Domain</span></span> | <span data-ttu-id="edd5c-127">Геометрия</span><span class="sxs-lookup"><span data-stu-id="edd5c-127">Geometry</span></span> | <span data-ttu-id="edd5c-128">Пиксель</span><span class="sxs-lookup"><span data-stu-id="edd5c-128">Pixel</span></span> | <span data-ttu-id="edd5c-129">Вычисления</span><span class="sxs-lookup"><span data-stu-id="edd5c-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="edd5c-130">x</span><span class="sxs-lookup"><span data-stu-id="edd5c-130">x</span></span>      | <span data-ttu-id="edd5c-131">x</span><span class="sxs-lookup"><span data-stu-id="edd5c-131">x</span></span>    | <span data-ttu-id="edd5c-132">x</span><span class="sxs-lookup"><span data-stu-id="edd5c-132">x</span></span>      | <span data-ttu-id="edd5c-133">x</span><span class="sxs-lookup"><span data-stu-id="edd5c-133">x</span></span>        | <span data-ttu-id="edd5c-134">x</span><span class="sxs-lookup"><span data-stu-id="edd5c-134">x</span></span>     | <span data-ttu-id="edd5c-135">x</span><span class="sxs-lookup"><span data-stu-id="edd5c-135">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="edd5c-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="edd5c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edd5c-137">Методы Гасералфа</span><span class="sxs-lookup"><span data-stu-id="edd5c-137">GatherAlpha methods</span></span>](texture2d-gatheralpha.md)
</dt> <dt>

[<span data-ttu-id="edd5c-138">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="edd5c-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




