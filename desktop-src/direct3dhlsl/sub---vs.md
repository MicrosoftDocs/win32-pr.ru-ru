---
title: Подсистема VS
description: Вычитает источники. | Подсистема VS
ms.assetid: ccd7ca57-05a9-4ee8-8bda-c8c875476aaf
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a4bf15522798e1da5ec0bde5b729f241ff9dabde
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104000183"
---
# <a name="sub---vs"></a><span data-ttu-id="3d566-104">Подсистема VS</span><span class="sxs-lookup"><span data-stu-id="3d566-104">sub - vs</span></span>

<span data-ttu-id="3d566-105">Вычитает источники.</span><span class="sxs-lookup"><span data-stu-id="3d566-105">Subtracts sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d566-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3d566-106">Syntax</span></span>



| <span data-ttu-id="3d566-107">дополнительный DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="3d566-107">sub dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="3d566-108">где</span><span class="sxs-lookup"><span data-stu-id="3d566-108">where</span></span>

-   <span data-ttu-id="3d566-109">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="3d566-109">dst is the destination register.</span></span>
-   <span data-ttu-id="3d566-110">src0 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="3d566-110">src0 is a source register.</span></span>
-   <span data-ttu-id="3d566-111">src1 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="3d566-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d566-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="3d566-112">Remarks</span></span>



| <span data-ttu-id="3d566-113">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="3d566-113">Vertex shader versions</span></span> | <span data-ttu-id="3d566-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="3d566-114">1\_1</span></span> | <span data-ttu-id="3d566-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3d566-115">2\_0</span></span> | <span data-ttu-id="3d566-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="3d566-116">2\_x</span></span> | <span data-ttu-id="3d566-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3d566-117">2\_sw</span></span> | <span data-ttu-id="3d566-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3d566-118">3\_0</span></span> | <span data-ttu-id="3d566-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="3d566-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="3d566-120">sub</span><span class="sxs-lookup"><span data-stu-id="3d566-120">sub</span></span>                    | <span data-ttu-id="3d566-121">x</span><span class="sxs-lookup"><span data-stu-id="3d566-121">x</span></span>    | <span data-ttu-id="3d566-122">x</span><span class="sxs-lookup"><span data-stu-id="3d566-122">x</span></span>    | <span data-ttu-id="3d566-123">x</span><span class="sxs-lookup"><span data-stu-id="3d566-123">x</span></span>    | <span data-ttu-id="3d566-124">x</span><span class="sxs-lookup"><span data-stu-id="3d566-124">x</span></span>     | <span data-ttu-id="3d566-125">x</span><span class="sxs-lookup"><span data-stu-id="3d566-125">x</span></span>    | <span data-ttu-id="3d566-126">x</span><span class="sxs-lookup"><span data-stu-id="3d566-126">x</span></span>     |



 

<span data-ttu-id="3d566-127">Эта инструкция выполняет вычитание, показанное в этой формуле.</span><span class="sxs-lookup"><span data-stu-id="3d566-127">This instruction performs the subtraction shown in this formula.</span></span>


```
dest.x = src0.x - src1.x
dest.y = src0.y - src1.y
dest.z = src0.z - src1.z
dest.w = src0.w - src1.w
```



## <a name="related-topics"></a><span data-ttu-id="3d566-128">См. также</span><span class="sxs-lookup"><span data-stu-id="3d566-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d566-129">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="3d566-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




