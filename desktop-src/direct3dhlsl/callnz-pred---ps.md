---
title: каллнз, пред-PS
description: Вызов с предикатом, если он не равен нулю. Выполняет условный вызов инструкции, помеченной индексом метки. Затенения использует логическое значение, чтобы определить, не нужно ли выполнять инструкцию.
ms.assetid: 9c839fc7-8b4d-4ca1-b30f-5c3f8fb45eae
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a04bd4b1bfa16d965a90b66e3956674ecb112590
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103987077"
---
# <a name="callnz-pred---ps"></a><span data-ttu-id="698bd-105">каллнз, пред-PS</span><span class="sxs-lookup"><span data-stu-id="698bd-105">callnz pred - ps</span></span>

<span data-ttu-id="698bd-106">Вызов с предикатом, если он не равен нулю.</span><span class="sxs-lookup"><span data-stu-id="698bd-106">Call with a predicate, if not zero.</span></span> <span data-ttu-id="698bd-107">Выполняет условный вызов инструкции, помеченной индексом метки.</span><span class="sxs-lookup"><span data-stu-id="698bd-107">Performs a conditional call to the instruction marked by the label index.</span></span> <span data-ttu-id="698bd-108">Затенения использует логическое значение, чтобы определить, не нужно ли выполнять инструкцию.</span><span class="sxs-lookup"><span data-stu-id="698bd-108">Predication uses a Boolean value to determine whether of not to perform the instruction.</span></span>

## <a name="syntax"></a><span data-ttu-id="698bd-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="698bd-109">Syntax</span></span>



| <span data-ttu-id="698bd-110">каллнз l \# , \[ ! \] P0. x</span><span class="sxs-lookup"><span data-stu-id="698bd-110">callnz l\#, \[!\]p0.{x\</span></span>|<span data-ttu-id="698bd-111">&</span><span class="sxs-lookup"><span data-stu-id="698bd-111">y\</span></span>|<span data-ttu-id="698bd-112">гармошкой</span><span class="sxs-lookup"><span data-stu-id="698bd-112">z\</span></span>|<span data-ttu-id="698bd-113">Белая</span><span class="sxs-lookup"><span data-stu-id="698bd-113">w}</span></span> |
|----------------------------------|



 

<span data-ttu-id="698bd-114">Где:</span><span class="sxs-lookup"><span data-stu-id="698bd-114">Where:</span></span>

-   <span data-ttu-id="698bd-115">где l \# — [Метка-PS](label---ps.md) , помечающая начало подпрограммы для вызова.</span><span class="sxs-lookup"><span data-stu-id="698bd-115">where l\# is a [label - ps](label---ps.md) marking the beginning of the subroutine to be called.</span></span>
-   <span data-ttu-id="698bd-116">\[!\] является необязательным модификатором отрицания.</span><span class="sxs-lookup"><span data-stu-id="698bd-116">\[!\] is an optional negate modifier.</span></span>
-   <span data-ttu-id="698bd-117">P0 — это регистр предикатов.</span><span class="sxs-lookup"><span data-stu-id="698bd-117">p0 is the predicate register.</span></span> <span data-ttu-id="698bd-118">См. раздел [Регистрация предиката](dx9-graphics-reference-asm-ps-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="698bd-118">See [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).</span></span>
-   <span data-ttu-id="698bd-119">{x \| y \| z \| w} — это обязательная репликация свиззле в P0.</span><span class="sxs-lookup"><span data-stu-id="698bd-119">{x\|y\|z\|w} is the required replicate swizzle on p0.</span></span>

## <a name="remarks"></a><span data-ttu-id="698bd-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="698bd-120">Remarks</span></span>



| <span data-ttu-id="698bd-121">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="698bd-121">Pixel shader versions</span></span> | <span data-ttu-id="698bd-122">1\_1</span><span class="sxs-lookup"><span data-stu-id="698bd-122">1\_1</span></span> | <span data-ttu-id="698bd-123">1\_2</span><span class="sxs-lookup"><span data-stu-id="698bd-123">1\_2</span></span> | <span data-ttu-id="698bd-124">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="698bd-124">1\_3</span></span> | <span data-ttu-id="698bd-125">1\_4</span><span class="sxs-lookup"><span data-stu-id="698bd-125">1\_4</span></span> | <span data-ttu-id="698bd-126">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="698bd-126">2\_0</span></span> | <span data-ttu-id="698bd-127">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="698bd-127">2\_x</span></span> | <span data-ttu-id="698bd-128">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="698bd-128">2\_sw</span></span> | <span data-ttu-id="698bd-129">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="698bd-129">3\_0</span></span> | <span data-ttu-id="698bd-130">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="698bd-130">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="698bd-131">каллнз, пред.</span><span class="sxs-lookup"><span data-stu-id="698bd-131">callnz pred</span></span>           |      |      |      |      |      | <span data-ttu-id="698bd-132">x</span><span class="sxs-lookup"><span data-stu-id="698bd-132">x</span></span>    | <span data-ttu-id="698bd-133">x</span><span class="sxs-lookup"><span data-stu-id="698bd-133">x</span></span>     | <span data-ttu-id="698bd-134">x</span><span class="sxs-lookup"><span data-stu-id="698bd-134">x</span></span>    | <span data-ttu-id="698bd-135">x</span><span class="sxs-lookup"><span data-stu-id="698bd-135">x</span></span>     |



 

<span data-ttu-id="698bd-136">Эта инструкция выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="698bd-136">This instruction does the following:</span></span>


```
if (specified register component is not zero)
{
    Push address of the next instruction to the return address stack
    Continue execution from the instruction marked by the label
}
```



## <a name="related-topics"></a><span data-ttu-id="698bd-137">См. также</span><span class="sxs-lookup"><span data-stu-id="698bd-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="698bd-138">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="698bd-138">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




