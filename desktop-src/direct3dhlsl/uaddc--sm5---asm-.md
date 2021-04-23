---
title: уаддк (SM5-ASM)
description: Целое число без знака, добавленное с помощью макрокоманды.
ms.assetid: 1007253C-F920-4003-B266-D124A255F731
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f57f75be617e32c15212207110851520a7a281e2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104532867"
---
# <a name="uaddc-sm5---asm"></a><span data-ttu-id="f9240-103">уаддк (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="f9240-103">uaddc (sm5 - asm)</span></span>

<span data-ttu-id="f9240-104">Целое число без знака, добавленное с помощью макрокоманды.</span><span class="sxs-lookup"><span data-stu-id="f9240-104">Unsigned integer add with carry.</span></span>



| <span data-ttu-id="f9240-105">уаддк dest0 \[ . Mask \] , dest1 \[ . Mask \] , src0 \[ . свиззле \] , src1 \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="f9240-105">uaddc dest0\[.mask\], dest1\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="f9240-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="f9240-106">Item</span></span>                                                               | <span data-ttu-id="f9240-107">Описание</span><span class="sxs-lookup"><span data-stu-id="f9240-107">Description</span></span>                                            |
|--------------------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="f9240-108"><span id="dest0"></span><span id="DEST0"></span>*dest0*</span><span class="sxs-lookup"><span data-stu-id="f9240-108"><span id="dest0"></span><span id="DEST0"></span>*dest0*</span></span><br/> | <span data-ttu-id="f9240-109">\[в \] поле Адрес результата.</span><span class="sxs-lookup"><span data-stu-id="f9240-109">\[in\] Address of the result.</span></span><br/>               |
| <span data-ttu-id="f9240-110"><span id="dest1"></span><span id="DEST1"></span>*dest1*</span><span class="sxs-lookup"><span data-stu-id="f9240-110"><span id="dest1"></span><span id="DEST1"></span>*dest1*</span></span><br/> | <span data-ttu-id="f9240-111">\[в \] 1, если создается.</span><span class="sxs-lookup"><span data-stu-id="f9240-111">\[in\] 1 if carry is produced.</span></span> <span data-ttu-id="f9240-112">В противном случае 0.</span><span class="sxs-lookup"><span data-stu-id="f9240-112">Otherwise 0.</span></span><br/> |
| <span data-ttu-id="f9240-113"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="f9240-113"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>    | <span data-ttu-id="f9240-114">\[в \] 32-разрядный операнд для добавления.</span><span class="sxs-lookup"><span data-stu-id="f9240-114">\[in\] 32-bit operand to be added.</span></span><br/>          |
| <span data-ttu-id="f9240-115"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="f9240-115"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>    | <span data-ttu-id="f9240-116">\[в \] 32-разрядный операнд для добавления.</span><span class="sxs-lookup"><span data-stu-id="f9240-116">\[in\] 32-bit operand to be added.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="f9240-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="f9240-117">Remarks</span></span>

<span data-ttu-id="f9240-118">*dest1* может иметь значение null, если не требуется выполнение.</span><span class="sxs-lookup"><span data-stu-id="f9240-118">*dest1* can be NULL if the carry is not needed.</span></span>

<span data-ttu-id="f9240-119">Используйте эту инструкцию для арифметических операций с высокой точностью.</span><span class="sxs-lookup"><span data-stu-id="f9240-119">Use this instruction for high precision arithmetic.</span></span>

<span data-ttu-id="f9240-120">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="f9240-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f9240-121">Вершина</span><span class="sxs-lookup"><span data-stu-id="f9240-121">Vertex</span></span> | <span data-ttu-id="f9240-122">Поверхности</span><span class="sxs-lookup"><span data-stu-id="f9240-122">Hull</span></span> | <span data-ttu-id="f9240-123">Домен</span><span class="sxs-lookup"><span data-stu-id="f9240-123">Domain</span></span> | <span data-ttu-id="f9240-124">Геометрия</span><span class="sxs-lookup"><span data-stu-id="f9240-124">Geometry</span></span> | <span data-ttu-id="f9240-125">Пиксель</span><span class="sxs-lookup"><span data-stu-id="f9240-125">Pixel</span></span> | <span data-ttu-id="f9240-126">Вычисления</span><span class="sxs-lookup"><span data-stu-id="f9240-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f9240-127">X</span><span class="sxs-lookup"><span data-stu-id="f9240-127">X</span></span>      | <span data-ttu-id="f9240-128">X</span><span class="sxs-lookup"><span data-stu-id="f9240-128">X</span></span>    | <span data-ttu-id="f9240-129">X</span><span class="sxs-lookup"><span data-stu-id="f9240-129">X</span></span>      | <span data-ttu-id="f9240-130">X</span><span class="sxs-lookup"><span data-stu-id="f9240-130">X</span></span>        | <span data-ttu-id="f9240-131">X</span><span class="sxs-lookup"><span data-stu-id="f9240-131">X</span></span>     | <span data-ttu-id="f9240-132">X</span><span class="sxs-lookup"><span data-stu-id="f9240-132">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f9240-133">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="f9240-133">Minimum Shader Model</span></span>

<span data-ttu-id="f9240-134">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="f9240-134">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="f9240-135">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="f9240-135">Shader Model</span></span>                                              | <span data-ttu-id="f9240-136">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="f9240-136">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f9240-137">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="f9240-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f9240-138">да</span><span class="sxs-lookup"><span data-stu-id="f9240-138">yes</span></span>       |
| [<span data-ttu-id="f9240-139">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="f9240-139">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f9240-140">Нет</span><span class="sxs-lookup"><span data-stu-id="f9240-140">no</span></span>        |
| [<span data-ttu-id="f9240-141">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="f9240-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f9240-142">Нет</span><span class="sxs-lookup"><span data-stu-id="f9240-142">no</span></span>        |
| [<span data-ttu-id="f9240-143">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f9240-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f9240-144">Нет</span><span class="sxs-lookup"><span data-stu-id="f9240-144">no</span></span>        |
| [<span data-ttu-id="f9240-145">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f9240-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f9240-146">Нет</span><span class="sxs-lookup"><span data-stu-id="f9240-146">no</span></span>        |
| [<span data-ttu-id="f9240-147">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f9240-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f9240-148">Нет</span><span class="sxs-lookup"><span data-stu-id="f9240-148">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f9240-149">См. также</span><span class="sxs-lookup"><span data-stu-id="f9240-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9240-150">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f9240-150">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





