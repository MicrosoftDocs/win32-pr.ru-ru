---
title: летнее время и
description: Вычисляет вектор расстояний. | летнее время и
ms.assetid: 4315a29f-58e7-427f-aaa0-1fe1a81eb392
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e41c1da0eae001d314e2682a3295a0b88b993ee1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914344"
---
# <a name="dst---vs"></a><span data-ttu-id="99bdf-104">летнее время и</span><span class="sxs-lookup"><span data-stu-id="99bdf-104">dst - vs</span></span>

<span data-ttu-id="99bdf-105">Вычисляет вектор расстояний.</span><span class="sxs-lookup"><span data-stu-id="99bdf-105">Calculates a distance vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="99bdf-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="99bdf-106">Syntax</span></span>



| <span data-ttu-id="99bdf-107">конечный DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="99bdf-107">dst dest, src0, src1</span></span> |
|----------------------|



 

<span data-ttu-id="99bdf-108">где</span><span class="sxs-lookup"><span data-stu-id="99bdf-108">where</span></span>

-   <span data-ttu-id="99bdf-109">dest — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="99bdf-109">dest is the destination register.</span></span>
-   <span data-ttu-id="99bdf-110">src0 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="99bdf-110">src0 is a source register.</span></span>
-   <span data-ttu-id="99bdf-111">src1 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="99bdf-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="99bdf-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="99bdf-112">Remarks</span></span>



| <span data-ttu-id="99bdf-113">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="99bdf-113">Vertex shader versions</span></span> | <span data-ttu-id="99bdf-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="99bdf-114">1\_1</span></span> | <span data-ttu-id="99bdf-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="99bdf-115">2\_0</span></span> | <span data-ttu-id="99bdf-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="99bdf-116">2\_x</span></span> | <span data-ttu-id="99bdf-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="99bdf-117">2\_sw</span></span> | <span data-ttu-id="99bdf-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="99bdf-118">3\_0</span></span> | <span data-ttu-id="99bdf-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="99bdf-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="99bdf-120">кон</span><span class="sxs-lookup"><span data-stu-id="99bdf-120">dst</span></span>                    | <span data-ttu-id="99bdf-121">x</span><span class="sxs-lookup"><span data-stu-id="99bdf-121">x</span></span>    | <span data-ttu-id="99bdf-122">x</span><span class="sxs-lookup"><span data-stu-id="99bdf-122">x</span></span>    | <span data-ttu-id="99bdf-123">x</span><span class="sxs-lookup"><span data-stu-id="99bdf-123">x</span></span>    | <span data-ttu-id="99bdf-124">x</span><span class="sxs-lookup"><span data-stu-id="99bdf-124">x</span></span>     | <span data-ttu-id="99bdf-125">x</span><span class="sxs-lookup"><span data-stu-id="99bdf-125">x</span></span>    | <span data-ttu-id="99bdf-126">x</span><span class="sxs-lookup"><span data-stu-id="99bdf-126">x</span></span>     |



 

<span data-ttu-id="99bdf-127">В следующем фрагменте кода показаны выполняемые операции.</span><span class="sxs-lookup"><span data-stu-id="99bdf-127">The following code fragment shows the operations performed:</span></span>


```
dest.x = 1;
dest.y = src0.y * src1.y;
dest.z = src0.z;
dest.w = src1.w;
```



<span data-ttu-id="99bdf-128">Предполагается, что первый исходный операнд (src0) является вектором (пропускается, d \* d, d \* d, игнорируется), а второй исходный операнд (src1) — вектором (игнорируется, 1/d, игнорируется, 1/d).</span><span class="sxs-lookup"><span data-stu-id="99bdf-128">The first source operand (src0) is assumed to be the vector (ignored, d\*d, d\*d, ignored) and the second source operand (src1) is assumed to be the vector (ignored, 1/d, ignored, 1/d).</span></span> <span data-ttu-id="99bdf-129">Назначение (dest) является вектором результата (1, d, d \* d, 1/d).</span><span class="sxs-lookup"><span data-stu-id="99bdf-129">The destination (dest) is the result vector (1, d, d\*d, 1/d).</span></span>

## <a name="related-topics"></a><span data-ttu-id="99bdf-130">См. также</span><span class="sxs-lookup"><span data-stu-id="99bdf-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99bdf-131">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="99bdf-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




