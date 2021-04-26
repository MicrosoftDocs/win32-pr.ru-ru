---
title: дркп (SM5-ASM)
description: Вычисление взаимной точности с двойной точностью.
ms.assetid: 499A14D6-36DB-4860-94D1-887D931E60D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 770159f5007b08f5482ba8b58634b44e7f3e6ef0
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998341"
---
# <a name="drcp-sm5---asm"></a><span data-ttu-id="df521-103">дркп (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="df521-103">drcp (sm5 - asm)</span></span>

<span data-ttu-id="df521-104">Вычисление взаимной точности с двойной точностью.</span><span class="sxs-lookup"><span data-stu-id="df521-104">Computes a component-wise double-precision reciprocal.</span></span>



| <span data-ttu-id="df521-105">rcp No \[ \_ \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="df521-105">rcp\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="df521-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="df521-106">Item</span></span>                                                            | <span data-ttu-id="df521-107">Описание</span><span class="sxs-lookup"><span data-stu-id="df521-107">Description</span></span>                                                                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df521-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="df521-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="df521-109">\[в \] адресе результатов</span><span class="sxs-lookup"><span data-stu-id="df521-109">\[in\] The address of the results</span></span><br/> <span data-ttu-id="df521-110">*конечный адрес*  =  **1,0**  /  *src0*.</span><span class="sxs-lookup"><span data-stu-id="df521-110">*dest* = **1.0** / *src0*.</span></span> <span data-ttu-id="df521-111">Значение результата должно быть точным до 1,0 ULP</span><span class="sxs-lookup"><span data-stu-id="df521-111">The result value must be accurate to 1.0 ULP</span></span><br/> |
| <span data-ttu-id="df521-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="df521-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="df521-113">\[\]число, которое нужно взять за обратную величину.</span><span class="sxs-lookup"><span data-stu-id="df521-113">\[in\] The number to take the reciprocal of.</span></span><br/>                                                                         |



 

## <a name="remarks"></a><span data-ttu-id="df521-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="df521-114">Remarks</span></span>

<span data-ttu-id="df521-115">Инструкция ДРКП создается компилятором HLSL только при явном вызове с помощью функции RCP (), если в качестве аргумента используется Double.</span><span class="sxs-lookup"><span data-stu-id="df521-115">The DRCP instruction is emitted by the HLSL compiler only when explicitly called via the rcp() intrinsic, when a double is used as the argument.</span></span> <span data-ttu-id="df521-116">Точность этой инструкции должна быть 1,0 ULP.</span><span class="sxs-lookup"><span data-stu-id="df521-116">The accuracy of this instruction is required to be 1.0 ULP.</span></span>

<span data-ttu-id="df521-117">Шейдеры, использующие эту инструкцию, будут помечены флагом построителя текстуры, который приведет к сбою привязки, если не выполняются все следующие условия.</span><span class="sxs-lookup"><span data-stu-id="df521-117">Shaders that use this instruction will be marked with a shader flag that will cause them to fail to bind unless all the following conditions are met.</span></span>

-   <span data-ttu-id="df521-118">Система поддерживает DirectX 11,1.</span><span class="sxs-lookup"><span data-stu-id="df521-118">The system supports DirectX 11.1.</span></span>
-   <span data-ttu-id="df521-119">Система включает драйвер WDDM 1,2.</span><span class="sxs-lookup"><span data-stu-id="df521-119">The system includes a WDDM 1.2 driver.</span></span>
-   <span data-ttu-id="df521-120">Драйвер сообщает о поддержке этой инструкции с помощью **\_ \_ параметров D3D11 Data Feature D3D11 \_ \_ . Для Екстендеддаублесшадеринструктионс** задано значение **true**.</span><span class="sxs-lookup"><span data-stu-id="df521-120">The driver reports support for this instruction via **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS.ExtendedDoublesShaderInstructions** set to **TRUE**.</span></span>

<span data-ttu-id="df521-121">В следующей таблице показаны результаты, полученные при выполнении инструкции с различными классами чисел, предполагая, что ни переполнение, ни потеря точности не происходит.</span><span class="sxs-lookup"><span data-stu-id="df521-121">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="df521-122">В этой таблице F означает ограничение по настоящему вещественному числу.</span><span class="sxs-lookup"><span data-stu-id="df521-122">In this table F means finite-real number.</span></span>



| <span data-ttu-id="df521-123">**src**-></span><span class="sxs-lookup"><span data-stu-id="df521-123">**src**-></span></span>  | <span data-ttu-id="df521-124">**-INF**</span><span class="sxs-lookup"><span data-stu-id="df521-124">**-inf**</span></span> | <span data-ttu-id="df521-125">**-F**</span><span class="sxs-lookup"><span data-stu-id="df521-125">**-F**</span></span> | <span data-ttu-id="df521-126">**-0**</span><span class="sxs-lookup"><span data-stu-id="df521-126">**-0**</span></span> | <span data-ttu-id="df521-127">**+0**</span><span class="sxs-lookup"><span data-stu-id="df521-127">**+0**</span></span> | <span data-ttu-id="df521-128">**+ F**</span><span class="sxs-lookup"><span data-stu-id="df521-128">**+F**</span></span> | <span data-ttu-id="df521-129">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="df521-129">**+inf**</span></span> | <span data-ttu-id="df521-130">**Не число**</span><span class="sxs-lookup"><span data-stu-id="df521-130">**NaN**</span></span> |
|---------------|----------|--------|--------|--------|--------|----------|---------|
| <span data-ttu-id="df521-131">**dest**-></span><span class="sxs-lookup"><span data-stu-id="df521-131">**dest**-></span></span> | <span data-ttu-id="df521-132">-0</span><span class="sxs-lookup"><span data-stu-id="df521-132">-0</span></span>       | <span data-ttu-id="df521-133">-F</span><span class="sxs-lookup"><span data-stu-id="df521-133">-F</span></span>     | <span data-ttu-id="df521-134">-inf</span><span class="sxs-lookup"><span data-stu-id="df521-134">-inf</span></span>   | <span data-ttu-id="df521-135">+inf</span><span class="sxs-lookup"><span data-stu-id="df521-135">+inf</span></span>   | <span data-ttu-id="df521-136">+ F</span><span class="sxs-lookup"><span data-stu-id="df521-136">+F</span></span>     | <span data-ttu-id="df521-137">+0</span><span class="sxs-lookup"><span data-stu-id="df521-137">+0</span></span>       | <span data-ttu-id="df521-138">Не число</span><span class="sxs-lookup"><span data-stu-id="df521-138">NaN</span></span>     |



 

<span data-ttu-id="df521-139">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="df521-139">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="df521-140">Вершина</span><span class="sxs-lookup"><span data-stu-id="df521-140">Vertex</span></span> | <span data-ttu-id="df521-141">Поверхности</span><span class="sxs-lookup"><span data-stu-id="df521-141">Hull</span></span> | <span data-ttu-id="df521-142">Домен</span><span class="sxs-lookup"><span data-stu-id="df521-142">Domain</span></span> | <span data-ttu-id="df521-143">Геометрия</span><span class="sxs-lookup"><span data-stu-id="df521-143">Geometry</span></span> | <span data-ttu-id="df521-144">Пиксель</span><span class="sxs-lookup"><span data-stu-id="df521-144">Pixel</span></span> | <span data-ttu-id="df521-145">Службы вычислений</span><span class="sxs-lookup"><span data-stu-id="df521-145">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="df521-146">X</span><span class="sxs-lookup"><span data-stu-id="df521-146">X</span></span>      | <span data-ttu-id="df521-147">X</span><span class="sxs-lookup"><span data-stu-id="df521-147">X</span></span>    | <span data-ttu-id="df521-148">X</span><span class="sxs-lookup"><span data-stu-id="df521-148">X</span></span>      | <span data-ttu-id="df521-149">X</span><span class="sxs-lookup"><span data-stu-id="df521-149">X</span></span>        | <span data-ttu-id="df521-150">X</span><span class="sxs-lookup"><span data-stu-id="df521-150">X</span></span>     | <span data-ttu-id="df521-151">X</span><span class="sxs-lookup"><span data-stu-id="df521-151">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="df521-152">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="df521-152">Minimum Shader Model</span></span>

<span data-ttu-id="df521-153">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="df521-153">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="df521-154">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="df521-154">Shader Model</span></span>                                              | <span data-ttu-id="df521-155">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="df521-155">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="df521-156">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="df521-156">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="df521-157">да</span><span class="sxs-lookup"><span data-stu-id="df521-157">yes</span></span>       |
| [<span data-ttu-id="df521-158">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="df521-158">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="df521-159">Нет</span><span class="sxs-lookup"><span data-stu-id="df521-159">no</span></span>        |
| [<span data-ttu-id="df521-160">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="df521-160">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="df521-161">Нет</span><span class="sxs-lookup"><span data-stu-id="df521-161">no</span></span>        |
| [<span data-ttu-id="df521-162">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="df521-162">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="df521-163">Нет</span><span class="sxs-lookup"><span data-stu-id="df521-163">no</span></span>        |
| [<span data-ttu-id="df521-164">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="df521-164">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="df521-165">Нет</span><span class="sxs-lookup"><span data-stu-id="df521-165">no</span></span>        |
| [<span data-ttu-id="df521-166">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="df521-166">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="df521-167">Нет</span><span class="sxs-lookup"><span data-stu-id="df521-167">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="df521-168">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="df521-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df521-169">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="df521-169">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





