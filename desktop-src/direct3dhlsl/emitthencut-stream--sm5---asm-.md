---
title: emitThenCut_stream (SM5-ASM)
description: Эквивалентно команде Emit, за которой следует команда Cut. | emitThenCut_stream (SM5-ASM)
ms.assetid: E9D84647-E29B-4E31-9E95-9F7A173293D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae3129f2a3fb50664a5dbf070c7a1dae9bf5d6e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986265"
---
# <a name="emitthencut_stream-sm5---asm"></a><span data-ttu-id="7756f-104">\_поток емитсенкут (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="7756f-104">emitThenCut\_stream (sm5 - asm)</span></span>

<span data-ttu-id="7756f-105">Эквивалентно команде [Emit](emit--sm4---asm-.md) , за которой следует команда [Cut](cut--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="7756f-105">Equivalent to an [emit](emit--sm4---asm-.md) command followed by a [cut](cut--sm4---asm-.md) command.</span></span>



| <span data-ttu-id="7756f-106">Емитсенкут \_ Stream стреаминдекс</span><span class="sxs-lookup"><span data-stu-id="7756f-106">emitThenCut\_stream streamIndex</span></span> |
|---------------------------------|



 



| <span data-ttu-id="7756f-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="7756f-107">Item</span></span>                                                                                                               | <span data-ttu-id="7756f-108">Описание</span><span class="sxs-lookup"><span data-stu-id="7756f-108">Description</span></span>                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="7756f-109"><span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*стреаминдекс*</span><span class="sxs-lookup"><span data-stu-id="7756f-109"><span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*</span></span><br/> | <span data-ttu-id="7756f-110">\[в \] индексе потока.</span><span class="sxs-lookup"><span data-stu-id="7756f-110">\[in\] The stream index.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7756f-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="7756f-111">Remarks</span></span>

<span data-ttu-id="7756f-112">Эта операция полезна, когда вы узнаете о размещении последней вершины в топологии.</span><span class="sxs-lookup"><span data-stu-id="7756f-112">This operation is useful when knowingly outputting the last vertex in a topology.</span></span>

<span data-ttu-id="7756f-113">Если потоки не объявлены, необходимо использовать [емитсенкут](emitthencut--sm4---asm-.md) вместо **\_ потока емитсенкут**.</span><span class="sxs-lookup"><span data-stu-id="7756f-113">If streams have not been declared, then you must use [emitThenCut](emitthencut--sm4---asm-.md) instead of **emitThenCut\_stream**.</span></span>

<span data-ttu-id="7756f-114">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="7756f-114">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="7756f-115">Вершина</span><span class="sxs-lookup"><span data-stu-id="7756f-115">Vertex</span></span> | <span data-ttu-id="7756f-116">Поверхности</span><span class="sxs-lookup"><span data-stu-id="7756f-116">Hull</span></span> | <span data-ttu-id="7756f-117">Домен</span><span class="sxs-lookup"><span data-stu-id="7756f-117">Domain</span></span> | <span data-ttu-id="7756f-118">Геометрия</span><span class="sxs-lookup"><span data-stu-id="7756f-118">Geometry</span></span> | <span data-ttu-id="7756f-119">Пиксель</span><span class="sxs-lookup"><span data-stu-id="7756f-119">Pixel</span></span> | <span data-ttu-id="7756f-120">Вычисления</span><span class="sxs-lookup"><span data-stu-id="7756f-120">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        | <span data-ttu-id="7756f-121">X</span><span class="sxs-lookup"><span data-stu-id="7756f-121">X</span></span>        |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7756f-122">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="7756f-122">Minimum Shader Model</span></span>

<span data-ttu-id="7756f-123">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="7756f-123">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="7756f-124">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="7756f-124">Shader Model</span></span>                                              | <span data-ttu-id="7756f-125">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="7756f-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="7756f-126">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="7756f-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="7756f-127">да</span><span class="sxs-lookup"><span data-stu-id="7756f-127">yes</span></span>       |
| [<span data-ttu-id="7756f-128">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="7756f-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="7756f-129">Нет</span><span class="sxs-lookup"><span data-stu-id="7756f-129">no</span></span>        |
| [<span data-ttu-id="7756f-130">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="7756f-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="7756f-131">Нет</span><span class="sxs-lookup"><span data-stu-id="7756f-131">no</span></span>        |
| [<span data-ttu-id="7756f-132">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7756f-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="7756f-133">Нет</span><span class="sxs-lookup"><span data-stu-id="7756f-133">no</span></span>        |
| [<span data-ttu-id="7756f-134">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7756f-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="7756f-135">Нет</span><span class="sxs-lookup"><span data-stu-id="7756f-135">no</span></span>        |
| [<span data-ttu-id="7756f-136">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7756f-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="7756f-137">Нет</span><span class="sxs-lookup"><span data-stu-id="7756f-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="7756f-138">См. также</span><span class="sxs-lookup"><span data-stu-id="7756f-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7756f-139">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7756f-139">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





