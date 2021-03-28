---
title: DP4-PS
description: Выполняет вычисление 4-компонентного произведения исходных регистров. | DP4-PS
ms.assetid: 83ef6097-cacf-4498-842b-3eb03e57bd6f
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2562259af164b8680d54e9a120abaa405fd781c5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104081780"
---
# <a name="dp4---ps"></a><span data-ttu-id="0bbb9-104">DP4-PS</span><span class="sxs-lookup"><span data-stu-id="0bbb9-104">dp4 - ps</span></span>

<span data-ttu-id="0bbb9-105">Выполняет вычисление 4-компонентного произведения исходных регистров.</span><span class="sxs-lookup"><span data-stu-id="0bbb9-105">Computes the four-component dot product of the source registers.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bbb9-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0bbb9-106">Syntax</span></span>



| <span data-ttu-id="0bbb9-107">DP4 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="0bbb9-107">dp4 dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="0bbb9-108">где</span><span class="sxs-lookup"><span data-stu-id="0bbb9-108">where</span></span>

-   <span data-ttu-id="0bbb9-109">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="0bbb9-109">dst is the destination register.</span></span>
-   <span data-ttu-id="0bbb9-110">src0 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="0bbb9-110">src0 is a source register.</span></span>
-   <span data-ttu-id="0bbb9-111">src1 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="0bbb9-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bbb9-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="0bbb9-112">Remarks</span></span>



| <span data-ttu-id="0bbb9-113">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="0bbb9-113">Pixel shader versions</span></span> | <span data-ttu-id="0bbb9-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="0bbb9-114">1\_1</span></span> | <span data-ttu-id="0bbb9-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="0bbb9-115">1\_2</span></span> | <span data-ttu-id="0bbb9-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="0bbb9-116">1\_3</span></span> | <span data-ttu-id="0bbb9-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="0bbb9-117">1\_4</span></span> | <span data-ttu-id="0bbb9-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0bbb9-118">2\_0</span></span> | <span data-ttu-id="0bbb9-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="0bbb9-119">2\_x</span></span> | <span data-ttu-id="0bbb9-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0bbb9-120">2\_sw</span></span> | <span data-ttu-id="0bbb9-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0bbb9-121">3\_0</span></span> | <span data-ttu-id="0bbb9-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0bbb9-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="0bbb9-123">dp4</span><span class="sxs-lookup"><span data-stu-id="0bbb9-123">dp4</span></span>                   |      | <span data-ttu-id="0bbb9-124">x</span><span class="sxs-lookup"><span data-stu-id="0bbb9-124">x</span></span>    | <span data-ttu-id="0bbb9-125">x</span><span class="sxs-lookup"><span data-stu-id="0bbb9-125">x</span></span>    | <span data-ttu-id="0bbb9-126">x</span><span class="sxs-lookup"><span data-stu-id="0bbb9-126">x</span></span>    | <span data-ttu-id="0bbb9-127">x</span><span class="sxs-lookup"><span data-stu-id="0bbb9-127">x</span></span>    | <span data-ttu-id="0bbb9-128">x</span><span class="sxs-lookup"><span data-stu-id="0bbb9-128">x</span></span>    | <span data-ttu-id="0bbb9-129">x</span><span class="sxs-lookup"><span data-stu-id="0bbb9-129">x</span></span>     | <span data-ttu-id="0bbb9-130">x</span><span class="sxs-lookup"><span data-stu-id="0bbb9-130">x</span></span>    | <span data-ttu-id="0bbb9-131">x</span><span class="sxs-lookup"><span data-stu-id="0bbb9-131">x</span></span>     |



 

<span data-ttu-id="0bbb9-132">В следующем фрагменте кода показаны выполняемые операции.</span><span class="sxs-lookup"><span data-stu-id="0bbb9-132">The following code snippet shows the operations performed:</span></span>


```
dest.x = dest.y = dest.z = dest.w = 
    (src0.x * src1.x) + (src0.y * src1.y) + 
    (src0.z * src1.z) + (src0.w * src1.w);
```



<span data-ttu-id="0bbb9-133">Ограничения для PS \_ 1 \_ 2 и PS \_ 1 \_ 3:</span><span class="sxs-lookup"><span data-stu-id="0bbb9-133">Limitations for ps\_1\_2 and ps\_1\_3:</span></span>

-   <span data-ttu-id="0bbb9-134">Каждый шейдер может использовать не более четырех инструкций DP4.</span><span class="sxs-lookup"><span data-stu-id="0bbb9-134">Each shader can use up to a maximum of four dp4 instructions.</span></span>
-   <span data-ttu-id="0bbb9-135">Каждая инструкция DP4 считается двумя арифметическими инструкциями.</span><span class="sxs-lookup"><span data-stu-id="0bbb9-135">Each dp4 instruction counts as two arithmetic instructions.</span></span>

<span data-ttu-id="0bbb9-136">Ограничения для \_ версий 1 X:</span><span class="sxs-lookup"><span data-stu-id="0bbb9-136">Limitations for 1\_X versions:</span></span>

-   <span data-ttu-id="0bbb9-137">Эта инструкция не может быть выдана, так как DP4 выполняется как в векторном, так и в альфа-канале.</span><span class="sxs-lookup"><span data-stu-id="0bbb9-137">This instruction cannot be co-issued because dp4 runs in both the vector and alpha pipeline.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0bbb9-138">См. также</span><span class="sxs-lookup"><span data-stu-id="0bbb9-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bbb9-139">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="0bbb9-139">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




