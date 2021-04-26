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
ms.openlocfilehash: e3e7af7b2d30e9d9f2092cb6671610f008ec781d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994881"
---
# <a name="abs---ps"></a><span data-ttu-id="738c5-104">ABS-PS</span><span class="sxs-lookup"><span data-stu-id="738c5-104">abs - ps</span></span>

<span data-ttu-id="738c5-105">Вычисление абсолютного значения.</span><span class="sxs-lookup"><span data-stu-id="738c5-105">Computes absolute value.</span></span>

## <a name="syntax"></a><span data-ttu-id="738c5-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="738c5-106">Syntax</span></span>



|              |
|--------------|
| <span data-ttu-id="738c5-107">ABS DST, src</span><span class="sxs-lookup"><span data-stu-id="738c5-107">abs dst, src</span></span> |



 

<span data-ttu-id="738c5-108">where</span><span class="sxs-lookup"><span data-stu-id="738c5-108">where</span></span>

-   <span data-ttu-id="738c5-109">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="738c5-109">dst is the destination register.</span></span>
-   <span data-ttu-id="738c5-110">src является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="738c5-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="738c5-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="738c5-111">Remarks</span></span>



| <span data-ttu-id="738c5-112">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="738c5-112">Pixel shader versions</span></span> | <span data-ttu-id="738c5-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="738c5-113">1\_1</span></span> | <span data-ttu-id="738c5-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="738c5-114">1\_2</span></span> | <span data-ttu-id="738c5-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="738c5-115">1\_3</span></span> | <span data-ttu-id="738c5-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="738c5-116">1\_4</span></span> | <span data-ttu-id="738c5-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="738c5-117">2\_0</span></span> | <span data-ttu-id="738c5-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="738c5-118">2\_x</span></span> | <span data-ttu-id="738c5-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="738c5-119">2\_sw</span></span> | <span data-ttu-id="738c5-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="738c5-120">3\_0</span></span> | <span data-ttu-id="738c5-121">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="738c5-121">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="738c5-122">abs</span><span class="sxs-lookup"><span data-stu-id="738c5-122">abs</span></span>                   |      |      |      |      | <span data-ttu-id="738c5-123">x</span><span class="sxs-lookup"><span data-stu-id="738c5-123">x</span></span>    | <span data-ttu-id="738c5-124">x</span><span class="sxs-lookup"><span data-stu-id="738c5-124">x</span></span>    | <span data-ttu-id="738c5-125">x</span><span class="sxs-lookup"><span data-stu-id="738c5-125">x</span></span>     | <span data-ttu-id="738c5-126">x</span><span class="sxs-lookup"><span data-stu-id="738c5-126">x</span></span>    | <span data-ttu-id="738c5-127">x</span><span class="sxs-lookup"><span data-stu-id="738c5-127">x</span></span>     |



 

<span data-ttu-id="738c5-128">Эта инструкция работает, как показано здесь.</span><span class="sxs-lookup"><span data-stu-id="738c5-128">This instruction works as shown here.</span></span>


```
dest.x = abs(src.x)
dest.y = abs(src.y)
dest.z = abs(src.z)
dest.w = abs(src.w)
```



## <a name="instruction-information"></a><span data-ttu-id="738c5-129">Сведения о инструкции</span><span class="sxs-lookup"><span data-stu-id="738c5-129">Instruction Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="738c5-130">Минимальная операционная система</span><span class="sxs-lookup"><span data-stu-id="738c5-130">Minimum operating system</span></span> | <span data-ttu-id="738c5-131">Windows 98</span><span class="sxs-lookup"><span data-stu-id="738c5-131">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="738c5-132">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="738c5-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="738c5-133">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="738c5-133">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




