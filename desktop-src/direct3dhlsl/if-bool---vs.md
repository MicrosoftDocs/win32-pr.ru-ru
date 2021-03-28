---
title: Если bool — VS
description: Запускает if... else... endif — блок vs.
ms.assetid: d77e2f81-400c-4997-9c34-426b6e6f47be
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 261ff572cbaf519cc0099f3ab68d1a0becca706f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104069318"
---
# <a name="if-bool---vs"></a><span data-ttu-id="ffd2d-103">Если bool — VS</span><span class="sxs-lookup"><span data-stu-id="ffd2d-103">if bool - vs</span></span>

<span data-ttu-id="ffd2d-104">Запускает if... [else](else---vs.md)... [endif — блок VS](endif---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="ffd2d-104">Starts an if...[else](else---vs.md)...[endif - vs](endif---vs.md) block.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffd2d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ffd2d-105">Syntax</span></span>



| <span data-ttu-id="ffd2d-106">Если bool</span><span class="sxs-lookup"><span data-stu-id="ffd2d-106">if bool</span></span> |
|---------|



 

<span data-ttu-id="ffd2d-107">где bool — номер регистра bool.</span><span class="sxs-lookup"><span data-stu-id="ffd2d-107">where bool is a bool register number.</span></span> <span data-ttu-id="ffd2d-108">См. раздел [Постоянный логический регистр](dx9-graphics-reference-asm-vs-registers-constant-boolean.md).</span><span class="sxs-lookup"><span data-stu-id="ffd2d-108">See [Constant Boolean Register](dx9-graphics-reference-asm-vs-registers-constant-boolean.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ffd2d-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="ffd2d-109">Remarks</span></span>



| <span data-ttu-id="ffd2d-110">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="ffd2d-110">Vertex shader versions</span></span> | <span data-ttu-id="ffd2d-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="ffd2d-111">1\_1</span></span> | <span data-ttu-id="ffd2d-112">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ffd2d-112">2\_0</span></span> | <span data-ttu-id="ffd2d-113">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="ffd2d-113">2\_x</span></span> | <span data-ttu-id="ffd2d-114">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="ffd2d-114">2\_sw</span></span> | <span data-ttu-id="ffd2d-115">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ffd2d-115">3\_0</span></span> | <span data-ttu-id="ffd2d-116">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="ffd2d-116">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="ffd2d-117">Если bool</span><span class="sxs-lookup"><span data-stu-id="ffd2d-117">if bool</span></span>                |      | <span data-ttu-id="ffd2d-118">x</span><span class="sxs-lookup"><span data-stu-id="ffd2d-118">x</span></span>    | <span data-ttu-id="ffd2d-119">x</span><span class="sxs-lookup"><span data-stu-id="ffd2d-119">x</span></span>    | <span data-ttu-id="ffd2d-120">x</span><span class="sxs-lookup"><span data-stu-id="ffd2d-120">x</span></span>     | <span data-ttu-id="ffd2d-121">x</span><span class="sxs-lookup"><span data-stu-id="ffd2d-121">x</span></span>    | <span data-ttu-id="ffd2d-122">x</span><span class="sxs-lookup"><span data-stu-id="ffd2d-122">x</span></span>     |



 

<span data-ttu-id="ffd2d-123">Если исходный логический регистр в операторе If имеет значение true, выполняется код, заключенный в операторе if и соответствующий else.</span><span class="sxs-lookup"><span data-stu-id="ffd2d-123">If the source Boolean register in the if statement is true, the code enclosed by the if statement and the matching else is run.</span></span> <span data-ttu-id="ffd2d-124">В противном случае код, заключенный в [else](else---vs.md)... выполняется инструкция [endif-VS](endif---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="ffd2d-124">Otherwise, the code enclosed by the [else](else---vs.md)...[endif - vs](endif---vs.md) statements is run.</span></span> <span data-ttu-id="ffd2d-125">Эта инструкция использует один слот инструкций.</span><span class="sxs-lookup"><span data-stu-id="ffd2d-125">This instruction consumes one instruction slot.</span></span>

<span data-ttu-id="ffd2d-126">Если блоки могут быть вложенными.</span><span class="sxs-lookup"><span data-stu-id="ffd2d-126">if blocks can be nested.</span></span>

<span data-ttu-id="ffd2d-127">Блок if не может помешать блоку цикла.</span><span class="sxs-lookup"><span data-stu-id="ffd2d-127">An if block cannot straddle a loop block.</span></span>

## <a name="example"></a><span data-ttu-id="ffd2d-128">Например, .</span><span class="sxs-lookup"><span data-stu-id="ffd2d-128">Example</span></span>

<span data-ttu-id="ffd2d-129">Эта инструкция предоставляет условное статическое управление потоком.</span><span class="sxs-lookup"><span data-stu-id="ffd2d-129">This instruction provides conditional static flow control.</span></span>


```
defb b2, TRUE

...

if b2
// Instructions to run if b2 is nonzero

else
// Instructions to run otherwise

endif
```



## <a name="related-topics"></a><span data-ttu-id="ffd2d-130">См. также</span><span class="sxs-lookup"><span data-stu-id="ffd2d-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffd2d-131">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="ffd2d-131">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[<span data-ttu-id="ffd2d-132">else — VS</span><span class="sxs-lookup"><span data-stu-id="ffd2d-132">else - vs</span></span>](else---vs.md)
</dt> <dt>

[<span data-ttu-id="ffd2d-133">endif — VS</span><span class="sxs-lookup"><span data-stu-id="ffd2d-133">endif - vs</span></span>](endif---vs.md)
</dt> </dl>

 

 




