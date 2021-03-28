---
title: mul — VS
description: Умножает источники на место назначения. | mul — VS
ms.assetid: 0b048cc2-b165-418f-893e-6dee28ca5ad3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e33ac35831b19f771f4f5b64d94bcc47c6657db5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998110"
---
# <a name="mul---vs"></a><span data-ttu-id="8d55e-104">mul — VS</span><span class="sxs-lookup"><span data-stu-id="8d55e-104">mul - vs</span></span>

<span data-ttu-id="8d55e-105">Умножает источники на место назначения.</span><span class="sxs-lookup"><span data-stu-id="8d55e-105">Multiplies sources into the destination.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d55e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8d55e-106">Syntax</span></span>



| <span data-ttu-id="8d55e-107">mul DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="8d55e-107">mul dst, src0, src1</span></span> |
|---------------------|



 

<span data-ttu-id="8d55e-108">где</span><span class="sxs-lookup"><span data-stu-id="8d55e-108">where</span></span>

-   <span data-ttu-id="8d55e-109">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="8d55e-109">dst is the destination register.</span></span>
-   <span data-ttu-id="8d55e-110">src0 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="8d55e-110">src0 is a source register.</span></span>
-   <span data-ttu-id="8d55e-111">src1 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="8d55e-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d55e-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="8d55e-112">Remarks</span></span>



| <span data-ttu-id="8d55e-113">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="8d55e-113">Vertex shader versions</span></span> | <span data-ttu-id="8d55e-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="8d55e-114">1\_1</span></span> | <span data-ttu-id="8d55e-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8d55e-115">2\_0</span></span> | <span data-ttu-id="8d55e-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="8d55e-116">2\_x</span></span> | <span data-ttu-id="8d55e-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8d55e-117">2\_sw</span></span> | <span data-ttu-id="8d55e-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8d55e-118">3\_0</span></span> | <span data-ttu-id="8d55e-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8d55e-119">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="8d55e-120">mul</span><span class="sxs-lookup"><span data-stu-id="8d55e-120">mul</span></span>                    | <span data-ttu-id="8d55e-121">x</span><span class="sxs-lookup"><span data-stu-id="8d55e-121">x</span></span>    | <span data-ttu-id="8d55e-122">x</span><span class="sxs-lookup"><span data-stu-id="8d55e-122">x</span></span>    | <span data-ttu-id="8d55e-123">x</span><span class="sxs-lookup"><span data-stu-id="8d55e-123">x</span></span>    | <span data-ttu-id="8d55e-124">x</span><span class="sxs-lookup"><span data-stu-id="8d55e-124">x</span></span>     | <span data-ttu-id="8d55e-125">x</span><span class="sxs-lookup"><span data-stu-id="8d55e-125">x</span></span>    | <span data-ttu-id="8d55e-126">x</span><span class="sxs-lookup"><span data-stu-id="8d55e-126">x</span></span>     |



 

<span data-ttu-id="8d55e-127">В следующем фрагменте кода показаны выполняемые операции.</span><span class="sxs-lookup"><span data-stu-id="8d55e-127">The following code fragment shows the operations performed.</span></span>


```
dest.x = src0.x * src1.x;
dest.y = src0.y * src1.y;
dest.z = src0.z * src1.z;
dest.w = src0.w * src1.w;
```



## <a name="related-topics"></a><span data-ttu-id="8d55e-128">См. также</span><span class="sxs-lookup"><span data-stu-id="8d55e-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d55e-129">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="8d55e-129">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




