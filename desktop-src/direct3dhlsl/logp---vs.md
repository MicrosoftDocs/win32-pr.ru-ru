---
title: логп — VS
description: Частичная точность логп ₂ (x).
ms.assetid: 8547ca8a-7bde-4e41-9e65-f7fcd65454c1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0a261d63ad47dcf12728b8bcd0025ec578ede0b4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104069353"
---
# <a name="logp---vs"></a><span data-ttu-id="ab720-103">логп — VS</span><span class="sxs-lookup"><span data-stu-id="ab720-103">logp - vs</span></span>

<span data-ttu-id="ab720-104">Частичная точность логп ₂ (x).</span><span class="sxs-lookup"><span data-stu-id="ab720-104">Partial precision logp₂(x).</span></span>

## <a name="syntax"></a><span data-ttu-id="ab720-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ab720-105">Syntax</span></span>



| <span data-ttu-id="ab720-106">логп DST, src</span><span class="sxs-lookup"><span data-stu-id="ab720-106">logp dst, src</span></span> |
|---------------|



 

<span data-ttu-id="ab720-107">где</span><span class="sxs-lookup"><span data-stu-id="ab720-107">where</span></span>

-   <span data-ttu-id="ab720-108">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="ab720-108">dst is the destination register.</span></span>
-   <span data-ttu-id="ab720-109">src является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="ab720-109">src is a source register.</span></span> <span data-ttu-id="ab720-110">Для исходного регистра требуется явное использование репликации свиззле, то есть только один из компонентов. x,. y,. z,. w свиззле (или. r,. g,. b,. a эквивалент) должен быть указан.</span><span class="sxs-lookup"><span data-stu-id="ab720-110">Source register requires explicit use of replicate swizzle, that is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab720-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="ab720-111">Remarks</span></span>



| <span data-ttu-id="ab720-112">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="ab720-112">Vertex shader versions</span></span> | <span data-ttu-id="ab720-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="ab720-113">1\_1</span></span> | <span data-ttu-id="ab720-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ab720-114">2\_0</span></span> | <span data-ttu-id="ab720-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="ab720-115">2\_x</span></span> | <span data-ttu-id="ab720-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="ab720-116">2\_sw</span></span> | <span data-ttu-id="ab720-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ab720-117">3\_0</span></span> | <span data-ttu-id="ab720-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="ab720-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="ab720-119">логп</span><span class="sxs-lookup"><span data-stu-id="ab720-119">logp</span></span>                   | <span data-ttu-id="ab720-120">x</span><span class="sxs-lookup"><span data-stu-id="ab720-120">x</span></span>    | <span data-ttu-id="ab720-121">x</span><span class="sxs-lookup"><span data-stu-id="ab720-121">x</span></span>    | <span data-ttu-id="ab720-122">x</span><span class="sxs-lookup"><span data-stu-id="ab720-122">x</span></span>    | <span data-ttu-id="ab720-123">x</span><span class="sxs-lookup"><span data-stu-id="ab720-123">x</span></span>     | <span data-ttu-id="ab720-124">x</span><span class="sxs-lookup"><span data-stu-id="ab720-124">x</span></span>    | <span data-ttu-id="ab720-125">x</span><span class="sxs-lookup"><span data-stu-id="ab720-125">x</span></span>     |



 

<span data-ttu-id="ab720-126">В следующем фрагменте кода показаны выполняемые операции.</span><span class="sxs-lookup"><span data-stu-id="ab720-126">The following code fragment shows the operations performed.</span></span>


```
float f = abs(src);
if (f != 0)
    dest.x = dest.y = dest.z = dest.w = (float)(log(f)/log(2));
else
    dest.x = dest.y = dest.z = dest.w = -FLT_MAX;   
```



<span data-ttu-id="ab720-127">Эта инструкция предоставляет логарифм с основанием 2 с частичным точностью до 10 бит.</span><span class="sxs-lookup"><span data-stu-id="ab720-127">This instruction provides logarithm base 2 partial precision, up to 10 bits.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ab720-128">См. также</span><span class="sxs-lookup"><span data-stu-id="ab720-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab720-129">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="ab720-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




