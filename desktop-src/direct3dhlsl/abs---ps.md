---
title: ABS-PS
description: Вычисление абсолютного значения. | ABS-PS
ms.assetid: e97db550-2a03-421a-86f4-a6fc5f8e0bca
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f4f22261a114333ed77d67d7c0ac2738d3522054
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343330"
---
# <a name="abs---ps"></a><span data-ttu-id="b2ee4-104">ABS-PS</span><span class="sxs-lookup"><span data-stu-id="b2ee4-104">abs - ps</span></span>

<span data-ttu-id="b2ee4-105">Вычисление абсолютного значения.</span><span class="sxs-lookup"><span data-stu-id="b2ee4-105">Computes absolute value.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2ee4-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b2ee4-106">Syntax</span></span>

<span data-ttu-id="b2ee4-107">**ABS DST, src**</span><span class="sxs-lookup"><span data-stu-id="b2ee4-107">**abs dst, src**</span></span>

<span data-ttu-id="b2ee4-108">where</span><span class="sxs-lookup"><span data-stu-id="b2ee4-108">where</span></span>

-   <span data-ttu-id="b2ee4-109">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="b2ee4-109">dst is the destination register.</span></span>
-   <span data-ttu-id="b2ee4-110">src является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="b2ee4-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2ee4-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="b2ee4-111">Remarks</span></span>



| <span data-ttu-id="b2ee4-112">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="b2ee4-112">Pixel shader versions</span></span> | <span data-ttu-id="b2ee4-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="b2ee4-113">1\_1</span></span> | <span data-ttu-id="b2ee4-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="b2ee4-114">1\_2</span></span> | <span data-ttu-id="b2ee4-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="b2ee4-115">1\_3</span></span> | <span data-ttu-id="b2ee4-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="b2ee4-116">1\_4</span></span> | <span data-ttu-id="b2ee4-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b2ee4-117">2\_0</span></span> | <span data-ttu-id="b2ee4-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b2ee4-118">2\_x</span></span> | <span data-ttu-id="b2ee4-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b2ee4-119">2\_sw</span></span> | <span data-ttu-id="b2ee4-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b2ee4-120">3\_0</span></span> | <span data-ttu-id="b2ee4-121">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b2ee4-121">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="b2ee4-122">abs</span><span class="sxs-lookup"><span data-stu-id="b2ee4-122">abs</span></span>                   |      |      |      |      | <span data-ttu-id="b2ee4-123">x</span><span class="sxs-lookup"><span data-stu-id="b2ee4-123">x</span></span>    | <span data-ttu-id="b2ee4-124">x</span><span class="sxs-lookup"><span data-stu-id="b2ee4-124">x</span></span>    | <span data-ttu-id="b2ee4-125">x</span><span class="sxs-lookup"><span data-stu-id="b2ee4-125">x</span></span>     | <span data-ttu-id="b2ee4-126">x</span><span class="sxs-lookup"><span data-stu-id="b2ee4-126">x</span></span>    | <span data-ttu-id="b2ee4-127">x</span><span class="sxs-lookup"><span data-stu-id="b2ee4-127">x</span></span>     |



 

<span data-ttu-id="b2ee4-128">Эта инструкция работает, как показано здесь.</span><span class="sxs-lookup"><span data-stu-id="b2ee4-128">This instruction works as shown here.</span></span>


```
dest.x = abs(src.x)
dest.y = abs(src.y)
dest.z = abs(src.z)
dest.w = abs(src.w)
```



## <a name="instruction-information"></a><span data-ttu-id="b2ee4-129">Сведения о инструкции</span><span class="sxs-lookup"><span data-stu-id="b2ee4-129">Instruction Information</span></span>



| <span data-ttu-id="b2ee4-130">Требование</span><span class="sxs-lookup"><span data-stu-id="b2ee4-130">Requirement</span></span>                         | <span data-ttu-id="b2ee4-131">Значение</span><span class="sxs-lookup"><span data-stu-id="b2ee4-131">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="b2ee4-132">Минимальная операционная система</span><span class="sxs-lookup"><span data-stu-id="b2ee4-132">Minimum operating system</span></span> | <span data-ttu-id="b2ee4-133">Windows 98</span><span class="sxs-lookup"><span data-stu-id="b2ee4-133">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b2ee4-134">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="b2ee4-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2ee4-135">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="b2ee4-135">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




