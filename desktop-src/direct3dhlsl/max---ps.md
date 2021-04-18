---
title: Max-PS
description: Вычисляет максимум источников. | Max-PS
ms.assetid: 3d3bef5b-0ff7-441b-8681-a3f4cde0ae4f
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c6186f0bd57acd4862a62a4c0a30ae92118b75ce
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986744"
---
# <a name="max---ps"></a><span data-ttu-id="c100f-104">Max-PS</span><span class="sxs-lookup"><span data-stu-id="c100f-104">max - ps</span></span>

<span data-ttu-id="c100f-105">Вычисляет максимум источников.</span><span class="sxs-lookup"><span data-stu-id="c100f-105">Calculates the maximum of the sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="c100f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c100f-106">Syntax</span></span>



| <span data-ttu-id="c100f-107">максимальный DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="c100f-107">max dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="c100f-108">где</span><span class="sxs-lookup"><span data-stu-id="c100f-108">where</span></span>

-   <span data-ttu-id="c100f-109">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="c100f-109">dst is the destination register.</span></span>
-   <span data-ttu-id="c100f-110">src0 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="c100f-110">src0 is a source register.</span></span>
-   <span data-ttu-id="c100f-111">src1 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="c100f-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="c100f-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="c100f-112">Remarks</span></span>



| <span data-ttu-id="c100f-113">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="c100f-113">Pixel shader versions</span></span> | <span data-ttu-id="c100f-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="c100f-114">1\_1</span></span> | <span data-ttu-id="c100f-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="c100f-115">1\_2</span></span> | <span data-ttu-id="c100f-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="c100f-116">1\_3</span></span> | <span data-ttu-id="c100f-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="c100f-117">1\_4</span></span> | <span data-ttu-id="c100f-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c100f-118">2\_0</span></span> | <span data-ttu-id="c100f-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c100f-119">2\_x</span></span> | <span data-ttu-id="c100f-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c100f-120">2\_sw</span></span> | <span data-ttu-id="c100f-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c100f-121">3\_0</span></span> | <span data-ttu-id="c100f-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c100f-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="c100f-123">max</span><span class="sxs-lookup"><span data-stu-id="c100f-123">max</span></span>                   |      |      |      |      | <span data-ttu-id="c100f-124">x</span><span class="sxs-lookup"><span data-stu-id="c100f-124">x</span></span>    | <span data-ttu-id="c100f-125">x</span><span class="sxs-lookup"><span data-stu-id="c100f-125">x</span></span>    | <span data-ttu-id="c100f-126">x</span><span class="sxs-lookup"><span data-stu-id="c100f-126">x</span></span>     | <span data-ttu-id="c100f-127">x</span><span class="sxs-lookup"><span data-stu-id="c100f-127">x</span></span>    | <span data-ttu-id="c100f-128">x</span><span class="sxs-lookup"><span data-stu-id="c100f-128">x</span></span>     |



 

<span data-ttu-id="c100f-129">В следующем фрагменте кода показаны выполняемые операции.</span><span class="sxs-lookup"><span data-stu-id="c100f-129">The following code snippet shows the operations performed.</span></span>


```
dest.x=(src0.x >= src1.x) ? src0.x : src1.x;
dest.y=(src0.y >= src1.y) ? src0.y : src1.y;
dest.z=(src0.z >= src1.z) ? src0.z : src1.z;
dest.w=(src0.w >= src1.w) ? src0.w : src1.w;
```



## <a name="related-topics"></a><span data-ttu-id="c100f-130">См. также</span><span class="sxs-lookup"><span data-stu-id="c100f-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c100f-131">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="c100f-131">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




