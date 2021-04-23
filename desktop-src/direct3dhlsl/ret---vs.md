---
title: RET-VS
description: Возврат из подпрограммы или функции Main.
ms.assetid: ee3a6a7a-c068-442f-9f86-c637b5707224
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3b91a9f2fb30dbd243e29043a1655d441215bc75
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335496"
---
# <a name="ret---vs"></a><span data-ttu-id="8bcb3-103">RET-VS</span><span class="sxs-lookup"><span data-stu-id="8bcb3-103">ret - vs</span></span>

<span data-ttu-id="8bcb3-104">Возврат из подпрограммы или функции Main.</span><span class="sxs-lookup"><span data-stu-id="8bcb3-104">Return from a subroutine or a main function.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bcb3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8bcb3-105">Syntax</span></span>



| <span data-ttu-id="8bcb3-106">обратно</span><span class="sxs-lookup"><span data-stu-id="8bcb3-106">ret</span></span> |
|-----|



 

## <a name="remarks"></a><span data-ttu-id="8bcb3-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="8bcb3-107">Remarks</span></span>



| <span data-ttu-id="8bcb3-108">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="8bcb3-108">Vertex shader versions</span></span> | <span data-ttu-id="8bcb3-109">1\_1</span><span class="sxs-lookup"><span data-stu-id="8bcb3-109">1\_1</span></span> | <span data-ttu-id="8bcb3-110">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8bcb3-110">2\_0</span></span> | <span data-ttu-id="8bcb3-111">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="8bcb3-111">2\_x</span></span> | <span data-ttu-id="8bcb3-112">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8bcb3-112">2\_sw</span></span> | <span data-ttu-id="8bcb3-113">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="8bcb3-113">3\_0</span></span> | <span data-ttu-id="8bcb3-114">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="8bcb3-114">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="8bcb3-115">обратно</span><span class="sxs-lookup"><span data-stu-id="8bcb3-115">ret</span></span>                    |      | <span data-ttu-id="8bcb3-116">x</span><span class="sxs-lookup"><span data-stu-id="8bcb3-116">x</span></span>    | <span data-ttu-id="8bcb3-117">x</span><span class="sxs-lookup"><span data-stu-id="8bcb3-117">x</span></span>    | <span data-ttu-id="8bcb3-118">x</span><span class="sxs-lookup"><span data-stu-id="8bcb3-118">x</span></span>     | <span data-ttu-id="8bcb3-119">x</span><span class="sxs-lookup"><span data-stu-id="8bcb3-119">x</span></span>    | <span data-ttu-id="8bcb3-120">x</span><span class="sxs-lookup"><span data-stu-id="8bcb3-120">x</span></span>     |



 

<span data-ttu-id="8bcb3-121">Эта инструкция принимает адрес инструкции из стека адресов возврата и возобновляет выполнение из него.</span><span class="sxs-lookup"><span data-stu-id="8bcb3-121">This instruction takes the address of an instruction from the return address stack and continues execution from it.</span></span> <span data-ttu-id="8bcb3-122">В случае функции Main эта инструкция останавливает выполнение шейдера.</span><span class="sxs-lookup"><span data-stu-id="8bcb3-122">In the case of the main function, this instruction stops shader execution.</span></span>

<span data-ttu-id="8bcb3-123">Инструкция ret использует один слот инструкций шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="8bcb3-123">The ret instruction consumes one vertex shader instruction slot.</span></span>

<span data-ttu-id="8bcb3-124">Если шейдер не содержит подподпрограмм, использование функции RET в конце основной программы является необязательным.</span><span class="sxs-lookup"><span data-stu-id="8bcb3-124">If a shader contains no subroutines, using ret at the end of the main program is optional.</span></span>

<span data-ttu-id="8bcb3-125">Несколько инструкций Return не разрешены в основной программе или в любой подпрограмме, первая инструкция return обрабатывается как конец основной программы или подпрограммы.</span><span class="sxs-lookup"><span data-stu-id="8bcb3-125">Multiple return statements are not permitted in the main program or in any subroutine, the first return statement is treated as the end of the main program or subroutine.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8bcb3-126">См. также</span><span class="sxs-lookup"><span data-stu-id="8bcb3-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8bcb3-127">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="8bcb3-127">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




