---
title: бреакп-PS
description: Условное нарушение текущего цикла в ближайшем ендлуп-PS или ендреп-PS. Используйте один из компонентов в качестве условия, чтобы определить, следует ли выполнять инструкцию.
ms.assetid: be219239-fccb-4561-8b71-083c47ba915b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6e358debb2377f08574997acd96c11f83d32e66c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412192"
---
# <a name="breakp---ps"></a><span data-ttu-id="07245-104">бреакп-PS</span><span class="sxs-lookup"><span data-stu-id="07245-104">breakp - ps</span></span>

<span data-ttu-id="07245-105">Условное нарушение текущего цикла в ближайшем [ендлуп-PS](endloop---ps.md) или [ендреп-PS](endrep---ps.md).</span><span class="sxs-lookup"><span data-stu-id="07245-105">Conditionally break out of the current loop at the nearest [endloop - ps](endloop---ps.md) or [endrep - ps](endrep---ps.md).</span></span> <span data-ttu-id="07245-106">Используйте один из компонентов в качестве условия, чтобы определить, следует ли выполнять инструкцию.</span><span class="sxs-lookup"><span data-stu-id="07245-106">Use one of the components of the predicate register as a condition to determine whether or not to perform the instruction.</span></span>

## <a name="syntax"></a><span data-ttu-id="07245-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="07245-107">Syntax</span></span>



| <span data-ttu-id="07245-108">бреакп \[ ! \] P0. x</span><span class="sxs-lookup"><span data-stu-id="07245-108">breakp \[!\]p0.{x\</span></span>|<span data-ttu-id="07245-109">&</span><span class="sxs-lookup"><span data-stu-id="07245-109">y\</span></span>|<span data-ttu-id="07245-110">гармошкой</span><span class="sxs-lookup"><span data-stu-id="07245-110">z\</span></span>|<span data-ttu-id="07245-111">Белая</span><span class="sxs-lookup"><span data-stu-id="07245-111">w}</span></span> |
|-----------------------------|



 

<span data-ttu-id="07245-112">Где:</span><span class="sxs-lookup"><span data-stu-id="07245-112">Where:</span></span>

-   <span data-ttu-id="07245-113">\[!\] является необязательным модификатором отрицания.</span><span class="sxs-lookup"><span data-stu-id="07245-113">\[!\] is an optional negate modifier.</span></span>
-   <span data-ttu-id="07245-114">P0 — это [регистр предикатов](dx9-graphics-reference-asm-ps-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="07245-114">p0 is the [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).</span></span>
-   <span data-ttu-id="07245-115">{x \| y \| z \| w} — это обязательная репликация свиззле в P0.</span><span class="sxs-lookup"><span data-stu-id="07245-115">{x\|y\|z\|w} is the required replicate swizzle on p0.</span></span>

## <a name="remarks"></a><span data-ttu-id="07245-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="07245-116">Remarks</span></span>



| <span data-ttu-id="07245-117">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="07245-117">Pixel shader versions</span></span> | <span data-ttu-id="07245-118">1\_1</span><span class="sxs-lookup"><span data-stu-id="07245-118">1\_1</span></span> | <span data-ttu-id="07245-119">1\_2</span><span class="sxs-lookup"><span data-stu-id="07245-119">1\_2</span></span> | <span data-ttu-id="07245-120">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="07245-120">1\_3</span></span> | <span data-ttu-id="07245-121">1\_4</span><span class="sxs-lookup"><span data-stu-id="07245-121">1\_4</span></span> | <span data-ttu-id="07245-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="07245-122">2\_0</span></span> | <span data-ttu-id="07245-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="07245-123">2\_x</span></span> | <span data-ttu-id="07245-124">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="07245-124">2\_sw</span></span> | <span data-ttu-id="07245-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="07245-125">3\_0</span></span> | <span data-ttu-id="07245-126">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="07245-126">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="07245-127">бреакп</span><span class="sxs-lookup"><span data-stu-id="07245-127">breakp</span></span>                |      |      |      |      |      | <span data-ttu-id="07245-128">x</span><span class="sxs-lookup"><span data-stu-id="07245-128">x</span></span>    | <span data-ttu-id="07245-129">x</span><span class="sxs-lookup"><span data-stu-id="07245-129">x</span></span>     | <span data-ttu-id="07245-130">x</span><span class="sxs-lookup"><span data-stu-id="07245-130">x</span></span>    | <span data-ttu-id="07245-131">x</span><span class="sxs-lookup"><span data-stu-id="07245-131">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="07245-132">См. также</span><span class="sxs-lookup"><span data-stu-id="07245-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07245-133">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="07245-133">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




