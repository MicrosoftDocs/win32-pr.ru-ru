---
title: Модификаторы инструкций (Справочник по HLSL VS)
description: Модификаторы инструкций
ms.assetid: b713d847-c858-4492-918c-7a105f751624
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 573f2ef618c4cd29092fb38fb4c805bdeeecc219
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/23/2019
ms.locfileid: "104487200"
---
# <a name="instruction-modifiers-hlsl-vs-reference"></a><span data-ttu-id="9a246-103">Модификаторы инструкций (Справочник по HLSL VS)</span><span class="sxs-lookup"><span data-stu-id="9a246-103">Instruction modifiers (HLSL VS reference)</span></span>

<span data-ttu-id="9a246-104">Модификаторы инструкций влияют на результат инструкции перед его записью в регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="9a246-104">Instruction modifiers affect the result of the instruction before it is written into the destination register.</span></span>

## <a name="_sat"></a><span data-ttu-id="9a246-105">\_Кот</span><span class="sxs-lookup"><span data-stu-id="9a246-105">\_sat</span></span>

<span data-ttu-id="9a246-106">Насыщенность (или фиксации) результата инструкции в \[ 0, 1 \] диапазон перед записью в регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="9a246-106">Saturates (or clamps) the instruction result to \[0,1\] range before writing to the destination register.</span></span>

<span data-ttu-id="9a246-107">Например:</span><span class="sxs-lookup"><span data-stu-id="9a246-107">For example:</span></span>


```
add_sat dst, src0, src1
```



<span data-ttu-id="9a246-108">Где:</span><span class="sxs-lookup"><span data-stu-id="9a246-108">Where:</span></span>

<span data-ttu-id="9a246-109">DST = срез \_ между \_ 0 \_ и \_ 1 (src0 + src1)</span><span class="sxs-lookup"><span data-stu-id="9a246-109">dst = clamp\_between\_0\_and\_1(src0 + src1)</span></span>

<span data-ttu-id="9a246-110">\_Модификатор инструкции "Кот" не требует дополнительных слотов инструкций.</span><span class="sxs-lookup"><span data-stu-id="9a246-110">The \_sat instruction modifier costs no additional instruction slots.</span></span>

<span data-ttu-id="9a246-111">Если поддерживается, \_ Модификатор инструкции «Кот» можно использовать с любыми инструкциями, кроме: [ФРК-VS](frc---vs.md), [синкос-VS](sincos---vs.md)и [текслдл-VS](texldl---vs.md).</span><span class="sxs-lookup"><span data-stu-id="9a246-111">If supported, the \_sat instruction modifier can be used with any instruction except: [frc - vs](frc---vs.md), [sincos - vs](sincos---vs.md), and [texldl - vs](texldl---vs.md).</span></span>



| <span data-ttu-id="9a246-112">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="9a246-112">Vertex shader versions</span></span> | <span data-ttu-id="9a246-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="9a246-113">1\_1</span></span> | <span data-ttu-id="9a246-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9a246-114">2\_0</span></span> | <span data-ttu-id="9a246-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="9a246-115">2\_x</span></span> | <span data-ttu-id="9a246-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="9a246-116">2\_sw</span></span> | <span data-ttu-id="9a246-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9a246-117">3\_0</span></span> | <span data-ttu-id="9a246-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="9a246-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="9a246-119">\_Кот</span><span class="sxs-lookup"><span data-stu-id="9a246-119">\_sat</span></span>                  |      |      |      |       | <span data-ttu-id="9a246-120">x</span><span class="sxs-lookup"><span data-stu-id="9a246-120">x</span></span>    | <span data-ttu-id="9a246-121">x</span><span class="sxs-lookup"><span data-stu-id="9a246-121">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="9a246-122">См. также</span><span class="sxs-lookup"><span data-stu-id="9a246-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a246-123">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="9a246-123">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




