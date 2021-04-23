---
title: Mad-PS
description: Умножение и Добавление инструкции. Задает регистр назначения (src0 \ src1) + src2.
ms.assetid: 0bcf5dcc-3657-4ee0-9aeb-bd2d8feea7a6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b3570f5826f91b35b07478e1ea34940a27d706cf
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412195"
---
# <a name="mad---ps"></a><span data-ttu-id="688e9-104">Mad-PS</span><span class="sxs-lookup"><span data-stu-id="688e9-104">mad - ps</span></span>

<span data-ttu-id="688e9-105">Умножение и Добавление инструкции.</span><span class="sxs-lookup"><span data-stu-id="688e9-105">Multiply and add instruction.</span></span> <span data-ttu-id="688e9-106">Задает регистр назначения (src0 \* src1) + src2.</span><span class="sxs-lookup"><span data-stu-id="688e9-106">Sets the destination register to (src0 \* src1) + src2.</span></span>

## <a name="syntax"></a><span data-ttu-id="688e9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="688e9-107">Syntax</span></span>



| <span data-ttu-id="688e9-108">Mad DST, src0, src1, src2</span><span class="sxs-lookup"><span data-stu-id="688e9-108">mad dst, src0, src1, src2</span></span> |
|---------------------------|



 

<span data-ttu-id="688e9-109">где</span><span class="sxs-lookup"><span data-stu-id="688e9-109">where</span></span>

-   <span data-ttu-id="688e9-110">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="688e9-110">dst is the destination register.</span></span>
-   <span data-ttu-id="688e9-111">src0 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="688e9-111">src0 is a source register.</span></span>
-   <span data-ttu-id="688e9-112">src1 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="688e9-112">src1 is a source register.</span></span>
-   <span data-ttu-id="688e9-113">src2 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="688e9-113">src2 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="688e9-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="688e9-114">Remarks</span></span>



| <span data-ttu-id="688e9-115">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="688e9-115">Pixel shader versions</span></span> | <span data-ttu-id="688e9-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="688e9-116">1\_1</span></span> | <span data-ttu-id="688e9-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="688e9-117">1\_2</span></span> | <span data-ttu-id="688e9-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="688e9-118">1\_3</span></span> | <span data-ttu-id="688e9-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="688e9-119">1\_4</span></span> | <span data-ttu-id="688e9-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="688e9-120">2\_0</span></span> | <span data-ttu-id="688e9-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="688e9-121">2\_x</span></span> | <span data-ttu-id="688e9-122">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="688e9-122">2\_sw</span></span> | <span data-ttu-id="688e9-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="688e9-123">3\_0</span></span> | <span data-ttu-id="688e9-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="688e9-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="688e9-125">отслеживания</span><span class="sxs-lookup"><span data-stu-id="688e9-125">mad</span></span>                   | <span data-ttu-id="688e9-126">x</span><span class="sxs-lookup"><span data-stu-id="688e9-126">x</span></span>    | <span data-ttu-id="688e9-127">x</span><span class="sxs-lookup"><span data-stu-id="688e9-127">x</span></span>    | <span data-ttu-id="688e9-128">x</span><span class="sxs-lookup"><span data-stu-id="688e9-128">x</span></span>    | <span data-ttu-id="688e9-129">x</span><span class="sxs-lookup"><span data-stu-id="688e9-129">x</span></span>    | <span data-ttu-id="688e9-130">x</span><span class="sxs-lookup"><span data-stu-id="688e9-130">x</span></span>    | <span data-ttu-id="688e9-131">x</span><span class="sxs-lookup"><span data-stu-id="688e9-131">x</span></span>    | <span data-ttu-id="688e9-132">x</span><span class="sxs-lookup"><span data-stu-id="688e9-132">x</span></span>     | <span data-ttu-id="688e9-133">x</span><span class="sxs-lookup"><span data-stu-id="688e9-133">x</span></span>    | <span data-ttu-id="688e9-134">x</span><span class="sxs-lookup"><span data-stu-id="688e9-134">x</span></span>     |



 

<span data-ttu-id="688e9-135">В следующем фрагменте кода показаны выполняемые операции.</span><span class="sxs-lookup"><span data-stu-id="688e9-135">The following code snippet shows the operations performed.</span></span>


```
dest.x = src0.x * src1.x + src2.x;
dest.y = src0.y * src1.y + src2.y;
dest.z = src0.z * src1.z + src2.z;
dest.w = src0.w * src1.w + src2.w;
```



## <a name="related-topics"></a><span data-ttu-id="688e9-136">См. также</span><span class="sxs-lookup"><span data-stu-id="688e9-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="688e9-137">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="688e9-137">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




