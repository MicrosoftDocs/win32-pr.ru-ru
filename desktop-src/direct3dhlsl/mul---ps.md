---
title: mul-PS
description: Умножает источники на место назначения. | mul-PS
ms.assetid: 03823c10-9631-4468-8488-4bd17224d16c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fefe89d4fdbe5f75965f2707a5ceb2c1673e1326
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998231"
---
# <a name="mul---ps"></a><span data-ttu-id="7760d-104">mul-PS</span><span class="sxs-lookup"><span data-stu-id="7760d-104">mul - ps</span></span>

<span data-ttu-id="7760d-105">Умножает источники на место назначения.</span><span class="sxs-lookup"><span data-stu-id="7760d-105">Multiplies sources into the destination.</span></span>

## <a name="syntax"></a><span data-ttu-id="7760d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7760d-106">Syntax</span></span>



| <span data-ttu-id="7760d-107">mul DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="7760d-107">mul dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="7760d-108">где</span><span class="sxs-lookup"><span data-stu-id="7760d-108">where</span></span>

-   <span data-ttu-id="7760d-109">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="7760d-109">dst is the destination register.</span></span>
-   <span data-ttu-id="7760d-110">src0 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="7760d-110">src0 is a source register.</span></span>
-   <span data-ttu-id="7760d-111">src1 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="7760d-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="7760d-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="7760d-112">Remarks</span></span>



| <span data-ttu-id="7760d-113">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="7760d-113">Pixel shader versions</span></span> | <span data-ttu-id="7760d-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="7760d-114">1\_1</span></span> | <span data-ttu-id="7760d-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="7760d-115">1\_2</span></span> | <span data-ttu-id="7760d-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="7760d-116">1\_3</span></span> | <span data-ttu-id="7760d-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="7760d-117">1\_4</span></span> | <span data-ttu-id="7760d-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7760d-118">2\_0</span></span> | <span data-ttu-id="7760d-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="7760d-119">2\_x</span></span> | <span data-ttu-id="7760d-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7760d-120">2\_sw</span></span> | <span data-ttu-id="7760d-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7760d-121">3\_0</span></span> | <span data-ttu-id="7760d-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7760d-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="7760d-123">mul</span><span class="sxs-lookup"><span data-stu-id="7760d-123">mul</span></span>                   | <span data-ttu-id="7760d-124">x</span><span class="sxs-lookup"><span data-stu-id="7760d-124">x</span></span>    | <span data-ttu-id="7760d-125">x</span><span class="sxs-lookup"><span data-stu-id="7760d-125">x</span></span>    | <span data-ttu-id="7760d-126">x</span><span class="sxs-lookup"><span data-stu-id="7760d-126">x</span></span>    | <span data-ttu-id="7760d-127">x</span><span class="sxs-lookup"><span data-stu-id="7760d-127">x</span></span>    | <span data-ttu-id="7760d-128">x</span><span class="sxs-lookup"><span data-stu-id="7760d-128">x</span></span>    | <span data-ttu-id="7760d-129">x</span><span class="sxs-lookup"><span data-stu-id="7760d-129">x</span></span>    | <span data-ttu-id="7760d-130">x</span><span class="sxs-lookup"><span data-stu-id="7760d-130">x</span></span>     | <span data-ttu-id="7760d-131">x</span><span class="sxs-lookup"><span data-stu-id="7760d-131">x</span></span>    | <span data-ttu-id="7760d-132">x</span><span class="sxs-lookup"><span data-stu-id="7760d-132">x</span></span>     |



 

<span data-ttu-id="7760d-133">В следующем фрагменте кода показаны выполняемые операции.</span><span class="sxs-lookup"><span data-stu-id="7760d-133">The following code snippet shows the operations performed.</span></span>


```
dest.x = src0.x * src1.x;
dest.y = src0.y * src1.y;
dest.z = src0.z * src1.z;
dest.w = src0.w * src1.w;
```



## <a name="related-topics"></a><span data-ttu-id="7760d-134">См. также</span><span class="sxs-lookup"><span data-stu-id="7760d-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7760d-135">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="7760d-135">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




