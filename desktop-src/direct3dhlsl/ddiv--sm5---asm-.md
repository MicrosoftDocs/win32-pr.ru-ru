---
title: ддив (SM5-ASM)
description: Выполняет вычисление деления с двойной точностью на уровне компонентов.
ms.assetid: 0A67FC35-7F2F-4258-83CE-1CA398E57952
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81fc039b222b28a5fb1217d23c78470aff1739f7
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999161"
---
# <a name="ddiv-sm5---asm"></a><span data-ttu-id="1c2bf-103">ддив (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="1c2bf-103">ddiv (sm5 - asm)</span></span>

<span data-ttu-id="1c2bf-104">Выполняет вычисление деления с двойной точностью на уровне компонентов.</span><span class="sxs-lookup"><span data-stu-id="1c2bf-104">Computes a component-wise double-precision division.</span></span>



| <span data-ttu-id="1c2bf-105">ддив \[ \_ \] \[ . Маска \] , \[ - \] src0 \[ \_ ABS \] \[ . свиззле \] \[ - \] src1 \[ \_ ABS \] \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="1c2bf-105">ddiv\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\] \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="1c2bf-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="1c2bf-106">Item</span></span>                                                            | <span data-ttu-id="1c2bf-107">Описание</span><span class="sxs-lookup"><span data-stu-id="1c2bf-107">Description</span></span>                                                                                   |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c2bf-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="1c2bf-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="1c2bf-109">\[в \] результате операции.</span><span class="sxs-lookup"><span data-stu-id="1c2bf-109">\[in\] The result of the operation.</span></span> <span data-ttu-id="1c2bf-110">Значение результата должно быть точным до 0,5 ULP.</span><span class="sxs-lookup"><span data-stu-id="1c2bf-110">The result value must be accurate to 0.5 ULP.</span></span> <br/> |
| <span data-ttu-id="1c2bf-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="1c2bf-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="1c2bf-112">\[в \] делимом.</span><span class="sxs-lookup"><span data-stu-id="1c2bf-112">\[in\] The dividend.</span></span><br/>                                                               |
| <span data-ttu-id="1c2bf-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="1c2bf-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="1c2bf-114">\[в \] делителье.</span><span class="sxs-lookup"><span data-stu-id="1c2bf-114">\[in\] The divisor.</span></span><br/>                                                                |



 

## <a name="remarks"></a><span data-ttu-id="1c2bf-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="1c2bf-115">Remarks</span></span>

<span data-ttu-id="1c2bf-116">Инструкция ДДИВ будет выдаваться компилятором HLSL каждый раз, когда оператор деления используется с Double.</span><span class="sxs-lookup"><span data-stu-id="1c2bf-116">The DDIV instruction will be emitted by the HLSL compiler whenever the division operator is used with doubles.</span></span> <span data-ttu-id="1c2bf-117">Точность этой инструкции должна быть 0,5 ULP.</span><span class="sxs-lookup"><span data-stu-id="1c2bf-117">The accuracy of this instruction will be required to be 0.5 ULP.</span></span>

<span data-ttu-id="1c2bf-118">Шейдеры, использующие эту инструкцию, будут помечены флагом построителя текстуры, который приведет к сбою привязки, если не выполняются все следующие условия.</span><span class="sxs-lookup"><span data-stu-id="1c2bf-118">Shaders that use this instruction will be marked with a shader flag that will cause them to fail to bind unless all the following conditions are met.</span></span>

-   <span data-ttu-id="1c2bf-119">Система поддерживает DirectX 11,1.</span><span class="sxs-lookup"><span data-stu-id="1c2bf-119">The system supports DirectX 11.1.</span></span>
-   <span data-ttu-id="1c2bf-120">Система включает драйвер WDDM 1,2.</span><span class="sxs-lookup"><span data-stu-id="1c2bf-120">The system includes a WDDM 1.2 driver.</span></span>
-   <span data-ttu-id="1c2bf-121">Драйвер сообщает о поддержке этой инструкции с помощью **\_ \_ параметров D3D11 Data Feature D3D11 \_ \_ . Для Екстендеддаублесшадеринструктионс** задано значение **true**.</span><span class="sxs-lookup"><span data-stu-id="1c2bf-121">The driver reports support for this instruction via **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS.ExtendedDoublesShaderInstructions** set to **TRUE**.</span></span>

<span data-ttu-id="1c2bf-122">В следующей таблице показаны результаты, бтаинед при выполнении инструкции с различными классами чисел, предполагая, что ни переполнение, ни потеря точности не происходит.</span><span class="sxs-lookup"><span data-stu-id="1c2bf-122">The following table shows the results btained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="1c2bf-123">В этой таблице F означает ограничение по настоящему вещественному числу.</span><span class="sxs-lookup"><span data-stu-id="1c2bf-123">In this table F means finite-real number.</span></span>



| <span data-ttu-id="1c2bf-124">**src0 src1 — >**</span><span class="sxs-lookup"><span data-stu-id="1c2bf-124">**src0 src1 ->**</span></span> | <span data-ttu-id="1c2bf-125">**-INF**</span><span class="sxs-lookup"><span data-stu-id="1c2bf-125">**-inf**</span></span> | <span data-ttu-id="1c2bf-126">**-F**</span><span class="sxs-lookup"><span data-stu-id="1c2bf-126">**-F**</span></span> | <span data-ttu-id="1c2bf-127">**— 1,0**</span><span class="sxs-lookup"><span data-stu-id="1c2bf-127">**-1.0**</span></span> | <span data-ttu-id="1c2bf-128">**-0**</span><span class="sxs-lookup"><span data-stu-id="1c2bf-128">**-0**</span></span> | <span data-ttu-id="1c2bf-129">**+0**</span><span class="sxs-lookup"><span data-stu-id="1c2bf-129">**+0**</span></span> | <span data-ttu-id="1c2bf-130">**+ 1,0**</span><span class="sxs-lookup"><span data-stu-id="1c2bf-130">**+1.0**</span></span> | <span data-ttu-id="1c2bf-131">**+ F**</span><span class="sxs-lookup"><span data-stu-id="1c2bf-131">**+F**</span></span> | <span data-ttu-id="1c2bf-132">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="1c2bf-132">**+inf**</span></span> | <span data-ttu-id="1c2bf-133">**Не число**</span><span class="sxs-lookup"><span data-stu-id="1c2bf-133">**NaN**</span></span> |
|---------------------|----------|--------|----------|--------|--------|----------|--------|----------|---------|
| <span data-ttu-id="1c2bf-134">**-INF**</span><span class="sxs-lookup"><span data-stu-id="1c2bf-134">**-inf**</span></span>            | <span data-ttu-id="1c2bf-135">не число</span><span class="sxs-lookup"><span data-stu-id="1c2bf-135">NaN</span></span>      | <span data-ttu-id="1c2bf-136">+inf</span><span class="sxs-lookup"><span data-stu-id="1c2bf-136">+inf</span></span>   | <span data-ttu-id="1c2bf-137">+inf</span><span class="sxs-lookup"><span data-stu-id="1c2bf-137">+inf</span></span>     | <span data-ttu-id="1c2bf-138">+inf</span><span class="sxs-lookup"><span data-stu-id="1c2bf-138">+inf</span></span>   | <span data-ttu-id="1c2bf-139">-inf</span><span class="sxs-lookup"><span data-stu-id="1c2bf-139">-inf</span></span>   | <span data-ttu-id="1c2bf-140">-inf</span><span class="sxs-lookup"><span data-stu-id="1c2bf-140">-inf</span></span>     | <span data-ttu-id="1c2bf-141">-inf</span><span class="sxs-lookup"><span data-stu-id="1c2bf-141">-inf</span></span>   | <span data-ttu-id="1c2bf-142">Не число</span><span class="sxs-lookup"><span data-stu-id="1c2bf-142">NaN</span></span>      | <span data-ttu-id="1c2bf-143">Не число</span><span class="sxs-lookup"><span data-stu-id="1c2bf-143">NaN</span></span>     |
| <span data-ttu-id="1c2bf-144">**-F**</span><span class="sxs-lookup"><span data-stu-id="1c2bf-144">**-F**</span></span>              | <span data-ttu-id="1c2bf-145">+0</span><span class="sxs-lookup"><span data-stu-id="1c2bf-145">+0</span></span>       | <span data-ttu-id="1c2bf-146">+ F</span><span class="sxs-lookup"><span data-stu-id="1c2bf-146">+F</span></span>     | <span data-ttu-id="1c2bf-147">-src0</span><span class="sxs-lookup"><span data-stu-id="1c2bf-147">-src0</span></span>    | <span data-ttu-id="1c2bf-148">+inf</span><span class="sxs-lookup"><span data-stu-id="1c2bf-148">+inf</span></span>   | <span data-ttu-id="1c2bf-149">-inf</span><span class="sxs-lookup"><span data-stu-id="1c2bf-149">-inf</span></span>   | <span data-ttu-id="1c2bf-150">src0</span><span class="sxs-lookup"><span data-stu-id="1c2bf-150">src0</span></span>     | <span data-ttu-id="1c2bf-151">-F</span><span class="sxs-lookup"><span data-stu-id="1c2bf-151">-F</span></span>     | <span data-ttu-id="1c2bf-152">-0</span><span class="sxs-lookup"><span data-stu-id="1c2bf-152">-0</span></span>       | <span data-ttu-id="1c2bf-153">Не число</span><span class="sxs-lookup"><span data-stu-id="1c2bf-153">NaN</span></span>     |
| <span data-ttu-id="1c2bf-154">**-0**</span><span class="sxs-lookup"><span data-stu-id="1c2bf-154">**-0**</span></span>              | <span data-ttu-id="1c2bf-155">+0</span><span class="sxs-lookup"><span data-stu-id="1c2bf-155">+0</span></span>       | <span data-ttu-id="1c2bf-156">+0</span><span class="sxs-lookup"><span data-stu-id="1c2bf-156">+0</span></span>     | <span data-ttu-id="1c2bf-157">+0</span><span class="sxs-lookup"><span data-stu-id="1c2bf-157">+0</span></span>       | <span data-ttu-id="1c2bf-158">Не число</span><span class="sxs-lookup"><span data-stu-id="1c2bf-158">NaN</span></span>    | <span data-ttu-id="1c2bf-159">Не число</span><span class="sxs-lookup"><span data-stu-id="1c2bf-159">NaN</span></span>    | <span data-ttu-id="1c2bf-160">-0</span><span class="sxs-lookup"><span data-stu-id="1c2bf-160">-0</span></span>       | <span data-ttu-id="1c2bf-161">-0</span><span class="sxs-lookup"><span data-stu-id="1c2bf-161">-0</span></span>     | <span data-ttu-id="1c2bf-162">-0</span><span class="sxs-lookup"><span data-stu-id="1c2bf-162">-0</span></span>       | <span data-ttu-id="1c2bf-163">Не число</span><span class="sxs-lookup"><span data-stu-id="1c2bf-163">NaN</span></span>     |
| <span data-ttu-id="1c2bf-164">**+0**</span><span class="sxs-lookup"><span data-stu-id="1c2bf-164">**+0**</span></span>              | <span data-ttu-id="1c2bf-165">-0</span><span class="sxs-lookup"><span data-stu-id="1c2bf-165">-0</span></span>       | <span data-ttu-id="1c2bf-166">-0</span><span class="sxs-lookup"><span data-stu-id="1c2bf-166">-0</span></span>     | <span data-ttu-id="1c2bf-167">-0</span><span class="sxs-lookup"><span data-stu-id="1c2bf-167">-0</span></span>       | <span data-ttu-id="1c2bf-168">Не число</span><span class="sxs-lookup"><span data-stu-id="1c2bf-168">NaN</span></span>    | <span data-ttu-id="1c2bf-169">Не число</span><span class="sxs-lookup"><span data-stu-id="1c2bf-169">NaN</span></span>    | <span data-ttu-id="1c2bf-170">+0</span><span class="sxs-lookup"><span data-stu-id="1c2bf-170">+0</span></span>       | <span data-ttu-id="1c2bf-171">+0</span><span class="sxs-lookup"><span data-stu-id="1c2bf-171">+0</span></span>     | <span data-ttu-id="1c2bf-172">+0</span><span class="sxs-lookup"><span data-stu-id="1c2bf-172">+0</span></span>       | <span data-ttu-id="1c2bf-173">Не число</span><span class="sxs-lookup"><span data-stu-id="1c2bf-173">NaN</span></span>     |
| <span data-ttu-id="1c2bf-174">**+ F**</span><span class="sxs-lookup"><span data-stu-id="1c2bf-174">**+F**</span></span>              | <span data-ttu-id="1c2bf-175">-0</span><span class="sxs-lookup"><span data-stu-id="1c2bf-175">-0</span></span>       | <span data-ttu-id="1c2bf-176">-F</span><span class="sxs-lookup"><span data-stu-id="1c2bf-176">-F</span></span>     | <span data-ttu-id="1c2bf-177">-src0</span><span class="sxs-lookup"><span data-stu-id="1c2bf-177">-src0</span></span>    | <span data-ttu-id="1c2bf-178">-inf</span><span class="sxs-lookup"><span data-stu-id="1c2bf-178">-inf</span></span>   | <span data-ttu-id="1c2bf-179">+inf</span><span class="sxs-lookup"><span data-stu-id="1c2bf-179">+inf</span></span>   | <span data-ttu-id="1c2bf-180">src0</span><span class="sxs-lookup"><span data-stu-id="1c2bf-180">src0</span></span>     | <span data-ttu-id="1c2bf-181">+ F</span><span class="sxs-lookup"><span data-stu-id="1c2bf-181">+F</span></span>     | <span data-ttu-id="1c2bf-182">+0</span><span class="sxs-lookup"><span data-stu-id="1c2bf-182">+0</span></span>       | <span data-ttu-id="1c2bf-183">Не число</span><span class="sxs-lookup"><span data-stu-id="1c2bf-183">NaN</span></span>     |
| <span data-ttu-id="1c2bf-184">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="1c2bf-184">**+inf**</span></span>            | <span data-ttu-id="1c2bf-185">не число</span><span class="sxs-lookup"><span data-stu-id="1c2bf-185">NaN</span></span>      | <span data-ttu-id="1c2bf-186">-inf</span><span class="sxs-lookup"><span data-stu-id="1c2bf-186">-inf</span></span>   | <span data-ttu-id="1c2bf-187">-inf</span><span class="sxs-lookup"><span data-stu-id="1c2bf-187">-inf</span></span>     | <span data-ttu-id="1c2bf-188">-inf</span><span class="sxs-lookup"><span data-stu-id="1c2bf-188">-inf</span></span>   | <span data-ttu-id="1c2bf-189">+inf</span><span class="sxs-lookup"><span data-stu-id="1c2bf-189">+inf</span></span>   | <span data-ttu-id="1c2bf-190">+inf</span><span class="sxs-lookup"><span data-stu-id="1c2bf-190">+inf</span></span>     | <span data-ttu-id="1c2bf-191">+inf</span><span class="sxs-lookup"><span data-stu-id="1c2bf-191">+inf</span></span>   | <span data-ttu-id="1c2bf-192">Не число</span><span class="sxs-lookup"><span data-stu-id="1c2bf-192">NaN</span></span>      | <span data-ttu-id="1c2bf-193">Не число</span><span class="sxs-lookup"><span data-stu-id="1c2bf-193">NaN</span></span>     |
| <span data-ttu-id="1c2bf-194">**Не число**</span><span class="sxs-lookup"><span data-stu-id="1c2bf-194">**NaN**</span></span>             | <span data-ttu-id="1c2bf-195">Не число</span><span class="sxs-lookup"><span data-stu-id="1c2bf-195">NaN</span></span>      | <span data-ttu-id="1c2bf-196">Не число</span><span class="sxs-lookup"><span data-stu-id="1c2bf-196">NaN</span></span>    | <span data-ttu-id="1c2bf-197">Не число</span><span class="sxs-lookup"><span data-stu-id="1c2bf-197">NaN</span></span>      | <span data-ttu-id="1c2bf-198">Не число</span><span class="sxs-lookup"><span data-stu-id="1c2bf-198">NaN</span></span>    | <span data-ttu-id="1c2bf-199">Не число</span><span class="sxs-lookup"><span data-stu-id="1c2bf-199">NaN</span></span>    | <span data-ttu-id="1c2bf-200">Не число</span><span class="sxs-lookup"><span data-stu-id="1c2bf-200">NaN</span></span>      | <span data-ttu-id="1c2bf-201">Не число</span><span class="sxs-lookup"><span data-stu-id="1c2bf-201">NaN</span></span>    | <span data-ttu-id="1c2bf-202">Не число</span><span class="sxs-lookup"><span data-stu-id="1c2bf-202">NaN</span></span>      | <span data-ttu-id="1c2bf-203">Не число</span><span class="sxs-lookup"><span data-stu-id="1c2bf-203">NaN</span></span>     |



 

<span data-ttu-id="1c2bf-204">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="1c2bf-204">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="1c2bf-205">Вершина</span><span class="sxs-lookup"><span data-stu-id="1c2bf-205">Vertex</span></span> | <span data-ttu-id="1c2bf-206">Поверхности</span><span class="sxs-lookup"><span data-stu-id="1c2bf-206">Hull</span></span> | <span data-ttu-id="1c2bf-207">Домен</span><span class="sxs-lookup"><span data-stu-id="1c2bf-207">Domain</span></span> | <span data-ttu-id="1c2bf-208">Геометрия</span><span class="sxs-lookup"><span data-stu-id="1c2bf-208">Geometry</span></span> | <span data-ttu-id="1c2bf-209">Пиксель</span><span class="sxs-lookup"><span data-stu-id="1c2bf-209">Pixel</span></span> | <span data-ttu-id="1c2bf-210">Службы вычислений</span><span class="sxs-lookup"><span data-stu-id="1c2bf-210">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="1c2bf-211">X</span><span class="sxs-lookup"><span data-stu-id="1c2bf-211">X</span></span>      | <span data-ttu-id="1c2bf-212">X</span><span class="sxs-lookup"><span data-stu-id="1c2bf-212">X</span></span>    | <span data-ttu-id="1c2bf-213">X</span><span class="sxs-lookup"><span data-stu-id="1c2bf-213">X</span></span>      | <span data-ttu-id="1c2bf-214">X</span><span class="sxs-lookup"><span data-stu-id="1c2bf-214">X</span></span>        | <span data-ttu-id="1c2bf-215">X</span><span class="sxs-lookup"><span data-stu-id="1c2bf-215">X</span></span>     | <span data-ttu-id="1c2bf-216">X</span><span class="sxs-lookup"><span data-stu-id="1c2bf-216">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1c2bf-217">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="1c2bf-217">Minimum Shader Model</span></span>

<span data-ttu-id="1c2bf-218">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="1c2bf-218">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="1c2bf-219">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="1c2bf-219">Shader Model</span></span>                                              | <span data-ttu-id="1c2bf-220">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="1c2bf-220">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1c2bf-221">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="1c2bf-221">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1c2bf-222">да</span><span class="sxs-lookup"><span data-stu-id="1c2bf-222">yes</span></span>       |
| [<span data-ttu-id="1c2bf-223">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="1c2bf-223">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1c2bf-224">Нет</span><span class="sxs-lookup"><span data-stu-id="1c2bf-224">no</span></span>        |
| [<span data-ttu-id="1c2bf-225">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="1c2bf-225">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1c2bf-226">Нет</span><span class="sxs-lookup"><span data-stu-id="1c2bf-226">no</span></span>        |
| [<span data-ttu-id="1c2bf-227">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1c2bf-227">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1c2bf-228">Нет</span><span class="sxs-lookup"><span data-stu-id="1c2bf-228">no</span></span>        |
| [<span data-ttu-id="1c2bf-229">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1c2bf-229">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1c2bf-230">Нет</span><span class="sxs-lookup"><span data-stu-id="1c2bf-230">no</span></span>        |
| [<span data-ttu-id="1c2bf-231">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1c2bf-231">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1c2bf-232">Нет</span><span class="sxs-lookup"><span data-stu-id="1c2bf-232">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1c2bf-233">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="1c2bf-233">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c2bf-234">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1c2bf-234">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





