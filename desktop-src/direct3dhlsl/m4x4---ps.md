---
title: m4x4-PS
description: Умножает вектор с 4 компонентами на матрицу 4x4. | m4x4-PS
ms.assetid: 2a9915a3-f396-4108-97f7-d70c5262ff59
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 93f2da73c45151f5287f3acf773efb4bd57d21e1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986424"
---
# <a name="m4x4---ps"></a><span data-ttu-id="4fbd5-104">m4x4-PS</span><span class="sxs-lookup"><span data-stu-id="4fbd5-104">m4x4 - ps</span></span>

<span data-ttu-id="4fbd5-105">Умножает вектор с 4 компонентами на матрицу 4x4.</span><span class="sxs-lookup"><span data-stu-id="4fbd5-105">Multiplies a 4-component vector by a 4x4 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fbd5-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4fbd5-106">Syntax</span></span>



| <span data-ttu-id="4fbd5-107">m4x4 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="4fbd5-107">m4x4 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="4fbd5-108">где</span><span class="sxs-lookup"><span data-stu-id="4fbd5-108">where</span></span>

-   <span data-ttu-id="4fbd5-109">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="4fbd5-109">dst is the destination register.</span></span> <span data-ttu-id="4fbd5-110">Result является вектором из 4 компонентов.</span><span class="sxs-lookup"><span data-stu-id="4fbd5-110">Result is a 4-component vector.</span></span>
-   <span data-ttu-id="4fbd5-111">src0 — это исходный регистр, представляющий 4-компонентный вектор.</span><span class="sxs-lookup"><span data-stu-id="4fbd5-111">src0 is a source register representing a 4-component vector.</span></span>
-   <span data-ttu-id="4fbd5-112">src1 — это исходный регистр, представляющий матрицу 4x4, которая соответствует первому из четырех последовательных регистров.</span><span class="sxs-lookup"><span data-stu-id="4fbd5-112">src1 is a source register representing a 4x4 matrix, which corresponds to the first of 4 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fbd5-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="4fbd5-113">Remarks</span></span>



| <span data-ttu-id="4fbd5-114">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="4fbd5-114">Pixel shader versions</span></span> | <span data-ttu-id="4fbd5-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="4fbd5-115">1\_1</span></span> | <span data-ttu-id="4fbd5-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="4fbd5-116">1\_2</span></span> | <span data-ttu-id="4fbd5-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="4fbd5-117">1\_3</span></span> | <span data-ttu-id="4fbd5-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="4fbd5-118">1\_4</span></span> | <span data-ttu-id="4fbd5-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4fbd5-119">2\_0</span></span> | <span data-ttu-id="4fbd5-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="4fbd5-120">2\_x</span></span> | <span data-ttu-id="4fbd5-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4fbd5-121">2\_sw</span></span> | <span data-ttu-id="4fbd5-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4fbd5-122">3\_0</span></span> | <span data-ttu-id="4fbd5-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4fbd5-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="4fbd5-124">m4x4</span><span class="sxs-lookup"><span data-stu-id="4fbd5-124">m4x4</span></span>                  |      |      |      |      | <span data-ttu-id="4fbd5-125">x</span><span class="sxs-lookup"><span data-stu-id="4fbd5-125">x</span></span>    | <span data-ttu-id="4fbd5-126">x</span><span class="sxs-lookup"><span data-stu-id="4fbd5-126">x</span></span>    | <span data-ttu-id="4fbd5-127">x</span><span class="sxs-lookup"><span data-stu-id="4fbd5-127">x</span></span>     | <span data-ttu-id="4fbd5-128">x</span><span class="sxs-lookup"><span data-stu-id="4fbd5-128">x</span></span>    | <span data-ttu-id="4fbd5-129">x</span><span class="sxs-lookup"><span data-stu-id="4fbd5-129">x</span></span>     |



 

<span data-ttu-id="4fbd5-130">Для регистра назначения требуется маска ксизв (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="4fbd5-130">The xyzw (default) mask is required for the destination register.</span></span> <span data-ttu-id="4fbd5-131">Модификаторы отрицания и свиззле разрешены для src0, но не для src1.</span><span class="sxs-lookup"><span data-stu-id="4fbd5-131">Negate and swizzle modifiers are allowed for src0, but not for src1.</span></span>

<span data-ttu-id="4fbd5-132">Модификаторы свиззле и отрицания недопустимы для регистра src0.</span><span class="sxs-lookup"><span data-stu-id="4fbd5-132">Swizzle and negate modifiers are invalid for the src0 register.</span></span> <span data-ttu-id="4fbd5-133">Регистры DST и src0 не могут совпадать.</span><span class="sxs-lookup"><span data-stu-id="4fbd5-133">The dst and src0 registers cannot be the same.</span></span>

<span data-ttu-id="4fbd5-134">В следующем фрагменте кода показаны выполняемые операции.</span><span class="sxs-lookup"><span data-stu-id="4fbd5-134">The following code snippet shows the operations performed.</span></span>


```
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z) + (src0.w*src1.w);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z) + (src0.w*src2.w);
dest.z = (src0.x*src3.x) + (src0.y*src3.y) + (src0.z*src3.z) + (src0.w*src3.w);
dest.w = (src0.x*src4.x) + (src0.y*src4.y) + (src0.z*src4.z) + (src0.w*src4.w);
```



<span data-ttu-id="4fbd5-135">Входной вектор находится в регистре src0.</span><span class="sxs-lookup"><span data-stu-id="4fbd5-135">The input vector is in register src0.</span></span> <span data-ttu-id="4fbd5-136">Матрица входных данных 4x4 находится в регистре src1 и следующих трех старших регистров, как показано в расширении ниже.</span><span class="sxs-lookup"><span data-stu-id="4fbd5-136">The input 4x4 matrix is in register src1, and the next three higher registers, as shown in the expansion below.</span></span>

<span data-ttu-id="4fbd5-137">Эта операция обычно используется для преобразования расположения матрицей проекции.</span><span class="sxs-lookup"><span data-stu-id="4fbd5-137">This operation is commonly used for transforming a position by a projection matrix.</span></span> <span data-ttu-id="4fbd5-138">Эта инструкция реализуется как набор изделий с точками, как показано здесь.</span><span class="sxs-lookup"><span data-stu-id="4fbd5-138">This instruction is implemented as a set of dot products as shown here.</span></span>


```
m4x4   r0.xyzw, r1, c0    will be expanded to:

dp4   r0.x, r1, c0
dp4   r0.y, r1, c1
dp4   r0.z, r1, c2
dp4   r0.w, r1, c3
```



## <a name="related-topics"></a><span data-ttu-id="4fbd5-139">См. также</span><span class="sxs-lookup"><span data-stu-id="4fbd5-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4fbd5-140">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="4fbd5-140">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




