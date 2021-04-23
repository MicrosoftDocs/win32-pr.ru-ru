---
title: CR-PS
description: Вычисление перекрестного произведения с помощью правого правила. | CR-PS
ms.assetid: 602fa7cc-4e2b-4d90-90d8-df00d5812c81
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b6098c8bf01bf0d8cce886276c1d1081720ea667
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352565"
---
# <a name="crs---ps"></a><span data-ttu-id="459a7-104">CR-PS</span><span class="sxs-lookup"><span data-stu-id="459a7-104">crs - ps</span></span>

<span data-ttu-id="459a7-105">Вычисление перекрестного произведения с помощью правого правила.</span><span class="sxs-lookup"><span data-stu-id="459a7-105">Computes a cross product using the right-hand rule.</span></span>

## <a name="syntax"></a><span data-ttu-id="459a7-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="459a7-106">Syntax</span></span>



| <span data-ttu-id="459a7-107">CR, летнее время, src0, src1</span><span class="sxs-lookup"><span data-stu-id="459a7-107">crs dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="459a7-108">где</span><span class="sxs-lookup"><span data-stu-id="459a7-108">where</span></span>

-   <span data-ttu-id="459a7-109">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="459a7-109">dst is the destination register.</span></span>
-   <span data-ttu-id="459a7-110">src0 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="459a7-110">src0 is a source register.</span></span>
-   <span data-ttu-id="459a7-111">src1 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="459a7-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="459a7-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="459a7-112">Remarks</span></span>



| <span data-ttu-id="459a7-113">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="459a7-113">Pixel shader versions</span></span> | <span data-ttu-id="459a7-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="459a7-114">1\_1</span></span> | <span data-ttu-id="459a7-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="459a7-115">1\_2</span></span> | <span data-ttu-id="459a7-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="459a7-116">1\_3</span></span> | <span data-ttu-id="459a7-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="459a7-117">1\_4</span></span> | <span data-ttu-id="459a7-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="459a7-118">2\_0</span></span> | <span data-ttu-id="459a7-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="459a7-119">2\_x</span></span> | <span data-ttu-id="459a7-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="459a7-120">2\_sw</span></span> | <span data-ttu-id="459a7-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="459a7-121">3\_0</span></span> | <span data-ttu-id="459a7-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="459a7-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="459a7-123">запросы</span><span class="sxs-lookup"><span data-stu-id="459a7-123">crs</span></span>                   |      |      |      |      | <span data-ttu-id="459a7-124">x</span><span class="sxs-lookup"><span data-stu-id="459a7-124">x</span></span>    | <span data-ttu-id="459a7-125">x</span><span class="sxs-lookup"><span data-stu-id="459a7-125">x</span></span>    | <span data-ttu-id="459a7-126">x</span><span class="sxs-lookup"><span data-stu-id="459a7-126">x</span></span>     | <span data-ttu-id="459a7-127">x</span><span class="sxs-lookup"><span data-stu-id="459a7-127">x</span></span>    | <span data-ttu-id="459a7-128">x</span><span class="sxs-lookup"><span data-stu-id="459a7-128">x</span></span>     |



 

<span data-ttu-id="459a7-129">Эта инструкция работает, как показано здесь.</span><span class="sxs-lookup"><span data-stu-id="459a7-129">This instruction works as shown here.</span></span>


```
dest.x = src0.y * src1.z - src0.z * src1.y;
dest.y = src0.z * src1.x - src0.x * src1.z;
dest.z = src0.x * src1.y - src0.y * src1.x;
```



<span data-ttu-id="459a7-130">Некоторые ограничения на использование:</span><span class="sxs-lookup"><span data-stu-id="459a7-130">Some restrictions on use:</span></span>

-   <span data-ttu-id="459a7-131">src0 не может быть тем же регистром, что и dest.</span><span class="sxs-lookup"><span data-stu-id="459a7-131">src0 cannot be the same register as dest.</span></span>
-   <span data-ttu-id="459a7-132">src1 не может быть тем же регистром, что и dest.</span><span class="sxs-lookup"><span data-stu-id="459a7-132">src1 cannot be the same register as dest.</span></span>
-   <span data-ttu-id="459a7-133">src0 не может иметь свиззле, кроме свиззле по умолчанию (ксизв).</span><span class="sxs-lookup"><span data-stu-id="459a7-133">src0 cannot have any swizzle other than the default swizzle (.xyzw).</span></span>
-   <span data-ttu-id="459a7-134">src1 не может иметь свиззле, кроме свиззле по умолчанию (ксизв).</span><span class="sxs-lookup"><span data-stu-id="459a7-134">src1 cannot have any swizzle other than the default swizzle (.xyzw).</span></span>
-   <span data-ttu-id="459a7-135">dest должен иметь ровно одну из следующих семи масок:. x \| . y \| . z \| . XY \| . КСЗ \| . из \| . xyz.</span><span class="sxs-lookup"><span data-stu-id="459a7-135">dest has to have exactly one of the following seven masks: .x \| .y \| .z \| .xy \| .xz \| .yz \| .xyz.</span></span>
-   <span data-ttu-id="459a7-136">конечный объект должен быть временным регистром.</span><span class="sxs-lookup"><span data-stu-id="459a7-136">dest must be a temporary register.</span></span>
-   <span data-ttu-id="459a7-137">конечный объект не должен совпадать с регистром src0 или src1</span><span class="sxs-lookup"><span data-stu-id="459a7-137">dest must not be the same register as src0 or src1</span></span>

## <a name="related-topics"></a><span data-ttu-id="459a7-138">См. также</span><span class="sxs-lookup"><span data-stu-id="459a7-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="459a7-139">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="459a7-139">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




