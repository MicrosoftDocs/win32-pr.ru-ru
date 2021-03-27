---
title: 'Функция Texture2DArray:: Гасералфа (S, float, int2, int2, int2, int2)'
description: 'Возвращает альфа-компоненты четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации. | Функция Texture2DArray:: Гасералфа (S, float, int2, int2, int2, int2)'
ms.assetid: A7F96B45-A097-437B-A0D0-18555FF76544
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
ms.openlocfilehash: ff6910152c9ac133c819456b9ec7aaeb2406b791
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104000092"
---
# <a name="texture2darraygatheralphasfloatint2int2int2int2-function"></a><span data-ttu-id="ee281-105">Функция Texture2DArray:: Гасералфа (S, float, int2, int2, int2, int2)</span><span class="sxs-lookup"><span data-stu-id="ee281-105">Texture2DArray::GatherAlpha(S,float,int2,int2,int2,int2) function</span></span>

<span data-ttu-id="ee281-106">Возвращает альфа-компоненты четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="ee281-106">Returns the alpha components of the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee281-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ee281-107">Syntax</span></span>


``` syntax
TemplateType GatherAlpha(
  in SamplerState S,
  in float        Location,
  in int2         Offset1,
  in int2         Offset2,
  in int2         Offset3,
  in int2         Offset4
);
```



## <a name="parameters"></a><span data-ttu-id="ee281-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ee281-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee281-109">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="ee281-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee281-110">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="ee281-110">Type: **SamplerState**</span></span>

<span data-ttu-id="ee281-111">Индекс выборки с отсчетом от нуля.</span><span class="sxs-lookup"><span data-stu-id="ee281-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="ee281-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ee281-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee281-113">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="ee281-113">Type: **float**</span></span>

<span data-ttu-id="ee281-114">Образцы координат (u, v).</span><span class="sxs-lookup"><span data-stu-id="ee281-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="ee281-115">*Offset1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ee281-115">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee281-116">Тип: **int2**</span><span class="sxs-lookup"><span data-stu-id="ee281-116">Type: **int2**</span></span>

<span data-ttu-id="ee281-117">Первый компонент смещения, применяемый к координатам текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="ee281-117">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="ee281-118">*Offset2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ee281-118">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee281-119">Тип: **int2**</span><span class="sxs-lookup"><span data-stu-id="ee281-119">Type: **int2**</span></span>

<span data-ttu-id="ee281-120">Второй компонент смещения, применяемый к координатам текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="ee281-120">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="ee281-121">*Offset3* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ee281-121">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee281-122">Тип: **int2**</span><span class="sxs-lookup"><span data-stu-id="ee281-122">Type: **int2**</span></span>

<span data-ttu-id="ee281-123">Третий компонент смещения, применяемый к координатам текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="ee281-123">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="ee281-124">*Offset4* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ee281-124">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee281-125">Тип: **int2**</span><span class="sxs-lookup"><span data-stu-id="ee281-125">Type: **int2**</span></span>

<span data-ttu-id="ee281-126">Четвертый компонент смещения, применяемый к координатам текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="ee281-126">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee281-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ee281-127">Return value</span></span>

<span data-ttu-id="ee281-128">Тип: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="ee281-128">Type: **TemplateType**</span></span>

<span data-ttu-id="ee281-129">Значение из четырех компонентов, тип которого совпадает с типом шаблона.</span><span class="sxs-lookup"><span data-stu-id="ee281-129">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee281-130">Примечания</span><span class="sxs-lookup"><span data-stu-id="ee281-130">Remarks</span></span>

<span data-ttu-id="ee281-131">Примеры текстур можно использовать для интерполяции билинейной.</span><span class="sxs-lookup"><span data-stu-id="ee281-131">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="ee281-132">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="ee281-132">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="ee281-133">Вершина</span><span class="sxs-lookup"><span data-stu-id="ee281-133">Vertex</span></span> | <span data-ttu-id="ee281-134">Поверхности</span><span class="sxs-lookup"><span data-stu-id="ee281-134">Hull</span></span> | <span data-ttu-id="ee281-135">Домен</span><span class="sxs-lookup"><span data-stu-id="ee281-135">Domain</span></span> | <span data-ttu-id="ee281-136">Геометрия</span><span class="sxs-lookup"><span data-stu-id="ee281-136">Geometry</span></span> | <span data-ttu-id="ee281-137">Пиксель</span><span class="sxs-lookup"><span data-stu-id="ee281-137">Pixel</span></span> | <span data-ttu-id="ee281-138">Вычисления</span><span class="sxs-lookup"><span data-stu-id="ee281-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ee281-139">x</span><span class="sxs-lookup"><span data-stu-id="ee281-139">x</span></span>      | <span data-ttu-id="ee281-140">x</span><span class="sxs-lookup"><span data-stu-id="ee281-140">x</span></span>    | <span data-ttu-id="ee281-141">x</span><span class="sxs-lookup"><span data-stu-id="ee281-141">x</span></span>      | <span data-ttu-id="ee281-142">x</span><span class="sxs-lookup"><span data-stu-id="ee281-142">x</span></span>        | <span data-ttu-id="ee281-143">x</span><span class="sxs-lookup"><span data-stu-id="ee281-143">x</span></span>     | <span data-ttu-id="ee281-144">x</span><span class="sxs-lookup"><span data-stu-id="ee281-144">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="ee281-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ee281-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee281-146">Методы Гасералфа</span><span class="sxs-lookup"><span data-stu-id="ee281-146">GatherAlpha methods</span></span>](texture2darray-gatheralpha.md)
</dt> </dl>

 

 




