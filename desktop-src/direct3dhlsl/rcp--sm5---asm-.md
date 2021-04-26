---
title: rcp (SM5-ASM)
description: Обратная на уровне компонентов.
ms.assetid: 499A14D6-36DB-4860-94D1-887D931E60D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa37499a981bae86333b071c2e96a37ccb8ac1a6
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998251"
---
# <a name="rcp-sm5---asm"></a><span data-ttu-id="e8e0e-103">rcp (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="e8e0e-103">rcp (sm5 - asm)</span></span>

<span data-ttu-id="e8e0e-104">Обратная на уровне компонентов.</span><span class="sxs-lookup"><span data-stu-id="e8e0e-104">Component-wise reciprocal.</span></span>



| <span data-ttu-id="e8e0e-105">rcp No \[ \_ \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="e8e0e-105">rcp\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="e8e0e-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="e8e0e-106">Item</span></span>                                                            | <span data-ttu-id="e8e0e-107">Описание</span><span class="sxs-lookup"><span data-stu-id="e8e0e-107">Description</span></span>                                                                         |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e8e0e-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="e8e0e-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="e8e0e-109">\[в \] адресе результатов</span><span class="sxs-lookup"><span data-stu-id="e8e0e-109">\[in\] The address of the results</span></span><br/> <span data-ttu-id="e8e0e-110">*конечный адрес*  =  **1.0 f**  /  *src0*.</span><span class="sxs-lookup"><span data-stu-id="e8e0e-110">*dest* = **1.0f** / *src0*.</span></span><br/> |
| <span data-ttu-id="e8e0e-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="e8e0e-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="e8e0e-112">\[\]число, которое нужно взять за обратную величину.</span><span class="sxs-lookup"><span data-stu-id="e8e0e-112">\[in\] The number to take the reciprocal of.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="e8e0e-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="e8e0e-113">Remarks</span></span>

<span data-ttu-id="e8e0e-114">Используйте эту инструкцию для обратной величины с низкой точностью, независимо от строгих требований деления.</span><span class="sxs-lookup"><span data-stu-id="e8e0e-114">Use this instruction for reduced precision reciprocal, independent of the strict requirements for divide.</span></span>

<span data-ttu-id="e8e0e-115">Максимальная относительная ошибка — 2-21.</span><span class="sxs-lookup"><span data-stu-id="e8e0e-115">Maximum relative error is 2-21.</span></span> <span data-ttu-id="e8e0e-116">(Погрешность ошибки только соответствует РСК)</span><span class="sxs-lookup"><span data-stu-id="e8e0e-116">(The error tolerance just matches rsq)</span></span>

<span data-ttu-id="e8e0e-117">В следующей таблице показаны результаты, полученные при выполнении инструкции с различными классами чисел.</span><span class="sxs-lookup"><span data-stu-id="e8e0e-117">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>



| <span data-ttu-id="e8e0e-118">*src*</span><span class="sxs-lookup"><span data-stu-id="e8e0e-118">*src*</span></span>  | <span data-ttu-id="e8e0e-119">**-INF**</span><span class="sxs-lookup"><span data-stu-id="e8e0e-119">**-inf**</span></span> | <span data-ttu-id="e8e0e-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="e8e0e-120">**-F**</span></span> | <span data-ttu-id="e8e0e-121">**— денорма**</span><span class="sxs-lookup"><span data-stu-id="e8e0e-121">**-denorm**</span></span> | <span data-ttu-id="e8e0e-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="e8e0e-122">**-0**</span></span> | <span data-ttu-id="e8e0e-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="e8e0e-123">**+0**</span></span> | <span data-ttu-id="e8e0e-124">**+ денорма**</span><span class="sxs-lookup"><span data-stu-id="e8e0e-124">**+denorm**</span></span> | <span data-ttu-id="e8e0e-125">**+ F**</span><span class="sxs-lookup"><span data-stu-id="e8e0e-125">**+F**</span></span> | <span data-ttu-id="e8e0e-126">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="e8e0e-126">**+inf**</span></span> | <span data-ttu-id="e8e0e-127">**Не число**</span><span class="sxs-lookup"><span data-stu-id="e8e0e-127">**NaN**</span></span> |
|--------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="e8e0e-128">*dest*</span><span class="sxs-lookup"><span data-stu-id="e8e0e-128">*dest*</span></span> | <span data-ttu-id="e8e0e-129">-0</span><span class="sxs-lookup"><span data-stu-id="e8e0e-129">-0</span></span>       | <span data-ttu-id="e8e0e-130">-F</span><span class="sxs-lookup"><span data-stu-id="e8e0e-130">-F</span></span>     | <span data-ttu-id="e8e0e-131">-inf</span><span class="sxs-lookup"><span data-stu-id="e8e0e-131">-inf</span></span>        | <span data-ttu-id="e8e0e-132">-inf</span><span class="sxs-lookup"><span data-stu-id="e8e0e-132">-inf</span></span>   | <span data-ttu-id="e8e0e-133">+inf</span><span class="sxs-lookup"><span data-stu-id="e8e0e-133">+inf</span></span>   | <span data-ttu-id="e8e0e-134">+inf</span><span class="sxs-lookup"><span data-stu-id="e8e0e-134">+inf</span></span>        | <span data-ttu-id="e8e0e-135">+ F</span><span class="sxs-lookup"><span data-stu-id="e8e0e-135">+F</span></span>     | <span data-ttu-id="e8e0e-136">+0</span><span class="sxs-lookup"><span data-stu-id="e8e0e-136">+0</span></span>       | <span data-ttu-id="e8e0e-137">Не число</span><span class="sxs-lookup"><span data-stu-id="e8e0e-137">NaN</span></span>     |



 

<span data-ttu-id="e8e0e-138">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="e8e0e-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e8e0e-139">Вершина</span><span class="sxs-lookup"><span data-stu-id="e8e0e-139">Vertex</span></span> | <span data-ttu-id="e8e0e-140">Поверхности</span><span class="sxs-lookup"><span data-stu-id="e8e0e-140">Hull</span></span> | <span data-ttu-id="e8e0e-141">Домен</span><span class="sxs-lookup"><span data-stu-id="e8e0e-141">Domain</span></span> | <span data-ttu-id="e8e0e-142">Геометрия</span><span class="sxs-lookup"><span data-stu-id="e8e0e-142">Geometry</span></span> | <span data-ttu-id="e8e0e-143">Пиксель</span><span class="sxs-lookup"><span data-stu-id="e8e0e-143">Pixel</span></span> | <span data-ttu-id="e8e0e-144">Службы вычислений</span><span class="sxs-lookup"><span data-stu-id="e8e0e-144">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e8e0e-145">X</span><span class="sxs-lookup"><span data-stu-id="e8e0e-145">X</span></span>      | <span data-ttu-id="e8e0e-146">X</span><span class="sxs-lookup"><span data-stu-id="e8e0e-146">X</span></span>    | <span data-ttu-id="e8e0e-147">X</span><span class="sxs-lookup"><span data-stu-id="e8e0e-147">X</span></span>      | <span data-ttu-id="e8e0e-148">X</span><span class="sxs-lookup"><span data-stu-id="e8e0e-148">X</span></span>        | <span data-ttu-id="e8e0e-149">X</span><span class="sxs-lookup"><span data-stu-id="e8e0e-149">X</span></span>     | <span data-ttu-id="e8e0e-150">X</span><span class="sxs-lookup"><span data-stu-id="e8e0e-150">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e8e0e-151">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="e8e0e-151">Minimum Shader Model</span></span>

<span data-ttu-id="e8e0e-152">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="e8e0e-152">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="e8e0e-153">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="e8e0e-153">Shader Model</span></span>                                              | <span data-ttu-id="e8e0e-154">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="e8e0e-154">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e8e0e-155">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="e8e0e-155">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e8e0e-156">да</span><span class="sxs-lookup"><span data-stu-id="e8e0e-156">yes</span></span>       |
| [<span data-ttu-id="e8e0e-157">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="e8e0e-157">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e8e0e-158">Нет</span><span class="sxs-lookup"><span data-stu-id="e8e0e-158">no</span></span>        |
| [<span data-ttu-id="e8e0e-159">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="e8e0e-159">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e8e0e-160">Нет</span><span class="sxs-lookup"><span data-stu-id="e8e0e-160">no</span></span>        |
| [<span data-ttu-id="e8e0e-161">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e8e0e-161">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e8e0e-162">Нет</span><span class="sxs-lookup"><span data-stu-id="e8e0e-162">no</span></span>        |
| [<span data-ttu-id="e8e0e-163">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e8e0e-163">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e8e0e-164">Нет</span><span class="sxs-lookup"><span data-stu-id="e8e0e-164">no</span></span>        |
| [<span data-ttu-id="e8e0e-165">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e8e0e-165">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e8e0e-166">Нет</span><span class="sxs-lookup"><span data-stu-id="e8e0e-166">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e8e0e-167">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="e8e0e-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8e0e-168">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e8e0e-168">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





