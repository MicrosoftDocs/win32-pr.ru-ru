---
title: ддив (SM5-ASM)
description: Выполняет вычисление деления с двойной точностью на уровне компонентов.
ms.assetid: 0A67FC35-7F2F-4258-83CE-1CA398E57952
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56f5c3aae9d416d24f41de8d8308c5a69be9d016
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996875"
---
# <a name="ddiv-sm5---asm"></a><span data-ttu-id="20bc2-103">ддив (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="20bc2-103">ddiv (sm5 - asm)</span></span>

<span data-ttu-id="20bc2-104">Выполняет вычисление деления с двойной точностью на уровне компонентов.</span><span class="sxs-lookup"><span data-stu-id="20bc2-104">Computes a component-wise double-precision division.</span></span>



| <span data-ttu-id="20bc2-105">ддив \[ \_ \] \[ . Маска \] , \[ - \] src0 \[ \_ ABS \] \[ . свиззле \] \[ - \] src1 \[ \_ ABS \] \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="20bc2-105">ddiv\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\] \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="20bc2-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="20bc2-106">Item</span></span>                                                            | <span data-ttu-id="20bc2-107">Описание</span><span class="sxs-lookup"><span data-stu-id="20bc2-107">Description</span></span>                                                                                   |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="20bc2-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="20bc2-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="20bc2-109">\[в \] результате операции.</span><span class="sxs-lookup"><span data-stu-id="20bc2-109">\[in\] The result of the operation.</span></span> <span data-ttu-id="20bc2-110">Значение результата должно быть точным до 0,5 ULP.</span><span class="sxs-lookup"><span data-stu-id="20bc2-110">The result value must be accurate to 0.5 ULP.</span></span> <br/> |
| <span data-ttu-id="20bc2-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="20bc2-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="20bc2-112">\[в \] делимом.</span><span class="sxs-lookup"><span data-stu-id="20bc2-112">\[in\] The dividend.</span></span><br/>                                                               |
| <span data-ttu-id="20bc2-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="20bc2-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="20bc2-114">\[в \] делителье.</span><span class="sxs-lookup"><span data-stu-id="20bc2-114">\[in\] The divisor.</span></span><br/>                                                                |



 

## <a name="remarks"></a><span data-ttu-id="20bc2-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="20bc2-115">Remarks</span></span>

<span data-ttu-id="20bc2-116">Инструкция ДДИВ будет выдаваться компилятором HLSL каждый раз, когда оператор деления используется с Double.</span><span class="sxs-lookup"><span data-stu-id="20bc2-116">The DDIV instruction will be emitted by the HLSL compiler whenever the division operator is used with doubles.</span></span> <span data-ttu-id="20bc2-117">Точность этой инструкции должна быть 0,5 ULP.</span><span class="sxs-lookup"><span data-stu-id="20bc2-117">The accuracy of this instruction will be required to be 0.5 ULP.</span></span>

<span data-ttu-id="20bc2-118">Шейдеры, использующие эту инструкцию, будут помечены флагом построителя текстуры, который приведет к сбою привязки, если не выполняются все следующие условия.</span><span class="sxs-lookup"><span data-stu-id="20bc2-118">Shaders that use this instruction will be marked with a shader flag that will cause them to fail to bind unless all the following conditions are met.</span></span>

-   <span data-ttu-id="20bc2-119">Система поддерживает DirectX 11,1.</span><span class="sxs-lookup"><span data-stu-id="20bc2-119">The system supports DirectX 11.1.</span></span>
-   <span data-ttu-id="20bc2-120">Система включает драйвер WDDM 1,2.</span><span class="sxs-lookup"><span data-stu-id="20bc2-120">The system includes a WDDM 1.2 driver.</span></span>
-   <span data-ttu-id="20bc2-121">Драйвер сообщает о поддержке этой инструкции с помощью **\_ \_ параметров D3D11 Data Feature D3D11 \_ \_ . Для Екстендеддаублесшадеринструктионс** задано значение **true**.</span><span class="sxs-lookup"><span data-stu-id="20bc2-121">The driver reports support for this instruction via **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS.ExtendedDoublesShaderInstructions** set to **TRUE**.</span></span>

<span data-ttu-id="20bc2-122">В следующей таблице показаны результаты, бтаинед при выполнении инструкции с различными классами чисел, предполагая, что ни переполнение, ни потеря точности не происходит.</span><span class="sxs-lookup"><span data-stu-id="20bc2-122">The following table shows the results btained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="20bc2-123">В этой таблице F означает ограничение по настоящему вещественному числу.</span><span class="sxs-lookup"><span data-stu-id="20bc2-123">In this table F means finite-real number.</span></span>



|                     |          |        |          |        |        |          |        |          |         |
|---------------------|----------|--------|----------|--------|--------|----------|--------|----------|---------|
| <span data-ttu-id="20bc2-124">**src0 src1 — >**</span><span class="sxs-lookup"><span data-stu-id="20bc2-124">**src0 src1 ->**</span></span> | <span data-ttu-id="20bc2-125">**-INF**</span><span class="sxs-lookup"><span data-stu-id="20bc2-125">**-inf**</span></span> | <span data-ttu-id="20bc2-126">**-F**</span><span class="sxs-lookup"><span data-stu-id="20bc2-126">**-F**</span></span> | <span data-ttu-id="20bc2-127">**— 1,0**</span><span class="sxs-lookup"><span data-stu-id="20bc2-127">**-1.0**</span></span> | <span data-ttu-id="20bc2-128">**-0**</span><span class="sxs-lookup"><span data-stu-id="20bc2-128">**-0**</span></span> | <span data-ttu-id="20bc2-129">**+0**</span><span class="sxs-lookup"><span data-stu-id="20bc2-129">**+0**</span></span> | <span data-ttu-id="20bc2-130">**+ 1,0**</span><span class="sxs-lookup"><span data-stu-id="20bc2-130">**+1.0**</span></span> | <span data-ttu-id="20bc2-131">**+ F**</span><span class="sxs-lookup"><span data-stu-id="20bc2-131">**+F**</span></span> | <span data-ttu-id="20bc2-132">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="20bc2-132">**+inf**</span></span> | <span data-ttu-id="20bc2-133">**Не число**</span><span class="sxs-lookup"><span data-stu-id="20bc2-133">**NaN**</span></span> |
| <span data-ttu-id="20bc2-134">**-INF**</span><span class="sxs-lookup"><span data-stu-id="20bc2-134">**-inf**</span></span>            | <span data-ttu-id="20bc2-135">не число</span><span class="sxs-lookup"><span data-stu-id="20bc2-135">NaN</span></span>      | <span data-ttu-id="20bc2-136">+inf</span><span class="sxs-lookup"><span data-stu-id="20bc2-136">+inf</span></span>   | <span data-ttu-id="20bc2-137">+inf</span><span class="sxs-lookup"><span data-stu-id="20bc2-137">+inf</span></span>     | <span data-ttu-id="20bc2-138">+inf</span><span class="sxs-lookup"><span data-stu-id="20bc2-138">+inf</span></span>   | <span data-ttu-id="20bc2-139">-inf</span><span class="sxs-lookup"><span data-stu-id="20bc2-139">-inf</span></span>   | <span data-ttu-id="20bc2-140">-inf</span><span class="sxs-lookup"><span data-stu-id="20bc2-140">-inf</span></span>     | <span data-ttu-id="20bc2-141">-inf</span><span class="sxs-lookup"><span data-stu-id="20bc2-141">-inf</span></span>   | <span data-ttu-id="20bc2-142">Не число</span><span class="sxs-lookup"><span data-stu-id="20bc2-142">NaN</span></span>      | <span data-ttu-id="20bc2-143">Не число</span><span class="sxs-lookup"><span data-stu-id="20bc2-143">NaN</span></span>     |
| <span data-ttu-id="20bc2-144">**-F**</span><span class="sxs-lookup"><span data-stu-id="20bc2-144">**-F**</span></span>              | <span data-ttu-id="20bc2-145">+0</span><span class="sxs-lookup"><span data-stu-id="20bc2-145">+0</span></span>       | <span data-ttu-id="20bc2-146">+ F</span><span class="sxs-lookup"><span data-stu-id="20bc2-146">+F</span></span>     | <span data-ttu-id="20bc2-147">-src0</span><span class="sxs-lookup"><span data-stu-id="20bc2-147">-src0</span></span>    | <span data-ttu-id="20bc2-148">+inf</span><span class="sxs-lookup"><span data-stu-id="20bc2-148">+inf</span></span>   | <span data-ttu-id="20bc2-149">-inf</span><span class="sxs-lookup"><span data-stu-id="20bc2-149">-inf</span></span>   | <span data-ttu-id="20bc2-150">src0</span><span class="sxs-lookup"><span data-stu-id="20bc2-150">src0</span></span>     | <span data-ttu-id="20bc2-151">-F</span><span class="sxs-lookup"><span data-stu-id="20bc2-151">-F</span></span>     | <span data-ttu-id="20bc2-152">-0</span><span class="sxs-lookup"><span data-stu-id="20bc2-152">-0</span></span>       | <span data-ttu-id="20bc2-153">Не число</span><span class="sxs-lookup"><span data-stu-id="20bc2-153">NaN</span></span>     |
| <span data-ttu-id="20bc2-154">**-0**</span><span class="sxs-lookup"><span data-stu-id="20bc2-154">**-0**</span></span>              | <span data-ttu-id="20bc2-155">+0</span><span class="sxs-lookup"><span data-stu-id="20bc2-155">+0</span></span>       | <span data-ttu-id="20bc2-156">+0</span><span class="sxs-lookup"><span data-stu-id="20bc2-156">+0</span></span>     | <span data-ttu-id="20bc2-157">+0</span><span class="sxs-lookup"><span data-stu-id="20bc2-157">+0</span></span>       | <span data-ttu-id="20bc2-158">Не число</span><span class="sxs-lookup"><span data-stu-id="20bc2-158">NaN</span></span>    | <span data-ttu-id="20bc2-159">Не число</span><span class="sxs-lookup"><span data-stu-id="20bc2-159">NaN</span></span>    | <span data-ttu-id="20bc2-160">-0</span><span class="sxs-lookup"><span data-stu-id="20bc2-160">-0</span></span>       | <span data-ttu-id="20bc2-161">-0</span><span class="sxs-lookup"><span data-stu-id="20bc2-161">-0</span></span>     | <span data-ttu-id="20bc2-162">-0</span><span class="sxs-lookup"><span data-stu-id="20bc2-162">-0</span></span>       | <span data-ttu-id="20bc2-163">Не число</span><span class="sxs-lookup"><span data-stu-id="20bc2-163">NaN</span></span>     |
| <span data-ttu-id="20bc2-164">**+0**</span><span class="sxs-lookup"><span data-stu-id="20bc2-164">**+0**</span></span>              | <span data-ttu-id="20bc2-165">-0</span><span class="sxs-lookup"><span data-stu-id="20bc2-165">-0</span></span>       | <span data-ttu-id="20bc2-166">-0</span><span class="sxs-lookup"><span data-stu-id="20bc2-166">-0</span></span>     | <span data-ttu-id="20bc2-167">-0</span><span class="sxs-lookup"><span data-stu-id="20bc2-167">-0</span></span>       | <span data-ttu-id="20bc2-168">Не число</span><span class="sxs-lookup"><span data-stu-id="20bc2-168">NaN</span></span>    | <span data-ttu-id="20bc2-169">Не число</span><span class="sxs-lookup"><span data-stu-id="20bc2-169">NaN</span></span>    | <span data-ttu-id="20bc2-170">+0</span><span class="sxs-lookup"><span data-stu-id="20bc2-170">+0</span></span>       | <span data-ttu-id="20bc2-171">+0</span><span class="sxs-lookup"><span data-stu-id="20bc2-171">+0</span></span>     | <span data-ttu-id="20bc2-172">+0</span><span class="sxs-lookup"><span data-stu-id="20bc2-172">+0</span></span>       | <span data-ttu-id="20bc2-173">Не число</span><span class="sxs-lookup"><span data-stu-id="20bc2-173">NaN</span></span>     |
| <span data-ttu-id="20bc2-174">**+ F**</span><span class="sxs-lookup"><span data-stu-id="20bc2-174">**+F**</span></span>              | <span data-ttu-id="20bc2-175">-0</span><span class="sxs-lookup"><span data-stu-id="20bc2-175">-0</span></span>       | <span data-ttu-id="20bc2-176">-F</span><span class="sxs-lookup"><span data-stu-id="20bc2-176">-F</span></span>     | <span data-ttu-id="20bc2-177">-src0</span><span class="sxs-lookup"><span data-stu-id="20bc2-177">-src0</span></span>    | <span data-ttu-id="20bc2-178">-inf</span><span class="sxs-lookup"><span data-stu-id="20bc2-178">-inf</span></span>   | <span data-ttu-id="20bc2-179">+inf</span><span class="sxs-lookup"><span data-stu-id="20bc2-179">+inf</span></span>   | <span data-ttu-id="20bc2-180">src0</span><span class="sxs-lookup"><span data-stu-id="20bc2-180">src0</span></span>     | <span data-ttu-id="20bc2-181">+ F</span><span class="sxs-lookup"><span data-stu-id="20bc2-181">+F</span></span>     | <span data-ttu-id="20bc2-182">+0</span><span class="sxs-lookup"><span data-stu-id="20bc2-182">+0</span></span>       | <span data-ttu-id="20bc2-183">Не число</span><span class="sxs-lookup"><span data-stu-id="20bc2-183">NaN</span></span>     |
| <span data-ttu-id="20bc2-184">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="20bc2-184">**+inf**</span></span>            | <span data-ttu-id="20bc2-185">не число</span><span class="sxs-lookup"><span data-stu-id="20bc2-185">NaN</span></span>      | <span data-ttu-id="20bc2-186">-inf</span><span class="sxs-lookup"><span data-stu-id="20bc2-186">-inf</span></span>   | <span data-ttu-id="20bc2-187">-inf</span><span class="sxs-lookup"><span data-stu-id="20bc2-187">-inf</span></span>     | <span data-ttu-id="20bc2-188">-inf</span><span class="sxs-lookup"><span data-stu-id="20bc2-188">-inf</span></span>   | <span data-ttu-id="20bc2-189">+inf</span><span class="sxs-lookup"><span data-stu-id="20bc2-189">+inf</span></span>   | <span data-ttu-id="20bc2-190">+inf</span><span class="sxs-lookup"><span data-stu-id="20bc2-190">+inf</span></span>     | <span data-ttu-id="20bc2-191">+inf</span><span class="sxs-lookup"><span data-stu-id="20bc2-191">+inf</span></span>   | <span data-ttu-id="20bc2-192">Не число</span><span class="sxs-lookup"><span data-stu-id="20bc2-192">NaN</span></span>      | <span data-ttu-id="20bc2-193">Не число</span><span class="sxs-lookup"><span data-stu-id="20bc2-193">NaN</span></span>     |
| <span data-ttu-id="20bc2-194">**Не число**</span><span class="sxs-lookup"><span data-stu-id="20bc2-194">**NaN**</span></span>             | <span data-ttu-id="20bc2-195">Не число</span><span class="sxs-lookup"><span data-stu-id="20bc2-195">NaN</span></span>      | <span data-ttu-id="20bc2-196">Не число</span><span class="sxs-lookup"><span data-stu-id="20bc2-196">NaN</span></span>    | <span data-ttu-id="20bc2-197">Не число</span><span class="sxs-lookup"><span data-stu-id="20bc2-197">NaN</span></span>      | <span data-ttu-id="20bc2-198">Не число</span><span class="sxs-lookup"><span data-stu-id="20bc2-198">NaN</span></span>    | <span data-ttu-id="20bc2-199">Не число</span><span class="sxs-lookup"><span data-stu-id="20bc2-199">NaN</span></span>    | <span data-ttu-id="20bc2-200">Не число</span><span class="sxs-lookup"><span data-stu-id="20bc2-200">NaN</span></span>      | <span data-ttu-id="20bc2-201">Не число</span><span class="sxs-lookup"><span data-stu-id="20bc2-201">NaN</span></span>    | <span data-ttu-id="20bc2-202">Не число</span><span class="sxs-lookup"><span data-stu-id="20bc2-202">NaN</span></span>      | <span data-ttu-id="20bc2-203">Не число</span><span class="sxs-lookup"><span data-stu-id="20bc2-203">NaN</span></span>     |



 

<span data-ttu-id="20bc2-204">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="20bc2-204">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="20bc2-205">Вершина</span><span class="sxs-lookup"><span data-stu-id="20bc2-205">Vertex</span></span> | <span data-ttu-id="20bc2-206">Поверхности</span><span class="sxs-lookup"><span data-stu-id="20bc2-206">Hull</span></span> | <span data-ttu-id="20bc2-207">Домен</span><span class="sxs-lookup"><span data-stu-id="20bc2-207">Domain</span></span> | <span data-ttu-id="20bc2-208">Геометрия</span><span class="sxs-lookup"><span data-stu-id="20bc2-208">Geometry</span></span> | <span data-ttu-id="20bc2-209">Пиксель</span><span class="sxs-lookup"><span data-stu-id="20bc2-209">Pixel</span></span> | <span data-ttu-id="20bc2-210">Вычисления</span><span class="sxs-lookup"><span data-stu-id="20bc2-210">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="20bc2-211">X</span><span class="sxs-lookup"><span data-stu-id="20bc2-211">X</span></span>      | <span data-ttu-id="20bc2-212">X</span><span class="sxs-lookup"><span data-stu-id="20bc2-212">X</span></span>    | <span data-ttu-id="20bc2-213">X</span><span class="sxs-lookup"><span data-stu-id="20bc2-213">X</span></span>      | <span data-ttu-id="20bc2-214">X</span><span class="sxs-lookup"><span data-stu-id="20bc2-214">X</span></span>        | <span data-ttu-id="20bc2-215">X</span><span class="sxs-lookup"><span data-stu-id="20bc2-215">X</span></span>     | <span data-ttu-id="20bc2-216">X</span><span class="sxs-lookup"><span data-stu-id="20bc2-216">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="20bc2-217">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="20bc2-217">Minimum Shader Model</span></span>

<span data-ttu-id="20bc2-218">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="20bc2-218">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="20bc2-219">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="20bc2-219">Shader Model</span></span>                                              | <span data-ttu-id="20bc2-220">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="20bc2-220">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="20bc2-221">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="20bc2-221">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="20bc2-222">да</span><span class="sxs-lookup"><span data-stu-id="20bc2-222">yes</span></span>       |
| [<span data-ttu-id="20bc2-223">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="20bc2-223">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="20bc2-224">Нет</span><span class="sxs-lookup"><span data-stu-id="20bc2-224">no</span></span>        |
| [<span data-ttu-id="20bc2-225">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="20bc2-225">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="20bc2-226">Нет</span><span class="sxs-lookup"><span data-stu-id="20bc2-226">no</span></span>        |
| [<span data-ttu-id="20bc2-227">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="20bc2-227">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="20bc2-228">Нет</span><span class="sxs-lookup"><span data-stu-id="20bc2-228">no</span></span>        |
| [<span data-ttu-id="20bc2-229">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="20bc2-229">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="20bc2-230">Нет</span><span class="sxs-lookup"><span data-stu-id="20bc2-230">no</span></span>        |
| [<span data-ttu-id="20bc2-231">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="20bc2-231">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="20bc2-232">Нет</span><span class="sxs-lookup"><span data-stu-id="20bc2-232">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="20bc2-233">См. также</span><span class="sxs-lookup"><span data-stu-id="20bc2-233">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20bc2-234">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="20bc2-234">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





