---
title: дмул (SM5-ASM)
description: Возведение двойной точности на уровне компонентов.
ms.assetid: 53AE27BE-2F4B-4C55-B496-D7122C00DC52
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18cce59ae237610b1038d90e02dff429812b4f00
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996894"
---
# <a name="dmul-sm5---asm"></a><span data-ttu-id="4df3d-103">дмул (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="4df3d-103">dmul (sm5 - asm)</span></span>

<span data-ttu-id="4df3d-104">Возведение двойной точности на уровне компонентов.</span><span class="sxs-lookup"><span data-stu-id="4df3d-104">Component-wise double-precision multiply.</span></span>



| <span data-ttu-id="4df3d-105">дмул \[ \_ \] \[ . Маска \] , \[ - \] src0 \[ \_ ABS \] \[ . свиззле \] , \[ - \] src1 \[ \_ ABS \] \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="4df3d-105">dmul\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="4df3d-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="4df3d-106">Item</span></span>                                                            | <span data-ttu-id="4df3d-107">Описание</span><span class="sxs-lookup"><span data-stu-id="4df3d-107">Description</span></span>                                                                                        |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4df3d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="4df3d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="4df3d-109">\[в \] адресе результата операции.</span><span class="sxs-lookup"><span data-stu-id="4df3d-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="4df3d-110">*конечный адрес*  =  *src0* \* *src1*</span><span class="sxs-lookup"><span data-stu-id="4df3d-110">*dest* = *src0* \* *src1*</span></span><br/> |
| <span data-ttu-id="4df3d-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="4df3d-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="4df3d-112">\[в \] компонентах для перемножения с *src1*.</span><span class="sxs-lookup"><span data-stu-id="4df3d-112">\[in\] The components to multiply with *src1*.</span></span><br/>                                          |
| <span data-ttu-id="4df3d-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="4df3d-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="4df3d-114">\[в \] компонентах для перемножения с *src0*.</span><span class="sxs-lookup"><span data-stu-id="4df3d-114">\[in\] The components to multiply with *src0*.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="4df3d-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="4df3d-115">Remarks</span></span>

<span data-ttu-id="4df3d-116">Допустимыми свиззлес для параметров источника являются. ксизв,. ксикси,. звкси,. звзв.</span><span class="sxs-lookup"><span data-stu-id="4df3d-116">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="4df3d-117">Допустимые маски *приемников* : XY, ZW и. ксизв.</span><span class="sxs-lookup"><span data-stu-id="4df3d-117">The valid *dest* masks are .xy, .zw, and .xyzw.</span></span> <span data-ttu-id="4df3d-118">Следующие сопоставления *src* — это POST-свиззле:</span><span class="sxs-lookup"><span data-stu-id="4df3d-118">The following *src* mappings are post-swizzle:</span></span>

-   <span data-ttu-id="4df3d-119">*dest* — это двойное vec2 в (x 32LSB, y 32MSB) и (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="4df3d-119">*dest* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="4df3d-120">*src0* — это двойное vec2 в (x 32LSB, y 32MSB) и (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="4df3d-120">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="4df3d-121">*src1* — это двойное vec2 в (x 32LSB, y 32MSB) и (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="4df3d-121">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="4df3d-122">В следующей таблице показаны результаты, полученные при выполнении инструкции с различными классами чисел, предполагая, что ни переполнение, ни потеря точности не происходит.</span><span class="sxs-lookup"><span data-stu-id="4df3d-122">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="4df3d-123">F означает ограничение по настоящему вещественному числу.</span><span class="sxs-lookup"><span data-stu-id="4df3d-123">F means finite-real number.</span></span>



|                    |          |        |          |        |        |          |        |          |         |
|--------------------|----------|--------|----------|--------|--------|----------|--------|----------|---------|
| <span data-ttu-id="4df3d-124">**src0 src1 — >**</span><span class="sxs-lookup"><span data-stu-id="4df3d-124">**src0 src1->**</span></span> | <span data-ttu-id="4df3d-125">**-INF**</span><span class="sxs-lookup"><span data-stu-id="4df3d-125">**-inf**</span></span> | <span data-ttu-id="4df3d-126">**-F**</span><span class="sxs-lookup"><span data-stu-id="4df3d-126">**-F**</span></span> | <span data-ttu-id="4df3d-127">**— 1,0**</span><span class="sxs-lookup"><span data-stu-id="4df3d-127">**-1.0**</span></span> | <span data-ttu-id="4df3d-128">**-0**</span><span class="sxs-lookup"><span data-stu-id="4df3d-128">**-0**</span></span> | <span data-ttu-id="4df3d-129">**+0**</span><span class="sxs-lookup"><span data-stu-id="4df3d-129">**+0**</span></span> | <span data-ttu-id="4df3d-130">**+ 1,0**</span><span class="sxs-lookup"><span data-stu-id="4df3d-130">**+1.0**</span></span> | <span data-ttu-id="4df3d-131">**+ F**</span><span class="sxs-lookup"><span data-stu-id="4df3d-131">**+F**</span></span> | <span data-ttu-id="4df3d-132">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="4df3d-132">**+inf**</span></span> | <span data-ttu-id="4df3d-133">**Не число**</span><span class="sxs-lookup"><span data-stu-id="4df3d-133">**NaN**</span></span> |
| <span data-ttu-id="4df3d-134">**-INF**</span><span class="sxs-lookup"><span data-stu-id="4df3d-134">**-inf**</span></span>           | <span data-ttu-id="4df3d-135">+inf</span><span class="sxs-lookup"><span data-stu-id="4df3d-135">+inf</span></span>     | <span data-ttu-id="4df3d-136">+inf</span><span class="sxs-lookup"><span data-stu-id="4df3d-136">+inf</span></span>   | <span data-ttu-id="4df3d-137">+inf</span><span class="sxs-lookup"><span data-stu-id="4df3d-137">+inf</span></span>     | <span data-ttu-id="4df3d-138">Не число</span><span class="sxs-lookup"><span data-stu-id="4df3d-138">NaN</span></span>    | <span data-ttu-id="4df3d-139">Не число</span><span class="sxs-lookup"><span data-stu-id="4df3d-139">NaN</span></span>    | <span data-ttu-id="4df3d-140">-inf</span><span class="sxs-lookup"><span data-stu-id="4df3d-140">-inf</span></span>     | <span data-ttu-id="4df3d-141">-inf</span><span class="sxs-lookup"><span data-stu-id="4df3d-141">-inf</span></span>   | <span data-ttu-id="4df3d-142">-inf</span><span class="sxs-lookup"><span data-stu-id="4df3d-142">-inf</span></span>     | <span data-ttu-id="4df3d-143">не число</span><span class="sxs-lookup"><span data-stu-id="4df3d-143">NaN</span></span>     |
| <span data-ttu-id="4df3d-144">**-F**</span><span class="sxs-lookup"><span data-stu-id="4df3d-144">**-F**</span></span>             | <span data-ttu-id="4df3d-145">+inf</span><span class="sxs-lookup"><span data-stu-id="4df3d-145">+inf</span></span>     | <span data-ttu-id="4df3d-146">+ F</span><span class="sxs-lookup"><span data-stu-id="4df3d-146">+F</span></span>     | <span data-ttu-id="4df3d-147">-src0</span><span class="sxs-lookup"><span data-stu-id="4df3d-147">-src0</span></span>    | <span data-ttu-id="4df3d-148">+0</span><span class="sxs-lookup"><span data-stu-id="4df3d-148">+0</span></span>     | <span data-ttu-id="4df3d-149">-0</span><span class="sxs-lookup"><span data-stu-id="4df3d-149">-0</span></span>     | <span data-ttu-id="4df3d-150">src0</span><span class="sxs-lookup"><span data-stu-id="4df3d-150">src0</span></span>     | <span data-ttu-id="4df3d-151">-F</span><span class="sxs-lookup"><span data-stu-id="4df3d-151">-F</span></span>     | <span data-ttu-id="4df3d-152">-inf</span><span class="sxs-lookup"><span data-stu-id="4df3d-152">-inf</span></span>     | <span data-ttu-id="4df3d-153">не число</span><span class="sxs-lookup"><span data-stu-id="4df3d-153">NaN</span></span>     |
| <span data-ttu-id="4df3d-154">**-1.0 f**</span><span class="sxs-lookup"><span data-stu-id="4df3d-154">**-1.0F**</span></span>          | <span data-ttu-id="4df3d-155">+inf</span><span class="sxs-lookup"><span data-stu-id="4df3d-155">+inf</span></span>     | <span data-ttu-id="4df3d-156">-src1</span><span class="sxs-lookup"><span data-stu-id="4df3d-156">-src1</span></span>  | <span data-ttu-id="4df3d-157">+ 1,0</span><span class="sxs-lookup"><span data-stu-id="4df3d-157">+1.0</span></span>     | <span data-ttu-id="4df3d-158">+0</span><span class="sxs-lookup"><span data-stu-id="4df3d-158">+0</span></span>     | <span data-ttu-id="4df3d-159">-0</span><span class="sxs-lookup"><span data-stu-id="4df3d-159">-0</span></span>     | <span data-ttu-id="4df3d-160">-1.0</span><span class="sxs-lookup"><span data-stu-id="4df3d-160">-1.0</span></span>     | <span data-ttu-id="4df3d-161">-src1</span><span class="sxs-lookup"><span data-stu-id="4df3d-161">-src1</span></span>  | <span data-ttu-id="4df3d-162">-inf</span><span class="sxs-lookup"><span data-stu-id="4df3d-162">-inf</span></span>     | <span data-ttu-id="4df3d-163">Не число</span><span class="sxs-lookup"><span data-stu-id="4df3d-163">NaN</span></span>     |
| <span data-ttu-id="4df3d-164">**-0**</span><span class="sxs-lookup"><span data-stu-id="4df3d-164">**-0**</span></span>             | <span data-ttu-id="4df3d-165">Не число</span><span class="sxs-lookup"><span data-stu-id="4df3d-165">NaN</span></span>      | <span data-ttu-id="4df3d-166">+0</span><span class="sxs-lookup"><span data-stu-id="4df3d-166">+0</span></span>     | <span data-ttu-id="4df3d-167">+0</span><span class="sxs-lookup"><span data-stu-id="4df3d-167">+0</span></span>       | <span data-ttu-id="4df3d-168">+0</span><span class="sxs-lookup"><span data-stu-id="4df3d-168">+0</span></span>     | <span data-ttu-id="4df3d-169">-0</span><span class="sxs-lookup"><span data-stu-id="4df3d-169">-0</span></span>     | <span data-ttu-id="4df3d-170">-0</span><span class="sxs-lookup"><span data-stu-id="4df3d-170">-0</span></span>       | <span data-ttu-id="4df3d-171">-0</span><span class="sxs-lookup"><span data-stu-id="4df3d-171">-0</span></span>     | <span data-ttu-id="4df3d-172">Не число</span><span class="sxs-lookup"><span data-stu-id="4df3d-172">NaN</span></span>      | <span data-ttu-id="4df3d-173">Не число</span><span class="sxs-lookup"><span data-stu-id="4df3d-173">NaN</span></span>     |
| <span data-ttu-id="4df3d-174">**+0**</span><span class="sxs-lookup"><span data-stu-id="4df3d-174">**+0**</span></span>             | <span data-ttu-id="4df3d-175">Не число</span><span class="sxs-lookup"><span data-stu-id="4df3d-175">NaN</span></span>      | <span data-ttu-id="4df3d-176">-0</span><span class="sxs-lookup"><span data-stu-id="4df3d-176">-0</span></span>     | <span data-ttu-id="4df3d-177">-0</span><span class="sxs-lookup"><span data-stu-id="4df3d-177">-0</span></span>       | <span data-ttu-id="4df3d-178">-0</span><span class="sxs-lookup"><span data-stu-id="4df3d-178">-0</span></span>     | <span data-ttu-id="4df3d-179">+0</span><span class="sxs-lookup"><span data-stu-id="4df3d-179">+0</span></span>     | <span data-ttu-id="4df3d-180">+0</span><span class="sxs-lookup"><span data-stu-id="4df3d-180">+0</span></span>       | <span data-ttu-id="4df3d-181">+0</span><span class="sxs-lookup"><span data-stu-id="4df3d-181">+0</span></span>     | <span data-ttu-id="4df3d-182">Не число</span><span class="sxs-lookup"><span data-stu-id="4df3d-182">NaN</span></span>      | <span data-ttu-id="4df3d-183">Не число</span><span class="sxs-lookup"><span data-stu-id="4df3d-183">NaN</span></span>     |
| <span data-ttu-id="4df3d-184">**+ 1,0**</span><span class="sxs-lookup"><span data-stu-id="4df3d-184">**+1.0**</span></span>           | <span data-ttu-id="4df3d-185">-inf</span><span class="sxs-lookup"><span data-stu-id="4df3d-185">-inf</span></span>     | <span data-ttu-id="4df3d-186">src1</span><span class="sxs-lookup"><span data-stu-id="4df3d-186">src1</span></span>   | <span data-ttu-id="4df3d-187">-1.0</span><span class="sxs-lookup"><span data-stu-id="4df3d-187">-1.0</span></span>     | <span data-ttu-id="4df3d-188">-0</span><span class="sxs-lookup"><span data-stu-id="4df3d-188">-0</span></span>     | <span data-ttu-id="4df3d-189">+0</span><span class="sxs-lookup"><span data-stu-id="4df3d-189">+0</span></span>     | <span data-ttu-id="4df3d-190">+1</span><span class="sxs-lookup"><span data-stu-id="4df3d-190">+1</span></span>       | <span data-ttu-id="4df3d-191">src1</span><span class="sxs-lookup"><span data-stu-id="4df3d-191">src1</span></span>   | <span data-ttu-id="4df3d-192">+inf</span><span class="sxs-lookup"><span data-stu-id="4df3d-192">+inf</span></span>     | <span data-ttu-id="4df3d-193">не число</span><span class="sxs-lookup"><span data-stu-id="4df3d-193">NaN</span></span>     |
| <span data-ttu-id="4df3d-194">**+ F**</span><span class="sxs-lookup"><span data-stu-id="4df3d-194">**+F**</span></span>             | <span data-ttu-id="4df3d-195">-inf</span><span class="sxs-lookup"><span data-stu-id="4df3d-195">-inf</span></span>     | <span data-ttu-id="4df3d-196">-F</span><span class="sxs-lookup"><span data-stu-id="4df3d-196">-F</span></span>     | <span data-ttu-id="4df3d-197">-src0</span><span class="sxs-lookup"><span data-stu-id="4df3d-197">-src0</span></span>    | <span data-ttu-id="4df3d-198">-0</span><span class="sxs-lookup"><span data-stu-id="4df3d-198">-0</span></span>     | <span data-ttu-id="4df3d-199">+0</span><span class="sxs-lookup"><span data-stu-id="4df3d-199">+0</span></span>     | <span data-ttu-id="4df3d-200">src0</span><span class="sxs-lookup"><span data-stu-id="4df3d-200">src0</span></span>     | <span data-ttu-id="4df3d-201">+ F</span><span class="sxs-lookup"><span data-stu-id="4df3d-201">+F</span></span>     | <span data-ttu-id="4df3d-202">+inf</span><span class="sxs-lookup"><span data-stu-id="4df3d-202">+inf</span></span>     | <span data-ttu-id="4df3d-203">не число</span><span class="sxs-lookup"><span data-stu-id="4df3d-203">NaN</span></span>     |
| <span data-ttu-id="4df3d-204">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="4df3d-204">**+inf**</span></span>           | <span data-ttu-id="4df3d-205">-inf</span><span class="sxs-lookup"><span data-stu-id="4df3d-205">-inf</span></span>     | <span data-ttu-id="4df3d-206">-inf</span><span class="sxs-lookup"><span data-stu-id="4df3d-206">-inf</span></span>   | <span data-ttu-id="4df3d-207">-inf</span><span class="sxs-lookup"><span data-stu-id="4df3d-207">-inf</span></span>     | <span data-ttu-id="4df3d-208">Не число</span><span class="sxs-lookup"><span data-stu-id="4df3d-208">NaN</span></span>    | <span data-ttu-id="4df3d-209">Не число</span><span class="sxs-lookup"><span data-stu-id="4df3d-209">NaN</span></span>    | <span data-ttu-id="4df3d-210">+inf</span><span class="sxs-lookup"><span data-stu-id="4df3d-210">+inf</span></span>     | <span data-ttu-id="4df3d-211">+inf</span><span class="sxs-lookup"><span data-stu-id="4df3d-211">+inf</span></span>   | <span data-ttu-id="4df3d-212">+inf</span><span class="sxs-lookup"><span data-stu-id="4df3d-212">+inf</span></span>     | <span data-ttu-id="4df3d-213">Не число</span><span class="sxs-lookup"><span data-stu-id="4df3d-213">NaN</span></span>     |
| <span data-ttu-id="4df3d-214">**Не число**</span><span class="sxs-lookup"><span data-stu-id="4df3d-214">**NaN**</span></span>            | <span data-ttu-id="4df3d-215">Не число</span><span class="sxs-lookup"><span data-stu-id="4df3d-215">NaN</span></span>      | <span data-ttu-id="4df3d-216">Не число</span><span class="sxs-lookup"><span data-stu-id="4df3d-216">NaN</span></span>    | <span data-ttu-id="4df3d-217">Не число</span><span class="sxs-lookup"><span data-stu-id="4df3d-217">NaN</span></span>      | <span data-ttu-id="4df3d-218">Не число</span><span class="sxs-lookup"><span data-stu-id="4df3d-218">NaN</span></span>    | <span data-ttu-id="4df3d-219">Не число</span><span class="sxs-lookup"><span data-stu-id="4df3d-219">NaN</span></span>    | <span data-ttu-id="4df3d-220">Не число</span><span class="sxs-lookup"><span data-stu-id="4df3d-220">NaN</span></span>      | <span data-ttu-id="4df3d-221">Не число</span><span class="sxs-lookup"><span data-stu-id="4df3d-221">NaN</span></span>    | <span data-ttu-id="4df3d-222">Не число</span><span class="sxs-lookup"><span data-stu-id="4df3d-222">NaN</span></span>      | <span data-ttu-id="4df3d-223">Не число</span><span class="sxs-lookup"><span data-stu-id="4df3d-223">NaN</span></span>     |



 

<span data-ttu-id="4df3d-224">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="4df3d-224">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="4df3d-225">Вершина</span><span class="sxs-lookup"><span data-stu-id="4df3d-225">Vertex</span></span> | <span data-ttu-id="4df3d-226">Поверхности</span><span class="sxs-lookup"><span data-stu-id="4df3d-226">Hull</span></span> | <span data-ttu-id="4df3d-227">Домен</span><span class="sxs-lookup"><span data-stu-id="4df3d-227">Domain</span></span> | <span data-ttu-id="4df3d-228">Геометрия</span><span class="sxs-lookup"><span data-stu-id="4df3d-228">Geometry</span></span> | <span data-ttu-id="4df3d-229">Пиксель</span><span class="sxs-lookup"><span data-stu-id="4df3d-229">Pixel</span></span> | <span data-ttu-id="4df3d-230">Вычисления</span><span class="sxs-lookup"><span data-stu-id="4df3d-230">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="4df3d-231">X</span><span class="sxs-lookup"><span data-stu-id="4df3d-231">X</span></span>      | <span data-ttu-id="4df3d-232">X</span><span class="sxs-lookup"><span data-stu-id="4df3d-232">X</span></span>    | <span data-ttu-id="4df3d-233">X</span><span class="sxs-lookup"><span data-stu-id="4df3d-233">X</span></span>      | <span data-ttu-id="4df3d-234">X</span><span class="sxs-lookup"><span data-stu-id="4df3d-234">X</span></span>        | <span data-ttu-id="4df3d-235">X</span><span class="sxs-lookup"><span data-stu-id="4df3d-235">X</span></span>     | <span data-ttu-id="4df3d-236">X</span><span class="sxs-lookup"><span data-stu-id="4df3d-236">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4df3d-237">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="4df3d-237">Minimum Shader Model</span></span>

<span data-ttu-id="4df3d-238">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="4df3d-238">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="4df3d-239">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="4df3d-239">Shader Model</span></span>                                              | <span data-ttu-id="4df3d-240">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="4df3d-240">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="4df3d-241">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="4df3d-241">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="4df3d-242">да</span><span class="sxs-lookup"><span data-stu-id="4df3d-242">yes</span></span>       |
| [<span data-ttu-id="4df3d-243">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="4df3d-243">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="4df3d-244">Нет</span><span class="sxs-lookup"><span data-stu-id="4df3d-244">no</span></span>        |
| [<span data-ttu-id="4df3d-245">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="4df3d-245">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4df3d-246">Нет</span><span class="sxs-lookup"><span data-stu-id="4df3d-246">no</span></span>        |
| [<span data-ttu-id="4df3d-247">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4df3d-247">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4df3d-248">Нет</span><span class="sxs-lookup"><span data-stu-id="4df3d-248">no</span></span>        |
| [<span data-ttu-id="4df3d-249">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4df3d-249">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4df3d-250">Нет</span><span class="sxs-lookup"><span data-stu-id="4df3d-250">no</span></span>        |
| [<span data-ttu-id="4df3d-251">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4df3d-251">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4df3d-252">Нет</span><span class="sxs-lookup"><span data-stu-id="4df3d-252">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="4df3d-253">См. также</span><span class="sxs-lookup"><span data-stu-id="4df3d-253">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4df3d-254">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4df3d-254">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





