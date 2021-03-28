---
title: Loop-PS
description: Запускает цикл... блок ендлуп-PS.
ms.assetid: vs|directx_sdk|~\loop___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cf4c71641003d460e9752dcf33f983c70a82e4f6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104069352"
---
# <a name="loop---ps"></a><span data-ttu-id="f1300-103">Loop-PS</span><span class="sxs-lookup"><span data-stu-id="f1300-103">loop - ps</span></span>

<span data-ttu-id="f1300-104">Запускает цикл... блок [ендлуп-PS](endloop---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="f1300-104">Starts a loop...[endloop - ps](endloop---ps.md) block.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1300-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f1300-105">Syntax</span></span>



| <span data-ttu-id="f1300-106">цикл aL, i\#</span><span class="sxs-lookup"><span data-stu-id="f1300-106">loop aL, i\#</span></span> |
|--------------|



 

<span data-ttu-id="f1300-107">Где:</span><span class="sxs-lookup"><span data-stu-id="f1300-107">Where:</span></span>

-   <span data-ttu-id="f1300-108">aL — это [регистр счетчиков циклов](dx9-graphics-reference-asm-ps-registers-loop-counter.md) , содержащий текущее число циклов.</span><span class="sxs-lookup"><span data-stu-id="f1300-108">aL is the [Loop Counter Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) holding the current loop count.</span></span>
-   <span data-ttu-id="f1300-109">я \# является [постоянным целочисленным регистром](dx9-graphics-reference-asm-ps-registers-constant-integer.md).</span><span class="sxs-lookup"><span data-stu-id="f1300-109">i\# is a [Constant Integer Register](dx9-graphics-reference-asm-ps-registers-constant-integer.md).</span></span> <span data-ttu-id="f1300-110">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="f1300-110">See remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1300-111">Remarks</span><span class="sxs-lookup"><span data-stu-id="f1300-111">Remarks</span></span>



| <span data-ttu-id="f1300-112">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="f1300-112">Pixel shader versions</span></span> | <span data-ttu-id="f1300-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="f1300-113">1\_1</span></span> | <span data-ttu-id="f1300-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="f1300-114">1\_2</span></span> | <span data-ttu-id="f1300-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="f1300-115">1\_3</span></span> | <span data-ttu-id="f1300-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="f1300-116">1\_4</span></span> | <span data-ttu-id="f1300-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f1300-117">2\_0</span></span> | <span data-ttu-id="f1300-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="f1300-118">2\_x</span></span> | <span data-ttu-id="f1300-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f1300-119">2\_sw</span></span> | <span data-ttu-id="f1300-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f1300-120">3\_0</span></span> | <span data-ttu-id="f1300-121">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f1300-121">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="f1300-122">loop</span><span class="sxs-lookup"><span data-stu-id="f1300-122">loop</span></span>                  |      |      |      |      |      |      |       | <span data-ttu-id="f1300-123">x</span><span class="sxs-lookup"><span data-stu-id="f1300-123">x</span></span>    | <span data-ttu-id="f1300-124">x</span><span class="sxs-lookup"><span data-stu-id="f1300-124">x</span></span>     |



 

-   <span data-ttu-id="f1300-125">[Регистр счетчика цикла](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (Al) содержит текущее число циклов и может использоваться для относительной адресации в [регистре входных цветов](dx9-graphics-reference-asm-ps-registers-input-color.md) (v \# ) внутри блока цикла.</span><span class="sxs-lookup"><span data-stu-id="f1300-125">The [Loop Counter Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (aL) holds the current loop count and can be used for relative addressing into [Input Color Register](dx9-graphics-reference-asm-ps-registers-input-color.md) (v\#) inside the loop block.</span></span>
-   <span data-ttu-id="f1300-126">i \# . x указывает число итераций.</span><span class="sxs-lookup"><span data-stu-id="f1300-126">i\#.x specifies the iteration count.</span></span> <span data-ttu-id="f1300-127">Допустимый диапазон: \[ 0, 255 \] .</span><span class="sxs-lookup"><span data-stu-id="f1300-127">The legal range is \[0, 255\].</span></span> <span data-ttu-id="f1300-128">Обратите внимание, что эта инструкция не увеличивает или не уменьшает значение i \# . x.</span><span class="sxs-lookup"><span data-stu-id="f1300-128">Note that this instruction does not increment or decrement the value of i\#.x.</span></span>
-   <span data-ttu-id="f1300-129">i \# . y указывает начальное значение регистра [счетчика циклов](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (Al).</span><span class="sxs-lookup"><span data-stu-id="f1300-129">i\#.y specifies the initial value of the [Loop Counter Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (aL) register.</span></span> <span data-ttu-id="f1300-130">Допустимый диапазон: \[ 0, 255 \] .</span><span class="sxs-lookup"><span data-stu-id="f1300-130">The legal range is \[0, 255\].</span></span> <span data-ttu-id="f1300-131">Обратите внимание, что эта инструкция не увеличивает или не уменьшает значение i \# . y.</span><span class="sxs-lookup"><span data-stu-id="f1300-131">Note that this instruction does not increment or decrement the value of i\#.y.</span></span>
-   <span data-ttu-id="f1300-132">i \# . z указывает размер шага или шаг.</span><span class="sxs-lookup"><span data-stu-id="f1300-132">i\#.z specifies the step/stride size.</span></span> <span data-ttu-id="f1300-133">Допустимый диапазон — \[ 128, 127 \] .</span><span class="sxs-lookup"><span data-stu-id="f1300-133">The legal range is \[-128, 127\].</span></span>
-   <span data-ttu-id="f1300-134">i \# . w не используется блоком цикла и должен быть равен 0.</span><span class="sxs-lookup"><span data-stu-id="f1300-134">i\#.w is not used by the loop block and has to be 0.</span></span>
-   <span data-ttu-id="f1300-135">Блоки циклов могут быть вложенными.</span><span class="sxs-lookup"><span data-stu-id="f1300-135">Loop blocks may be nested.</span></span> <span data-ttu-id="f1300-136">См. раздел [ограничения управления потоком](dx9-graphics-reference-asm-ps-instructions-flow-control.md).</span><span class="sxs-lookup"><span data-stu-id="f1300-136">See [Flow Control Limitations](dx9-graphics-reference-asm-ps-instructions-flow-control.md).</span></span>
-   <span data-ttu-id="f1300-137">При вложении значение [регистра счетчика цикла](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (Al) ссылается на непосредственный блок цикла.</span><span class="sxs-lookup"><span data-stu-id="f1300-137">When nested, the value of the [Loop Counter Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (aL) refers to the immediate enclosing loop block.</span></span>
-   <span data-ttu-id="f1300-138">Блоки циклов могут быть либо полностью внутри \* блока if, либо полностью окружающи его.</span><span class="sxs-lookup"><span data-stu-id="f1300-138">Loop blocks are allowed to be either completely inside an if\* block or completely surrounding it.</span></span> <span data-ttu-id="f1300-139">Помещается в недопустимый.</span><span class="sxs-lookup"><span data-stu-id="f1300-139">No straddling is allowed.</span></span>

## <a name="example"></a><span data-ttu-id="f1300-140">Например, .</span><span class="sxs-lookup"><span data-stu-id="f1300-140">Example</span></span>


```
loop aL, i3
    add r1, r0, v2[ aL ]
endloop
```



## <a name="related-topics"></a><span data-ttu-id="f1300-141">См. также</span><span class="sxs-lookup"><span data-stu-id="f1300-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1300-142">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="f1300-142">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




