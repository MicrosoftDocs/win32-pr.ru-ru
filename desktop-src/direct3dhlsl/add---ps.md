---
title: Add-PS
description: Складывает два вектора. | Add-PS
ms.assetid: f7d29a66-879b-4160-82fd-0a1b2076559a
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54092caf19a486b68b92ef63d992f11289a51c93
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/01/2021
ms.locfileid: "113130093"
---
# <a name="add---ps"></a><span data-ttu-id="dc711-104">Add-PS</span><span class="sxs-lookup"><span data-stu-id="dc711-104">add - ps</span></span>

<span data-ttu-id="dc711-105">Складывает два вектора.</span><span class="sxs-lookup"><span data-stu-id="dc711-105">Adds two vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc711-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dc711-106">Syntax</span></span>



| <span data-ttu-id="dc711-107">Добавление летнего времени, src0, src1</span><span class="sxs-lookup"><span data-stu-id="dc711-107">add dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="dc711-108">where</span><span class="sxs-lookup"><span data-stu-id="dc711-108">where</span></span>

-   <span data-ttu-id="dc711-109">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="dc711-109">dst is the destination register.</span></span>
-   <span data-ttu-id="dc711-110">src0 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="dc711-110">src0 is a source register.</span></span>
-   <span data-ttu-id="dc711-111">src1 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="dc711-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc711-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="dc711-112">Remarks</span></span>



| <span data-ttu-id="dc711-113">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="dc711-113">Pixel shader versions</span></span> | <span data-ttu-id="dc711-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="dc711-114">1\_1</span></span> | <span data-ttu-id="dc711-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="dc711-115">1\_2</span></span> | <span data-ttu-id="dc711-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="dc711-116">1\_3</span></span> | <span data-ttu-id="dc711-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="dc711-117">1\_4</span></span> | <span data-ttu-id="dc711-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="dc711-118">2\_0</span></span> | <span data-ttu-id="dc711-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="dc711-119">2\_x</span></span> | <span data-ttu-id="dc711-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="dc711-120">2\_sw</span></span> | <span data-ttu-id="dc711-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="dc711-121">3\_0</span></span> | <span data-ttu-id="dc711-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="dc711-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="dc711-123">add</span><span class="sxs-lookup"><span data-stu-id="dc711-123">add</span></span>                   | <span data-ttu-id="dc711-124">x</span><span class="sxs-lookup"><span data-stu-id="dc711-124">x</span></span>    | <span data-ttu-id="dc711-125">x</span><span class="sxs-lookup"><span data-stu-id="dc711-125">x</span></span>    | <span data-ttu-id="dc711-126">x</span><span class="sxs-lookup"><span data-stu-id="dc711-126">x</span></span>    | <span data-ttu-id="dc711-127">x</span><span class="sxs-lookup"><span data-stu-id="dc711-127">x</span></span>    | <span data-ttu-id="dc711-128">x</span><span class="sxs-lookup"><span data-stu-id="dc711-128">x</span></span>    | <span data-ttu-id="dc711-129">x</span><span class="sxs-lookup"><span data-stu-id="dc711-129">x</span></span>    | <span data-ttu-id="dc711-130">x</span><span class="sxs-lookup"><span data-stu-id="dc711-130">x</span></span>     | <span data-ttu-id="dc711-131">x</span><span class="sxs-lookup"><span data-stu-id="dc711-131">x</span></span>    | <span data-ttu-id="dc711-132">x</span><span class="sxs-lookup"><span data-stu-id="dc711-132">x</span></span>     |



 

<span data-ttu-id="dc711-133">В следующем фрагменте кода показаны выполняемые операции.</span><span class="sxs-lookup"><span data-stu-id="dc711-133">The following code snippet shows the operations performed.</span></span>


```
dest.x = src0.x + src1.x;
dest.y = src0.y + src1.y;
dest.z = src0.z + src1.z;
dest.w = src0.w + src1.w;
```



## <a name="instruction-information"></a><span data-ttu-id="dc711-134">Сведения о инструкции</span><span class="sxs-lookup"><span data-stu-id="dc711-134">Instruction Information</span></span>



|   <span data-ttu-id="dc711-135">Требование</span><span class="sxs-lookup"><span data-stu-id="dc711-135">Requirement</span></span>                       | <span data-ttu-id="dc711-136">Значение</span><span class="sxs-lookup"><span data-stu-id="dc711-136">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="dc711-137">Минимальная операционная система</span><span class="sxs-lookup"><span data-stu-id="dc711-137">Minimum operating system</span></span> | <span data-ttu-id="dc711-138">Windows 98</span><span class="sxs-lookup"><span data-stu-id="dc711-138">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="dc711-139">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="dc711-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc711-140">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="dc711-140">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




