---
title: 'Функция Texture2D:: Гасергрин (S, float, int2, int2, int2, int2)'
description: 'Возвращает зеленые компоненты четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации. | Функция Texture2D:: Гасергрин (S, float, int2, int2, int2, int2)'
ms.assetid: 043434C0-BB12-4A08-A3E5-34C9738DEBDB
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
ms.openlocfilehash: af1bbaf4052bab32ab1841542bfb63322de154ba
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104547658"
---
# <a name="texture2dgathergreensfloatint2int2int2int2-function"></a><span data-ttu-id="12602-105">Функция Texture2D:: Гасергрин (S, float, int2, int2, int2, int2)</span><span class="sxs-lookup"><span data-stu-id="12602-105">Texture2D::GatherGreen(S,float,int2,int2,int2,int2) function</span></span>

<span data-ttu-id="12602-106">Возвращает зеленые компоненты четырех значений шаг текселя, которые будут использоваться в операции линейной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="12602-106">Returns the green components of the four texel values that would be used in a bi-linear filtering operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="12602-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="12602-107">Syntax</span></span>


``` syntax
TemplateType GatherGreen(
  in SamplerState S,
  in float        Location,
  in int2         Offset1,
  in int2         Offset2,
  in int2         Offset3,
  in int2         Offset4
);
```



## <a name="parameters"></a><span data-ttu-id="12602-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="12602-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12602-109">*S* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="12602-109">*S* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12602-110">Тип: **самплерстате**</span><span class="sxs-lookup"><span data-stu-id="12602-110">Type: **SamplerState**</span></span>

<span data-ttu-id="12602-111">Индекс выборки с отсчетом от нуля.</span><span class="sxs-lookup"><span data-stu-id="12602-111">The zero-based sampler index.</span></span>

</dd> <dt>

<span data-ttu-id="12602-112">*Расположение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="12602-112">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12602-113">Тип: **float**</span><span class="sxs-lookup"><span data-stu-id="12602-113">Type: **float**</span></span>

<span data-ttu-id="12602-114">Образцы координат (u, v).</span><span class="sxs-lookup"><span data-stu-id="12602-114">The sample coordinates (u,v).</span></span>

</dd> <dt>

<span data-ttu-id="12602-115">*Offset1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="12602-115">*Offset1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12602-116">Тип: **int2**</span><span class="sxs-lookup"><span data-stu-id="12602-116">Type: **int2**</span></span>

<span data-ttu-id="12602-117">Первый компонент смещения, применяемый к координатам текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="12602-117">The first offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="12602-118">*Offset2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="12602-118">*Offset2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12602-119">Тип: **int2**</span><span class="sxs-lookup"><span data-stu-id="12602-119">Type: **int2**</span></span>

<span data-ttu-id="12602-120">Второй компонент смещения, применяемый к координатам текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="12602-120">The second offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="12602-121">*Offset3* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="12602-121">*Offset3* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12602-122">Тип: **int2**</span><span class="sxs-lookup"><span data-stu-id="12602-122">Type: **int2**</span></span>

<span data-ttu-id="12602-123">Третий компонент смещения, применяемый к координатам текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="12602-123">The third offset component applied to the texture coordinates before sampling.</span></span>

</dd> <dt>

<span data-ttu-id="12602-124">*Offset4* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="12602-124">*Offset4* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12602-125">Тип: **int2**</span><span class="sxs-lookup"><span data-stu-id="12602-125">Type: **int2**</span></span>

<span data-ttu-id="12602-126">Четвертый компонент смещения, применяемый к координатам текстуры перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="12602-126">The fourth offset component applied to the texture coordinates before sampling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12602-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="12602-127">Return value</span></span>

<span data-ttu-id="12602-128">Тип: **TemplateType**</span><span class="sxs-lookup"><span data-stu-id="12602-128">Type: **TemplateType**</span></span>

<span data-ttu-id="12602-129">Значение из четырех компонентов, тип которого совпадает с типом шаблона.</span><span class="sxs-lookup"><span data-stu-id="12602-129">A four-component value whose type is the same as the template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="12602-130">Примечания</span><span class="sxs-lookup"><span data-stu-id="12602-130">Remarks</span></span>

<span data-ttu-id="12602-131">Примеры текстур можно использовать для интерполяции билинейной.</span><span class="sxs-lookup"><span data-stu-id="12602-131">The texture samples can be used for bilinear interpolation.</span></span>

<span data-ttu-id="12602-132">Эта функция поддерживается для следующих типов шейдеров:</span><span class="sxs-lookup"><span data-stu-id="12602-132">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="12602-133">Вершина</span><span class="sxs-lookup"><span data-stu-id="12602-133">Vertex</span></span> | <span data-ttu-id="12602-134">Поверхности</span><span class="sxs-lookup"><span data-stu-id="12602-134">Hull</span></span> | <span data-ttu-id="12602-135">Домен</span><span class="sxs-lookup"><span data-stu-id="12602-135">Domain</span></span> | <span data-ttu-id="12602-136">Геометрия</span><span class="sxs-lookup"><span data-stu-id="12602-136">Geometry</span></span> | <span data-ttu-id="12602-137">Пиксель</span><span class="sxs-lookup"><span data-stu-id="12602-137">Pixel</span></span> | <span data-ttu-id="12602-138">Вычисления</span><span class="sxs-lookup"><span data-stu-id="12602-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="12602-139">x</span><span class="sxs-lookup"><span data-stu-id="12602-139">x</span></span>      | <span data-ttu-id="12602-140">x</span><span class="sxs-lookup"><span data-stu-id="12602-140">x</span></span>    | <span data-ttu-id="12602-141">x</span><span class="sxs-lookup"><span data-stu-id="12602-141">x</span></span>      | <span data-ttu-id="12602-142">x</span><span class="sxs-lookup"><span data-stu-id="12602-142">x</span></span>        | <span data-ttu-id="12602-143">x</span><span class="sxs-lookup"><span data-stu-id="12602-143">x</span></span>     | <span data-ttu-id="12602-144">x</span><span class="sxs-lookup"><span data-stu-id="12602-144">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="12602-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="12602-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12602-146">Методы Гасергрин</span><span class="sxs-lookup"><span data-stu-id="12602-146">GatherGreen methods</span></span>](texture2d-gathergreen.md)
</dt> </dl>

 

 




