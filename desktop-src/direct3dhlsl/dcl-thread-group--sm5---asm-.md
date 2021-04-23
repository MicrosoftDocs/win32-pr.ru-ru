---
title: dcl_thread_group (SM5-ASM)
description: Объявить размер группы потоков.
ms.assetid: CB8192C4-100D-49B6-94E7-6CD3AEC28149
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8141c80e82f1dfd1ae5a4d360d04fac32ba5221
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104069372"
---
# <a name="dcl_thread_group-sm5---asm"></a><span data-ttu-id="c4f9e-103">\_группа потоков дкл \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="c4f9e-103">dcl\_thread\_group (sm5 - asm)</span></span>

<span data-ttu-id="c4f9e-104">Объявить размер группы потоков.</span><span class="sxs-lookup"><span data-stu-id="c4f9e-104">Declare thread group size.</span></span>



| <span data-ttu-id="c4f9e-105">\_группа потоков дкл \_ x, y, z</span><span class="sxs-lookup"><span data-stu-id="c4f9e-105">dcl\_thread\_group x, y, z</span></span> |
|----------------------------|



 



| <span data-ttu-id="c4f9e-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="c4f9e-106">Item</span></span>                                                   | <span data-ttu-id="c4f9e-107">Описание</span><span class="sxs-lookup"><span data-stu-id="c4f9e-107">Description</span></span>                                                        |
|--------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="c4f9e-108"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="c4f9e-108"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="c4f9e-109">\[в \] усигнед 32-разрядное целое число.</span><span class="sxs-lookup"><span data-stu-id="c4f9e-109">\[in\] An usigned 32-bit integer.</span></span> <span data-ttu-id="c4f9e-110">1 <= x <= 1024</span><span class="sxs-lookup"><span data-stu-id="c4f9e-110">1 <= x <= 1024</span></span> <br/> |
| <span data-ttu-id="c4f9e-111"><span id="y"></span><span id="Y"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="c4f9e-111"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="c4f9e-112">\[в \] усигнед 32-разрядное целое число.</span><span class="sxs-lookup"><span data-stu-id="c4f9e-112">\[in\] An usigned 32-bit integer.</span></span> <span data-ttu-id="c4f9e-113">1 <= y <= 1024</span><span class="sxs-lookup"><span data-stu-id="c4f9e-113">1 <= y <= 1024</span></span><br/>  |
| <span data-ttu-id="c4f9e-114"><span id="z"></span><span id="Z"></span>*гармошкой*</span><span class="sxs-lookup"><span data-stu-id="c4f9e-114"><span id="z"></span><span id="Z"></span>*z*</span></span><br/> | <span data-ttu-id="c4f9e-115">\[в \] усигнед 32-разрядное целое число.</span><span class="sxs-lookup"><span data-stu-id="c4f9e-115">\[in\] An usigned 32-bit integer.</span></span> <span data-ttu-id="c4f9e-116">1 <= z <= 64</span><span class="sxs-lookup"><span data-stu-id="c4f9e-116">1 <= z <= 64</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="c4f9e-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="c4f9e-117">Remarks</span></span>

<span data-ttu-id="c4f9e-118">x \* y \* z <= 1024</span><span class="sxs-lookup"><span data-stu-id="c4f9e-118">x\*y\*z <= 1024</span></span>

<span data-ttu-id="c4f9e-119">Это объявление группы потоков должно появиться в шейдере вычислений один раз.</span><span class="sxs-lookup"><span data-stu-id="c4f9e-119">This thread group declaration must appear once in a compute shader.</span></span>

<span data-ttu-id="c4f9e-120">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="c4f9e-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c4f9e-121">Вершина</span><span class="sxs-lookup"><span data-stu-id="c4f9e-121">Vertex</span></span> | <span data-ttu-id="c4f9e-122">Поверхности</span><span class="sxs-lookup"><span data-stu-id="c4f9e-122">Hull</span></span> | <span data-ttu-id="c4f9e-123">Домен</span><span class="sxs-lookup"><span data-stu-id="c4f9e-123">Domain</span></span> | <span data-ttu-id="c4f9e-124">Геометрия</span><span class="sxs-lookup"><span data-stu-id="c4f9e-124">Geometry</span></span> | <span data-ttu-id="c4f9e-125">Пиксель</span><span class="sxs-lookup"><span data-stu-id="c4f9e-125">Pixel</span></span> | <span data-ttu-id="c4f9e-126">Вычисления</span><span class="sxs-lookup"><span data-stu-id="c4f9e-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="c4f9e-127">X</span><span class="sxs-lookup"><span data-stu-id="c4f9e-127">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c4f9e-128">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="c4f9e-128">Minimum Shader Model</span></span>

<span data-ttu-id="c4f9e-129">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="c4f9e-129">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="c4f9e-130">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="c4f9e-130">Shader Model</span></span>                                              | <span data-ttu-id="c4f9e-131">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="c4f9e-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c4f9e-132">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="c4f9e-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c4f9e-133">да</span><span class="sxs-lookup"><span data-stu-id="c4f9e-133">yes</span></span>       |
| [<span data-ttu-id="c4f9e-134">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="c4f9e-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c4f9e-135">Нет</span><span class="sxs-lookup"><span data-stu-id="c4f9e-135">no</span></span>        |
| [<span data-ttu-id="c4f9e-136">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="c4f9e-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c4f9e-137">Нет</span><span class="sxs-lookup"><span data-stu-id="c4f9e-137">no</span></span>        |
| [<span data-ttu-id="c4f9e-138">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c4f9e-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c4f9e-139">Нет</span><span class="sxs-lookup"><span data-stu-id="c4f9e-139">no</span></span>        |
| [<span data-ttu-id="c4f9e-140">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c4f9e-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c4f9e-141">Нет</span><span class="sxs-lookup"><span data-stu-id="c4f9e-141">no</span></span>        |
| [<span data-ttu-id="c4f9e-142">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c4f9e-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c4f9e-143">Нет</span><span class="sxs-lookup"><span data-stu-id="c4f9e-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c4f9e-144">См. также</span><span class="sxs-lookup"><span data-stu-id="c4f9e-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4f9e-145">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c4f9e-145">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





