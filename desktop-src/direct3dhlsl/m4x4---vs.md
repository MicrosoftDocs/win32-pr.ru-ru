---
title: m4x4 — VS
description: Умножает вектор с 4 компонентами на матрицу 4x4. | m4x4 — VS
ms.assetid: 016100ac-e316-41fd-a606-271be7394a1a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 846802f46cd829b3e610ec016a546c5302895bd9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273454"
---
# <a name="m4x4---vs"></a><span data-ttu-id="5c2d0-104">m4x4 — VS</span><span class="sxs-lookup"><span data-stu-id="5c2d0-104">m4x4 - vs</span></span>

<span data-ttu-id="5c2d0-105">Умножает вектор с 4 компонентами на матрицу 4x4.</span><span class="sxs-lookup"><span data-stu-id="5c2d0-105">Multiplies a 4-component vector by a 4x4 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c2d0-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5c2d0-106">Syntax</span></span>



| <span data-ttu-id="5c2d0-107">m4x4 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="5c2d0-107">m4x4 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="5c2d0-108">где</span><span class="sxs-lookup"><span data-stu-id="5c2d0-108">where</span></span>

-   <span data-ttu-id="5c2d0-109">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="5c2d0-109">dst is the destination register.</span></span> <span data-ttu-id="5c2d0-110">Result является вектором из 4 компонентов.</span><span class="sxs-lookup"><span data-stu-id="5c2d0-110">Result is a 4-component vector.</span></span>
-   <span data-ttu-id="5c2d0-111">src0 — это исходный регистр, представляющий 4-компонентный вектор.</span><span class="sxs-lookup"><span data-stu-id="5c2d0-111">src0 is a source register representing a 4-component vector.</span></span>
-   <span data-ttu-id="5c2d0-112">src1 — это исходный регистр, представляющий матрицу 4x4, которая соответствует первому из четырех последовательных регистров.</span><span class="sxs-lookup"><span data-stu-id="5c2d0-112">src1 is a source register representing a 4x4 matrix, which corresponds to the first of 4 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c2d0-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="5c2d0-113">Remarks</span></span>



| <span data-ttu-id="5c2d0-114">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="5c2d0-114">Vertex shader versions</span></span> | <span data-ttu-id="5c2d0-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="5c2d0-115">1\_1</span></span> | <span data-ttu-id="5c2d0-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5c2d0-116">2\_0</span></span> | <span data-ttu-id="5c2d0-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5c2d0-117">2\_x</span></span> | <span data-ttu-id="5c2d0-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5c2d0-118">2\_sw</span></span> | <span data-ttu-id="5c2d0-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5c2d0-119">3\_0</span></span> | <span data-ttu-id="5c2d0-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5c2d0-120">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="5c2d0-121">m4x4</span><span class="sxs-lookup"><span data-stu-id="5c2d0-121">m4x4</span></span>                   | <span data-ttu-id="5c2d0-122">x</span><span class="sxs-lookup"><span data-stu-id="5c2d0-122">x</span></span>    | <span data-ttu-id="5c2d0-123">x</span><span class="sxs-lookup"><span data-stu-id="5c2d0-123">x</span></span>    | <span data-ttu-id="5c2d0-124">x</span><span class="sxs-lookup"><span data-stu-id="5c2d0-124">x</span></span>    | <span data-ttu-id="5c2d0-125">x</span><span class="sxs-lookup"><span data-stu-id="5c2d0-125">x</span></span>     | <span data-ttu-id="5c2d0-126">x</span><span class="sxs-lookup"><span data-stu-id="5c2d0-126">x</span></span>    | <span data-ttu-id="5c2d0-127">x</span><span class="sxs-lookup"><span data-stu-id="5c2d0-127">x</span></span>     |



 

<span data-ttu-id="5c2d0-128">Для регистра назначения требуется маска ксизв (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="5c2d0-128">The xyzw (default) mask is required for the destination register.</span></span> <span data-ttu-id="5c2d0-129">Модификаторы отрицания и свиззле разрешены для src0, но не для src1.</span><span class="sxs-lookup"><span data-stu-id="5c2d0-129">Negate and swizzle modifiers are allowed for src0, but not for src1.</span></span>

<span data-ttu-id="5c2d0-130">Модификаторы свиззле и отрицания недопустимы для регистра src0.</span><span class="sxs-lookup"><span data-stu-id="5c2d0-130">Swizzle and negate modifiers are invalid for the src0 register.</span></span> <span data-ttu-id="5c2d0-131">Регистры dest и src0 не могут совпадать.</span><span class="sxs-lookup"><span data-stu-id="5c2d0-131">The dest and src0 registers cannot be the same.</span></span>

<span data-ttu-id="5c2d0-132">В следующем фрагменте кода показаны выполняемые операции.</span><span class="sxs-lookup"><span data-stu-id="5c2d0-132">The following code fragment shows the operations performed.</span></span>


```
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z) + 
        (src0.w * src1.w);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z) + 
        (src0.w * src2.w);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z) + 
        (src0.w * src3.w);
dest.w = (src0.x * src4.x) + (src0.y * src4.y) + (src0.z * src4.z) + 
        (src0.w * src4.w);
```



<span data-ttu-id="5c2d0-133">Входной вектор находится в регистре src0.</span><span class="sxs-lookup"><span data-stu-id="5c2d0-133">The input vector is in register src0.</span></span> <span data-ttu-id="5c2d0-134">Матрица входных данных 4x4 находится в регистре src1 и следующих трех старших регистров, как показано в расширении ниже.</span><span class="sxs-lookup"><span data-stu-id="5c2d0-134">The input 4x4 matrix is in register src1, and the next three higher registers, as shown in the expansion below.</span></span>

<span data-ttu-id="5c2d0-135">Эта операция обычно используется для преобразования расположения матрицей проекции.</span><span class="sxs-lookup"><span data-stu-id="5c2d0-135">This operation is commonly used for transforming a position by a projection matrix.</span></span> <span data-ttu-id="5c2d0-136">Эта инструкция реализована в виде серии изделий с точками, как показано здесь.</span><span class="sxs-lookup"><span data-stu-id="5c2d0-136">This instruction is implemented as a series of dot products as shown here.</span></span>


```
m4x4   r0.xyzw, r1, c0    will be expanded to:

dp4   r0.x, r1, c0
dp4   r0.y, r1, c1
dp4   r0.z, r1, c2
dp4   r0.w, r1, c3
```



## <a name="related-topics"></a><span data-ttu-id="5c2d0-137">См. также</span><span class="sxs-lookup"><span data-stu-id="5c2d0-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c2d0-138">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="5c2d0-138">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




