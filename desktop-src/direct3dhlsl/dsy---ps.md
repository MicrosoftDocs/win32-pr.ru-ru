---
title: ДСИ-PS
description: Вычисление скорости изменения в направлении y для целевого объекта отрисовки.
ms.assetid: b35862d7-fc43-4cf8-bfe3-3eccbda2a133
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c5f595d836ed8eb8525175ddb81e743cb7a04811
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412155"
---
# <a name="dsy---ps"></a><span data-ttu-id="55a3b-103">ДСИ-PS</span><span class="sxs-lookup"><span data-stu-id="55a3b-103">dsy - ps</span></span>

<span data-ttu-id="55a3b-104">Вычисление скорости изменения в направлении y для целевого объекта отрисовки.</span><span class="sxs-lookup"><span data-stu-id="55a3b-104">Compute the rate of change in the render target's y-direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="55a3b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="55a3b-105">Syntax</span></span>



| <span data-ttu-id="55a3b-106">ДСИ DST, src</span><span class="sxs-lookup"><span data-stu-id="55a3b-106">dsy dst, src</span></span> |
|--------------|



 

<span data-ttu-id="55a3b-107">Где:</span><span class="sxs-lookup"><span data-stu-id="55a3b-107">Where:</span></span>

-   <span data-ttu-id="55a3b-108">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="55a3b-108">dst is a destination register.</span></span>
-   <span data-ttu-id="55a3b-109">src является регистром входного источника.</span><span class="sxs-lookup"><span data-stu-id="55a3b-109">src is an input source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="55a3b-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="55a3b-110">Remarks</span></span>



| <span data-ttu-id="55a3b-111">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="55a3b-111">Pixel shader versions</span></span> | <span data-ttu-id="55a3b-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="55a3b-112">1\_1</span></span> | <span data-ttu-id="55a3b-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="55a3b-113">1\_2</span></span> | <span data-ttu-id="55a3b-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="55a3b-114">1\_3</span></span> | <span data-ttu-id="55a3b-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="55a3b-115">1\_4</span></span> | <span data-ttu-id="55a3b-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="55a3b-116">2\_0</span></span> | <span data-ttu-id="55a3b-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="55a3b-117">2\_x</span></span> | <span data-ttu-id="55a3b-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="55a3b-118">2\_sw</span></span> | <span data-ttu-id="55a3b-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="55a3b-119">3\_0</span></span> | <span data-ttu-id="55a3b-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="55a3b-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="55a3b-121">дси</span><span class="sxs-lookup"><span data-stu-id="55a3b-121">dsy</span></span>                   |      |      |      |      |      | <span data-ttu-id="55a3b-122">x</span><span class="sxs-lookup"><span data-stu-id="55a3b-122">x</span></span>    | <span data-ttu-id="55a3b-123">x</span><span class="sxs-lookup"><span data-stu-id="55a3b-123">x</span></span>     | <span data-ttu-id="55a3b-124">x</span><span class="sxs-lookup"><span data-stu-id="55a3b-124">x</span></span>    | <span data-ttu-id="55a3b-125">x</span><span class="sxs-lookup"><span data-stu-id="55a3b-125">x</span></span>     |



 

<span data-ttu-id="55a3b-126">Частота изменений, вычисленная на основе регистра исходного кода, является приближением к содержимому того же регистра в смежных пикселях, в которых выполняется пошаговый шейдер с текущим пикселем.</span><span class="sxs-lookup"><span data-stu-id="55a3b-126">The rate of change computed from the source register is an approximation on the contents of the same register in adjacent pixel(s) running the pixel shader in lock-step with the current pixel.</span></span>

<span data-ttu-id="55a3b-127">Инструкции [ДСКС](dsx---ps.md) и ДСИ вычисляют результат, просмотрев текущее содержимое регистра источника (для каждого компонента) для различных пикселей в локальной области, выполняемой на этапе блокировки.</span><span class="sxs-lookup"><span data-stu-id="55a3b-127">The [dsx](dsx---ps.md) And dsy instructions compute their result by looking at the current contents of the source register (per component) for the various pixels in the local area executing in the lock-step.</span></span> <span data-ttu-id="55a3b-128">Точная формула, используемая для вычисления градиента, зависит от оборудования, но должна быть согласована с тем, как оборудование выполняет те же операции, что и часть процесса вычисления уровня детализации для выборки текстуры.</span><span class="sxs-lookup"><span data-stu-id="55a3b-128">The exact formula used to compute the gradient varies depending on the hardware but should be consistent with the way the hardware does the same operations as part of the level-of-detail calculation process for texture sampling.</span></span>

## <a name="related-topics"></a><span data-ttu-id="55a3b-129">См. также</span><span class="sxs-lookup"><span data-stu-id="55a3b-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55a3b-130">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="55a3b-130">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[<span data-ttu-id="55a3b-131">текслдд-PS</span><span class="sxs-lookup"><span data-stu-id="55a3b-131">texldd - ps</span></span>](texldd---ps.md)
</dt> </dl>

 

 




