---
title: If bool-PS
description: Начало блока if.
ms.assetid: cff53072-1c73-4cf8-9ecd-11032a9c4bbb
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 92c3158a09aeb871ef367133c07278b0f3b87390
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784890"
---
# <a name="if-bool---ps"></a><span data-ttu-id="98860-103">If bool-PS</span><span class="sxs-lookup"><span data-stu-id="98860-103">if bool - ps</span></span>

<span data-ttu-id="98860-104">Начало блока if.</span><span class="sxs-lookup"><span data-stu-id="98860-104">Start of an if block.</span></span>

## <a name="syntax"></a><span data-ttu-id="98860-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="98860-105">Syntax</span></span>



| <span data-ttu-id="98860-106">Если bool</span><span class="sxs-lookup"><span data-stu-id="98860-106">if bool</span></span> |
|---------|



 

<span data-ttu-id="98860-107">Где:</span><span class="sxs-lookup"><span data-stu-id="98860-107">Where:</span></span>

-   <span data-ttu-id="98860-108">bool представляет собой логический (логический) номер регистра.</span><span class="sxs-lookup"><span data-stu-id="98860-108">bool is a bool (Boolean) register number.</span></span> <span data-ttu-id="98860-109">См. раздел [Постоянный логический регистр](dx9-graphics-reference-asm-ps-registers-constant-boolean.md).</span><span class="sxs-lookup"><span data-stu-id="98860-109">See [Constant Boolean Register](dx9-graphics-reference-asm-ps-registers-constant-boolean.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="98860-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="98860-110">Remarks</span></span>



| <span data-ttu-id="98860-111">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="98860-111">Pixel shader versions</span></span> | <span data-ttu-id="98860-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="98860-112">1\_1</span></span> | <span data-ttu-id="98860-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="98860-113">1\_2</span></span> | <span data-ttu-id="98860-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="98860-114">1\_3</span></span> | <span data-ttu-id="98860-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="98860-115">1\_4</span></span> | <span data-ttu-id="98860-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="98860-116">2\_0</span></span> | <span data-ttu-id="98860-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="98860-117">2\_x</span></span> | <span data-ttu-id="98860-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="98860-118">2\_sw</span></span> | <span data-ttu-id="98860-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="98860-119">3\_0</span></span> | <span data-ttu-id="98860-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="98860-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="98860-121">Если bool</span><span class="sxs-lookup"><span data-stu-id="98860-121">if bool</span></span>               |      |      |      |      |      | <span data-ttu-id="98860-122">x</span><span class="sxs-lookup"><span data-stu-id="98860-122">x</span></span>    | <span data-ttu-id="98860-123">x</span><span class="sxs-lookup"><span data-stu-id="98860-123">x</span></span>     | <span data-ttu-id="98860-124">x</span><span class="sxs-lookup"><span data-stu-id="98860-124">x</span></span>    | <span data-ttu-id="98860-125">x</span><span class="sxs-lookup"><span data-stu-id="98860-125">x</span></span>     |



 

<span data-ttu-id="98860-126">Если исходный логический регистр в операторе If имеет значение true, выполняется код, заключенный в операторе if и соответствующий параметру [endif-PS](endif---ps.md) или [else-PS](else---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="98860-126">If the source Boolean register in the if statement is true, the code enclosed by the if statement and the matching [endif - ps](endif---ps.md) or [else - ps](else---ps.md) is executed.</span></span> <span data-ttu-id="98860-127">В противном случае код, заключенный в else-PS... выполняется инструкция endif-PS.</span><span class="sxs-lookup"><span data-stu-id="98860-127">Otherwise, the code enclosed by the else - ps...endif - ps statements is executed.</span></span> <span data-ttu-id="98860-128">Эта инструкция использует один слот инструкций.</span><span class="sxs-lookup"><span data-stu-id="98860-128">This instruction consumes one instruction slot.</span></span>

<span data-ttu-id="98860-129">Блок If может быть вложенным.</span><span class="sxs-lookup"><span data-stu-id="98860-129">An if block can be nested.</span></span>

<span data-ttu-id="98860-130">Блок if не может помешать блоку цикла.</span><span class="sxs-lookup"><span data-stu-id="98860-130">An if block cannot straddle a loop block.</span></span>

<span data-ttu-id="98860-131">За блоком if может следовать блок инструкции, или инструкция [else-PS](else---ps.md) , а также инструкция [endif-PS](endif---ps.md) .</span><span class="sxs-lookup"><span data-stu-id="98860-131">An if block can be followed by a statement block, and/or an [else - ps](else---ps.md) instruction, and/or an [endif - ps](endif---ps.md) instruction.</span></span>

## <a name="example"></a><span data-ttu-id="98860-132">Например, .</span><span class="sxs-lookup"><span data-stu-id="98860-132">Example</span></span>

<span data-ttu-id="98860-133">Эта инструкция предоставляет условное статическое управление потоком.</span><span class="sxs-lookup"><span data-stu-id="98860-133">This instruction provides conditional static flow control.</span></span>


```
defb b3, true

if b3
// Instructions to run if b3 is nonzero
else
// Instructions to run otherwise
endif
```



## <a name="related-topics"></a><span data-ttu-id="98860-134">См. также</span><span class="sxs-lookup"><span data-stu-id="98860-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98860-135">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="98860-135">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[<span data-ttu-id="98860-136">else-PS</span><span class="sxs-lookup"><span data-stu-id="98860-136">else - ps</span></span>](else---ps.md)
</dt> <dt>

[<span data-ttu-id="98860-137">endif-PS</span><span class="sxs-lookup"><span data-stu-id="98860-137">endif - ps</span></span>](endif---ps.md)
</dt> </dl>

 

 




