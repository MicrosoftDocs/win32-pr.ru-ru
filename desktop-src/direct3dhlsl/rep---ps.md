---
title: Представитель-PS
description: Запустить представителя... блок ендреп-PS.
ms.assetid: vs|directx_sdk|~\rep___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a6873a6aee9e31b1f28ba2755b1869cddb177306
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784923"
---
# <a name="rep---ps"></a><span data-ttu-id="7deef-103">Представитель-PS</span><span class="sxs-lookup"><span data-stu-id="7deef-103">rep - ps</span></span>

<span data-ttu-id="7deef-104">Запустить представителя... блок [ендреп-PS](endrep---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="7deef-104">Start a rep...[endrep - ps](endrep---ps.md) block.</span></span>

## <a name="syntax"></a><span data-ttu-id="7deef-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7deef-105">Syntax</span></span>



| <span data-ttu-id="7deef-106">Представитель\#</span><span class="sxs-lookup"><span data-stu-id="7deef-106">rep i\#</span></span> |
|---------|



 

<span data-ttu-id="7deef-107">где i \# — это целочисленный регистр, указывающий число повторов в компоненте. x.</span><span class="sxs-lookup"><span data-stu-id="7deef-107">where i\# is an integer register that specifies the repeat count in the .x component.</span></span> <span data-ttu-id="7deef-108">См. раздел [Постоянный целочисленный регистр](dx9-graphics-reference-asm-ps-registers-constant-integer.md).</span><span class="sxs-lookup"><span data-stu-id="7deef-108">See [Constant Integer Register](dx9-graphics-reference-asm-ps-registers-constant-integer.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7deef-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="7deef-109">Remarks</span></span>



| <span data-ttu-id="7deef-110">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="7deef-110">Pixel shader versions</span></span> | <span data-ttu-id="7deef-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="7deef-111">1\_1</span></span> | <span data-ttu-id="7deef-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="7deef-112">1\_2</span></span> | <span data-ttu-id="7deef-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="7deef-113">1\_3</span></span> | <span data-ttu-id="7deef-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="7deef-114">1\_4</span></span> | <span data-ttu-id="7deef-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7deef-115">2\_0</span></span> | <span data-ttu-id="7deef-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="7deef-116">2\_x</span></span> | <span data-ttu-id="7deef-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7deef-117">2\_sw</span></span> | <span data-ttu-id="7deef-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7deef-118">3\_0</span></span> | <span data-ttu-id="7deef-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7deef-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="7deef-120">склад</span><span class="sxs-lookup"><span data-stu-id="7deef-120">rep</span></span>                   |      |      |      |      |      | <span data-ttu-id="7deef-121">x</span><span class="sxs-lookup"><span data-stu-id="7deef-121">x</span></span>    | <span data-ttu-id="7deef-122">x</span><span class="sxs-lookup"><span data-stu-id="7deef-122">x</span></span>     | <span data-ttu-id="7deef-123">x</span><span class="sxs-lookup"><span data-stu-id="7deef-123">x</span></span>    | <span data-ttu-id="7deef-124">x</span><span class="sxs-lookup"><span data-stu-id="7deef-124">x</span></span>     |



 

-   <span data-ttu-id="7deef-125">i \# . x указывает число итераций.</span><span class="sxs-lookup"><span data-stu-id="7deef-125">i\#.x specifies the iteration count.</span></span> <span data-ttu-id="7deef-126">Допустимый диапазон: \[ 0, 255 \] .</span><span class="sxs-lookup"><span data-stu-id="7deef-126">The legal range is \[0, 255\].</span></span> <span data-ttu-id="7deef-127">Обратите внимание, что эта инструкция не увеличивает или не уменьшает значение i \# . x.</span><span class="sxs-lookup"><span data-stu-id="7deef-127">Note that this instruction does not increment or decrement the value of i\#.x.</span></span>
-   <span data-ttu-id="7deef-128">i \# . ИЗВ не используются в блоке REPEAT.</span><span class="sxs-lookup"><span data-stu-id="7deef-128">i\#.yzw are not used by the repeat block.</span></span>
-   <span data-ttu-id="7deef-129">Блоки Repeat могут быть вложенными.</span><span class="sxs-lookup"><span data-stu-id="7deef-129">Repeat blocks may be nested.</span></span> <span data-ttu-id="7deef-130">См. раздел [ограничения управления потоком](dx9-graphics-reference-asm-ps-instructions-flow-control.md).</span><span class="sxs-lookup"><span data-stu-id="7deef-130">See [Flow Control Limitations](dx9-graphics-reference-asm-ps-instructions-flow-control.md).</span></span>
-   <span data-ttu-id="7deef-131">Блоки Repeat могут быть либо полностью внутри \* блока if, либо полностью окружающи ее.</span><span class="sxs-lookup"><span data-stu-id="7deef-131">Repeat blocks are allowed to be either completely inside an if\* block or completely surrounding it.</span></span> <span data-ttu-id="7deef-132">Помещается в недопустимый.</span><span class="sxs-lookup"><span data-stu-id="7deef-132">No straddling is allowed.</span></span>
-   <span data-ttu-id="7deef-133">Использование одного и того же i \# для различных или вложенных инструкций — Точная — каждый цикл выполняет итерацию в зависимости от указанного числа.</span><span class="sxs-lookup"><span data-stu-id="7deef-133">Using the same i\# for different or nested rep instructions is fine - each loop will iterate based on the specified count.</span></span>

## <a name="example"></a><span data-ttu-id="7deef-134">Например, .</span><span class="sxs-lookup"><span data-stu-id="7deef-134">Example</span></span>


```
rep i2
    add r0, r0, c0
endrep  
```



## <a name="related-topics"></a><span data-ttu-id="7deef-135">См. также</span><span class="sxs-lookup"><span data-stu-id="7deef-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7deef-136">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="7deef-136">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




