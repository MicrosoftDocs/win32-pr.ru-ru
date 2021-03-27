---
title: break_comp-PS
description: Разбейте текущий цикл на ближайшее ендлуп-PS или ендреп-PS на основе сравнения для каждого компонента.
ms.assetid: d21e850f-05db-4a29-b15b-85bb1c1410d0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5088312a16102153ad78afffdcd9ea1275d34e0d
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104133318"
---
# <a name="break_comp---ps"></a><span data-ttu-id="16665-103">Останов \_ comp-PS</span><span class="sxs-lookup"><span data-stu-id="16665-103">break\_comp - ps</span></span>

<span data-ttu-id="16665-104">Разбейте текущий цикл на ближайшее [ендлуп-PS](endloop---ps.md) или [ендреп-PS](endrep---ps.md)на основе сравнения для каждого компонента.</span><span class="sxs-lookup"><span data-stu-id="16665-104">Break out of the current loop at the nearest [endloop - ps](endloop---ps.md) or [endrep - ps](endrep---ps.md), based on a per-component comparison.</span></span>

## <a name="syntax"></a><span data-ttu-id="16665-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="16665-105">Syntax</span></span>



| <span data-ttu-id="16665-106">Разбейте \_ comp src0, src1</span><span class="sxs-lookup"><span data-stu-id="16665-106">break\_comp src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="16665-107">Где:</span><span class="sxs-lookup"><span data-stu-id="16665-107">Where:</span></span>

-   <span data-ttu-id="16665-108">\_Comp — это скалярное (или единственное) сравнение между двумя исходными регистрами.</span><span class="sxs-lookup"><span data-stu-id="16665-108">\_comp is a scalar (or single) comparison between the two source registers.</span></span> <span data-ttu-id="16665-109">Может принимать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="16665-109">It can be one of the following:</span></span> 

    | <span data-ttu-id="16665-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="16665-110">Syntax</span></span> | <span data-ttu-id="16665-111">Сравнение</span><span class="sxs-lookup"><span data-stu-id="16665-111">Comparison</span></span>            |
    |--------|-----------------------|
    | <span data-ttu-id="16665-112">\_gt</span><span class="sxs-lookup"><span data-stu-id="16665-112">\_gt</span></span>   | <span data-ttu-id="16665-113">Больше чем</span><span class="sxs-lookup"><span data-stu-id="16665-113">Greater than</span></span>          |
    | <span data-ttu-id="16665-114">\_светл</span><span class="sxs-lookup"><span data-stu-id="16665-114">\_lt</span></span>   | <span data-ttu-id="16665-115">Меньше чем</span><span class="sxs-lookup"><span data-stu-id="16665-115">Less than</span></span>             |
    | <span data-ttu-id="16665-116">\_GE</span><span class="sxs-lookup"><span data-stu-id="16665-116">\_ge</span></span>   | <span data-ttu-id="16665-117">Больше или равно</span><span class="sxs-lookup"><span data-stu-id="16665-117">Greater than or equal</span></span> |
    | <span data-ttu-id="16665-118">\_Le</span><span class="sxs-lookup"><span data-stu-id="16665-118">\_le</span></span>   | <span data-ttu-id="16665-119">Меньше или равно</span><span class="sxs-lookup"><span data-stu-id="16665-119">Less than or equal</span></span>    |
    | <span data-ttu-id="16665-120">\_EQ</span><span class="sxs-lookup"><span data-stu-id="16665-120">\_eq</span></span>   | <span data-ttu-id="16665-121">Равно</span><span class="sxs-lookup"><span data-stu-id="16665-121">Equal to</span></span>              |
    | <span data-ttu-id="16665-122">\_видимому</span><span class="sxs-lookup"><span data-stu-id="16665-122">\_ne</span></span>   | <span data-ttu-id="16665-123">Не равно</span><span class="sxs-lookup"><span data-stu-id="16665-123">Not equal to</span></span>          |

    

     

-   <span data-ttu-id="16665-124">src0 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="16665-124">src0 is a source register.</span></span> <span data-ttu-id="16665-125">При выборе одного компонента требуется репликация свиззле.</span><span class="sxs-lookup"><span data-stu-id="16665-125">Replicate swizzle is required if selecting a single component.</span></span>
-   <span data-ttu-id="16665-126">src1 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="16665-126">src1 is a source register.</span></span> <span data-ttu-id="16665-127">При выборе одного компонента требуется репликация свиззле.</span><span class="sxs-lookup"><span data-stu-id="16665-127">Replicate swizzle is required if selecting a single component.</span></span>

## <a name="remarks"></a><span data-ttu-id="16665-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="16665-128">Remarks</span></span>

<span data-ttu-id="16665-129">Эта инструкция поддерживается в следующих версиях.</span><span class="sxs-lookup"><span data-stu-id="16665-129">This instruction is supported in the following versions.</span></span>



| <span data-ttu-id="16665-130">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="16665-130">Pixel shader versions</span></span> | <span data-ttu-id="16665-131">1\_1</span><span class="sxs-lookup"><span data-stu-id="16665-131">1\_1</span></span> | <span data-ttu-id="16665-132">1\_2</span><span class="sxs-lookup"><span data-stu-id="16665-132">1\_2</span></span> | <span data-ttu-id="16665-133">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="16665-133">1\_3</span></span> | <span data-ttu-id="16665-134">1\_4</span><span class="sxs-lookup"><span data-stu-id="16665-134">1\_4</span></span> | <span data-ttu-id="16665-135">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="16665-135">2\_0</span></span> | <span data-ttu-id="16665-136">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="16665-136">2\_x</span></span> | <span data-ttu-id="16665-137">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="16665-137">2\_sw</span></span> | <span data-ttu-id="16665-138">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="16665-138">3\_0</span></span> | <span data-ttu-id="16665-139">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="16665-139">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="16665-140">разбить \_ comp</span><span class="sxs-lookup"><span data-stu-id="16665-140">break\_comp</span></span>           |      |      |      |      |      | <span data-ttu-id="16665-141">x</span><span class="sxs-lookup"><span data-stu-id="16665-141">x</span></span>    | <span data-ttu-id="16665-142">x</span><span class="sxs-lookup"><span data-stu-id="16665-142">x</span></span>     | <span data-ttu-id="16665-143">x</span><span class="sxs-lookup"><span data-stu-id="16665-143">x</span></span>    | <span data-ttu-id="16665-144">x</span><span class="sxs-lookup"><span data-stu-id="16665-144">x</span></span>     |



 

<span data-ttu-id="16665-145">Если сравнение истинно, оно выходит из текущего цикла, как показано.</span><span class="sxs-lookup"><span data-stu-id="16665-145">When the comparison is true, it breaks out of the current loop, as shown.</span></span>


```
if (!(src0 comparison src1))
   jump to the corresponding endloop or endrep instruction;
```



## <a name="related-topics"></a><span data-ttu-id="16665-146">См. также</span><span class="sxs-lookup"><span data-stu-id="16665-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16665-147">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="16665-147">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




