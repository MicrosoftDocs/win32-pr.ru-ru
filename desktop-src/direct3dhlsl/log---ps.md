---
title: log-PS
description: Полная точность журнала ₂ (x). | log-PS
ms.assetid: e540a082-5916-4111-b908-bb229c9e7dc8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a8face264d5221cf4b39f99260bec476ee5742f0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986690"
---
# <a name="log---ps"></a><span data-ttu-id="1de09-104">log-PS</span><span class="sxs-lookup"><span data-stu-id="1de09-104">log - ps</span></span>

<span data-ttu-id="1de09-105">Полная точность журнала ₂ (x).</span><span class="sxs-lookup"><span data-stu-id="1de09-105">Full precision log₂(x).</span></span>

## <a name="syntax"></a><span data-ttu-id="1de09-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1de09-106">Syntax</span></span>



| <span data-ttu-id="1de09-107">Журнал DST, src</span><span class="sxs-lookup"><span data-stu-id="1de09-107">log dst, src</span></span> |
|--------------|



 

<span data-ttu-id="1de09-108">где</span><span class="sxs-lookup"><span data-stu-id="1de09-108">where</span></span>

-   <span data-ttu-id="1de09-109">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="1de09-109">dst is the destination register.</span></span>
-   <span data-ttu-id="1de09-110">src является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="1de09-110">src is a source register.</span></span> <span data-ttu-id="1de09-111">Регистр исходного кода требует явного использования репликации свиззле; то есть необходимо указать только один из компонентов. x,. y,. z,. w свиззле (или. r,. g,. b,. a эквивалент).</span><span class="sxs-lookup"><span data-stu-id="1de09-111">Source register requires explicit use of replicate swizzle; that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="1de09-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="1de09-112">Remarks</span></span>



| <span data-ttu-id="1de09-113">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="1de09-113">Pixel shader versions</span></span> | <span data-ttu-id="1de09-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="1de09-114">1\_1</span></span> | <span data-ttu-id="1de09-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="1de09-115">1\_2</span></span> | <span data-ttu-id="1de09-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="1de09-116">1\_3</span></span> | <span data-ttu-id="1de09-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="1de09-117">1\_4</span></span> | <span data-ttu-id="1de09-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1de09-118">2\_0</span></span> | <span data-ttu-id="1de09-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="1de09-119">2\_x</span></span> | <span data-ttu-id="1de09-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="1de09-120">2\_sw</span></span> | <span data-ttu-id="1de09-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="1de09-121">3\_0</span></span> | <span data-ttu-id="1de09-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="1de09-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="1de09-123">log</span><span class="sxs-lookup"><span data-stu-id="1de09-123">log</span></span>                   |      |      |      |      | <span data-ttu-id="1de09-124">x</span><span class="sxs-lookup"><span data-stu-id="1de09-124">x</span></span>    | <span data-ttu-id="1de09-125">x</span><span class="sxs-lookup"><span data-stu-id="1de09-125">x</span></span>    | <span data-ttu-id="1de09-126">x</span><span class="sxs-lookup"><span data-stu-id="1de09-126">x</span></span>     | <span data-ttu-id="1de09-127">x</span><span class="sxs-lookup"><span data-stu-id="1de09-127">x</span></span>    | <span data-ttu-id="1de09-128">x</span><span class="sxs-lookup"><span data-stu-id="1de09-128">x</span></span>     |



 

<span data-ttu-id="1de09-129">В следующем фрагменте кода показаны выполняемые операции.</span><span class="sxs-lookup"><span data-stu-id="1de09-129">The following code snippet shows the operations performed.</span></span>


```
float v = abs(src);
if (v != 0)
{
    dest.x = dest.y = dest.z = dest.w = 
        (float)(log(v)/log(2));  
}
else
{
    dest.x = dest.y = dest.z = dest.w = -FLT_MAX;
}
```



<span data-ttu-id="1de09-130">Эта инструкция принимает скалярный источник, бит подписи которого не учитывается.</span><span class="sxs-lookup"><span data-stu-id="1de09-130">This instruction accepts a scalar source whose sign bit is ignored.</span></span> <span data-ttu-id="1de09-131">Результат реплицируется на все четыре канала.</span><span class="sxs-lookup"><span data-stu-id="1de09-131">The result is replicated to all four channels.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1de09-132">См. также</span><span class="sxs-lookup"><span data-stu-id="1de09-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1de09-133">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="1de09-133">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




