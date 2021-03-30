---
title: каллнз bool-PS
description: Вызовите, если не равен нулю. Выполняет условный вызов инструкции, помеченной индексом метки. | каллнз bool-PS
ms.assetid: 1b9ff276-c2b8-46cc-96ac-a5b5455c5cc0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0516e62ce07c60866715591bc59123f38dc5c272
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998279"
---
# <a name="callnz-bool---ps"></a><span data-ttu-id="09b72-105">каллнз bool-PS</span><span class="sxs-lookup"><span data-stu-id="09b72-105">callnz bool - ps</span></span>

<span data-ttu-id="09b72-106">Вызовите, если не равен нулю.</span><span class="sxs-lookup"><span data-stu-id="09b72-106">Call if not zero.</span></span> <span data-ttu-id="09b72-107">Выполняет условный вызов инструкции, помеченной индексом метки.</span><span class="sxs-lookup"><span data-stu-id="09b72-107">Performs a conditional call to the instruction marked by the label index.</span></span>

## <a name="syntax"></a><span data-ttu-id="09b72-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="09b72-108">Syntax</span></span>



| <span data-ttu-id="09b72-109">каллнз l \# , \[ ! \] &\#</span><span class="sxs-lookup"><span data-stu-id="09b72-109">callnz l\#, \[!\]b\#</span></span> |
|----------------------|



 

<span data-ttu-id="09b72-110">Где:</span><span class="sxs-lookup"><span data-stu-id="09b72-110">Where:</span></span>

-   <span data-ttu-id="09b72-111">l \# — [Метка-PS](label---ps.md) , помечающая начало подпрограммы для вызова.</span><span class="sxs-lookup"><span data-stu-id="09b72-111">l\# is a [label - ps](label---ps.md) marking the beginning of the subroutine to be called.</span></span>
-   <span data-ttu-id="09b72-112">\[!\] является необязательным модификатором отрицания.</span><span class="sxs-lookup"><span data-stu-id="09b72-112">\[!\] is an optional negate modifier.</span></span>
-   <span data-ttu-id="09b72-113">b \# определяет [константу логического регистра](dx9-graphics-reference-asm-ps-registers-constant-boolean.md).</span><span class="sxs-lookup"><span data-stu-id="09b72-113">b\# identifies a [Constant Boolean Register](dx9-graphics-reference-asm-ps-registers-constant-boolean.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="09b72-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="09b72-114">Remarks</span></span>



| <span data-ttu-id="09b72-115">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="09b72-115">Pixel shader versions</span></span> | <span data-ttu-id="09b72-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="09b72-116">1\_1</span></span> | <span data-ttu-id="09b72-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="09b72-117">1\_2</span></span> | <span data-ttu-id="09b72-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="09b72-118">1\_3</span></span> | <span data-ttu-id="09b72-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="09b72-119">1\_4</span></span> | <span data-ttu-id="09b72-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="09b72-120">2\_0</span></span> | <span data-ttu-id="09b72-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="09b72-121">2\_x</span></span> | <span data-ttu-id="09b72-122">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="09b72-122">2\_sw</span></span> | <span data-ttu-id="09b72-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="09b72-123">3\_0</span></span> | <span data-ttu-id="09b72-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="09b72-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="09b72-125">bool каллнз</span><span class="sxs-lookup"><span data-stu-id="09b72-125">callnz bool</span></span>           |      |      |      |      |      | <span data-ttu-id="09b72-126">x</span><span class="sxs-lookup"><span data-stu-id="09b72-126">x</span></span>    | <span data-ttu-id="09b72-127">x</span><span class="sxs-lookup"><span data-stu-id="09b72-127">x</span></span>     | <span data-ttu-id="09b72-128">x</span><span class="sxs-lookup"><span data-stu-id="09b72-128">x</span></span>    | <span data-ttu-id="09b72-129">x</span><span class="sxs-lookup"><span data-stu-id="09b72-129">x</span></span>     |



 

<span data-ttu-id="09b72-130">Эта инструкция выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="09b72-130">This instruction does the following:</span></span>


```
if (specified Boolean register is not zero)
{
    Push address of the next instruction to the return address stack
    Continue execution from the instruction marked by the label
}
```



## <a name="related-topics"></a><span data-ttu-id="09b72-131">См. также</span><span class="sxs-lookup"><span data-stu-id="09b72-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09b72-132">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="09b72-132">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




