---
title: dcl_output_control_point_count (SM5-ASM)
description: Объявляет число точек управления выходными данными шейдера поверхности.
ms.assetid: 51E8117F-1802-413B-9820-04D5CEBE2DB6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 147f8f7021252f07cdb6dd0f225555ff0f23d54b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104069384"
---
# <a name="dcl_output_control_point_count-sm5---asm"></a><span data-ttu-id="73634-103">\_ \_ число точек управления выходом дкл \_ \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="73634-103">dcl\_output\_control\_point\_count (sm5 - asm)</span></span>

<span data-ttu-id="73634-104">Объявляет число точек управления выходными данными шейдера поверхности.</span><span class="sxs-lookup"><span data-stu-id="73634-104">Declares the hull shader output control point count.</span></span>



| <span data-ttu-id="73634-105">\_ \_ число точек управления выходом дкл \_ \_ N</span><span class="sxs-lookup"><span data-stu-id="73634-105">dcl\_output\_control\_point\_count N</span></span> |
|--------------------------------------|



 



| <span data-ttu-id="73634-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="73634-106">Item</span></span>                                                   | <span data-ttu-id="73634-107">Описание</span><span class="sxs-lookup"><span data-stu-id="73634-107">Description</span></span>                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73634-108"><span id="N"></span><span id="n"></span>*\N*</span><span class="sxs-lookup"><span data-stu-id="73634-108"><span id="N"></span><span id="n"></span>*N*</span></span><br/> | <span data-ttu-id="73634-109">\[\]целочисленное значение от 0 до 32, указывающее число контрольных точек вывода.</span><span class="sxs-lookup"><span data-stu-id="73634-109">\[in\] An integer value from 0 to 32 that specifies the output control point count.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="73634-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="73634-110">Remarks</span></span>

<span data-ttu-id="73634-111">Шейдер поверхности может выводить 0 контрольные точки, если они не нужны.</span><span class="sxs-lookup"><span data-stu-id="73634-111">The hull shader can output 0 control points if they are not needed.</span></span>

<span data-ttu-id="73634-112">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="73634-112">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="73634-113">Вершина</span><span class="sxs-lookup"><span data-stu-id="73634-113">Vertex</span></span> | <span data-ttu-id="73634-114">Поверхности</span><span class="sxs-lookup"><span data-stu-id="73634-114">Hull</span></span>                 | <span data-ttu-id="73634-115">Домен</span><span class="sxs-lookup"><span data-stu-id="73634-115">Domain</span></span> | <span data-ttu-id="73634-116">Геометрия</span><span class="sxs-lookup"><span data-stu-id="73634-116">Geometry</span></span> | <span data-ttu-id="73634-117">Пиксель</span><span class="sxs-lookup"><span data-stu-id="73634-117">Pixel</span></span> | <span data-ttu-id="73634-118">Вычисления</span><span class="sxs-lookup"><span data-stu-id="73634-118">Compute</span></span> |
|--------|----------------------|--------|----------|-------|---------|
|        | <span data-ttu-id="73634-119">Раздел объявлений</span><span class="sxs-lookup"><span data-stu-id="73634-119">Declarations Section</span></span> |        |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="73634-120">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="73634-120">Minimum Shader Model</span></span>

<span data-ttu-id="73634-121">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="73634-121">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="73634-122">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="73634-122">Shader Model</span></span>                                              | <span data-ttu-id="73634-123">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="73634-123">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="73634-124">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="73634-124">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="73634-125">да</span><span class="sxs-lookup"><span data-stu-id="73634-125">yes</span></span>       |
| [<span data-ttu-id="73634-126">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="73634-126">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="73634-127">Нет</span><span class="sxs-lookup"><span data-stu-id="73634-127">no</span></span>        |
| [<span data-ttu-id="73634-128">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="73634-128">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="73634-129">Нет</span><span class="sxs-lookup"><span data-stu-id="73634-129">no</span></span>        |
| [<span data-ttu-id="73634-130">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="73634-130">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="73634-131">Нет</span><span class="sxs-lookup"><span data-stu-id="73634-131">no</span></span>        |
| [<span data-ttu-id="73634-132">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="73634-132">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="73634-133">Нет</span><span class="sxs-lookup"><span data-stu-id="73634-133">no</span></span>        |
| [<span data-ttu-id="73634-134">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="73634-134">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="73634-135">Нет</span><span class="sxs-lookup"><span data-stu-id="73634-135">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="73634-136">См. также</span><span class="sxs-lookup"><span data-stu-id="73634-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73634-137">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="73634-137">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





