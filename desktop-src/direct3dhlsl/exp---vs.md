---
title: EXP — VS
description: Обеспечивает полную экспоненциальную точность 2. | EXP — VS
ms.assetid: 3644046b-3257-4257-9880-146ca50f6b0b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c5b49b69e1270075aef4368dedca5791c2784657
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998222"
---
# <a name="exp---vs"></a><span data-ttu-id="2469b-104">EXP — VS</span><span class="sxs-lookup"><span data-stu-id="2469b-104">exp - vs</span></span>

<span data-ttu-id="2469b-105">Обеспечивает полную экспоненциальную точность 2<sup>x</sup>.</span><span class="sxs-lookup"><span data-stu-id="2469b-105">Provides full precision exponential 2<sup>x</sup>.</span></span>

## <a name="syntax"></a><span data-ttu-id="2469b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2469b-106">Syntax</span></span>



| <span data-ttu-id="2469b-107">EXP DST, src</span><span class="sxs-lookup"><span data-stu-id="2469b-107">exp dst, src</span></span> |
|--------------|



 

<span data-ttu-id="2469b-108">где</span><span class="sxs-lookup"><span data-stu-id="2469b-108">where</span></span>

-   <span data-ttu-id="2469b-109">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="2469b-109">dst is the destination register.</span></span>
-   <span data-ttu-id="2469b-110">src является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="2469b-110">src is a source register.</span></span> <span data-ttu-id="2469b-111">Для исходного регистра требуется явное использование репликации свиззле, то есть только один из компонентов. x,. y,. z,. w свиззле (или. r,. g,. b,. a эквивалент) должен быть указан.</span><span class="sxs-lookup"><span data-stu-id="2469b-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span> <span data-ttu-id="2469b-112">См. раздел [Source Register группирующие](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md).</span><span class="sxs-lookup"><span data-stu-id="2469b-112">See [Source Register Swizzling](dx9-graphics-reference-asm-vs-registers-modifiers-source-swizzling.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2469b-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="2469b-113">Remarks</span></span>



| <span data-ttu-id="2469b-114">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="2469b-114">Vertex shader versions</span></span> | <span data-ttu-id="2469b-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="2469b-115">1\_1</span></span> | <span data-ttu-id="2469b-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2469b-116">2\_0</span></span> | <span data-ttu-id="2469b-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="2469b-117">2\_x</span></span> | <span data-ttu-id="2469b-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="2469b-118">2\_sw</span></span> | <span data-ttu-id="2469b-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2469b-119">3\_0</span></span> | <span data-ttu-id="2469b-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="2469b-120">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="2469b-121">exp</span><span class="sxs-lookup"><span data-stu-id="2469b-121">exp</span></span>                    | <span data-ttu-id="2469b-122">x</span><span class="sxs-lookup"><span data-stu-id="2469b-122">x</span></span>    | <span data-ttu-id="2469b-123">x</span><span class="sxs-lookup"><span data-stu-id="2469b-123">x</span></span>    | <span data-ttu-id="2469b-124">x</span><span class="sxs-lookup"><span data-stu-id="2469b-124">x</span></span>    | <span data-ttu-id="2469b-125">x</span><span class="sxs-lookup"><span data-stu-id="2469b-125">x</span></span>     | <span data-ttu-id="2469b-126">x</span><span class="sxs-lookup"><span data-stu-id="2469b-126">x</span></span>    | <span data-ttu-id="2469b-127">x</span><span class="sxs-lookup"><span data-stu-id="2469b-127">x</span></span>     |



 

<span data-ttu-id="2469b-128">Эта инструкция предоставляет по меньшей мере 21 бит точности.</span><span class="sxs-lookup"><span data-stu-id="2469b-128">This instruction provides at least 21 bits of precision.</span></span>

<span data-ttu-id="2469b-129">В следующем фрагменте кода показаны выполняемые операции.</span><span class="sxs-lookup"><span data-stu-id="2469b-129">The following code fragment shows the operations performed:</span></span>


```
dest.x = dest.y = dest.z = dest.w = (float)pow(2, src.replicateSwizzleComponent);
```



## <a name="related-topics"></a><span data-ttu-id="2469b-130">См. также</span><span class="sxs-lookup"><span data-stu-id="2469b-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2469b-131">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="2469b-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




