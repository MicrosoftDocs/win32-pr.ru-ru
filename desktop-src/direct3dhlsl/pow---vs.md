---
title: Pow — VS
description: Src1 с полной точностью ABS (src0). | Pow — VS
ms.assetid: 51da86c6-bafa-42e0-90a5-d1545e39e600
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3263fa19015bc32c94ae714891c3bbb2128c9463
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273438"
---
# <a name="pow---vs"></a><span data-ttu-id="8bc31-104">Pow — VS</span><span class="sxs-lookup"><span data-stu-id="8bc31-104">pow - vs</span></span>

<span data-ttu-id="8bc31-105"><sup>Src1</sup>с полной точностью ABS (src0).</span><span class="sxs-lookup"><span data-stu-id="8bc31-105">Full precision abs(src0)<sup>src1</sup>.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bc31-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8bc31-106">Syntax</span></span>



| <span data-ttu-id="8bc31-107">Pow DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="8bc31-107">pow dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="8bc31-108">где</span><span class="sxs-lookup"><span data-stu-id="8bc31-108">where</span></span>

-   <span data-ttu-id="8bc31-109">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="8bc31-109">dst is the destination register.</span></span>
-   <span data-ttu-id="8bc31-110">src0 является регистром входного источника.</span><span class="sxs-lookup"><span data-stu-id="8bc31-110">src0 is an input source register.</span></span> <span data-ttu-id="8bc31-111">Для исходного регистра требуется явное использование репликации свиззле, то есть только один из компонентов. x,. y,. z,. w свиззле (или. r,. g,. b,. a эквивалент) должен быть указан.</span><span class="sxs-lookup"><span data-stu-id="8bc31-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>
-   <span data-ttu-id="8bc31-112">src1 является регистром входного источника.</span><span class="sxs-lookup"><span data-stu-id="8bc31-112">src1 is an input source register.</span></span> <span data-ttu-id="8bc31-113">Для исходного регистра требуется явное использование репликации свиззле, то есть только один из компонентов. x,. y,. z,. w свиззле (или. r,. g,. b,. a эквивалент) должен быть указан.</span><span class="sxs-lookup"><span data-stu-id="8bc31-113">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="8bc31-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="8bc31-114">Remarks</span></span>



| <span data-ttu-id="8bc31-115">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="8bc31-115">Vertex shader versions</span></span> | <span data-ttu-id="8bc31-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="8bc31-116">1\_1</span></span> | <span data-ttu-id="8bc31-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8bc31-117">2\_0</span></span> | <span data-ttu-id="8bc31-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="8bc31-118">2\_x</span></span> | <span data-ttu-id="8bc31-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8bc31-119">2\_sw</span></span> | <span data-ttu-id="8bc31-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8bc31-120">3\_0</span></span> | <span data-ttu-id="8bc31-121">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8bc31-121">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="8bc31-122">pow</span><span class="sxs-lookup"><span data-stu-id="8bc31-122">pow</span></span>                    |      | <span data-ttu-id="8bc31-123">x</span><span class="sxs-lookup"><span data-stu-id="8bc31-123">x</span></span>    | <span data-ttu-id="8bc31-124">x</span><span class="sxs-lookup"><span data-stu-id="8bc31-124">x</span></span>    | <span data-ttu-id="8bc31-125">x</span><span class="sxs-lookup"><span data-stu-id="8bc31-125">x</span></span>     | <span data-ttu-id="8bc31-126">x</span><span class="sxs-lookup"><span data-stu-id="8bc31-126">x</span></span>    | <span data-ttu-id="8bc31-127">x</span><span class="sxs-lookup"><span data-stu-id="8bc31-127">x</span></span>     |



 

<span data-ttu-id="8bc31-128">Эта инструкция работает, как показано здесь.</span><span class="sxs-lookup"><span data-stu-id="8bc31-128">This instruction works as shown here.</span></span>


```
dest = pow(abs(src0), src1);
```



<span data-ttu-id="8bc31-129">Это скалярная инструкция, поэтому исходные регистры должны иметь репликацию свиззлес, чтобы указать, какие каналы используются.</span><span class="sxs-lookup"><span data-stu-id="8bc31-129">This is a scalar instruction, therefore the source registers should have replicate swizzles to indicate which channels are used.</span></span>

<span data-ttu-id="8bc31-130">Скалярный результат реплицируется во все четыре выходных канала.</span><span class="sxs-lookup"><span data-stu-id="8bc31-130">The scalar result is replicated to all four output channels.</span></span>

<span data-ttu-id="8bc31-131">Эту инструкцию можно расширить как exp ( \* Журнал src1 (src0)).</span><span class="sxs-lookup"><span data-stu-id="8bc31-131">This instruction could be expanded as exp(src1 \* log(src0)).</span></span>

<span data-ttu-id="8bc31-132">Точность не меньше 15 бит.</span><span class="sxs-lookup"><span data-stu-id="8bc31-132">Precision is not lower than 15 bits.</span></span>

<span data-ttu-id="8bc31-133">Регистр приемника должен быть временным регистром и не должен совпадать с src1.</span><span class="sxs-lookup"><span data-stu-id="8bc31-133">The dest register should be a temporary register, and should not be the same register as src1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8bc31-134">См. также</span><span class="sxs-lookup"><span data-stu-id="8bc31-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8bc31-135">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="8bc31-135">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




