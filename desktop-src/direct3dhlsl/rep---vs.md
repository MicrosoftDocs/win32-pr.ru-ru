---
title: Представитель-VS
description: Запустить представителя... блок ендреп.
ms.assetid: vs|directx_sdk|~\rep___vs.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5441d5d134ee2d60e14db9f273ec374323f93902
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412165"
---
# <a name="rep---vs"></a><span data-ttu-id="64ab7-103">Представитель-VS</span><span class="sxs-lookup"><span data-stu-id="64ab7-103">rep - vs</span></span>

<span data-ttu-id="64ab7-104">Запустить представителя... блок [ендреп](endrep---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="64ab7-104">Start a rep...[endrep](endrep---vs.md) block.</span></span>

## <a name="syntax"></a><span data-ttu-id="64ab7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="64ab7-105">Syntax</span></span>



| <span data-ttu-id="64ab7-106">Представитель\#</span><span class="sxs-lookup"><span data-stu-id="64ab7-106">rep i\#</span></span> |
|---------|



 

<span data-ttu-id="64ab7-107">где i \# — это целочисленный регистр, указывающий число повторов в компоненте. x.</span><span class="sxs-lookup"><span data-stu-id="64ab7-107">where i\# is an integer register that specifies the repeat count in the .x component.</span></span> <span data-ttu-id="64ab7-108">См. раздел [Постоянный целочисленный регистр](dx9-graphics-reference-asm-vs-registers-constant-integer.md).</span><span class="sxs-lookup"><span data-stu-id="64ab7-108">See [Constant Integer Register](dx9-graphics-reference-asm-vs-registers-constant-integer.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="64ab7-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="64ab7-109">Remarks</span></span>



| <span data-ttu-id="64ab7-110">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="64ab7-110">Vertex shader versions</span></span> | <span data-ttu-id="64ab7-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="64ab7-111">1\_1</span></span> | <span data-ttu-id="64ab7-112">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="64ab7-112">2\_0</span></span> | <span data-ttu-id="64ab7-113">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="64ab7-113">2\_x</span></span> | <span data-ttu-id="64ab7-114">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="64ab7-114">2\_sw</span></span> | <span data-ttu-id="64ab7-115">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="64ab7-115">3\_0</span></span> | <span data-ttu-id="64ab7-116">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="64ab7-116">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="64ab7-117">склад</span><span class="sxs-lookup"><span data-stu-id="64ab7-117">rep</span></span>                    |      | <span data-ttu-id="64ab7-118">x</span><span class="sxs-lookup"><span data-stu-id="64ab7-118">x</span></span>    | <span data-ttu-id="64ab7-119">x</span><span class="sxs-lookup"><span data-stu-id="64ab7-119">x</span></span>    | <span data-ttu-id="64ab7-120">x</span><span class="sxs-lookup"><span data-stu-id="64ab7-120">x</span></span>     | <span data-ttu-id="64ab7-121">x</span><span class="sxs-lookup"><span data-stu-id="64ab7-121">x</span></span>    | <span data-ttu-id="64ab7-122">x</span><span class="sxs-lookup"><span data-stu-id="64ab7-122">x</span></span>     |



 

-   <span data-ttu-id="64ab7-123">i \# . x указывает число итераций.</span><span class="sxs-lookup"><span data-stu-id="64ab7-123">i\#.x specifies the iteration count.</span></span> <span data-ttu-id="64ab7-124">Допустимый диапазон: \[ 0, 255 \] .</span><span class="sxs-lookup"><span data-stu-id="64ab7-124">The legal range is \[0, 255\].</span></span> <span data-ttu-id="64ab7-125">Обратите внимание, что эта инструкция не увеличивает или не уменьшает значение i \# . x.</span><span class="sxs-lookup"><span data-stu-id="64ab7-125">Note that this instruction does not increment or decrement the value of i\#.x.</span></span>
-   <span data-ttu-id="64ab7-126">i \# . ИЗВ не используются в блоке REPEAT.</span><span class="sxs-lookup"><span data-stu-id="64ab7-126">i\#.yzw are not used by the repeat block.</span></span>
-   <span data-ttu-id="64ab7-127">Блоки Repeat могут быть вложенными.</span><span class="sxs-lookup"><span data-stu-id="64ab7-127">Repeat blocks may be nested.</span></span> <span data-ttu-id="64ab7-128">См. раздел [ограничения вложений управления потоком](dx9-graphics-reference-asm-vs-instructions-flow-control.md).</span><span class="sxs-lookup"><span data-stu-id="64ab7-128">See [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md).</span></span>
-   <span data-ttu-id="64ab7-129">Блоки Repeat могут быть либо полностью внутри \* блока if, либо полностью окружающи ее.</span><span class="sxs-lookup"><span data-stu-id="64ab7-129">Repeat blocks are allowed to be either completely inside an if\* block or completely surrounding it.</span></span> <span data-ttu-id="64ab7-130">Помещается в недопустимый.</span><span class="sxs-lookup"><span data-stu-id="64ab7-130">No straddling is allowed.</span></span>
-   <span data-ttu-id="64ab7-131">Использование одного и того же i \# для различных или вложенных инструкций — Точная — каждый цикл выполняет итерацию в зависимости от указанного числа.</span><span class="sxs-lookup"><span data-stu-id="64ab7-131">Using the same i\# for different or nested rep instructions is fine - each loop will iterate based on the specified count.</span></span>

## <a name="example"></a><span data-ttu-id="64ab7-132">Например, .</span><span class="sxs-lookup"><span data-stu-id="64ab7-132">Example</span></span>


```
rep i2
    add r0, r0, c0
endrep  
```



## <a name="related-topics"></a><span data-ttu-id="64ab7-133">См. также</span><span class="sxs-lookup"><span data-stu-id="64ab7-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64ab7-134">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="64ab7-134">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




