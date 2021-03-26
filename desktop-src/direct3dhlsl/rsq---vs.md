---
title: РСК — VS
description: Вычисляет значение корня обратного квадрата (только положительный) исходного скаляра. | РСК — VS
ms.assetid: 1ac37dad-0cea-41af-8dae-f299896462b1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f477d6f7d8a7ff94472c689bf5844183e2f016ee
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986560"
---
# <a name="rsq---vs"></a><span data-ttu-id="f5bc1-104">РСК — VS</span><span class="sxs-lookup"><span data-stu-id="f5bc1-104">rsq - vs</span></span>

<span data-ttu-id="f5bc1-105">Вычисляет значение корня обратного квадрата (только положительный) исходного скаляра.</span><span class="sxs-lookup"><span data-stu-id="f5bc1-105">Computes the reciprocal square root (positive only) of the source scalar.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5bc1-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f5bc1-106">Syntax</span></span>



| <span data-ttu-id="f5bc1-107">РСК DST, src</span><span class="sxs-lookup"><span data-stu-id="f5bc1-107">rsq dst, src</span></span> |
|--------------|



 

<span data-ttu-id="f5bc1-108">где</span><span class="sxs-lookup"><span data-stu-id="f5bc1-108">where</span></span>

-   <span data-ttu-id="f5bc1-109">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="f5bc1-109">dst is the destination register.</span></span>
-   <span data-ttu-id="f5bc1-110">src является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="f5bc1-110">src is a source register.</span></span> <span data-ttu-id="f5bc1-111">Для исходного регистра требуется явное использование репликации свиззле, то есть только один из компонентов. x,. y,. z,. w свиззле (или. r,. g,. b,. a эквивалент) должен быть указан.</span><span class="sxs-lookup"><span data-stu-id="f5bc1-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5bc1-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="f5bc1-112">Remarks</span></span>



| <span data-ttu-id="f5bc1-113">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="f5bc1-113">Vertex shader versions</span></span> | <span data-ttu-id="f5bc1-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="f5bc1-114">1\_1</span></span> | <span data-ttu-id="f5bc1-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f5bc1-115">2\_0</span></span> | <span data-ttu-id="f5bc1-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="f5bc1-116">2\_x</span></span> | <span data-ttu-id="f5bc1-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f5bc1-117">2\_sw</span></span> | <span data-ttu-id="f5bc1-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f5bc1-118">3\_0</span></span> | <span data-ttu-id="f5bc1-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f5bc1-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="f5bc1-120">рск</span><span class="sxs-lookup"><span data-stu-id="f5bc1-120">rsq</span></span>                    | <span data-ttu-id="f5bc1-121">x</span><span class="sxs-lookup"><span data-stu-id="f5bc1-121">x</span></span>    | <span data-ttu-id="f5bc1-122">x</span><span class="sxs-lookup"><span data-stu-id="f5bc1-122">x</span></span>    | <span data-ttu-id="f5bc1-123">x</span><span class="sxs-lookup"><span data-stu-id="f5bc1-123">x</span></span>    | <span data-ttu-id="f5bc1-124">x</span><span class="sxs-lookup"><span data-stu-id="f5bc1-124">x</span></span>     | <span data-ttu-id="f5bc1-125">x</span><span class="sxs-lookup"><span data-stu-id="f5bc1-125">x</span></span>    | <span data-ttu-id="f5bc1-126">x</span><span class="sxs-lookup"><span data-stu-id="f5bc1-126">x</span></span>     |



 

<span data-ttu-id="f5bc1-127">В следующем фрагменте кода показаны выполняемые операции.</span><span class="sxs-lookup"><span data-stu-id="f5bc1-127">The following code fragment shows the operations performed.</span></span>


```
float f = abs(src0);
if (f == 0)
    f = FLT_MAX
else
{
    if (f != 1.0)
        f = 1.0/(float)sqrt(f);
}

dest.z = dest.y = dest.z = dest.w = f;
```



<span data-ttu-id="f5bc1-128">Абсолютное значение берется перед обработкой.</span><span class="sxs-lookup"><span data-stu-id="f5bc1-128">The absolute value is taken before processing.</span></span>

<span data-ttu-id="f5bc1-129">Точность должна составлять по крайней мере 1,0/(2 ²) абсолютную ошибку в диапазоне (1,0, 4,0), так как распространенные реализации будут разделять мантисса и экспоненту.</span><span class="sxs-lookup"><span data-stu-id="f5bc1-129">Precision should be at least 1.0/(2²²) absolute error over the range (1.0, 4.0) because common implementations will separate mantissa and exponent.</span></span>

<span data-ttu-id="f5bc1-130">Если в источнике нет индексов, используется компонент x.</span><span class="sxs-lookup"><span data-stu-id="f5bc1-130">If source has no subscripts, the x-component is used.</span></span> <span data-ttu-id="f5bc1-131">Если входные данные представляют собой ровно 1,0, выходные данные должны быть ровно 1,0.</span><span class="sxs-lookup"><span data-stu-id="f5bc1-131">The output must be exactly 1.0 if the input is exactly 1.0.</span></span> <span data-ttu-id="f5bc1-132">Источник 0,0 дает бесконечное значение.</span><span class="sxs-lookup"><span data-stu-id="f5bc1-132">A source of 0.0 yields infinity.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f5bc1-133">См. также</span><span class="sxs-lookup"><span data-stu-id="f5bc1-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5bc1-134">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="f5bc1-134">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




