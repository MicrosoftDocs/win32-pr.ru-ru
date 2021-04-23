---
title: rcp — VS
description: Выполняет вычисление обратной стороны исходного скаляра. | rcp — VS
ms.assetid: be638a42-b693-461d-ab0a-3a6c0fa1acfc
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 145a998cbca9dc3721d9c7d6ba251d539286a3f1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986684"
---
# <a name="rcp---vs"></a><span data-ttu-id="e338d-104">rcp — VS</span><span class="sxs-lookup"><span data-stu-id="e338d-104">rcp - vs</span></span>

<span data-ttu-id="e338d-105">Выполняет вычисление обратной стороны исходного скаляра.</span><span class="sxs-lookup"><span data-stu-id="e338d-105">Computes the reciprocal of the source scalar.</span></span>

## <a name="syntax"></a><span data-ttu-id="e338d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e338d-106">Syntax</span></span>



| <span data-ttu-id="e338d-107">rcp DST, src</span><span class="sxs-lookup"><span data-stu-id="e338d-107">rcp dst, src</span></span> |
|--------------|



 

<span data-ttu-id="e338d-108">где</span><span class="sxs-lookup"><span data-stu-id="e338d-108">where</span></span>

-   <span data-ttu-id="e338d-109">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="e338d-109">dst is the destination register.</span></span>
-   <span data-ttu-id="e338d-110">src является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="e338d-110">src is a source register.</span></span> <span data-ttu-id="e338d-111">Для исходного регистра требуется явное использование репликации свиззле, то есть только один из компонентов. x,. y,. z,. w свиззле (или. r,. g,. b,. a эквивалент) должен быть указан.</span><span class="sxs-lookup"><span data-stu-id="e338d-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="e338d-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="e338d-112">Remarks</span></span>



| <span data-ttu-id="e338d-113">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="e338d-113">Vertex shader versions</span></span> | <span data-ttu-id="e338d-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="e338d-114">1\_1</span></span> | <span data-ttu-id="e338d-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e338d-115">2\_0</span></span> | <span data-ttu-id="e338d-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e338d-116">2\_x</span></span> | <span data-ttu-id="e338d-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e338d-117">2\_sw</span></span> | <span data-ttu-id="e338d-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e338d-118">3\_0</span></span> | <span data-ttu-id="e338d-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e338d-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="e338d-120">rcp</span><span class="sxs-lookup"><span data-stu-id="e338d-120">rcp</span></span>                    | <span data-ttu-id="e338d-121">x</span><span class="sxs-lookup"><span data-stu-id="e338d-121">x</span></span>    | <span data-ttu-id="e338d-122">x</span><span class="sxs-lookup"><span data-stu-id="e338d-122">x</span></span>    | <span data-ttu-id="e338d-123">x</span><span class="sxs-lookup"><span data-stu-id="e338d-123">x</span></span>    | <span data-ttu-id="e338d-124">x</span><span class="sxs-lookup"><span data-stu-id="e338d-124">x</span></span>     | <span data-ttu-id="e338d-125">x</span><span class="sxs-lookup"><span data-stu-id="e338d-125">x</span></span>    | <span data-ttu-id="e338d-126">x</span><span class="sxs-lookup"><span data-stu-id="e338d-126">x</span></span>     |



 

<span data-ttu-id="e338d-127">В следующем фрагменте кода показаны выполняемые операции.</span><span class="sxs-lookup"><span data-stu-id="e338d-127">The following code fragment shows the operations performed.</span></span>


```
float f = src0;
if(f == 0.0f)
{
    f = FLT_MAX;
}
else 
{
    if(f != 1.0)
    {
        f = 1/f;
    }
}

dest = f;
```



<span data-ttu-id="e338d-128">Если входные данные представляют собой ровно 1,0, выходные данные должны быть ровно 1,0.</span><span class="sxs-lookup"><span data-stu-id="e338d-128">The output must be exactly 1.0 if the input is exactly 1.0.</span></span> <span data-ttu-id="e338d-129">Источник 0,0 дает бесконечное значение.</span><span class="sxs-lookup"><span data-stu-id="e338d-129">A source of 0.0 yields infinity.</span></span>

<span data-ttu-id="e338d-130">Точность должна составлять по крайней мере 1,0/(2 ²) абсолютную ошибку в диапазоне (1,0, 2,0), так как распространенные реализации будут разделять мантисса и экспоненту.</span><span class="sxs-lookup"><span data-stu-id="e338d-130">Precision should be at least 1.0/(2²²) absolute error over the range (1.0, 2.0) because common implementations will separate mantissa and exponent.</span></span>

<span data-ttu-id="e338d-131">Если у источника нет индексов, используется компонент x.</span><span class="sxs-lookup"><span data-stu-id="e338d-131">If the source has no subscripts, the x-component is used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e338d-132">См. также</span><span class="sxs-lookup"><span data-stu-id="e338d-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e338d-133">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="e338d-133">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




