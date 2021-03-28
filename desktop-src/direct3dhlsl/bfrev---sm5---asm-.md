---
title: бфрев (SM5-ASM)
description: Обратный 32-разрядное число.
ms.assetid: 24F8209A-093E-4737-BF50-12F228024E9D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11bf0f07b6c66babf8e7f91108f86ba753420fc2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996927"
---
# <a name="bfrev-sm5---asm"></a><span data-ttu-id="8c4e8-103">бфрев (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="8c4e8-103">bfrev (sm5 - asm)</span></span>

<span data-ttu-id="8c4e8-104">Обратный 32-разрядное число.</span><span class="sxs-lookup"><span data-stu-id="8c4e8-104">Reverse a 32-bit number.</span></span>



| <span data-ttu-id="8c4e8-105">бфрев dest \[ . Mask \] , src0 \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="8c4e8-105">bfrev dest\[.mask\], src0\[.swizzle\]</span></span> |
|---------------------------------------|



 



| <span data-ttu-id="8c4e8-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="8c4e8-106">Item</span></span>                                                            | <span data-ttu-id="8c4e8-107">Описание</span><span class="sxs-lookup"><span data-stu-id="8c4e8-107">Description</span></span>                                                  |
|-----------------------------------------------------------------|--------------------------------------------------------------|
| <span data-ttu-id="8c4e8-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="8c4e8-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="8c4e8-109">\[в \] адресе для *src0* с обратным BITS.</span><span class="sxs-lookup"><span data-stu-id="8c4e8-109">\[in\] The address for *src0* with bits reversed.</span></span><br/> |
| <span data-ttu-id="8c4e8-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="8c4e8-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="8c4e8-111">\[в \] 32-разрядном числе для обращения.</span><span class="sxs-lookup"><span data-stu-id="8c4e8-111">\[in\] The 32-bit number to reverse.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="8c4e8-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="8c4e8-112">Remarks</span></span>

<span data-ttu-id="8c4e8-113">Например, при наличии 0x12345678 результат будет 0x1e6a2c48.</span><span class="sxs-lookup"><span data-stu-id="8c4e8-113">For example, given 0x12345678 the result would be 0x1e6a2c48.</span></span>

<span data-ttu-id="8c4e8-114">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="8c4e8-114">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="8c4e8-115">Вершина</span><span class="sxs-lookup"><span data-stu-id="8c4e8-115">Vertex</span></span> | <span data-ttu-id="8c4e8-116">Поверхности</span><span class="sxs-lookup"><span data-stu-id="8c4e8-116">Hull</span></span> | <span data-ttu-id="8c4e8-117">Домен</span><span class="sxs-lookup"><span data-stu-id="8c4e8-117">Domain</span></span> | <span data-ttu-id="8c4e8-118">Геометрия</span><span class="sxs-lookup"><span data-stu-id="8c4e8-118">Geometry</span></span> | <span data-ttu-id="8c4e8-119">Пиксель</span><span class="sxs-lookup"><span data-stu-id="8c4e8-119">Pixel</span></span> | <span data-ttu-id="8c4e8-120">Вычисления</span><span class="sxs-lookup"><span data-stu-id="8c4e8-120">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="8c4e8-121">X</span><span class="sxs-lookup"><span data-stu-id="8c4e8-121">X</span></span>      | <span data-ttu-id="8c4e8-122">X</span><span class="sxs-lookup"><span data-stu-id="8c4e8-122">X</span></span>    | <span data-ttu-id="8c4e8-123">X</span><span class="sxs-lookup"><span data-stu-id="8c4e8-123">X</span></span>      | <span data-ttu-id="8c4e8-124">X</span><span class="sxs-lookup"><span data-stu-id="8c4e8-124">X</span></span>        | <span data-ttu-id="8c4e8-125">X</span><span class="sxs-lookup"><span data-stu-id="8c4e8-125">X</span></span>     | <span data-ttu-id="8c4e8-126">X</span><span class="sxs-lookup"><span data-stu-id="8c4e8-126">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8c4e8-127">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="8c4e8-127">Minimum Shader Model</span></span>

<span data-ttu-id="8c4e8-128">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="8c4e8-128">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="8c4e8-129">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="8c4e8-129">Shader Model</span></span>                                              | <span data-ttu-id="8c4e8-130">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="8c4e8-130">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="8c4e8-131">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="8c4e8-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="8c4e8-132">да</span><span class="sxs-lookup"><span data-stu-id="8c4e8-132">yes</span></span>       |
| [<span data-ttu-id="8c4e8-133">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="8c4e8-133">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="8c4e8-134">Нет</span><span class="sxs-lookup"><span data-stu-id="8c4e8-134">no</span></span>        |
| [<span data-ttu-id="8c4e8-135">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="8c4e8-135">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8c4e8-136">Нет</span><span class="sxs-lookup"><span data-stu-id="8c4e8-136">no</span></span>        |
| [<span data-ttu-id="8c4e8-137">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8c4e8-137">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8c4e8-138">Нет</span><span class="sxs-lookup"><span data-stu-id="8c4e8-138">no</span></span>        |
| [<span data-ttu-id="8c4e8-139">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8c4e8-139">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8c4e8-140">Нет</span><span class="sxs-lookup"><span data-stu-id="8c4e8-140">no</span></span>        |
| [<span data-ttu-id="8c4e8-141">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8c4e8-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8c4e8-142">Нет</span><span class="sxs-lookup"><span data-stu-id="8c4e8-142">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="8c4e8-143">См. также</span><span class="sxs-lookup"><span data-stu-id="8c4e8-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c4e8-144">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8c4e8-144">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





