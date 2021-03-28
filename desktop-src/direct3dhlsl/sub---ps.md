---
title: Подсистема PS
description: Вычитает источники. | Подсистема PS
ms.assetid: e130724f-63bf-4d7f-bc9f-6a4441a788b8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4998892aa06eff55632600a9c2f7fe359c11f830
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "103820500"
---
# <a name="sub---ps"></a><span data-ttu-id="63653-104">Подсистема PS</span><span class="sxs-lookup"><span data-stu-id="63653-104">sub - ps</span></span>

<span data-ttu-id="63653-105">Вычитает источники.</span><span class="sxs-lookup"><span data-stu-id="63653-105">Subtracts sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="63653-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="63653-106">Syntax</span></span>



| <span data-ttu-id="63653-107">дополнительный DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="63653-107">sub dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="63653-108">где</span><span class="sxs-lookup"><span data-stu-id="63653-108">where</span></span>

-   <span data-ttu-id="63653-109">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="63653-109">dst is the destination register.</span></span>
-   <span data-ttu-id="63653-110">src0 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="63653-110">src0 is a source register.</span></span>
-   <span data-ttu-id="63653-111">src1 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="63653-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="63653-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="63653-112">Remarks</span></span>



| <span data-ttu-id="63653-113">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="63653-113">Pixel shader versions</span></span> | <span data-ttu-id="63653-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="63653-114">1\_1</span></span> | <span data-ttu-id="63653-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="63653-115">1\_2</span></span> | <span data-ttu-id="63653-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="63653-116">1\_3</span></span> | <span data-ttu-id="63653-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="63653-117">1\_4</span></span> | <span data-ttu-id="63653-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="63653-118">2\_0</span></span> | <span data-ttu-id="63653-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="63653-119">2\_x</span></span> | <span data-ttu-id="63653-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="63653-120">2\_sw</span></span> | <span data-ttu-id="63653-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="63653-121">3\_0</span></span> | <span data-ttu-id="63653-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="63653-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="63653-123">sub</span><span class="sxs-lookup"><span data-stu-id="63653-123">sub</span></span>                   | <span data-ttu-id="63653-124">x</span><span class="sxs-lookup"><span data-stu-id="63653-124">x</span></span>    | <span data-ttu-id="63653-125">x</span><span class="sxs-lookup"><span data-stu-id="63653-125">x</span></span>    | <span data-ttu-id="63653-126">x</span><span class="sxs-lookup"><span data-stu-id="63653-126">x</span></span>    | <span data-ttu-id="63653-127">x</span><span class="sxs-lookup"><span data-stu-id="63653-127">x</span></span>    | <span data-ttu-id="63653-128">x</span><span class="sxs-lookup"><span data-stu-id="63653-128">x</span></span>    | <span data-ttu-id="63653-129">x</span><span class="sxs-lookup"><span data-stu-id="63653-129">x</span></span>    | <span data-ttu-id="63653-130">x</span><span class="sxs-lookup"><span data-stu-id="63653-130">x</span></span>     | <span data-ttu-id="63653-131">x</span><span class="sxs-lookup"><span data-stu-id="63653-131">x</span></span>    | <span data-ttu-id="63653-132">x</span><span class="sxs-lookup"><span data-stu-id="63653-132">x</span></span>     |



 

<span data-ttu-id="63653-133">Эта инструкция выполняет вычитание, показанное в этой формуле.</span><span class="sxs-lookup"><span data-stu-id="63653-133">This instruction performs the subtraction shown in this formula.</span></span>


```
dest = src0 - src1
```



## <a name="related-topics"></a><span data-ttu-id="63653-134">См. также</span><span class="sxs-lookup"><span data-stu-id="63653-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63653-135">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="63653-135">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




