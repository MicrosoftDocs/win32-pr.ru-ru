---
title: Относительная адресация (Справочник по HLSL VS)
description: Для шейдеров вершин синтаксис \ \ можно использовать только в типах регистров, которые могут быть относительно устранены в определенных моделях шейдеров.
ms.assetid: 9f9d2499-73a5-4c9d-9dce-94c914933334
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2bbba694878ba84ac3c2fa9c4e8058bb0d91830e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406697"
---
# <a name="relative-addressing-hlsl-vs-reference"></a><span data-ttu-id="59cc7-103">Относительная адресация (Справочник по HLSL VS)</span><span class="sxs-lookup"><span data-stu-id="59cc7-103">Relative Addressing (HLSL VS reference)</span></span>

<span data-ttu-id="59cc7-104">\[ \] Синтаксис можно использовать только в типах регистров, которые могут быть относительно устранены в некоторых моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="59cc7-104">The \[ \] syntax can be used only in register types that can be relatively addressed in certain shader models.</span></span> <span data-ttu-id="59cc7-105">Ниже перечислены поддерживаемые формы \[ \] синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="59cc7-105">The supported forms of \[ \] syntax are listed as follows:</span></span>

<span data-ttu-id="59cc7-106">Где:</span><span class="sxs-lookup"><span data-stu-id="59cc7-106">Where:</span></span>

-   <span data-ttu-id="59cc7-107">"R" обозначает любой тип регистра, который может быть относительно адресован.</span><span class="sxs-lookup"><span data-stu-id="59cc7-107">"R" denotes any register type that can be relatively addressed.</span></span>
-   <span data-ttu-id="59cc7-108">"A" обозначает любой регистр, который можно использовать в качестве индекса для относительно других регистров.</span><span class="sxs-lookup"><span data-stu-id="59cc7-108">"A" denotes any register that can be used as an index to relatively address other registers.</span></span>
-   <span data-ttu-id="59cc7-109">N0 — Ni, M0-MJ и k — целые числа >= 0.</span><span class="sxs-lookup"><span data-stu-id="59cc7-109">n0 - ni, m0 - mj, and k are integers >= 0.</span></span>



| <span data-ttu-id="59cc7-110">\[\]синтаксис</span><span class="sxs-lookup"><span data-stu-id="59cc7-110">\[ \] syntax</span></span>                              | <span data-ttu-id="59cc7-111">Эффективный индекс</span><span class="sxs-lookup"><span data-stu-id="59cc7-111">Effective index</span></span>                       | <span data-ttu-id="59cc7-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="59cc7-112">Examples</span></span>                         |
|-------------------------------------------|---------------------------------------|----------------------------------|
| <span data-ttu-id="59cc7-113">R \[ A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="59cc7-113">R\[ A + m0 + ... + mj \]</span></span>                  | <span data-ttu-id="59cc7-114">A + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="59cc7-114">A + m0 + ... + mj</span></span>                     | <span data-ttu-id="59cc7-115">c \[ a0. x + 3 + 7 \]</span><span class="sxs-lookup"><span data-stu-id="59cc7-115">c\[ a0.x + 3 + 7 \]</span></span>              |
| <span data-ttu-id="59cc7-116">R \[ k \] (= ать)</span><span class="sxs-lookup"><span data-stu-id="59cc7-116">R\[ k \] ( = Rk )</span></span>                         | <span data-ttu-id="59cc7-117">k</span><span class="sxs-lookup"><span data-stu-id="59cc7-117">k</span></span>                                     | <span data-ttu-id="59cc7-118">c \[ 10 \] (= C10)</span><span class="sxs-lookup"><span data-stu-id="59cc7-118">c\[ 10 \] ( = c10 )</span></span>              |
| <span data-ttu-id="59cc7-119">R \[ A \]</span><span class="sxs-lookup"><span data-stu-id="59cc7-119">R\[ A \]</span></span>                                  | <span data-ttu-id="59cc7-120">A</span><span class="sxs-lookup"><span data-stu-id="59cc7-120">A</span></span>                                     | <span data-ttu-id="59cc7-121">c \[ a0. y \]</span><span class="sxs-lookup"><span data-stu-id="59cc7-121">c\[ a0.y \]</span></span>                      |
| <span data-ttu-id="59cc7-122">Ать \[ N0 +... + Ni + A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="59cc7-122">Rk\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span> | <span data-ttu-id="59cc7-123">A + k + N0 +... + Ni + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="59cc7-123">A + k + n0 + ... + ni + m0 + ... + mj</span></span> | <span data-ttu-id="59cc7-124">C8 \[ 3 + 2 + a0. w + 5 + 6 + 1 \]</span><span class="sxs-lookup"><span data-stu-id="59cc7-124">c8\[ 3 + 2 + a0.w + 5 + 6 + 1 \]</span></span> |
| <span data-ttu-id="59cc7-125">R \[ N0 +... + Ni + A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="59cc7-125">R\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span>  | <span data-ttu-id="59cc7-126">A + N0 +... + Ni + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="59cc7-126">A + n0 + ... + ni + m0 + ... + mj</span></span>     | <span data-ttu-id="59cc7-127">c \[ 2 + 1 + Al + 3 + 4 + 5 \]</span><span class="sxs-lookup"><span data-stu-id="59cc7-127">c\[ 2 + 1 + aL + 3 + 4 + 5 \]</span></span>    |
| <span data-ttu-id="59cc7-128">Ать \[ A \]</span><span class="sxs-lookup"><span data-stu-id="59cc7-128">Rk\[ A \]</span></span>                                 | <span data-ttu-id="59cc7-129">A + k</span><span class="sxs-lookup"><span data-stu-id="59cc7-129">A + k</span></span>                                 | <span data-ttu-id="59cc7-130">C12 \[ Al \] , C0 \[ a0. z \]</span><span class="sxs-lookup"><span data-stu-id="59cc7-130">c12\[ aL \], c0\[ a0.z \]</span></span>        |
| <span data-ttu-id="59cc7-131">Ать \[ A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="59cc7-131">Rk\[ A + m0 + ... + mj \]</span></span>                 | <span data-ttu-id="59cc7-132">A + k + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="59cc7-132">A + k + m0 + ... + mj</span></span>                 | <span data-ttu-id="59cc7-133">v1 \[ Al + 4 + 8 \]</span><span class="sxs-lookup"><span data-stu-id="59cc7-133">v1\[ aL + 4 + 8 \]</span></span>               |
| <span data-ttu-id="59cc7-134">R \[ N0 +... + Ni + A \]</span><span class="sxs-lookup"><span data-stu-id="59cc7-134">R\[ n0 + ... + ni + A \]</span></span>                  | <span data-ttu-id="59cc7-135">A + N0 +... + Ni</span><span class="sxs-lookup"><span data-stu-id="59cc7-135">A + n0 + ... + ni</span></span>                     | <span data-ttu-id="59cc7-136">o \[ 3 + 1 + Al \]</span><span class="sxs-lookup"><span data-stu-id="59cc7-136">o\[ 3 + 1 + aL \]</span></span>                |
| <span data-ttu-id="59cc7-137">Ать \[ N0 +... + Ni + A \]</span><span class="sxs-lookup"><span data-stu-id="59cc7-137">Rk\[ n0 + ... + ni + A \]</span></span>                 | <span data-ttu-id="59cc7-138">A + k + N0 +... + Ni</span><span class="sxs-lookup"><span data-stu-id="59cc7-138">A + k + n0 + ... + ni</span></span>                 | <span data-ttu-id="59cc7-139">O1 \[ 2 + 1 + 3 + Al \]</span><span class="sxs-lookup"><span data-stu-id="59cc7-139">o1\[ 2 + 1 + 3 + aL \]</span></span>           |



 

<span data-ttu-id="59cc7-140">Регистры доступны в следующих версиях:</span><span class="sxs-lookup"><span data-stu-id="59cc7-140">The registers are available in the following versions:</span></span>



| <span data-ttu-id="59cc7-141">Тип регистра</span><span class="sxs-lookup"><span data-stu-id="59cc7-141">Register type</span></span> | <span data-ttu-id="59cc7-142">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="59cc7-142">Vertex Shader Versions</span></span> |
|---------------|------------------------|
| <span data-ttu-id="59cc7-143">a0</span><span class="sxs-lookup"><span data-stu-id="59cc7-143">a0</span></span>            | <span data-ttu-id="59cc7-144">Все</span><span class="sxs-lookup"><span data-stu-id="59cc7-144">All</span></span>                    |
| <span data-ttu-id="59cc7-145">aL</span><span class="sxs-lookup"><span data-stu-id="59cc7-145">aL</span></span>            | <span data-ttu-id="59cc7-146">VS \_ 2 \_ 0 и выше</span><span class="sxs-lookup"><span data-stu-id="59cc7-146">vs\_2\_0 and higher</span></span>    |
| <span data-ttu-id="59cc7-147">cn</span><span class="sxs-lookup"><span data-stu-id="59cc7-147">cn</span></span>            | <span data-ttu-id="59cc7-148">VS \_ 1 \_ и выше</span><span class="sxs-lookup"><span data-stu-id="59cc7-148">vs\_1\_1 and higher</span></span>    |
| <span data-ttu-id="59cc7-149">on</span><span class="sxs-lookup"><span data-stu-id="59cc7-149">on</span></span>            | <span data-ttu-id="59cc7-150">VS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="59cc7-150">vs\_3\_0</span></span>               |



 

## <a name="related-topics"></a><span data-ttu-id="59cc7-151">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="59cc7-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59cc7-152">Регистры шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="59cc7-152">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




