---
title: Относительная адресация (Справочник по HLSL PS)
description: Синтаксис \ \ можно использовать только в типах регистров, которые могут быть сравнительно устранены в некоторых моделях шейдеров.
ms.assetid: 37e2bab9-f6fe-438a-8a2d-c963634ef8c3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 38c7be68245cfedbb27898e0fbb689e9e43755ca
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/23/2019
ms.locfileid: "103785064"
---
# <a name="relative-addressing-hlsl-ps-reference"></a><span data-ttu-id="599f6-103">Относительная адресация (Справочник по HLSL PS)</span><span class="sxs-lookup"><span data-stu-id="599f6-103">Relative addressing (HLSL PS reference)</span></span>

<span data-ttu-id="599f6-104">\[ \] Синтаксис можно использовать только в типах регистров, которые могут быть относительно устранены в некоторых моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="599f6-104">The \[ \] syntax can be used only in register types that can be relatively addressed in certain shader models.</span></span> <span data-ttu-id="599f6-105">Ниже перечислены поддерживаемые формы \[ \] синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="599f6-105">The supported forms of \[ \] syntax are listed as follows:</span></span>

<span data-ttu-id="599f6-106">Где:</span><span class="sxs-lookup"><span data-stu-id="599f6-106">Where:</span></span>

-   <span data-ttu-id="599f6-107">"R" обозначает любой тип регистра, который может быть относительно адресован.</span><span class="sxs-lookup"><span data-stu-id="599f6-107">"R" denotes any register type that can be relatively addressed.</span></span>
-   <span data-ttu-id="599f6-108">"A" обозначает любой регистр, который можно использовать в качестве индекса для относительно других регистров.</span><span class="sxs-lookup"><span data-stu-id="599f6-108">"A" denotes any register that can be used as an index to relatively address other registers.</span></span>
-   <span data-ttu-id="599f6-109">N0 — Ni, M0-MJ и k — целые числа >= 0.</span><span class="sxs-lookup"><span data-stu-id="599f6-109">n0 - ni, m0 - mj, and k are integers >= 0.</span></span>



| <span data-ttu-id="599f6-110">\[\]синтаксис</span><span class="sxs-lookup"><span data-stu-id="599f6-110">\[ \] syntax</span></span>                              | <span data-ttu-id="599f6-111">Эффективный индекс</span><span class="sxs-lookup"><span data-stu-id="599f6-111">Effective index</span></span>                       | <span data-ttu-id="599f6-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="599f6-112">Examples</span></span>                         |
|-------------------------------------------|---------------------------------------|----------------------------------|
| <span data-ttu-id="599f6-113">R \[ A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="599f6-113">R\[ A + m0 + ... + mj \]</span></span>                  | <span data-ttu-id="599f6-114">A + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="599f6-114">A + m0 + ... + mj</span></span>                     | <span data-ttu-id="599f6-115">c \[ a0. x + 3 + 7 \]</span><span class="sxs-lookup"><span data-stu-id="599f6-115">c\[ a0.x + 3 + 7 \]</span></span>              |
| <span data-ttu-id="599f6-116">R \[ k \] (= ать)</span><span class="sxs-lookup"><span data-stu-id="599f6-116">R\[ k \] ( = Rk )</span></span>                         | <span data-ttu-id="599f6-117">k</span><span class="sxs-lookup"><span data-stu-id="599f6-117">k</span></span>                                     | <span data-ttu-id="599f6-118">c \[ 10 \] (= C10)</span><span class="sxs-lookup"><span data-stu-id="599f6-118">c\[ 10 \] ( = c10 )</span></span>              |
| <span data-ttu-id="599f6-119">R \[ A \]</span><span class="sxs-lookup"><span data-stu-id="599f6-119">R\[ A \]</span></span>                                  | <span data-ttu-id="599f6-120">Объект</span><span class="sxs-lookup"><span data-stu-id="599f6-120">A</span></span>                                     | <span data-ttu-id="599f6-121">c \[ a0. y \]</span><span class="sxs-lookup"><span data-stu-id="599f6-121">c\[ a0.y \]</span></span>                      |
| <span data-ttu-id="599f6-122">Ать \[ N0 +... + Ni + A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="599f6-122">Rk\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span> | <span data-ttu-id="599f6-123">A + k + N0 +... + Ni + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="599f6-123">A + k + n0 + ... + ni + m0 + ... + mj</span></span> | <span data-ttu-id="599f6-124">C8 \[ 3 + 2 + a0. w + 5 + 6 + 1 \]</span><span class="sxs-lookup"><span data-stu-id="599f6-124">c8\[ 3 + 2 + a0.w + 5 + 6 + 1 \]</span></span> |
| <span data-ttu-id="599f6-125">R \[ N0 +... + Ni + A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="599f6-125">R\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span>  | <span data-ttu-id="599f6-126">A + N0 +... + Ni + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="599f6-126">A + n0 + ... + ni + m0 + ... + mj</span></span>     | <span data-ttu-id="599f6-127">c \[ 2 + 1 + Al + 3 + 4 + 5 \]</span><span class="sxs-lookup"><span data-stu-id="599f6-127">c\[ 2 + 1 + aL + 3 + 4 + 5 \]</span></span>    |
| <span data-ttu-id="599f6-128">Ать \[ A \]</span><span class="sxs-lookup"><span data-stu-id="599f6-128">Rk\[ A \]</span></span>                                 | <span data-ttu-id="599f6-129">A + k</span><span class="sxs-lookup"><span data-stu-id="599f6-129">A + k</span></span>                                 | <span data-ttu-id="599f6-130">C12 \[ Al \] , C0 \[ a0. z \]</span><span class="sxs-lookup"><span data-stu-id="599f6-130">c12\[ aL \], c0\[ a0.z \]</span></span>        |
| <span data-ttu-id="599f6-131">Ать \[ A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="599f6-131">Rk\[ A + m0 + ... + mj \]</span></span>                 | <span data-ttu-id="599f6-132">A + k + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="599f6-132">A + k + m0 + ... + mj</span></span>                 | <span data-ttu-id="599f6-133">v1 \[ Al + 4 + 8 \]</span><span class="sxs-lookup"><span data-stu-id="599f6-133">v1\[ aL + 4 + 8 \]</span></span>               |
| <span data-ttu-id="599f6-134">R \[ N0 +... + Ni + A \]</span><span class="sxs-lookup"><span data-stu-id="599f6-134">R\[ n0 + ... + ni + A \]</span></span>                  | <span data-ttu-id="599f6-135">A + N0 +... + Ni</span><span class="sxs-lookup"><span data-stu-id="599f6-135">A + n0 + ... + ni</span></span>                     | <span data-ttu-id="599f6-136">o \[ 3 + 1 + Al \]</span><span class="sxs-lookup"><span data-stu-id="599f6-136">o\[ 3 + 1 + aL \]</span></span>                |
| <span data-ttu-id="599f6-137">Ать \[ N0 +... + Ni + A \]</span><span class="sxs-lookup"><span data-stu-id="599f6-137">Rk\[ n0 + ... + ni + A \]</span></span>                 | <span data-ttu-id="599f6-138">A + k + N0 +... + Ni</span><span class="sxs-lookup"><span data-stu-id="599f6-138">A + k + n0 + ... + ni</span></span>                 | <span data-ttu-id="599f6-139">O1 \[ 2 + 1 + 3 + Al \]</span><span class="sxs-lookup"><span data-stu-id="599f6-139">o1\[ 2 + 1 + 3 + aL \]</span></span>           |



 

<span data-ttu-id="599f6-140">Регистры доступны в следующих версиях:</span><span class="sxs-lookup"><span data-stu-id="599f6-140">The registers are available in the following versions:</span></span>



| <span data-ttu-id="599f6-141">Тип регистра</span><span class="sxs-lookup"><span data-stu-id="599f6-141">Register type</span></span>                                                                                   | <span data-ttu-id="599f6-142">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="599f6-142">Pixel Shader Versions</span></span> |
|-------------------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="599f6-143">[Счетчик цикла](dx9-graphics-reference-asm-ps-registers-loop-counter.md): Al во входных регистрах</span><span class="sxs-lookup"><span data-stu-id="599f6-143">[loop counter](dx9-graphics-reference-asm-ps-registers-loop-counter.md): aL on input registers</span></span> | <span data-ttu-id="599f6-144">PS \_ 3 \_ и выше</span><span class="sxs-lookup"><span data-stu-id="599f6-144">ps\_3\_0 and higher</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="599f6-145">См. также</span><span class="sxs-lookup"><span data-stu-id="599f6-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="599f6-146">Регистры</span><span class="sxs-lookup"><span data-stu-id="599f6-146">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




