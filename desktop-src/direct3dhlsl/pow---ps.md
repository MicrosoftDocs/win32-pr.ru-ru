---
title: Pow-PS
description: Src1 с полной точностью ABS (src0). | Pow-PS
ms.assetid: 39037c51-a524-459c-8422-bd7831e2aa3d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 84be39ca8f2633482165d76eabfe0f5d0bb22161
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986296"
---
# <a name="pow---ps"></a><span data-ttu-id="2a99a-104">Pow-PS</span><span class="sxs-lookup"><span data-stu-id="2a99a-104">pow - ps</span></span>

<span data-ttu-id="2a99a-105"><sup>Src1</sup>с полной точностью ABS (src0).</span><span class="sxs-lookup"><span data-stu-id="2a99a-105">Full precision abs(src0)<sup>src1</sup>.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a99a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2a99a-106">Syntax</span></span>



| <span data-ttu-id="2a99a-107">Pow DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="2a99a-107">pow dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="2a99a-108">где</span><span class="sxs-lookup"><span data-stu-id="2a99a-108">where</span></span>

-   <span data-ttu-id="2a99a-109">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="2a99a-109">dst is the destination register.</span></span>
-   <span data-ttu-id="2a99a-110">src0 является регистром входного источника.</span><span class="sxs-lookup"><span data-stu-id="2a99a-110">src0 is an input source register.</span></span> <span data-ttu-id="2a99a-111">Для исходного регистра требуется явное использование репликации свиззле, то есть только один из компонентов. x,. y,. z,. w свиззле (или. r,. g,. b,. a эквивалент) должен быть указан.</span><span class="sxs-lookup"><span data-stu-id="2a99a-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>
-   <span data-ttu-id="2a99a-112">src1 является регистром входного источника.</span><span class="sxs-lookup"><span data-stu-id="2a99a-112">src1 is an input source register.</span></span> <span data-ttu-id="2a99a-113">Для исходного регистра требуется явное использование репликации свиззле, то есть только один из компонентов. x,. y,. z,. w свиззле (или. r,. g,. b,. a эквивалент) должен быть указан.</span><span class="sxs-lookup"><span data-stu-id="2a99a-113">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a99a-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="2a99a-114">Remarks</span></span>



| <span data-ttu-id="2a99a-115">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="2a99a-115">Pixel shader versions</span></span> | <span data-ttu-id="2a99a-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="2a99a-116">1\_1</span></span> | <span data-ttu-id="2a99a-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="2a99a-117">1\_2</span></span> | <span data-ttu-id="2a99a-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="2a99a-118">1\_3</span></span> | <span data-ttu-id="2a99a-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="2a99a-119">1\_4</span></span> | <span data-ttu-id="2a99a-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2a99a-120">2\_0</span></span> | <span data-ttu-id="2a99a-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="2a99a-121">2\_x</span></span> | <span data-ttu-id="2a99a-122">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="2a99a-122">2\_sw</span></span> | <span data-ttu-id="2a99a-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2a99a-123">3\_0</span></span> | <span data-ttu-id="2a99a-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="2a99a-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="2a99a-125">pow</span><span class="sxs-lookup"><span data-stu-id="2a99a-125">pow</span></span>                   |      |      |      |      | <span data-ttu-id="2a99a-126">x</span><span class="sxs-lookup"><span data-stu-id="2a99a-126">x</span></span>    | <span data-ttu-id="2a99a-127">x</span><span class="sxs-lookup"><span data-stu-id="2a99a-127">x</span></span>    | <span data-ttu-id="2a99a-128">x</span><span class="sxs-lookup"><span data-stu-id="2a99a-128">x</span></span>     | <span data-ttu-id="2a99a-129">x</span><span class="sxs-lookup"><span data-stu-id="2a99a-129">x</span></span>    | <span data-ttu-id="2a99a-130">x</span><span class="sxs-lookup"><span data-stu-id="2a99a-130">x</span></span>     |



 

<span data-ttu-id="2a99a-131">Эта инструкция работает следующим образом:</span><span class="sxs-lookup"><span data-stu-id="2a99a-131">This instruction works as follows:</span></span>

<span data-ttu-id="2a99a-132">dest. x = dest. y = dest. z = dest. w = \[ ABS (src0) \] <sup>src1</sup>;</span><span class="sxs-lookup"><span data-stu-id="2a99a-132">dest.x = dest.y = dest.z = dest.w = \[abs(src0)\]<sup>src1</sup>;</span></span>

<span data-ttu-id="2a99a-133">Это скалярная инструкция, поэтому исходные регистры должны иметь репликацию свиззлес, чтобы указать, какие каналы используются.</span><span class="sxs-lookup"><span data-stu-id="2a99a-133">This is a scalar instruction, therefore the source registers should have replicate swizzles to indicate which channels are used.</span></span>

<span data-ttu-id="2a99a-134">Входная мощность (src1) должна быть скалярной.</span><span class="sxs-lookup"><span data-stu-id="2a99a-134">The input power (src1) must be a scalar.</span></span>

<span data-ttu-id="2a99a-135">Скалярный результат реплицируется во все четыре выходных канала.</span><span class="sxs-lookup"><span data-stu-id="2a99a-135">The scalar result is replicated to all four output channels.</span></span>

<span data-ttu-id="2a99a-136">Эту инструкцию можно расширить как exp ( \* Журнал src1 (src0)).</span><span class="sxs-lookup"><span data-stu-id="2a99a-136">This instruction could be expanded as exp(src1 \* log(src0)).</span></span>

<span data-ttu-id="2a99a-137">Регистр летнего времени должен быть временным регистром и не должен совпадать с src1.</span><span class="sxs-lookup"><span data-stu-id="2a99a-137">The dst register should be a temporary register, and should not be the same register as src1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a99a-138">См. также</span><span class="sxs-lookup"><span data-stu-id="2a99a-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a99a-139">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="2a99a-139">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




