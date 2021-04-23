---
title: Метка — VS
description: Пометьте следующую инструкцию как индекс метки. | Метка — VS
ms.assetid: e1aee8bc-4655-4bd5-8012-bd7a2d46e712
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6e2b72fe21301aa66d8428dc3696ceb3f12e6214
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998237"
---
# <a name="label---vs"></a><span data-ttu-id="0c2c9-104">Метка — VS</span><span class="sxs-lookup"><span data-stu-id="0c2c9-104">label - vs</span></span>

<span data-ttu-id="0c2c9-105">Пометьте следующую инструкцию как индекс метки.</span><span class="sxs-lookup"><span data-stu-id="0c2c9-105">Mark the next instruction as having a label index.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c2c9-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0c2c9-106">Syntax</span></span>



| <span data-ttu-id="0c2c9-107">Метка l\#</span><span class="sxs-lookup"><span data-stu-id="0c2c9-107">label l\#</span></span> |
|-----------|



 

<span data-ttu-id="0c2c9-108">где \# определяет номер метки.</span><span class="sxs-lookup"><span data-stu-id="0c2c9-108">where \# identifies the label number.</span></span>

<span data-ttu-id="0c2c9-109">Для VS \_ 2 \_ 0 и VS \_ 2 \_ x номер метки должен находиться в диапазоне от 0 до 15.</span><span class="sxs-lookup"><span data-stu-id="0c2c9-109">For vs\_2\_0, and vs\_2\_x, the label number must be between between 0 and 15.</span></span>

<span data-ttu-id="0c2c9-110">Для VS \_ 2 \_ SW, VS \_ 3 \_ 0 и VS \_ 3 \_ SW номер метки должен находиться в диапазоне от 0 до 2047.</span><span class="sxs-lookup"><span data-stu-id="0c2c9-110">For vs\_2\_sw, vs\_3\_0 and vs\_3\_sw, the label number must be between between 0 and 2047.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c2c9-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="0c2c9-111">Remarks</span></span>



| <span data-ttu-id="0c2c9-112">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="0c2c9-112">Vertex shader versions</span></span> | <span data-ttu-id="0c2c9-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="0c2c9-113">1\_1</span></span> | <span data-ttu-id="0c2c9-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0c2c9-114">2\_0</span></span> | <span data-ttu-id="0c2c9-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="0c2c9-115">2\_x</span></span> | <span data-ttu-id="0c2c9-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0c2c9-116">2\_sw</span></span> | <span data-ttu-id="0c2c9-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0c2c9-117">3\_0</span></span> | <span data-ttu-id="0c2c9-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0c2c9-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="0c2c9-119">метка</span><span class="sxs-lookup"><span data-stu-id="0c2c9-119">label</span></span>                  |      | <span data-ttu-id="0c2c9-120">x</span><span class="sxs-lookup"><span data-stu-id="0c2c9-120">x</span></span>    | <span data-ttu-id="0c2c9-121">x</span><span class="sxs-lookup"><span data-stu-id="0c2c9-121">x</span></span>    | <span data-ttu-id="0c2c9-122">x</span><span class="sxs-lookup"><span data-stu-id="0c2c9-122">x</span></span>     | <span data-ttu-id="0c2c9-123">x</span><span class="sxs-lookup"><span data-stu-id="0c2c9-123">x</span></span>    | <span data-ttu-id="0c2c9-124">x</span><span class="sxs-lookup"><span data-stu-id="0c2c9-124">x</span></span>     |



 

<span data-ttu-id="0c2c9-125">Эта инструкция определяет метку, расположенную в следующей инструкции шейдера.</span><span class="sxs-lookup"><span data-stu-id="0c2c9-125">This instruction defines a label located at the next shader instruction.</span></span> <span data-ttu-id="0c2c9-126">Инструкция Label может присутствовать непосредственно после инструкции [RET](ret---vs.md) (которая определяет конец предыдущей подпрограммы или основной программы).</span><span class="sxs-lookup"><span data-stu-id="0c2c9-126">The label instruction can only be present directly after a [ret](ret---vs.md) instruction (which defines the end of the previous subroutine or main program).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c2c9-127">См. также</span><span class="sxs-lookup"><span data-stu-id="0c2c9-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c2c9-128">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="0c2c9-128">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




