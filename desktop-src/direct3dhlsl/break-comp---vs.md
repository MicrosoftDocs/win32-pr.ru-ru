---
title: Сравнение break_comp
description: Безусловное нарушение текущего цикла в ближайшем ендлуп-VS или ендреп-vs.
ms.assetid: 01745e03-874a-4594-b6ab-12db22d0cb4a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 631998aeba6612d945495d8115a74d00f7e657c7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103890012"
---
# <a name="break_comp---vs"></a><span data-ttu-id="a271d-103">прерывание \_ comp-VS</span><span class="sxs-lookup"><span data-stu-id="a271d-103">break\_comp - vs</span></span>

<span data-ttu-id="a271d-104">Безусловное нарушение текущего цикла в ближайшем [ендлуп-VS](endloop---vs.md) или [ендреп-VS](endrep---vs.md).</span><span class="sxs-lookup"><span data-stu-id="a271d-104">Conditionally break out of the current loop at the nearest [endloop - vs](endloop---vs.md) or [endrep - vs](endrep---vs.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a271d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a271d-105">Syntax</span></span>



| <span data-ttu-id="a271d-106">Разбейте \_ comp src0, src1</span><span class="sxs-lookup"><span data-stu-id="a271d-106">break\_comp src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="a271d-107">Где:</span><span class="sxs-lookup"><span data-stu-id="a271d-107">Where:</span></span>

-   <span data-ttu-id="a271d-108">\_Comp — это сравнение двух исходных регистров.</span><span class="sxs-lookup"><span data-stu-id="a271d-108">\_comp is a comparison between the two source registers.</span></span> <span data-ttu-id="a271d-109">Может принимать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="a271d-109">It can be one of the following:</span></span> 

    | <span data-ttu-id="a271d-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a271d-110">Syntax</span></span> | <span data-ttu-id="a271d-111">Сравнение</span><span class="sxs-lookup"><span data-stu-id="a271d-111">Comparison</span></span>            |
    |--------|-----------------------|
    | <span data-ttu-id="a271d-112">\_gt</span><span class="sxs-lookup"><span data-stu-id="a271d-112">\_gt</span></span>   | <span data-ttu-id="a271d-113">Больше чем</span><span class="sxs-lookup"><span data-stu-id="a271d-113">Greater than</span></span>          |
    | <span data-ttu-id="a271d-114">\_светл</span><span class="sxs-lookup"><span data-stu-id="a271d-114">\_lt</span></span>   | <span data-ttu-id="a271d-115">Меньше чем</span><span class="sxs-lookup"><span data-stu-id="a271d-115">Less than</span></span>             |
    | <span data-ttu-id="a271d-116">\_GE</span><span class="sxs-lookup"><span data-stu-id="a271d-116">\_ge</span></span>   | <span data-ttu-id="a271d-117">Больше или равно</span><span class="sxs-lookup"><span data-stu-id="a271d-117">Greater than or equal</span></span> |
    | <span data-ttu-id="a271d-118">\_Le</span><span class="sxs-lookup"><span data-stu-id="a271d-118">\_le</span></span>   | <span data-ttu-id="a271d-119">Меньше или равно</span><span class="sxs-lookup"><span data-stu-id="a271d-119">Less than or equal</span></span>    |
    | <span data-ttu-id="a271d-120">\_EQ</span><span class="sxs-lookup"><span data-stu-id="a271d-120">\_eq</span></span>   | <span data-ttu-id="a271d-121">Равно</span><span class="sxs-lookup"><span data-stu-id="a271d-121">Equal to</span></span>              |
    | <span data-ttu-id="a271d-122">\_видимому</span><span class="sxs-lookup"><span data-stu-id="a271d-122">\_ne</span></span>   | <span data-ttu-id="a271d-123">Не равно</span><span class="sxs-lookup"><span data-stu-id="a271d-123">Not equal to</span></span>          |

    

     

-   <span data-ttu-id="a271d-124">src0 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="a271d-124">src0 is a source register.</span></span> <span data-ttu-id="a271d-125">Для выбора одного компонента требуется репликация свиззле.</span><span class="sxs-lookup"><span data-stu-id="a271d-125">Replicate swizzle is required to select a single component.</span></span>
-   <span data-ttu-id="a271d-126">src1 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="a271d-126">src1 is a source register.</span></span> <span data-ttu-id="a271d-127">Для выбора одного компонента требуется репликация свиззле.</span><span class="sxs-lookup"><span data-stu-id="a271d-127">Replicate swizzle is required to select a single component.</span></span>

## <a name="remarks"></a><span data-ttu-id="a271d-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="a271d-128">Remarks</span></span>

<span data-ttu-id="a271d-129">Эта инструкция поддерживается в следующих версиях.</span><span class="sxs-lookup"><span data-stu-id="a271d-129">This instruction is supported in the following versions.</span></span>



| <span data-ttu-id="a271d-130">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="a271d-130">Vertex shader versions</span></span> | <span data-ttu-id="a271d-131">1\_1</span><span class="sxs-lookup"><span data-stu-id="a271d-131">1\_1</span></span> | <span data-ttu-id="a271d-132">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a271d-132">2\_0</span></span> | <span data-ttu-id="a271d-133">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a271d-133">2\_x</span></span> | <span data-ttu-id="a271d-134">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a271d-134">2\_sw</span></span> | <span data-ttu-id="a271d-135">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a271d-135">3\_0</span></span> | <span data-ttu-id="a271d-136">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a271d-136">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="a271d-137">разбить \_ comp</span><span class="sxs-lookup"><span data-stu-id="a271d-137">break\_comp</span></span>            |      |      | <span data-ttu-id="a271d-138">x</span><span class="sxs-lookup"><span data-stu-id="a271d-138">x</span></span>    | <span data-ttu-id="a271d-139">x</span><span class="sxs-lookup"><span data-stu-id="a271d-139">x</span></span>     | <span data-ttu-id="a271d-140">x</span><span class="sxs-lookup"><span data-stu-id="a271d-140">x</span></span>    | <span data-ttu-id="a271d-141">x</span><span class="sxs-lookup"><span data-stu-id="a271d-141">x</span></span>     |



 

<span data-ttu-id="a271d-142">Если сравнение истинно, оно выходит из текущего цикла, как показано.</span><span class="sxs-lookup"><span data-stu-id="a271d-142">When the comparison is true, it breaks out of the current loop, as shown.</span></span>


```
if (src0 comparison src1)
   jump to the corresponding endloop or endrep instruction;
```



## <a name="related-topics"></a><span data-ttu-id="a271d-143">См. также</span><span class="sxs-lookup"><span data-stu-id="a271d-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a271d-144">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="a271d-144">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




