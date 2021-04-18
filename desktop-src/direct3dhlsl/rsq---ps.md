---
title: РСК-PS
description: Вычисляет значение корня обратного квадрата (только положительный) исходного скаляра. | РСК-PS
ms.assetid: deb1bd12-6347-4b1e-b21b-f3ef48da4c13
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 13777810c67ba38b2c8f47f0c0db0cf9b70771ad
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986436"
---
# <a name="rsq---ps"></a><span data-ttu-id="ef33b-104">РСК-PS</span><span class="sxs-lookup"><span data-stu-id="ef33b-104">rsq - ps</span></span>

<span data-ttu-id="ef33b-105">Вычисляет значение корня обратного квадрата (только положительный) исходного скаляра.</span><span class="sxs-lookup"><span data-stu-id="ef33b-105">Computes the reciprocal square root (positive only) of the source scalar.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef33b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ef33b-106">Syntax</span></span>



| <span data-ttu-id="ef33b-107">РСК DST, src</span><span class="sxs-lookup"><span data-stu-id="ef33b-107">rsq dst, src</span></span> |
|--------------|



 

<span data-ttu-id="ef33b-108">где</span><span class="sxs-lookup"><span data-stu-id="ef33b-108">where</span></span>

-   <span data-ttu-id="ef33b-109">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="ef33b-109">dst is the destination register.</span></span>
-   <span data-ttu-id="ef33b-110">src является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="ef33b-110">src is a source register.</span></span> <span data-ttu-id="ef33b-111">Для исходного регистра требуется явное использование репликации свиззле, то есть только один из компонентов. x,. y,. z,. w свиззле (или. r,. g,. b,. a эквивалент) должен быть указан.</span><span class="sxs-lookup"><span data-stu-id="ef33b-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef33b-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="ef33b-112">Remarks</span></span>



| <span data-ttu-id="ef33b-113">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="ef33b-113">Pixel shader versions</span></span> | <span data-ttu-id="ef33b-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="ef33b-114">1\_1</span></span> | <span data-ttu-id="ef33b-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="ef33b-115">1\_2</span></span> | <span data-ttu-id="ef33b-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="ef33b-116">1\_3</span></span> | <span data-ttu-id="ef33b-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="ef33b-117">1\_4</span></span> | <span data-ttu-id="ef33b-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ef33b-118">2\_0</span></span> | <span data-ttu-id="ef33b-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="ef33b-119">2\_x</span></span> | <span data-ttu-id="ef33b-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="ef33b-120">2\_sw</span></span> | <span data-ttu-id="ef33b-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ef33b-121">3\_0</span></span> | <span data-ttu-id="ef33b-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="ef33b-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="ef33b-123">рск</span><span class="sxs-lookup"><span data-stu-id="ef33b-123">rsq</span></span>                   |      |      |      |      | <span data-ttu-id="ef33b-124">x</span><span class="sxs-lookup"><span data-stu-id="ef33b-124">x</span></span>    | <span data-ttu-id="ef33b-125">x</span><span class="sxs-lookup"><span data-stu-id="ef33b-125">x</span></span>    | <span data-ttu-id="ef33b-126">x</span><span class="sxs-lookup"><span data-stu-id="ef33b-126">x</span></span>     | <span data-ttu-id="ef33b-127">x</span><span class="sxs-lookup"><span data-stu-id="ef33b-127">x</span></span>    | <span data-ttu-id="ef33b-128">x</span><span class="sxs-lookup"><span data-stu-id="ef33b-128">x</span></span>     |



 

<span data-ttu-id="ef33b-129">Абсолютное значение берется перед обработкой.</span><span class="sxs-lookup"><span data-stu-id="ef33b-129">The absolute value is taken before processing.</span></span>

<span data-ttu-id="ef33b-130">Точность должна составлять по крайней мере 1,0/(2 ²) абсолютную ошибку в диапазоне (1,0, 4,0), так как распространенные реализации будут разделять мантисса и экспоненту.</span><span class="sxs-lookup"><span data-stu-id="ef33b-130">Precision should be at least 1.0/(2²²) absolute error over the range (1.0, 4.0) because common implementations will separate mantissa and exponent.</span></span>

<span data-ttu-id="ef33b-131">Если входные данные представляют собой ровно 1,0, выходные данные должны быть ровно 1,0.</span><span class="sxs-lookup"><span data-stu-id="ef33b-131">The output must be exactly 1.0 if the input is exactly 1.0.</span></span> <span data-ttu-id="ef33b-132">Источник 0,0 дает бесконечное значение.</span><span class="sxs-lookup"><span data-stu-id="ef33b-132">A source of 0.0 yields infinity.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef33b-133">См. также</span><span class="sxs-lookup"><span data-stu-id="ef33b-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef33b-134">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="ef33b-134">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




