---
title: ABS-VS
description: Вычисление абсолютного значения. | ABS-VS
ms.assetid: d3b4cf06-dc87-4c71-aa2d-5ade4cf98caa
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e4d73ee738f575d93c2316e4ec47dced7cb128d3
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994751"
---
# <a name="abs---vs"></a><span data-ttu-id="56e61-104">ABS-VS</span><span class="sxs-lookup"><span data-stu-id="56e61-104">abs - vs</span></span>

<span data-ttu-id="56e61-105">Вычисление абсолютного значения.</span><span class="sxs-lookup"><span data-stu-id="56e61-105">Computes absolute value.</span></span>

## <a name="syntax"></a><span data-ttu-id="56e61-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="56e61-106">Syntax</span></span>



|              |
|--------------|
| <span data-ttu-id="56e61-107">ABS DST, src</span><span class="sxs-lookup"><span data-stu-id="56e61-107">abs dst, src</span></span> |



 

<span data-ttu-id="56e61-108">where</span><span class="sxs-lookup"><span data-stu-id="56e61-108">where</span></span>

-   <span data-ttu-id="56e61-109">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="56e61-109">dst is the destination register.</span></span>
-   <span data-ttu-id="56e61-110">src является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="56e61-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="56e61-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="56e61-111">Remarks</span></span>



| <span data-ttu-id="56e61-112">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="56e61-112">Vertex shader versions</span></span> | <span data-ttu-id="56e61-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="56e61-113">1\_1</span></span> | <span data-ttu-id="56e61-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="56e61-114">2\_0</span></span> | <span data-ttu-id="56e61-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="56e61-115">2\_x</span></span> | <span data-ttu-id="56e61-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="56e61-116">2\_sw</span></span> | <span data-ttu-id="56e61-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="56e61-117">3\_0</span></span> | <span data-ttu-id="56e61-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="56e61-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="56e61-119">abs</span><span class="sxs-lookup"><span data-stu-id="56e61-119">abs</span></span>                    |      | <span data-ttu-id="56e61-120">x</span><span class="sxs-lookup"><span data-stu-id="56e61-120">x</span></span>    | <span data-ttu-id="56e61-121">x</span><span class="sxs-lookup"><span data-stu-id="56e61-121">x</span></span>    | <span data-ttu-id="56e61-122">x</span><span class="sxs-lookup"><span data-stu-id="56e61-122">x</span></span>     | <span data-ttu-id="56e61-123">x</span><span class="sxs-lookup"><span data-stu-id="56e61-123">x</span></span>    | <span data-ttu-id="56e61-124">x</span><span class="sxs-lookup"><span data-stu-id="56e61-124">x</span></span>     |



 

<span data-ttu-id="56e61-125">Эта инструкция работает, как показано здесь.</span><span class="sxs-lookup"><span data-stu-id="56e61-125">This instruction works as shown here.</span></span>


```
dest.x = abs(src.x)
dest.y = abs(src.y)
dest.z = abs(src.z)
dest.w = abs(src.w)
```



## <a name="related-topics"></a><span data-ttu-id="56e61-126">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="56e61-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56e61-127">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="56e61-127">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




