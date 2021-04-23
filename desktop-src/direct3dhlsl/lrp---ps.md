---
title: ЛРП-PS
description: Выполняет линейную интерполяцию между вторым и третьим регистрами источника по пропорциям, заданным в первом регистре источника. | ЛРП-PS
ms.assetid: b360f28e-cb2a-4403-a020-180524df6549
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aec1ac23cc6c86f768d435e4c8169117c1bbe899
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104081824"
---
# <a name="lrp---ps"></a><span data-ttu-id="85dd4-104">ЛРП-PS</span><span class="sxs-lookup"><span data-stu-id="85dd4-104">lrp - ps</span></span>

<span data-ttu-id="85dd4-105">Выполняет линейную интерполяцию между вторым и третьим регистрами источника по пропорциям, заданным в первом регистре источника.</span><span class="sxs-lookup"><span data-stu-id="85dd4-105">Interpolates linearly between the second and third source registers by a proportion specified in the first source register.</span></span>

## <a name="syntax"></a><span data-ttu-id="85dd4-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="85dd4-106">Syntax</span></span>



| <span data-ttu-id="85dd4-107">ЛРП DST, src0, src1, src2</span><span class="sxs-lookup"><span data-stu-id="85dd4-107">lrp dst, src0, src1, src2</span></span> |
|---------------------------|



 

<span data-ttu-id="85dd4-108">где</span><span class="sxs-lookup"><span data-stu-id="85dd4-108">where</span></span>

-   <span data-ttu-id="85dd4-109">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="85dd4-109">dst is the destination register.</span></span>
-   <span data-ttu-id="85dd4-110">src0 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="85dd4-110">src0 is a source register.</span></span>
-   <span data-ttu-id="85dd4-111">src1 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="85dd4-111">src1 is a source register.</span></span>
-   <span data-ttu-id="85dd4-112">src2 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="85dd4-112">src2 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="85dd4-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="85dd4-113">Remarks</span></span>



| <span data-ttu-id="85dd4-114">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="85dd4-114">Pixel shader versions</span></span> | <span data-ttu-id="85dd4-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="85dd4-115">1\_1</span></span> | <span data-ttu-id="85dd4-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="85dd4-116">1\_2</span></span> | <span data-ttu-id="85dd4-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="85dd4-117">1\_3</span></span> | <span data-ttu-id="85dd4-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="85dd4-118">1\_4</span></span> | <span data-ttu-id="85dd4-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="85dd4-119">2\_0</span></span> | <span data-ttu-id="85dd4-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="85dd4-120">2\_x</span></span> | <span data-ttu-id="85dd4-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="85dd4-121">2\_sw</span></span> | <span data-ttu-id="85dd4-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="85dd4-122">3\_0</span></span> | <span data-ttu-id="85dd4-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="85dd4-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="85dd4-124">лрп</span><span class="sxs-lookup"><span data-stu-id="85dd4-124">lrp</span></span>                   | <span data-ttu-id="85dd4-125">x</span><span class="sxs-lookup"><span data-stu-id="85dd4-125">x</span></span>    | <span data-ttu-id="85dd4-126">x</span><span class="sxs-lookup"><span data-stu-id="85dd4-126">x</span></span>    | <span data-ttu-id="85dd4-127">x</span><span class="sxs-lookup"><span data-stu-id="85dd4-127">x</span></span>    | <span data-ttu-id="85dd4-128">x</span><span class="sxs-lookup"><span data-stu-id="85dd4-128">x</span></span>    | <span data-ttu-id="85dd4-129">x</span><span class="sxs-lookup"><span data-stu-id="85dd4-129">x</span></span>    | <span data-ttu-id="85dd4-130">x</span><span class="sxs-lookup"><span data-stu-id="85dd4-130">x</span></span>    | <span data-ttu-id="85dd4-131">x</span><span class="sxs-lookup"><span data-stu-id="85dd4-131">x</span></span>     | <span data-ttu-id="85dd4-132">x</span><span class="sxs-lookup"><span data-stu-id="85dd4-132">x</span></span>    | <span data-ttu-id="85dd4-133">x</span><span class="sxs-lookup"><span data-stu-id="85dd4-133">x</span></span>     |



 

<span data-ttu-id="85dd4-134">Эта инструкция выполняет линейную интерполяцию на основе следующей формулы.</span><span class="sxs-lookup"><span data-stu-id="85dd4-134">This instruction performs the linear interpolation based on the following formula.</span></span>


```
 
dest = src0 * src1 + (1-src0) * src2
// which is the same as
dest = src2 + src0 * (src1 - src2)
```



## <a name="related-topics"></a><span data-ttu-id="85dd4-135">См. также</span><span class="sxs-lookup"><span data-stu-id="85dd4-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85dd4-136">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="85dd4-136">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




