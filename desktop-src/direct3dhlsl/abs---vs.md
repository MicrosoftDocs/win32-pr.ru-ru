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
ms.openlocfilehash: 07667954de97e2a1da3999237930fb33796d9030
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273392"
---
# <a name="abs---vs"></a><span data-ttu-id="30a94-104">ABS-VS</span><span class="sxs-lookup"><span data-stu-id="30a94-104">abs - vs</span></span>

<span data-ttu-id="30a94-105">Вычисление абсолютного значения.</span><span class="sxs-lookup"><span data-stu-id="30a94-105">Computes absolute value.</span></span>

## <a name="syntax"></a><span data-ttu-id="30a94-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="30a94-106">Syntax</span></span>



|              |
|--------------|
| <span data-ttu-id="30a94-107">ABS DST, src</span><span class="sxs-lookup"><span data-stu-id="30a94-107">abs dst, src</span></span> |



 

<span data-ttu-id="30a94-108">где</span><span class="sxs-lookup"><span data-stu-id="30a94-108">where</span></span>

-   <span data-ttu-id="30a94-109">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="30a94-109">dst is the destination register.</span></span>
-   <span data-ttu-id="30a94-110">src является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="30a94-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="30a94-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="30a94-111">Remarks</span></span>



|                        |      |      |      |       |      |       |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="30a94-112">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="30a94-112">Vertex shader versions</span></span> | <span data-ttu-id="30a94-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="30a94-113">1\_1</span></span> | <span data-ttu-id="30a94-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="30a94-114">2\_0</span></span> | <span data-ttu-id="30a94-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="30a94-115">2\_x</span></span> | <span data-ttu-id="30a94-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="30a94-116">2\_sw</span></span> | <span data-ttu-id="30a94-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="30a94-117">3\_0</span></span> | <span data-ttu-id="30a94-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="30a94-118">3\_sw</span></span> |
| <span data-ttu-id="30a94-119">abs</span><span class="sxs-lookup"><span data-stu-id="30a94-119">abs</span></span>                    |      | <span data-ttu-id="30a94-120">x</span><span class="sxs-lookup"><span data-stu-id="30a94-120">x</span></span>    | <span data-ttu-id="30a94-121">x</span><span class="sxs-lookup"><span data-stu-id="30a94-121">x</span></span>    | <span data-ttu-id="30a94-122">x</span><span class="sxs-lookup"><span data-stu-id="30a94-122">x</span></span>     | <span data-ttu-id="30a94-123">x</span><span class="sxs-lookup"><span data-stu-id="30a94-123">x</span></span>    | <span data-ttu-id="30a94-124">x</span><span class="sxs-lookup"><span data-stu-id="30a94-124">x</span></span>     |



 

<span data-ttu-id="30a94-125">Эта инструкция работает, как показано здесь.</span><span class="sxs-lookup"><span data-stu-id="30a94-125">This instruction works as shown here.</span></span>


```
dest.x = abs(src.x)
dest.y = abs(src.y)
dest.z = abs(src.z)
dest.w = abs(src.w)
```



## <a name="related-topics"></a><span data-ttu-id="30a94-126">См. также</span><span class="sxs-lookup"><span data-stu-id="30a94-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30a94-127">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="30a94-127">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




