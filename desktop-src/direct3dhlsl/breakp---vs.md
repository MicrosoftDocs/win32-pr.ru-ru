---
title: бреакп — VS
description: Безусловное нарушение текущего цикла в ближайшем ендлуп-VS или ендреп-vs. Используйте один из компонентов, зарегистрированных в предикате, чтобы определить, следует ли выполнять инструкцию.
ms.assetid: 940252a0-6f6a-45d8-9d2f-315cc97686ca
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dbd0d5e20040bc2d353287eb4243c9e9d6d21dc8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104069346"
---
# <a name="breakp---vs"></a><span data-ttu-id="b7aee-103">бреакп — VS</span><span class="sxs-lookup"><span data-stu-id="b7aee-103">breakp - vs</span></span>

<span data-ttu-id="b7aee-104">Безусловное нарушение текущего цикла в ближайшем [ендлуп-VS](endloop---vs.md) или [ендреп-VS](endrep---vs.md). Используйте один из компонентов в качестве условия, чтобы определить, следует ли выполнять инструкцию.</span><span class="sxs-lookup"><span data-stu-id="b7aee-104">Conditionally break out of the current loop at the nearest [endloop - vs](endloop---vs.md) or [endrep - vs](endrep---vs.md). Use one of the components of the predicate register as a condition to determine whether or not to perform the instruction.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7aee-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b7aee-105">Syntax</span></span>



| <span data-ttu-id="b7aee-106">бреакп \[ ! \] P0. x</span><span class="sxs-lookup"><span data-stu-id="b7aee-106">breakp \[!\]p0.{x\</span></span>|<span data-ttu-id="b7aee-107">&</span><span class="sxs-lookup"><span data-stu-id="b7aee-107">y\</span></span>|<span data-ttu-id="b7aee-108">гармошкой</span><span class="sxs-lookup"><span data-stu-id="b7aee-108">z\</span></span>|<span data-ttu-id="b7aee-109">Белая</span><span class="sxs-lookup"><span data-stu-id="b7aee-109">w}</span></span> |
|-----------------------------|



 

<span data-ttu-id="b7aee-110">Где:</span><span class="sxs-lookup"><span data-stu-id="b7aee-110">Where:</span></span>

-   <span data-ttu-id="b7aee-111">\[!\] Необязательное логическое значение NOT.</span><span class="sxs-lookup"><span data-stu-id="b7aee-111">\[!\] optional boolean NOT.</span></span>
-   <span data-ttu-id="b7aee-112">P0 — это регистр предикатов.</span><span class="sxs-lookup"><span data-stu-id="b7aee-112">p0 is the predicate register.</span></span> <span data-ttu-id="b7aee-113">См. раздел [Регистрация предиката](dx9-graphics-reference-asm-vs-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="b7aee-113">See [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md).</span></span>
-   <span data-ttu-id="b7aee-114">{x \| y \| z \| w} — это обязательная репликация свиззле в P0.</span><span class="sxs-lookup"><span data-stu-id="b7aee-114">{x\|y\|z\|w} is the required replicate swizzle on p0.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7aee-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="b7aee-115">Remarks</span></span>



| <span data-ttu-id="b7aee-116">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="b7aee-116">Vertex shader versions</span></span> | <span data-ttu-id="b7aee-117">1\_1</span><span class="sxs-lookup"><span data-stu-id="b7aee-117">1\_1</span></span> | <span data-ttu-id="b7aee-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b7aee-118">2\_0</span></span> | <span data-ttu-id="b7aee-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b7aee-119">2\_x</span></span> | <span data-ttu-id="b7aee-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b7aee-120">2\_sw</span></span> | <span data-ttu-id="b7aee-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b7aee-121">3\_0</span></span> | <span data-ttu-id="b7aee-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b7aee-122">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="b7aee-123">бреакп</span><span class="sxs-lookup"><span data-stu-id="b7aee-123">breakp</span></span>                 |      |      | <span data-ttu-id="b7aee-124">x</span><span class="sxs-lookup"><span data-stu-id="b7aee-124">x</span></span>    | <span data-ttu-id="b7aee-125">x</span><span class="sxs-lookup"><span data-stu-id="b7aee-125">x</span></span>     | <span data-ttu-id="b7aee-126">x</span><span class="sxs-lookup"><span data-stu-id="b7aee-126">x</span></span>    | <span data-ttu-id="b7aee-127">x</span><span class="sxs-lookup"><span data-stu-id="b7aee-127">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="b7aee-128">См. также</span><span class="sxs-lookup"><span data-stu-id="b7aee-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7aee-129">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="b7aee-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




