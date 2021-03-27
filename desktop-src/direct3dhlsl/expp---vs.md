---
title: експп — VS
description: Обеспечивает частичную точность 2 экспоненциального представления.
ms.assetid: ac080ac9-5dfd-49e4-92ea-50bb26844ff6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0d57e2723c90eee8df728aa540baeab86932e773
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784941"
---
# <a name="expp---vs"></a><span data-ttu-id="cd7b3-103">експп — VS</span><span class="sxs-lookup"><span data-stu-id="cd7b3-103">expp - vs</span></span>

<span data-ttu-id="cd7b3-104">Предоставляет экспоненциальное 2<sup>x</sup>частичной точности.</span><span class="sxs-lookup"><span data-stu-id="cd7b3-104">Provides partial precision exponential 2<sup>x</sup>.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd7b3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd7b3-105">Syntax</span></span>



| <span data-ttu-id="cd7b3-106">експп DST, src. x</span><span class="sxs-lookup"><span data-stu-id="cd7b3-106">expp dst, src.{x\</span></span>|<span data-ttu-id="cd7b3-107">&</span><span class="sxs-lookup"><span data-stu-id="cd7b3-107">y\</span></span>|<span data-ttu-id="cd7b3-108">гармошкой</span><span class="sxs-lookup"><span data-stu-id="cd7b3-108">z\</span></span>|<span data-ttu-id="cd7b3-109">Белая</span><span class="sxs-lookup"><span data-stu-id="cd7b3-109">w}</span></span> |
|----------------------------|



 

<span data-ttu-id="cd7b3-110">Где:</span><span class="sxs-lookup"><span data-stu-id="cd7b3-110">Where:</span></span>

-   <span data-ttu-id="cd7b3-111">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="cd7b3-111">dst is the destination register.</span></span>
-   <span data-ttu-id="cd7b3-112">src является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="cd7b3-112">src is a source register.</span></span> <span data-ttu-id="cd7b3-113">Для исходного регистра требуется явное использование репликации свиззле, то есть только один из компонентов. x,. y,. z,. w свиззле (или. r,. g,. b,. a эквивалент) должен быть указан.</span><span class="sxs-lookup"><span data-stu-id="cd7b3-113">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>
-   <span data-ttu-id="cd7b3-114">{x \| y \| z \| w} — это обязательная репликация свиззле для исходного регистра.</span><span class="sxs-lookup"><span data-stu-id="cd7b3-114">{x\|y\|z\|w} is the required replicate swizzle on source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd7b3-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="cd7b3-115">Remarks</span></span>



| <span data-ttu-id="cd7b3-116">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="cd7b3-116">Vertex shader versions</span></span> | <span data-ttu-id="cd7b3-117">1\_1</span><span class="sxs-lookup"><span data-stu-id="cd7b3-117">1\_1</span></span> | <span data-ttu-id="cd7b3-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cd7b3-118">2\_0</span></span> | <span data-ttu-id="cd7b3-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="cd7b3-119">2\_x</span></span> | <span data-ttu-id="cd7b3-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="cd7b3-120">2\_sw</span></span> | <span data-ttu-id="cd7b3-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cd7b3-121">3\_0</span></span> | <span data-ttu-id="cd7b3-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="cd7b3-122">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="cd7b3-123">експп</span><span class="sxs-lookup"><span data-stu-id="cd7b3-123">expp</span></span>                   | <span data-ttu-id="cd7b3-124">x</span><span class="sxs-lookup"><span data-stu-id="cd7b3-124">x</span></span>    | <span data-ttu-id="cd7b3-125">x</span><span class="sxs-lookup"><span data-stu-id="cd7b3-125">x</span></span>    | <span data-ttu-id="cd7b3-126">x</span><span class="sxs-lookup"><span data-stu-id="cd7b3-126">x</span></span>    | <span data-ttu-id="cd7b3-127">x</span><span class="sxs-lookup"><span data-stu-id="cd7b3-127">x</span></span>     | <span data-ttu-id="cd7b3-128">x</span><span class="sxs-lookup"><span data-stu-id="cd7b3-128">x</span></span>    | <span data-ttu-id="cd7b3-129">x</span><span class="sxs-lookup"><span data-stu-id="cd7b3-129">x</span></span>     |



 

### <a name="vs_1_1"></a><span data-ttu-id="cd7b3-130">VS \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="cd7b3-130">vs\_1\_1</span></span>

<span data-ttu-id="cd7b3-131">Инструкция [exp-VS](exp---vs.md) работает по-разному в зависимости от версий шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="cd7b3-131">The [exp - vs](exp---vs.md) instruction operates differently depending on vertex shader versions.</span></span>

<span data-ttu-id="cd7b3-132">В VS \_ 1 \_ 1 Инструкция експп дает следующие результаты.</span><span class="sxs-lookup"><span data-stu-id="cd7b3-132">In vs\_1\_1, the expp instruction gives the following results:</span></span>


```
v = the scalar value from the source register with a replicate swizzle

dest.x = pow(2, floor(v))
dest.y = v - floor(v)
dest.z = pow(2, v) (partial-precision)
dest.w = 1
```



<span data-ttu-id="cd7b3-133">В VS \_ 2 \_ 0 и выше инструкция експп дает следующие результаты.</span><span class="sxs-lookup"><span data-stu-id="cd7b3-133">In vs\_2\_0 and up, the expp instruction gives the following results:</span></span>


```
v = the scalar value from the source register with a replicate swizzle

dest.x = dest.y = dest.z = dest.y = pow(2, v) (partial-precision)
```



### <a name="vs_2_0"></a><span data-ttu-id="cd7b3-134">VS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cd7b3-134">vs\_2\_0</span></span>

<span data-ttu-id="cd7b3-135">В VS \_ 2 \_ 0 и выше инструкция работает следующим образом:</span><span class="sxs-lookup"><span data-stu-id="cd7b3-135">In vs\_2\_0 and up, the instruction works like this:</span></span>


```
float V = the scalar value from the source register with a replicate swizzle

dest.x = dest.y = dest.z = dest.y = pow( 2, V ) (partial-precision)
```



<span data-ttu-id="cd7b3-136">Инструкция предоставляет не менее 10 разрядов точности.</span><span class="sxs-lookup"><span data-stu-id="cd7b3-136">The instruction provides at least 10 bits of precision.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cd7b3-137">См. также</span><span class="sxs-lookup"><span data-stu-id="cd7b3-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd7b3-138">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="cd7b3-138">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




