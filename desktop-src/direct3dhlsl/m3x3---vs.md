---
title: m3x3 — VS
description: Умножает вектор трех компонентов на матрицу 3X3. | m3x3 — VS
ms.assetid: 6a749ed0-097d-4354-bc70-fbcd879eafab
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e75cdb4b098b92ea358c32e40b3948c7ac73e0cf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104424269"
---
# <a name="m3x3---vs"></a><span data-ttu-id="9a5d1-104">m3x3 — VS</span><span class="sxs-lookup"><span data-stu-id="9a5d1-104">m3x3 - vs</span></span>

<span data-ttu-id="9a5d1-105">Умножает вектор трех компонентов на матрицу 3X3.</span><span class="sxs-lookup"><span data-stu-id="9a5d1-105">Multiplies a 3-component vector by a 3x3 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a5d1-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9a5d1-106">Syntax</span></span>



| <span data-ttu-id="9a5d1-107">m3x3 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="9a5d1-107">m3x3 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="9a5d1-108">где</span><span class="sxs-lookup"><span data-stu-id="9a5d1-108">where</span></span>

-   <span data-ttu-id="9a5d1-109">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="9a5d1-109">dst is the destination register.</span></span> <span data-ttu-id="9a5d1-110">Result является вектором из трех компонентов.</span><span class="sxs-lookup"><span data-stu-id="9a5d1-110">Result is a 3-component vector.</span></span>
-   <span data-ttu-id="9a5d1-111">src0 — это исходный регистр, представляющий 3-компонентный вектор.</span><span class="sxs-lookup"><span data-stu-id="9a5d1-111">src0 is a source register representing a 3-component vector.</span></span>
-   <span data-ttu-id="9a5d1-112">src1 — это исходный регистр, представляющий матрицу 3x3, которая соответствует первому из трех последовательных регистров.</span><span class="sxs-lookup"><span data-stu-id="9a5d1-112">src1 is a source register representing a 3x3 matrix, which corresponds to the first of 3 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a5d1-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="9a5d1-113">Remarks</span></span>



| <span data-ttu-id="9a5d1-114">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="9a5d1-114">Vertex shader versions</span></span> | <span data-ttu-id="9a5d1-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="9a5d1-115">1\_1</span></span> | <span data-ttu-id="9a5d1-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9a5d1-116">2\_0</span></span> | <span data-ttu-id="9a5d1-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="9a5d1-117">2\_x</span></span> | <span data-ttu-id="9a5d1-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="9a5d1-118">2\_sw</span></span> | <span data-ttu-id="9a5d1-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9a5d1-119">3\_0</span></span> | <span data-ttu-id="9a5d1-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="9a5d1-120">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="9a5d1-121">m3x3</span><span class="sxs-lookup"><span data-stu-id="9a5d1-121">m3x3</span></span>                   | <span data-ttu-id="9a5d1-122">x</span><span class="sxs-lookup"><span data-stu-id="9a5d1-122">x</span></span>    | <span data-ttu-id="9a5d1-123">x</span><span class="sxs-lookup"><span data-stu-id="9a5d1-123">x</span></span>    | <span data-ttu-id="9a5d1-124">x</span><span class="sxs-lookup"><span data-stu-id="9a5d1-124">x</span></span>    | <span data-ttu-id="9a5d1-125">x</span><span class="sxs-lookup"><span data-stu-id="9a5d1-125">x</span></span>     | <span data-ttu-id="9a5d1-126">x</span><span class="sxs-lookup"><span data-stu-id="9a5d1-126">x</span></span>    | <span data-ttu-id="9a5d1-127">x</span><span class="sxs-lookup"><span data-stu-id="9a5d1-127">x</span></span>     |



 

<span data-ttu-id="9a5d1-128">Для регистра назначения требуется маска XYZ.</span><span class="sxs-lookup"><span data-stu-id="9a5d1-128">The xyz mask is required for the destination register.</span></span> <span data-ttu-id="9a5d1-129">Модификаторы отрицания и свиззле разрешены для src0, но не для src1.</span><span class="sxs-lookup"><span data-stu-id="9a5d1-129">Negate and swizzle modifiers are allowed for src0 but not for src1.</span></span>

<span data-ttu-id="9a5d1-130">В следующем фрагменте кода показаны выполняемые операции.</span><span class="sxs-lookup"><span data-stu-id="9a5d1-130">The following code fragment shows the operations performed.</span></span>


```
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z);
```



<span data-ttu-id="9a5d1-131">Входной вектор находится в регистре src0.</span><span class="sxs-lookup"><span data-stu-id="9a5d1-131">The input vector is in register src0.</span></span> <span data-ttu-id="9a5d1-132">Входная матрица 3x3 находится в регистре src1 и следующих двух старших регистров, как показано в расширении ниже.</span><span class="sxs-lookup"><span data-stu-id="9a5d1-132">The input 3x3 matrix is in register src1, and the next two higher registers, as shown in the expansion below.</span></span> <span data-ttu-id="9a5d1-133">Создается объемный результат, при этом другой элемент регистр назначения (dest. w) не затронут.</span><span class="sxs-lookup"><span data-stu-id="9a5d1-133">A 3D result is produced, leaving the other element of the destination register (dest.w) unaffected.</span></span>

<span data-ttu-id="9a5d1-134">Эта операция обычно используется для преобразования обычных векторов во время вычислений освещения.</span><span class="sxs-lookup"><span data-stu-id="9a5d1-134">This operation is commonly used for transforming normal vectors during lighting computations.</span></span> <span data-ttu-id="9a5d1-135">Эта инструкция реализуется как пара изделий с точками, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="9a5d1-135">This instruction is implemented as a pair of dot products as shown below.</span></span>


```
m3x3 r0.xyz, r1, c0  which will be expanded to:

dp3   r0.x, r1, c0
dp3   r0.y, r1, c1
dp3   r0.z, r1, c2
```



## <a name="related-topics"></a><span data-ttu-id="9a5d1-136">См. также</span><span class="sxs-lookup"><span data-stu-id="9a5d1-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a5d1-137">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="9a5d1-137">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




