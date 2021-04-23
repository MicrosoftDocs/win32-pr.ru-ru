---
title: min — VS
description: Вычисляет минимум источников. | min — VS
ms.assetid: cecfe98b-8efd-4fbf-a7b5-d228de724e71
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: eda47b75398b8643f7010ff7468f72f4a7d8c199
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986548"
---
# <a name="min---vs"></a><span data-ttu-id="42538-104">min — VS</span><span class="sxs-lookup"><span data-stu-id="42538-104">min - vs</span></span>

<span data-ttu-id="42538-105">Вычисляет минимум источников.</span><span class="sxs-lookup"><span data-stu-id="42538-105">Calculates the minimum of the sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="42538-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="42538-106">Syntax</span></span>



| <span data-ttu-id="42538-107">min DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="42538-107">min dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="42538-108">где</span><span class="sxs-lookup"><span data-stu-id="42538-108">where</span></span>

-   <span data-ttu-id="42538-109">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="42538-109">dst is the destination register.</span></span>
-   <span data-ttu-id="42538-110">src0 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="42538-110">src0 is a source register.</span></span>
-   <span data-ttu-id="42538-111">src1 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="42538-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="42538-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="42538-112">Remarks</span></span>



| <span data-ttu-id="42538-113">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="42538-113">Vertex shader versions</span></span> | <span data-ttu-id="42538-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="42538-114">1\_1</span></span> | <span data-ttu-id="42538-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="42538-115">2\_0</span></span> | <span data-ttu-id="42538-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="42538-116">2\_x</span></span> | <span data-ttu-id="42538-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="42538-117">2\_sw</span></span> | <span data-ttu-id="42538-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="42538-118">3\_0</span></span> | <span data-ttu-id="42538-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="42538-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="42538-120">мин</span><span class="sxs-lookup"><span data-stu-id="42538-120">min</span></span>                    | <span data-ttu-id="42538-121">x</span><span class="sxs-lookup"><span data-stu-id="42538-121">x</span></span>    | <span data-ttu-id="42538-122">x</span><span class="sxs-lookup"><span data-stu-id="42538-122">x</span></span>    | <span data-ttu-id="42538-123">x</span><span class="sxs-lookup"><span data-stu-id="42538-123">x</span></span>    | <span data-ttu-id="42538-124">x</span><span class="sxs-lookup"><span data-stu-id="42538-124">x</span></span>     | <span data-ttu-id="42538-125">x</span><span class="sxs-lookup"><span data-stu-id="42538-125">x</span></span>    | <span data-ttu-id="42538-126">x</span><span class="sxs-lookup"><span data-stu-id="42538-126">x</span></span>     |



 

<span data-ttu-id="42538-127">В следующем фрагменте кода показаны выполняемые операции.</span><span class="sxs-lookup"><span data-stu-id="42538-127">The following code fragment shows the operations performed.</span></span>


```
dest.x=(src0.x < src1.x) ? src0.x : src1.x;
dest.y=(src0.y < src1.y) ? src0.y : src1.y;
dest.z=(src0.z < src1.z) ? src0.z : src1.z;
dest.w=(src0.w < src1.w) ? src0.w : src1.w;
```



## <a name="related-topics"></a><span data-ttu-id="42538-128">См. также</span><span class="sxs-lookup"><span data-stu-id="42538-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42538-129">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="42538-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




