---
title: m3x2 — VS
description: Умножает вектор трех компонентов на матрицу 3x2. | m3x2 — VS
ms.assetid: 4ef3bd47-3e38-4d9d-a8f5-6ee9c08de69c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 870a8d4918870930faa536ead01dab2947d5faea
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273457"
---
# <a name="m3x2---vs"></a><span data-ttu-id="af51f-104">m3x2 — VS</span><span class="sxs-lookup"><span data-stu-id="af51f-104">m3x2 - vs</span></span>

<span data-ttu-id="af51f-105">Умножает вектор трех компонентов на матрицу 3x2.</span><span class="sxs-lookup"><span data-stu-id="af51f-105">Multiplies a 3-component vector by a 3x2 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="af51f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="af51f-106">Syntax</span></span>



| <span data-ttu-id="af51f-107">m3x2 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="af51f-107">m3x2 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="af51f-108">где</span><span class="sxs-lookup"><span data-stu-id="af51f-108">where</span></span>

-   <span data-ttu-id="af51f-109">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="af51f-109">dst is the destination register.</span></span> <span data-ttu-id="af51f-110">Result является вектором из двух компонентов.</span><span class="sxs-lookup"><span data-stu-id="af51f-110">Result is a 2-component vector.</span></span>
-   <span data-ttu-id="af51f-111">src0 — это исходный регистр, представляющий 3-компонентный вектор.</span><span class="sxs-lookup"><span data-stu-id="af51f-111">src0 is a source register representing a 3-component vector.</span></span>
-   <span data-ttu-id="af51f-112">src1 — это исходный регистр, представляющий матрицу 3x2, которая соответствует первому из двух последовательных регистров.</span><span class="sxs-lookup"><span data-stu-id="af51f-112">src1 is a source register representing a 3x2 matrix, which corresponds to the first of 2 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="af51f-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="af51f-113">Remarks</span></span>



| <span data-ttu-id="af51f-114">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="af51f-114">Vertex shader versions</span></span> | <span data-ttu-id="af51f-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="af51f-115">1\_1</span></span> | <span data-ttu-id="af51f-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="af51f-116">2\_0</span></span> | <span data-ttu-id="af51f-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="af51f-117">2\_x</span></span> | <span data-ttu-id="af51f-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="af51f-118">2\_sw</span></span> | <span data-ttu-id="af51f-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="af51f-119">3\_0</span></span> | <span data-ttu-id="af51f-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="af51f-120">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="af51f-121">m3x2</span><span class="sxs-lookup"><span data-stu-id="af51f-121">m3x2</span></span>                   | <span data-ttu-id="af51f-122">x</span><span class="sxs-lookup"><span data-stu-id="af51f-122">x</span></span>    | <span data-ttu-id="af51f-123">x</span><span class="sxs-lookup"><span data-stu-id="af51f-123">x</span></span>    | <span data-ttu-id="af51f-124">x</span><span class="sxs-lookup"><span data-stu-id="af51f-124">x</span></span>    | <span data-ttu-id="af51f-125">x</span><span class="sxs-lookup"><span data-stu-id="af51f-125">x</span></span>     | <span data-ttu-id="af51f-126">x</span><span class="sxs-lookup"><span data-stu-id="af51f-126">x</span></span>    | <span data-ttu-id="af51f-127">x</span><span class="sxs-lookup"><span data-stu-id="af51f-127">x</span></span>     |



 

<span data-ttu-id="af51f-128">Для регистрации назначения требуется маска XY.</span><span class="sxs-lookup"><span data-stu-id="af51f-128">The xy mask is required for the destination register.</span></span> <span data-ttu-id="af51f-129">Модификаторы отрицания и свиззле разрешены для src0, но не для src1.</span><span class="sxs-lookup"><span data-stu-id="af51f-129">Negate and swizzle modifiers are allowed for src0 but not for src1.</span></span>

<span data-ttu-id="af51f-130">В следующих уравнениях показано, как работает инструкция.</span><span class="sxs-lookup"><span data-stu-id="af51f-130">The following equations show how the instruction operates:</span></span>


```
dest.x = (src0.x * src1.x) + (src0.x * src1.y) + (src0.x * src1.z);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z);
```



<span data-ttu-id="af51f-131">Входной вектор находится в регистре src0.</span><span class="sxs-lookup"><span data-stu-id="af51f-131">The input vector is in register src0.</span></span> <span data-ttu-id="af51f-132">Входная матрица 3x2 находится в регистре src1 и следующем более высоком регистре в том же файле регистрации, как показано в следующем развертывании.</span><span class="sxs-lookup"><span data-stu-id="af51f-132">The input 3x2 matrix is in register src1 and the next higher register in the same register file, as shown in the following expansion.</span></span> <span data-ttu-id="af51f-133">Создается 2D-результат, в результате чего остальные элементы регистра назначения (dest. z и dest. w) не затрагиваются.</span><span class="sxs-lookup"><span data-stu-id="af51f-133">A 2D result is produced, leaving the other elements of the destination register (dest.z and dest.w) unaffected.</span></span>

<span data-ttu-id="af51f-134">Эта операция обычно используется для двумерных преобразований.</span><span class="sxs-lookup"><span data-stu-id="af51f-134">This operation is commonly used for 2D transforms.</span></span> <span data-ttu-id="af51f-135">Эта инструкция реализуется как пара изделий с точками, как показано здесь.</span><span class="sxs-lookup"><span data-stu-id="af51f-135">This instruction is implemented as a pair of dot products as shown here.</span></span>


```
m3x2   r0.xy, r1, c0   which will be expanded to:

dp3   r0.x, r1, c0
dp3   r0.y, r1, c1
```



<span data-ttu-id="af51f-136">Модификаторы свиззле и отрицания недопустимы для регистра src1.</span><span class="sxs-lookup"><span data-stu-id="af51f-136">Swizzle and negate modifiers are invalid for the src1 register.</span></span> <span data-ttu-id="af51f-137">Регистр dest и src0 или любой из src1 + i не могут быть одинаковыми.</span><span class="sxs-lookup"><span data-stu-id="af51f-137">The dest and src0 register, or any of src1+i registers, cannot be the same.</span></span>

## <a name="related-topics"></a><span data-ttu-id="af51f-138">См. также</span><span class="sxs-lookup"><span data-stu-id="af51f-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af51f-139">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="af51f-139">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




