---
title: m4x3-PS
description: Умножает вектор с 4 компонентами на матрицу 4x3. | m4x3-PS
ms.assetid: cf9ae4c3-6cdf-4c6f-b34c-0ebd3c8a4123
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7787268906c2c9e92dc1e3fa1ec87c4af3079255
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986628"
---
# <a name="m4x3---ps"></a><span data-ttu-id="aa825-104">m4x3-PS</span><span class="sxs-lookup"><span data-stu-id="aa825-104">m4x3 - ps</span></span>

<span data-ttu-id="aa825-105">Умножает вектор с 4 компонентами на матрицу 4x3.</span><span class="sxs-lookup"><span data-stu-id="aa825-105">Multiplies a 4-component vector by a 4x3 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa825-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aa825-106">Syntax</span></span>



| <span data-ttu-id="aa825-107">m4x3 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="aa825-107">m4x3 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="aa825-108">где</span><span class="sxs-lookup"><span data-stu-id="aa825-108">where</span></span>

-   <span data-ttu-id="aa825-109">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="aa825-109">dst is the destination register.</span></span> <span data-ttu-id="aa825-110">Result является вектором из трех компонентов.</span><span class="sxs-lookup"><span data-stu-id="aa825-110">Result is a 3-component vector.</span></span>
-   <span data-ttu-id="aa825-111">src0 — это исходный регистр, представляющий 4-компонентный вектор.</span><span class="sxs-lookup"><span data-stu-id="aa825-111">src0 is a source register representing a 4-component vector.</span></span>
-   <span data-ttu-id="aa825-112">src1 — это исходный регистр, представляющий матрицу 4x3, которая соответствует первому из трех последовательных регистров.</span><span class="sxs-lookup"><span data-stu-id="aa825-112">src1 is a source register representing a 4x3 matrix, which corresponds to the first of 3 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa825-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="aa825-113">Remarks</span></span>



| <span data-ttu-id="aa825-114">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="aa825-114">Pixel shader versions</span></span> | <span data-ttu-id="aa825-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="aa825-115">1\_1</span></span> | <span data-ttu-id="aa825-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="aa825-116">1\_2</span></span> | <span data-ttu-id="aa825-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="aa825-117">1\_3</span></span> | <span data-ttu-id="aa825-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="aa825-118">1\_4</span></span> | <span data-ttu-id="aa825-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="aa825-119">2\_0</span></span> | <span data-ttu-id="aa825-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="aa825-120">2\_x</span></span> | <span data-ttu-id="aa825-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="aa825-121">2\_sw</span></span> | <span data-ttu-id="aa825-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="aa825-122">3\_0</span></span> | <span data-ttu-id="aa825-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="aa825-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="aa825-124">m4x3</span><span class="sxs-lookup"><span data-stu-id="aa825-124">m4x3</span></span>                  |      |      |      |      | <span data-ttu-id="aa825-125">x</span><span class="sxs-lookup"><span data-stu-id="aa825-125">x</span></span>    | <span data-ttu-id="aa825-126">x</span><span class="sxs-lookup"><span data-stu-id="aa825-126">x</span></span>    | <span data-ttu-id="aa825-127">x</span><span class="sxs-lookup"><span data-stu-id="aa825-127">x</span></span>     | <span data-ttu-id="aa825-128">x</span><span class="sxs-lookup"><span data-stu-id="aa825-128">x</span></span>    | <span data-ttu-id="aa825-129">x</span><span class="sxs-lookup"><span data-stu-id="aa825-129">x</span></span>     |



 

<span data-ttu-id="aa825-130">Для регистра назначения требуется маска XYZ.</span><span class="sxs-lookup"><span data-stu-id="aa825-130">The xyz mask is required for the destination register.</span></span> <span data-ttu-id="aa825-131">Модификаторы отрицания и свиззле разрешены для src0, но не для src1.</span><span class="sxs-lookup"><span data-stu-id="aa825-131">Negate and swizzle modifiers are allowed for src0, but not for src1.</span></span>

<span data-ttu-id="aa825-132">В следующем фрагменте кода показаны выполняемые операции.</span><span class="sxs-lookup"><span data-stu-id="aa825-132">The following code snippet shows the operations performed.</span></span>


```
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z) + (src0.w*src1.w);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z) + (src0.w*src2.w);
dest.z = (src0.x*src3.x) + (src0.y*src3.y) + (src0.z*src3.z) + (src0.w*src3.w);
```



<span data-ttu-id="aa825-133">Входной вектор находится в регистре src0.</span><span class="sxs-lookup"><span data-stu-id="aa825-133">The input vector is in register src0.</span></span> <span data-ttu-id="aa825-134">Входная матрица 4x3 находится в регистре src1 и следующих двух старших регистров, как показано в расширении ниже.</span><span class="sxs-lookup"><span data-stu-id="aa825-134">The input 4x3 matrix is in register src1, and the next two higher registers, as shown in the expansion below.</span></span> <span data-ttu-id="aa825-135">Создается объемный результат, при этом другой элемент регистр назначения (dest. w) не затронут.</span><span class="sxs-lookup"><span data-stu-id="aa825-135">A 3D result is produced, leaving the other element of the destination register (dest.w) unaffected.</span></span>

<span data-ttu-id="aa825-136">Эта операция обычно используется для преобразования вектора расположения матрицы, не имеющей пошаговых эффектов, например, в преобразованиях пространства модели.</span><span class="sxs-lookup"><span data-stu-id="aa825-136">This operation is commonly used for transforming a position vector by a matrix that has no projective effect, such as occurs in model-space transformations.</span></span> <span data-ttu-id="aa825-137">Эта инструкция реализована в виде набора изделий с точками, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="aa825-137">This instruction is implemented as a set of dot products as shown below.</span></span>


```
m4x3   r0.xyz, r1, c0    will be expanded to:

dp4   r0.x, r1, c0
dp4   r0.y, r1, c1
dp4   r0.z, r1, c2
```



<span data-ttu-id="aa825-138">Модификаторы свиззле и отрицания недопустимы для регистра src1.</span><span class="sxs-lookup"><span data-stu-id="aa825-138">Swizzle and negate modifiers are invalid for the src1 register.</span></span> <span data-ttu-id="aa825-139">Регистр летнего времени и src0 не могут совпадать.</span><span class="sxs-lookup"><span data-stu-id="aa825-139">The dst and src0 register cannot be the same.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa825-140">См. также</span><span class="sxs-lookup"><span data-stu-id="aa825-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa825-141">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="aa825-141">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




