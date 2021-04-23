---
title: Add (SM4-ASM)
description: Компонентно-ориентированное добавление двух векторов.
ms.assetid: 405A513C-B2DD-43B9-A86D-1D173B084C51
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5630b983c88da3ba512b5fece6202e0217b2ed39
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104532891"
---
# <a name="add-sm4---asm"></a><span data-ttu-id="fee3d-103">Add (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="fee3d-103">add (sm4 - asm)</span></span>

<span data-ttu-id="fee3d-104">Компонентно-ориентированное добавление двух векторов.</span><span class="sxs-lookup"><span data-stu-id="fee3d-104">Component-wise add of 2 vectors.</span></span>



| <span data-ttu-id="fee3d-105">добавить \[ \_ адрес "Кот. \] Маска" \[ \] , \[ - \] src0 \[ \_ ABS. \] \[ свиззле \] , \[ - \] src1 \[ \_ ABS \] \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="fee3d-105">add\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="fee3d-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="fee3d-106">Item</span></span>                                                            | <span data-ttu-id="fee3d-107">Описание</span><span class="sxs-lookup"><span data-stu-id="fee3d-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="fee3d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="fee3d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="fee3d-109">\[в \] адресе результата операции.</span><span class="sxs-lookup"><span data-stu-id="fee3d-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="fee3d-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="fee3d-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="fee3d-111">\[в \] векторе, добавляемом в *src1*.</span><span class="sxs-lookup"><span data-stu-id="fee3d-111">\[in\] The vector to add to *src1*.</span></span><br/>                |
| <span data-ttu-id="fee3d-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="fee3d-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="fee3d-113">\[в \] векторе, добавляемом в *src0*.</span><span class="sxs-lookup"><span data-stu-id="fee3d-113">\[in\] The vector to add to *src0*.</span></span><br/>                |



 

## <a name="remarks"></a><span data-ttu-id="fee3d-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="fee3d-114">Remarks</span></span>

<span data-ttu-id="fee3d-115">В следующей таблице показаны результаты, полученные при выполнении инструкции с различными классами чисел, предполагая, что ни переполнение, ни потеря точности не происходит.</span><span class="sxs-lookup"><span data-stu-id="fee3d-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="fee3d-116">F означает конечное вещественное число.</span><span class="sxs-lookup"><span data-stu-id="fee3d-116">F means finite real number.</span></span>



|                    |          |            |             |        |        |            |            |          |         |
|--------------------|----------|------------|-------------|--------|--------|------------|------------|----------|---------|
| <span data-ttu-id="fee3d-117">**src0 src1 — >**</span><span class="sxs-lookup"><span data-stu-id="fee3d-117">**src0 src1->**</span></span> | <span data-ttu-id="fee3d-118">**-INF**</span><span class="sxs-lookup"><span data-stu-id="fee3d-118">**-inf**</span></span> | <span data-ttu-id="fee3d-119">**-F**</span><span class="sxs-lookup"><span data-stu-id="fee3d-119">**-F**</span></span>     | <span data-ttu-id="fee3d-120">**— денорма**</span><span class="sxs-lookup"><span data-stu-id="fee3d-120">**-denorm**</span></span> | <span data-ttu-id="fee3d-121">**-0**</span><span class="sxs-lookup"><span data-stu-id="fee3d-121">**-0**</span></span> | <span data-ttu-id="fee3d-122">**+0**</span><span class="sxs-lookup"><span data-stu-id="fee3d-122">**+0**</span></span> | <span data-ttu-id="fee3d-123">**денорма**</span><span class="sxs-lookup"><span data-stu-id="fee3d-123">**denorm**</span></span> | <span data-ttu-id="fee3d-124">**+ F**</span><span class="sxs-lookup"><span data-stu-id="fee3d-124">**+F**</span></span>     | <span data-ttu-id="fee3d-125">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="fee3d-125">**+inf**</span></span> | <span data-ttu-id="fee3d-126">**Не число**</span><span class="sxs-lookup"><span data-stu-id="fee3d-126">**NaN**</span></span> |
| <span data-ttu-id="fee3d-127">**-INF**</span><span class="sxs-lookup"><span data-stu-id="fee3d-127">**-inf**</span></span>           | <span data-ttu-id="fee3d-128">-inf</span><span class="sxs-lookup"><span data-stu-id="fee3d-128">-inf</span></span>     | <span data-ttu-id="fee3d-129">-inf</span><span class="sxs-lookup"><span data-stu-id="fee3d-129">-inf</span></span>       | <span data-ttu-id="fee3d-130">-inf</span><span class="sxs-lookup"><span data-stu-id="fee3d-130">-inf</span></span>        | <span data-ttu-id="fee3d-131">-inf</span><span class="sxs-lookup"><span data-stu-id="fee3d-131">-inf</span></span>   | <span data-ttu-id="fee3d-132">-inf</span><span class="sxs-lookup"><span data-stu-id="fee3d-132">-inf</span></span>   | <span data-ttu-id="fee3d-133">-inf</span><span class="sxs-lookup"><span data-stu-id="fee3d-133">-inf</span></span>       | <span data-ttu-id="fee3d-134">-inf</span><span class="sxs-lookup"><span data-stu-id="fee3d-134">-inf</span></span>       | <span data-ttu-id="fee3d-135">Не число</span><span class="sxs-lookup"><span data-stu-id="fee3d-135">NaN</span></span>      | <span data-ttu-id="fee3d-136">Не число</span><span class="sxs-lookup"><span data-stu-id="fee3d-136">NaN</span></span>     |
| <span data-ttu-id="fee3d-137">**-F**</span><span class="sxs-lookup"><span data-stu-id="fee3d-137">**-F**</span></span>             | <span data-ttu-id="fee3d-138">-inf</span><span class="sxs-lookup"><span data-stu-id="fee3d-138">-inf</span></span>     | <span data-ttu-id="fee3d-139">-F</span><span class="sxs-lookup"><span data-stu-id="fee3d-139">-F</span></span>         | <span data-ttu-id="fee3d-140">src0</span><span class="sxs-lookup"><span data-stu-id="fee3d-140">src0</span></span>        | <span data-ttu-id="fee3d-141">src0</span><span class="sxs-lookup"><span data-stu-id="fee3d-141">src0</span></span>   | <span data-ttu-id="fee3d-142">src0</span><span class="sxs-lookup"><span data-stu-id="fee3d-142">src0</span></span>   | <span data-ttu-id="fee3d-143">src0</span><span class="sxs-lookup"><span data-stu-id="fee3d-143">src0</span></span>       | <span data-ttu-id="fee3d-144">+-F или +-0</span><span class="sxs-lookup"><span data-stu-id="fee3d-144">+-F or +-0</span></span> | <span data-ttu-id="fee3d-145">+inf</span><span class="sxs-lookup"><span data-stu-id="fee3d-145">+inf</span></span>     | <span data-ttu-id="fee3d-146">не число</span><span class="sxs-lookup"><span data-stu-id="fee3d-146">NaN</span></span>     |
| <span data-ttu-id="fee3d-147">**— денорма**</span><span class="sxs-lookup"><span data-stu-id="fee3d-147">**-denorm**</span></span>        | <span data-ttu-id="fee3d-148">-inf</span><span class="sxs-lookup"><span data-stu-id="fee3d-148">-inf</span></span>     | <span data-ttu-id="fee3d-149">src1</span><span class="sxs-lookup"><span data-stu-id="fee3d-149">src1</span></span>       | <span data-ttu-id="fee3d-150">-0</span><span class="sxs-lookup"><span data-stu-id="fee3d-150">-0</span></span>          | <span data-ttu-id="fee3d-151">-0</span><span class="sxs-lookup"><span data-stu-id="fee3d-151">-0</span></span>     | <span data-ttu-id="fee3d-152">+0</span><span class="sxs-lookup"><span data-stu-id="fee3d-152">+0</span></span>     | <span data-ttu-id="fee3d-153">+0</span><span class="sxs-lookup"><span data-stu-id="fee3d-153">+0</span></span>         | <span data-ttu-id="fee3d-154">src1</span><span class="sxs-lookup"><span data-stu-id="fee3d-154">src1</span></span>       | <span data-ttu-id="fee3d-155">+inf</span><span class="sxs-lookup"><span data-stu-id="fee3d-155">+inf</span></span>     | <span data-ttu-id="fee3d-156">Не число</span><span class="sxs-lookup"><span data-stu-id="fee3d-156">NaN</span></span>     |
| <span data-ttu-id="fee3d-157">**-0**</span><span class="sxs-lookup"><span data-stu-id="fee3d-157">**-0**</span></span>             | <span data-ttu-id="fee3d-158">-inf</span><span class="sxs-lookup"><span data-stu-id="fee3d-158">-inf</span></span>     | <span data-ttu-id="fee3d-159">src1</span><span class="sxs-lookup"><span data-stu-id="fee3d-159">src1</span></span>       | <span data-ttu-id="fee3d-160">-0</span><span class="sxs-lookup"><span data-stu-id="fee3d-160">-0</span></span>          | <span data-ttu-id="fee3d-161">-0</span><span class="sxs-lookup"><span data-stu-id="fee3d-161">-0</span></span>     | <span data-ttu-id="fee3d-162">+0</span><span class="sxs-lookup"><span data-stu-id="fee3d-162">+0</span></span>     | <span data-ttu-id="fee3d-163">+0</span><span class="sxs-lookup"><span data-stu-id="fee3d-163">+0</span></span>         | <span data-ttu-id="fee3d-164">src1</span><span class="sxs-lookup"><span data-stu-id="fee3d-164">src1</span></span>       | <span data-ttu-id="fee3d-165">+inf</span><span class="sxs-lookup"><span data-stu-id="fee3d-165">+inf</span></span>     | <span data-ttu-id="fee3d-166">Не число</span><span class="sxs-lookup"><span data-stu-id="fee3d-166">NaN</span></span>     |
| <span data-ttu-id="fee3d-167">**+0**</span><span class="sxs-lookup"><span data-stu-id="fee3d-167">**+0**</span></span>             | <span data-ttu-id="fee3d-168">i-INF</span><span class="sxs-lookup"><span data-stu-id="fee3d-168">i-inf</span></span>    | <span data-ttu-id="fee3d-169">src1</span><span class="sxs-lookup"><span data-stu-id="fee3d-169">src1</span></span>       | <span data-ttu-id="fee3d-170">+0</span><span class="sxs-lookup"><span data-stu-id="fee3d-170">+0</span></span>          | <span data-ttu-id="fee3d-171">+0</span><span class="sxs-lookup"><span data-stu-id="fee3d-171">+0</span></span>     | <span data-ttu-id="fee3d-172">+0</span><span class="sxs-lookup"><span data-stu-id="fee3d-172">+0</span></span>     | <span data-ttu-id="fee3d-173">+0</span><span class="sxs-lookup"><span data-stu-id="fee3d-173">+0</span></span>         | <span data-ttu-id="fee3d-174">src1</span><span class="sxs-lookup"><span data-stu-id="fee3d-174">src1</span></span>       | <span data-ttu-id="fee3d-175">+inf</span><span class="sxs-lookup"><span data-stu-id="fee3d-175">+inf</span></span>     | <span data-ttu-id="fee3d-176">не число</span><span class="sxs-lookup"><span data-stu-id="fee3d-176">NaN</span></span>     |
| <span data-ttu-id="fee3d-177">**+ денорма**</span><span class="sxs-lookup"><span data-stu-id="fee3d-177">**+denorm**</span></span>        | <span data-ttu-id="fee3d-178">-inf</span><span class="sxs-lookup"><span data-stu-id="fee3d-178">-inf</span></span>     | <span data-ttu-id="fee3d-179">src1</span><span class="sxs-lookup"><span data-stu-id="fee3d-179">src1</span></span>       | <span data-ttu-id="fee3d-180">+0</span><span class="sxs-lookup"><span data-stu-id="fee3d-180">+0</span></span>          | <span data-ttu-id="fee3d-181">+0</span><span class="sxs-lookup"><span data-stu-id="fee3d-181">+0</span></span>     | <span data-ttu-id="fee3d-182">+0</span><span class="sxs-lookup"><span data-stu-id="fee3d-182">+0</span></span>     | <span data-ttu-id="fee3d-183">+0</span><span class="sxs-lookup"><span data-stu-id="fee3d-183">+0</span></span>         | <span data-ttu-id="fee3d-184">src1</span><span class="sxs-lookup"><span data-stu-id="fee3d-184">src1</span></span>       | <span data-ttu-id="fee3d-185">+inf</span><span class="sxs-lookup"><span data-stu-id="fee3d-185">+inf</span></span>     | <span data-ttu-id="fee3d-186">не число</span><span class="sxs-lookup"><span data-stu-id="fee3d-186">NaN</span></span>     |
| <span data-ttu-id="fee3d-187">**+ F**</span><span class="sxs-lookup"><span data-stu-id="fee3d-187">**+F**</span></span>             | <span data-ttu-id="fee3d-188">-inf</span><span class="sxs-lookup"><span data-stu-id="fee3d-188">-inf</span></span>     | <span data-ttu-id="fee3d-189">+-F или +-0</span><span class="sxs-lookup"><span data-stu-id="fee3d-189">+-F or +-0</span></span> | <span data-ttu-id="fee3d-190">src0</span><span class="sxs-lookup"><span data-stu-id="fee3d-190">src0</span></span>        | <span data-ttu-id="fee3d-191">src0</span><span class="sxs-lookup"><span data-stu-id="fee3d-191">src0</span></span>   | <span data-ttu-id="fee3d-192">src0</span><span class="sxs-lookup"><span data-stu-id="fee3d-192">src0</span></span>   | <span data-ttu-id="fee3d-193">src0</span><span class="sxs-lookup"><span data-stu-id="fee3d-193">src0</span></span>       | <span data-ttu-id="fee3d-194">+ F</span><span class="sxs-lookup"><span data-stu-id="fee3d-194">+F</span></span>         | <span data-ttu-id="fee3d-195">+inf</span><span class="sxs-lookup"><span data-stu-id="fee3d-195">+inf</span></span>     | <span data-ttu-id="fee3d-196">не число</span><span class="sxs-lookup"><span data-stu-id="fee3d-196">NaN</span></span>     |
| <span data-ttu-id="fee3d-197">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="fee3d-197">**+inf**</span></span>           | <span data-ttu-id="fee3d-198">не число</span><span class="sxs-lookup"><span data-stu-id="fee3d-198">NaN</span></span>      | <span data-ttu-id="fee3d-199">+inf</span><span class="sxs-lookup"><span data-stu-id="fee3d-199">+inf</span></span>       | <span data-ttu-id="fee3d-200">+inf</span><span class="sxs-lookup"><span data-stu-id="fee3d-200">+inf</span></span>        | <span data-ttu-id="fee3d-201">+inf</span><span class="sxs-lookup"><span data-stu-id="fee3d-201">+inf</span></span>   | <span data-ttu-id="fee3d-202">+inf</span><span class="sxs-lookup"><span data-stu-id="fee3d-202">+inf</span></span>   | <span data-ttu-id="fee3d-203">+inf</span><span class="sxs-lookup"><span data-stu-id="fee3d-203">+inf</span></span>       | <span data-ttu-id="fee3d-204">+inf</span><span class="sxs-lookup"><span data-stu-id="fee3d-204">+inf</span></span>       | <span data-ttu-id="fee3d-205">+inf</span><span class="sxs-lookup"><span data-stu-id="fee3d-205">+inf</span></span>     | <span data-ttu-id="fee3d-206">Не число</span><span class="sxs-lookup"><span data-stu-id="fee3d-206">NaN</span></span>     |
| <span data-ttu-id="fee3d-207">**Не число**</span><span class="sxs-lookup"><span data-stu-id="fee3d-207">**NaN**</span></span>            | <span data-ttu-id="fee3d-208">Не число</span><span class="sxs-lookup"><span data-stu-id="fee3d-208">NaN</span></span>      | <span data-ttu-id="fee3d-209">Не число</span><span class="sxs-lookup"><span data-stu-id="fee3d-209">NaN</span></span>        | <span data-ttu-id="fee3d-210">Не число</span><span class="sxs-lookup"><span data-stu-id="fee3d-210">NaN</span></span>         | <span data-ttu-id="fee3d-211">Не число</span><span class="sxs-lookup"><span data-stu-id="fee3d-211">NaN</span></span>    | <span data-ttu-id="fee3d-212">Не число</span><span class="sxs-lookup"><span data-stu-id="fee3d-212">NaN</span></span>    | <span data-ttu-id="fee3d-213">Не число</span><span class="sxs-lookup"><span data-stu-id="fee3d-213">NaN</span></span>        | <span data-ttu-id="fee3d-214">Не число</span><span class="sxs-lookup"><span data-stu-id="fee3d-214">NaN</span></span>        | <span data-ttu-id="fee3d-215">Не число</span><span class="sxs-lookup"><span data-stu-id="fee3d-215">NaN</span></span>      | <span data-ttu-id="fee3d-216">Не число</span><span class="sxs-lookup"><span data-stu-id="fee3d-216">NaN</span></span>     |



 

<span data-ttu-id="fee3d-217">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="fee3d-217">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="fee3d-218">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="fee3d-218">Vertex Shader</span></span> | <span data-ttu-id="fee3d-219">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="fee3d-219">Geometry Shader</span></span> | <span data-ttu-id="fee3d-220">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="fee3d-220">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="fee3d-221">x</span><span class="sxs-lookup"><span data-stu-id="fee3d-221">x</span></span>             | <span data-ttu-id="fee3d-222">x</span><span class="sxs-lookup"><span data-stu-id="fee3d-222">x</span></span>               | <span data-ttu-id="fee3d-223">x</span><span class="sxs-lookup"><span data-stu-id="fee3d-223">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="fee3d-224">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="fee3d-224">Minimum Shader Model</span></span>

<span data-ttu-id="fee3d-225">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="fee3d-225">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="fee3d-226">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="fee3d-226">Shader Model</span></span>                                              | <span data-ttu-id="fee3d-227">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="fee3d-227">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="fee3d-228">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="fee3d-228">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="fee3d-229">да</span><span class="sxs-lookup"><span data-stu-id="fee3d-229">yes</span></span>       |
| [<span data-ttu-id="fee3d-230">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="fee3d-230">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="fee3d-231">да</span><span class="sxs-lookup"><span data-stu-id="fee3d-231">yes</span></span>       |
| [<span data-ttu-id="fee3d-232">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="fee3d-232">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="fee3d-233">да</span><span class="sxs-lookup"><span data-stu-id="fee3d-233">yes</span></span>       |
| [<span data-ttu-id="fee3d-234">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fee3d-234">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="fee3d-235">Нет</span><span class="sxs-lookup"><span data-stu-id="fee3d-235">no</span></span>        |
| [<span data-ttu-id="fee3d-236">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fee3d-236">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="fee3d-237">Нет</span><span class="sxs-lookup"><span data-stu-id="fee3d-237">no</span></span>        |
| [<span data-ttu-id="fee3d-238">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fee3d-238">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="fee3d-239">Нет</span><span class="sxs-lookup"><span data-stu-id="fee3d-239">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="fee3d-240">См. также</span><span class="sxs-lookup"><span data-stu-id="fee3d-240">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fee3d-241">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fee3d-241">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





