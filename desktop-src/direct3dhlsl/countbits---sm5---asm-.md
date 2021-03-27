---
title: каунтбитс (SM5-ASM)
description: Подсчитывает количество битов, заданных в числе.
ms.assetid: ED75487F-46FF-45F5-BEAA-7A32BEFB0571
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55d46fe9c750790d65630a743dd9ddc347fea50e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103890008"
---
# <a name="countbits-sm5---asm"></a><span data-ttu-id="ff4bb-103">каунтбитс (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="ff4bb-103">countbits (sm5 - asm)</span></span>

<span data-ttu-id="ff4bb-104">Подсчитывает количество битов, заданных в числе.</span><span class="sxs-lookup"><span data-stu-id="ff4bb-104">Counts the number of bits set in a number.</span></span>



| <span data-ttu-id="ff4bb-105">каунтбитс dest \[ . Mask \] , src0 \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="ff4bb-105">countbits dest\[.mask\], src0\[.swizzle\]</span></span> |
|-------------------------------------------|



 



| <span data-ttu-id="ff4bb-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="ff4bb-106">Item</span></span>                                                            | <span data-ttu-id="ff4bb-107">Описание</span><span class="sxs-lookup"><span data-stu-id="ff4bb-107">Description</span></span>                                   |
|-----------------------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="ff4bb-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="ff4bb-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="ff4bb-109">\[в \] адресе результатов.</span><span class="sxs-lookup"><span data-stu-id="ff4bb-109">\[in\] The address of the results.</span></span><br/> |
| <span data-ttu-id="ff4bb-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="ff4bb-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="ff4bb-111">\[во \] входном 32-разрядном номере.</span><span class="sxs-lookup"><span data-stu-id="ff4bb-111">\[in\] The input 32-bit number.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="ff4bb-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="ff4bb-112">Remarks</span></span>

<span data-ttu-id="ff4bb-113">Эту инструкцию можно использовать для расчета процентного покрытия заполнения шейдером.</span><span class="sxs-lookup"><span data-stu-id="ff4bb-113">This instruction can be used to compute shader input coverage percentage.</span></span>

<span data-ttu-id="ff4bb-114">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="ff4bb-114">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ff4bb-115">Вершина</span><span class="sxs-lookup"><span data-stu-id="ff4bb-115">Vertex</span></span> | <span data-ttu-id="ff4bb-116">Поверхности</span><span class="sxs-lookup"><span data-stu-id="ff4bb-116">Hull</span></span> | <span data-ttu-id="ff4bb-117">Домен</span><span class="sxs-lookup"><span data-stu-id="ff4bb-117">Domain</span></span> | <span data-ttu-id="ff4bb-118">Геометрия</span><span class="sxs-lookup"><span data-stu-id="ff4bb-118">Geometry</span></span> | <span data-ttu-id="ff4bb-119">Пиксель</span><span class="sxs-lookup"><span data-stu-id="ff4bb-119">Pixel</span></span> | <span data-ttu-id="ff4bb-120">Вычисления</span><span class="sxs-lookup"><span data-stu-id="ff4bb-120">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ff4bb-121">X</span><span class="sxs-lookup"><span data-stu-id="ff4bb-121">X</span></span>      | <span data-ttu-id="ff4bb-122">X</span><span class="sxs-lookup"><span data-stu-id="ff4bb-122">X</span></span>    | <span data-ttu-id="ff4bb-123">X</span><span class="sxs-lookup"><span data-stu-id="ff4bb-123">X</span></span>      | <span data-ttu-id="ff4bb-124">X</span><span class="sxs-lookup"><span data-stu-id="ff4bb-124">X</span></span>        | <span data-ttu-id="ff4bb-125">X</span><span class="sxs-lookup"><span data-stu-id="ff4bb-125">X</span></span>     | <span data-ttu-id="ff4bb-126">X</span><span class="sxs-lookup"><span data-stu-id="ff4bb-126">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ff4bb-127">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ff4bb-127">Minimum Shader Model</span></span>

<span data-ttu-id="ff4bb-128">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="ff4bb-128">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="ff4bb-129">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ff4bb-129">Shader Model</span></span>                                              | <span data-ttu-id="ff4bb-130">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="ff4bb-130">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ff4bb-131">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="ff4bb-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ff4bb-132">да</span><span class="sxs-lookup"><span data-stu-id="ff4bb-132">yes</span></span>       |
| [<span data-ttu-id="ff4bb-133">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="ff4bb-133">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ff4bb-134">Нет</span><span class="sxs-lookup"><span data-stu-id="ff4bb-134">no</span></span>        |
| [<span data-ttu-id="ff4bb-135">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="ff4bb-135">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ff4bb-136">Нет</span><span class="sxs-lookup"><span data-stu-id="ff4bb-136">no</span></span>        |
| [<span data-ttu-id="ff4bb-137">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ff4bb-137">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ff4bb-138">Нет</span><span class="sxs-lookup"><span data-stu-id="ff4bb-138">no</span></span>        |
| [<span data-ttu-id="ff4bb-139">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ff4bb-139">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ff4bb-140">Нет</span><span class="sxs-lookup"><span data-stu-id="ff4bb-140">no</span></span>        |
| [<span data-ttu-id="ff4bb-141">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ff4bb-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ff4bb-142">Нет</span><span class="sxs-lookup"><span data-stu-id="ff4bb-142">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ff4bb-143">См. также</span><span class="sxs-lookup"><span data-stu-id="ff4bb-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff4bb-144">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ff4bb-144">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





