---
title: Сравнение журналов и
description: Полная точность журнала ₂ (x). | Сравнение журналов и
ms.assetid: 53c91825-ec54-4b04-bf08-52d4b1c5122d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b9e0564ab5b38943017e61bde171d0db3060ca0c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273540"
---
# <a name="log---vs"></a><span data-ttu-id="35937-104">Сравнение журналов и</span><span class="sxs-lookup"><span data-stu-id="35937-104">log - vs</span></span>

<span data-ttu-id="35937-105">Полная точность журнала ₂ (x).</span><span class="sxs-lookup"><span data-stu-id="35937-105">Full precision log₂(x).</span></span>

## <a name="syntax"></a><span data-ttu-id="35937-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="35937-106">Syntax</span></span>



| <span data-ttu-id="35937-107">Журнал DST, src</span><span class="sxs-lookup"><span data-stu-id="35937-107">log dst, src</span></span> |
|--------------|



 

<span data-ttu-id="35937-108">где</span><span class="sxs-lookup"><span data-stu-id="35937-108">where</span></span>

-   <span data-ttu-id="35937-109">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="35937-109">dst is the destination register.</span></span>
-   <span data-ttu-id="35937-110">src является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="35937-110">src is a source register.</span></span> <span data-ttu-id="35937-111">Для исходного регистра требуется явное использование репликации свиззле, то есть только один из компонентов. x,. y,. z,. w свиззле (или. r,. g,. b,. a эквивалент) должен быть указан.</span><span class="sxs-lookup"><span data-stu-id="35937-111">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="35937-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="35937-112">Remarks</span></span>



| <span data-ttu-id="35937-113">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="35937-113">Vertex shader versions</span></span> | <span data-ttu-id="35937-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="35937-114">1\_1</span></span> | <span data-ttu-id="35937-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="35937-115">2\_0</span></span> | <span data-ttu-id="35937-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="35937-116">2\_x</span></span> | <span data-ttu-id="35937-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="35937-117">2\_sw</span></span> | <span data-ttu-id="35937-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="35937-118">3\_0</span></span> | <span data-ttu-id="35937-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="35937-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="35937-120">log</span><span class="sxs-lookup"><span data-stu-id="35937-120">log</span></span>                    | <span data-ttu-id="35937-121">x</span><span class="sxs-lookup"><span data-stu-id="35937-121">x</span></span>    | <span data-ttu-id="35937-122">x</span><span class="sxs-lookup"><span data-stu-id="35937-122">x</span></span>    | <span data-ttu-id="35937-123">x</span><span class="sxs-lookup"><span data-stu-id="35937-123">x</span></span>    | <span data-ttu-id="35937-124">x</span><span class="sxs-lookup"><span data-stu-id="35937-124">x</span></span>     | <span data-ttu-id="35937-125">x</span><span class="sxs-lookup"><span data-stu-id="35937-125">x</span></span>    | <span data-ttu-id="35937-126">x</span><span class="sxs-lookup"><span data-stu-id="35937-126">x</span></span>     |



 

<span data-ttu-id="35937-127">В следующем фрагменте кода показаны выполняемые операции.</span><span class="sxs-lookup"><span data-stu-id="35937-127">The following code fragment shows the operations performed.</span></span>


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



<span data-ttu-id="35937-128">Эта инструкция принимает скалярный источник, бит подписи которого не учитывается.</span><span class="sxs-lookup"><span data-stu-id="35937-128">This instruction accepts a scalar source whose sign bit is ignored.</span></span> <span data-ttu-id="35937-129">Результат реплицируется на все четыре канала.</span><span class="sxs-lookup"><span data-stu-id="35937-129">The result is replicated to all four channels.</span></span>

<span data-ttu-id="35937-130">Эта инструкция предоставляет 21 бит точности.</span><span class="sxs-lookup"><span data-stu-id="35937-130">This instruction provides 21 bits of precision.</span></span>

## <a name="related-topics"></a><span data-ttu-id="35937-131">См. также</span><span class="sxs-lookup"><span data-stu-id="35937-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35937-132">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="35937-132">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




