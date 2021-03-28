---
title: ЛРП — VS
description: Выполняет линейную интерполяцию между вторым и третьим регистрами источника по пропорциям, заданным в первом регистре источника. | ЛРП — VS
ms.assetid: 8438bcf3-9b00-4963-b2a3-54fd1c345961
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 485d7720dc2c71ee599db93d179de8e665bfab77
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998151"
---
# <a name="lrp---vs"></a><span data-ttu-id="f16e8-104">ЛРП — VS</span><span class="sxs-lookup"><span data-stu-id="f16e8-104">lrp - vs</span></span>

<span data-ttu-id="f16e8-105">Выполняет линейную интерполяцию между вторым и третьим регистрами источника по пропорциям, заданным в первом регистре источника.</span><span class="sxs-lookup"><span data-stu-id="f16e8-105">Interpolates linearly between the second and third source registers by a proportion specified in the first source register.</span></span>

## <a name="syntax"></a><span data-ttu-id="f16e8-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f16e8-106">Syntax</span></span>



| <span data-ttu-id="f16e8-107">ЛРП DST, src0, src1, src2</span><span class="sxs-lookup"><span data-stu-id="f16e8-107">lrp dst, src0, src1, src2</span></span> |
|---------------------------|



 

<span data-ttu-id="f16e8-108">где</span><span class="sxs-lookup"><span data-stu-id="f16e8-108">where</span></span>

-   <span data-ttu-id="f16e8-109">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="f16e8-109">dst is the destination register.</span></span>
-   <span data-ttu-id="f16e8-110">src0 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="f16e8-110">src0 is a source register.</span></span>
-   <span data-ttu-id="f16e8-111">src1 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="f16e8-111">src1 is a source register.</span></span>
-   <span data-ttu-id="f16e8-112">src2 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="f16e8-112">src2 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="f16e8-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="f16e8-113">Remarks</span></span>



| <span data-ttu-id="f16e8-114">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="f16e8-114">Vertex shader versions</span></span> | <span data-ttu-id="f16e8-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="f16e8-115">1\_1</span></span> | <span data-ttu-id="f16e8-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f16e8-116">2\_0</span></span> | <span data-ttu-id="f16e8-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="f16e8-117">2\_x</span></span> | <span data-ttu-id="f16e8-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f16e8-118">2\_sw</span></span> | <span data-ttu-id="f16e8-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f16e8-119">3\_0</span></span> | <span data-ttu-id="f16e8-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f16e8-120">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="f16e8-121">лрп</span><span class="sxs-lookup"><span data-stu-id="f16e8-121">lrp</span></span>                    |      | <span data-ttu-id="f16e8-122">x</span><span class="sxs-lookup"><span data-stu-id="f16e8-122">x</span></span>    | <span data-ttu-id="f16e8-123">x</span><span class="sxs-lookup"><span data-stu-id="f16e8-123">x</span></span>    | <span data-ttu-id="f16e8-124">x</span><span class="sxs-lookup"><span data-stu-id="f16e8-124">x</span></span>     | <span data-ttu-id="f16e8-125">x</span><span class="sxs-lookup"><span data-stu-id="f16e8-125">x</span></span>    | <span data-ttu-id="f16e8-126">x</span><span class="sxs-lookup"><span data-stu-id="f16e8-126">x</span></span>     |



 

<span data-ttu-id="f16e8-127">Эта инструкция выполняет линейную интерполяцию на основе следующей формулы.</span><span class="sxs-lookup"><span data-stu-id="f16e8-127">This instruction performs the linear interpolation based on the following formula.</span></span>


```
dest.x = src0.x * (src1.x - src2.x) + src2.x;
dest.y = src0.y * (src1.y - src2.y) + src2.y;
dest.z = src0.z * (src1.z - src2.z) + src2.z;
dest.w = src0.w * (src1.w - src2.w) + src2.w;
```



## <a name="related-topics"></a><span data-ttu-id="f16e8-128">См. также</span><span class="sxs-lookup"><span data-stu-id="f16e8-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f16e8-129">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="f16e8-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




