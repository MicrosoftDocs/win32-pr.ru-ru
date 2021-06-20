---
title: Относительная адресация (Справочник по HLSL PS)
description: Для шейдеров пикселей синтаксис \ \ можно использовать только в типах регистров, которые могут быть сравнительно устранены в некоторых моделях шейдеров.
ms.assetid: 37e2bab9-f6fe-438a-8a2d-c963634ef8c3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8bdafe23696c460da75d87cf1f6d5a968c89ed28
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405487"
---
# <a name="relative-addressing-hlsl-ps-reference"></a><span data-ttu-id="d96df-103">Относительная адресация (Справочник по HLSL PS)</span><span class="sxs-lookup"><span data-stu-id="d96df-103">Relative addressing (HLSL PS reference)</span></span>

<span data-ttu-id="d96df-104">\[ \] Синтаксис можно использовать только в типах регистров, которые могут быть относительно устранены в некоторых моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="d96df-104">The \[ \] syntax can be used only in register types that can be relatively addressed in certain shader models.</span></span> <span data-ttu-id="d96df-105">Ниже перечислены поддерживаемые формы \[ \] синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="d96df-105">The supported forms of \[ \] syntax are listed as follows:</span></span>

<span data-ttu-id="d96df-106">Где:</span><span class="sxs-lookup"><span data-stu-id="d96df-106">Where:</span></span>

-   <span data-ttu-id="d96df-107">"R" обозначает любой тип регистра, который может быть относительно адресован.</span><span class="sxs-lookup"><span data-stu-id="d96df-107">"R" denotes any register type that can be relatively addressed.</span></span>
-   <span data-ttu-id="d96df-108">"A" обозначает любой регистр, который можно использовать в качестве индекса для относительно других регистров.</span><span class="sxs-lookup"><span data-stu-id="d96df-108">"A" denotes any register that can be used as an index to relatively address other registers.</span></span>
-   <span data-ttu-id="d96df-109">N0 — Ni, M0-MJ и k — целые числа >= 0.</span><span class="sxs-lookup"><span data-stu-id="d96df-109">n0 - ni, m0 - mj, and k are integers >= 0.</span></span>



| <span data-ttu-id="d96df-110">\[\]синтаксис</span><span class="sxs-lookup"><span data-stu-id="d96df-110">\[ \] syntax</span></span>                              | <span data-ttu-id="d96df-111">Эффективный индекс</span><span class="sxs-lookup"><span data-stu-id="d96df-111">Effective index</span></span>                       | <span data-ttu-id="d96df-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="d96df-112">Examples</span></span>                         |
|-------------------------------------------|---------------------------------------|----------------------------------|
| <span data-ttu-id="d96df-113">R \[ A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="d96df-113">R\[ A + m0 + ... + mj \]</span></span>                  | <span data-ttu-id="d96df-114">A + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="d96df-114">A + m0 + ... + mj</span></span>                     | <span data-ttu-id="d96df-115">c \[ a0. x + 3 + 7 \]</span><span class="sxs-lookup"><span data-stu-id="d96df-115">c\[ a0.x + 3 + 7 \]</span></span>              |
| <span data-ttu-id="d96df-116">R \[ k \] (= ать)</span><span class="sxs-lookup"><span data-stu-id="d96df-116">R\[ k \] ( = Rk )</span></span>                         | <span data-ttu-id="d96df-117">k</span><span class="sxs-lookup"><span data-stu-id="d96df-117">k</span></span>                                     | <span data-ttu-id="d96df-118">c \[ 10 \] (= C10)</span><span class="sxs-lookup"><span data-stu-id="d96df-118">c\[ 10 \] ( = c10 )</span></span>              |
| <span data-ttu-id="d96df-119">R \[ A \]</span><span class="sxs-lookup"><span data-stu-id="d96df-119">R\[ A \]</span></span>                                  | <span data-ttu-id="d96df-120">A</span><span class="sxs-lookup"><span data-stu-id="d96df-120">A</span></span>                                     | <span data-ttu-id="d96df-121">c \[ a0. y \]</span><span class="sxs-lookup"><span data-stu-id="d96df-121">c\[ a0.y \]</span></span>                      |
| <span data-ttu-id="d96df-122">Ать \[ N0 +... + Ni + A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="d96df-122">Rk\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span> | <span data-ttu-id="d96df-123">A + k + N0 +... + Ni + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="d96df-123">A + k + n0 + ... + ni + m0 + ... + mj</span></span> | <span data-ttu-id="d96df-124">C8 \[ 3 + 2 + a0. w + 5 + 6 + 1 \]</span><span class="sxs-lookup"><span data-stu-id="d96df-124">c8\[ 3 + 2 + a0.w + 5 + 6 + 1 \]</span></span> |
| <span data-ttu-id="d96df-125">R \[ N0 +... + Ni + A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="d96df-125">R\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span>  | <span data-ttu-id="d96df-126">A + N0 +... + Ni + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="d96df-126">A + n0 + ... + ni + m0 + ... + mj</span></span>     | <span data-ttu-id="d96df-127">c \[ 2 + 1 + Al + 3 + 4 + 5 \]</span><span class="sxs-lookup"><span data-stu-id="d96df-127">c\[ 2 + 1 + aL + 3 + 4 + 5 \]</span></span>    |
| <span data-ttu-id="d96df-128">Ать \[ A \]</span><span class="sxs-lookup"><span data-stu-id="d96df-128">Rk\[ A \]</span></span>                                 | <span data-ttu-id="d96df-129">A + k</span><span class="sxs-lookup"><span data-stu-id="d96df-129">A + k</span></span>                                 | <span data-ttu-id="d96df-130">C12 \[ Al \] , C0 \[ a0. z \]</span><span class="sxs-lookup"><span data-stu-id="d96df-130">c12\[ aL \], c0\[ a0.z \]</span></span>        |
| <span data-ttu-id="d96df-131">Ать \[ A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="d96df-131">Rk\[ A + m0 + ... + mj \]</span></span>                 | <span data-ttu-id="d96df-132">A + k + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="d96df-132">A + k + m0 + ... + mj</span></span>                 | <span data-ttu-id="d96df-133">v1 \[ Al + 4 + 8 \]</span><span class="sxs-lookup"><span data-stu-id="d96df-133">v1\[ aL + 4 + 8 \]</span></span>               |
| <span data-ttu-id="d96df-134">R \[ N0 +... + Ni + A \]</span><span class="sxs-lookup"><span data-stu-id="d96df-134">R\[ n0 + ... + ni + A \]</span></span>                  | <span data-ttu-id="d96df-135">A + N0 +... + Ni</span><span class="sxs-lookup"><span data-stu-id="d96df-135">A + n0 + ... + ni</span></span>                     | <span data-ttu-id="d96df-136">o \[ 3 + 1 + Al \]</span><span class="sxs-lookup"><span data-stu-id="d96df-136">o\[ 3 + 1 + aL \]</span></span>                |
| <span data-ttu-id="d96df-137">Ать \[ N0 +... + Ni + A \]</span><span class="sxs-lookup"><span data-stu-id="d96df-137">Rk\[ n0 + ... + ni + A \]</span></span>                 | <span data-ttu-id="d96df-138">A + k + N0 +... + Ni</span><span class="sxs-lookup"><span data-stu-id="d96df-138">A + k + n0 + ... + ni</span></span>                 | <span data-ttu-id="d96df-139">O1 \[ 2 + 1 + 3 + Al \]</span><span class="sxs-lookup"><span data-stu-id="d96df-139">o1\[ 2 + 1 + 3 + aL \]</span></span>           |



 

<span data-ttu-id="d96df-140">Регистры доступны в следующих версиях:</span><span class="sxs-lookup"><span data-stu-id="d96df-140">The registers are available in the following versions:</span></span>



| <span data-ttu-id="d96df-141">Тип регистра</span><span class="sxs-lookup"><span data-stu-id="d96df-141">Register type</span></span>                                                                                   | <span data-ttu-id="d96df-142">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="d96df-142">Pixel Shader Versions</span></span> |
|-------------------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="d96df-143">[Счетчик цикла](dx9-graphics-reference-asm-ps-registers-loop-counter.md): Al во входных регистрах</span><span class="sxs-lookup"><span data-stu-id="d96df-143">[loop counter](dx9-graphics-reference-asm-ps-registers-loop-counter.md): aL on input registers</span></span> | <span data-ttu-id="d96df-144">PS \_ 3 \_ и выше</span><span class="sxs-lookup"><span data-stu-id="d96df-144">ps\_3\_0 and higher</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="d96df-145">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="d96df-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d96df-146">Регистры</span><span class="sxs-lookup"><span data-stu-id="d96df-146">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




