---
title: emit_stream (SM5-ASM)
description: Выдача вершины в заданный поток.
ms.assetid: 5DBB0BEC-6EA4-4C04-A3D2-853E48260226
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f56c2582453d18120e3e95b27af9c7613728fa62
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412166"
---
# <a name="emit_stream-sm5---asm"></a><span data-ttu-id="1f6a3-103">Эмиссия \_ потока (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="1f6a3-103">emit\_stream (sm5 - asm)</span></span>

<span data-ttu-id="1f6a3-104">Выдача вершины в заданный поток.</span><span class="sxs-lookup"><span data-stu-id="1f6a3-104">Emit a vertex to a given stream.</span></span>



| <span data-ttu-id="1f6a3-105">Порождение \_ потока стреаминдекс</span><span class="sxs-lookup"><span data-stu-id="1f6a3-105">emit\_stream streamIndex</span></span> |
|--------------------------|



 



| <span data-ttu-id="1f6a3-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="1f6a3-106">Item</span></span>                                                                                                               | <span data-ttu-id="1f6a3-107">Описание</span><span class="sxs-lookup"><span data-stu-id="1f6a3-107">Description</span></span>                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="1f6a3-108"><span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*стреаминдекс*</span><span class="sxs-lookup"><span data-stu-id="1f6a3-108"><span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*</span></span><br/> | <span data-ttu-id="1f6a3-109">\[в \] индексе потока.</span><span class="sxs-lookup"><span data-stu-id="1f6a3-109">\[in\] The stream index.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1f6a3-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="1f6a3-110">Remarks</span></span>

<span data-ttu-id="1f6a3-111">Эта инструкция приводит к тому, что все объявленные \# регистры o для данного потока будут считываться из шейдера Geometry для создания вершины.</span><span class="sxs-lookup"><span data-stu-id="1f6a3-111">This instruction causes all declared o\# registers for the given stream to be read out of the geometry shader to generate a vertex.</span></span> <span data-ttu-id="1f6a3-112">Объект после выдачи, все данные во всех выходных регистрах для всех потоков становятся неинициализированными, а не только потоком, переданным в.</span><span class="sxs-lookup"><span data-stu-id="1f6a3-112">Afer the emit, all data in all output registers for all streams become uninitialized, not just the stream emitted to.</span></span>

<span data-ttu-id="1f6a3-113">*стреаминдекс* должно быть непосредственным значением \[ 0.. 3 \] для объявленного потока.</span><span class="sxs-lookup"><span data-stu-id="1f6a3-113">*streamIndex* must be an immediate value \[0..3\] for a declared stream.</span></span>

<span data-ttu-id="1f6a3-114">При выдаче нескольких вызовов **\_ потока выдачи** создаются примитивы.</span><span class="sxs-lookup"><span data-stu-id="1f6a3-114">As multiple **emit\_stream** calls are issued, primitives are generated.</span></span>

### <a name="restrictions"></a><span data-ttu-id="1f6a3-115">Ограничения</span><span class="sxs-lookup"><span data-stu-id="1f6a3-115">Restrictions</span></span>

-   <span data-ttu-id="1f6a3-116">**\_ поток выдачи** может отображаться любое количество раз в шейдере Geometry, в том числе в элементе управления потоком.</span><span class="sxs-lookup"><span data-stu-id="1f6a3-116">**emit\_stream** can appear any number of times in a geometry shader, including within flow control.</span></span>
-   <span data-ttu-id="1f6a3-117">Если потоки не объявлены, необходимо использовать [Emit](emit--sm4---asm-.md) вместо **\_ Stream выпуска**.</span><span class="sxs-lookup"><span data-stu-id="1f6a3-117">If streams have not been declared, then you must use [emit](emit--sm4---asm-.md) instead of **emit\_stream**.</span></span>

<span data-ttu-id="1f6a3-118">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="1f6a3-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="1f6a3-119">Вершина</span><span class="sxs-lookup"><span data-stu-id="1f6a3-119">Vertex</span></span> | <span data-ttu-id="1f6a3-120">Поверхности</span><span class="sxs-lookup"><span data-stu-id="1f6a3-120">Hull</span></span> | <span data-ttu-id="1f6a3-121">Домен</span><span class="sxs-lookup"><span data-stu-id="1f6a3-121">Domain</span></span> | <span data-ttu-id="1f6a3-122">Геометрия</span><span class="sxs-lookup"><span data-stu-id="1f6a3-122">Geometry</span></span> | <span data-ttu-id="1f6a3-123">Пиксель</span><span class="sxs-lookup"><span data-stu-id="1f6a3-123">Pixel</span></span> | <span data-ttu-id="1f6a3-124">Вычисления</span><span class="sxs-lookup"><span data-stu-id="1f6a3-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        | <span data-ttu-id="1f6a3-125">X</span><span class="sxs-lookup"><span data-stu-id="1f6a3-125">X</span></span>        |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1f6a3-126">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="1f6a3-126">Minimum Shader Model</span></span>

<span data-ttu-id="1f6a3-127">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="1f6a3-127">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="1f6a3-128">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="1f6a3-128">Shader Model</span></span>                                              | <span data-ttu-id="1f6a3-129">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="1f6a3-129">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1f6a3-130">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="1f6a3-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1f6a3-131">да</span><span class="sxs-lookup"><span data-stu-id="1f6a3-131">yes</span></span>       |
| [<span data-ttu-id="1f6a3-132">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="1f6a3-132">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1f6a3-133">Нет</span><span class="sxs-lookup"><span data-stu-id="1f6a3-133">no</span></span>        |
| [<span data-ttu-id="1f6a3-134">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="1f6a3-134">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1f6a3-135">Нет</span><span class="sxs-lookup"><span data-stu-id="1f6a3-135">no</span></span>        |
| [<span data-ttu-id="1f6a3-136">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1f6a3-136">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1f6a3-137">Нет</span><span class="sxs-lookup"><span data-stu-id="1f6a3-137">no</span></span>        |
| [<span data-ttu-id="1f6a3-138">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1f6a3-138">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1f6a3-139">Нет</span><span class="sxs-lookup"><span data-stu-id="1f6a3-139">no</span></span>        |
| [<span data-ttu-id="1f6a3-140">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1f6a3-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1f6a3-141">Нет</span><span class="sxs-lookup"><span data-stu-id="1f6a3-141">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1f6a3-142">См. также</span><span class="sxs-lookup"><span data-stu-id="1f6a3-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f6a3-143">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1f6a3-143">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





