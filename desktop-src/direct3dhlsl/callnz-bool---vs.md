---
title: каллнз bool — VS
description: Вызовите, если не равен нулю. Выполняет условный вызов инструкции, помеченной индексом метки. | каллнз bool — VS
ms.assetid: 9be030b9-fa21-459f-bd6c-f34ad6f177fc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f3932f4c5d50445b3220a0460a5c434a1ff8aae4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998276"
---
# <a name="callnz-bool---vs"></a><span data-ttu-id="4798f-105">каллнз bool — VS</span><span class="sxs-lookup"><span data-stu-id="4798f-105">callnz bool - vs</span></span>

<span data-ttu-id="4798f-106">Вызовите, если не равен нулю.</span><span class="sxs-lookup"><span data-stu-id="4798f-106">Call if not zero.</span></span> <span data-ttu-id="4798f-107">Выполняет условный вызов инструкции, помеченной индексом метки.</span><span class="sxs-lookup"><span data-stu-id="4798f-107">Performs a conditional call to the instruction marked by the label index.</span></span>

## <a name="syntax"></a><span data-ttu-id="4798f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4798f-108">Syntax</span></span>



| <span data-ttu-id="4798f-109">каллнз l \# , \[ ! \] &\#</span><span class="sxs-lookup"><span data-stu-id="4798f-109">callnz l\#, \[!\]b\#</span></span> |
|----------------------|



 

<span data-ttu-id="4798f-110">где:</span><span class="sxs-lookup"><span data-stu-id="4798f-110">where:</span></span>

-   <span data-ttu-id="4798f-111">где l \# — [Метка — VS](label---vs.md) отмечает начало подпрограммы, которую необходимо вызвать.</span><span class="sxs-lookup"><span data-stu-id="4798f-111">where l\# is a [label - vs](label---vs.md) marking the beginning of the subroutine to be called.</span></span>
-   <span data-ttu-id="4798f-112">\[!\] Необязательный логический модификатор NOT.</span><span class="sxs-lookup"><span data-stu-id="4798f-112">\[!\] is the optional boolean NOT modifier.</span></span>
-   <span data-ttu-id="4798f-113">b \# определяет [константу логического регистра](dx9-graphics-reference-asm-vs-registers-constant-boolean.md).</span><span class="sxs-lookup"><span data-stu-id="4798f-113">b\# identifies a [Constant Boolean Register](dx9-graphics-reference-asm-vs-registers-constant-boolean.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4798f-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="4798f-114">Remarks</span></span>



| <span data-ttu-id="4798f-115">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="4798f-115">Vertex shader versions</span></span> | <span data-ttu-id="4798f-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="4798f-116">1\_1</span></span> | <span data-ttu-id="4798f-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4798f-117">2\_0</span></span> | <span data-ttu-id="4798f-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="4798f-118">2\_x</span></span> | <span data-ttu-id="4798f-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4798f-119">2\_sw</span></span> | <span data-ttu-id="4798f-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4798f-120">3\_0</span></span> | <span data-ttu-id="4798f-121">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4798f-121">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="4798f-122">bool каллнз</span><span class="sxs-lookup"><span data-stu-id="4798f-122">callnz bool</span></span>            |      | <span data-ttu-id="4798f-123">x</span><span class="sxs-lookup"><span data-stu-id="4798f-123">x</span></span>    | <span data-ttu-id="4798f-124">x</span><span class="sxs-lookup"><span data-stu-id="4798f-124">x</span></span>    | <span data-ttu-id="4798f-125">x</span><span class="sxs-lookup"><span data-stu-id="4798f-125">x</span></span>     | <span data-ttu-id="4798f-126">x</span><span class="sxs-lookup"><span data-stu-id="4798f-126">x</span></span>    | <span data-ttu-id="4798f-127">x</span><span class="sxs-lookup"><span data-stu-id="4798f-127">x</span></span>     |



 

<span data-ttu-id="4798f-128">Эта инструкция выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="4798f-128">This instruction does the following:</span></span>


```
if (specified boolean register is not zero)
{
    Push address of the next instruction to the return address stack.
    Continue execution from the instruction marked by the label.
}
```



<span data-ttu-id="4798f-129">Эта инструкция использует один слот инструкций шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="4798f-129">This instruction consumes one vertex shader instruction slot.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4798f-130">См. также</span><span class="sxs-lookup"><span data-stu-id="4798f-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4798f-131">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="4798f-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




