---
title: m3x4 — VS
description: Умножает вектор трех компонентов на матрицу 3X4. | m3x4 — VS
ms.assetid: 8bec1ac5-376b-4eae-ba82-b42a6c0e7c4e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a4018698dbe6ab986945a84c1fcf9ce0431bd0fc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986313"
---
# <a name="m3x4---vs"></a><span data-ttu-id="13938-104">m3x4 — VS</span><span class="sxs-lookup"><span data-stu-id="13938-104">m3x4 - vs</span></span>

<span data-ttu-id="13938-105">Умножает вектор трех компонентов на матрицу 3X4.</span><span class="sxs-lookup"><span data-stu-id="13938-105">Multiplies a 3-component vector by a 3x4 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="13938-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="13938-106">Syntax</span></span>



| <span data-ttu-id="13938-107">m3x4 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="13938-107">m3x4 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="13938-108">где</span><span class="sxs-lookup"><span data-stu-id="13938-108">where</span></span>

-   <span data-ttu-id="13938-109">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="13938-109">dst is the destination register.</span></span> <span data-ttu-id="13938-110">Result является вектором из 4 компонентов.</span><span class="sxs-lookup"><span data-stu-id="13938-110">Result is a 4-component vector.</span></span>
-   <span data-ttu-id="13938-111">src0 — это исходный регистр, представляющий 3-компонентный вектор.</span><span class="sxs-lookup"><span data-stu-id="13938-111">src0 is a source register representing a 3-component vector.</span></span>
-   <span data-ttu-id="13938-112">src1 — это исходный регистр, представляющий матрицу 3X4, которая соответствует первому из четырех последовательных регистров.</span><span class="sxs-lookup"><span data-stu-id="13938-112">src1 is a source register representing a 3x4 matrix, which corresponds to the first of 4 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="13938-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="13938-113">Remarks</span></span>



| <span data-ttu-id="13938-114">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="13938-114">Vertex shader versions</span></span> | <span data-ttu-id="13938-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="13938-115">1\_1</span></span> | <span data-ttu-id="13938-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="13938-116">2\_0</span></span> | <span data-ttu-id="13938-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="13938-117">2\_x</span></span> | <span data-ttu-id="13938-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="13938-118">2\_sw</span></span> | <span data-ttu-id="13938-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="13938-119">3\_0</span></span> | <span data-ttu-id="13938-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="13938-120">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="13938-121">m3x4</span><span class="sxs-lookup"><span data-stu-id="13938-121">m3x4</span></span>                   | <span data-ttu-id="13938-122">x</span><span class="sxs-lookup"><span data-stu-id="13938-122">x</span></span>    | <span data-ttu-id="13938-123">x</span><span class="sxs-lookup"><span data-stu-id="13938-123">x</span></span>    | <span data-ttu-id="13938-124">x</span><span class="sxs-lookup"><span data-stu-id="13938-124">x</span></span>    | <span data-ttu-id="13938-125">x</span><span class="sxs-lookup"><span data-stu-id="13938-125">x</span></span>     | <span data-ttu-id="13938-126">x</span><span class="sxs-lookup"><span data-stu-id="13938-126">x</span></span>    | <span data-ttu-id="13938-127">x</span><span class="sxs-lookup"><span data-stu-id="13938-127">x</span></span>     |



 

<span data-ttu-id="13938-128">Для регистра назначения требуется маска ксизв (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="13938-128">The xyzw (default) mask is required for the destination register.</span></span> <span data-ttu-id="13938-129">Модификаторы отрицания и свиззле разрешены для src0, но не для src1.</span><span class="sxs-lookup"><span data-stu-id="13938-129">Negate and swizzle modifiers are allowed for src0 but not for src1.</span></span>

<span data-ttu-id="13938-130">В следующем фрагменте кода показаны выполняемые операции.</span><span class="sxs-lookup"><span data-stu-id="13938-130">The following code fragment shows the operations performed.</span></span>


```
 
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z);
dest.w = (src0.x * src4.x) + (src0.y * src4.y) + (src0.z * src4.z);
```



<span data-ttu-id="13938-131">Входной вектор находится в регистре src0.</span><span class="sxs-lookup"><span data-stu-id="13938-131">The input vector is in register src0.</span></span> <span data-ttu-id="13938-132">Входная матрица 3X4 находится в регистре src1 и следующих трех старших регистров, как показано в расширении ниже.</span><span class="sxs-lookup"><span data-stu-id="13938-132">The input 3x4 matrix is in register src1 and the next three higher registers, as shown in the expansion below.</span></span>

<span data-ttu-id="13938-133">Эта операция обычно используется для преобразования вектора расположения в матрицу, которая имеет проектный результат, но не применяет перевод.</span><span class="sxs-lookup"><span data-stu-id="13938-133">This operation is commonly used for transforming a position vector by a matrix that has a projective effect but applies no translation.</span></span> <span data-ttu-id="13938-134">Эта инструкция реализуется как пара изделий с точками, как показано здесь.</span><span class="sxs-lookup"><span data-stu-id="13938-134">This instruction is implemented as a pair of dot products as shown here.</span></span>


```
m3x4   r0.xyzw, r1, c0   will be expanded to: 

dp3 r0.x, r1, c0
dp3 r0.y, r1, c1
dp3 r0.z, r1, c2
dp3 r0.w, r1, c3
```



## <a name="related-topics"></a><span data-ttu-id="13938-135">См. также</span><span class="sxs-lookup"><span data-stu-id="13938-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13938-136">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="13938-136">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




