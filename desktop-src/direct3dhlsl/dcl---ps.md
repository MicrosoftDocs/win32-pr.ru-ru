---
title: дкл-(SM2, SM3-PS ASM)
description: Объявите входной регистр шейдера пикселей.
ms.assetid: d6fcd94e-80d7-4e8a-8b4f-ff86c980cc38
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4f2ba81650611351970ff4068edaa75d27d34fc4
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/01/2021
ms.locfileid: "113130103"
---
# <a name="dcl---sm2-sm3---ps-asm"></a><span data-ttu-id="a1676-103">дкл-(SM2, SM3-PS ASM)</span><span class="sxs-lookup"><span data-stu-id="a1676-103">dcl - (sm2, sm3 - ps asm)</span></span>

<span data-ttu-id="a1676-104">Объявите входной регистр шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="a1676-104">Declare a pixel shader input register.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1676-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a1676-105">Syntax</span></span>

<span data-ttu-id="a1676-106">дкл \[ \_ PP \] dest \[ . Mask\]</span><span class="sxs-lookup"><span data-stu-id="a1676-106">dcl\[\_pp\] dest\[.mask\]</span></span>



 

<span data-ttu-id="a1676-107">Где:</span><span class="sxs-lookup"><span data-stu-id="a1676-107">Where:</span></span>

-   <span data-ttu-id="a1676-108">\[\_PP \] является необязательной частичной точностью.</span><span class="sxs-lookup"><span data-stu-id="a1676-108">\[\_pp\] is optional partial precision.</span></span> <span data-ttu-id="a1676-109">См. раздел [частичная точность](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md).</span><span class="sxs-lookup"><span data-stu-id="a1676-109">See [Partial Precision](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md).</span></span>
-   <span data-ttu-id="a1676-110">dest — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="a1676-110">dest is a destination register.</span></span> <span data-ttu-id="a1676-111">Это должен быть либо [Регистр цвета ввода](dx9-graphics-reference-asm-ps-registers-input-color.md) (VN), либо [регистр текстурной координаты](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (тн).</span><span class="sxs-lookup"><span data-stu-id="a1676-111">It must be either a [Input Color Register](dx9-graphics-reference-asm-ps-registers-input-color.md) (vn), or an [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (tn).</span></span>
-   <span data-ttu-id="a1676-112">\[. Mask \] — это необязательная маска записи, которая определяет, в какие компоненты регистра назначения могут быть записаны.</span><span class="sxs-lookup"><span data-stu-id="a1676-112">\[.mask\] is an optional write mask that controls which components of the destination register that can be written to.</span></span> <span data-ttu-id="a1676-113">См. раздел " [маска записи целевого регистра](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)".</span><span class="sxs-lookup"><span data-stu-id="a1676-113">See [Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a1676-114">Remarks</span><span class="sxs-lookup"><span data-stu-id="a1676-114">Remarks</span></span>



| <span data-ttu-id="a1676-115">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="a1676-115">Pixel shader versions</span></span> | <span data-ttu-id="a1676-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="a1676-116">1\_1</span></span> | <span data-ttu-id="a1676-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="a1676-117">1\_2</span></span> | <span data-ttu-id="a1676-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="a1676-118">1\_3</span></span> | <span data-ttu-id="a1676-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="a1676-119">1\_4</span></span> | <span data-ttu-id="a1676-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a1676-120">2\_0</span></span> | <span data-ttu-id="a1676-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a1676-121">2\_x</span></span> | <span data-ttu-id="a1676-122">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a1676-122">2\_sw</span></span> | <span data-ttu-id="a1676-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a1676-123">3\_0</span></span> | <span data-ttu-id="a1676-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a1676-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="a1676-125">дкл</span><span class="sxs-lookup"><span data-stu-id="a1676-125">dcl</span></span>                   |      |      |      |      | <span data-ttu-id="a1676-126">x</span><span class="sxs-lookup"><span data-stu-id="a1676-126">x</span></span>    | <span data-ttu-id="a1676-127">x</span><span class="sxs-lookup"><span data-stu-id="a1676-127">x</span></span>    | <span data-ttu-id="a1676-128">x</span><span class="sxs-lookup"><span data-stu-id="a1676-128">x</span></span>     | <span data-ttu-id="a1676-129">x</span><span class="sxs-lookup"><span data-stu-id="a1676-129">x</span></span>    | <span data-ttu-id="a1676-130">x</span><span class="sxs-lookup"><span data-stu-id="a1676-130">x</span></span>     |



 

<span data-ttu-id="a1676-131">Все инструкции дкл должны располагаться перед первой исполняемой инструкцией.</span><span class="sxs-lookup"><span data-stu-id="a1676-131">All dcl instructions must appear before the first executable instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1676-132">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="a1676-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1676-133">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="a1676-133">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




