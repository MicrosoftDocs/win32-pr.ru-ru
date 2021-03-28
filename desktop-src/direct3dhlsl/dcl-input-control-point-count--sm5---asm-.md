---
title: dcl_input_control_point_count (SM5-ASM)
description: Объявите число точек управления входными данными шейдера поверхности в разделе объявления шейдера поверхности.
ms.assetid: 2E524BF0-3DD0-446A-8437-0CF17B348D83
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f0a674a05bfd66b4c1d94da73958dc68f00fe21
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412243"
---
# <a name="dcl_input_control_point_count-sm5---asm"></a><span data-ttu-id="8f34a-103">число контрольных \_ точек ввода дкл \_ \_ \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="8f34a-103">dcl\_input\_control\_point\_count (sm5 - asm)</span></span>

<span data-ttu-id="8f34a-104">Объявите число точек управления входными данными шейдера поверхности в разделе объявления шейдера поверхности.</span><span class="sxs-lookup"><span data-stu-id="8f34a-104">Declare the hull shader input control point count in the hull shader declaration section.</span></span>



| <span data-ttu-id="8f34a-105">\_ \_ число контрольных \_ точек ввода дкл \_ {1.. 32}</span><span class="sxs-lookup"><span data-stu-id="8f34a-105">dcl\_input\_control\_point\_count {1..32}</span></span> |
|-------------------------------------------|



 



| <span data-ttu-id="8f34a-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="8f34a-106">Item</span></span>                                                   | <span data-ttu-id="8f34a-107">Описание</span><span class="sxs-lookup"><span data-stu-id="8f34a-107">Description</span></span>                                      |
|--------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="8f34a-108"><span id="N"></span><span id="n"></span>*\N*</span><span class="sxs-lookup"><span data-stu-id="8f34a-108"><span id="N"></span><span id="n"></span>*N*</span></span><br/> | <span data-ttu-id="8f34a-109">\[во \] счетчике контрольных точек ввода.</span><span class="sxs-lookup"><span data-stu-id="8f34a-109">\[in\] The input control point count.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8f34a-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="8f34a-110">Remarks</span></span>

<span data-ttu-id="8f34a-111">Требуется по крайней мере одна контрольная точка ввода. оно может быть пустым, если оно не требуется.</span><span class="sxs-lookup"><span data-stu-id="8f34a-111">At least 1 input control point is required; it can be empty if it is not needed.</span></span>

<span data-ttu-id="8f34a-112">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="8f34a-112">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="8f34a-113">Вершина</span><span class="sxs-lookup"><span data-stu-id="8f34a-113">Vertex</span></span> | <span data-ttu-id="8f34a-114">Поверхности</span><span class="sxs-lookup"><span data-stu-id="8f34a-114">Hull</span></span> | <span data-ttu-id="8f34a-115">Домен</span><span class="sxs-lookup"><span data-stu-id="8f34a-115">Domain</span></span> | <span data-ttu-id="8f34a-116">Геометрия</span><span class="sxs-lookup"><span data-stu-id="8f34a-116">Geometry</span></span> | <span data-ttu-id="8f34a-117">Пиксель</span><span class="sxs-lookup"><span data-stu-id="8f34a-117">Pixel</span></span> | <span data-ttu-id="8f34a-118">Вычисления</span><span class="sxs-lookup"><span data-stu-id="8f34a-118">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="8f34a-119">X</span><span class="sxs-lookup"><span data-stu-id="8f34a-119">X</span></span>    |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8f34a-120">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="8f34a-120">Minimum Shader Model</span></span>

<span data-ttu-id="8f34a-121">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="8f34a-121">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="8f34a-122">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="8f34a-122">Shader Model</span></span>                                              | <span data-ttu-id="8f34a-123">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="8f34a-123">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="8f34a-124">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="8f34a-124">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="8f34a-125">да</span><span class="sxs-lookup"><span data-stu-id="8f34a-125">yes</span></span>       |
| [<span data-ttu-id="8f34a-126">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="8f34a-126">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="8f34a-127">Нет</span><span class="sxs-lookup"><span data-stu-id="8f34a-127">no</span></span>        |
| [<span data-ttu-id="8f34a-128">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="8f34a-128">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8f34a-129">Нет</span><span class="sxs-lookup"><span data-stu-id="8f34a-129">no</span></span>        |
| [<span data-ttu-id="8f34a-130">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8f34a-130">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8f34a-131">Нет</span><span class="sxs-lookup"><span data-stu-id="8f34a-131">no</span></span>        |
| [<span data-ttu-id="8f34a-132">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8f34a-132">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8f34a-133">Нет</span><span class="sxs-lookup"><span data-stu-id="8f34a-133">no</span></span>        |
| [<span data-ttu-id="8f34a-134">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8f34a-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8f34a-135">Нет</span><span class="sxs-lookup"><span data-stu-id="8f34a-135">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="8f34a-136">См. также</span><span class="sxs-lookup"><span data-stu-id="8f34a-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f34a-137">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8f34a-137">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





