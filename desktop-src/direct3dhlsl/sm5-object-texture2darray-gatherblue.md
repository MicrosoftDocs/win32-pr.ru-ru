---
title: 'Функция Texture2DArray:: Гасерблуе (S, float, int)'
description: 'Возвращает синие компоненты четырех шаг текселя значений, которые будут использоваться в операции линейной фильтрации. | Функция Texture2DArray:: Гасерблуе (S, float, int)'
ms.assetid: f81596b5-afd1-4baf-b6c0-ca4661a3ef22
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
ms.openlocfilehash: 1844b898deca767b04aba438f4784a54a5afa112
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998071"
---
# <a name="texture2darraygatherbluesfloatint-function"></a><span data-ttu-id="c5089-105">Функция Texture2DArray:: Гасерблуе (S, float, int)</span><span class="sxs-lookup"><span data-stu-id="c5089-105">Texture2DArray::GatherBlue(S,float,int) function</span></span>

<span data-ttu-id="c5089-106">Возвращает синие компоненты четырех шаг текселя значений, которые будут использоваться в операции линейной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="c5089-106">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5089-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c5089-107">Syntax</span></span>

``` syntax
TemplateType GatherBlue(
  in sampler s,
  in float3 location,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="c5089-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c5089-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5089-109">*s* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="c5089-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5089-110">Тип: **образец**</span><span class="sxs-lookup"><span data-stu-id="c5089-110">Type: **sampler**</span></span>

<span data-ttu-id="c5089-111">Индекс выборки с отсчетом от нуля.</span><span class="sxs-lookup"><span data-stu-id="c5089-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="c5089-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c5089-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5089-113">Тип: **float3**</span><span class="sxs-lookup"><span data-stu-id="c5089-113">Type: **float3**</span></span>

<span data-ttu-id="c5089-114">Образцы координат (u, v).</span><span class="sxs-lookup"><span data-stu-id="c5089-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="c5089-115">*смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c5089-115">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5089-116">Тип: **int2**</span><span class="sxs-lookup"><span data-stu-id="c5089-116">Type: **int2**</span></span>

<span data-ttu-id="c5089-117">Смещение, применяемое к координате текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="c5089-117">An offset that is applied to the texture coordinate before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5089-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c5089-118">Return value</span></span>

<span data-ttu-id="c5089-119">Тип: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="c5089-119">Type: **TemplateType**</span></span>

<span data-ttu-id="c5089-120">Значение из четырех компонентов, тип которого совпадает с типом шаблона.</span><span class="sxs-lookup"><span data-stu-id="c5089-120">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5089-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="c5089-121">Remarks</span></span>

<span data-ttu-id="c5089-122">Примеры текстур можно использовать для интерполяции билинейной.</span><span class="sxs-lookup"><span data-stu-id="c5089-122">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="c5089-123">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="c5089-123">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="c5089-124">Вершина</span><span class="sxs-lookup"><span data-stu-id="c5089-124">Vertex</span></span> | <span data-ttu-id="c5089-125">Поверхности</span><span class="sxs-lookup"><span data-stu-id="c5089-125">Hull</span></span> | <span data-ttu-id="c5089-126">Домен</span><span class="sxs-lookup"><span data-stu-id="c5089-126">Domain</span></span> | <span data-ttu-id="c5089-127">Геометрия</span><span class="sxs-lookup"><span data-stu-id="c5089-127">Geometry</span></span> | <span data-ttu-id="c5089-128">Пиксель</span><span class="sxs-lookup"><span data-stu-id="c5089-128">Pixel</span></span> | <span data-ttu-id="c5089-129">Вычисления</span><span class="sxs-lookup"><span data-stu-id="c5089-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="c5089-130">x</span><span class="sxs-lookup"><span data-stu-id="c5089-130">x</span></span>      | <span data-ttu-id="c5089-131">x</span><span class="sxs-lookup"><span data-stu-id="c5089-131">x</span></span>    | <span data-ttu-id="c5089-132">x</span><span class="sxs-lookup"><span data-stu-id="c5089-132">x</span></span>      | <span data-ttu-id="c5089-133">x</span><span class="sxs-lookup"><span data-stu-id="c5089-133">x</span></span>        | <span data-ttu-id="c5089-134">x</span><span class="sxs-lookup"><span data-stu-id="c5089-134">x</span></span>     | <span data-ttu-id="c5089-135">x</span><span class="sxs-lookup"><span data-stu-id="c5089-135">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="c5089-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c5089-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5089-137">Методы Гасерблуе</span><span class="sxs-lookup"><span data-stu-id="c5089-137">GatherBlue methods</span></span>](texture2darray-gatherblue.md)
</dt> <dt>

[<span data-ttu-id="c5089-138">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="c5089-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




