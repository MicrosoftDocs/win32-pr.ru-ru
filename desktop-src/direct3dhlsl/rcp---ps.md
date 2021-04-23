---
title: rcp-PS
description: Выполняет вычисление обратной стороны исходного скаляра. | rcp-PS
ms.assetid: d8dfc2b3-4404-47ec-aeaf-1adb7e7a342e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2df8ad2d673d96dced84630b1a641c7e4f27ceb2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986525"
---
# <a name="rcp---ps"></a><span data-ttu-id="b09e4-104">rcp-PS</span><span class="sxs-lookup"><span data-stu-id="b09e4-104">rcp - ps</span></span>

<span data-ttu-id="b09e4-105">Выполняет вычисление обратной стороны исходного скаляра.</span><span class="sxs-lookup"><span data-stu-id="b09e4-105">Computes the reciprocal of the source scalar.</span></span>

## <a name="syntax"></a><span data-ttu-id="b09e4-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b09e4-106">Syntax</span></span>



| <span data-ttu-id="b09e4-107">rcp DST, src</span><span class="sxs-lookup"><span data-stu-id="b09e4-107">rcp dst, src</span></span> |
|--------------|



 

<span data-ttu-id="b09e4-108">где</span><span class="sxs-lookup"><span data-stu-id="b09e4-108">where</span></span>

-   <span data-ttu-id="b09e4-109">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="b09e4-109">dst is the destination register.</span></span>
-   <span data-ttu-id="b09e4-110">src является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="b09e4-110">src is a source register.</span></span> <span data-ttu-id="b09e4-111">Для исходного регистра требуется явное использование репликации свиззле, то есть только один из компонентов. x,. y,. z,. w свиззле (или. r,. g,. b,. a эквивалент) должен быть указан.</span><span class="sxs-lookup"><span data-stu-id="b09e4-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="b09e4-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="b09e4-112">Remarks</span></span>



| <span data-ttu-id="b09e4-113">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="b09e4-113">Pixel shader versions</span></span> | <span data-ttu-id="b09e4-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="b09e4-114">1\_1</span></span> | <span data-ttu-id="b09e4-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="b09e4-115">1\_2</span></span> | <span data-ttu-id="b09e4-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="b09e4-116">1\_3</span></span> | <span data-ttu-id="b09e4-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="b09e4-117">1\_4</span></span> | <span data-ttu-id="b09e4-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b09e4-118">2\_0</span></span> | <span data-ttu-id="b09e4-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b09e4-119">2\_x</span></span> | <span data-ttu-id="b09e4-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b09e4-120">2\_sw</span></span> | <span data-ttu-id="b09e4-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b09e4-121">3\_0</span></span> | <span data-ttu-id="b09e4-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b09e4-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="b09e4-123">rcp</span><span class="sxs-lookup"><span data-stu-id="b09e4-123">rcp</span></span>                   |      |      |      |      | <span data-ttu-id="b09e4-124">x</span><span class="sxs-lookup"><span data-stu-id="b09e4-124">x</span></span>    | <span data-ttu-id="b09e4-125">x</span><span class="sxs-lookup"><span data-stu-id="b09e4-125">x</span></span>    | <span data-ttu-id="b09e4-126">x</span><span class="sxs-lookup"><span data-stu-id="b09e4-126">x</span></span>     | <span data-ttu-id="b09e4-127">x</span><span class="sxs-lookup"><span data-stu-id="b09e4-127">x</span></span>    | <span data-ttu-id="b09e4-128">x</span><span class="sxs-lookup"><span data-stu-id="b09e4-128">x</span></span>     |



 

<span data-ttu-id="b09e4-129">Если входные данные представляют собой ровно 1,0, выходные данные должны быть ровно 1,0.</span><span class="sxs-lookup"><span data-stu-id="b09e4-129">The output must be exactly 1.0 if the input is exactly 1.0.</span></span> <span data-ttu-id="b09e4-130">Источник 0,0 дает бесконечное значение.</span><span class="sxs-lookup"><span data-stu-id="b09e4-130">A source of 0.0 yields infinity.</span></span>

<span data-ttu-id="b09e4-131">Скалярный результат реплицируется на все каналы в конечной маске записи.</span><span class="sxs-lookup"><span data-stu-id="b09e4-131">The scalar result is replicated to all channels in the destination write mask.</span></span>

<span data-ttu-id="b09e4-132">Точность должна составлять по крайней мере 1,0/(2 ²) абсолютную ошибку в диапазоне (1,0, 2,0), так как распространенные реализации будут разделять мантисса и экспоненту.</span><span class="sxs-lookup"><span data-stu-id="b09e4-132">Precision should be at least 1.0/(2²²) absolute error over the range (1.0, 2.0) because common implementations will separate mantissa and exponent.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b09e4-133">См. также</span><span class="sxs-lookup"><span data-stu-id="b09e4-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b09e4-134">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="b09e4-134">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




