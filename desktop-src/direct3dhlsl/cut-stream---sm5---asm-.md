---
title: cut_stream (SM5-ASM)
description: Инструкция шейдера геометрии, которая завершает текущую топологию примитива в указанном потоке, если в нее были переданы вершины, и запускает новую топологию типа, объявленного шейдером геометрии в этом потоке.
ms.assetid: CEFDD13B-34FD-4E9C-94A0-CB8879A7DBDE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4650628d7f6b66130568f885e008a5163a9ee44f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412149"
---
# <a name="cut_stream-sm5---asm"></a><span data-ttu-id="e92b6-103">вырезать \_ поток (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="e92b6-103">cut\_stream (sm5 - asm)</span></span>

<span data-ttu-id="e92b6-104">Инструкция шейдера геометрии, которая завершает текущую топологию примитива в указанном потоке, если в нее были переданы вершины, и запускает новую топологию типа, объявленного шейдером геометрии в этом потоке.</span><span class="sxs-lookup"><span data-stu-id="e92b6-104">The geometry shader instruction that completes the current primitive topology at the specified stream, if any vertices have been emitted to it, and starts a new topology of the type declared by the geometry shader at that stream.</span></span>



| <span data-ttu-id="e92b6-105">вырезать \_ поток стреаминдекс</span><span class="sxs-lookup"><span data-stu-id="e92b6-105">cut\_stream streamIndex</span></span> |
|-------------------------|



 



| <span data-ttu-id="e92b6-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="e92b6-106">Item</span></span>                                                                                                               | <span data-ttu-id="e92b6-107">Описание</span><span class="sxs-lookup"><span data-stu-id="e92b6-107">Description</span></span>                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="e92b6-108"><span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*стреаминдекс*</span><span class="sxs-lookup"><span data-stu-id="e92b6-108"><span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*</span></span><br/> | <span data-ttu-id="e92b6-109">\[в \] индексе потока.</span><span class="sxs-lookup"><span data-stu-id="e92b6-109">\[in\] The stream index.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e92b6-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="e92b6-110">Remarks</span></span>

<span data-ttu-id="e92b6-111">При выполнении этой инструкции все ранее выпущенные топологии по вызову шейдера Geometry завершаются.</span><span class="sxs-lookup"><span data-stu-id="e92b6-111">When this instruction is executed, any previously emitted topology by the geometry shader invocation is completed.</span></span> <span data-ttu-id="e92b6-112">Если для предыдущей простой топологии не хватает вершин, они отбрасываются.</span><span class="sxs-lookup"><span data-stu-id="e92b6-112">If there are not enough vertices emitted for the previous primitive topology, then they are discarded.</span></span> <span data-ttu-id="e92b6-113">Поскольку единственными доступными выходными топологиями шейдера Geometry являются поинтлист, линестрип и трианглестрип, нет ни одного из оставшихся вершин.</span><span class="sxs-lookup"><span data-stu-id="e92b6-113">Because the only available output topologies for the geometry shader are pointlist, linestrip and trianglestrip, there are never any leftover vertices.</span></span>

<span data-ttu-id="e92b6-114">*стреаминдекс* должно быть непосредственным значением \[ 0.. 3 \] для объявленного потока.</span><span class="sxs-lookup"><span data-stu-id="e92b6-114">*streamIndex* must be an immediate value \[0..3\] for a declared stream.</span></span>

<span data-ttu-id="e92b6-115">После завершения предыдущей топологии, если таковая имеется, эта инструкция приводит к началу новой топологии с использованием топологии, объявленной в качестве выходных данных для шейдера Geometry.</span><span class="sxs-lookup"><span data-stu-id="e92b6-115">After the previous topology, if any, is completed, this instruction causes a new topology to begin, using the topology declared as the output for the geometry shader.</span></span>

### <a name="restrictions"></a><span data-ttu-id="e92b6-116">Ограничения</span><span class="sxs-lookup"><span data-stu-id="e92b6-116">Restrictions</span></span>

-   <span data-ttu-id="e92b6-117">Эта инструкция применяется только к шейдеру Geometry.</span><span class="sxs-lookup"><span data-stu-id="e92b6-117">This instruction applies to the geometry shader only.</span></span>
-   <span data-ttu-id="e92b6-118">**Вырезать \_ поток** может отображаться любое количество раз в шейдере Geometry, в том числе в элементе управления потоком.</span><span class="sxs-lookup"><span data-stu-id="e92b6-118">**cut\_stream** can appear any number of times in the geometry shader, including within flow control.</span></span>
-   <span data-ttu-id="e92b6-119">Если шейдер геометрии завершается и порождены вершины, топология, которую они создают, завершается, как если бы инструкция **Вырезать \_ поток** выполнялась в качестве последней инструкции.</span><span class="sxs-lookup"><span data-stu-id="e92b6-119">If the geometry shader ends and vertices have been emitted, the topology they are building is completed, as if a **cut\_stream** instruction was executed as the last instruction.</span></span>
-   <span data-ttu-id="e92b6-120">Если потоки не объявлены, необходимо использовать функцию [Cut](cut--sm4---asm-.md) вместо **Вырезать \_ поток**.</span><span class="sxs-lookup"><span data-stu-id="e92b6-120">If streams have not been declared, you must use [cut](cut--sm4---asm-.md) instead of **cut\_stream**.</span></span>

<span data-ttu-id="e92b6-121">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="e92b6-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e92b6-122">Вершина</span><span class="sxs-lookup"><span data-stu-id="e92b6-122">Vertex</span></span> | <span data-ttu-id="e92b6-123">Поверхности</span><span class="sxs-lookup"><span data-stu-id="e92b6-123">Hull</span></span> | <span data-ttu-id="e92b6-124">Домен</span><span class="sxs-lookup"><span data-stu-id="e92b6-124">Domain</span></span> | <span data-ttu-id="e92b6-125">Геометрия</span><span class="sxs-lookup"><span data-stu-id="e92b6-125">Geometry</span></span> | <span data-ttu-id="e92b6-126">Пиксель</span><span class="sxs-lookup"><span data-stu-id="e92b6-126">Pixel</span></span> | <span data-ttu-id="e92b6-127">Вычисления</span><span class="sxs-lookup"><span data-stu-id="e92b6-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        | <span data-ttu-id="e92b6-128">X</span><span class="sxs-lookup"><span data-stu-id="e92b6-128">X</span></span>        |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e92b6-129">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="e92b6-129">Minimum Shader Model</span></span>

<span data-ttu-id="e92b6-130">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="e92b6-130">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="e92b6-131">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="e92b6-131">Shader Model</span></span>                                              | <span data-ttu-id="e92b6-132">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="e92b6-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e92b6-133">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="e92b6-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e92b6-134">да</span><span class="sxs-lookup"><span data-stu-id="e92b6-134">yes</span></span>       |
| [<span data-ttu-id="e92b6-135">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="e92b6-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e92b6-136">Нет</span><span class="sxs-lookup"><span data-stu-id="e92b6-136">no</span></span>        |
| [<span data-ttu-id="e92b6-137">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="e92b6-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e92b6-138">Нет</span><span class="sxs-lookup"><span data-stu-id="e92b6-138">no</span></span>        |
| [<span data-ttu-id="e92b6-139">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e92b6-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e92b6-140">Нет</span><span class="sxs-lookup"><span data-stu-id="e92b6-140">no</span></span>        |
| [<span data-ttu-id="e92b6-141">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e92b6-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e92b6-142">Нет</span><span class="sxs-lookup"><span data-stu-id="e92b6-142">no</span></span>        |
| [<span data-ttu-id="e92b6-143">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e92b6-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e92b6-144">Нет</span><span class="sxs-lookup"><span data-stu-id="e92b6-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e92b6-145">См. также</span><span class="sxs-lookup"><span data-stu-id="e92b6-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e92b6-146">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e92b6-146">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





