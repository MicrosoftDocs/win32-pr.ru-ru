---
title: 'Функция Texture2D:: собрать (S, float, int)'
description: 'Возвращает четыре значения шаг текселя, которые будут использоваться в операции линейной фильтрации. | Функция Texture2D:: собрать (S, float, int)'
ms.assetid: 5d196c1c-8cc9-4add-9d33-654294314ee2
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
ms.openlocfilehash: 4d0a58be0580572441f91a3b3f637601d70cd9c8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "103820701"
---
# <a name="texture2dgathersfloatint-function"></a><span data-ttu-id="e546d-105">Функция Texture2D:: собрать (S, float, int)</span><span class="sxs-lookup"><span data-stu-id="e546d-105">Texture2D::Gather(S,float,int) function</span></span>

<span data-ttu-id="e546d-106">Возвращает четыре значения шаг текселя, которые будут использоваться в операции линейной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="e546d-106">Returns the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="e546d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e546d-107">Syntax</span></span>

``` syntax
TemplateType Gather(
  in sampler s,
  in float2 location,
  in int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="e546d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e546d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e546d-109">*s* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="e546d-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e546d-110">Тип: **образец**</span><span class="sxs-lookup"><span data-stu-id="e546d-110">Type: **sampler**</span></span>

<span data-ttu-id="e546d-111">Индекс выборки с отсчетом от нуля.</span><span class="sxs-lookup"><span data-stu-id="e546d-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="e546d-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e546d-112">*location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e546d-113">Тип: **float2**</span><span class="sxs-lookup"><span data-stu-id="e546d-113">Type: **float2**</span></span>

<span data-ttu-id="e546d-114">Образцы координат (u, v).</span><span class="sxs-lookup"><span data-stu-id="e546d-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="e546d-115">*смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e546d-115">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e546d-116">Тип: **int2**</span><span class="sxs-lookup"><span data-stu-id="e546d-116">Type: **int2**</span></span>

<span data-ttu-id="e546d-117">Смещение, применяемое к координатам текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="e546d-117">The offset applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e546d-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e546d-118">Return value</span></span>

<span data-ttu-id="e546d-119">Тип: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="e546d-119">Type: **TemplateType**</span></span>

<span data-ttu-id="e546d-120">Значение из четырех компонентов, тип которого совпадает с типом шаблона.</span><span class="sxs-lookup"><span data-stu-id="e546d-120">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="e546d-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="e546d-121">Remarks</span></span>

<span data-ttu-id="e546d-122">Примеры текстур можно использовать для интерполяции билинейной.</span><span class="sxs-lookup"><span data-stu-id="e546d-122">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="e546d-123">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="e546d-123">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="e546d-124">Вершина</span><span class="sxs-lookup"><span data-stu-id="e546d-124">Vertex</span></span> | <span data-ttu-id="e546d-125">Поверхности</span><span class="sxs-lookup"><span data-stu-id="e546d-125">Hull</span></span> | <span data-ttu-id="e546d-126">Домен</span><span class="sxs-lookup"><span data-stu-id="e546d-126">Domain</span></span> | <span data-ttu-id="e546d-127">Геометрия</span><span class="sxs-lookup"><span data-stu-id="e546d-127">Geometry</span></span> | <span data-ttu-id="e546d-128">Пиксель</span><span class="sxs-lookup"><span data-stu-id="e546d-128">Pixel</span></span> | <span data-ttu-id="e546d-129">Вычисления</span><span class="sxs-lookup"><span data-stu-id="e546d-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e546d-130">x</span><span class="sxs-lookup"><span data-stu-id="e546d-130">x</span></span>      | <span data-ttu-id="e546d-131">x</span><span class="sxs-lookup"><span data-stu-id="e546d-131">x</span></span>    | <span data-ttu-id="e546d-132">x</span><span class="sxs-lookup"><span data-stu-id="e546d-132">x</span></span>      | <span data-ttu-id="e546d-133">x</span><span class="sxs-lookup"><span data-stu-id="e546d-133">x</span></span>        | <span data-ttu-id="e546d-134">x</span><span class="sxs-lookup"><span data-stu-id="e546d-134">x</span></span>     | <span data-ttu-id="e546d-135">x</span><span class="sxs-lookup"><span data-stu-id="e546d-135">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="e546d-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e546d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e546d-137">Собрать методы</span><span class="sxs-lookup"><span data-stu-id="e546d-137">Gather methods</span></span>](texture2d-gather.md)
</dt> <dt>

[<span data-ttu-id="e546d-138">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="e546d-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




