---
title: dcl_tgsm_raw (SM5-ASM)
description: Объявите ссылку на область общей памяти, доступную для группы потоков COMPUTE Shader s.
ms.assetid: 8EA6931C-5B13-431F-A886-04F8C73CD22D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd20d8a0d8d2309b9b895a5cb5439877bb10d31a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103785001"
---
# <a name="dcl_tgsm_raw-sm5---asm"></a><span data-ttu-id="8d86b-103">дкл \_ тгсм \_ RAW (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="8d86b-103">dcl\_tgsm\_raw (sm5 - asm)</span></span>

<span data-ttu-id="8d86b-104">Объявите ссылку на область общей памяти, доступную для группы потоков COMPUTE Shader s.</span><span class="sxs-lookup"><span data-stu-id="8d86b-104">Declare a reference to a region of shared memory space available to the compute shader s thread group.</span></span>



| <span data-ttu-id="8d86b-105">дкл \_ тгсм \_ RAW g \# , byteCount</span><span class="sxs-lookup"><span data-stu-id="8d86b-105">dcl\_tgsm\_raw g\#, byteCount</span></span> |
|-------------------------------|



 



| <span data-ttu-id="8d86b-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="8d86b-106">Item</span></span>                                                                                                       | <span data-ttu-id="8d86b-107">Описание</span><span class="sxs-lookup"><span data-stu-id="8d86b-107">Description</span></span>                                                                             |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d86b-108"><span id="g_"></span><span id="G_"></span>*модуле\#*</span><span class="sxs-lookup"><span data-stu-id="8d86b-108"><span id="g_"></span><span id="G_"></span>*g\#*</span></span><br/>                                                 | <span data-ttu-id="8d86b-109">\[в \] ссылке на блок типа *byteCount* для нетипизированной общей памяти.</span><span class="sxs-lookup"><span data-stu-id="8d86b-109">\[in\] A reference to a block of size *byteCount* of untyped shared memory.</span></span> <br/> |
| <span data-ttu-id="8d86b-110"><span id="byteCount"></span><span id="bytecount"></span><span id="BYTECOUNT"></span>*byteCount*</span><span class="sxs-lookup"><span data-stu-id="8d86b-110"><span id="byteCount"></span><span id="bytecount"></span><span id="BYTECOUNT"></span>*byteCount*</span></span><br/> | <span data-ttu-id="8d86b-111">\[в \] должно быть кратно 4.</span><span class="sxs-lookup"><span data-stu-id="8d86b-111">\[in\] Must be a multiple of 4.</span></span> <br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="8d86b-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="8d86b-112">Remarks</span></span>

<span data-ttu-id="8d86b-113">Общий объем хранилища для всех g \# должен быть <= объем общей памяти, доступной для каждой группы потоков, которая является 32 КБ.</span><span class="sxs-lookup"><span data-stu-id="8d86b-113">The total storage for all g\# must be <= the amount of shared memory available per thread group, which is 32kB.</span></span>

<span data-ttu-id="8d86b-114">В экстремальном случае можно объявить 8192 \# с общим числом g s, каждый с параметром *byteCount* 4.</span><span class="sxs-lookup"><span data-stu-id="8d86b-114">In an extreme case, you can declare 8192 total g\# s, each with a *byteCount* of 4.</span></span>

<span data-ttu-id="8d86b-115">В противоположной крайней части можно объявить один g \# с *byteCount* 32768.</span><span class="sxs-lookup"><span data-stu-id="8d86b-115">In the opposite extreme, you can declare a single g\# with a *byteCount* of 32768.</span></span>

> [!Note]  
> <span data-ttu-id="8d86b-116">CS \_ 4 \_ 0 и CS \_ 4 \_ 1 поддерживают [дкл \_ тгсм \_ Structured](dcl-tgsm-structured--sm5---asm-.md), но не **дкл \_ тгсм \_ RAW**.</span><span class="sxs-lookup"><span data-stu-id="8d86b-116">cs\_4\_0 and cs\_4\_1 supports [dcl\_tgsm\_structured](dcl-tgsm-structured--sm5---asm-.md), but not **dcl\_tgsm\_raw**.</span></span>

 

<span data-ttu-id="8d86b-117">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="8d86b-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="8d86b-118">Вершина</span><span class="sxs-lookup"><span data-stu-id="8d86b-118">Vertex</span></span> | <span data-ttu-id="8d86b-119">Поверхности</span><span class="sxs-lookup"><span data-stu-id="8d86b-119">Hull</span></span> | <span data-ttu-id="8d86b-120">Домен</span><span class="sxs-lookup"><span data-stu-id="8d86b-120">Domain</span></span> | <span data-ttu-id="8d86b-121">Геометрия</span><span class="sxs-lookup"><span data-stu-id="8d86b-121">Geometry</span></span> | <span data-ttu-id="8d86b-122">Пиксель</span><span class="sxs-lookup"><span data-stu-id="8d86b-122">Pixel</span></span> | <span data-ttu-id="8d86b-123">Вычисления</span><span class="sxs-lookup"><span data-stu-id="8d86b-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="8d86b-124">X</span><span class="sxs-lookup"><span data-stu-id="8d86b-124">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8d86b-125">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="8d86b-125">Minimum Shader Model</span></span>

<span data-ttu-id="8d86b-126">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="8d86b-126">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="8d86b-127">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="8d86b-127">Shader Model</span></span>                                              | <span data-ttu-id="8d86b-128">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="8d86b-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="8d86b-129">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="8d86b-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="8d86b-130">да</span><span class="sxs-lookup"><span data-stu-id="8d86b-130">yes</span></span>       |
| [<span data-ttu-id="8d86b-131">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="8d86b-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="8d86b-132">Нет</span><span class="sxs-lookup"><span data-stu-id="8d86b-132">no</span></span>        |
| [<span data-ttu-id="8d86b-133">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="8d86b-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8d86b-134">Нет</span><span class="sxs-lookup"><span data-stu-id="8d86b-134">no</span></span>        |
| [<span data-ttu-id="8d86b-135">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8d86b-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8d86b-136">Нет</span><span class="sxs-lookup"><span data-stu-id="8d86b-136">no</span></span>        |
| [<span data-ttu-id="8d86b-137">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8d86b-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8d86b-138">Нет</span><span class="sxs-lookup"><span data-stu-id="8d86b-138">no</span></span>        |
| [<span data-ttu-id="8d86b-139">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8d86b-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8d86b-140">Нет</span><span class="sxs-lookup"><span data-stu-id="8d86b-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="8d86b-141">См. также</span><span class="sxs-lookup"><span data-stu-id="8d86b-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d86b-142">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8d86b-142">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





