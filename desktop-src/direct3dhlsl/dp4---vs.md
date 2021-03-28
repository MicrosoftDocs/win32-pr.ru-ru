---
title: DP4 — VS
description: Выполняет вычисление 4-компонентного произведения исходных регистров. | DP4 — VS
ms.assetid: ee3d3c8d-6031-4264-80ba-2b200a721310
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 747695436094dd5d2e9787e3eeca525b292f14c4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986361"
---
# <a name="dp4---vs"></a><span data-ttu-id="a04ab-104">DP4 — VS</span><span class="sxs-lookup"><span data-stu-id="a04ab-104">dp4 - vs</span></span>

<span data-ttu-id="a04ab-105">Выполняет вычисление 4-компонентного произведения исходных регистров.</span><span class="sxs-lookup"><span data-stu-id="a04ab-105">Computes the four-component dot product of the source registers.</span></span>

## <a name="syntax"></a><span data-ttu-id="a04ab-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a04ab-106">Syntax</span></span>



| <span data-ttu-id="a04ab-107">DP4 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="a04ab-107">dp4 dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="a04ab-108">где</span><span class="sxs-lookup"><span data-stu-id="a04ab-108">where</span></span>

-   <span data-ttu-id="a04ab-109">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="a04ab-109">dst is the destination register.</span></span>
-   <span data-ttu-id="a04ab-110">src0 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="a04ab-110">src0 is a source register.</span></span>
-   <span data-ttu-id="a04ab-111">src1 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="a04ab-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="a04ab-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="a04ab-112">Remarks</span></span>



| <span data-ttu-id="a04ab-113">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="a04ab-113">Vertex shader versions</span></span> | <span data-ttu-id="a04ab-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="a04ab-114">1\_1</span></span> | <span data-ttu-id="a04ab-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a04ab-115">2\_0</span></span> | <span data-ttu-id="a04ab-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a04ab-116">2\_x</span></span> | <span data-ttu-id="a04ab-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a04ab-117">2\_sw</span></span> | <span data-ttu-id="a04ab-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a04ab-118">3\_0</span></span> | <span data-ttu-id="a04ab-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a04ab-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="a04ab-120">dp4</span><span class="sxs-lookup"><span data-stu-id="a04ab-120">dp4</span></span>                    | <span data-ttu-id="a04ab-121">x</span><span class="sxs-lookup"><span data-stu-id="a04ab-121">x</span></span>    | <span data-ttu-id="a04ab-122">x</span><span class="sxs-lookup"><span data-stu-id="a04ab-122">x</span></span>    | <span data-ttu-id="a04ab-123">x</span><span class="sxs-lookup"><span data-stu-id="a04ab-123">x</span></span>    | <span data-ttu-id="a04ab-124">x</span><span class="sxs-lookup"><span data-stu-id="a04ab-124">x</span></span>     | <span data-ttu-id="a04ab-125">x</span><span class="sxs-lookup"><span data-stu-id="a04ab-125">x</span></span>    | <span data-ttu-id="a04ab-126">x</span><span class="sxs-lookup"><span data-stu-id="a04ab-126">x</span></span>     |



 

<span data-ttu-id="a04ab-127">В следующем фрагменте кода показаны выполняемые операции.</span><span class="sxs-lookup"><span data-stu-id="a04ab-127">The following code fragment shows the operations performed:</span></span>


```
dest.w = (src0.x * src1.x) + (src0.y * src1.y) + 
         (src0.z * src1.z) + (src0.w * src1.w);
dest.x = dest.y = dest.z = dest.w;
```



## <a name="related-topics"></a><span data-ttu-id="a04ab-128">См. также</span><span class="sxs-lookup"><span data-stu-id="a04ab-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a04ab-129">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="a04ab-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




