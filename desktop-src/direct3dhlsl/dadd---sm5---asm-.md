---
title: Дадд (SM5-ASM)
description: Добавление двойной точности с привязкум к компоненту.
ms.assetid: 416F1103-E27B-4AFC-9ED1-492FF8A93492
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e217a03a5ba9e4da0d365bbfd15e4283f1a69cb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412140"
---
# <a name="dadd-sm5---asm"></a><span data-ttu-id="9a21a-103">Дадд (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="9a21a-103">dadd (sm5 - asm)</span></span>

<span data-ttu-id="9a21a-104">Добавление двойной точности с привязкум к компоненту.</span><span class="sxs-lookup"><span data-stu-id="9a21a-104">Component-wise double-precision add.</span></span>



| <span data-ttu-id="9a21a-105">Дадд \[ \_ \] \[ . Маска \] , \[ - \] src0 \[ \_ ABS \] \[ . свиззле \] , \[ - \] src1 \[ \_ ABS \] \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="9a21a-105">dadd\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="9a21a-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="9a21a-106">Item</span></span>                                                            | <span data-ttu-id="9a21a-107">Описание</span><span class="sxs-lookup"><span data-stu-id="9a21a-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="9a21a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="9a21a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="9a21a-109">\[в \] адресе результата операции.</span><span class="sxs-lookup"><span data-stu-id="9a21a-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="9a21a-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="9a21a-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="9a21a-111">\[в \] компонентах, добавляемых с помощью *src1*.</span><span class="sxs-lookup"><span data-stu-id="9a21a-111">\[in\] The components to add with *src1*.</span></span><br/>          |
| <span data-ttu-id="9a21a-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="9a21a-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="9a21a-113">\[в \] компонентах, добавляемых с помощью *src0*</span><span class="sxs-lookup"><span data-stu-id="9a21a-113">\[in\] The components to add with *src0*</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="9a21a-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="9a21a-114">Remarks</span></span>

<span data-ttu-id="9a21a-115">Допустимыми свиззлес для параметров источника являются. ксизв,. ксикси,. звкси,. звзв.</span><span class="sxs-lookup"><span data-stu-id="9a21a-115">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="9a21a-116">Допустимые маски *приемников* : XY, ZW и. ксизв.</span><span class="sxs-lookup"><span data-stu-id="9a21a-116">The valid *dest* masks are .xy, .zw, and .xyzw.</span></span> <span data-ttu-id="9a21a-117">Следующие сопоставления являются свиззле.</span><span class="sxs-lookup"><span data-stu-id="9a21a-117">The following mappings are post-swizzle:</span></span>

-   <span data-ttu-id="9a21a-118">*dest* — это двойное vec2 в (x 32LSB, y 32MSB) и (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="9a21a-118">*dest* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="9a21a-119">*src0* — это двойное vec2 в (x 32LSB, y 32MSB) и (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="9a21a-119">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="9a21a-120">*src1* — это двойное vec2 в (x 32LSB, y 32MSB) и (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="9a21a-120">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="9a21a-121">В следующей таблице показаны результаты, полученные при выполнении инструкции с различными классами чисел, предполагая, что ни переполнение, ни потеря точности не происходит.</span><span class="sxs-lookup"><span data-stu-id="9a21a-121">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="9a21a-122">F означает ограничение по настоящему вещественному числу.</span><span class="sxs-lookup"><span data-stu-id="9a21a-122">F means finite-real number.</span></span>



<table>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="9a21a-123"><strong>src0</strong></span><span class="sxs-lookup"><span data-stu-id="9a21a-123"><strong>src0</strong></span></span><br /><span data-ttu-id="9a21a-124">
<strong>src1 — ></strong></span><span class="sxs-lookup"><span data-stu-id="9a21a-124">
<strong>src1-></strong></span></span><br />
</dl></td>
<td><span data-ttu-id="9a21a-125"><strong>-INF</strong></span><span class="sxs-lookup"><span data-stu-id="9a21a-125"><strong>-inf</strong></span></span></td>
<td><span data-ttu-id="9a21a-126"><strong>-F</strong></span><span class="sxs-lookup"><span data-stu-id="9a21a-126"><strong>-F</strong></span></span></td>
<td><span data-ttu-id="9a21a-127"><strong>-0</strong></span><span class="sxs-lookup"><span data-stu-id="9a21a-127"><strong>-0</strong></span></span></td>
<td><span data-ttu-id="9a21a-128"><strong>+0</strong></span><span class="sxs-lookup"><span data-stu-id="9a21a-128"><strong>+0</strong></span></span></td>
<td><span data-ttu-id="9a21a-129"><strong>+ F</strong></span><span class="sxs-lookup"><span data-stu-id="9a21a-129"><strong>+F</strong></span></span></td>
<td><span data-ttu-id="9a21a-130"><strong>+ INF</strong></span><span class="sxs-lookup"><span data-stu-id="9a21a-130"><strong>+inf</strong></span></span></td>
<td><span data-ttu-id="9a21a-131"><strong>Не число</strong></span><span class="sxs-lookup"><span data-stu-id="9a21a-131"><strong>NaN</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a21a-132"><strong>-INF</strong></span><span class="sxs-lookup"><span data-stu-id="9a21a-132"><strong>-inf</strong></span></span></td>
<td><span data-ttu-id="9a21a-133">-inf</span><span class="sxs-lookup"><span data-stu-id="9a21a-133">-inf</span></span></td>
<td><span data-ttu-id="9a21a-134">-inf</span><span class="sxs-lookup"><span data-stu-id="9a21a-134">-inf</span></span></td>
<td><span data-ttu-id="9a21a-135">-inf</span><span class="sxs-lookup"><span data-stu-id="9a21a-135">-inf</span></span></td>
<td><span data-ttu-id="9a21a-136">-inf</span><span class="sxs-lookup"><span data-stu-id="9a21a-136">-inf</span></span></td>
<td><span data-ttu-id="9a21a-137">-inf</span><span class="sxs-lookup"><span data-stu-id="9a21a-137">-inf</span></span></td>
<td><span data-ttu-id="9a21a-138">Не число</span><span class="sxs-lookup"><span data-stu-id="9a21a-138">NaN</span></span></td>
<td><span data-ttu-id="9a21a-139">Не число</span><span class="sxs-lookup"><span data-stu-id="9a21a-139">NaN</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9a21a-140"><strong>-F</strong></span><span class="sxs-lookup"><span data-stu-id="9a21a-140"><strong>-F</strong></span></span></td>
<td><span data-ttu-id="9a21a-141">-inf</span><span class="sxs-lookup"><span data-stu-id="9a21a-141">-inf</span></span></td>
<td><span data-ttu-id="9a21a-142">-F</span><span class="sxs-lookup"><span data-stu-id="9a21a-142">-F</span></span></td>
<td><span data-ttu-id="9a21a-143">src0</span><span class="sxs-lookup"><span data-stu-id="9a21a-143">src0</span></span></td>
<td><span data-ttu-id="9a21a-144">src0</span><span class="sxs-lookup"><span data-stu-id="9a21a-144">src0</span></span></td>
<td><span data-ttu-id="9a21a-145">+-F или +-0</span><span class="sxs-lookup"><span data-stu-id="9a21a-145">+-F or +-0</span></span></td>
<td><span data-ttu-id="9a21a-146">+inf</span><span class="sxs-lookup"><span data-stu-id="9a21a-146">+inf</span></span></td>
<td><span data-ttu-id="9a21a-147">Не число</span><span class="sxs-lookup"><span data-stu-id="9a21a-147">NaN</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a21a-148"><strong>-0</strong></span><span class="sxs-lookup"><span data-stu-id="9a21a-148"><strong>-0</strong></span></span></td>
<td><span data-ttu-id="9a21a-149">-inf</span><span class="sxs-lookup"><span data-stu-id="9a21a-149">-inf</span></span></td>
<td><span data-ttu-id="9a21a-150">src1</span><span class="sxs-lookup"><span data-stu-id="9a21a-150">src1</span></span></td>
<td><span data-ttu-id="9a21a-151">-0</span><span class="sxs-lookup"><span data-stu-id="9a21a-151">-0</span></span></td>
<td><span data-ttu-id="9a21a-152">+0</span><span class="sxs-lookup"><span data-stu-id="9a21a-152">+0</span></span></td>
<td><span data-ttu-id="9a21a-153">src1</span><span class="sxs-lookup"><span data-stu-id="9a21a-153">src1</span></span></td>
<td><span data-ttu-id="9a21a-154">+inf</span><span class="sxs-lookup"><span data-stu-id="9a21a-154">+inf</span></span></td>
<td><span data-ttu-id="9a21a-155">Не число</span><span class="sxs-lookup"><span data-stu-id="9a21a-155">NaN</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9a21a-156"><strong>+0</strong></span><span class="sxs-lookup"><span data-stu-id="9a21a-156"><strong>+0</strong></span></span></td>
<td><span data-ttu-id="9a21a-157">-inf</span><span class="sxs-lookup"><span data-stu-id="9a21a-157">-inf</span></span></td>
<td><span data-ttu-id="9a21a-158">src1</span><span class="sxs-lookup"><span data-stu-id="9a21a-158">src1</span></span></td>
<td><span data-ttu-id="9a21a-159">+0</span><span class="sxs-lookup"><span data-stu-id="9a21a-159">+0</span></span></td>
<td><span data-ttu-id="9a21a-160">+0</span><span class="sxs-lookup"><span data-stu-id="9a21a-160">+0</span></span></td>
<td><span data-ttu-id="9a21a-161">src1</span><span class="sxs-lookup"><span data-stu-id="9a21a-161">src1</span></span></td>
<td><span data-ttu-id="9a21a-162">+inf</span><span class="sxs-lookup"><span data-stu-id="9a21a-162">+inf</span></span></td>
<td><span data-ttu-id="9a21a-163">не число</span><span class="sxs-lookup"><span data-stu-id="9a21a-163">NaN</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a21a-164"><strong>+ F</strong></span><span class="sxs-lookup"><span data-stu-id="9a21a-164"><strong>+F</strong></span></span></td>
<td><span data-ttu-id="9a21a-165">-inf</span><span class="sxs-lookup"><span data-stu-id="9a21a-165">-inf</span></span></td>
<td><span data-ttu-id="9a21a-166">+-F или +-0</span><span class="sxs-lookup"><span data-stu-id="9a21a-166">+-F or +-0</span></span></td>
<td><span data-ttu-id="9a21a-167">src0</span><span class="sxs-lookup"><span data-stu-id="9a21a-167">src0</span></span></td>
<td><span data-ttu-id="9a21a-168">src0</span><span class="sxs-lookup"><span data-stu-id="9a21a-168">src0</span></span></td>
<td><span data-ttu-id="9a21a-169">+ F</span><span class="sxs-lookup"><span data-stu-id="9a21a-169">+F</span></span></td>
<td><span data-ttu-id="9a21a-170">+inf</span><span class="sxs-lookup"><span data-stu-id="9a21a-170">+inf</span></span></td>
<td><span data-ttu-id="9a21a-171">не число</span><span class="sxs-lookup"><span data-stu-id="9a21a-171">NaN</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9a21a-172"><strong>+ INF</strong></span><span class="sxs-lookup"><span data-stu-id="9a21a-172"><strong>+inf</strong></span></span></td>
<td><span data-ttu-id="9a21a-173">не число</span><span class="sxs-lookup"><span data-stu-id="9a21a-173">NaN</span></span></td>
<td><span data-ttu-id="9a21a-174">+inf</span><span class="sxs-lookup"><span data-stu-id="9a21a-174">+inf</span></span></td>
<td><span data-ttu-id="9a21a-175">+inf</span><span class="sxs-lookup"><span data-stu-id="9a21a-175">+inf</span></span></td>
<td><span data-ttu-id="9a21a-176">+inf</span><span class="sxs-lookup"><span data-stu-id="9a21a-176">+inf</span></span></td>
<td><span data-ttu-id="9a21a-177">+inf</span><span class="sxs-lookup"><span data-stu-id="9a21a-177">+inf</span></span></td>
<td><span data-ttu-id="9a21a-178">+inf</span><span class="sxs-lookup"><span data-stu-id="9a21a-178">+inf</span></span></td>
<td><span data-ttu-id="9a21a-179">Не число</span><span class="sxs-lookup"><span data-stu-id="9a21a-179">NaN</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9a21a-180"><strong>Не число</strong></span><span class="sxs-lookup"><span data-stu-id="9a21a-180"><strong>NaN</strong></span></span></td>
<td><span data-ttu-id="9a21a-181">Не число</span><span class="sxs-lookup"><span data-stu-id="9a21a-181">NaN</span></span></td>
<td><span data-ttu-id="9a21a-182">Не число</span><span class="sxs-lookup"><span data-stu-id="9a21a-182">NaN</span></span></td>
<td><span data-ttu-id="9a21a-183">Не число</span><span class="sxs-lookup"><span data-stu-id="9a21a-183">NaN</span></span></td>
<td><span data-ttu-id="9a21a-184">Не число</span><span class="sxs-lookup"><span data-stu-id="9a21a-184">NaN</span></span></td>
<td><span data-ttu-id="9a21a-185">Не число</span><span class="sxs-lookup"><span data-stu-id="9a21a-185">NaN</span></span></td>
<td><span data-ttu-id="9a21a-186">Не число</span><span class="sxs-lookup"><span data-stu-id="9a21a-186">NaN</span></span></td>
<td><span data-ttu-id="9a21a-187">Не число</span><span class="sxs-lookup"><span data-stu-id="9a21a-187">NaN</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9a21a-188">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="9a21a-188">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9a21a-189">Вершина</span><span class="sxs-lookup"><span data-stu-id="9a21a-189">Vertex</span></span> | <span data-ttu-id="9a21a-190">Поверхности</span><span class="sxs-lookup"><span data-stu-id="9a21a-190">Hull</span></span> | <span data-ttu-id="9a21a-191">Домен</span><span class="sxs-lookup"><span data-stu-id="9a21a-191">Domain</span></span> | <span data-ttu-id="9a21a-192">Геометрия</span><span class="sxs-lookup"><span data-stu-id="9a21a-192">Geometry</span></span> | <span data-ttu-id="9a21a-193">Пиксель</span><span class="sxs-lookup"><span data-stu-id="9a21a-193">Pixel</span></span> | <span data-ttu-id="9a21a-194">Вычисления</span><span class="sxs-lookup"><span data-stu-id="9a21a-194">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="9a21a-195">X</span><span class="sxs-lookup"><span data-stu-id="9a21a-195">X</span></span>      | <span data-ttu-id="9a21a-196">X</span><span class="sxs-lookup"><span data-stu-id="9a21a-196">X</span></span>    | <span data-ttu-id="9a21a-197">X</span><span class="sxs-lookup"><span data-stu-id="9a21a-197">X</span></span>      | <span data-ttu-id="9a21a-198">X</span><span class="sxs-lookup"><span data-stu-id="9a21a-198">X</span></span>        | <span data-ttu-id="9a21a-199">X</span><span class="sxs-lookup"><span data-stu-id="9a21a-199">X</span></span>     | <span data-ttu-id="9a21a-200">X</span><span class="sxs-lookup"><span data-stu-id="9a21a-200">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9a21a-201">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="9a21a-201">Minimum Shader Model</span></span>

<span data-ttu-id="9a21a-202">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="9a21a-202">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="9a21a-203">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="9a21a-203">Shader Model</span></span>                                              | <span data-ttu-id="9a21a-204">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="9a21a-204">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9a21a-205">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="9a21a-205">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9a21a-206">да</span><span class="sxs-lookup"><span data-stu-id="9a21a-206">yes</span></span>       |
| [<span data-ttu-id="9a21a-207">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="9a21a-207">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9a21a-208">Нет</span><span class="sxs-lookup"><span data-stu-id="9a21a-208">no</span></span>        |
| [<span data-ttu-id="9a21a-209">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="9a21a-209">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9a21a-210">Нет</span><span class="sxs-lookup"><span data-stu-id="9a21a-210">no</span></span>        |
| [<span data-ttu-id="9a21a-211">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9a21a-211">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9a21a-212">Нет</span><span class="sxs-lookup"><span data-stu-id="9a21a-212">no</span></span>        |
| [<span data-ttu-id="9a21a-213">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9a21a-213">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9a21a-214">Нет</span><span class="sxs-lookup"><span data-stu-id="9a21a-214">no</span></span>        |
| [<span data-ttu-id="9a21a-215">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9a21a-215">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9a21a-216">Нет</span><span class="sxs-lookup"><span data-stu-id="9a21a-216">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9a21a-217">См. также</span><span class="sxs-lookup"><span data-stu-id="9a21a-217">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a21a-218">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9a21a-218">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





