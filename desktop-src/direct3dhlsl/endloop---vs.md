---
title: ендлуп — VS
description: Конец цикла... блок ендлуп.
ms.assetid: fd7df120-a927-4a66-b152-6ce5247446e4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8a9aec4d1b2c5237a87fae2c0beab4e8d995db97
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412127"
---
# <a name="endloop---vs"></a><span data-ttu-id="a8638-103">ендлуп — VS</span><span class="sxs-lookup"><span data-stu-id="a8638-103">endloop - vs</span></span>

<span data-ttu-id="a8638-104">Конец [цикла](loop---vs.md)... блок ендлуп.</span><span class="sxs-lookup"><span data-stu-id="a8638-104">End of a [loop](loop---vs.md)...endloop block.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8638-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a8638-105">Syntax</span></span>



| <span data-ttu-id="a8638-106">ендлуп</span><span class="sxs-lookup"><span data-stu-id="a8638-106">endloop</span></span> |
|---------|



 

## <a name="remarks"></a><span data-ttu-id="a8638-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="a8638-107">Remarks</span></span>



| <span data-ttu-id="a8638-108">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="a8638-108">Vertex shader versions</span></span> | <span data-ttu-id="a8638-109">1\_1</span><span class="sxs-lookup"><span data-stu-id="a8638-109">1\_1</span></span> | <span data-ttu-id="a8638-110">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a8638-110">2\_0</span></span> | <span data-ttu-id="a8638-111">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a8638-111">2\_x</span></span> | <span data-ttu-id="a8638-112">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a8638-112">2\_sw</span></span> | <span data-ttu-id="a8638-113">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a8638-113">3\_0</span></span> | <span data-ttu-id="a8638-114">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a8638-114">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="a8638-115">ендлуп</span><span class="sxs-lookup"><span data-stu-id="a8638-115">endloop</span></span>                |      | <span data-ttu-id="a8638-116">x</span><span class="sxs-lookup"><span data-stu-id="a8638-116">x</span></span>    | <span data-ttu-id="a8638-117">x</span><span class="sxs-lookup"><span data-stu-id="a8638-117">x</span></span>    | <span data-ttu-id="a8638-118">x</span><span class="sxs-lookup"><span data-stu-id="a8638-118">x</span></span>     | <span data-ttu-id="a8638-119">x</span><span class="sxs-lookup"><span data-stu-id="a8638-119">x</span></span>    | <span data-ttu-id="a8638-120">x</span><span class="sxs-lookup"><span data-stu-id="a8638-120">x</span></span>     |



 

<span data-ttu-id="a8638-121">Эта инструкция работает, как показано здесь.</span><span class="sxs-lookup"><span data-stu-id="a8638-121">This instruction works as shown here.</span></span>


```
LoopCounter += LoopStep;
LoopInterationCount = LoopIterationCount - 1;
if (LoopIterationCount > 0)
    Continue execution at the StartLoopOffset
```



<span data-ttu-id="a8638-122">ендлуп должен следовать последней инструкции блока [цикла VS](loop---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="a8638-122">endloop must follow the last instruction of a [loop - vs](loop---vs.md) block.</span></span>

## <a name="example"></a><span data-ttu-id="a8638-123">Например, .</span><span class="sxs-lookup"><span data-stu-id="a8638-123">Example</span></span>


```
loop aL, i3
    add r1, r0, c2[ aL ]
endloop
```



## <a name="related-topics"></a><span data-ttu-id="a8638-124">См. также</span><span class="sxs-lookup"><span data-stu-id="a8638-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8638-125">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="a8638-125">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




