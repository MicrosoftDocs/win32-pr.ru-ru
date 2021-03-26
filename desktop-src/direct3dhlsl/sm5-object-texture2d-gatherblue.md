---
title: 'Функция Texture2D:: Гасерблуе (S, float, int)'
description: 'Возвращает синие компоненты четырех шаг текселя значений, которые будут использоваться в операции линейной фильтрации. | Функция Texture2D:: Гасерблуе (S, float, int)'
ms.assetid: 6d753ef2-2818-4990-81df-52dda044d21d
keywords:
- Функция Гасерблуе HLSL
topic_type:
- apiref
api_name:
- GatherBlue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 54885ccd8f31fdf55270b6c9ac2dbafa1805d866
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986417"
---
# <a name="texture2dgatherbluesfloatint-function"></a><span data-ttu-id="099ed-105">Функция Texture2D:: Гасерблуе (S, float, int)</span><span class="sxs-lookup"><span data-stu-id="099ed-105">Texture2D::GatherBlue(S,float,int) function</span></span>

<span data-ttu-id="099ed-106">Возвращает синие компоненты четырех шаг текселя значений, которые будут использоваться в операции линейной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="099ed-106">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="099ed-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="099ed-107">Syntax</span></span>

``` syntax
TemplateType GatherBlue(
  in sampler s,
  in float2 location,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="099ed-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="099ed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="099ed-109">*s* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="099ed-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="099ed-110">Тип: **образец**</span><span class="sxs-lookup"><span data-stu-id="099ed-110">Type: **sampler**</span></span>

<span data-ttu-id="099ed-111">Индекс выборки с отсчетом от нуля.</span><span class="sxs-lookup"><span data-stu-id="099ed-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="099ed-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="099ed-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="099ed-113">Тип: **float2**</span><span class="sxs-lookup"><span data-stu-id="099ed-113">Type: **float2**</span></span>

<span data-ttu-id="099ed-114">Образцы координат (u, v).</span><span class="sxs-lookup"><span data-stu-id="099ed-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="099ed-115">*смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="099ed-115">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="099ed-116">Тип: **int2**</span><span class="sxs-lookup"><span data-stu-id="099ed-116">Type: **int2**</span></span>

<span data-ttu-id="099ed-117">Смещение, применяемое к координате текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="099ed-117">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="099ed-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="099ed-118">Return value</span></span>

<span data-ttu-id="099ed-119">Тип: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="099ed-119">Type: **TemplateType**</span></span>

<span data-ttu-id="099ed-120">Значение из четырех компонентов, тип которого совпадает с типом шаблона.</span><span class="sxs-lookup"><span data-stu-id="099ed-120">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="099ed-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="099ed-121">Remarks</span></span>

<span data-ttu-id="099ed-122">Примеры текстур можно использовать для интерполяции билинейной.</span><span class="sxs-lookup"><span data-stu-id="099ed-122">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="099ed-123">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="099ed-123">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="099ed-124">Вершина</span><span class="sxs-lookup"><span data-stu-id="099ed-124">Vertex</span></span> | <span data-ttu-id="099ed-125">Поверхности</span><span class="sxs-lookup"><span data-stu-id="099ed-125">Hull</span></span> | <span data-ttu-id="099ed-126">Домен</span><span class="sxs-lookup"><span data-stu-id="099ed-126">Domain</span></span> | <span data-ttu-id="099ed-127">Геометрия</span><span class="sxs-lookup"><span data-stu-id="099ed-127">Geometry</span></span> | <span data-ttu-id="099ed-128">Пиксель</span><span class="sxs-lookup"><span data-stu-id="099ed-128">Pixel</span></span> | <span data-ttu-id="099ed-129">Вычисления</span><span class="sxs-lookup"><span data-stu-id="099ed-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="099ed-130">x</span><span class="sxs-lookup"><span data-stu-id="099ed-130">x</span></span>      | <span data-ttu-id="099ed-131">x</span><span class="sxs-lookup"><span data-stu-id="099ed-131">x</span></span>    | <span data-ttu-id="099ed-132">x</span><span class="sxs-lookup"><span data-stu-id="099ed-132">x</span></span>      | <span data-ttu-id="099ed-133">x</span><span class="sxs-lookup"><span data-stu-id="099ed-133">x</span></span>        | <span data-ttu-id="099ed-134">x</span><span class="sxs-lookup"><span data-stu-id="099ed-134">x</span></span>     | <span data-ttu-id="099ed-135">x</span><span class="sxs-lookup"><span data-stu-id="099ed-135">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="099ed-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="099ed-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="099ed-137">Методы Гасерблуе</span><span class="sxs-lookup"><span data-stu-id="099ed-137">GatherBlue methods</span></span>](texture2d-gatherblue.md)
</dt> <dt>

[<span data-ttu-id="099ed-138">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="099ed-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




