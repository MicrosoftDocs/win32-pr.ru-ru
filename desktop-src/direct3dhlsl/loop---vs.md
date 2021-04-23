---
title: цикл — VS
description: Начать цикл... блок ендлуп.
ms.assetid: vs|directx_sdk|~\loop___vs.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6a96a1ce53b850ec8feeba282055e8111b275bfd
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996922"
---
# <a name="loop---vs"></a><span data-ttu-id="b23a9-103">цикл — VS</span><span class="sxs-lookup"><span data-stu-id="b23a9-103">loop - vs</span></span>

<span data-ttu-id="b23a9-104">Начать цикл... блок [ендлуп](endloop---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="b23a9-104">Start a loop...[endloop](endloop---vs.md) block.</span></span>

## <a name="syntax"></a><span data-ttu-id="b23a9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b23a9-105">Syntax</span></span>



| <span data-ttu-id="b23a9-106">цикл aL, i\#</span><span class="sxs-lookup"><span data-stu-id="b23a9-106">loop aL, i\#</span></span> |
|--------------|



 

<span data-ttu-id="b23a9-107">Где:</span><span class="sxs-lookup"><span data-stu-id="b23a9-107">Where:</span></span>

-   <span data-ttu-id="b23a9-108">aL — это [регистр счетчиков циклов](dx9-graphics-reference-asm-vs-registers-loop-counter.md) , содержащий текущее число циклов.</span><span class="sxs-lookup"><span data-stu-id="b23a9-108">aL is the [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) holding the current loop count.</span></span>
-   <span data-ttu-id="b23a9-109">я \# является [постоянным целочисленным регистром](dx9-graphics-reference-asm-vs-registers-constant-integer.md).</span><span class="sxs-lookup"><span data-stu-id="b23a9-109">i\# is a [Constant Integer Register](dx9-graphics-reference-asm-vs-registers-constant-integer.md).</span></span> <span data-ttu-id="b23a9-110">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="b23a9-110">See remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="b23a9-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="b23a9-111">Remarks</span></span>



| <span data-ttu-id="b23a9-112">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="b23a9-112">Vertex shader versions</span></span> | <span data-ttu-id="b23a9-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="b23a9-113">1\_1</span></span> | <span data-ttu-id="b23a9-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b23a9-114">2\_0</span></span> | <span data-ttu-id="b23a9-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b23a9-115">2\_x</span></span> | <span data-ttu-id="b23a9-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b23a9-116">2\_sw</span></span> | <span data-ttu-id="b23a9-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b23a9-117">3\_0</span></span> | <span data-ttu-id="b23a9-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b23a9-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="b23a9-119">loop</span><span class="sxs-lookup"><span data-stu-id="b23a9-119">loop</span></span>                   |      | <span data-ttu-id="b23a9-120">x</span><span class="sxs-lookup"><span data-stu-id="b23a9-120">x</span></span>    | <span data-ttu-id="b23a9-121">x</span><span class="sxs-lookup"><span data-stu-id="b23a9-121">x</span></span>    | <span data-ttu-id="b23a9-122">x</span><span class="sxs-lookup"><span data-stu-id="b23a9-122">x</span></span>     | <span data-ttu-id="b23a9-123">x</span><span class="sxs-lookup"><span data-stu-id="b23a9-123">x</span></span>    | <span data-ttu-id="b23a9-124">x</span><span class="sxs-lookup"><span data-stu-id="b23a9-124">x</span></span>     |



 

-   <span data-ttu-id="b23a9-125">[Регистр счетчика цикла](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (Al) содержит текущее число циклов и может использоваться для относительных адресов в [Постоянный целочисленный регистр](dx9-graphics-reference-asm-vs-registers-constant-integer.md) (c \# ) или [выходные регистры](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o \# ) внутри блока цикла.</span><span class="sxs-lookup"><span data-stu-id="b23a9-125">The [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL) holds the current loop count, and can be used for relative addressing into [Constant Integer Register](dx9-graphics-reference-asm-vs-registers-constant-integer.md) (c\#) or [Output Registers](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o\#) inside the loop block.</span></span>
-   <span data-ttu-id="b23a9-126">i \# . x указывает число итераций.</span><span class="sxs-lookup"><span data-stu-id="b23a9-126">i\#.x specifies the iteration count.</span></span> <span data-ttu-id="b23a9-127">Допустимый диапазон: \[ 0, 255 \] .</span><span class="sxs-lookup"><span data-stu-id="b23a9-127">The legal range is \[0, 255\].</span></span> <span data-ttu-id="b23a9-128">Обратите внимание, что эта инструкция не увеличивает или не уменьшает значение i \# . x.</span><span class="sxs-lookup"><span data-stu-id="b23a9-128">Note that this instruction does not increment or decrement the value of i\#.x.</span></span>
-   <span data-ttu-id="b23a9-129">i \# . y указывает начальное значение регистра [счетчика циклов](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (Al).</span><span class="sxs-lookup"><span data-stu-id="b23a9-129">i\#.y specifies the initial value of the [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL) register.</span></span> <span data-ttu-id="b23a9-130">Допустимый диапазон: \[ 0, 255 \] .</span><span class="sxs-lookup"><span data-stu-id="b23a9-130">The legal range is \[0, 255\].</span></span> <span data-ttu-id="b23a9-131">Обратите внимание, что эта инструкция не увеличивает или не уменьшает значение i \# . y.</span><span class="sxs-lookup"><span data-stu-id="b23a9-131">Note that this instruction does not increment or decrement the value of i\#.y.</span></span>
-   <span data-ttu-id="b23a9-132">i \# . z указывает размер шага или шаг.</span><span class="sxs-lookup"><span data-stu-id="b23a9-132">i\#.z specifies the step/stride size.</span></span> <span data-ttu-id="b23a9-133">Допустимый диапазон — \[ 128, 127 \] .</span><span class="sxs-lookup"><span data-stu-id="b23a9-133">The legal range is \[-128, 127\].</span></span>
-   <span data-ttu-id="b23a9-134">i \# . w не используется, и его значение должно быть равно 0.</span><span class="sxs-lookup"><span data-stu-id="b23a9-134">i\#.w is not used and must be set to 0.</span></span>
-   <span data-ttu-id="b23a9-135">Блоки циклов могут быть вложенными.</span><span class="sxs-lookup"><span data-stu-id="b23a9-135">Loop blocks may be nested.</span></span> <span data-ttu-id="b23a9-136">См. раздел [ограничения вложений управления потоком](dx9-graphics-reference-asm-vs-instructions-flow-control.md).</span><span class="sxs-lookup"><span data-stu-id="b23a9-136">See [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md).</span></span>
-   <span data-ttu-id="b23a9-137">При вложении значение [регистра счетчика цикла](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (Al) ссылается на непосредственный блок цикла.</span><span class="sxs-lookup"><span data-stu-id="b23a9-137">When nested, the value of the [Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL) refers to the immediate enclosing loop block.</span></span>
-   <span data-ttu-id="b23a9-138">Блоки циклов могут быть либо полностью внутри \* блока if, либо полностью окружающи его.</span><span class="sxs-lookup"><span data-stu-id="b23a9-138">Loop blocks are allowed to be either completely inside an if\* block or completely surrounding it.</span></span> <span data-ttu-id="b23a9-139">Помещается в недопустимый.</span><span class="sxs-lookup"><span data-stu-id="b23a9-139">No straddling is allowed.</span></span>

## <a name="example"></a><span data-ttu-id="b23a9-140">Например, .</span><span class="sxs-lookup"><span data-stu-id="b23a9-140">Example</span></span>


```
loop aL, i3
    add r1, r0, c2[aL]
endloop
```



## <a name="related-topics"></a><span data-ttu-id="b23a9-141">См. также</span><span class="sxs-lookup"><span data-stu-id="b23a9-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b23a9-142">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="b23a9-142">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




