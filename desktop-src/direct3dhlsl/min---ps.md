---
title: min-PS
description: Вычисляет минимум источников. | min-PS
ms.assetid: 2ee6208d-a353-4747-8037-c21dd1a05016
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3a735b38769a30e9dccf544785d931641469f5dc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986444"
---
# <a name="min---ps"></a><span data-ttu-id="83db1-104">min-PS</span><span class="sxs-lookup"><span data-stu-id="83db1-104">min - ps</span></span>

<span data-ttu-id="83db1-105">Вычисляет минимум источников.</span><span class="sxs-lookup"><span data-stu-id="83db1-105">Calculates the minimum of the sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="83db1-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="83db1-106">Syntax</span></span>



| <span data-ttu-id="83db1-107">min DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="83db1-107">min dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="83db1-108">где</span><span class="sxs-lookup"><span data-stu-id="83db1-108">where</span></span>

-   <span data-ttu-id="83db1-109">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="83db1-109">dst is the destination register.</span></span>
-   <span data-ttu-id="83db1-110">src0 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="83db1-110">src0 is a source register.</span></span>
-   <span data-ttu-id="83db1-111">src1 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="83db1-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="83db1-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="83db1-112">Remarks</span></span>



| <span data-ttu-id="83db1-113">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="83db1-113">Pixel shader versions</span></span> | <span data-ttu-id="83db1-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="83db1-114">1\_1</span></span> | <span data-ttu-id="83db1-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="83db1-115">1\_2</span></span> | <span data-ttu-id="83db1-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="83db1-116">1\_3</span></span> | <span data-ttu-id="83db1-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="83db1-117">1\_4</span></span> | <span data-ttu-id="83db1-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="83db1-118">2\_0</span></span> | <span data-ttu-id="83db1-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="83db1-119">2\_x</span></span> | <span data-ttu-id="83db1-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="83db1-120">2\_sw</span></span> | <span data-ttu-id="83db1-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="83db1-121">3\_0</span></span> | <span data-ttu-id="83db1-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="83db1-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="83db1-123">мин</span><span class="sxs-lookup"><span data-stu-id="83db1-123">min</span></span>                   |      |      |      |      | <span data-ttu-id="83db1-124">x</span><span class="sxs-lookup"><span data-stu-id="83db1-124">x</span></span>    | <span data-ttu-id="83db1-125">x</span><span class="sxs-lookup"><span data-stu-id="83db1-125">x</span></span>    | <span data-ttu-id="83db1-126">x</span><span class="sxs-lookup"><span data-stu-id="83db1-126">x</span></span>     | <span data-ttu-id="83db1-127">x</span><span class="sxs-lookup"><span data-stu-id="83db1-127">x</span></span>    | <span data-ttu-id="83db1-128">x</span><span class="sxs-lookup"><span data-stu-id="83db1-128">x</span></span>     |



 

<span data-ttu-id="83db1-129">В следующем фрагменте кода показаны выполняемые операции.</span><span class="sxs-lookup"><span data-stu-id="83db1-129">The following code snippet shows the operations performed.</span></span>


```
dest.x=(src0.x < src1.x) ? src0.x : src1.x;
dest.y=(src0.y < src1.y) ? src0.y : src1.y;
dest.z=(src0.z < src1.z) ? src0.z : src1.z;
dest.w=(src0.w < src1.w) ? src0.w : src1.w;
```



## <a name="related-topics"></a><span data-ttu-id="83db1-130">См. также</span><span class="sxs-lookup"><span data-stu-id="83db1-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83db1-131">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="83db1-131">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




