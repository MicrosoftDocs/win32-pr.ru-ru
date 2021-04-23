---
title: m3x2-PS
description: Умножает вектор трех компонентов на матрицу 3x2. | m3x2-PS
ms.assetid: a88e6228-a61a-408c-8d89-a5706dd146d5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 26532c78fa829b9c2a41f715b814ee8a0f44c879
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986687"
---
# <a name="m3x2---ps"></a><span data-ttu-id="0d26e-104">m3x2-PS</span><span class="sxs-lookup"><span data-stu-id="0d26e-104">m3x2 - ps</span></span>

<span data-ttu-id="0d26e-105">Умножает вектор трех компонентов на матрицу 3x2.</span><span class="sxs-lookup"><span data-stu-id="0d26e-105">Multiplies a 3-component vector by a 3x2 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d26e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0d26e-106">Syntax</span></span>



| <span data-ttu-id="0d26e-107">m3x2 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="0d26e-107">m3x2 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="0d26e-108">где</span><span class="sxs-lookup"><span data-stu-id="0d26e-108">where</span></span>

-   <span data-ttu-id="0d26e-109">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="0d26e-109">dst is the destination register.</span></span> <span data-ttu-id="0d26e-110">Result является вектором из двух компонентов.</span><span class="sxs-lookup"><span data-stu-id="0d26e-110">Result is a 2-component vector.</span></span>
-   <span data-ttu-id="0d26e-111">src0 — это исходный регистр, представляющий 3-компонентный вектор.</span><span class="sxs-lookup"><span data-stu-id="0d26e-111">src0 is a source register representing a 3-component vector.</span></span>
-   <span data-ttu-id="0d26e-112">src1 — это исходный регистр, представляющий матрицу 3x2, которая соответствует первому из двух последовательных регистров.</span><span class="sxs-lookup"><span data-stu-id="0d26e-112">src1 is a source register representing a 3x2 matrix, which corresponds to the first of 2 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d26e-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="0d26e-113">Remarks</span></span>



| <span data-ttu-id="0d26e-114">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="0d26e-114">Pixel shader versions</span></span> | <span data-ttu-id="0d26e-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="0d26e-115">1\_1</span></span> | <span data-ttu-id="0d26e-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="0d26e-116">1\_2</span></span> | <span data-ttu-id="0d26e-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="0d26e-117">1\_3</span></span> | <span data-ttu-id="0d26e-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="0d26e-118">1\_4</span></span> | <span data-ttu-id="0d26e-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0d26e-119">2\_0</span></span> | <span data-ttu-id="0d26e-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="0d26e-120">2\_x</span></span> | <span data-ttu-id="0d26e-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0d26e-121">2\_sw</span></span> | <span data-ttu-id="0d26e-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0d26e-122">3\_0</span></span> | <span data-ttu-id="0d26e-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0d26e-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="0d26e-124">m3x2</span><span class="sxs-lookup"><span data-stu-id="0d26e-124">m3x2</span></span>                  |      |      |      |      | <span data-ttu-id="0d26e-125">x</span><span class="sxs-lookup"><span data-stu-id="0d26e-125">x</span></span>    | <span data-ttu-id="0d26e-126">x</span><span class="sxs-lookup"><span data-stu-id="0d26e-126">x</span></span>    | <span data-ttu-id="0d26e-127">x</span><span class="sxs-lookup"><span data-stu-id="0d26e-127">x</span></span>     | <span data-ttu-id="0d26e-128">x</span><span class="sxs-lookup"><span data-stu-id="0d26e-128">x</span></span>    | <span data-ttu-id="0d26e-129">x</span><span class="sxs-lookup"><span data-stu-id="0d26e-129">x</span></span>     |



 

<span data-ttu-id="0d26e-130">Для регистрации назначения требуется маска XY.</span><span class="sxs-lookup"><span data-stu-id="0d26e-130">The xy mask is required for the destination register.</span></span> <span data-ttu-id="0d26e-131">Модификаторы отрицания и свиззле разрешены для src0, но не для src1.</span><span class="sxs-lookup"><span data-stu-id="0d26e-131">Negate and swizzle modifiers are allowed for src0 but not for src1.</span></span>

<span data-ttu-id="0d26e-132">В следующих уравнениях показано, как работает инструкция.</span><span class="sxs-lookup"><span data-stu-id="0d26e-132">The following equations show how the instruction operates:</span></span>


```
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z);
```



<span data-ttu-id="0d26e-133">Входной вектор находится в регистре src0.</span><span class="sxs-lookup"><span data-stu-id="0d26e-133">The input vector is in register src0.</span></span> <span data-ttu-id="0d26e-134">Входная матрица 3x2 находится в регистре src1 и следующем более высоком регистре в том же файле регистрации, как показано в следующем развертывании.</span><span class="sxs-lookup"><span data-stu-id="0d26e-134">The input 3x2 matrix is in register src1 and the next higher register in the same register file, as shown in the following expansion.</span></span> <span data-ttu-id="0d26e-135">Создается 2D-результат, в результате чего остальные элементы регистра назначения (dest. z и dest. w) не затрагиваются.</span><span class="sxs-lookup"><span data-stu-id="0d26e-135">A 2D result is produced, leaving the other elements of the destination register (dest.z and dest.w) unaffected.</span></span>

<span data-ttu-id="0d26e-136">Эта операция обычно используется для двумерных преобразований.</span><span class="sxs-lookup"><span data-stu-id="0d26e-136">This operation is commonly used for 2D transforms.</span></span> <span data-ttu-id="0d26e-137">Эта инструкция реализуется как пара изделий с точками, как показано здесь.</span><span class="sxs-lookup"><span data-stu-id="0d26e-137">This instruction is implemented as a pair of dot products as shown here.</span></span>


```
m3x2   r0.xy, r1, c0   which will be expanded to:

dp3   r0.x, r1, c0
dp3   r0.y, r1, c1
```



<span data-ttu-id="0d26e-138">Модификаторы свиззле и отрицания недопустимы для регистра src1.</span><span class="sxs-lookup"><span data-stu-id="0d26e-138">Swizzle and negate modifiers are invalid for the src1 register.</span></span> <span data-ttu-id="0d26e-139">Регистр летнего времени и src0 или любой из src1 + i не могут быть одинаковыми.</span><span class="sxs-lookup"><span data-stu-id="0d26e-139">The dst and src0 register, or any of src1+i registers, cannot be the same.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d26e-140">См. также</span><span class="sxs-lookup"><span data-stu-id="0d26e-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d26e-141">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="0d26e-141">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




