---
title: Относительная адресация (Справочник по HLSL VS)
description: Синтаксис \ \ можно использовать только в типах регистров, которые могут быть сравнительно устранены в некоторых моделях шейдеров.
ms.assetid: 9f9d2499-73a5-4c9d-9dce-94c914933334
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c11d6f6c4b448e1dee5f4237696c110519bc0dd0
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/23/2019
ms.locfileid: "104335675"
---
# <a name="relative-addressing-hlsl-vs-reference"></a><span data-ttu-id="f5700-103">Относительная адресация (Справочник по HLSL VS)</span><span class="sxs-lookup"><span data-stu-id="f5700-103">Relative Addressing (HLSL VS reference)</span></span>

<span data-ttu-id="f5700-104">\[ \] Синтаксис можно использовать только в типах регистров, которые могут быть относительно устранены в некоторых моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="f5700-104">The \[ \] syntax can be used only in register types that can be relatively addressed in certain shader models.</span></span> <span data-ttu-id="f5700-105">Ниже перечислены поддерживаемые формы \[ \] синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="f5700-105">The supported forms of \[ \] syntax are listed as follows:</span></span>

<span data-ttu-id="f5700-106">Где:</span><span class="sxs-lookup"><span data-stu-id="f5700-106">Where:</span></span>

-   <span data-ttu-id="f5700-107">"R" обозначает любой тип регистра, который может быть относительно адресован.</span><span class="sxs-lookup"><span data-stu-id="f5700-107">"R" denotes any register type that can be relatively addressed.</span></span>
-   <span data-ttu-id="f5700-108">"A" обозначает любой регистр, который можно использовать в качестве индекса для относительно других регистров.</span><span class="sxs-lookup"><span data-stu-id="f5700-108">"A" denotes any register that can be used as an index to relatively address other registers.</span></span>
-   <span data-ttu-id="f5700-109">N0 — Ni, M0-MJ и k — целые числа >= 0.</span><span class="sxs-lookup"><span data-stu-id="f5700-109">n0 - ni, m0 - mj, and k are integers >= 0.</span></span>



| <span data-ttu-id="f5700-110">\[\]синтаксис</span><span class="sxs-lookup"><span data-stu-id="f5700-110">\[ \] syntax</span></span>                              | <span data-ttu-id="f5700-111">Эффективный индекс</span><span class="sxs-lookup"><span data-stu-id="f5700-111">Effective index</span></span>                       | <span data-ttu-id="f5700-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="f5700-112">Examples</span></span>                         |
|-------------------------------------------|---------------------------------------|----------------------------------|
| <span data-ttu-id="f5700-113">R \[ A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="f5700-113">R\[ A + m0 + ... + mj \]</span></span>                  | <span data-ttu-id="f5700-114">A + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="f5700-114">A + m0 + ... + mj</span></span>                     | <span data-ttu-id="f5700-115">c \[ a0. x + 3 + 7 \]</span><span class="sxs-lookup"><span data-stu-id="f5700-115">c\[ a0.x + 3 + 7 \]</span></span>              |
| <span data-ttu-id="f5700-116">R \[ k \] (= ать)</span><span class="sxs-lookup"><span data-stu-id="f5700-116">R\[ k \] ( = Rk )</span></span>                         | <span data-ttu-id="f5700-117">k</span><span class="sxs-lookup"><span data-stu-id="f5700-117">k</span></span>                                     | <span data-ttu-id="f5700-118">c \[ 10 \] (= C10)</span><span class="sxs-lookup"><span data-stu-id="f5700-118">c\[ 10 \] ( = c10 )</span></span>              |
| <span data-ttu-id="f5700-119">R \[ A \]</span><span class="sxs-lookup"><span data-stu-id="f5700-119">R\[ A \]</span></span>                                  | <span data-ttu-id="f5700-120">Объект</span><span class="sxs-lookup"><span data-stu-id="f5700-120">A</span></span>                                     | <span data-ttu-id="f5700-121">c \[ a0. y \]</span><span class="sxs-lookup"><span data-stu-id="f5700-121">c\[ a0.y \]</span></span>                      |
| <span data-ttu-id="f5700-122">Ать \[ N0 +... + Ni + A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="f5700-122">Rk\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span> | <span data-ttu-id="f5700-123">A + k + N0 +... + Ni + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="f5700-123">A + k + n0 + ... + ni + m0 + ... + mj</span></span> | <span data-ttu-id="f5700-124">C8 \[ 3 + 2 + a0. w + 5 + 6 + 1 \]</span><span class="sxs-lookup"><span data-stu-id="f5700-124">c8\[ 3 + 2 + a0.w + 5 + 6 + 1 \]</span></span> |
| <span data-ttu-id="f5700-125">R \[ N0 +... + Ni + A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="f5700-125">R\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span>  | <span data-ttu-id="f5700-126">A + N0 +... + Ni + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="f5700-126">A + n0 + ... + ni + m0 + ... + mj</span></span>     | <span data-ttu-id="f5700-127">c \[ 2 + 1 + Al + 3 + 4 + 5 \]</span><span class="sxs-lookup"><span data-stu-id="f5700-127">c\[ 2 + 1 + aL + 3 + 4 + 5 \]</span></span>    |
| <span data-ttu-id="f5700-128">Ать \[ A \]</span><span class="sxs-lookup"><span data-stu-id="f5700-128">Rk\[ A \]</span></span>                                 | <span data-ttu-id="f5700-129">A + k</span><span class="sxs-lookup"><span data-stu-id="f5700-129">A + k</span></span>                                 | <span data-ttu-id="f5700-130">C12 \[ Al \] , C0 \[ a0. z \]</span><span class="sxs-lookup"><span data-stu-id="f5700-130">c12\[ aL \], c0\[ a0.z \]</span></span>        |
| <span data-ttu-id="f5700-131">Ать \[ A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="f5700-131">Rk\[ A + m0 + ... + mj \]</span></span>                 | <span data-ttu-id="f5700-132">A + k + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="f5700-132">A + k + m0 + ... + mj</span></span>                 | <span data-ttu-id="f5700-133">v1 \[ Al + 4 + 8 \]</span><span class="sxs-lookup"><span data-stu-id="f5700-133">v1\[ aL + 4 + 8 \]</span></span>               |
| <span data-ttu-id="f5700-134">R \[ N0 +... + Ni + A \]</span><span class="sxs-lookup"><span data-stu-id="f5700-134">R\[ n0 + ... + ni + A \]</span></span>                  | <span data-ttu-id="f5700-135">A + N0 +... + Ni</span><span class="sxs-lookup"><span data-stu-id="f5700-135">A + n0 + ... + ni</span></span>                     | <span data-ttu-id="f5700-136">o \[ 3 + 1 + Al \]</span><span class="sxs-lookup"><span data-stu-id="f5700-136">o\[ 3 + 1 + aL \]</span></span>                |
| <span data-ttu-id="f5700-137">Ать \[ N0 +... + Ni + A \]</span><span class="sxs-lookup"><span data-stu-id="f5700-137">Rk\[ n0 + ... + ni + A \]</span></span>                 | <span data-ttu-id="f5700-138">A + k + N0 +... + Ni</span><span class="sxs-lookup"><span data-stu-id="f5700-138">A + k + n0 + ... + ni</span></span>                 | <span data-ttu-id="f5700-139">O1 \[ 2 + 1 + 3 + Al \]</span><span class="sxs-lookup"><span data-stu-id="f5700-139">o1\[ 2 + 1 + 3 + aL \]</span></span>           |



 

<span data-ttu-id="f5700-140">Регистры доступны в следующих версиях:</span><span class="sxs-lookup"><span data-stu-id="f5700-140">The registers are available in the following versions:</span></span>



| <span data-ttu-id="f5700-141">Тип регистра</span><span class="sxs-lookup"><span data-stu-id="f5700-141">Register type</span></span> | <span data-ttu-id="f5700-142">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="f5700-142">Vertex Shader Versions</span></span> |
|---------------|------------------------|
| <span data-ttu-id="f5700-143">a0</span><span class="sxs-lookup"><span data-stu-id="f5700-143">a0</span></span>            | <span data-ttu-id="f5700-144">Все</span><span class="sxs-lookup"><span data-stu-id="f5700-144">All</span></span>                    |
| <span data-ttu-id="f5700-145">aL</span><span class="sxs-lookup"><span data-stu-id="f5700-145">aL</span></span>            | <span data-ttu-id="f5700-146">VS \_ 2 \_ 0 и выше</span><span class="sxs-lookup"><span data-stu-id="f5700-146">vs\_2\_0 and higher</span></span>    |
| <span data-ttu-id="f5700-147">cn</span><span class="sxs-lookup"><span data-stu-id="f5700-147">cn</span></span>            | <span data-ttu-id="f5700-148">VS \_ 1 \_ и выше</span><span class="sxs-lookup"><span data-stu-id="f5700-148">vs\_1\_1 and higher</span></span>    |
| <span data-ttu-id="f5700-149">on</span><span class="sxs-lookup"><span data-stu-id="f5700-149">on</span></span>            | <span data-ttu-id="f5700-150">VS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f5700-150">vs\_3\_0</span></span>               |



 

## <a name="related-topics"></a><span data-ttu-id="f5700-151">См. также</span><span class="sxs-lookup"><span data-stu-id="f5700-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5700-152">Регистры шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="f5700-152">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




