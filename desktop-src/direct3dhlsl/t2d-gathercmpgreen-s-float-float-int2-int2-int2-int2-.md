---
title: 'Функция Texture2D:: Гасеркмпгрин (S, float, float, int2, int2, int2, int2)'
description: 'Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, функция возвращает сравнение зеленого компонента со значением сравнения. | Функция Texture2D:: Гасеркмпгрин (S, float, float, int2, int2, int2, int2)'
ms.assetid: AC19838B-BA51-408D-8299-DC5F4551628C
keywords:
- Функция Гасеркмпгрин HLSL
topic_type:
- apiref
api_name:
- GatherCmpGreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ffcb312bd450b7c468a1fc83d57ff91b102db8a1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352742"
---
# <a name="texture2dgathercmpgreensfloatfloatint2int2int2int2-function"></a><span data-ttu-id="1e7c7-105">Функция Texture2D:: Гасеркмпгрин (S, float, float, int2, int2, int2, int2)</span><span class="sxs-lookup"><span data-stu-id="1e7c7-105">Texture2D::GatherCmpGreen(S,float,float,int2,int2,int2,int2) function</span></span>

<span data-ttu-id="1e7c7-106">Для четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации, функция возвращает сравнение зеленого компонента со значением сравнения.</span><span class="sxs-lookup"><span data-stu-id="1e7c7-106">For four texel values that would be used in a bi-linear filtering operation, returns a comparison of their green component against a compare value.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e7c7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1e7c7-107">Syntax</span></span>


``` syntax
TemplateType GatherCmpGreen(
  in SamplerState S,
  in float        Location,
  in float        CompareValue,
  in int2         Offset1,
  in int2         Offset2,
  in int2         Offset3,
  in int2         Offset4
);
```



## <a name="parameters"></a><span data-ttu-id="1e7c7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1e7c7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e7c7-109">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="1e7c7-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e7c7-110">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="1e7c7-110">Type: **SamplerState**</span></span>

<span data-ttu-id="1e7c7-111">Индекс выборки с отсчетом от нуля.</span><span class="sxs-lookup"><span data-stu-id="1e7c7-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="1e7c7-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1e7c7-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e7c7-113">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="1e7c7-113">Type: **float**</span></span>

<span data-ttu-id="1e7c7-114">Образцы координат (u, v).</span><span class="sxs-lookup"><span data-stu-id="1e7c7-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="1e7c7-115">*Компаревалуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1e7c7-115">*CompareValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e7c7-116">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="1e7c7-116">Type: **float**</span></span>

<span data-ttu-id="1e7c7-117">Значение, сравниваемое по каждому значению выборки.</span><span class="sxs-lookup"><span data-stu-id="1e7c7-117">A value to compare each against each sampled value.</span></span>

</dd> <dt>

<span data-ttu-id="1e7c7-118">*Offset1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1e7c7-118">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e7c7-119">Тип: **int2**</span><span class="sxs-lookup"><span data-stu-id="1e7c7-119">Type: **int2**</span></span>

<span data-ttu-id="1e7c7-120">Первый компонент смещения, применяемый к координатам текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="1e7c7-120">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="1e7c7-121">*Offset2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1e7c7-121">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e7c7-122">Тип: **int2**</span><span class="sxs-lookup"><span data-stu-id="1e7c7-122">Type: **int2**</span></span>

<span data-ttu-id="1e7c7-123">Второй компонент смещения, применяемый к координатам текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="1e7c7-123">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="1e7c7-124">*Offset3* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1e7c7-124">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e7c7-125">Тип: **int2**</span><span class="sxs-lookup"><span data-stu-id="1e7c7-125">Type: **int2**</span></span>

<span data-ttu-id="1e7c7-126">Третий компонент смещения, применяемый к координатам текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="1e7c7-126">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="1e7c7-127">*Offset4* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1e7c7-127">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e7c7-128">Тип: **int2**</span><span class="sxs-lookup"><span data-stu-id="1e7c7-128">Type: **int2**</span></span>

<span data-ttu-id="1e7c7-129">Четвертый компонент смещения, применяемый к координатам текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="1e7c7-129">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e7c7-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1e7c7-130">Return value</span></span>

<span data-ttu-id="1e7c7-131">Тип: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="1e7c7-131">Type: **TemplateType**</span></span>

<span data-ttu-id="1e7c7-132">Значение из четырех компонентов, тип которого совпадает с типом шаблона.</span><span class="sxs-lookup"><span data-stu-id="1e7c7-132">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e7c7-133">Примечания</span><span class="sxs-lookup"><span data-stu-id="1e7c7-133">Remarks</span></span>

<span data-ttu-id="1e7c7-134">Примеры текстур можно использовать для интерполяции билинейной.</span><span class="sxs-lookup"><span data-stu-id="1e7c7-134">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="1e7c7-135">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="1e7c7-135">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="1e7c7-136">Вершина</span><span class="sxs-lookup"><span data-stu-id="1e7c7-136">Vertex</span></span> | <span data-ttu-id="1e7c7-137">Поверхности</span><span class="sxs-lookup"><span data-stu-id="1e7c7-137">Hull</span></span> | <span data-ttu-id="1e7c7-138">Домен</span><span class="sxs-lookup"><span data-stu-id="1e7c7-138">Domain</span></span> | <span data-ttu-id="1e7c7-139">Геометрия</span><span class="sxs-lookup"><span data-stu-id="1e7c7-139">Geometry</span></span> | <span data-ttu-id="1e7c7-140">Пиксель</span><span class="sxs-lookup"><span data-stu-id="1e7c7-140">Pixel</span></span> | <span data-ttu-id="1e7c7-141">Вычисления</span><span class="sxs-lookup"><span data-stu-id="1e7c7-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="1e7c7-142">x</span><span class="sxs-lookup"><span data-stu-id="1e7c7-142">x</span></span>      | <span data-ttu-id="1e7c7-143">x</span><span class="sxs-lookup"><span data-stu-id="1e7c7-143">x</span></span>    | <span data-ttu-id="1e7c7-144">x</span><span class="sxs-lookup"><span data-stu-id="1e7c7-144">x</span></span>      | <span data-ttu-id="1e7c7-145">x</span><span class="sxs-lookup"><span data-stu-id="1e7c7-145">x</span></span>        | <span data-ttu-id="1e7c7-146">x</span><span class="sxs-lookup"><span data-stu-id="1e7c7-146">x</span></span>     | <span data-ttu-id="1e7c7-147">x</span><span class="sxs-lookup"><span data-stu-id="1e7c7-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="1e7c7-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1e7c7-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e7c7-149">Методы Гасеркмпгрин</span><span class="sxs-lookup"><span data-stu-id="1e7c7-149">GatherCmpGreen methods</span></span>](texture2d-gathercmpgreen.md)
</dt> </dl>

 

 




