---
title: НРМ — VS
description: Нормализация трехмерного вектора. | НРМ — VS
ms.assetid: 735e9971-c0c3-4648-8362-58bda6fac46a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0e696277136826294392149c4b7430e4c75f9d9a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273520"
---
# <a name="nrm---vs"></a><span data-ttu-id="d26ff-104">НРМ — VS</span><span class="sxs-lookup"><span data-stu-id="d26ff-104">nrm - vs</span></span>

<span data-ttu-id="d26ff-105">Нормализация трехмерного вектора.</span><span class="sxs-lookup"><span data-stu-id="d26ff-105">Normalize a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="d26ff-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d26ff-106">Syntax</span></span>



| <span data-ttu-id="d26ff-107">НРМ DST, src</span><span class="sxs-lookup"><span data-stu-id="d26ff-107">nrm dst, src</span></span> |
|--------------|



 

<span data-ttu-id="d26ff-108">где</span><span class="sxs-lookup"><span data-stu-id="d26ff-108">where</span></span>

-   <span data-ttu-id="d26ff-109">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="d26ff-109">dst is the destination register.</span></span>
-   <span data-ttu-id="d26ff-110">src является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="d26ff-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="d26ff-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="d26ff-111">Remarks</span></span>



| <span data-ttu-id="d26ff-112">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="d26ff-112">Vertex shader versions</span></span> | <span data-ttu-id="d26ff-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="d26ff-113">1\_1</span></span> | <span data-ttu-id="d26ff-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d26ff-114">2\_0</span></span> | <span data-ttu-id="d26ff-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="d26ff-115">2\_x</span></span> | <span data-ttu-id="d26ff-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="d26ff-116">2\_sw</span></span> | <span data-ttu-id="d26ff-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="d26ff-117">3\_0</span></span> | <span data-ttu-id="d26ff-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="d26ff-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="d26ff-119">нрм</span><span class="sxs-lookup"><span data-stu-id="d26ff-119">nrm</span></span>                    |      | <span data-ttu-id="d26ff-120">x</span><span class="sxs-lookup"><span data-stu-id="d26ff-120">x</span></span>    | <span data-ttu-id="d26ff-121">x</span><span class="sxs-lookup"><span data-stu-id="d26ff-121">x</span></span>    | <span data-ttu-id="d26ff-122">x</span><span class="sxs-lookup"><span data-stu-id="d26ff-122">x</span></span>     | <span data-ttu-id="d26ff-123">x</span><span class="sxs-lookup"><span data-stu-id="d26ff-123">x</span></span>    | <span data-ttu-id="d26ff-124">x</span><span class="sxs-lookup"><span data-stu-id="d26ff-124">x</span></span>     |



 

<span data-ttu-id="d26ff-125">Эта инструкция работает по принципу, как показано здесь.</span><span class="sxs-lookup"><span data-stu-id="d26ff-125">This instruction works conceptually as shown here.</span></span>

<span data-ttu-id="d26ff-126">Скуарерутофсесум = (src0. x \* src0. x + src0. y \* src0. y + src0. z \* src0. z)<sup>1/2</sup>;</span><span class="sxs-lookup"><span data-stu-id="d26ff-126">squareRootOfTheSum = (src0.x\*src0.x + src0.y\*src0.y + src0.z\*src0.z)<sup>1/2</sup>;</span></span>


```
dest.x = src0.x * (1 / squareRootOfTheSum);
dest.y = src0.y * (1 / squareRootOfTheSum);
dest.z = src0.z * (1 / squareRootOfTheSum);
dest.w = src0.w * (1 / squareRootOfTheSum);
```



<span data-ttu-id="d26ff-127">Регистры dest и src не могут совпадать.</span><span class="sxs-lookup"><span data-stu-id="d26ff-127">The dest and src registers cannot be the same.</span></span> <span data-ttu-id="d26ff-128">Регистр приемника должен быть временным регистром.</span><span class="sxs-lookup"><span data-stu-id="d26ff-128">The dest register must be a temporary register.</span></span>

<span data-ttu-id="d26ff-129">Эта инструкция выполняет линейную интерполяцию на основе следующей формулы.</span><span class="sxs-lookup"><span data-stu-id="d26ff-129">This instruction performs the linear interpolation based on the following formula.</span></span>


```
float f = src0.x*src0.x + src0.y*src0.y + src0.z*src0.z;
if (f != 0)
    f = (float)(1/sqrt(f));
else
    f = FLT_MAX;

dest.x = src0.x*f;
dest.y = src0.y*f;
dest.z = src0.z*f;
dest.w = src0.w*f;
```



## <a name="related-topics"></a><span data-ttu-id="d26ff-130">См. также</span><span class="sxs-lookup"><span data-stu-id="d26ff-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d26ff-131">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="d26ff-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




