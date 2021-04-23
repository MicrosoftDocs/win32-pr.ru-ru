---
title: этап — PS
description: Инструкция этапа отмечает переход между этапом 1 и фазой 2. Если инструкция этапа отсутствует, весь шейдер выполняется так, как если бы это был этап 2-шейдер.
ms.assetid: e0e89425-dc8e-489f-a0d1-3eefbfd09178
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e9a16b01e186de5645ffe65e003ebbe6defca2d5
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104069373"
---
# <a name="phase---ps"></a><span data-ttu-id="cf680-104">этап — PS</span><span class="sxs-lookup"><span data-stu-id="cf680-104">phase - ps</span></span>

<span data-ttu-id="cf680-105">Инструкция этапа отмечает переход между этапом 1 и фазой 2.</span><span class="sxs-lookup"><span data-stu-id="cf680-105">The phase instruction marks the transition between phase 1 and phase 2.</span></span> <span data-ttu-id="cf680-106">Если инструкция этапа отсутствует, весь шейдер выполняется так, как если бы это был этап 2-шейдер.</span><span class="sxs-lookup"><span data-stu-id="cf680-106">If no phase instruction is present, the entire shader runs as if it is a phase 2 shader.</span></span>

<span data-ttu-id="cf680-107">Эта инструкция применима только к версии 1 \_ 4.</span><span class="sxs-lookup"><span data-stu-id="cf680-107">This instruction applies to version 1\_4 only.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf680-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cf680-108">Syntax</span></span>


```
phase
```



## <a name="remarks"></a><span data-ttu-id="cf680-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="cf680-109">Remarks</span></span>



| <span data-ttu-id="cf680-110">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="cf680-110">Pixel shader versions</span></span> | <span data-ttu-id="cf680-111">1\_1</span><span class="sxs-lookup"><span data-stu-id="cf680-111">1\_1</span></span> | <span data-ttu-id="cf680-112">1\_2</span><span class="sxs-lookup"><span data-stu-id="cf680-112">1\_2</span></span> | <span data-ttu-id="cf680-113">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="cf680-113">1\_3</span></span> | <span data-ttu-id="cf680-114">1\_4</span><span class="sxs-lookup"><span data-stu-id="cf680-114">1\_4</span></span> | <span data-ttu-id="cf680-115">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cf680-115">2\_0</span></span> | <span data-ttu-id="cf680-116">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="cf680-116">2\_x</span></span> | <span data-ttu-id="cf680-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="cf680-117">2\_sw</span></span> | <span data-ttu-id="cf680-118">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cf680-118">3\_0</span></span> | <span data-ttu-id="cf680-119">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="cf680-119">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="cf680-120">этап</span><span class="sxs-lookup"><span data-stu-id="cf680-120">phase</span></span>                 |      |      |      | <span data-ttu-id="cf680-121">x</span><span class="sxs-lookup"><span data-stu-id="cf680-121">x</span></span>    |      |      |       |      |       |



 

<span data-ttu-id="cf680-122">Инструкции шейдера, которые выполняются перед инструкцией этапа, являются инструкциями первого этапа.</span><span class="sxs-lookup"><span data-stu-id="cf680-122">Shader instructions that occur before the phase instruction are phase 1 instructions.</span></span> <span data-ttu-id="cf680-123">Все остальные инструкции являются инструкциями второго этапа.</span><span class="sxs-lookup"><span data-stu-id="cf680-123">All other instructions are phase 2 instructions.</span></span> <span data-ttu-id="cf680-124">При наличии двух этапов выполнения инструкций максимальное количество инструкций на шейдер увеличивается.</span><span class="sxs-lookup"><span data-stu-id="cf680-124">By having two phases for instructions, the maximum number of instructions per shader is increased.</span></span>

<span data-ttu-id="cf680-125">Нерекомендуемым побочным эффектом перехода на этапы является то, что альфа-компонент [временных регистров](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) не сохраняется во всех переходах.</span><span class="sxs-lookup"><span data-stu-id="cf680-125">The unfortunate side-effect of the phase transition is that the alpha component of [temporary registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) do not persist across the transition.</span></span> <span data-ttu-id="cf680-126">Иными словами, компонент Alpha должен быть повторно инициализирован после инструкции этапа.</span><span class="sxs-lookup"><span data-stu-id="cf680-126">In other words, the alpha component must be reinitialized after the phase instruction.</span></span>

## <a name="example"></a><span data-ttu-id="cf680-127">Например, .</span><span class="sxs-lookup"><span data-stu-id="cf680-127">Example</span></span>

<span data-ttu-id="cf680-128">В этом примере показано, как группировать инструкции в виде шагов 1 или 2 этапа в шейдере.</span><span class="sxs-lookup"><span data-stu-id="cf680-128">This example shows how to group instructions as phase 1 or phase 2 instructions within a shader.</span></span>

<span data-ttu-id="cf680-129">Инструкция этапа также часто называется маркером этапа, так как он отмечает переход между этапами 1 и 2.</span><span class="sxs-lookup"><span data-stu-id="cf680-129">The phase instruction is also commonly called the phase marker because it marks the transition between phase 1 and 2 instructions.</span></span> <span data-ttu-id="cf680-130">В \_ шейдере версии 1 4 пикселя, если маркер этапа отсутствует, шейдер выполняется так, как если бы он был запущен на этапе 2.</span><span class="sxs-lookup"><span data-stu-id="cf680-130">In a version 1\_4 pixel shader, if the phase marker is not present, the shader is run as if it is running in phase 2.</span></span> <span data-ttu-id="cf680-131">Это важно, поскольку существуют различия между этапом 1 и 2 инструкциями и регистрацией доступности.</span><span class="sxs-lookup"><span data-stu-id="cf680-131">This is important because there are differences between phase 1 and 2 instructions and register availability.</span></span> <span data-ttu-id="cf680-132">Различия указаны во всем разделе справки.</span><span class="sxs-lookup"><span data-stu-id="cf680-132">The differences are noted throughout the reference section.</span></span>


```
ps_1_4
  // Add phase 1 instructions here

phase
  // Add phase 2 instructions here
```



## <a name="related-topics"></a><span data-ttu-id="cf680-133">См. также</span><span class="sxs-lookup"><span data-stu-id="cf680-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf680-134">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="cf680-134">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




