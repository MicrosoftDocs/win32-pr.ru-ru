---
title: m3x4-PS
description: Умножает вектор трех компонентов на матрицу 3X4. | m3x4-PS
ms.assetid: b749d3cd-2acf-450c-94f2-fea5e1c8f4d2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4c245f4765853301a7c8319c8038b9ed342e3715
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986640"
---
# <a name="m3x4---ps"></a><span data-ttu-id="09222-104">m3x4-PS</span><span class="sxs-lookup"><span data-stu-id="09222-104">m3x4 - ps</span></span>

<span data-ttu-id="09222-105">Умножает вектор трех компонентов на матрицу 3X4.</span><span class="sxs-lookup"><span data-stu-id="09222-105">Multiplies a 3-component vector by a 3x4 matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="09222-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="09222-106">Syntax</span></span>



| <span data-ttu-id="09222-107">m3x4 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="09222-107">m3x4 dst, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="09222-108">где</span><span class="sxs-lookup"><span data-stu-id="09222-108">where</span></span>

-   <span data-ttu-id="09222-109">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="09222-109">dst is the destination register.</span></span> <span data-ttu-id="09222-110">Result является вектором из 4 компонентов.</span><span class="sxs-lookup"><span data-stu-id="09222-110">Result is a 4-component vector.</span></span>
-   <span data-ttu-id="09222-111">src0 — это исходный регистр, представляющий 3-компонентный вектор.</span><span class="sxs-lookup"><span data-stu-id="09222-111">src0 is a source register representing a 3-component vector.</span></span>
-   <span data-ttu-id="09222-112">src1 — это исходный регистр, представляющий матрицу 3X4, которая соответствует первому из четырех последовательных регистров.</span><span class="sxs-lookup"><span data-stu-id="09222-112">src1 is a source register representing a 3x4 matrix, which corresponds to the first of 4 consecutive registers.</span></span>

## <a name="remarks"></a><span data-ttu-id="09222-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="09222-113">Remarks</span></span>



| <span data-ttu-id="09222-114">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="09222-114">Pixel shader versions</span></span> | <span data-ttu-id="09222-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="09222-115">1\_1</span></span> | <span data-ttu-id="09222-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="09222-116">1\_2</span></span> | <span data-ttu-id="09222-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="09222-117">1\_3</span></span> | <span data-ttu-id="09222-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="09222-118">1\_4</span></span> | <span data-ttu-id="09222-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="09222-119">2\_0</span></span> | <span data-ttu-id="09222-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="09222-120">2\_x</span></span> | <span data-ttu-id="09222-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="09222-121">2\_sw</span></span> | <span data-ttu-id="09222-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="09222-122">3\_0</span></span> | <span data-ttu-id="09222-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="09222-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="09222-124">m3x4</span><span class="sxs-lookup"><span data-stu-id="09222-124">m3x4</span></span>                  |      |      |      |      | <span data-ttu-id="09222-125">x</span><span class="sxs-lookup"><span data-stu-id="09222-125">x</span></span>    | <span data-ttu-id="09222-126">x</span><span class="sxs-lookup"><span data-stu-id="09222-126">x</span></span>    | <span data-ttu-id="09222-127">x</span><span class="sxs-lookup"><span data-stu-id="09222-127">x</span></span>     | <span data-ttu-id="09222-128">x</span><span class="sxs-lookup"><span data-stu-id="09222-128">x</span></span>    | <span data-ttu-id="09222-129">x</span><span class="sxs-lookup"><span data-stu-id="09222-129">x</span></span>     |



 

<span data-ttu-id="09222-130">Для регистра назначения требуется маска ксизв (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="09222-130">The xyzw (default) mask is required for the destination register.</span></span> <span data-ttu-id="09222-131">Модификаторы отрицания и свиззле разрешены для src0, но не для src1.</span><span class="sxs-lookup"><span data-stu-id="09222-131">Negate and swizzle modifiers are allowed for src0 but not for src1.</span></span>

<span data-ttu-id="09222-132">В следующем фрагменте кода показаны выполняемые операции.</span><span class="sxs-lookup"><span data-stu-id="09222-132">The following code snippet shows the operations performed.</span></span>


```
 
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z);
dest.z = (src0.x*src3.x) + (src0.y*src3.y) + (src0.z*src3.z);
dest.w = (src0.x*src4.x) + (src0.y*src4.y) + (src0.z*src4.z);
```



<span data-ttu-id="09222-133">Входной вектор находится в регистре src0.</span><span class="sxs-lookup"><span data-stu-id="09222-133">The input vector is in register src0.</span></span> <span data-ttu-id="09222-134">Входная матрица 3X4 находится в регистре src1 и следующих двух старших регистров, как показано в расширении ниже.</span><span class="sxs-lookup"><span data-stu-id="09222-134">The input 3x4 matrix is in register src1, and the next two higher registers, as shown in the expansion below.</span></span>

<span data-ttu-id="09222-135">Эта операция обычно используется для преобразования вектора расположения в матрицу, которая имеет проектный результат, но не применяет перевод.</span><span class="sxs-lookup"><span data-stu-id="09222-135">This operation is commonly used for transforming a position vector by a matrix that has a projective effect but applies no translation.</span></span> <span data-ttu-id="09222-136">Эта инструкция реализуется как пара изделий с точками, как показано здесь.</span><span class="sxs-lookup"><span data-stu-id="09222-136">This instruction is implemented as a pair of dot products as shown here.</span></span>


```
m3x4   r0.xyzw, r1, c0   will be expanded to: 

dp3 r0.x, r1, c0
dp3 r0.y, r1, c1
dp3 r0.z, r1, c2
dp3 r0.w, r1, c3
```



## <a name="related-topics"></a><span data-ttu-id="09222-137">См. также</span><span class="sxs-lookup"><span data-stu-id="09222-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09222-138">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="09222-138">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




