---
title: CR-VS
description: Вычисление перекрестного произведения с помощью правого правила. | CR-VS
ms.assetid: 102108f5-acc8-49ce-a84b-b8060decbaa7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fee30fab91b4f491efd4311919245ec2cb98b555
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352562"
---
# <a name="crs---vs"></a><span data-ttu-id="f082f-104">CR-VS</span><span class="sxs-lookup"><span data-stu-id="f082f-104">crs - vs</span></span>

<span data-ttu-id="f082f-105">Вычисление перекрестного произведения с помощью правого правила.</span><span class="sxs-lookup"><span data-stu-id="f082f-105">Computes a cross product using the right-hand rule.</span></span>

## <a name="syntax"></a><span data-ttu-id="f082f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f082f-106">Syntax</span></span>



| <span data-ttu-id="f082f-107">CR, летнее время, src0, src1</span><span class="sxs-lookup"><span data-stu-id="f082f-107">crs dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="f082f-108">где</span><span class="sxs-lookup"><span data-stu-id="f082f-108">where</span></span>

-   <span data-ttu-id="f082f-109">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="f082f-109">dst is the destination register.</span></span>
-   <span data-ttu-id="f082f-110">src0 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="f082f-110">src0 is a source register.</span></span>
-   <span data-ttu-id="f082f-111">src1 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="f082f-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="f082f-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="f082f-112">Remarks</span></span>



| <span data-ttu-id="f082f-113">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="f082f-113">Vertex shader versions</span></span> | <span data-ttu-id="f082f-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="f082f-114">1\_1</span></span> | <span data-ttu-id="f082f-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f082f-115">2\_0</span></span> | <span data-ttu-id="f082f-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="f082f-116">2\_x</span></span> | <span data-ttu-id="f082f-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f082f-117">2\_sw</span></span> | <span data-ttu-id="f082f-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f082f-118">3\_0</span></span> | <span data-ttu-id="f082f-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f082f-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="f082f-120">запросы</span><span class="sxs-lookup"><span data-stu-id="f082f-120">crs</span></span>                    |      | <span data-ttu-id="f082f-121">x</span><span class="sxs-lookup"><span data-stu-id="f082f-121">x</span></span>    | <span data-ttu-id="f082f-122">x</span><span class="sxs-lookup"><span data-stu-id="f082f-122">x</span></span>    | <span data-ttu-id="f082f-123">x</span><span class="sxs-lookup"><span data-stu-id="f082f-123">x</span></span>     | <span data-ttu-id="f082f-124">x</span><span class="sxs-lookup"><span data-stu-id="f082f-124">x</span></span>    | <span data-ttu-id="f082f-125">x</span><span class="sxs-lookup"><span data-stu-id="f082f-125">x</span></span>     |



 

<span data-ttu-id="f082f-126">Эта инструкция работает, как показано здесь.</span><span class="sxs-lookup"><span data-stu-id="f082f-126">This instruction works as shown here.</span></span>


```
dest.x = src0.y * src1.z - src0.z * src1.y;
dest.y = src0.z * src1.x - src0.x * src1.z;
dest.z = src0.x * src1.y - src0.y * src1.x;
```



<span data-ttu-id="f082f-127">Некоторые ограничения на использование:</span><span class="sxs-lookup"><span data-stu-id="f082f-127">Some restrictions on use:</span></span>

-   <span data-ttu-id="f082f-128">src0 не может быть тем же регистром, что и dest.</span><span class="sxs-lookup"><span data-stu-id="f082f-128">src0 cannot be the same register as dest.</span></span>
-   <span data-ttu-id="f082f-129">src1 не может быть тем же регистром, что и dest.</span><span class="sxs-lookup"><span data-stu-id="f082f-129">src1 cannot be the same register as dest.</span></span>
-   <span data-ttu-id="f082f-130">src0 не может иметь свиззле, кроме свиззле по умолчанию (ксизв).</span><span class="sxs-lookup"><span data-stu-id="f082f-130">src0 cannot have any swizzle other than the default swizzle (.xyzw).</span></span>
-   <span data-ttu-id="f082f-131">src1 не может иметь свиззле, кроме свиззле по умолчанию (ксизв).</span><span class="sxs-lookup"><span data-stu-id="f082f-131">src1 cannot have any swizzle other than the default swizzle (.xyzw).</span></span>
-   <span data-ttu-id="f082f-132">dest должен иметь ровно одну из следующих семи масок:. x \| . y \| . z \| . XY \| . КСЗ \| . из \| . xyz.</span><span class="sxs-lookup"><span data-stu-id="f082f-132">dest has to have exactly one of the following seven masks: .x \| .y \| .z \| .xy \| .xz \| .yz \| .xyz.</span></span>
-   <span data-ttu-id="f082f-133">конечный объект должен быть временным регистром.</span><span class="sxs-lookup"><span data-stu-id="f082f-133">dest must be a temporary register.</span></span>
-   <span data-ttu-id="f082f-134">конечный объект не должен совпадать с регистром src0 или src1</span><span class="sxs-lookup"><span data-stu-id="f082f-134">dest must not be the same register as src0 or src1</span></span>

## <a name="related-topics"></a><span data-ttu-id="f082f-135">См. также</span><span class="sxs-lookup"><span data-stu-id="f082f-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f082f-136">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="f082f-136">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




