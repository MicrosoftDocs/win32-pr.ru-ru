---
title: EXP-PS
description: Обеспечивает полную экспоненциальную точность 2. | EXP-PS
ms.assetid: 09e4446f-4149-4ec8-b3e3-2045b55bd591
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: acd7c50c1f0d6ff08ee5d66e50fdd3e56939f0d9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104081764"
---
# <a name="exp---ps"></a><span data-ttu-id="ef0ff-104">EXP-PS</span><span class="sxs-lookup"><span data-stu-id="ef0ff-104">exp - ps</span></span>

<span data-ttu-id="ef0ff-105">Обеспечивает полную экспоненциальную точность 2<sup>x</sup>.</span><span class="sxs-lookup"><span data-stu-id="ef0ff-105">Provides full precision exponential 2<sup>x</sup>.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef0ff-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ef0ff-106">Syntax</span></span>



| <span data-ttu-id="ef0ff-107">EXP DST, src</span><span class="sxs-lookup"><span data-stu-id="ef0ff-107">exp dst, src</span></span> |
|--------------|



 

<span data-ttu-id="ef0ff-108">где</span><span class="sxs-lookup"><span data-stu-id="ef0ff-108">where</span></span>

-   <span data-ttu-id="ef0ff-109">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="ef0ff-109">dst is the destination register.</span></span>
-   <span data-ttu-id="ef0ff-110">src является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="ef0ff-110">src is a source register.</span></span> <span data-ttu-id="ef0ff-111">Регистр исходного кода требует явного использования репликации свиззле; то есть необходимо указать только один из компонентов. x,. y,. z,. w свиззле (или. r,. g,. b,. a эквивалент).</span><span class="sxs-lookup"><span data-stu-id="ef0ff-111">Source register requires explicit use of replicate swizzle; that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span> <span data-ttu-id="ef0ff-112">См. раздел [Source Register группирующие](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).</span><span class="sxs-lookup"><span data-stu-id="ef0ff-112">See [Source Register Swizzling](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ef0ff-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="ef0ff-113">Remarks</span></span>



| <span data-ttu-id="ef0ff-114">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="ef0ff-114">Pixel shader versions</span></span> | <span data-ttu-id="ef0ff-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="ef0ff-115">1\_1</span></span> | <span data-ttu-id="ef0ff-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="ef0ff-116">1\_2</span></span> | <span data-ttu-id="ef0ff-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="ef0ff-117">1\_3</span></span> | <span data-ttu-id="ef0ff-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="ef0ff-118">1\_4</span></span> | <span data-ttu-id="ef0ff-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ef0ff-119">2\_0</span></span> | <span data-ttu-id="ef0ff-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="ef0ff-120">2\_x</span></span> | <span data-ttu-id="ef0ff-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="ef0ff-121">2\_sw</span></span> | <span data-ttu-id="ef0ff-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ef0ff-122">3\_0</span></span> | <span data-ttu-id="ef0ff-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="ef0ff-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="ef0ff-124">exp</span><span class="sxs-lookup"><span data-stu-id="ef0ff-124">exp</span></span>                   |      |      |      |      | <span data-ttu-id="ef0ff-125">x</span><span class="sxs-lookup"><span data-stu-id="ef0ff-125">x</span></span>    | <span data-ttu-id="ef0ff-126">x</span><span class="sxs-lookup"><span data-stu-id="ef0ff-126">x</span></span>    | <span data-ttu-id="ef0ff-127">x</span><span class="sxs-lookup"><span data-stu-id="ef0ff-127">x</span></span>     | <span data-ttu-id="ef0ff-128">x</span><span class="sxs-lookup"><span data-stu-id="ef0ff-128">x</span></span>    | <span data-ttu-id="ef0ff-129">x</span><span class="sxs-lookup"><span data-stu-id="ef0ff-129">x</span></span>     |



 

<span data-ttu-id="ef0ff-130">В следующем фрагменте кода показаны выполняемые операции.</span><span class="sxs-lookup"><span data-stu-id="ef0ff-130">The following code snippet shows the operations performed:</span></span>


```
dest.x = dest.y = dest.z = dest.w = (float)pow(2, src.replicateSwizzleComponent);
```



## <a name="related-topics"></a><span data-ttu-id="ef0ff-131">См. также</span><span class="sxs-lookup"><span data-stu-id="ef0ff-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef0ff-132">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="ef0ff-132">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




