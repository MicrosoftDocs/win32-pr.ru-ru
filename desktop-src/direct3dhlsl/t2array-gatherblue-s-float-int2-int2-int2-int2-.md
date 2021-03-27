---
title: Функция Гасерблуе (S, float, int2, int2, int2, int2) (HLSL Reference)
description: Возвращает синие компоненты четырех шаг текселя значений, которые будут использоваться в операции линейной фильтрации. | Функция Гасерблуе (S, float, int2, int2, int2, int2) (HLSL Reference)
ms.assetid: 0DDD3235-4F12-4D74-975A-F70A271C1FC0
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
ms.openlocfilehash: a5676d9d6b25c6e67123c59dac14efa234386d4e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353542"
---
# <a name="gatherbluesfloatint2int2int2int2-function-hlsl-reference"></a><span data-ttu-id="396c9-105">Функция Гасерблуе (S, float, int2, int2, int2, int2) (HLSL Reference)</span><span class="sxs-lookup"><span data-stu-id="396c9-105">GatherBlue(S,float,int2,int2,int2,int2) function (HLSL reference)</span></span>

<span data-ttu-id="396c9-106">Возвращает синие компоненты четырех шаг текселя значений, которые будут использоваться в операции линейной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="396c9-106">Returns the blue components of the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="396c9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="396c9-107">Syntax</span></span>


``` syntax
TemplateType GatherBlue(
  in SamplerState S,
  in float        Location,
  in int2         Offset1,
  in int2         Offset2,
  in int2         Offset3,
  in int2         Offset4
);
```



## <a name="parameters"></a><span data-ttu-id="396c9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="396c9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="396c9-109">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="396c9-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="396c9-110">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="396c9-110">Type: **SamplerState**</span></span>

<span data-ttu-id="396c9-111">Индекс выборки с отсчетом от нуля.</span><span class="sxs-lookup"><span data-stu-id="396c9-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="396c9-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="396c9-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="396c9-113">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="396c9-113">Type: **float**</span></span>

<span data-ttu-id="396c9-114">Образцы координат (u, v).</span><span class="sxs-lookup"><span data-stu-id="396c9-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="396c9-115">*Offset1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="396c9-115">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="396c9-116">Тип: **int2**</span><span class="sxs-lookup"><span data-stu-id="396c9-116">Type: **int2**</span></span>

<span data-ttu-id="396c9-117">Первый компонент смещения, применяемый к координатам текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="396c9-117">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="396c9-118">*Offset2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="396c9-118">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="396c9-119">Тип: **int2**</span><span class="sxs-lookup"><span data-stu-id="396c9-119">Type: **int2**</span></span>

<span data-ttu-id="396c9-120">Второй компонент смещения, применяемый к координатам текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="396c9-120">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="396c9-121">*Offset3* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="396c9-121">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="396c9-122">Тип: **int2**</span><span class="sxs-lookup"><span data-stu-id="396c9-122">Type: **int2**</span></span>

<span data-ttu-id="396c9-123">Третий компонент смещения, применяемый к координатам текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="396c9-123">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="396c9-124">*Offset4* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="396c9-124">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="396c9-125">Тип: **int2**</span><span class="sxs-lookup"><span data-stu-id="396c9-125">Type: **int2**</span></span>

<span data-ttu-id="396c9-126">Четвертый компонент смещения, применяемый к координатам текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="396c9-126">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="396c9-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="396c9-127">Return value</span></span>

<span data-ttu-id="396c9-128">Тип: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="396c9-128">Type: **TemplateType**</span></span>

<span data-ttu-id="396c9-129">Значение из четырех компонентов, тип которого совпадает с типом шаблона.</span><span class="sxs-lookup"><span data-stu-id="396c9-129">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="396c9-130">Примечания</span><span class="sxs-lookup"><span data-stu-id="396c9-130">Remarks</span></span>

<span data-ttu-id="396c9-131">Примеры текстур можно использовать для интерполяции билинейной.</span><span class="sxs-lookup"><span data-stu-id="396c9-131">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="396c9-132">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="396c9-132">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="396c9-133">Вершина</span><span class="sxs-lookup"><span data-stu-id="396c9-133">Vertex</span></span> | <span data-ttu-id="396c9-134">Поверхности</span><span class="sxs-lookup"><span data-stu-id="396c9-134">Hull</span></span> | <span data-ttu-id="396c9-135">Домен</span><span class="sxs-lookup"><span data-stu-id="396c9-135">Domain</span></span> | <span data-ttu-id="396c9-136">Геометрия</span><span class="sxs-lookup"><span data-stu-id="396c9-136">Geometry</span></span> | <span data-ttu-id="396c9-137">Пиксель</span><span class="sxs-lookup"><span data-stu-id="396c9-137">Pixel</span></span> | <span data-ttu-id="396c9-138">Вычисления</span><span class="sxs-lookup"><span data-stu-id="396c9-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="396c9-139">x</span><span class="sxs-lookup"><span data-stu-id="396c9-139">x</span></span>      | <span data-ttu-id="396c9-140">x</span><span class="sxs-lookup"><span data-stu-id="396c9-140">x</span></span>    | <span data-ttu-id="396c9-141">x</span><span class="sxs-lookup"><span data-stu-id="396c9-141">x</span></span>      | <span data-ttu-id="396c9-142">x</span><span class="sxs-lookup"><span data-stu-id="396c9-142">x</span></span>        | <span data-ttu-id="396c9-143">x</span><span class="sxs-lookup"><span data-stu-id="396c9-143">x</span></span>     | <span data-ttu-id="396c9-144">x</span><span class="sxs-lookup"><span data-stu-id="396c9-144">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="396c9-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="396c9-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="396c9-146">Методы Гасерблуе</span><span class="sxs-lookup"><span data-stu-id="396c9-146">GatherBlue methods</span></span>](texture2darray-gatherblue.md)
</dt> </dl>

 

 




