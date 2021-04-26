---
title: Div (SM4-ASM)
description: Деление на уровне компонентов.
ms.assetid: B086F069-8F43-4746-A6A5-8F4462212648
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d406c5e61b4615990b445abe169619227d22124c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999101"
---
# <a name="div-sm4---asm"></a><span data-ttu-id="23632-103">Div (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="23632-103">div (sm4 - asm)</span></span>

<span data-ttu-id="23632-104">Деление на уровне компонентов.</span><span class="sxs-lookup"><span data-stu-id="23632-104">Component-wise divide.</span></span>



| <span data-ttu-id="23632-105">Div \[ \_ Кот \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS. \] \[ свиззле \] \[ - \] src1 \[ \_ ABS \] \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="23632-105">div\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\] \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="23632-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="23632-106">Item</span></span>                                                            | <span data-ttu-id="23632-107">Описание</span><span class="sxs-lookup"><span data-stu-id="23632-107">Description</span></span>                                    |
|-----------------------------------------------------------------|------------------------------------------------|
| <span data-ttu-id="23632-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="23632-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="23632-109">\[в \] результате операции.</span><span class="sxs-lookup"><span data-stu-id="23632-109">\[in\] The result of the operation.</span></span><br/> |
| <span data-ttu-id="23632-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="23632-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="23632-111">\[в \] делимом.</span><span class="sxs-lookup"><span data-stu-id="23632-111">\[in\] The dividend.</span></span><br/>                |
| <span data-ttu-id="23632-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="23632-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="23632-113">\[в \] делителье.</span><span class="sxs-lookup"><span data-stu-id="23632-113">\[in\] The divisor.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="23632-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="23632-114">Remarks</span></span>

<span data-ttu-id="23632-115">В следующей таблице показаны результаты, полученные при выполнении инструкции с различными классами чисел, предполагая, что ни переполнение, ни потеря точности не происходит.</span><span class="sxs-lookup"><span data-stu-id="23632-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="23632-116">Обратите внимание на две допустимые реализации деления: a/b и a \* (1/b).</span><span class="sxs-lookup"><span data-stu-id="23632-116">You should note the two allowed implementations of divide: a/b and a\*(1/b).</span></span>

<span data-ttu-id="23632-117">Один из результатов заключается в том, что существуют исключения из таблицы ниже для значений больших знаменателей (больше 8.5070592 e + 37), где 1/знаменатель — это денорма.</span><span class="sxs-lookup"><span data-stu-id="23632-117">One outcome of this is that there are exceptions to the table below for large denominator values (greater than 8.5070592e+37), where 1/denominator is a denorm.</span></span> <span data-ttu-id="23632-118">Поскольку реализации могут выполнять деление как \* (1/b), вместо a/b напрямую, а 1/ \[ большое значение \] — это денорма, которая может быть очищена, в некоторых случаях в таблице могут возникать разные результаты.</span><span class="sxs-lookup"><span data-stu-id="23632-118">Because implementations may perform divide as a\*(1/b), instead of a/b directly, and 1/\[large value\] is a denorm that could get flushed, some cases in the table would produce different results.</span></span> <span data-ttu-id="23632-119">Например, значение (+/-) INF/(+/-) \[ > 8.5070592 e + 37 \] может возвращать NaN в некоторых реализациях, но (+/-) в других реализациях</span><span class="sxs-lookup"><span data-stu-id="23632-119">For example, (+/-)INF / (+/-)\[value > 8.5070592e+37\] may produce NaN on some implementations, but (+/-)INF on other implementations</span></span>

<span data-ttu-id="23632-120">В этой таблице F означает ограничение по настоящему вещественному числу.</span><span class="sxs-lookup"><span data-stu-id="23632-120">In this table F means finite-real number.</span></span>



| <span data-ttu-id="23632-121">**src0 src1 — >**</span><span class="sxs-lookup"><span data-stu-id="23632-121">**src0 src1 ->**</span></span> | <span data-ttu-id="23632-122">**-INF**</span><span class="sxs-lookup"><span data-stu-id="23632-122">**-inf**</span></span> | <span data-ttu-id="23632-123">**-F**</span><span class="sxs-lookup"><span data-stu-id="23632-123">**-F**</span></span>     | <span data-ttu-id="23632-124">**— денорма**</span><span class="sxs-lookup"><span data-stu-id="23632-124">**-denorm**</span></span> | <span data-ttu-id="23632-125">**-0**</span><span class="sxs-lookup"><span data-stu-id="23632-125">**-0**</span></span> | <span data-ttu-id="23632-126">**+0**</span><span class="sxs-lookup"><span data-stu-id="23632-126">**+0**</span></span> | <span data-ttu-id="23632-127">**+ денорма**</span><span class="sxs-lookup"><span data-stu-id="23632-127">**+denorm**</span></span> | <span data-ttu-id="23632-128">**+ F**</span><span class="sxs-lookup"><span data-stu-id="23632-128">**+F**</span></span>     | <span data-ttu-id="23632-129">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="23632-129">**+inf**</span></span> | <span data-ttu-id="23632-130">**NaN**</span><span class="sxs-lookup"><span data-stu-id="23632-130">**Nan**</span></span> |
|---------------------|----------|------------|-------------|--------|--------|-------------|------------|----------|---------|
| <span data-ttu-id="23632-131">**-INF**</span><span class="sxs-lookup"><span data-stu-id="23632-131">**-inf**</span></span>            | <span data-ttu-id="23632-132">-inf</span><span class="sxs-lookup"><span data-stu-id="23632-132">-inf</span></span>     | <span data-ttu-id="23632-133">-inf</span><span class="sxs-lookup"><span data-stu-id="23632-133">-inf</span></span>       | <span data-ttu-id="23632-134">-inf</span><span class="sxs-lookup"><span data-stu-id="23632-134">-inf</span></span>        | <span data-ttu-id="23632-135">-inf</span><span class="sxs-lookup"><span data-stu-id="23632-135">-inf</span></span>   | <span data-ttu-id="23632-136">-inf</span><span class="sxs-lookup"><span data-stu-id="23632-136">-inf</span></span>   | <span data-ttu-id="23632-137">-inf</span><span class="sxs-lookup"><span data-stu-id="23632-137">-inf</span></span>        | <span data-ttu-id="23632-138">-inf</span><span class="sxs-lookup"><span data-stu-id="23632-138">-inf</span></span>       | <span data-ttu-id="23632-139">Не число</span><span class="sxs-lookup"><span data-stu-id="23632-139">NaN</span></span>      | <span data-ttu-id="23632-140">Не число</span><span class="sxs-lookup"><span data-stu-id="23632-140">NaN</span></span>     |
| <span data-ttu-id="23632-141">**-F**</span><span class="sxs-lookup"><span data-stu-id="23632-141">**-F**</span></span>              | <span data-ttu-id="23632-142">-inf</span><span class="sxs-lookup"><span data-stu-id="23632-142">-inf</span></span>     | <span data-ttu-id="23632-143">-F</span><span class="sxs-lookup"><span data-stu-id="23632-143">-F</span></span>         | <span data-ttu-id="23632-144">src0</span><span class="sxs-lookup"><span data-stu-id="23632-144">src0</span></span>        | <span data-ttu-id="23632-145">src0</span><span class="sxs-lookup"><span data-stu-id="23632-145">src0</span></span>   | <span data-ttu-id="23632-146">src0</span><span class="sxs-lookup"><span data-stu-id="23632-146">src0</span></span>   | <span data-ttu-id="23632-147">src0</span><span class="sxs-lookup"><span data-stu-id="23632-147">src0</span></span>        | <span data-ttu-id="23632-148">+-F или +-0</span><span class="sxs-lookup"><span data-stu-id="23632-148">+-F or +-0</span></span> | <span data-ttu-id="23632-149">+inf</span><span class="sxs-lookup"><span data-stu-id="23632-149">+inf</span></span>     | <span data-ttu-id="23632-150">не число</span><span class="sxs-lookup"><span data-stu-id="23632-150">NaN</span></span>     |
| <span data-ttu-id="23632-151">**— денорма**</span><span class="sxs-lookup"><span data-stu-id="23632-151">**-denorm**</span></span>         | <span data-ttu-id="23632-152">-inf</span><span class="sxs-lookup"><span data-stu-id="23632-152">-inf</span></span>     | <span data-ttu-id="23632-153">src1</span><span class="sxs-lookup"><span data-stu-id="23632-153">src1</span></span>       | <span data-ttu-id="23632-154">-0</span><span class="sxs-lookup"><span data-stu-id="23632-154">-0</span></span>          | <span data-ttu-id="23632-155">-0</span><span class="sxs-lookup"><span data-stu-id="23632-155">-0</span></span>     | <span data-ttu-id="23632-156">+0</span><span class="sxs-lookup"><span data-stu-id="23632-156">+0</span></span>     | <span data-ttu-id="23632-157">+0</span><span class="sxs-lookup"><span data-stu-id="23632-157">+0</span></span>          | <span data-ttu-id="23632-158">src1</span><span class="sxs-lookup"><span data-stu-id="23632-158">src1</span></span>       | <span data-ttu-id="23632-159">+inf</span><span class="sxs-lookup"><span data-stu-id="23632-159">+inf</span></span>     | <span data-ttu-id="23632-160">Не число</span><span class="sxs-lookup"><span data-stu-id="23632-160">NaN</span></span>     |
| <span data-ttu-id="23632-161">**-0**</span><span class="sxs-lookup"><span data-stu-id="23632-161">**-0**</span></span>              | <span data-ttu-id="23632-162">-inf</span><span class="sxs-lookup"><span data-stu-id="23632-162">-inf</span></span>     | <span data-ttu-id="23632-163">src1</span><span class="sxs-lookup"><span data-stu-id="23632-163">src1</span></span>       | <span data-ttu-id="23632-164">-0</span><span class="sxs-lookup"><span data-stu-id="23632-164">-0</span></span>          | <span data-ttu-id="23632-165">-0</span><span class="sxs-lookup"><span data-stu-id="23632-165">-0</span></span>     | <span data-ttu-id="23632-166">+0</span><span class="sxs-lookup"><span data-stu-id="23632-166">+0</span></span>     | <span data-ttu-id="23632-167">+0</span><span class="sxs-lookup"><span data-stu-id="23632-167">+0</span></span>          | <span data-ttu-id="23632-168">src1</span><span class="sxs-lookup"><span data-stu-id="23632-168">src1</span></span>       | <span data-ttu-id="23632-169">+inf</span><span class="sxs-lookup"><span data-stu-id="23632-169">+inf</span></span>     | <span data-ttu-id="23632-170">Не число</span><span class="sxs-lookup"><span data-stu-id="23632-170">NaN</span></span>     |
| <span data-ttu-id="23632-171">**+0**</span><span class="sxs-lookup"><span data-stu-id="23632-171">**+0**</span></span>              | <span data-ttu-id="23632-172">-inf</span><span class="sxs-lookup"><span data-stu-id="23632-172">-inf</span></span>     | <span data-ttu-id="23632-173">src1</span><span class="sxs-lookup"><span data-stu-id="23632-173">src1</span></span>       | <span data-ttu-id="23632-174">+0</span><span class="sxs-lookup"><span data-stu-id="23632-174">+0</span></span>          | <span data-ttu-id="23632-175">+0</span><span class="sxs-lookup"><span data-stu-id="23632-175">+0</span></span>     | <span data-ttu-id="23632-176">+0</span><span class="sxs-lookup"><span data-stu-id="23632-176">+0</span></span>     | <span data-ttu-id="23632-177">+0</span><span class="sxs-lookup"><span data-stu-id="23632-177">+0</span></span>          | <span data-ttu-id="23632-178">src1</span><span class="sxs-lookup"><span data-stu-id="23632-178">src1</span></span>       | <span data-ttu-id="23632-179">+inf</span><span class="sxs-lookup"><span data-stu-id="23632-179">+inf</span></span>     | <span data-ttu-id="23632-180">не число</span><span class="sxs-lookup"><span data-stu-id="23632-180">NaN</span></span>     |
| <span data-ttu-id="23632-181">**+ денорма**</span><span class="sxs-lookup"><span data-stu-id="23632-181">**+denorm**</span></span>         | <span data-ttu-id="23632-182">-inf</span><span class="sxs-lookup"><span data-stu-id="23632-182">-inf</span></span>     | <span data-ttu-id="23632-183">src1</span><span class="sxs-lookup"><span data-stu-id="23632-183">src1</span></span>       | <span data-ttu-id="23632-184">+0</span><span class="sxs-lookup"><span data-stu-id="23632-184">+0</span></span>          | <span data-ttu-id="23632-185">+0</span><span class="sxs-lookup"><span data-stu-id="23632-185">+0</span></span>     | <span data-ttu-id="23632-186">+0</span><span class="sxs-lookup"><span data-stu-id="23632-186">+0</span></span>     | <span data-ttu-id="23632-187">+0</span><span class="sxs-lookup"><span data-stu-id="23632-187">+0</span></span>          | <span data-ttu-id="23632-188">src1</span><span class="sxs-lookup"><span data-stu-id="23632-188">src1</span></span>       | <span data-ttu-id="23632-189">+inf</span><span class="sxs-lookup"><span data-stu-id="23632-189">+inf</span></span>     | <span data-ttu-id="23632-190">не число</span><span class="sxs-lookup"><span data-stu-id="23632-190">NaN</span></span>     |
| <span data-ttu-id="23632-191">**+ F**</span><span class="sxs-lookup"><span data-stu-id="23632-191">**+F**</span></span>              | <span data-ttu-id="23632-192">-inf</span><span class="sxs-lookup"><span data-stu-id="23632-192">-inf</span></span>     | <span data-ttu-id="23632-193">+-F или +-0</span><span class="sxs-lookup"><span data-stu-id="23632-193">+-F or +-0</span></span> | <span data-ttu-id="23632-194">src0</span><span class="sxs-lookup"><span data-stu-id="23632-194">src0</span></span>        | <span data-ttu-id="23632-195">src0</span><span class="sxs-lookup"><span data-stu-id="23632-195">src0</span></span>   | <span data-ttu-id="23632-196">src0</span><span class="sxs-lookup"><span data-stu-id="23632-196">src0</span></span>   | <span data-ttu-id="23632-197">src0</span><span class="sxs-lookup"><span data-stu-id="23632-197">src0</span></span>        | <span data-ttu-id="23632-198">+ F</span><span class="sxs-lookup"><span data-stu-id="23632-198">+F</span></span>         | <span data-ttu-id="23632-199">+inf</span><span class="sxs-lookup"><span data-stu-id="23632-199">+inf</span></span>     | <span data-ttu-id="23632-200">не число</span><span class="sxs-lookup"><span data-stu-id="23632-200">NaN</span></span>     |
| <span data-ttu-id="23632-201">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="23632-201">**+inf**</span></span>            | <span data-ttu-id="23632-202">не число</span><span class="sxs-lookup"><span data-stu-id="23632-202">NaN</span></span>      | <span data-ttu-id="23632-203">+inf</span><span class="sxs-lookup"><span data-stu-id="23632-203">+inf</span></span>       | <span data-ttu-id="23632-204">+inf</span><span class="sxs-lookup"><span data-stu-id="23632-204">+inf</span></span>        | <span data-ttu-id="23632-205">+inf</span><span class="sxs-lookup"><span data-stu-id="23632-205">+inf</span></span>   | <span data-ttu-id="23632-206">+inf</span><span class="sxs-lookup"><span data-stu-id="23632-206">+inf</span></span>   | <span data-ttu-id="23632-207">+inf</span><span class="sxs-lookup"><span data-stu-id="23632-207">+inf</span></span>        | <span data-ttu-id="23632-208">+inf</span><span class="sxs-lookup"><span data-stu-id="23632-208">+inf</span></span>       | <span data-ttu-id="23632-209">+inf</span><span class="sxs-lookup"><span data-stu-id="23632-209">+inf</span></span>     | <span data-ttu-id="23632-210">Не число</span><span class="sxs-lookup"><span data-stu-id="23632-210">NaN</span></span>     |
| <span data-ttu-id="23632-211">**Не число**</span><span class="sxs-lookup"><span data-stu-id="23632-211">**NaN**</span></span>             | <span data-ttu-id="23632-212">Не число</span><span class="sxs-lookup"><span data-stu-id="23632-212">NaN</span></span>      | <span data-ttu-id="23632-213">Не число</span><span class="sxs-lookup"><span data-stu-id="23632-213">NaN</span></span>        | <span data-ttu-id="23632-214">Не число</span><span class="sxs-lookup"><span data-stu-id="23632-214">NaN</span></span>         | <span data-ttu-id="23632-215">Не число</span><span class="sxs-lookup"><span data-stu-id="23632-215">NaN</span></span>    | <span data-ttu-id="23632-216">Не число</span><span class="sxs-lookup"><span data-stu-id="23632-216">NaN</span></span>    | <span data-ttu-id="23632-217">Не число</span><span class="sxs-lookup"><span data-stu-id="23632-217">NaN</span></span>         | <span data-ttu-id="23632-218">Не число</span><span class="sxs-lookup"><span data-stu-id="23632-218">NaN</span></span>        | <span data-ttu-id="23632-219">Не число</span><span class="sxs-lookup"><span data-stu-id="23632-219">NaN</span></span>      | <span data-ttu-id="23632-220">Не число</span><span class="sxs-lookup"><span data-stu-id="23632-220">NaN</span></span>     |



 

<span data-ttu-id="23632-221">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="23632-221">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="23632-222">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="23632-222">Vertex Shader</span></span> | <span data-ttu-id="23632-223">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="23632-223">Geometry Shader</span></span> | <span data-ttu-id="23632-224">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="23632-224">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="23632-225">x</span><span class="sxs-lookup"><span data-stu-id="23632-225">x</span></span>             | <span data-ttu-id="23632-226">x</span><span class="sxs-lookup"><span data-stu-id="23632-226">x</span></span>               | <span data-ttu-id="23632-227">x</span><span class="sxs-lookup"><span data-stu-id="23632-227">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="23632-228">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="23632-228">Minimum Shader Model</span></span>

<span data-ttu-id="23632-229">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="23632-229">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="23632-230">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="23632-230">Shader Model</span></span>                                              | <span data-ttu-id="23632-231">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="23632-231">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="23632-232">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="23632-232">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="23632-233">да</span><span class="sxs-lookup"><span data-stu-id="23632-233">yes</span></span>       |
| [<span data-ttu-id="23632-234">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="23632-234">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="23632-235">да</span><span class="sxs-lookup"><span data-stu-id="23632-235">yes</span></span>       |
| [<span data-ttu-id="23632-236">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="23632-236">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="23632-237">да</span><span class="sxs-lookup"><span data-stu-id="23632-237">yes</span></span>       |
| [<span data-ttu-id="23632-238">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="23632-238">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="23632-239">Нет</span><span class="sxs-lookup"><span data-stu-id="23632-239">no</span></span>        |
| [<span data-ttu-id="23632-240">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="23632-240">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="23632-241">Нет</span><span class="sxs-lookup"><span data-stu-id="23632-241">no</span></span>        |
| [<span data-ttu-id="23632-242">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="23632-242">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="23632-243">Нет</span><span class="sxs-lookup"><span data-stu-id="23632-243">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="23632-244">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="23632-244">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23632-245">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="23632-245">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





