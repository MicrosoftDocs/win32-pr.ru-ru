---
title: DP3 — VS
description: Выполняет вычисление 3-компонентного произведения исходных регистров. | DP3 — VS
ms.assetid: a5263a18-ed53-41eb-85ca-2cff872e03d8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 81580401f25ddcf7ce1c1d53475d0c3beba74a89
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273391"
---
# <a name="dp3---vs"></a><span data-ttu-id="03850-104">DP3 — VS</span><span class="sxs-lookup"><span data-stu-id="03850-104">dp3 - vs</span></span>

<span data-ttu-id="03850-105">Выполняет вычисление 3-компонентного произведения исходных регистров.</span><span class="sxs-lookup"><span data-stu-id="03850-105">Computes the three-component dot product of the source registers.</span></span>

## <a name="syntax"></a><span data-ttu-id="03850-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="03850-106">Syntax</span></span>



| <span data-ttu-id="03850-107">DP3 DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="03850-107">dp3 dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="03850-108">где</span><span class="sxs-lookup"><span data-stu-id="03850-108">where</span></span>

-   <span data-ttu-id="03850-109">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="03850-109">dst is the destination register.</span></span>
-   <span data-ttu-id="03850-110">src0 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="03850-110">src0 is a source register.</span></span>
-   <span data-ttu-id="03850-111">src1 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="03850-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="03850-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="03850-112">Remarks</span></span>



| <span data-ttu-id="03850-113">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="03850-113">Vertex shader versions</span></span> | <span data-ttu-id="03850-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="03850-114">1\_1</span></span> | <span data-ttu-id="03850-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="03850-115">2\_0</span></span> | <span data-ttu-id="03850-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="03850-116">2\_x</span></span> | <span data-ttu-id="03850-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="03850-117">2\_sw</span></span> | <span data-ttu-id="03850-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="03850-118">3\_0</span></span> | <span data-ttu-id="03850-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="03850-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="03850-120">dp3</span><span class="sxs-lookup"><span data-stu-id="03850-120">dp3</span></span>                    | <span data-ttu-id="03850-121">x</span><span class="sxs-lookup"><span data-stu-id="03850-121">x</span></span>    | <span data-ttu-id="03850-122">x</span><span class="sxs-lookup"><span data-stu-id="03850-122">x</span></span>    | <span data-ttu-id="03850-123">x</span><span class="sxs-lookup"><span data-stu-id="03850-123">x</span></span>    | <span data-ttu-id="03850-124">x</span><span class="sxs-lookup"><span data-stu-id="03850-124">x</span></span>     | <span data-ttu-id="03850-125">x</span><span class="sxs-lookup"><span data-stu-id="03850-125">x</span></span>    | <span data-ttu-id="03850-126">x</span><span class="sxs-lookup"><span data-stu-id="03850-126">x</span></span>     |



 

<span data-ttu-id="03850-127">В следующем фрагменте кода показаны выполняемые операции.</span><span class="sxs-lookup"><span data-stu-id="03850-127">The following code fragment shows the operations performed:</span></span>


```
dest.w = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
dest.x = dest.y = dest.z = dest.w;
```



## <a name="related-topics"></a><span data-ttu-id="03850-128">См. также</span><span class="sxs-lookup"><span data-stu-id="03850-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03850-129">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="03850-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




