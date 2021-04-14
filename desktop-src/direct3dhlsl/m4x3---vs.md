---
title: m4x3 — VS
description: Умножает вектор с 4 компонентами на матрицу 4x3. | m4x3 — VS
ms.assetid: 12dd31bd-2078-44a1-912e-72c8f377bc4c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7608b1187cc90cf4914bdd42a197cc6044d53734
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986312"
---
# <a name="m4x3---vs"></a><span data-ttu-id="96b03-104">m4x3 — VS</span><span class="sxs-lookup"><span data-stu-id="96b03-104">m4x3 - vs</span></span>

<span data-ttu-id="96b03-105">Умножает вектор с 4 компонентами на матрицу 4x3.</span><span class="sxs-lookup"><span data-stu-id="96b03-105">Multiplies a 4-component vector by a 4x3 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="96b03-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="96b03-106">Syntax</span></span>



| <span data-ttu-id="96b03-107">m4x3 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="96b03-107">m4x3 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="96b03-108">где</span><span class="sxs-lookup"><span data-stu-id="96b03-108">where</span></span>

-   <span data-ttu-id="96b03-109">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="96b03-109">dst is the destination register.</span></span> <span data-ttu-id="96b03-110">Result является вектором из трех компонентов.</span><span class="sxs-lookup"><span data-stu-id="96b03-110">Result is a 3-component vector.</span></span>
-   <span data-ttu-id="96b03-111">src0 — это исходный регистр, представляющий 4-компонентный вектор.</span><span class="sxs-lookup"><span data-stu-id="96b03-111">src0 is a source register representing a 4-component vector.</span></span>
-   <span data-ttu-id="96b03-112">src1 — это исходный регистр, представляющий матрицу 4x3, которая соответствует первому из трех последовательных регистров.</span><span class="sxs-lookup"><span data-stu-id="96b03-112">src1 is a source register representing a 4x3 matrix, which corresponds to the first of 3 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="96b03-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="96b03-113">Remarks</span></span>



| <span data-ttu-id="96b03-114">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="96b03-114">Vertex shader versions</span></span> | <span data-ttu-id="96b03-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="96b03-115">1\_1</span></span> | <span data-ttu-id="96b03-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="96b03-116">2\_0</span></span> | <span data-ttu-id="96b03-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="96b03-117">2\_x</span></span> | <span data-ttu-id="96b03-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="96b03-118">2\_sw</span></span> | <span data-ttu-id="96b03-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="96b03-119">3\_0</span></span> | <span data-ttu-id="96b03-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="96b03-120">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="96b03-121">m4x3</span><span class="sxs-lookup"><span data-stu-id="96b03-121">m4x3</span></span>                   | <span data-ttu-id="96b03-122">x</span><span class="sxs-lookup"><span data-stu-id="96b03-122">x</span></span>    | <span data-ttu-id="96b03-123">x</span><span class="sxs-lookup"><span data-stu-id="96b03-123">x</span></span>    | <span data-ttu-id="96b03-124">x</span><span class="sxs-lookup"><span data-stu-id="96b03-124">x</span></span>    | <span data-ttu-id="96b03-125">x</span><span class="sxs-lookup"><span data-stu-id="96b03-125">x</span></span>     | <span data-ttu-id="96b03-126">x</span><span class="sxs-lookup"><span data-stu-id="96b03-126">x</span></span>    | <span data-ttu-id="96b03-127">x</span><span class="sxs-lookup"><span data-stu-id="96b03-127">x</span></span>     |



 

<span data-ttu-id="96b03-128">Для регистра назначения требуется маска XYZ.</span><span class="sxs-lookup"><span data-stu-id="96b03-128">The xyz mask is required for the destination register.</span></span> <span data-ttu-id="96b03-129">Модификаторы отрицания и свиззле разрешены для src0, но не для src1.</span><span class="sxs-lookup"><span data-stu-id="96b03-129">Negate and swizzle modifiers are allowed for src0, but not for src1.</span></span>

<span data-ttu-id="96b03-130">В следующем фрагменте кода показаны выполняемые операции.</span><span class="sxs-lookup"><span data-stu-id="96b03-130">The following code fragment shows the operations performed.</span></span>


```
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z) + (src0.w * src1.w);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z) + (src0.w * src2.w);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z) + (src0.w * src3.w);
```



<span data-ttu-id="96b03-131">Входной вектор находится в регистре src0.</span><span class="sxs-lookup"><span data-stu-id="96b03-131">The input vector is in register src0.</span></span> <span data-ttu-id="96b03-132">Входная матрица 4x3 находится в регистре src1 и следующих двух старших регистров, как показано в расширении ниже.</span><span class="sxs-lookup"><span data-stu-id="96b03-132">The input 4x3 matrix is in register src1, and the next two higher registers, as shown in the expansion below.</span></span> <span data-ttu-id="96b03-133">Создается объемный результат, при этом другой элемент регистр назначения (dest. w) не затронут.</span><span class="sxs-lookup"><span data-stu-id="96b03-133">A 3D result is produced, leaving the other element of the destination register (dest.w) unaffected.</span></span>

<span data-ttu-id="96b03-134">Эта операция обычно используется для преобразования вектора расположения матрицы, не имеющей пошаговых эффектов, например, в преобразованиях пространства модели.</span><span class="sxs-lookup"><span data-stu-id="96b03-134">This operation is commonly used for transforming a position vector by a matrix that has no projective effect, such as occurs in model-space transformations.</span></span> <span data-ttu-id="96b03-135">Эта инструкция реализуется как пара изделий с точками, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="96b03-135">This instruction is implemented as a pair of dot products as shown below.</span></span>


```
m4x3   r0.xyz, r1, c0    will be expanded to:

dp4   r0.x, r1, c0
dp4   r0.y, r1, c1
dp4   r0.z, r1, c2
```



<span data-ttu-id="96b03-136">Модификаторы свиззле и отрицания недопустимы для регистра src1.</span><span class="sxs-lookup"><span data-stu-id="96b03-136">Swizzle and negate modifiers are invalid for the src1 register.</span></span> <span data-ttu-id="96b03-137">Регистр летнего времени и src0 не могут совпадать.</span><span class="sxs-lookup"><span data-stu-id="96b03-137">The dst and src0 register cannot be the same.</span></span>

## <a name="related-topics"></a><span data-ttu-id="96b03-138">См. также</span><span class="sxs-lookup"><span data-stu-id="96b03-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96b03-139">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="96b03-139">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




