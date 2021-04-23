---
title: dcl_tgsm_structured (SM5-ASM)
description: Объявите ссылку на область общей памяти, доступную для группы потоков COMPUTE Shader s. Память просматривается как массив структур.
ms.assetid: C42CD506-58EB-4740-8403-3F9BF29F0CAE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a639d31c4449a0dfeb152c06b35cfb86c5cc30a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996887"
---
# <a name="dcl_tgsm_structured-sm5---asm"></a><span data-ttu-id="8cf92-104">дкл \_ тгсм \_ Structured (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="8cf92-104">dcl\_tgsm\_structured (sm5 - asm)</span></span>

<span data-ttu-id="8cf92-105">Объявите ссылку на область общей памяти, доступную для группы потоков COMPUTE Shader s.</span><span class="sxs-lookup"><span data-stu-id="8cf92-105">Declare a reference to a region of shared memory space available to the compute shader s thread group.</span></span> <span data-ttu-id="8cf92-106">Память просматривается как массив структур.</span><span class="sxs-lookup"><span data-stu-id="8cf92-106">The memory is viewed as an array of structures.</span></span>



| <span data-ttu-id="8cf92-107">дкл \_ тгсм \_ Structured g \# , структбитестриде, структкаунт</span><span class="sxs-lookup"><span data-stu-id="8cf92-107">dcl\_tgsm\_structured g\#, structByteStride, structCount</span></span> |
|----------------------------------------------------------|



 



| <span data-ttu-id="8cf92-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="8cf92-108">Item</span></span>                                                                                                                                   | <span data-ttu-id="8cf92-109">Описание</span><span class="sxs-lookup"><span data-stu-id="8cf92-109">Description</span></span>                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cf92-110"><span id="g_"></span><span id="G_"></span>*модуле\#*</span><span class="sxs-lookup"><span data-stu-id="8cf92-110"><span id="g_"></span><span id="G_"></span>*g\#*</span></span><br/>                                                                             | <span data-ttu-id="8cf92-111">\[в \] ссылке на блок общей памяти размером *структбитестриде* \* *структкаунт* байт.</span><span class="sxs-lookup"><span data-stu-id="8cf92-111">\[in\] A reference to a block of shared memory of size *structByteStride* \* *structCount* bytes.</span></span> <br/> |
| <span data-ttu-id="8cf92-112"><span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*структбитестриде*</span><span class="sxs-lookup"><span data-stu-id="8cf92-112"><span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*</span></span><br/> | <span data-ttu-id="8cf92-113">\[в \] структуре STRIDE.</span><span class="sxs-lookup"><span data-stu-id="8cf92-113">\[in\] The structure stride.</span></span> <span data-ttu-id="8cf92-114">Это значение равно uint в байтах и должно быть кратно 4.</span><span class="sxs-lookup"><span data-stu-id="8cf92-114">This value is a uint in bytes and must be a multiple of 4.</span></span> <br/>           |
| <span data-ttu-id="8cf92-115"><span id="structCount"></span><span id="structcount"></span><span id="STRUCTCOUNT"></span>*структкаунт*</span><span class="sxs-lookup"><span data-stu-id="8cf92-115"><span id="structCount"></span><span id="structcount"></span><span id="STRUCTCOUNT"></span>*structCount*</span></span><br/>                     | <span data-ttu-id="8cf92-116">\[в \] количестве структур.</span><span class="sxs-lookup"><span data-stu-id="8cf92-116">\[in\] The number of structures.</span></span><br/>                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="8cf92-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="8cf92-117">Remarks</span></span>

<span data-ttu-id="8cf92-118">Общий объем хранилища для всех g \# должен быть <= объем общей памяти, доступной для каждой группы потоков, которая представляет собой 32 КБ или 8192 32-разрядные скаляры.</span><span class="sxs-lookup"><span data-stu-id="8cf92-118">The total storage for all g\# must be <= the amount of shared memory available per thread group, which is 32kB, or 8192 32-bit scalars.</span></span>

<span data-ttu-id="8cf92-119">В экстремальном случае можно объявить 8192 с суммой g \# s, если каждый из них имеет *структбитестриде* 4 и *структкаунт* 1.</span><span class="sxs-lookup"><span data-stu-id="8cf92-119">In an extreme case, you can declare 8192 total g\# s, if each has a *structByteStride* of 4 and a *structCount* of 1.</span></span>

<span data-ttu-id="8cf92-120">В противоположной крайней части можно объявить одну g \# с шагом структуры 32 КБ и числом структур, равным 1.</span><span class="sxs-lookup"><span data-stu-id="8cf92-120">In the opposite extreme, you can declare a single g\# with a structure stride of 32kB and a structure count of 1.</span></span>

<span data-ttu-id="8cf92-121">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="8cf92-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="8cf92-122">Вершина</span><span class="sxs-lookup"><span data-stu-id="8cf92-122">Vertex</span></span> | <span data-ttu-id="8cf92-123">Поверхности</span><span class="sxs-lookup"><span data-stu-id="8cf92-123">Hull</span></span> | <span data-ttu-id="8cf92-124">Домен</span><span class="sxs-lookup"><span data-stu-id="8cf92-124">Domain</span></span> | <span data-ttu-id="8cf92-125">Геометрия</span><span class="sxs-lookup"><span data-stu-id="8cf92-125">Geometry</span></span> | <span data-ttu-id="8cf92-126">Пиксель</span><span class="sxs-lookup"><span data-stu-id="8cf92-126">Pixel</span></span> | <span data-ttu-id="8cf92-127">Вычисления</span><span class="sxs-lookup"><span data-stu-id="8cf92-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="8cf92-128">X</span><span class="sxs-lookup"><span data-stu-id="8cf92-128">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8cf92-129">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="8cf92-129">Minimum Shader Model</span></span>

<span data-ttu-id="8cf92-130">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="8cf92-130">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="8cf92-131">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="8cf92-131">Shader Model</span></span>                                              | <span data-ttu-id="8cf92-132">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="8cf92-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="8cf92-133">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="8cf92-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="8cf92-134">да</span><span class="sxs-lookup"><span data-stu-id="8cf92-134">yes</span></span>       |
| [<span data-ttu-id="8cf92-135">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="8cf92-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="8cf92-136">Нет</span><span class="sxs-lookup"><span data-stu-id="8cf92-136">no</span></span>        |
| [<span data-ttu-id="8cf92-137">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="8cf92-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8cf92-138">Нет</span><span class="sxs-lookup"><span data-stu-id="8cf92-138">no</span></span>        |
| [<span data-ttu-id="8cf92-139">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8cf92-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8cf92-140">Нет</span><span class="sxs-lookup"><span data-stu-id="8cf92-140">no</span></span>        |
| [<span data-ttu-id="8cf92-141">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8cf92-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8cf92-142">Нет</span><span class="sxs-lookup"><span data-stu-id="8cf92-142">no</span></span>        |
| [<span data-ttu-id="8cf92-143">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8cf92-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8cf92-144">Нет</span><span class="sxs-lookup"><span data-stu-id="8cf92-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="8cf92-145">См. также</span><span class="sxs-lookup"><span data-stu-id="8cf92-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8cf92-146">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8cf92-146">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





