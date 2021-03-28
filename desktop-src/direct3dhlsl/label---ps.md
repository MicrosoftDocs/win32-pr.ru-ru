---
title: Метка-PS
description: Пометьте следующую инструкцию как индекс метки. | Метка-PS
ms.assetid: 21afa062-c536-4891-ba69-ca5284b0539c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f3fb266b649642c82293e8310b6302c6763ddc27
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998155"
---
# <a name="label---ps"></a><span data-ttu-id="b436e-104">Метка-PS</span><span class="sxs-lookup"><span data-stu-id="b436e-104">label - ps</span></span>

<span data-ttu-id="b436e-105">Пометьте следующую инструкцию как индекс метки.</span><span class="sxs-lookup"><span data-stu-id="b436e-105">Mark the next instruction as having a label index.</span></span>

## <a name="syntax"></a><span data-ttu-id="b436e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b436e-106">Syntax</span></span>



| <span data-ttu-id="b436e-107">Метка l\#</span><span class="sxs-lookup"><span data-stu-id="b436e-107">label l\#</span></span> |
|-----------|



 

<span data-ttu-id="b436e-108">где \# определяет номер метки.</span><span class="sxs-lookup"><span data-stu-id="b436e-108">where \# identifies the label number.</span></span>

<span data-ttu-id="b436e-109">Для PS \_ 2 \_ x номер метки должен находиться в диапазоне от 0 до 15.</span><span class="sxs-lookup"><span data-stu-id="b436e-109">For ps\_2\_x, the label number must be between between 0 and 15.</span></span>

<span data-ttu-id="b436e-110">Для PS \_ 2 \_ SW, PS \_ 3 \_ 0 и PS \_ 3 \_ SW номер метки должен находиться в диапазоне от 0 до 2047.</span><span class="sxs-lookup"><span data-stu-id="b436e-110">For ps\_2\_sw, ps\_3\_0, and ps\_3\_sw, the label number must be between between 0 and 2047.</span></span>

## <a name="remarks"></a><span data-ttu-id="b436e-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="b436e-111">Remarks</span></span>



| <span data-ttu-id="b436e-112">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="b436e-112">Pixel shader versions</span></span> | <span data-ttu-id="b436e-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="b436e-113">1\_1</span></span> | <span data-ttu-id="b436e-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="b436e-114">1\_2</span></span> | <span data-ttu-id="b436e-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="b436e-115">1\_3</span></span> | <span data-ttu-id="b436e-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="b436e-116">1\_4</span></span> | <span data-ttu-id="b436e-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b436e-117">2\_0</span></span> | <span data-ttu-id="b436e-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b436e-118">2\_x</span></span> | <span data-ttu-id="b436e-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b436e-119">2\_sw</span></span> | <span data-ttu-id="b436e-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b436e-120">3\_0</span></span> | <span data-ttu-id="b436e-121">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="b436e-121">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="b436e-122">метка</span><span class="sxs-lookup"><span data-stu-id="b436e-122">label</span></span>                 |      |      |      |      |      | <span data-ttu-id="b436e-123">x</span><span class="sxs-lookup"><span data-stu-id="b436e-123">x</span></span>    | <span data-ttu-id="b436e-124">x</span><span class="sxs-lookup"><span data-stu-id="b436e-124">x</span></span>     | <span data-ttu-id="b436e-125">x</span><span class="sxs-lookup"><span data-stu-id="b436e-125">x</span></span>    | <span data-ttu-id="b436e-126">x</span><span class="sxs-lookup"><span data-stu-id="b436e-126">x</span></span>     |



 

<span data-ttu-id="b436e-127">Эта инструкция определяет метку, расположенную в следующей инструкции шейдера.</span><span class="sxs-lookup"><span data-stu-id="b436e-127">This instruction defines a label located at the next shader instruction.</span></span> <span data-ttu-id="b436e-128">Инструкция Label может присутствовать непосредственно после инструкции [RET](ret---ps.md) (которая определяет конец предыдущей подпрограммы или основной программы).</span><span class="sxs-lookup"><span data-stu-id="b436e-128">The label instruction can only be present directly after a [ret](ret---ps.md) instruction (which defines the end of the previous subroutine or main program).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b436e-129">См. также</span><span class="sxs-lookup"><span data-stu-id="b436e-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b436e-130">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="b436e-130">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




