---
title: Add (SM4-ASM)
description: Компонентно-ориентированное добавление двух векторов.
ms.assetid: 405A513C-B2DD-43B9-A86D-1D173B084C51
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e34f0a95ad9ee9ae4bdeed317eef133e3773311
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994981"
---
# <a name="add-sm4---asm"></a><span data-ttu-id="b597c-103">Add (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="b597c-103">add (sm4 - asm)</span></span>

<span data-ttu-id="b597c-104">Компонентно-ориентированное добавление двух векторов.</span><span class="sxs-lookup"><span data-stu-id="b597c-104">Component-wise add of 2 vectors.</span></span>



| <span data-ttu-id="b597c-105">добавить \[ \_ адрес "Кот. \] Маска" \[ \] , \[ - \] src0 \[ \_ ABS. \] \[ свиззле \] , \[ - \] src1 \[ \_ ABS \] \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="b597c-105">add\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="b597c-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="b597c-106">Item</span></span>                                                            | <span data-ttu-id="b597c-107">Описание</span><span class="sxs-lookup"><span data-stu-id="b597c-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="b597c-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="b597c-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="b597c-109">\[в \] адресе результата операции.</span><span class="sxs-lookup"><span data-stu-id="b597c-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="b597c-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="b597c-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="b597c-111">\[в \] векторе, добавляемом в *src1*.</span><span class="sxs-lookup"><span data-stu-id="b597c-111">\[in\] The vector to add to *src1*.</span></span><br/>                |
| <span data-ttu-id="b597c-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="b597c-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="b597c-113">\[в \] векторе, добавляемом в *src0*.</span><span class="sxs-lookup"><span data-stu-id="b597c-113">\[in\] The vector to add to *src0*.</span></span><br/>                |



 

## <a name="remarks"></a><span data-ttu-id="b597c-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="b597c-114">Remarks</span></span>

<span data-ttu-id="b597c-115">В следующей таблице показаны результаты, полученные при выполнении инструкции с различными классами чисел, предполагая, что ни переполнение, ни потеря точности не происходит.</span><span class="sxs-lookup"><span data-stu-id="b597c-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="b597c-116">F означает конечное вещественное число.</span><span class="sxs-lookup"><span data-stu-id="b597c-116">F means finite real number.</span></span>



| <span data-ttu-id="b597c-117">**src0 src1 — >**</span><span class="sxs-lookup"><span data-stu-id="b597c-117">**src0 src1->**</span></span> | <span data-ttu-id="b597c-118">**-INF**</span><span class="sxs-lookup"><span data-stu-id="b597c-118">**-inf**</span></span> | <span data-ttu-id="b597c-119">**-F**</span><span class="sxs-lookup"><span data-stu-id="b597c-119">**-F**</span></span>     | <span data-ttu-id="b597c-120">**— денорма**</span><span class="sxs-lookup"><span data-stu-id="b597c-120">**-denorm**</span></span> | <span data-ttu-id="b597c-121">**-0**</span><span class="sxs-lookup"><span data-stu-id="b597c-121">**-0**</span></span> | <span data-ttu-id="b597c-122">**+0**</span><span class="sxs-lookup"><span data-stu-id="b597c-122">**+0**</span></span> | <span data-ttu-id="b597c-123">**денорма**</span><span class="sxs-lookup"><span data-stu-id="b597c-123">**denorm**</span></span> | <span data-ttu-id="b597c-124">**+ F**</span><span class="sxs-lookup"><span data-stu-id="b597c-124">**+F**</span></span>     | <span data-ttu-id="b597c-125">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="b597c-125">**+inf**</span></span> | <span data-ttu-id="b597c-126">**Не число**</span><span class="sxs-lookup"><span data-stu-id="b597c-126">**NaN**</span></span> |
|--------------------|----------|------------|-------------|--------|--------|------------|------------|----------|---------|
| <span data-ttu-id="b597c-127">**-INF**</span><span class="sxs-lookup"><span data-stu-id="b597c-127">**-inf**</span></span>           | <span data-ttu-id="b597c-128">-inf</span><span class="sxs-lookup"><span data-stu-id="b597c-128">-inf</span></span>     | <span data-ttu-id="b597c-129">-inf</span><span class="sxs-lookup"><span data-stu-id="b597c-129">-inf</span></span>       | <span data-ttu-id="b597c-130">-inf</span><span class="sxs-lookup"><span data-stu-id="b597c-130">-inf</span></span>        | <span data-ttu-id="b597c-131">-inf</span><span class="sxs-lookup"><span data-stu-id="b597c-131">-inf</span></span>   | <span data-ttu-id="b597c-132">-inf</span><span class="sxs-lookup"><span data-stu-id="b597c-132">-inf</span></span>   | <span data-ttu-id="b597c-133">-inf</span><span class="sxs-lookup"><span data-stu-id="b597c-133">-inf</span></span>       | <span data-ttu-id="b597c-134">-inf</span><span class="sxs-lookup"><span data-stu-id="b597c-134">-inf</span></span>       | <span data-ttu-id="b597c-135">Не число</span><span class="sxs-lookup"><span data-stu-id="b597c-135">NaN</span></span>      | <span data-ttu-id="b597c-136">Не число</span><span class="sxs-lookup"><span data-stu-id="b597c-136">NaN</span></span>     |
| <span data-ttu-id="b597c-137">**-F**</span><span class="sxs-lookup"><span data-stu-id="b597c-137">**-F**</span></span>             | <span data-ttu-id="b597c-138">-inf</span><span class="sxs-lookup"><span data-stu-id="b597c-138">-inf</span></span>     | <span data-ttu-id="b597c-139">-F</span><span class="sxs-lookup"><span data-stu-id="b597c-139">-F</span></span>         | <span data-ttu-id="b597c-140">src0</span><span class="sxs-lookup"><span data-stu-id="b597c-140">src0</span></span>        | <span data-ttu-id="b597c-141">src0</span><span class="sxs-lookup"><span data-stu-id="b597c-141">src0</span></span>   | <span data-ttu-id="b597c-142">src0</span><span class="sxs-lookup"><span data-stu-id="b597c-142">src0</span></span>   | <span data-ttu-id="b597c-143">src0</span><span class="sxs-lookup"><span data-stu-id="b597c-143">src0</span></span>       | <span data-ttu-id="b597c-144">+-F или +-0</span><span class="sxs-lookup"><span data-stu-id="b597c-144">+-F or +-0</span></span> | <span data-ttu-id="b597c-145">+inf</span><span class="sxs-lookup"><span data-stu-id="b597c-145">+inf</span></span>     | <span data-ttu-id="b597c-146">не число</span><span class="sxs-lookup"><span data-stu-id="b597c-146">NaN</span></span>     |
| <span data-ttu-id="b597c-147">**— денорма**</span><span class="sxs-lookup"><span data-stu-id="b597c-147">**-denorm**</span></span>        | <span data-ttu-id="b597c-148">-inf</span><span class="sxs-lookup"><span data-stu-id="b597c-148">-inf</span></span>     | <span data-ttu-id="b597c-149">src1</span><span class="sxs-lookup"><span data-stu-id="b597c-149">src1</span></span>       | <span data-ttu-id="b597c-150">-0</span><span class="sxs-lookup"><span data-stu-id="b597c-150">-0</span></span>          | <span data-ttu-id="b597c-151">-0</span><span class="sxs-lookup"><span data-stu-id="b597c-151">-0</span></span>     | <span data-ttu-id="b597c-152">+0</span><span class="sxs-lookup"><span data-stu-id="b597c-152">+0</span></span>     | <span data-ttu-id="b597c-153">+0</span><span class="sxs-lookup"><span data-stu-id="b597c-153">+0</span></span>         | <span data-ttu-id="b597c-154">src1</span><span class="sxs-lookup"><span data-stu-id="b597c-154">src1</span></span>       | <span data-ttu-id="b597c-155">+inf</span><span class="sxs-lookup"><span data-stu-id="b597c-155">+inf</span></span>     | <span data-ttu-id="b597c-156">Не число</span><span class="sxs-lookup"><span data-stu-id="b597c-156">NaN</span></span>     |
| <span data-ttu-id="b597c-157">**-0**</span><span class="sxs-lookup"><span data-stu-id="b597c-157">**-0**</span></span>             | <span data-ttu-id="b597c-158">-inf</span><span class="sxs-lookup"><span data-stu-id="b597c-158">-inf</span></span>     | <span data-ttu-id="b597c-159">src1</span><span class="sxs-lookup"><span data-stu-id="b597c-159">src1</span></span>       | <span data-ttu-id="b597c-160">-0</span><span class="sxs-lookup"><span data-stu-id="b597c-160">-0</span></span>          | <span data-ttu-id="b597c-161">-0</span><span class="sxs-lookup"><span data-stu-id="b597c-161">-0</span></span>     | <span data-ttu-id="b597c-162">+0</span><span class="sxs-lookup"><span data-stu-id="b597c-162">+0</span></span>     | <span data-ttu-id="b597c-163">+0</span><span class="sxs-lookup"><span data-stu-id="b597c-163">+0</span></span>         | <span data-ttu-id="b597c-164">src1</span><span class="sxs-lookup"><span data-stu-id="b597c-164">src1</span></span>       | <span data-ttu-id="b597c-165">+inf</span><span class="sxs-lookup"><span data-stu-id="b597c-165">+inf</span></span>     | <span data-ttu-id="b597c-166">Не число</span><span class="sxs-lookup"><span data-stu-id="b597c-166">NaN</span></span>     |
| <span data-ttu-id="b597c-167">**+0**</span><span class="sxs-lookup"><span data-stu-id="b597c-167">**+0**</span></span>             | <span data-ttu-id="b597c-168">i-INF</span><span class="sxs-lookup"><span data-stu-id="b597c-168">i-inf</span></span>    | <span data-ttu-id="b597c-169">src1</span><span class="sxs-lookup"><span data-stu-id="b597c-169">src1</span></span>       | <span data-ttu-id="b597c-170">+0</span><span class="sxs-lookup"><span data-stu-id="b597c-170">+0</span></span>          | <span data-ttu-id="b597c-171">+0</span><span class="sxs-lookup"><span data-stu-id="b597c-171">+0</span></span>     | <span data-ttu-id="b597c-172">+0</span><span class="sxs-lookup"><span data-stu-id="b597c-172">+0</span></span>     | <span data-ttu-id="b597c-173">+0</span><span class="sxs-lookup"><span data-stu-id="b597c-173">+0</span></span>         | <span data-ttu-id="b597c-174">src1</span><span class="sxs-lookup"><span data-stu-id="b597c-174">src1</span></span>       | <span data-ttu-id="b597c-175">+inf</span><span class="sxs-lookup"><span data-stu-id="b597c-175">+inf</span></span>     | <span data-ttu-id="b597c-176">не число</span><span class="sxs-lookup"><span data-stu-id="b597c-176">NaN</span></span>     |
| <span data-ttu-id="b597c-177">**+ денорма**</span><span class="sxs-lookup"><span data-stu-id="b597c-177">**+denorm**</span></span>        | <span data-ttu-id="b597c-178">-inf</span><span class="sxs-lookup"><span data-stu-id="b597c-178">-inf</span></span>     | <span data-ttu-id="b597c-179">src1</span><span class="sxs-lookup"><span data-stu-id="b597c-179">src1</span></span>       | <span data-ttu-id="b597c-180">+0</span><span class="sxs-lookup"><span data-stu-id="b597c-180">+0</span></span>          | <span data-ttu-id="b597c-181">+0</span><span class="sxs-lookup"><span data-stu-id="b597c-181">+0</span></span>     | <span data-ttu-id="b597c-182">+0</span><span class="sxs-lookup"><span data-stu-id="b597c-182">+0</span></span>     | <span data-ttu-id="b597c-183">+0</span><span class="sxs-lookup"><span data-stu-id="b597c-183">+0</span></span>         | <span data-ttu-id="b597c-184">src1</span><span class="sxs-lookup"><span data-stu-id="b597c-184">src1</span></span>       | <span data-ttu-id="b597c-185">+inf</span><span class="sxs-lookup"><span data-stu-id="b597c-185">+inf</span></span>     | <span data-ttu-id="b597c-186">не число</span><span class="sxs-lookup"><span data-stu-id="b597c-186">NaN</span></span>     |
| <span data-ttu-id="b597c-187">**+ F**</span><span class="sxs-lookup"><span data-stu-id="b597c-187">**+F**</span></span>             | <span data-ttu-id="b597c-188">-inf</span><span class="sxs-lookup"><span data-stu-id="b597c-188">-inf</span></span>     | <span data-ttu-id="b597c-189">+-F или +-0</span><span class="sxs-lookup"><span data-stu-id="b597c-189">+-F or +-0</span></span> | <span data-ttu-id="b597c-190">src0</span><span class="sxs-lookup"><span data-stu-id="b597c-190">src0</span></span>        | <span data-ttu-id="b597c-191">src0</span><span class="sxs-lookup"><span data-stu-id="b597c-191">src0</span></span>   | <span data-ttu-id="b597c-192">src0</span><span class="sxs-lookup"><span data-stu-id="b597c-192">src0</span></span>   | <span data-ttu-id="b597c-193">src0</span><span class="sxs-lookup"><span data-stu-id="b597c-193">src0</span></span>       | <span data-ttu-id="b597c-194">+ F</span><span class="sxs-lookup"><span data-stu-id="b597c-194">+F</span></span>         | <span data-ttu-id="b597c-195">+inf</span><span class="sxs-lookup"><span data-stu-id="b597c-195">+inf</span></span>     | <span data-ttu-id="b597c-196">не число</span><span class="sxs-lookup"><span data-stu-id="b597c-196">NaN</span></span>     |
| <span data-ttu-id="b597c-197">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="b597c-197">**+inf**</span></span>           | <span data-ttu-id="b597c-198">не число</span><span class="sxs-lookup"><span data-stu-id="b597c-198">NaN</span></span>      | <span data-ttu-id="b597c-199">+inf</span><span class="sxs-lookup"><span data-stu-id="b597c-199">+inf</span></span>       | <span data-ttu-id="b597c-200">+inf</span><span class="sxs-lookup"><span data-stu-id="b597c-200">+inf</span></span>        | <span data-ttu-id="b597c-201">+inf</span><span class="sxs-lookup"><span data-stu-id="b597c-201">+inf</span></span>   | <span data-ttu-id="b597c-202">+inf</span><span class="sxs-lookup"><span data-stu-id="b597c-202">+inf</span></span>   | <span data-ttu-id="b597c-203">+inf</span><span class="sxs-lookup"><span data-stu-id="b597c-203">+inf</span></span>       | <span data-ttu-id="b597c-204">+inf</span><span class="sxs-lookup"><span data-stu-id="b597c-204">+inf</span></span>       | <span data-ttu-id="b597c-205">+inf</span><span class="sxs-lookup"><span data-stu-id="b597c-205">+inf</span></span>     | <span data-ttu-id="b597c-206">Не число</span><span class="sxs-lookup"><span data-stu-id="b597c-206">NaN</span></span>     |
| <span data-ttu-id="b597c-207">**Не число**</span><span class="sxs-lookup"><span data-stu-id="b597c-207">**NaN**</span></span>            | <span data-ttu-id="b597c-208">Не число</span><span class="sxs-lookup"><span data-stu-id="b597c-208">NaN</span></span>      | <span data-ttu-id="b597c-209">Не число</span><span class="sxs-lookup"><span data-stu-id="b597c-209">NaN</span></span>        | <span data-ttu-id="b597c-210">Не число</span><span class="sxs-lookup"><span data-stu-id="b597c-210">NaN</span></span>         | <span data-ttu-id="b597c-211">Не число</span><span class="sxs-lookup"><span data-stu-id="b597c-211">NaN</span></span>    | <span data-ttu-id="b597c-212">Не число</span><span class="sxs-lookup"><span data-stu-id="b597c-212">NaN</span></span>    | <span data-ttu-id="b597c-213">Не число</span><span class="sxs-lookup"><span data-stu-id="b597c-213">NaN</span></span>        | <span data-ttu-id="b597c-214">Не число</span><span class="sxs-lookup"><span data-stu-id="b597c-214">NaN</span></span>        | <span data-ttu-id="b597c-215">Не число</span><span class="sxs-lookup"><span data-stu-id="b597c-215">NaN</span></span>      | <span data-ttu-id="b597c-216">Не число</span><span class="sxs-lookup"><span data-stu-id="b597c-216">NaN</span></span>     |



 

<span data-ttu-id="b597c-217">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="b597c-217">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b597c-218">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="b597c-218">Vertex Shader</span></span> | <span data-ttu-id="b597c-219">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="b597c-219">Geometry Shader</span></span> | <span data-ttu-id="b597c-220">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="b597c-220">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="b597c-221">x</span><span class="sxs-lookup"><span data-stu-id="b597c-221">x</span></span>             | <span data-ttu-id="b597c-222">x</span><span class="sxs-lookup"><span data-stu-id="b597c-222">x</span></span>               | <span data-ttu-id="b597c-223">x</span><span class="sxs-lookup"><span data-stu-id="b597c-223">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b597c-224">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="b597c-224">Minimum Shader Model</span></span>

<span data-ttu-id="b597c-225">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="b597c-225">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b597c-226">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="b597c-226">Shader Model</span></span>                                              | <span data-ttu-id="b597c-227">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="b597c-227">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b597c-228">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="b597c-228">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b597c-229">да</span><span class="sxs-lookup"><span data-stu-id="b597c-229">yes</span></span>       |
| [<span data-ttu-id="b597c-230">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="b597c-230">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b597c-231">да</span><span class="sxs-lookup"><span data-stu-id="b597c-231">yes</span></span>       |
| [<span data-ttu-id="b597c-232">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="b597c-232">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b597c-233">да</span><span class="sxs-lookup"><span data-stu-id="b597c-233">yes</span></span>       |
| [<span data-ttu-id="b597c-234">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b597c-234">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b597c-235">Нет</span><span class="sxs-lookup"><span data-stu-id="b597c-235">no</span></span>        |
| [<span data-ttu-id="b597c-236">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b597c-236">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b597c-237">Нет</span><span class="sxs-lookup"><span data-stu-id="b597c-237">no</span></span>        |
| [<span data-ttu-id="b597c-238">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b597c-238">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b597c-239">Нет</span><span class="sxs-lookup"><span data-stu-id="b597c-239">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b597c-240">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="b597c-240">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b597c-241">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b597c-241">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





