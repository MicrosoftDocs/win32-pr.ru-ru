---
title: ABS-VS
description: Вычисление абсолютного значения. | ABS-VS
ms.assetid: d3b4cf06-dc87-4c71-aa2d-5ade4cf98caa
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 612ed14fb538a419a0e7f0b1cf07904d654bb010
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343319"
---
# <a name="abs---vs"></a><span data-ttu-id="d2f47-104">ABS-VS</span><span class="sxs-lookup"><span data-stu-id="d2f47-104">abs - vs</span></span>

<span data-ttu-id="d2f47-105">Вычисление абсолютного значения.</span><span class="sxs-lookup"><span data-stu-id="d2f47-105">Computes absolute value.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2f47-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d2f47-106">Syntax</span></span>

<span data-ttu-id="d2f47-107">**ABS DST, src**</span><span class="sxs-lookup"><span data-stu-id="d2f47-107">**abs dst, src**</span></span>

<span data-ttu-id="d2f47-108">where</span><span class="sxs-lookup"><span data-stu-id="d2f47-108">where</span></span>

- <span data-ttu-id="d2f47-109">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="d2f47-109">dst is the destination register.</span></span>
- <span data-ttu-id="d2f47-110">src является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="d2f47-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2f47-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="d2f47-111">Remarks</span></span>



| <span data-ttu-id="d2f47-112">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="d2f47-112">Vertex shader versions</span></span> | <span data-ttu-id="d2f47-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="d2f47-113">1\_1</span></span> | <span data-ttu-id="d2f47-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d2f47-114">2\_0</span></span> | <span data-ttu-id="d2f47-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="d2f47-115">2\_x</span></span> | <span data-ttu-id="d2f47-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="d2f47-116">2\_sw</span></span> | <span data-ttu-id="d2f47-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d2f47-117">3\_0</span></span> | <span data-ttu-id="d2f47-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="d2f47-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="d2f47-119">abs</span><span class="sxs-lookup"><span data-stu-id="d2f47-119">abs</span></span>                    |      | <span data-ttu-id="d2f47-120">x</span><span class="sxs-lookup"><span data-stu-id="d2f47-120">x</span></span>    | <span data-ttu-id="d2f47-121">x</span><span class="sxs-lookup"><span data-stu-id="d2f47-121">x</span></span>    | <span data-ttu-id="d2f47-122">x</span><span class="sxs-lookup"><span data-stu-id="d2f47-122">x</span></span>     | <span data-ttu-id="d2f47-123">x</span><span class="sxs-lookup"><span data-stu-id="d2f47-123">x</span></span>    | <span data-ttu-id="d2f47-124">x</span><span class="sxs-lookup"><span data-stu-id="d2f47-124">x</span></span>     |



 

<span data-ttu-id="d2f47-125">Эта инструкция работает, как показано здесь.</span><span class="sxs-lookup"><span data-stu-id="d2f47-125">This instruction works as shown here.</span></span>


```
dest.x = abs(src.x)
dest.y = abs(src.y)
dest.z = abs(src.z)
dest.w = abs(src.w)
```



## <a name="related-topics"></a><span data-ttu-id="d2f47-126">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="d2f47-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2f47-127">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="d2f47-127">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




