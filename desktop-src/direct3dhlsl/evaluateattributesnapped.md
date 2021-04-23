---
title: Функция Евалуатеаттрибутеснаппед
description: Вычисляет на пиксельном центроид со смещением.
ms.assetid: f5085016-0e94-49bb-96b6-42fa15c30b9f
keywords:
- Функция Евалуатеаттрибутеснаппед HLSL
topic_type:
- apiref
api_name:
- EvaluateAttributeSnapped
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 70a9389ed9e9f4fff16f82610cb611bc4da2c7a3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104996815"
---
# <a name="evaluateattributesnapped-function"></a><span data-ttu-id="e58e5-104">Функция Евалуатеаттрибутеснаппед</span><span class="sxs-lookup"><span data-stu-id="e58e5-104">EvaluateAttributeSnapped function</span></span>

<span data-ttu-id="e58e5-105">Вычисляет на пиксельном центроид со смещением.</span><span class="sxs-lookup"><span data-stu-id="e58e5-105">Evaluates at the pixel centroid with an offset.</span></span>

## <a name="syntax"></a><span data-ttu-id="e58e5-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e58e5-106">Syntax</span></span>

``` syntax
numeric EvaluateAttributeSnapped(
  in attrib numeric value,
  in 
            int2 offset
);
```

## <a name="parameters"></a><span data-ttu-id="e58e5-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e58e5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e58e5-108">*значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e58e5-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e58e5-109">Тип: **attrib numeric**</span><span class="sxs-lookup"><span data-stu-id="e58e5-109">Type: **attrib numeric**</span></span>

<span data-ttu-id="e58e5-110">Входное значение.</span><span class="sxs-lookup"><span data-stu-id="e58e5-110">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="e58e5-111">*смещение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e58e5-111">*offset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e58e5-112">Тип: **int2**</span><span class="sxs-lookup"><span data-stu-id="e58e5-112">Type: **int2**</span></span>

<span data-ttu-id="e58e5-113">2D-смещение от центра пикселей с помощью сетки 16x16.</span><span class="sxs-lookup"><span data-stu-id="e58e5-113">A 2D offset from the pixel center using a 16x16 grid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e58e5-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="e58e5-114">Remarks</span></span>

<span data-ttu-id="e58e5-115">Диапазон для параметра *offset* должен быть определен с помощью следующего байтового кода.</span><span class="sxs-lookup"><span data-stu-id="e58e5-115">The range for the *offset* parameter must be defined by the following byte code.</span></span>

<span data-ttu-id="e58e5-116">Используются только наименее значащие 4 бита первых двух компонентов (U, V) смещения пикселей.</span><span class="sxs-lookup"><span data-stu-id="e58e5-116">Only the least significant 4 bits of the first two components (U, V) of the pixel offset are used.</span></span> <span data-ttu-id="e58e5-117">Преобразование из 4-разрядной фиксированной точки в float имеет следующий вид (сверху вниз... ЛСБ), где символ конца является частью дроби и определяет знак:</span><span class="sxs-lookup"><span data-stu-id="e58e5-117">The conversion from the 4-bit fixed point to float is as follows (MSB...LSB), where the MSB is both a part of the fraction and determines the sign:</span></span>

-   <span data-ttu-id="e58e5-118">1000 =-0,5 f (-8/16)</span><span class="sxs-lookup"><span data-stu-id="e58e5-118">1000 = -0.5f (-8 / 16)</span></span>
-   <span data-ttu-id="e58e5-119">1001 =-0.4375 f (-7/16)</span><span class="sxs-lookup"><span data-stu-id="e58e5-119">1001 = -0.4375f (-7 / 16)</span></span>
-   <span data-ttu-id="e58e5-120">1010 =-0.375 f (-6/16)</span><span class="sxs-lookup"><span data-stu-id="e58e5-120">1010 = -0.375f (-6 / 16)</span></span>
-   <span data-ttu-id="e58e5-121">1011 =-0.3125 f (-5/16)</span><span class="sxs-lookup"><span data-stu-id="e58e5-121">1011 = -0.3125f (-5 / 16)</span></span>
-   <span data-ttu-id="e58e5-122">1100 =-0,25 f (-4/16)</span><span class="sxs-lookup"><span data-stu-id="e58e5-122">1100 = -0.25f (-4 / 16)</span></span>
-   <span data-ttu-id="e58e5-123">1101 =-0.1875 f (-3/16)</span><span class="sxs-lookup"><span data-stu-id="e58e5-123">1101 = -0.1875f (-3 / 16)</span></span>
-   <span data-ttu-id="e58e5-124">1110 =-0,125 f (-2/16)</span><span class="sxs-lookup"><span data-stu-id="e58e5-124">1110 = -0.125f (-2 / 16)</span></span>
-   <span data-ttu-id="e58e5-125">1111 =-0.0625 f (-1/16)</span><span class="sxs-lookup"><span data-stu-id="e58e5-125">1111 = -0.0625f (-1 / 16)</span></span>
-   <span data-ttu-id="e58e5-126">0000 = 0.0 f (0/16)</span><span class="sxs-lookup"><span data-stu-id="e58e5-126">0000 = 0.0f ( 0 / 16)</span></span>
-   <span data-ttu-id="e58e5-127">0001 = 0.0625 f (1/16)</span><span class="sxs-lookup"><span data-stu-id="e58e5-127">0001 = 0.0625f ( 1 / 16)</span></span>
-   <span data-ttu-id="e58e5-128">0010 = 0,125 f (2/16)</span><span class="sxs-lookup"><span data-stu-id="e58e5-128">0010 = 0.125f ( 2 / 16)</span></span>
-   <span data-ttu-id="e58e5-129">0011 = 0.1875 f (3/16)</span><span class="sxs-lookup"><span data-stu-id="e58e5-129">0011 = 0.1875f ( 3 / 16)</span></span>
-   <span data-ttu-id="e58e5-130">0100 = 0,25 f (4/16)</span><span class="sxs-lookup"><span data-stu-id="e58e5-130">0100 = 0.25f ( 4 / 16)</span></span>
-   <span data-ttu-id="e58e5-131">0101 = 0.3125 f (5/16)</span><span class="sxs-lookup"><span data-stu-id="e58e5-131">0101 = 0.3125f ( 5 / 16)</span></span>
-   <span data-ttu-id="e58e5-132">0110 = 0.375 f (6/16)</span><span class="sxs-lookup"><span data-stu-id="e58e5-132">0110 = 0.375f ( 6 / 16)</span></span>
-   <span data-ttu-id="e58e5-133">0111 = 0.4375 f (7/16)</span><span class="sxs-lookup"><span data-stu-id="e58e5-133">0111 = 0.4375f ( 7 / 16)</span></span>

> [!Note]  
> <span data-ttu-id="e58e5-134">Левый и верхний края пикселя включаются в смещение; Однако нижний и правый края не включаются.</span><span class="sxs-lookup"><span data-stu-id="e58e5-134">The left and top edges of a pixel are included in the offset; however, the bottom and right edges are not included.</span></span> <span data-ttu-id="e58e5-135">Все остальные биты в 32-разрядном целом значении и смещении в V не учитываются.</span><span class="sxs-lookup"><span data-stu-id="e58e5-135">All other bits in the 32-bit integer U and V offset values are ignored.</span></span>

 

<span data-ttu-id="e58e5-136">Реализация может принимать смещение, предоставленное шейдером, и получать полное 32-разрядное значение с фиксированной точкой (28,4), которое охватывает допустимый диапазон, выполняя следующее вычисление:</span><span class="sxs-lookup"><span data-stu-id="e58e5-136">An implementation can take the offset provided by the shader and obtain a full 32-bit fixed point value (28.4), which spans the valid range, by performing the following calculation:</span></span>


```
iU = (iU<<28)>>28  // keep lowest 4 bits and sign extend, which yields [-8..7]
```



<span data-ttu-id="e58e5-137">Если реализация должна сопоставлять смещение с смещением с плавающей запятой, выполняется следующее вычисление:</span><span class="sxs-lookup"><span data-stu-id="e58e5-137">If an implementation must map the offset to a floating-point offset, it performs the following calculation:</span></span>


```
fU = ((float)iU)/16
```



### <a name="minimum-shader-model"></a><span data-ttu-id="e58e5-138">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="e58e5-138">Minimum Shader Model</span></span>

<span data-ttu-id="e58e5-139">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="e58e5-139">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e58e5-140">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="e58e5-140">Shader Model</span></span>                                                                | <span data-ttu-id="e58e5-141">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="e58e5-141">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="e58e5-142">[Модели шейдера 5](d3d11-graphics-reference-sm5.md) и более поздних моделей шейдеров</span><span class="sxs-lookup"><span data-stu-id="e58e5-142">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="e58e5-143">да</span><span class="sxs-lookup"><span data-stu-id="e58e5-143">yes</span></span>       |



 

<span data-ttu-id="e58e5-144">Эта функция поддерживается в следующих типах шейдеров:</span><span class="sxs-lookup"><span data-stu-id="e58e5-144">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="e58e5-145">Вершина</span><span class="sxs-lookup"><span data-stu-id="e58e5-145">Vertex</span></span> | <span data-ttu-id="e58e5-146">Поверхности</span><span class="sxs-lookup"><span data-stu-id="e58e5-146">Hull</span></span> | <span data-ttu-id="e58e5-147">Домен</span><span class="sxs-lookup"><span data-stu-id="e58e5-147">Domain</span></span> | <span data-ttu-id="e58e5-148">Геометрия</span><span class="sxs-lookup"><span data-stu-id="e58e5-148">Geometry</span></span> | <span data-ttu-id="e58e5-149">Пиксель</span><span class="sxs-lookup"><span data-stu-id="e58e5-149">Pixel</span></span> | <span data-ttu-id="e58e5-150">Вычисления</span><span class="sxs-lookup"><span data-stu-id="e58e5-150">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="e58e5-151">x</span><span class="sxs-lookup"><span data-stu-id="e58e5-151">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="e58e5-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e58e5-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e58e5-153">Встроенные функции</span><span class="sxs-lookup"><span data-stu-id="e58e5-153">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="e58e5-154">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="e58e5-154">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




