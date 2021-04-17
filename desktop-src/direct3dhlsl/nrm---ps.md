---
title: НРМ-PS
description: Нормализация трехмерного вектора. | НРМ-PS
ms.assetid: 4881037d-3ad1-4afb-b4ad-d615c6b8fe34
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 165f1b8fa6adce4ffba079eff025ed1a3d8ce61e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352862"
---
# <a name="nrm---ps"></a><span data-ttu-id="b3ba7-104">НРМ-PS</span><span class="sxs-lookup"><span data-stu-id="b3ba7-104">nrm - ps</span></span>

<span data-ttu-id="b3ba7-105">Нормализация трехмерного вектора.</span><span class="sxs-lookup"><span data-stu-id="b3ba7-105">Normalize a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3ba7-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b3ba7-106">Syntax</span></span>



| <span data-ttu-id="b3ba7-107">НРМ DST, src</span><span class="sxs-lookup"><span data-stu-id="b3ba7-107">nrm dst, src</span></span> |
|--------------|



 

<span data-ttu-id="b3ba7-108">где</span><span class="sxs-lookup"><span data-stu-id="b3ba7-108">where</span></span>

-   <span data-ttu-id="b3ba7-109">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="b3ba7-109">dst is the destination register.</span></span>
-   <span data-ttu-id="b3ba7-110">src является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="b3ba7-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3ba7-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="b3ba7-111">Remarks</span></span>



| <span data-ttu-id="b3ba7-112">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="b3ba7-112">Pixel shader versions</span></span> | <span data-ttu-id="b3ba7-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="b3ba7-113">1\_1</span></span> | <span data-ttu-id="b3ba7-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="b3ba7-114">1\_2</span></span> | <span data-ttu-id="b3ba7-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="b3ba7-115">1\_3</span></span> | <span data-ttu-id="b3ba7-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="b3ba7-116">1\_4</span></span> | <span data-ttu-id="b3ba7-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b3ba7-117">2\_0</span></span> | <span data-ttu-id="b3ba7-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b3ba7-118">2\_x</span></span> | <span data-ttu-id="b3ba7-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b3ba7-119">2\_sw</span></span> | <span data-ttu-id="b3ba7-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b3ba7-120">3\_0</span></span> | <span data-ttu-id="b3ba7-121">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b3ba7-121">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="b3ba7-122">нрм</span><span class="sxs-lookup"><span data-stu-id="b3ba7-122">nrm</span></span>                   |      |      |      |      | <span data-ttu-id="b3ba7-123">x</span><span class="sxs-lookup"><span data-stu-id="b3ba7-123">x</span></span>    | <span data-ttu-id="b3ba7-124">x</span><span class="sxs-lookup"><span data-stu-id="b3ba7-124">x</span></span>    | <span data-ttu-id="b3ba7-125">x</span><span class="sxs-lookup"><span data-stu-id="b3ba7-125">x</span></span>     | <span data-ttu-id="b3ba7-126">x</span><span class="sxs-lookup"><span data-stu-id="b3ba7-126">x</span></span>    | <span data-ttu-id="b3ba7-127">x</span><span class="sxs-lookup"><span data-stu-id="b3ba7-127">x</span></span>     |



 

<span data-ttu-id="b3ba7-128">Эта инструкция работает по принципу, как показано здесь.</span><span class="sxs-lookup"><span data-stu-id="b3ba7-128">This instruction works conceptually as shown here.</span></span>

<span data-ttu-id="b3ba7-129">Скуарерутофсесум = (src0. x \* src0. x + src0. y \* src0. y + src0. z \* src0. z)<sup>1/2</sup>;</span><span class="sxs-lookup"><span data-stu-id="b3ba7-129">squareRootOfTheSum = (src0.x\*src0.x + src0.y\*src0.y + src0.z\*src0.z)<sup>1/2</sup>;</span></span>


```
dest.x = src0.x * (1 / squareRootOfTheSum);
dest.y = src0.y * (1 / squareRootOfTheSum);
dest.z = src0.z * (1 / squareRootOfTheSum);
dest.w = src0.w * (1 / squareRootOfTheSum);
```



<span data-ttu-id="b3ba7-130">Регистры dest и src не могут совпадать.</span><span class="sxs-lookup"><span data-stu-id="b3ba7-130">The dest and src registers cannot be the same.</span></span> <span data-ttu-id="b3ba7-131">Регистр приемника должен быть временным регистром.</span><span class="sxs-lookup"><span data-stu-id="b3ba7-131">The dest register must be a temporary register.</span></span>

<span data-ttu-id="b3ba7-132">Эта инструкция выполняет линейную интерполяцию на основе следующей формулы.</span><span class="sxs-lookup"><span data-stu-id="b3ba7-132">This instruction performs the linear interpolation based on the following formula.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="b3ba7-133">См. также</span><span class="sxs-lookup"><span data-stu-id="b3ba7-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3ba7-134">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="b3ba7-134">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




