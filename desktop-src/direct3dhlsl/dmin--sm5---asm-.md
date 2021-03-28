---
title: DMin (SM5-ASM)
description: Минимальная точность в компоненте с двойной точностью.
ms.assetid: 77331B4D-C4B5-49B2-BB6A-77BD5050B575
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e199b01c68acca6609123425438f309af872fb4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104069350"
---
# <a name="dmin-sm5---asm"></a><span data-ttu-id="bae74-103">DMin (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="bae74-103">dmin (sm5 - asm)</span></span>

<span data-ttu-id="bae74-104">Минимальная точность в компоненте с двойной точностью.</span><span class="sxs-lookup"><span data-stu-id="bae74-104">Component-wise double-precision minimum.</span></span>



| <span data-ttu-id="bae74-105">DMin \[ \_ \] — dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS. \] \[ свиззле \] , \[ - \] src1 \[ \_ ABS \] \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="bae74-105">dmin\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="bae74-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="bae74-106">Item</span></span>                                                            | <span data-ttu-id="bae74-107">Описание</span><span class="sxs-lookup"><span data-stu-id="bae74-107">Description</span></span>                                                                                                                                                                                                  |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bae74-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="bae74-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="bae74-109">\[в \] адресе результатов операции.</span><span class="sxs-lookup"><span data-stu-id="bae74-109">\[in\] The address of the results of the operation.</span></span><br/> <span data-ttu-id="bae74-110">*конечный адрес*  =  *src0*  <  *src1* ?</span><span class="sxs-lookup"><span data-stu-id="bae74-110">*dest* = *src0* < *src1* ?</span></span> <span data-ttu-id="bae74-111">*src0* : *src1*</span><span class="sxs-lookup"><span data-stu-id="bae74-111">*src0* : *src1*</span></span><br/> <span data-ttu-id="bae74-112">< используется вместо <=, так что если min (x, y) = x, то Max (x, y) = y.</span><span class="sxs-lookup"><span data-stu-id="bae74-112">< is used instead of <= so that if min(x,y) = x then max(x,y) = y.</span></span> <br/> |
| <span data-ttu-id="bae74-113"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="bae74-113"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="bae74-114">\[в \] компонентах, сравниваемых с *src1*.</span><span class="sxs-lookup"><span data-stu-id="bae74-114">\[in\] The components to compare with *src1*.</span></span><br/>                                                                                                                                                     |
| <span data-ttu-id="bae74-115"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="bae74-115"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="bae74-116">\[в \] компонентах, сравниваемых с *src0*.</span><span class="sxs-lookup"><span data-stu-id="bae74-116">\[in\] The components to compare with *src0*.</span></span><br/>                                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="bae74-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="bae74-117">Remarks</span></span>

<span data-ttu-id="bae74-118">NaN имеет особую обработку.</span><span class="sxs-lookup"><span data-stu-id="bae74-118">NaN has special handling.</span></span> <span data-ttu-id="bae74-119">Если один исходный операнд равен NaN, то возвращается другой исходный операнд.</span><span class="sxs-lookup"><span data-stu-id="bae74-119">If one source operand is NaN, then the other source operand is returned.</span></span> <span data-ttu-id="bae74-120">Выбранный вариант выполняется для каждого компонента.</span><span class="sxs-lookup"><span data-stu-id="bae74-120">The choice is made per-component.</span></span> <span data-ttu-id="bae74-121">Если оба значения равны NaN, возвращается любое представление NaN.</span><span class="sxs-lookup"><span data-stu-id="bae74-121">If both are NaN, any NaN representation is returned.</span></span>

<span data-ttu-id="bae74-122">Допустимыми свиззлес для параметров источника являются. ксизв,. ксикси,. звкси,. звзв.</span><span class="sxs-lookup"><span data-stu-id="bae74-122">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="bae74-123">Допустимые маски *приемников* : XY, ZW и. ксизв.</span><span class="sxs-lookup"><span data-stu-id="bae74-123">The valid *dest* masks are .xy, .zw, and .xyzw.</span></span> <span data-ttu-id="bae74-124">Следующие сопоставления *src* — это POST-свиззле:</span><span class="sxs-lookup"><span data-stu-id="bae74-124">The following *src* mappings are post-swizzle:</span></span>

-   <span data-ttu-id="bae74-125">*dest* — это двойное vec2 в (x 32LSB, y 32MSB) и (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="bae74-125">*dest* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="bae74-126">*src0* — это двойное vec2 в (x 32LSB, y 32MSB) и (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="bae74-126">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="bae74-127">*src1* — это двойное vec2 в (x 32LSB, y 32MSB) и (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="bae74-127">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="bae74-128">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="bae74-128">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="bae74-129">Вершина</span><span class="sxs-lookup"><span data-stu-id="bae74-129">Vertex</span></span> | <span data-ttu-id="bae74-130">Поверхности</span><span class="sxs-lookup"><span data-stu-id="bae74-130">Hull</span></span> | <span data-ttu-id="bae74-131">Домен</span><span class="sxs-lookup"><span data-stu-id="bae74-131">Domain</span></span> | <span data-ttu-id="bae74-132">Геометрия</span><span class="sxs-lookup"><span data-stu-id="bae74-132">Geometry</span></span> | <span data-ttu-id="bae74-133">Пиксель</span><span class="sxs-lookup"><span data-stu-id="bae74-133">Pixel</span></span> | <span data-ttu-id="bae74-134">Вычисления</span><span class="sxs-lookup"><span data-stu-id="bae74-134">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="bae74-135">X</span><span class="sxs-lookup"><span data-stu-id="bae74-135">X</span></span>      | <span data-ttu-id="bae74-136">X</span><span class="sxs-lookup"><span data-stu-id="bae74-136">X</span></span>    | <span data-ttu-id="bae74-137">X</span><span class="sxs-lookup"><span data-stu-id="bae74-137">X</span></span>      | <span data-ttu-id="bae74-138">X</span><span class="sxs-lookup"><span data-stu-id="bae74-138">X</span></span>        | <span data-ttu-id="bae74-139">X</span><span class="sxs-lookup"><span data-stu-id="bae74-139">X</span></span>     | <span data-ttu-id="bae74-140">X</span><span class="sxs-lookup"><span data-stu-id="bae74-140">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="bae74-141">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="bae74-141">Minimum Shader Model</span></span>

<span data-ttu-id="bae74-142">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="bae74-142">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="bae74-143">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="bae74-143">Shader Model</span></span>                                              | <span data-ttu-id="bae74-144">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="bae74-144">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="bae74-145">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="bae74-145">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="bae74-146">да</span><span class="sxs-lookup"><span data-stu-id="bae74-146">yes</span></span>       |
| [<span data-ttu-id="bae74-147">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="bae74-147">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="bae74-148">Нет</span><span class="sxs-lookup"><span data-stu-id="bae74-148">no</span></span>        |
| [<span data-ttu-id="bae74-149">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="bae74-149">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="bae74-150">Нет</span><span class="sxs-lookup"><span data-stu-id="bae74-150">no</span></span>        |
| [<span data-ttu-id="bae74-151">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bae74-151">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="bae74-152">Нет</span><span class="sxs-lookup"><span data-stu-id="bae74-152">no</span></span>        |
| [<span data-ttu-id="bae74-153">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bae74-153">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="bae74-154">Нет</span><span class="sxs-lookup"><span data-stu-id="bae74-154">no</span></span>        |
| [<span data-ttu-id="bae74-155">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bae74-155">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="bae74-156">Нет</span><span class="sxs-lookup"><span data-stu-id="bae74-156">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="bae74-157">См. также</span><span class="sxs-lookup"><span data-stu-id="bae74-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bae74-158">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bae74-158">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





