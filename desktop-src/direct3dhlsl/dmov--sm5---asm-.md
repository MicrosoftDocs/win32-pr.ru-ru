---
title: дмов (SM5-ASM)
description: Перемещение на уровне компонентов. | дмов (SM5-ASM)
ms.assetid: 05DBB9E2-10EC-4324-BB8F-1A9E315DE90C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23b7d9c5ca0da1671ddf30fb9746333617f7688a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104000286"
---
# <a name="dmov-sm5---asm"></a><span data-ttu-id="db199-104">дмов (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="db199-104">dmov (sm5 - asm)</span></span>

<span data-ttu-id="db199-105">Перемещение на уровне компонентов.</span><span class="sxs-lookup"><span data-stu-id="db199-105">Component-wise move.</span></span>



| <span data-ttu-id="db199-106">дмов \[ \_ \] \[ . Маска \] , \[ - \] src0 \[ \_ ABS \] \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="db199-106">dmov\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="db199-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="db199-107">Item</span></span>                                                            | <span data-ttu-id="db199-108">Описание</span><span class="sxs-lookup"><span data-stu-id="db199-108">Description</span></span>                                              |
|-----------------------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="db199-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="db199-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="db199-110">\[в \] месте назначения перемещения.</span><span class="sxs-lookup"><span data-stu-id="db199-110">\[in\] The move destination.</span></span> <span data-ttu-id="db199-111">*конечный адрес*  =  *src0*.</span><span class="sxs-lookup"><span data-stu-id="db199-111">*dest* = *src0*.</span></span><br/> |
| <span data-ttu-id="db199-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="db199-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="db199-113">\[в \] перемещаемых компонентах.</span><span class="sxs-lookup"><span data-stu-id="db199-113">\[in\] The components to be moved.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="db199-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="db199-114">Remarks</span></span>

<span data-ttu-id="db199-115">Модификаторы, отличные от свиззле, предполагают, что данные являются плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="db199-115">The modifiers, other than swizzle, assume the data is floating point.</span></span> <span data-ttu-id="db199-116">Отсутствие модификаторов перемещает данные без изменения битов.</span><span class="sxs-lookup"><span data-stu-id="db199-116">The absence of modifiers moves data without altering bits.</span></span>

<span data-ttu-id="db199-117">Допустимыми свиззлес для параметров источника являются. ксизв,. ксикси,. звкси,. звзв.</span><span class="sxs-lookup"><span data-stu-id="db199-117">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="db199-118">Следующие сопоставления *src* — это POST-свиззле:</span><span class="sxs-lookup"><span data-stu-id="db199-118">The following *src* mappings are post-swizzle:</span></span>

-   <span data-ttu-id="db199-119">*src0* — это двойное vec2 в (x 32LSB, y 32MSB) и (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="db199-119">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="db199-120">*src1* — это двойное vec2 в (x 32LSB, y 32MSB) и (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="db199-120">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="db199-121">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="db199-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="db199-122">Вершина</span><span class="sxs-lookup"><span data-stu-id="db199-122">Vertex</span></span> | <span data-ttu-id="db199-123">Поверхности</span><span class="sxs-lookup"><span data-stu-id="db199-123">Hull</span></span> | <span data-ttu-id="db199-124">Домен</span><span class="sxs-lookup"><span data-stu-id="db199-124">Domain</span></span> | <span data-ttu-id="db199-125">Геометрия</span><span class="sxs-lookup"><span data-stu-id="db199-125">Geometry</span></span> | <span data-ttu-id="db199-126">Пиксель</span><span class="sxs-lookup"><span data-stu-id="db199-126">Pixel</span></span> | <span data-ttu-id="db199-127">Вычисления</span><span class="sxs-lookup"><span data-stu-id="db199-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="db199-128">X</span><span class="sxs-lookup"><span data-stu-id="db199-128">X</span></span>      | <span data-ttu-id="db199-129">X</span><span class="sxs-lookup"><span data-stu-id="db199-129">X</span></span>    | <span data-ttu-id="db199-130">X</span><span class="sxs-lookup"><span data-stu-id="db199-130">X</span></span>      | <span data-ttu-id="db199-131">X</span><span class="sxs-lookup"><span data-stu-id="db199-131">X</span></span>        | <span data-ttu-id="db199-132">X</span><span class="sxs-lookup"><span data-stu-id="db199-132">X</span></span>     | <span data-ttu-id="db199-133">X</span><span class="sxs-lookup"><span data-stu-id="db199-133">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="db199-134">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="db199-134">Minimum Shader Model</span></span>

<span data-ttu-id="db199-135">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="db199-135">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="db199-136">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="db199-136">Shader Model</span></span>                                              | <span data-ttu-id="db199-137">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="db199-137">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="db199-138">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="db199-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="db199-139">да</span><span class="sxs-lookup"><span data-stu-id="db199-139">yes</span></span>       |
| [<span data-ttu-id="db199-140">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="db199-140">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="db199-141">Нет</span><span class="sxs-lookup"><span data-stu-id="db199-141">no</span></span>        |
| [<span data-ttu-id="db199-142">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="db199-142">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="db199-143">Нет</span><span class="sxs-lookup"><span data-stu-id="db199-143">no</span></span>        |
| [<span data-ttu-id="db199-144">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="db199-144">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="db199-145">Нет</span><span class="sxs-lookup"><span data-stu-id="db199-145">no</span></span>        |
| [<span data-ttu-id="db199-146">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="db199-146">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="db199-147">Нет</span><span class="sxs-lookup"><span data-stu-id="db199-147">no</span></span>        |
| [<span data-ttu-id="db199-148">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="db199-148">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="db199-149">Нет</span><span class="sxs-lookup"><span data-stu-id="db199-149">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="db199-150">См. также</span><span class="sxs-lookup"><span data-stu-id="db199-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db199-151">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="db199-151">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





