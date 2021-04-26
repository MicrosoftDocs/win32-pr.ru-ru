---
title: дмул (SM5-ASM)
description: Возведение двойной точности на уровне компонентов.
ms.assetid: 53AE27BE-2F4B-4C55-B496-D7122C00DC52
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a5d311cb5c958e8b7403197027c9854d1a93a64
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999091"
---
# <a name="dmul-sm5---asm"></a><span data-ttu-id="96de0-103">дмул (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="96de0-103">dmul (sm5 - asm)</span></span>

<span data-ttu-id="96de0-104">Возведение двойной точности на уровне компонентов.</span><span class="sxs-lookup"><span data-stu-id="96de0-104">Component-wise double-precision multiply.</span></span>



| <span data-ttu-id="96de0-105">дмул \[ \_ \] \[ . Маска \] , \[ - \] src0 \[ \_ ABS \] \[ . свиззле \] , \[ - \] src1 \[ \_ ABS \] \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="96de0-105">dmul\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="96de0-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="96de0-106">Item</span></span>                                                            | <span data-ttu-id="96de0-107">Описание</span><span class="sxs-lookup"><span data-stu-id="96de0-107">Description</span></span>                                                                                        |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96de0-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="96de0-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="96de0-109">\[в \] адресе результата операции.</span><span class="sxs-lookup"><span data-stu-id="96de0-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="96de0-110">*конечный адрес*  =  *src0* \* *src1*</span><span class="sxs-lookup"><span data-stu-id="96de0-110">*dest* = *src0* \* *src1*</span></span><br/> |
| <span data-ttu-id="96de0-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="96de0-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="96de0-112">\[в \] компонентах для перемножения с *src1*.</span><span class="sxs-lookup"><span data-stu-id="96de0-112">\[in\] The components to multiply with *src1*.</span></span><br/>                                          |
| <span data-ttu-id="96de0-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="96de0-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="96de0-114">\[в \] компонентах для перемножения с *src0*.</span><span class="sxs-lookup"><span data-stu-id="96de0-114">\[in\] The components to multiply with *src0*.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="96de0-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="96de0-115">Remarks</span></span>

<span data-ttu-id="96de0-116">Допустимыми свиззлес для параметров источника являются. ксизв,. ксикси,. звкси,. звзв.</span><span class="sxs-lookup"><span data-stu-id="96de0-116">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="96de0-117">Допустимые маски *приемников* : XY, ZW и. ксизв.</span><span class="sxs-lookup"><span data-stu-id="96de0-117">The valid *dest* masks are .xy, .zw, and .xyzw.</span></span> <span data-ttu-id="96de0-118">Следующие сопоставления *src* — это POST-свиззле:</span><span class="sxs-lookup"><span data-stu-id="96de0-118">The following *src* mappings are post-swizzle:</span></span>

-   <span data-ttu-id="96de0-119">*dest* — это двойное vec2 в (x 32LSB, y 32MSB) и (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="96de0-119">*dest* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="96de0-120">*src0* — это двойное vec2 в (x 32LSB, y 32MSB) и (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="96de0-120">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="96de0-121">*src1* — это двойное vec2 в (x 32LSB, y 32MSB) и (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="96de0-121">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="96de0-122">В следующей таблице показаны результаты, полученные при выполнении инструкции с различными классами чисел, предполагая, что ни переполнение, ни потеря точности не происходит.</span><span class="sxs-lookup"><span data-stu-id="96de0-122">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="96de0-123">F означает ограничение по настоящему вещественному числу.</span><span class="sxs-lookup"><span data-stu-id="96de0-123">F means finite-real number.</span></span>



| <span data-ttu-id="96de0-124">**src0 src1 — >**</span><span class="sxs-lookup"><span data-stu-id="96de0-124">**src0 src1->**</span></span> | <span data-ttu-id="96de0-125">**-INF**</span><span class="sxs-lookup"><span data-stu-id="96de0-125">**-inf**</span></span> | <span data-ttu-id="96de0-126">**-F**</span><span class="sxs-lookup"><span data-stu-id="96de0-126">**-F**</span></span> | <span data-ttu-id="96de0-127">**— 1,0**</span><span class="sxs-lookup"><span data-stu-id="96de0-127">**-1.0**</span></span> | <span data-ttu-id="96de0-128">**-0**</span><span class="sxs-lookup"><span data-stu-id="96de0-128">**-0**</span></span> | <span data-ttu-id="96de0-129">**+0**</span><span class="sxs-lookup"><span data-stu-id="96de0-129">**+0**</span></span> | <span data-ttu-id="96de0-130">**+ 1,0**</span><span class="sxs-lookup"><span data-stu-id="96de0-130">**+1.0**</span></span> | <span data-ttu-id="96de0-131">**+ F**</span><span class="sxs-lookup"><span data-stu-id="96de0-131">**+F**</span></span> | <span data-ttu-id="96de0-132">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="96de0-132">**+inf**</span></span> | <span data-ttu-id="96de0-133">**Не число**</span><span class="sxs-lookup"><span data-stu-id="96de0-133">**NaN**</span></span> |
|--------------------|----------|--------|----------|--------|--------|----------|--------|----------|---------|
| <span data-ttu-id="96de0-134">**-INF**</span><span class="sxs-lookup"><span data-stu-id="96de0-134">**-inf**</span></span>           | <span data-ttu-id="96de0-135">+inf</span><span class="sxs-lookup"><span data-stu-id="96de0-135">+inf</span></span>     | <span data-ttu-id="96de0-136">+inf</span><span class="sxs-lookup"><span data-stu-id="96de0-136">+inf</span></span>   | <span data-ttu-id="96de0-137">+inf</span><span class="sxs-lookup"><span data-stu-id="96de0-137">+inf</span></span>     | <span data-ttu-id="96de0-138">Не число</span><span class="sxs-lookup"><span data-stu-id="96de0-138">NaN</span></span>    | <span data-ttu-id="96de0-139">Не число</span><span class="sxs-lookup"><span data-stu-id="96de0-139">NaN</span></span>    | <span data-ttu-id="96de0-140">-inf</span><span class="sxs-lookup"><span data-stu-id="96de0-140">-inf</span></span>     | <span data-ttu-id="96de0-141">-inf</span><span class="sxs-lookup"><span data-stu-id="96de0-141">-inf</span></span>   | <span data-ttu-id="96de0-142">-inf</span><span class="sxs-lookup"><span data-stu-id="96de0-142">-inf</span></span>     | <span data-ttu-id="96de0-143">не число</span><span class="sxs-lookup"><span data-stu-id="96de0-143">NaN</span></span>     |
| <span data-ttu-id="96de0-144">**-F**</span><span class="sxs-lookup"><span data-stu-id="96de0-144">**-F**</span></span>             | <span data-ttu-id="96de0-145">+inf</span><span class="sxs-lookup"><span data-stu-id="96de0-145">+inf</span></span>     | <span data-ttu-id="96de0-146">+ F</span><span class="sxs-lookup"><span data-stu-id="96de0-146">+F</span></span>     | <span data-ttu-id="96de0-147">-src0</span><span class="sxs-lookup"><span data-stu-id="96de0-147">-src0</span></span>    | <span data-ttu-id="96de0-148">+0</span><span class="sxs-lookup"><span data-stu-id="96de0-148">+0</span></span>     | <span data-ttu-id="96de0-149">-0</span><span class="sxs-lookup"><span data-stu-id="96de0-149">-0</span></span>     | <span data-ttu-id="96de0-150">src0</span><span class="sxs-lookup"><span data-stu-id="96de0-150">src0</span></span>     | <span data-ttu-id="96de0-151">-F</span><span class="sxs-lookup"><span data-stu-id="96de0-151">-F</span></span>     | <span data-ttu-id="96de0-152">-inf</span><span class="sxs-lookup"><span data-stu-id="96de0-152">-inf</span></span>     | <span data-ttu-id="96de0-153">не число</span><span class="sxs-lookup"><span data-stu-id="96de0-153">NaN</span></span>     |
| <span data-ttu-id="96de0-154">**-1.0 f**</span><span class="sxs-lookup"><span data-stu-id="96de0-154">**-1.0F**</span></span>          | <span data-ttu-id="96de0-155">+inf</span><span class="sxs-lookup"><span data-stu-id="96de0-155">+inf</span></span>     | <span data-ttu-id="96de0-156">-src1</span><span class="sxs-lookup"><span data-stu-id="96de0-156">-src1</span></span>  | <span data-ttu-id="96de0-157">+ 1,0</span><span class="sxs-lookup"><span data-stu-id="96de0-157">+1.0</span></span>     | <span data-ttu-id="96de0-158">+0</span><span class="sxs-lookup"><span data-stu-id="96de0-158">+0</span></span>     | <span data-ttu-id="96de0-159">-0</span><span class="sxs-lookup"><span data-stu-id="96de0-159">-0</span></span>     | <span data-ttu-id="96de0-160">-1.0</span><span class="sxs-lookup"><span data-stu-id="96de0-160">-1.0</span></span>     | <span data-ttu-id="96de0-161">-src1</span><span class="sxs-lookup"><span data-stu-id="96de0-161">-src1</span></span>  | <span data-ttu-id="96de0-162">-inf</span><span class="sxs-lookup"><span data-stu-id="96de0-162">-inf</span></span>     | <span data-ttu-id="96de0-163">Не число</span><span class="sxs-lookup"><span data-stu-id="96de0-163">NaN</span></span>     |
| <span data-ttu-id="96de0-164">**-0**</span><span class="sxs-lookup"><span data-stu-id="96de0-164">**-0**</span></span>             | <span data-ttu-id="96de0-165">Не число</span><span class="sxs-lookup"><span data-stu-id="96de0-165">NaN</span></span>      | <span data-ttu-id="96de0-166">+0</span><span class="sxs-lookup"><span data-stu-id="96de0-166">+0</span></span>     | <span data-ttu-id="96de0-167">+0</span><span class="sxs-lookup"><span data-stu-id="96de0-167">+0</span></span>       | <span data-ttu-id="96de0-168">+0</span><span class="sxs-lookup"><span data-stu-id="96de0-168">+0</span></span>     | <span data-ttu-id="96de0-169">-0</span><span class="sxs-lookup"><span data-stu-id="96de0-169">-0</span></span>     | <span data-ttu-id="96de0-170">-0</span><span class="sxs-lookup"><span data-stu-id="96de0-170">-0</span></span>       | <span data-ttu-id="96de0-171">-0</span><span class="sxs-lookup"><span data-stu-id="96de0-171">-0</span></span>     | <span data-ttu-id="96de0-172">Не число</span><span class="sxs-lookup"><span data-stu-id="96de0-172">NaN</span></span>      | <span data-ttu-id="96de0-173">Не число</span><span class="sxs-lookup"><span data-stu-id="96de0-173">NaN</span></span>     |
| <span data-ttu-id="96de0-174">**+0**</span><span class="sxs-lookup"><span data-stu-id="96de0-174">**+0**</span></span>             | <span data-ttu-id="96de0-175">Не число</span><span class="sxs-lookup"><span data-stu-id="96de0-175">NaN</span></span>      | <span data-ttu-id="96de0-176">-0</span><span class="sxs-lookup"><span data-stu-id="96de0-176">-0</span></span>     | <span data-ttu-id="96de0-177">-0</span><span class="sxs-lookup"><span data-stu-id="96de0-177">-0</span></span>       | <span data-ttu-id="96de0-178">-0</span><span class="sxs-lookup"><span data-stu-id="96de0-178">-0</span></span>     | <span data-ttu-id="96de0-179">+0</span><span class="sxs-lookup"><span data-stu-id="96de0-179">+0</span></span>     | <span data-ttu-id="96de0-180">+0</span><span class="sxs-lookup"><span data-stu-id="96de0-180">+0</span></span>       | <span data-ttu-id="96de0-181">+0</span><span class="sxs-lookup"><span data-stu-id="96de0-181">+0</span></span>     | <span data-ttu-id="96de0-182">Не число</span><span class="sxs-lookup"><span data-stu-id="96de0-182">NaN</span></span>      | <span data-ttu-id="96de0-183">Не число</span><span class="sxs-lookup"><span data-stu-id="96de0-183">NaN</span></span>     |
| <span data-ttu-id="96de0-184">**+ 1,0**</span><span class="sxs-lookup"><span data-stu-id="96de0-184">**+1.0**</span></span>           | <span data-ttu-id="96de0-185">-inf</span><span class="sxs-lookup"><span data-stu-id="96de0-185">-inf</span></span>     | <span data-ttu-id="96de0-186">src1</span><span class="sxs-lookup"><span data-stu-id="96de0-186">src1</span></span>   | <span data-ttu-id="96de0-187">-1.0</span><span class="sxs-lookup"><span data-stu-id="96de0-187">-1.0</span></span>     | <span data-ttu-id="96de0-188">-0</span><span class="sxs-lookup"><span data-stu-id="96de0-188">-0</span></span>     | <span data-ttu-id="96de0-189">+0</span><span class="sxs-lookup"><span data-stu-id="96de0-189">+0</span></span>     | <span data-ttu-id="96de0-190">+1</span><span class="sxs-lookup"><span data-stu-id="96de0-190">+1</span></span>       | <span data-ttu-id="96de0-191">src1</span><span class="sxs-lookup"><span data-stu-id="96de0-191">src1</span></span>   | <span data-ttu-id="96de0-192">+inf</span><span class="sxs-lookup"><span data-stu-id="96de0-192">+inf</span></span>     | <span data-ttu-id="96de0-193">не число</span><span class="sxs-lookup"><span data-stu-id="96de0-193">NaN</span></span>     |
| <span data-ttu-id="96de0-194">**+ F**</span><span class="sxs-lookup"><span data-stu-id="96de0-194">**+F**</span></span>             | <span data-ttu-id="96de0-195">-inf</span><span class="sxs-lookup"><span data-stu-id="96de0-195">-inf</span></span>     | <span data-ttu-id="96de0-196">-F</span><span class="sxs-lookup"><span data-stu-id="96de0-196">-F</span></span>     | <span data-ttu-id="96de0-197">-src0</span><span class="sxs-lookup"><span data-stu-id="96de0-197">-src0</span></span>    | <span data-ttu-id="96de0-198">-0</span><span class="sxs-lookup"><span data-stu-id="96de0-198">-0</span></span>     | <span data-ttu-id="96de0-199">+0</span><span class="sxs-lookup"><span data-stu-id="96de0-199">+0</span></span>     | <span data-ttu-id="96de0-200">src0</span><span class="sxs-lookup"><span data-stu-id="96de0-200">src0</span></span>     | <span data-ttu-id="96de0-201">+ F</span><span class="sxs-lookup"><span data-stu-id="96de0-201">+F</span></span>     | <span data-ttu-id="96de0-202">+inf</span><span class="sxs-lookup"><span data-stu-id="96de0-202">+inf</span></span>     | <span data-ttu-id="96de0-203">не число</span><span class="sxs-lookup"><span data-stu-id="96de0-203">NaN</span></span>     |
| <span data-ttu-id="96de0-204">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="96de0-204">**+inf**</span></span>           | <span data-ttu-id="96de0-205">-inf</span><span class="sxs-lookup"><span data-stu-id="96de0-205">-inf</span></span>     | <span data-ttu-id="96de0-206">-inf</span><span class="sxs-lookup"><span data-stu-id="96de0-206">-inf</span></span>   | <span data-ttu-id="96de0-207">-inf</span><span class="sxs-lookup"><span data-stu-id="96de0-207">-inf</span></span>     | <span data-ttu-id="96de0-208">Не число</span><span class="sxs-lookup"><span data-stu-id="96de0-208">NaN</span></span>    | <span data-ttu-id="96de0-209">Не число</span><span class="sxs-lookup"><span data-stu-id="96de0-209">NaN</span></span>    | <span data-ttu-id="96de0-210">+inf</span><span class="sxs-lookup"><span data-stu-id="96de0-210">+inf</span></span>     | <span data-ttu-id="96de0-211">+inf</span><span class="sxs-lookup"><span data-stu-id="96de0-211">+inf</span></span>   | <span data-ttu-id="96de0-212">+inf</span><span class="sxs-lookup"><span data-stu-id="96de0-212">+inf</span></span>     | <span data-ttu-id="96de0-213">Не число</span><span class="sxs-lookup"><span data-stu-id="96de0-213">NaN</span></span>     |
| <span data-ttu-id="96de0-214">**Не число**</span><span class="sxs-lookup"><span data-stu-id="96de0-214">**NaN**</span></span>            | <span data-ttu-id="96de0-215">Не число</span><span class="sxs-lookup"><span data-stu-id="96de0-215">NaN</span></span>      | <span data-ttu-id="96de0-216">Не число</span><span class="sxs-lookup"><span data-stu-id="96de0-216">NaN</span></span>    | <span data-ttu-id="96de0-217">Не число</span><span class="sxs-lookup"><span data-stu-id="96de0-217">NaN</span></span>      | <span data-ttu-id="96de0-218">Не число</span><span class="sxs-lookup"><span data-stu-id="96de0-218">NaN</span></span>    | <span data-ttu-id="96de0-219">Не число</span><span class="sxs-lookup"><span data-stu-id="96de0-219">NaN</span></span>    | <span data-ttu-id="96de0-220">Не число</span><span class="sxs-lookup"><span data-stu-id="96de0-220">NaN</span></span>      | <span data-ttu-id="96de0-221">Не число</span><span class="sxs-lookup"><span data-stu-id="96de0-221">NaN</span></span>    | <span data-ttu-id="96de0-222">Не число</span><span class="sxs-lookup"><span data-stu-id="96de0-222">NaN</span></span>      | <span data-ttu-id="96de0-223">Не число</span><span class="sxs-lookup"><span data-stu-id="96de0-223">NaN</span></span>     |



 

<span data-ttu-id="96de0-224">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="96de0-224">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="96de0-225">Вершина</span><span class="sxs-lookup"><span data-stu-id="96de0-225">Vertex</span></span> | <span data-ttu-id="96de0-226">Поверхности</span><span class="sxs-lookup"><span data-stu-id="96de0-226">Hull</span></span> | <span data-ttu-id="96de0-227">Домен</span><span class="sxs-lookup"><span data-stu-id="96de0-227">Domain</span></span> | <span data-ttu-id="96de0-228">Геометрия</span><span class="sxs-lookup"><span data-stu-id="96de0-228">Geometry</span></span> | <span data-ttu-id="96de0-229">Пиксель</span><span class="sxs-lookup"><span data-stu-id="96de0-229">Pixel</span></span> | <span data-ttu-id="96de0-230">Службы вычислений</span><span class="sxs-lookup"><span data-stu-id="96de0-230">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="96de0-231">X</span><span class="sxs-lookup"><span data-stu-id="96de0-231">X</span></span>      | <span data-ttu-id="96de0-232">X</span><span class="sxs-lookup"><span data-stu-id="96de0-232">X</span></span>    | <span data-ttu-id="96de0-233">X</span><span class="sxs-lookup"><span data-stu-id="96de0-233">X</span></span>      | <span data-ttu-id="96de0-234">X</span><span class="sxs-lookup"><span data-stu-id="96de0-234">X</span></span>        | <span data-ttu-id="96de0-235">X</span><span class="sxs-lookup"><span data-stu-id="96de0-235">X</span></span>     | <span data-ttu-id="96de0-236">X</span><span class="sxs-lookup"><span data-stu-id="96de0-236">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="96de0-237">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="96de0-237">Minimum Shader Model</span></span>

<span data-ttu-id="96de0-238">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="96de0-238">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="96de0-239">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="96de0-239">Shader Model</span></span>                                              | <span data-ttu-id="96de0-240">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="96de0-240">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="96de0-241">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="96de0-241">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="96de0-242">да</span><span class="sxs-lookup"><span data-stu-id="96de0-242">yes</span></span>       |
| [<span data-ttu-id="96de0-243">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="96de0-243">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="96de0-244">Нет</span><span class="sxs-lookup"><span data-stu-id="96de0-244">no</span></span>        |
| [<span data-ttu-id="96de0-245">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="96de0-245">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="96de0-246">Нет</span><span class="sxs-lookup"><span data-stu-id="96de0-246">no</span></span>        |
| [<span data-ttu-id="96de0-247">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="96de0-247">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="96de0-248">Нет</span><span class="sxs-lookup"><span data-stu-id="96de0-248">no</span></span>        |
| [<span data-ttu-id="96de0-249">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="96de0-249">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="96de0-250">Нет</span><span class="sxs-lookup"><span data-stu-id="96de0-250">no</span></span>        |
| [<span data-ttu-id="96de0-251">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="96de0-251">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="96de0-252">Нет</span><span class="sxs-lookup"><span data-stu-id="96de0-252">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="96de0-253">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="96de0-253">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96de0-254">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="96de0-254">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





