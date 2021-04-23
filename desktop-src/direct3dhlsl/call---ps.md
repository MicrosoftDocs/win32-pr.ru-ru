---
title: Call-PS
description: Выполняет вызов функции в инструкцию, помеченную указанной меткой. | Call-PS
ms.assetid: d5f5e5a1-f205-477d-a11b-ff9eeeec6c95
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 27be29c478afdf92c29fefd16a82319e0899d2ec
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998114"
---
# <a name="call---ps"></a><span data-ttu-id="2fd49-104">Call-PS</span><span class="sxs-lookup"><span data-stu-id="2fd49-104">call - ps</span></span>

<span data-ttu-id="2fd49-105">Выполняет вызов функции в инструкцию, помеченную указанной меткой.</span><span class="sxs-lookup"><span data-stu-id="2fd49-105">Performs a function call to the instruction marked with the provided label.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fd49-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2fd49-106">Syntax</span></span>



| <span data-ttu-id="2fd49-107">вызов l\#</span><span class="sxs-lookup"><span data-stu-id="2fd49-107">call l\#</span></span> |
|----------|



 

<span data-ttu-id="2fd49-108">Где:</span><span class="sxs-lookup"><span data-stu-id="2fd49-108">Where:</span></span>

-   <span data-ttu-id="2fd49-109">l \# — [Метка-PS](label---ps.md) , помечающая начало подпрограммы для вызова.</span><span class="sxs-lookup"><span data-stu-id="2fd49-109">l\# is a [label - ps](label---ps.md) marking the beginning of the subroutine to be called.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fd49-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="2fd49-110">Remarks</span></span>



| <span data-ttu-id="2fd49-111">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="2fd49-111">Pixel shader versions</span></span> | <span data-ttu-id="2fd49-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="2fd49-112">1\_1</span></span> | <span data-ttu-id="2fd49-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="2fd49-113">1\_2</span></span> | <span data-ttu-id="2fd49-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="2fd49-114">1\_3</span></span> | <span data-ttu-id="2fd49-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="2fd49-115">1\_4</span></span> | <span data-ttu-id="2fd49-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2fd49-116">2\_0</span></span> | <span data-ttu-id="2fd49-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="2fd49-117">2\_x</span></span> | <span data-ttu-id="2fd49-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="2fd49-118">2\_sw</span></span> | <span data-ttu-id="2fd49-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2fd49-119">3\_0</span></span> | <span data-ttu-id="2fd49-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="2fd49-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="2fd49-121">вызывает</span><span class="sxs-lookup"><span data-stu-id="2fd49-121">call</span></span>                  |      |      |      |      |      | <span data-ttu-id="2fd49-122">x</span><span class="sxs-lookup"><span data-stu-id="2fd49-122">x</span></span>    | <span data-ttu-id="2fd49-123">x</span><span class="sxs-lookup"><span data-stu-id="2fd49-123">x</span></span>     | <span data-ttu-id="2fd49-124">x</span><span class="sxs-lookup"><span data-stu-id="2fd49-124">x</span></span>    | <span data-ttu-id="2fd49-125">x</span><span class="sxs-lookup"><span data-stu-id="2fd49-125">x</span></span>     |



 

<span data-ttu-id="2fd49-126">Эта инструкция выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="2fd49-126">This instruction does the following:</span></span>

1.  <span data-ttu-id="2fd49-127">Адрес принудительной отправки следующей инструкции в стек адресов возврата.</span><span class="sxs-lookup"><span data-stu-id="2fd49-127">Push address of the next instruction to the return address stack.</span></span>
2.  <span data-ttu-id="2fd49-128">Продолжить выполнение из инструкции, помеченной меткой.</span><span class="sxs-lookup"><span data-stu-id="2fd49-128">Continue execution from the instruction marked by the label.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2fd49-129">См. также</span><span class="sxs-lookup"><span data-stu-id="2fd49-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2fd49-130">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="2fd49-130">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




