---
title: ДСКС-PS
description: Вычисление скорости изменения в направлении x для целевого объекта отрисовки.
ms.assetid: 3358ddca-97a3-421d-8e5d-6b425903e683
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 701dbe0125d10850760e6a1f08a2f84a50c55fe2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103987087"
---
# <a name="dsx---ps"></a><span data-ttu-id="de1ff-103">ДСКС-PS</span><span class="sxs-lookup"><span data-stu-id="de1ff-103">dsx - ps</span></span>

<span data-ttu-id="de1ff-104">Вычисление скорости изменения в направлении x для целевого объекта отрисовки.</span><span class="sxs-lookup"><span data-stu-id="de1ff-104">Compute the rate of change in the render target's x-direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="de1ff-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="de1ff-105">Syntax</span></span>



| <span data-ttu-id="de1ff-106">ДСКС DST, src</span><span class="sxs-lookup"><span data-stu-id="de1ff-106">dsx dst, src</span></span> |
|--------------|



 

<span data-ttu-id="de1ff-107">Где:</span><span class="sxs-lookup"><span data-stu-id="de1ff-107">Where:</span></span>

-   <span data-ttu-id="de1ff-108">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="de1ff-108">dst is a destination register.</span></span>
-   <span data-ttu-id="de1ff-109">src является регистром входного источника.</span><span class="sxs-lookup"><span data-stu-id="de1ff-109">src is an input source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="de1ff-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="de1ff-110">Remarks</span></span>



| <span data-ttu-id="de1ff-111">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="de1ff-111">Pixel shader versions</span></span> | <span data-ttu-id="de1ff-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="de1ff-112">1\_1</span></span> | <span data-ttu-id="de1ff-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="de1ff-113">1\_2</span></span> | <span data-ttu-id="de1ff-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="de1ff-114">1\_3</span></span> | <span data-ttu-id="de1ff-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="de1ff-115">1\_4</span></span> | <span data-ttu-id="de1ff-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="de1ff-116">2\_0</span></span> | <span data-ttu-id="de1ff-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="de1ff-117">2\_x</span></span> | <span data-ttu-id="de1ff-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="de1ff-118">2\_sw</span></span> | <span data-ttu-id="de1ff-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="de1ff-119">3\_0</span></span> | <span data-ttu-id="de1ff-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="de1ff-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="de1ff-121">дскс</span><span class="sxs-lookup"><span data-stu-id="de1ff-121">dsx</span></span>                   |      |      |      |      |      | <span data-ttu-id="de1ff-122">x</span><span class="sxs-lookup"><span data-stu-id="de1ff-122">x</span></span>    | <span data-ttu-id="de1ff-123">x</span><span class="sxs-lookup"><span data-stu-id="de1ff-123">x</span></span>     | <span data-ttu-id="de1ff-124">x</span><span class="sxs-lookup"><span data-stu-id="de1ff-124">x</span></span>    | <span data-ttu-id="de1ff-125">x</span><span class="sxs-lookup"><span data-stu-id="de1ff-125">x</span></span>     |



 

<span data-ttu-id="de1ff-126">Частота изменений, вычисленная на основе регистра исходного кода, является приближением к содержимому того же регистра в смежных пикселях, в которых выполняется пошаговый шейдер с текущим пикселем.</span><span class="sxs-lookup"><span data-stu-id="de1ff-126">The rate of change computed from the source register is an approximation on the contents of the same register in adjacent pixel(s) running the pixel shader in lock-step with the current pixel.</span></span>

<span data-ttu-id="de1ff-127">Инструкции ДСКС и [ДСИ](dsy---ps.md) вычисляют результат, просмотрев текущее содержимое регистра источника (для каждого компонента) для различных пикселей в локальной области, выполняемой на этапе блокировки.</span><span class="sxs-lookup"><span data-stu-id="de1ff-127">The dsx And [dsy](dsy---ps.md) instructions compute their result by looking at the current contents of the source register (per component) for the various pixels in the local area executing in the lock-step.</span></span> <span data-ttu-id="de1ff-128">Точная формула, используемая для вычисления градиента, зависит от оборудования, но должна быть согласована с тем, как оборудование выполняет те же операции, что и часть процесса вычисления уровня детализации для выборки текстуры.</span><span class="sxs-lookup"><span data-stu-id="de1ff-128">The exact formula used to compute the gradient varies depending on the hardware but should be consistent with the way the hardware does the same operations as part of the level-of-detail calculation process for texture sampling.</span></span>

## <a name="related-topics"></a><span data-ttu-id="de1ff-129">См. также</span><span class="sxs-lookup"><span data-stu-id="de1ff-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de1ff-130">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="de1ff-130">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[<span data-ttu-id="de1ff-131">текслдд-PS</span><span class="sxs-lookup"><span data-stu-id="de1ff-131">texldd - ps</span></span>](texldd---ps.md)
</dt> </dl>

 

 




