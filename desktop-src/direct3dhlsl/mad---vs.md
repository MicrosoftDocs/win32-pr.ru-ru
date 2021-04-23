---
title: Mad — VS
description: Умножает и добавляет источники.
ms.assetid: 059f0bf6-d143-4efc-b074-0ed026edb008
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 01e96bb63395fe9e5dd27a17fbb5c0ddd9bf3c17
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335520"
---
# <a name="mad---vs"></a><span data-ttu-id="a0b12-103">Mad — VS</span><span class="sxs-lookup"><span data-stu-id="a0b12-103">mad - vs</span></span>

<span data-ttu-id="a0b12-104">Умножает и добавляет источники.</span><span class="sxs-lookup"><span data-stu-id="a0b12-104">Multiplies and adds sources.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0b12-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a0b12-105">Syntax</span></span>



| <span data-ttu-id="a0b12-106">Mad DST, src0, src1, src2</span><span class="sxs-lookup"><span data-stu-id="a0b12-106">mad dst, src0, src1, src2</span></span> |
|---------------------------|



 

<span data-ttu-id="a0b12-107">где</span><span class="sxs-lookup"><span data-stu-id="a0b12-107">where</span></span>

-   <span data-ttu-id="a0b12-108">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="a0b12-108">dst is the destination register.</span></span>
-   <span data-ttu-id="a0b12-109">src0 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="a0b12-109">src0 is a source register.</span></span>
-   <span data-ttu-id="a0b12-110">src1 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="a0b12-110">src1 is a source register.</span></span>
-   <span data-ttu-id="a0b12-111">src2 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="a0b12-111">src2 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0b12-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="a0b12-112">Remarks</span></span>



| <span data-ttu-id="a0b12-113">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="a0b12-113">Vertex shader versions</span></span> | <span data-ttu-id="a0b12-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="a0b12-114">1\_1</span></span> | <span data-ttu-id="a0b12-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a0b12-115">2\_0</span></span> | <span data-ttu-id="a0b12-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a0b12-116">2\_x</span></span> | <span data-ttu-id="a0b12-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a0b12-117">2\_sw</span></span> | <span data-ttu-id="a0b12-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a0b12-118">3\_0</span></span> | <span data-ttu-id="a0b12-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a0b12-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="a0b12-120">отслеживания</span><span class="sxs-lookup"><span data-stu-id="a0b12-120">mad</span></span>                    | <span data-ttu-id="a0b12-121">x</span><span class="sxs-lookup"><span data-stu-id="a0b12-121">x</span></span>    | <span data-ttu-id="a0b12-122">x</span><span class="sxs-lookup"><span data-stu-id="a0b12-122">x</span></span>    | <span data-ttu-id="a0b12-123">x</span><span class="sxs-lookup"><span data-stu-id="a0b12-123">x</span></span>    | <span data-ttu-id="a0b12-124">x</span><span class="sxs-lookup"><span data-stu-id="a0b12-124">x</span></span>     | <span data-ttu-id="a0b12-125">x</span><span class="sxs-lookup"><span data-stu-id="a0b12-125">x</span></span>    | <span data-ttu-id="a0b12-126">x</span><span class="sxs-lookup"><span data-stu-id="a0b12-126">x</span></span>     |



 

<span data-ttu-id="a0b12-127">В следующем фрагменте кода показаны выполняемые операции.</span><span class="sxs-lookup"><span data-stu-id="a0b12-127">The following code fragment shows the operations performed.</span></span>


```
dest.x = src0.x * src1.x + src2.x;
dest.y = src0.y * src1.y + src2.y;
dest.z = src0.z * src1.z + src2.z;
dest.w = src0.w * src1.w + src2.w;
```



## <a name="related-topics"></a><span data-ttu-id="a0b12-128">См. также</span><span class="sxs-lookup"><span data-stu-id="a0b12-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0b12-129">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="a0b12-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




