---
title: rcp (SM5-ASM)
description: Обратная на уровне компонентов.
ms.assetid: 499A14D6-36DB-4860-94D1-887D931E60D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abbaa2ffc29a4c3373009d9dec1b895710186e67
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104532897"
---
# <a name="rcp-sm5---asm"></a><span data-ttu-id="298a9-103">rcp (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="298a9-103">rcp (sm5 - asm)</span></span>

<span data-ttu-id="298a9-104">Обратная на уровне компонентов.</span><span class="sxs-lookup"><span data-stu-id="298a9-104">Component-wise reciprocal.</span></span>



| <span data-ttu-id="298a9-105">rcp No \[ \_ \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="298a9-105">rcp\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="298a9-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="298a9-106">Item</span></span>                                                            | <span data-ttu-id="298a9-107">Описание</span><span class="sxs-lookup"><span data-stu-id="298a9-107">Description</span></span>                                                                         |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="298a9-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="298a9-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="298a9-109">\[в \] адресе результатов</span><span class="sxs-lookup"><span data-stu-id="298a9-109">\[in\] The address of the results</span></span><br/> <span data-ttu-id="298a9-110">*конечный адрес*  =  **1.0 f**  /  *src0*.</span><span class="sxs-lookup"><span data-stu-id="298a9-110">*dest* = **1.0f** / *src0*.</span></span><br/> |
| <span data-ttu-id="298a9-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="298a9-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="298a9-112">\[\]число, которое нужно взять за обратную величину.</span><span class="sxs-lookup"><span data-stu-id="298a9-112">\[in\] The number to take the reciprocal of.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="298a9-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="298a9-113">Remarks</span></span>

<span data-ttu-id="298a9-114">Используйте эту инструкцию для обратной величины с низкой точностью, независимо от строгих требований деления.</span><span class="sxs-lookup"><span data-stu-id="298a9-114">Use this instruction for reduced precision reciprocal, independent of the strict requirements for divide.</span></span>

<span data-ttu-id="298a9-115">Максимальная относительная ошибка — 2-21.</span><span class="sxs-lookup"><span data-stu-id="298a9-115">Maximum relative error is 2-21.</span></span> <span data-ttu-id="298a9-116">(Погрешность ошибки только соответствует РСК)</span><span class="sxs-lookup"><span data-stu-id="298a9-116">(The error tolerance just matches rsq)</span></span>

<span data-ttu-id="298a9-117">В следующей таблице показаны результаты, полученные при выполнении инструкции с различными классами чисел.</span><span class="sxs-lookup"><span data-stu-id="298a9-117">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>



|        |          |        |             |        |        |             |        |          |         |
|--------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="298a9-118">*src*</span><span class="sxs-lookup"><span data-stu-id="298a9-118">*src*</span></span>  | <span data-ttu-id="298a9-119">**-INF**</span><span class="sxs-lookup"><span data-stu-id="298a9-119">**-inf**</span></span> | <span data-ttu-id="298a9-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="298a9-120">**-F**</span></span> | <span data-ttu-id="298a9-121">**— денорма**</span><span class="sxs-lookup"><span data-stu-id="298a9-121">**-denorm**</span></span> | <span data-ttu-id="298a9-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="298a9-122">**-0**</span></span> | <span data-ttu-id="298a9-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="298a9-123">**+0**</span></span> | <span data-ttu-id="298a9-124">**+ денорма**</span><span class="sxs-lookup"><span data-stu-id="298a9-124">**+denorm**</span></span> | <span data-ttu-id="298a9-125">**+ F**</span><span class="sxs-lookup"><span data-stu-id="298a9-125">**+F**</span></span> | <span data-ttu-id="298a9-126">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="298a9-126">**+inf**</span></span> | <span data-ttu-id="298a9-127">**Не число**</span><span class="sxs-lookup"><span data-stu-id="298a9-127">**NaN**</span></span> |
| <span data-ttu-id="298a9-128">*dest*</span><span class="sxs-lookup"><span data-stu-id="298a9-128">*dest*</span></span> | <span data-ttu-id="298a9-129">-0</span><span class="sxs-lookup"><span data-stu-id="298a9-129">-0</span></span>       | <span data-ttu-id="298a9-130">-F</span><span class="sxs-lookup"><span data-stu-id="298a9-130">-F</span></span>     | <span data-ttu-id="298a9-131">-inf</span><span class="sxs-lookup"><span data-stu-id="298a9-131">-inf</span></span>        | <span data-ttu-id="298a9-132">-inf</span><span class="sxs-lookup"><span data-stu-id="298a9-132">-inf</span></span>   | <span data-ttu-id="298a9-133">+inf</span><span class="sxs-lookup"><span data-stu-id="298a9-133">+inf</span></span>   | <span data-ttu-id="298a9-134">+inf</span><span class="sxs-lookup"><span data-stu-id="298a9-134">+inf</span></span>        | <span data-ttu-id="298a9-135">+ F</span><span class="sxs-lookup"><span data-stu-id="298a9-135">+F</span></span>     | <span data-ttu-id="298a9-136">+0</span><span class="sxs-lookup"><span data-stu-id="298a9-136">+0</span></span>       | <span data-ttu-id="298a9-137">Не число</span><span class="sxs-lookup"><span data-stu-id="298a9-137">NaN</span></span>     |



 

<span data-ttu-id="298a9-138">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="298a9-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="298a9-139">Вершина</span><span class="sxs-lookup"><span data-stu-id="298a9-139">Vertex</span></span> | <span data-ttu-id="298a9-140">Поверхности</span><span class="sxs-lookup"><span data-stu-id="298a9-140">Hull</span></span> | <span data-ttu-id="298a9-141">Домен</span><span class="sxs-lookup"><span data-stu-id="298a9-141">Domain</span></span> | <span data-ttu-id="298a9-142">Геометрия</span><span class="sxs-lookup"><span data-stu-id="298a9-142">Geometry</span></span> | <span data-ttu-id="298a9-143">Пиксель</span><span class="sxs-lookup"><span data-stu-id="298a9-143">Pixel</span></span> | <span data-ttu-id="298a9-144">Вычисления</span><span class="sxs-lookup"><span data-stu-id="298a9-144">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="298a9-145">X</span><span class="sxs-lookup"><span data-stu-id="298a9-145">X</span></span>      | <span data-ttu-id="298a9-146">X</span><span class="sxs-lookup"><span data-stu-id="298a9-146">X</span></span>    | <span data-ttu-id="298a9-147">X</span><span class="sxs-lookup"><span data-stu-id="298a9-147">X</span></span>      | <span data-ttu-id="298a9-148">X</span><span class="sxs-lookup"><span data-stu-id="298a9-148">X</span></span>        | <span data-ttu-id="298a9-149">X</span><span class="sxs-lookup"><span data-stu-id="298a9-149">X</span></span>     | <span data-ttu-id="298a9-150">X</span><span class="sxs-lookup"><span data-stu-id="298a9-150">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="298a9-151">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="298a9-151">Minimum Shader Model</span></span>

<span data-ttu-id="298a9-152">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="298a9-152">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="298a9-153">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="298a9-153">Shader Model</span></span>                                              | <span data-ttu-id="298a9-154">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="298a9-154">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="298a9-155">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="298a9-155">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="298a9-156">да</span><span class="sxs-lookup"><span data-stu-id="298a9-156">yes</span></span>       |
| [<span data-ttu-id="298a9-157">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="298a9-157">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="298a9-158">Нет</span><span class="sxs-lookup"><span data-stu-id="298a9-158">no</span></span>        |
| [<span data-ttu-id="298a9-159">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="298a9-159">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="298a9-160">Нет</span><span class="sxs-lookup"><span data-stu-id="298a9-160">no</span></span>        |
| [<span data-ttu-id="298a9-161">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="298a9-161">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="298a9-162">Нет</span><span class="sxs-lookup"><span data-stu-id="298a9-162">no</span></span>        |
| [<span data-ttu-id="298a9-163">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="298a9-163">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="298a9-164">Нет</span><span class="sxs-lookup"><span data-stu-id="298a9-164">no</span></span>        |
| [<span data-ttu-id="298a9-165">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="298a9-165">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="298a9-166">Нет</span><span class="sxs-lookup"><span data-stu-id="298a9-166">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="298a9-167">См. также</span><span class="sxs-lookup"><span data-stu-id="298a9-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="298a9-168">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="298a9-168">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





