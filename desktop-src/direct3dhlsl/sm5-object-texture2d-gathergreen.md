---
title: 'Функция Texture2D:: Гасергрин (S, float, int)'
description: 'Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, функция возвращает сравнение зеленого компонента со значением сравнения. | Функция Texture2D:: Гасергрин (S, float, int)'
ms.assetid: 97e1fb52-75f4-4e73-93f1-98b7a5925efc
keywords:
- Функция Гасергрин HLSL
topic_type:
- apiref
api_name:
- GatherGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 722d7a3ac90fa3083b8f42f7704f5c9e0aeb1829
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998146"
---
# <a name="texture2dgathergreensfloatint-function"></a><span data-ttu-id="ade4e-105">Функция Texture2D:: Гасергрин (S, float, int)</span><span class="sxs-lookup"><span data-stu-id="ade4e-105">Texture2D::GatherGreen(S,float,int) function</span></span>

<span data-ttu-id="ade4e-106">Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, функция возвращает сравнение зеленого компонента со значением сравнения.</span><span class="sxs-lookup"><span data-stu-id="ade4e-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their green component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="ade4e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ade4e-107">Syntax</span></span>

``` syntax
TemplateType GatherGreen(
  in sampler s,
  in float2 location,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="ade4e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ade4e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ade4e-109">*s* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="ade4e-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ade4e-110">Тип: **образец**</span><span class="sxs-lookup"><span data-stu-id="ade4e-110">Type: **sampler**</span></span>

<span data-ttu-id="ade4e-111">Индекс выборки с отсчетом от нуля.</span><span class="sxs-lookup"><span data-stu-id="ade4e-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="ade4e-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ade4e-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ade4e-113">Тип: **float2**</span><span class="sxs-lookup"><span data-stu-id="ade4e-113">Type: **float2**</span></span>

<span data-ttu-id="ade4e-114">Образцы координат (u, v).</span><span class="sxs-lookup"><span data-stu-id="ade4e-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="ade4e-115">*смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ade4e-115">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ade4e-116">Тип: **int2**</span><span class="sxs-lookup"><span data-stu-id="ade4e-116">Type: **int2**</span></span>

<span data-ttu-id="ade4e-117">Смещение, применяемое к координате текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="ade4e-117">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ade4e-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ade4e-118">Return value</span></span>

<span data-ttu-id="ade4e-119">Тип: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="ade4e-119">Type: **TemplateType**</span></span>

<span data-ttu-id="ade4e-120">Значение из четырех компонентов, тип которого совпадает с типом шаблона.</span><span class="sxs-lookup"><span data-stu-id="ade4e-120">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="ade4e-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="ade4e-121">Remarks</span></span>

<span data-ttu-id="ade4e-122">Примеры текстур можно использовать для интерполяции билинейной.</span><span class="sxs-lookup"><span data-stu-id="ade4e-122">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="ade4e-123">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="ade4e-123">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="ade4e-124">Вершина</span><span class="sxs-lookup"><span data-stu-id="ade4e-124">Vertex</span></span> | <span data-ttu-id="ade4e-125">Поверхности</span><span class="sxs-lookup"><span data-stu-id="ade4e-125">Hull</span></span> | <span data-ttu-id="ade4e-126">Домен</span><span class="sxs-lookup"><span data-stu-id="ade4e-126">Domain</span></span> | <span data-ttu-id="ade4e-127">Геометрия</span><span class="sxs-lookup"><span data-stu-id="ade4e-127">Geometry</span></span> | <span data-ttu-id="ade4e-128">Пиксель</span><span class="sxs-lookup"><span data-stu-id="ade4e-128">Pixel</span></span> | <span data-ttu-id="ade4e-129">Вычисления</span><span class="sxs-lookup"><span data-stu-id="ade4e-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ade4e-130">x</span><span class="sxs-lookup"><span data-stu-id="ade4e-130">x</span></span>      | <span data-ttu-id="ade4e-131">x</span><span class="sxs-lookup"><span data-stu-id="ade4e-131">x</span></span>    | <span data-ttu-id="ade4e-132">x</span><span class="sxs-lookup"><span data-stu-id="ade4e-132">x</span></span>      | <span data-ttu-id="ade4e-133">x</span><span class="sxs-lookup"><span data-stu-id="ade4e-133">x</span></span>        | <span data-ttu-id="ade4e-134">x</span><span class="sxs-lookup"><span data-stu-id="ade4e-134">x</span></span>     | <span data-ttu-id="ade4e-135">x</span><span class="sxs-lookup"><span data-stu-id="ade4e-135">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ade4e-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ade4e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ade4e-137">Методы Гасергрин</span><span class="sxs-lookup"><span data-stu-id="ade4e-137">GatherGreen methods</span></span>](texture2d-gathergreen.md)
</dt> <dt>

[<span data-ttu-id="ade4e-138">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="ade4e-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




