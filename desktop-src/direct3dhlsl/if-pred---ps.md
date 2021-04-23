---
title: Если пред-PS
description: Начало if bool-PS... else-PS... endif-PS блок с условием, взятым из содержимого регистра предиката.
ms.assetid: 7b43bf71-a2e9-468f-805f-620de065db08
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ead7c5936550715d48ee1ef6a3938b6219558823
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784911"
---
# <a name="if-pred---ps"></a><span data-ttu-id="ce25c-103">Если пред-PS</span><span class="sxs-lookup"><span data-stu-id="ce25c-103">if pred - ps</span></span>

<span data-ttu-id="ce25c-104">Начало [If bool-PS](if-bool---ps.md)... [else-PS](else---ps.md)... [endif-PS](endif---ps.md) блок с условием, взятым из содержимого регистра предиката.</span><span class="sxs-lookup"><span data-stu-id="ce25c-104">Start of an [if bool - ps](if-bool---ps.md)...[else - ps](else---ps.md)...[endif - ps](endif---ps.md) block, with the condition taken from the content of the predicate register.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce25c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ce25c-105">Syntax</span></span>



| <span data-ttu-id="ce25c-106">Если \[ ! \] пред. Репликатесвиззле</span><span class="sxs-lookup"><span data-stu-id="ce25c-106">if \[!\]pred.replicateSwizzle</span></span> |
|-------------------------------|



 

<span data-ttu-id="ce25c-107">Где:</span><span class="sxs-lookup"><span data-stu-id="ce25c-107">Where:</span></span>

-   <span data-ttu-id="ce25c-108">\[!\] является необязательным модификатором NOT.</span><span class="sxs-lookup"><span data-stu-id="ce25c-108">\[!\] is an optional NOT modifier.</span></span> <span data-ttu-id="ce25c-109">Это приводит к изменению значения в регистре предиката.</span><span class="sxs-lookup"><span data-stu-id="ce25c-109">This modifies the value in the predicate register.</span></span>
-   <span data-ttu-id="ce25c-110">"пред" является [регистром предиката](dx9-graphics-reference-asm-ps-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="ce25c-110">pred is the [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).</span></span>
-   <span data-ttu-id="ce25c-111">Репликатесвиззле — это один компонент, который копируется (или реплицируется) во все четыре компонента (свиззлед).</span><span class="sxs-lookup"><span data-stu-id="ce25c-111">replicateSwizzle is a single component that is copied (or replicated) to all four components (swizzled).</span></span> <span data-ttu-id="ce25c-112">Допустимые компоненты: \[ x, y, z, w \] или \[ r, g, b, a \] .</span><span class="sxs-lookup"><span data-stu-id="ce25c-112">Valid components are: \[x, y, z, w\] or \[r, g, b, a\].</span></span>

## <a name="remarks"></a><span data-ttu-id="ce25c-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="ce25c-113">Remarks</span></span>



| <span data-ttu-id="ce25c-114">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="ce25c-114">Pixel shader versions</span></span> | <span data-ttu-id="ce25c-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="ce25c-115">1\_1</span></span> | <span data-ttu-id="ce25c-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="ce25c-116">1\_2</span></span> | <span data-ttu-id="ce25c-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="ce25c-117">1\_3</span></span> | <span data-ttu-id="ce25c-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="ce25c-118">1\_4</span></span> | <span data-ttu-id="ce25c-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ce25c-119">2\_0</span></span> | <span data-ttu-id="ce25c-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="ce25c-120">2\_x</span></span> | <span data-ttu-id="ce25c-121">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="ce25c-121">2\_sw</span></span> | <span data-ttu-id="ce25c-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ce25c-122">3\_0</span></span> | <span data-ttu-id="ce25c-123">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="ce25c-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="ce25c-124">Если \_ пред</span><span class="sxs-lookup"><span data-stu-id="ce25c-124">if\_pred</span></span>              |      |      |      |      |      | <span data-ttu-id="ce25c-125">x</span><span class="sxs-lookup"><span data-stu-id="ce25c-125">x</span></span>    | <span data-ttu-id="ce25c-126">x</span><span class="sxs-lookup"><span data-stu-id="ce25c-126">x</span></span>     | <span data-ttu-id="ce25c-127">x</span><span class="sxs-lookup"><span data-stu-id="ce25c-127">x</span></span>    | <span data-ttu-id="ce25c-128">x</span><span class="sxs-lookup"><span data-stu-id="ce25c-128">x</span></span>     |



 

<span data-ttu-id="ce25c-129">Эта инструкция используется для пропуска блока кода на основе канала регистра предиката.</span><span class="sxs-lookup"><span data-stu-id="ce25c-129">This instruction is used to skip a block of code, based on a channel of the predicate register.</span></span> <span data-ttu-id="ce25c-130">Каждый, если \_ пред-блок должен завершаться инструкцией [else – PS](else---ps.md) или [endif-PS](endif---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="ce25c-130">Each if\_pred block must end with an [else - ps](else---ps.md) or [endif - ps](endif---ps.md) instruction.</span></span>

<span data-ttu-id="ce25c-131">К ним относятся указанные ниже ограничения.</span><span class="sxs-lookup"><span data-stu-id="ce25c-131">Restrictions include:</span></span>

<span data-ttu-id="ce25c-132">Если \_ пред блоки могут быть вложенными.</span><span class="sxs-lookup"><span data-stu-id="ce25c-132">if\_pred blocks can be nested.</span></span> <span data-ttu-id="ce25c-133">Это значение учитывает общую глубину динамического вложения вместе с блоками, [если они \_ соответствуют](if-comp---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="ce25c-133">This counts to the total dynamic nesting depth along with [if\_comp](if-comp---ps.md) blocks.</span></span>

<span data-ttu-id="ce25c-134">Блок «Если//// \_ » не может помешать блоку цикла; он должен быть полностью внутри него или заключаться в него.</span><span class="sxs-lookup"><span data-stu-id="ce25c-134">An if\_pred block cannot straddle a loop block; it should either be completely inside it or surround it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ce25c-135">См. также</span><span class="sxs-lookup"><span data-stu-id="ce25c-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce25c-136">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="ce25c-136">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




