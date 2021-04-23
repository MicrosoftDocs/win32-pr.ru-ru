---
title: Надстройка VS
description: Складывает два вектора. | Надстройка VS
ms.assetid: f66d3264-68be-4a4f-84fc-cc0f6c4245c9
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 678e7f815a819be2abf1d985516fe081d3c09c94
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914315"
---
# <a name="add---vs"></a><span data-ttu-id="bf9e0-104">Надстройка VS</span><span class="sxs-lookup"><span data-stu-id="bf9e0-104">add - vs</span></span>

<span data-ttu-id="bf9e0-105">Складывает два вектора.</span><span class="sxs-lookup"><span data-stu-id="bf9e0-105">Adds two vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf9e0-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bf9e0-106">Syntax</span></span>



| <span data-ttu-id="bf9e0-107">Добавление летнего времени, src0, src1</span><span class="sxs-lookup"><span data-stu-id="bf9e0-107">add dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="bf9e0-108">где</span><span class="sxs-lookup"><span data-stu-id="bf9e0-108">where</span></span>

-   <span data-ttu-id="bf9e0-109">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="bf9e0-109">dst is the destination register.</span></span>
-   <span data-ttu-id="bf9e0-110">src0 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="bf9e0-110">src0 is a source register.</span></span>
-   <span data-ttu-id="bf9e0-111">src1 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="bf9e0-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf9e0-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="bf9e0-112">Remarks</span></span>



| <span data-ttu-id="bf9e0-113">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="bf9e0-113">Vertex shader versions</span></span> | <span data-ttu-id="bf9e0-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="bf9e0-114">1\_1</span></span> | <span data-ttu-id="bf9e0-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bf9e0-115">2\_0</span></span> | <span data-ttu-id="bf9e0-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="bf9e0-116">2\_x</span></span> | <span data-ttu-id="bf9e0-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="bf9e0-117">2\_sw</span></span> | <span data-ttu-id="bf9e0-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="bf9e0-118">3\_0</span></span> | <span data-ttu-id="bf9e0-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="bf9e0-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="bf9e0-120">add</span><span class="sxs-lookup"><span data-stu-id="bf9e0-120">add</span></span>                    | <span data-ttu-id="bf9e0-121">x</span><span class="sxs-lookup"><span data-stu-id="bf9e0-121">x</span></span>    | <span data-ttu-id="bf9e0-122">x</span><span class="sxs-lookup"><span data-stu-id="bf9e0-122">x</span></span>    | <span data-ttu-id="bf9e0-123">x</span><span class="sxs-lookup"><span data-stu-id="bf9e0-123">x</span></span>    | <span data-ttu-id="bf9e0-124">x</span><span class="sxs-lookup"><span data-stu-id="bf9e0-124">x</span></span>     | <span data-ttu-id="bf9e0-125">x</span><span class="sxs-lookup"><span data-stu-id="bf9e0-125">x</span></span>    | <span data-ttu-id="bf9e0-126">x</span><span class="sxs-lookup"><span data-stu-id="bf9e0-126">x</span></span>     |



 

<span data-ttu-id="bf9e0-127">В следующем фрагменте кода показаны выполняемые операции.</span><span class="sxs-lookup"><span data-stu-id="bf9e0-127">The following code fragment shows the operations performed.</span></span>


```
dest.x = src0.x + src1.x;
dest.y = src0.y + src1.y;
dest.z = src0.z + src1.z;
dest.w = src0.w + src1.w;
```



## <a name="related-topics"></a><span data-ttu-id="bf9e0-128">См. также</span><span class="sxs-lookup"><span data-stu-id="bf9e0-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf9e0-129">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="bf9e0-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




