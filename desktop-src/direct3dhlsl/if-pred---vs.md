---
title: Если пред-VS
description: Начало, если пред-и... else-vs... endif — блок VS с условием, взятым из содержимого регистра предиката.
ms.assetid: 03f60ca3-cda0-4653-8582-74d1a75e0aee
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0a1a36bb0c6c68f5132757719bbc7e37fbc71501
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335475"
---
# <a name="if-pred---vs"></a><span data-ttu-id="2e53a-103">Если пред-VS</span><span class="sxs-lookup"><span data-stu-id="2e53a-103">if pred - vs</span></span>

<span data-ttu-id="2e53a-104">Начало, если пред-и... [else-VS](else---vs.md)... [endif — блок VS](endif---vs.md) с условием, взятым из содержимого регистра предиката.</span><span class="sxs-lookup"><span data-stu-id="2e53a-104">Start of an if pred - vs...[else - vs](else---vs.md)...[endif - vs](endif---vs.md) block, with the condition taken from the content of the predicate register.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e53a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2e53a-105">Syntax</span></span>



| <span data-ttu-id="2e53a-106">Если \[ ! \] пред. Репликатесвиззле</span><span class="sxs-lookup"><span data-stu-id="2e53a-106">if \[!\]pred.replicateSwizzle</span></span> |
|-------------------------------|



 

<span data-ttu-id="2e53a-107">Где:</span><span class="sxs-lookup"><span data-stu-id="2e53a-107">Where:</span></span>

-   <span data-ttu-id="2e53a-108">\[!\] Необязательный модификатор NOT.</span><span class="sxs-lookup"><span data-stu-id="2e53a-108">\[!\] an optional NOT modifier.</span></span> <span data-ttu-id="2e53a-109">Это приводит к изменению значения в регистре предиката.</span><span class="sxs-lookup"><span data-stu-id="2e53a-109">This modifies the value in the predicate register.</span></span>
-   <span data-ttu-id="2e53a-110">"пред" — это регистр предиката, P0.</span><span class="sxs-lookup"><span data-stu-id="2e53a-110">pred is the predicate register, p0.</span></span> <span data-ttu-id="2e53a-111">См. раздел [Регистрация предиката](dx9-graphics-reference-asm-vs-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="2e53a-111">See [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md).</span></span>
-   <span data-ttu-id="2e53a-112">Репликатесвиззле — это один компонент, который копируется (или реплицируется) во все четыре компонента (свиззлед).</span><span class="sxs-lookup"><span data-stu-id="2e53a-112">replicateSwizzle is a single component that is copied (or replicated) to all four components (swizzled).</span></span> <span data-ttu-id="2e53a-113">Допустимые компоненты: x, y, z, w или r, g, b, a.</span><span class="sxs-lookup"><span data-stu-id="2e53a-113">Valid components are: x, y, z, w or r, g, b, a.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e53a-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="2e53a-114">Remarks</span></span>



| <span data-ttu-id="2e53a-115">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="2e53a-115">Vertex shader versions</span></span> | <span data-ttu-id="2e53a-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="2e53a-116">1\_1</span></span> | <span data-ttu-id="2e53a-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2e53a-117">2\_0</span></span> | <span data-ttu-id="2e53a-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="2e53a-118">2\_x</span></span> | <span data-ttu-id="2e53a-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="2e53a-119">2\_sw</span></span> | <span data-ttu-id="2e53a-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2e53a-120">3\_0</span></span> | <span data-ttu-id="2e53a-121">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="2e53a-121">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="2e53a-122">Если пред</span><span class="sxs-lookup"><span data-stu-id="2e53a-122">if pred</span></span>                |      |      | <span data-ttu-id="2e53a-123">x</span><span class="sxs-lookup"><span data-stu-id="2e53a-123">x</span></span>    | <span data-ttu-id="2e53a-124">x</span><span class="sxs-lookup"><span data-stu-id="2e53a-124">x</span></span>     | <span data-ttu-id="2e53a-125">x</span><span class="sxs-lookup"><span data-stu-id="2e53a-125">x</span></span>    | <span data-ttu-id="2e53a-126">x</span><span class="sxs-lookup"><span data-stu-id="2e53a-126">x</span></span>     |



 

<span data-ttu-id="2e53a-127">Эта инструкция используется для пропуска блока кода на основе канала регистра предиката.</span><span class="sxs-lookup"><span data-stu-id="2e53a-127">This instruction is used to skip a block of code, based on a channel of the predicate register.</span></span> <span data-ttu-id="2e53a-128">Каждый, если \_ пред блок должен завершаться инструкцией Else или endif.</span><span class="sxs-lookup"><span data-stu-id="2e53a-128">Each if\_pred block must end with an else or endif instruction.</span></span>

<span data-ttu-id="2e53a-129">К ним относятся указанные ниже ограничения.</span><span class="sxs-lookup"><span data-stu-id="2e53a-129">Restrictions include:</span></span>

<span data-ttu-id="2e53a-130">Если \_ пред блоки могут быть вложенными.</span><span class="sxs-lookup"><span data-stu-id="2e53a-130">if\_pred blocks can be nested.</span></span> <span data-ttu-id="2e53a-131">Это значение учитывает общую глубину динамического вложения вместе с блоками, [если они \_ соответствуют](if-comp---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="2e53a-131">This counts to the total dynamic nesting depth along with [if\_comp](if-comp---vs.md) blocks.</span></span>

<span data-ttu-id="2e53a-132">Блок «Если//// \_ » не может помешать блоку цикла, он должен быть полностью внутри него или заключаться в него.</span><span class="sxs-lookup"><span data-stu-id="2e53a-132">An if\_pred block cannot straddle a loop block, it should be either completely inside it or surround it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2e53a-133">См. также</span><span class="sxs-lookup"><span data-stu-id="2e53a-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e53a-134">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="2e53a-134">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




