---
title: ендлуп-PS
description: Конец цикла-PS... блок ендлуп.
ms.assetid: 8d05d0b3-88d2-44e3-a22d-54d8a8ceb5f4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee1a7eb10146e40a39c05bcecb99d3a7667dee2c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103987073"
---
# <a name="endloop---ps"></a><span data-ttu-id="6a42d-103">ендлуп-PS</span><span class="sxs-lookup"><span data-stu-id="6a42d-103">endloop - ps</span></span>

<span data-ttu-id="6a42d-104">Конец [цикла-PS](loop---ps.md)... блок ендлуп.</span><span class="sxs-lookup"><span data-stu-id="6a42d-104">End of a [loop - ps](loop---ps.md)...endloop block.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a42d-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="6a42d-105">Remarks</span></span>



| <span data-ttu-id="6a42d-106">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="6a42d-106">Pixel shader versions</span></span> | <span data-ttu-id="6a42d-107">1\_1</span><span class="sxs-lookup"><span data-stu-id="6a42d-107">1\_1</span></span> | <span data-ttu-id="6a42d-108">1\_2</span><span class="sxs-lookup"><span data-stu-id="6a42d-108">1\_2</span></span> | <span data-ttu-id="6a42d-109">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="6a42d-109">1\_3</span></span> | <span data-ttu-id="6a42d-110">1\_4</span><span class="sxs-lookup"><span data-stu-id="6a42d-110">1\_4</span></span> | <span data-ttu-id="6a42d-111">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6a42d-111">2\_0</span></span> | <span data-ttu-id="6a42d-112">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="6a42d-112">2\_x</span></span> | <span data-ttu-id="6a42d-113">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="6a42d-113">2\_sw</span></span> | <span data-ttu-id="6a42d-114">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6a42d-114">3\_0</span></span> | <span data-ttu-id="6a42d-115">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="6a42d-115">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="6a42d-116">ендлуп</span><span class="sxs-lookup"><span data-stu-id="6a42d-116">endloop</span></span>               |      |      |      |      |      |      |       | <span data-ttu-id="6a42d-117">x</span><span class="sxs-lookup"><span data-stu-id="6a42d-117">x</span></span>    | <span data-ttu-id="6a42d-118">x</span><span class="sxs-lookup"><span data-stu-id="6a42d-118">x</span></span>     |



 

<span data-ttu-id="6a42d-119">ендлуп должен следовать последней инструкции блока [Loop-PS](loop---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="6a42d-119">endloop must follow the last instruction of a [loop - ps](loop---ps.md) block.</span></span>

## <a name="example"></a><span data-ttu-id="6a42d-120">Например, .</span><span class="sxs-lookup"><span data-stu-id="6a42d-120">Example</span></span>


```
loop aL, i3
    add r1, r0, c2[ aL ]
endloop
```



## <a name="related-topics"></a><span data-ttu-id="6a42d-121">См. также</span><span class="sxs-lookup"><span data-stu-id="6a42d-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a42d-122">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="6a42d-122">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




