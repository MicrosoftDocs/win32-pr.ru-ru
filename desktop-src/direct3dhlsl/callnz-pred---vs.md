---
title: каллнз, пред. VS
description: Вызывайте, если не равен нулю, с предикатом. Выполняет условный вызов инструкции, помеченной индексом метки. Затенения использует логическое значение, чтобы определить, не нужно ли выполнять инструкцию.
ms.assetid: 3417f3e3-7e73-4131-8069-09c0de1469a7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e3c3de590dfee56013c76402c840a959e8f9306c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104069344"
---
# <a name="callnz-pred---vs"></a><span data-ttu-id="d36a3-105">каллнз, пред. VS</span><span class="sxs-lookup"><span data-stu-id="d36a3-105">callnz pred - vs</span></span>

<span data-ttu-id="d36a3-106">Вызывайте, если не равен нулю, с предикатом.</span><span class="sxs-lookup"><span data-stu-id="d36a3-106">Call if not zero, with a predicate.</span></span> <span data-ttu-id="d36a3-107">Выполняет условный вызов инструкции, помеченной индексом метки.</span><span class="sxs-lookup"><span data-stu-id="d36a3-107">Performs a conditional call to the instruction marked by the label index.</span></span> <span data-ttu-id="d36a3-108">Затенения использует логическое значение, чтобы определить, не нужно ли выполнять инструкцию.</span><span class="sxs-lookup"><span data-stu-id="d36a3-108">Predication uses a boolean value to determine whether of not to perform the instruction.</span></span>

## <a name="syntax"></a><span data-ttu-id="d36a3-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d36a3-109">Syntax</span></span>



| <span data-ttu-id="d36a3-110">каллнз l \# , \[ ! \] P0. x</span><span class="sxs-lookup"><span data-stu-id="d36a3-110">callnz l\#, \[!\]p0.{x\</span></span>|<span data-ttu-id="d36a3-111">&</span><span class="sxs-lookup"><span data-stu-id="d36a3-111">y\</span></span>|<span data-ttu-id="d36a3-112">гармошкой</span><span class="sxs-lookup"><span data-stu-id="d36a3-112">z\</span></span>|<span data-ttu-id="d36a3-113">Белая</span><span class="sxs-lookup"><span data-stu-id="d36a3-113">w}</span></span> |
|----------------------------------|



 

<span data-ttu-id="d36a3-114">где:</span><span class="sxs-lookup"><span data-stu-id="d36a3-114">where:</span></span>

-   <span data-ttu-id="d36a3-115">l \# — это [Метка — VS](label---vs.md) , помечающая начало подпрограммы для вызова.</span><span class="sxs-lookup"><span data-stu-id="d36a3-115">l\# is a [label - vs](label---vs.md) marking the beginning of the subroutine to be called.</span></span>
-   <span data-ttu-id="d36a3-116">\[!\] является необязательным модификатором отрицания.</span><span class="sxs-lookup"><span data-stu-id="d36a3-116">\[!\] is an optional negate modifier.</span></span>
-   <span data-ttu-id="d36a3-117">P0 — это [регистр предикатов](dx9-graphics-reference-asm-vs-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="d36a3-117">p0 is the [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md).</span></span>
-   <span data-ttu-id="d36a3-118">{x \| y \| z \| w} — это обязательная репликация свиззле в P0.</span><span class="sxs-lookup"><span data-stu-id="d36a3-118">{x\|y\|z\|w} is the required replicate swizzle on p0.</span></span>

## <a name="remarks"></a><span data-ttu-id="d36a3-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="d36a3-119">Remarks</span></span>



| <span data-ttu-id="d36a3-120">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="d36a3-120">Vertex shader versions</span></span> | <span data-ttu-id="d36a3-121">1\_1</span><span class="sxs-lookup"><span data-stu-id="d36a3-121">1\_1</span></span> | <span data-ttu-id="d36a3-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d36a3-122">2\_0</span></span> | <span data-ttu-id="d36a3-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="d36a3-123">2\_x</span></span> | <span data-ttu-id="d36a3-124">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="d36a3-124">2\_sw</span></span> | <span data-ttu-id="d36a3-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d36a3-125">3\_0</span></span> | <span data-ttu-id="d36a3-126">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="d36a3-126">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="d36a3-127">каллнз, пред.</span><span class="sxs-lookup"><span data-stu-id="d36a3-127">callnz pred</span></span>            |      |      | <span data-ttu-id="d36a3-128">x</span><span class="sxs-lookup"><span data-stu-id="d36a3-128">x</span></span>    | <span data-ttu-id="d36a3-129">x</span><span class="sxs-lookup"><span data-stu-id="d36a3-129">x</span></span>     | <span data-ttu-id="d36a3-130">x</span><span class="sxs-lookup"><span data-stu-id="d36a3-130">x</span></span>    | <span data-ttu-id="d36a3-131">x</span><span class="sxs-lookup"><span data-stu-id="d36a3-131">x</span></span>     |



 

<span data-ttu-id="d36a3-132">Эта инструкция выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="d36a3-132">This instruction does the following:</span></span>


```
if (specified register component is not zero)
{
    Push address of the next instruction to the return address stack.
    Continue execution from the instruction marked by the label.
}
```



<span data-ttu-id="d36a3-133">Эта инструкция использует один слот инструкций шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="d36a3-133">This instruction consumes one vertex shader instruction slot.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d36a3-134">См. также</span><span class="sxs-lookup"><span data-stu-id="d36a3-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d36a3-135">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="d36a3-135">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




