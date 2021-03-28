---
title: СЖЕ — VS
description: Выдает знак, если первый источник больше или равен второму источнику.
ms.assetid: 88e8eb68-8189-40c3-b20e-f395576f5f6a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7bad8816b87a32c5f10c73df27beb3cc2aef7716
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412185"
---
# <a name="sge---vs"></a><span data-ttu-id="792ea-103">СЖЕ — VS</span><span class="sxs-lookup"><span data-stu-id="792ea-103">sge - vs</span></span>

<span data-ttu-id="792ea-104">Выдает знак, если первый источник больше или равен второму источнику.</span><span class="sxs-lookup"><span data-stu-id="792ea-104">Computes the sign if the first source is greater than or equal to the second source.</span></span>

## <a name="syntax"></a><span data-ttu-id="792ea-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="792ea-105">Syntax</span></span>



| <span data-ttu-id="792ea-106">СЖЕ DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="792ea-106">sge dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="792ea-107">где</span><span class="sxs-lookup"><span data-stu-id="792ea-107">where</span></span>

-   <span data-ttu-id="792ea-108">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="792ea-108">dst is the destination register.</span></span>
-   <span data-ttu-id="792ea-109">src0 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="792ea-109">src0 is a source register.</span></span>
-   <span data-ttu-id="792ea-110">src1 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="792ea-110">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="792ea-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="792ea-111">Remarks</span></span>



| <span data-ttu-id="792ea-112">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="792ea-112">Vertex shader versions</span></span> | <span data-ttu-id="792ea-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="792ea-113">1\_1</span></span> | <span data-ttu-id="792ea-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="792ea-114">2\_0</span></span> | <span data-ttu-id="792ea-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="792ea-115">2\_x</span></span> | <span data-ttu-id="792ea-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="792ea-116">2\_sw</span></span> | <span data-ttu-id="792ea-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="792ea-117">3\_0</span></span> | <span data-ttu-id="792ea-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="792ea-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="792ea-119">сже</span><span class="sxs-lookup"><span data-stu-id="792ea-119">sge</span></span>                    | <span data-ttu-id="792ea-120">x</span><span class="sxs-lookup"><span data-stu-id="792ea-120">x</span></span>    | <span data-ttu-id="792ea-121">x</span><span class="sxs-lookup"><span data-stu-id="792ea-121">x</span></span>    | <span data-ttu-id="792ea-122">x</span><span class="sxs-lookup"><span data-stu-id="792ea-122">x</span></span>    | <span data-ttu-id="792ea-123">x</span><span class="sxs-lookup"><span data-stu-id="792ea-123">x</span></span>     | <span data-ttu-id="792ea-124">x</span><span class="sxs-lookup"><span data-stu-id="792ea-124">x</span></span>    | <span data-ttu-id="792ea-125">x</span><span class="sxs-lookup"><span data-stu-id="792ea-125">x</span></span>     |



 

<span data-ttu-id="792ea-126">В следующем фрагменте кода показаны выполняемые операции.</span><span class="sxs-lookup"><span data-stu-id="792ea-126">The following code fragment shows the operations performed.</span></span>


```
 
dest.x = (src0.x >= src1.x) ? 1.0f : 0.0f;
dest.y = (src0.y >= src1.y) ? 1.0f : 0.0f;
dest.z = (src0.z >= src1.z) ? 1.0f : 0.0f;
dest.w = (src0.w >= src1.w) ? 1.0f : 0.0f;
```



## <a name="related-topics"></a><span data-ttu-id="792ea-127">См. также</span><span class="sxs-lookup"><span data-stu-id="792ea-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="792ea-128">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="792ea-128">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




