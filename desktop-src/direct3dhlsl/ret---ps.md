---
title: RET-PS
description: Принимает адрес инструкции из стека адресов возврата и возобновляет выполнение из него. В случае функции Main эта инструкция останавливает выполнение шейдера.
ms.assetid: f853a137-8944-4f6e-89c0-7fd37d1a468e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b0535a4fcd66a1872b5eaa9ec97c292de710b48c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983833"
---
# <a name="ret---ps"></a><span data-ttu-id="4125e-104">RET-PS</span><span class="sxs-lookup"><span data-stu-id="4125e-104">ret - ps</span></span>

<span data-ttu-id="4125e-105">Принимает адрес инструкции из стека адресов возврата и возобновляет выполнение из него.</span><span class="sxs-lookup"><span data-stu-id="4125e-105">Takes the address of an instruction from the return address stack and continues execution from it.</span></span> <span data-ttu-id="4125e-106">В случае функции Main эта инструкция останавливает выполнение шейдера.</span><span class="sxs-lookup"><span data-stu-id="4125e-106">In the case of the main function, this instruction stops shader execution.</span></span>

## <a name="syntax"></a><span data-ttu-id="4125e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4125e-107">Syntax</span></span>



| <span data-ttu-id="4125e-108">обратно</span><span class="sxs-lookup"><span data-stu-id="4125e-108">ret</span></span> |
|-----|



 

## <a name="remarks"></a><span data-ttu-id="4125e-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="4125e-109">Remarks</span></span>



| <span data-ttu-id="4125e-110">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="4125e-110">Pixel shader versions</span></span> | <span data-ttu-id="4125e-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="4125e-111">1\_1</span></span> | <span data-ttu-id="4125e-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="4125e-112">1\_2</span></span> | <span data-ttu-id="4125e-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="4125e-113">1\_3</span></span> | <span data-ttu-id="4125e-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="4125e-114">1\_4</span></span> | <span data-ttu-id="4125e-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4125e-115">2\_0</span></span> | <span data-ttu-id="4125e-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="4125e-116">2\_x</span></span> | <span data-ttu-id="4125e-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4125e-117">2\_sw</span></span> | <span data-ttu-id="4125e-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="4125e-118">3\_0</span></span> | <span data-ttu-id="4125e-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="4125e-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="4125e-120">обратно</span><span class="sxs-lookup"><span data-stu-id="4125e-120">ret</span></span>                   |      |      |      |      |      | <span data-ttu-id="4125e-121">x</span><span class="sxs-lookup"><span data-stu-id="4125e-121">x</span></span>    | <span data-ttu-id="4125e-122">x</span><span class="sxs-lookup"><span data-stu-id="4125e-122">x</span></span>     | <span data-ttu-id="4125e-123">x</span><span class="sxs-lookup"><span data-stu-id="4125e-123">x</span></span>    | <span data-ttu-id="4125e-124">x</span><span class="sxs-lookup"><span data-stu-id="4125e-124">x</span></span>     |



 

<span data-ttu-id="4125e-125">Эта инструкция принимает адрес инструкции из стека адресов возврата и возобновляет выполнение из него.</span><span class="sxs-lookup"><span data-stu-id="4125e-125">This instruction takes the address of an instruction from the return address stack and continues execution from it.</span></span> <span data-ttu-id="4125e-126">В случае функции Main эта инструкция останавливает выполнение шейдера.</span><span class="sxs-lookup"><span data-stu-id="4125e-126">In the case of the main function, this instruction stops shader execution.</span></span>

<span data-ttu-id="4125e-127">Инструкция ret использует один слот инструкций шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="4125e-127">The ret instruction consumes one vertex shader instruction slot.</span></span>

<span data-ttu-id="4125e-128">Если шейдер не содержит подподпрограмм, использование функции RET в конце основной программы является необязательным.</span><span class="sxs-lookup"><span data-stu-id="4125e-128">If a shader contains no subroutines, using ret at the end of the main program is optional.</span></span>

<span data-ttu-id="4125e-129">Несколько инструкций Return не разрешены в основной программе или в любой подпрограмме, первая инструкция return обрабатывается как конец основной программы или подпрограммы.</span><span class="sxs-lookup"><span data-stu-id="4125e-129">Multiple return statements are not permitted in the main program or in any subroutine, the first return statement is treated as the end of the main program or subroutine.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4125e-130">См. также</span><span class="sxs-lookup"><span data-stu-id="4125e-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4125e-131">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="4125e-131">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




