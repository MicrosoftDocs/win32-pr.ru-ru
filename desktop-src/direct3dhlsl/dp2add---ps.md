---
title: dp2add-PS
description: Выполняет продукт с двухмерной точкой и скалярным добавлением.
ms.assetid: 4226ee34-2e68-4536-b171-68f3b967182e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 88d3d28cc64bdb7caa1b7456e87711c3dbee2b13
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104133302"
---
# <a name="dp2add---ps"></a><span data-ttu-id="2658e-103">dp2add-PS</span><span class="sxs-lookup"><span data-stu-id="2658e-103">dp2add - ps</span></span>

<span data-ttu-id="2658e-104">Выполняет продукт с двухмерной точкой и скалярным добавлением.</span><span class="sxs-lookup"><span data-stu-id="2658e-104">Performs a 2D dot product and a scalar addition.</span></span>

## <a name="syntax"></a><span data-ttu-id="2658e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2658e-105">Syntax</span></span>


```
dp2add dst, src0, src1, src2.{x|y|z|w}
```



<span data-ttu-id="2658e-106">Где:</span><span class="sxs-lookup"><span data-stu-id="2658e-106">Where:</span></span>

-   <span data-ttu-id="2658e-107">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="2658e-107">dst is a destination register.</span></span>
-   <span data-ttu-id="2658e-108">src0, src1 и src2 являются тремя исходными регистрами.</span><span class="sxs-lookup"><span data-stu-id="2658e-108">src0, src1, and src2 are three source registers.</span></span>
-   <span data-ttu-id="2658e-109">{x \| y \| z \| w} является обязательным параметром replicate свиззле on src2.</span><span class="sxs-lookup"><span data-stu-id="2658e-109">{x\|y\|z\|w} is the required replicate swizzle on src2.</span></span>

## <a name="remarks"></a><span data-ttu-id="2658e-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="2658e-110">Remarks</span></span>



| <span data-ttu-id="2658e-111">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="2658e-111">Pixel shader versions</span></span> | <span data-ttu-id="2658e-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="2658e-112">1\_1</span></span> | <span data-ttu-id="2658e-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="2658e-113">1\_2</span></span> | <span data-ttu-id="2658e-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="2658e-114">1\_3</span></span> | <span data-ttu-id="2658e-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="2658e-115">1\_4</span></span> | <span data-ttu-id="2658e-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2658e-116">2\_0</span></span> | <span data-ttu-id="2658e-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="2658e-117">2\_x</span></span> | <span data-ttu-id="2658e-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="2658e-118">2\_sw</span></span> | <span data-ttu-id="2658e-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2658e-119">3\_0</span></span> | <span data-ttu-id="2658e-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="2658e-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="2658e-121">dp2add</span><span class="sxs-lookup"><span data-stu-id="2658e-121">dp2add</span></span>                |      |      |      |      | <span data-ttu-id="2658e-122">x</span><span class="sxs-lookup"><span data-stu-id="2658e-122">x</span></span>    | <span data-ttu-id="2658e-123">x</span><span class="sxs-lookup"><span data-stu-id="2658e-123">x</span></span>    | <span data-ttu-id="2658e-124">x</span><span class="sxs-lookup"><span data-stu-id="2658e-124">x</span></span>     | <span data-ttu-id="2658e-125">x</span><span class="sxs-lookup"><span data-stu-id="2658e-125">x</span></span>    | <span data-ttu-id="2658e-126">x</span><span class="sxs-lookup"><span data-stu-id="2658e-126">x</span></span>     |



 

<span data-ttu-id="2658e-127">Скалярное значение для Add выбирается параметром replicate свиззле on src2.</span><span class="sxs-lookup"><span data-stu-id="2658e-127">The scalar value for add is chosen by the replicate swizzle on src2.</span></span>

<span data-ttu-id="2658e-128">В следующем фрагменте кода показаны выполняемые операции.</span><span class="sxs-lookup"><span data-stu-id="2658e-128">The following code snippet shows the operations performed.</span></span>


```
dest = src0.r * src1.r + src0.g * src1.g + src2.replicate_swizzle
// The scalar result is replicated to the write mask components
```



## <a name="related-topics"></a><span data-ttu-id="2658e-129">См. также</span><span class="sxs-lookup"><span data-stu-id="2658e-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2658e-130">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="2658e-130">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




