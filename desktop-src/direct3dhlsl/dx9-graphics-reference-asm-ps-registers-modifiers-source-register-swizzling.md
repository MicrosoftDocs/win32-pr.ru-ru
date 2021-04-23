---
title: Source Register группирующие (Справочник по HLSL PS)
description: Группирующие означает возможность копирования любого компонента регистрации источника в любой временный компонент регистрации. Группирующие не влияет на данные регистра источника. Перед выполнением инструкции данные в исходном регистре копируются во временную регистрацию.
ms.assetid: 27aee6a8-5185-4236-b3e4-44addf230c34
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4ffc655129740f112a3ade9eb40c0bbe29dfc1fb
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/23/2019
ms.locfileid: "104335683"
---
# <a name="source-register-swizzling-hlsl-ps-reference"></a><span data-ttu-id="17ced-105">Source Register группирующие (Справочник по HLSL PS)</span><span class="sxs-lookup"><span data-stu-id="17ced-105">Source register swizzling (HLSL PS reference)</span></span>

<span data-ttu-id="17ced-106">Группирующие означает возможность копирования любого компонента регистрации источника в любой временный компонент регистрации.</span><span class="sxs-lookup"><span data-stu-id="17ced-106">Swizzling refers to the ability to copy any source register component to any temporary register component.</span></span> <span data-ttu-id="17ced-107">Группирующие не влияет на данные регистра источника.</span><span class="sxs-lookup"><span data-stu-id="17ced-107">Swizzling does not affect the source register data.</span></span> <span data-ttu-id="17ced-108">Перед выполнением инструкции данные в исходном регистре копируются во временную регистрацию.</span><span class="sxs-lookup"><span data-stu-id="17ced-108">Before an instruction runs, the data in a source register is copied to a temporary register.</span></span>

## <a name="source-swizzling"></a><span data-ttu-id="17ced-109">Исходный группирующие</span><span class="sxs-lookup"><span data-stu-id="17ced-109">Source Swizzling</span></span>

<span data-ttu-id="17ced-110">Source свиззле позволяет отдельному компоненту исходного регистра принимать значения любого из четырех компонентов одного и того же исходного регистра до того, как регистр будет считан для вычисления.</span><span class="sxs-lookup"><span data-stu-id="17ced-110">Source swizzle allows individual component of a source register to take on the value of any of the four components of the same source register before the register is read for computation.</span></span>

<span data-ttu-id="17ced-111">Например, зкскси свиззле означает:</span><span class="sxs-lookup"><span data-stu-id="17ced-111">For example, the .zxxy swizzle means:</span></span>

-   <span data-ttu-id="17ced-112">компонент. x принимает значение компонента. z</span><span class="sxs-lookup"><span data-stu-id="17ced-112">.x component will take on the value of .z component</span></span>
-   <span data-ttu-id="17ced-113">компонент y принимает значение компонента. x</span><span class="sxs-lookup"><span data-stu-id="17ced-113">.y component will take on the value of .x component</span></span>
-   <span data-ttu-id="17ced-114">. z компонент принимает значение компонента x</span><span class="sxs-lookup"><span data-stu-id="17ced-114">.z component will take on the value of .x component</span></span>
-   <span data-ttu-id="17ced-115">компонент. w принимает значение компонента y.</span><span class="sxs-lookup"><span data-stu-id="17ced-115">.w component will take on the value of .y component</span></span>

<span data-ttu-id="17ced-116">Компоненты могут отображаться в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="17ced-116">The components can appear in any order.</span></span> <span data-ttu-id="17ced-117">Если указано менее четырех компонентов, последний компонент повторяется.</span><span class="sxs-lookup"><span data-stu-id="17ced-117">If fewer than four components are specified, the last component is repeated.</span></span> <span data-ttu-id="17ced-118">Например:</span><span class="sxs-lookup"><span data-stu-id="17ced-118">For example:</span></span>


```
.xy  = .xyyy
.wzx = .wzxx
.z   = .zzzz
```



<span data-ttu-id="17ced-119">Если компонент не указан, группирующие не применяется.</span><span class="sxs-lookup"><span data-stu-id="17ced-119">If no component is specified, no swizzling is applied.</span></span>

<span data-ttu-id="17ced-120">Некоторые инструкции имеют ограничения для Source свиззле.</span><span class="sxs-lookup"><span data-stu-id="17ced-120">Some instructions have restrictions for source swizzle.</span></span> <span data-ttu-id="17ced-121">Они перечислены на справочных страницах по соблюдающих инструкциях.</span><span class="sxs-lookup"><span data-stu-id="17ced-121">They are listed in the respected instruction reference pages.</span></span>



| <span data-ttu-id="17ced-122">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="17ced-122">Pixel shader versions</span></span> | <span data-ttu-id="17ced-123">1\_1</span><span class="sxs-lookup"><span data-stu-id="17ced-123">1\_1</span></span> | <span data-ttu-id="17ced-124">1\_2</span><span class="sxs-lookup"><span data-stu-id="17ced-124">1\_2</span></span> | <span data-ttu-id="17ced-125">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="17ced-125">1\_3</span></span> | <span data-ttu-id="17ced-126">1\_4</span><span class="sxs-lookup"><span data-stu-id="17ced-126">1\_4</span></span> | <span data-ttu-id="17ced-127">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="17ced-127">2\_0</span></span> | <span data-ttu-id="17ced-128">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="17ced-128">2\_x</span></span> | <span data-ttu-id="17ced-129">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="17ced-129">2\_sw</span></span> | <span data-ttu-id="17ced-130">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="17ced-130">3\_0</span></span> | <span data-ttu-id="17ced-131">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="17ced-131">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="17ced-132">. x</span><span class="sxs-lookup"><span data-stu-id="17ced-132">.x</span></span>                    |      |      |      | <span data-ttu-id="17ced-133">x</span><span class="sxs-lookup"><span data-stu-id="17ced-133">x</span></span>    | <span data-ttu-id="17ced-134">x</span><span class="sxs-lookup"><span data-stu-id="17ced-134">x</span></span>    | <span data-ttu-id="17ced-135">x</span><span class="sxs-lookup"><span data-stu-id="17ced-135">x</span></span>    | <span data-ttu-id="17ced-136">x</span><span class="sxs-lookup"><span data-stu-id="17ced-136">x</span></span>     | <span data-ttu-id="17ced-137">x</span><span class="sxs-lookup"><span data-stu-id="17ced-137">x</span></span>    | <span data-ttu-id="17ced-138">x</span><span class="sxs-lookup"><span data-stu-id="17ced-138">x</span></span>     |
| <span data-ttu-id="17ced-139">. y</span><span class="sxs-lookup"><span data-stu-id="17ced-139">.y</span></span>                    |      |      |      | <span data-ttu-id="17ced-140">x</span><span class="sxs-lookup"><span data-stu-id="17ced-140">x</span></span>    | <span data-ttu-id="17ced-141">x</span><span class="sxs-lookup"><span data-stu-id="17ced-141">x</span></span>    | <span data-ttu-id="17ced-142">x</span><span class="sxs-lookup"><span data-stu-id="17ced-142">x</span></span>    | <span data-ttu-id="17ced-143">x</span><span class="sxs-lookup"><span data-stu-id="17ced-143">x</span></span>     | <span data-ttu-id="17ced-144">x</span><span class="sxs-lookup"><span data-stu-id="17ced-144">x</span></span>    | <span data-ttu-id="17ced-145">x</span><span class="sxs-lookup"><span data-stu-id="17ced-145">x</span></span>     |
| <span data-ttu-id="17ced-146">. z</span><span class="sxs-lookup"><span data-stu-id="17ced-146">.z</span></span>                    | <span data-ttu-id="17ced-147">x\*</span><span class="sxs-lookup"><span data-stu-id="17ced-147">x\*</span></span>  | <span data-ttu-id="17ced-148">x\*</span><span class="sxs-lookup"><span data-stu-id="17ced-148">x\*</span></span>  | <span data-ttu-id="17ced-149">x\*</span><span class="sxs-lookup"><span data-stu-id="17ced-149">x\*</span></span>  | <span data-ttu-id="17ced-150">x</span><span class="sxs-lookup"><span data-stu-id="17ced-150">x</span></span>    | <span data-ttu-id="17ced-151">x</span><span class="sxs-lookup"><span data-stu-id="17ced-151">x</span></span>    | <span data-ttu-id="17ced-152">x</span><span class="sxs-lookup"><span data-stu-id="17ced-152">x</span></span>    | <span data-ttu-id="17ced-153">x</span><span class="sxs-lookup"><span data-stu-id="17ced-153">x</span></span>     | <span data-ttu-id="17ced-154">x</span><span class="sxs-lookup"><span data-stu-id="17ced-154">x</span></span>    | <span data-ttu-id="17ced-155">x</span><span class="sxs-lookup"><span data-stu-id="17ced-155">x</span></span>     |
| <span data-ttu-id="17ced-156">. w</span><span class="sxs-lookup"><span data-stu-id="17ced-156">.w</span></span>                    | <span data-ttu-id="17ced-157">x</span><span class="sxs-lookup"><span data-stu-id="17ced-157">x</span></span>    | <span data-ttu-id="17ced-158">x</span><span class="sxs-lookup"><span data-stu-id="17ced-158">x</span></span>    | <span data-ttu-id="17ced-159">x</span><span class="sxs-lookup"><span data-stu-id="17ced-159">x</span></span>    | <span data-ttu-id="17ced-160">x</span><span class="sxs-lookup"><span data-stu-id="17ced-160">x</span></span>    | <span data-ttu-id="17ced-161">x</span><span class="sxs-lookup"><span data-stu-id="17ced-161">x</span></span>    | <span data-ttu-id="17ced-162">x</span><span class="sxs-lookup"><span data-stu-id="17ced-162">x</span></span>    | <span data-ttu-id="17ced-163">x</span><span class="sxs-lookup"><span data-stu-id="17ced-163">x</span></span>     | <span data-ttu-id="17ced-164">x</span><span class="sxs-lookup"><span data-stu-id="17ced-164">x</span></span>    | <span data-ttu-id="17ced-165">x</span><span class="sxs-lookup"><span data-stu-id="17ced-165">x</span></span>     |
| <span data-ttu-id="17ced-166">. ксизв (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="17ced-166">.xyzw (default)</span></span>       | <span data-ttu-id="17ced-167">x</span><span class="sxs-lookup"><span data-stu-id="17ced-167">x</span></span>    | <span data-ttu-id="17ced-168">x</span><span class="sxs-lookup"><span data-stu-id="17ced-168">x</span></span>    | <span data-ttu-id="17ced-169">x</span><span class="sxs-lookup"><span data-stu-id="17ced-169">x</span></span>    | <span data-ttu-id="17ced-170">x</span><span class="sxs-lookup"><span data-stu-id="17ced-170">x</span></span>    | <span data-ttu-id="17ced-171">x</span><span class="sxs-lookup"><span data-stu-id="17ced-171">x</span></span>    | <span data-ttu-id="17ced-172">x</span><span class="sxs-lookup"><span data-stu-id="17ced-172">x</span></span>    | <span data-ttu-id="17ced-173">x</span><span class="sxs-lookup"><span data-stu-id="17ced-173">x</span></span>     | <span data-ttu-id="17ced-174">x</span><span class="sxs-lookup"><span data-stu-id="17ced-174">x</span></span>    | <span data-ttu-id="17ced-175">x</span><span class="sxs-lookup"><span data-stu-id="17ced-175">x</span></span>     |
| <span data-ttu-id="17ced-176">. изксв</span><span class="sxs-lookup"><span data-stu-id="17ced-176">.yzxw</span></span>                 |      |      |      |      | <span data-ttu-id="17ced-177">x</span><span class="sxs-lookup"><span data-stu-id="17ced-177">x</span></span>    | <span data-ttu-id="17ced-178">x</span><span class="sxs-lookup"><span data-stu-id="17ced-178">x</span></span>    | <span data-ttu-id="17ced-179">x</span><span class="sxs-lookup"><span data-stu-id="17ced-179">x</span></span>     | <span data-ttu-id="17ced-180">x</span><span class="sxs-lookup"><span data-stu-id="17ced-180">x</span></span>    | <span data-ttu-id="17ced-181">x</span><span class="sxs-lookup"><span data-stu-id="17ced-181">x</span></span>     |
| <span data-ttu-id="17ced-182">. зксив</span><span class="sxs-lookup"><span data-stu-id="17ced-182">.zxyw</span></span>                 |      |      |      |      | <span data-ttu-id="17ced-183">x</span><span class="sxs-lookup"><span data-stu-id="17ced-183">x</span></span>    | <span data-ttu-id="17ced-184">x</span><span class="sxs-lookup"><span data-stu-id="17ced-184">x</span></span>    | <span data-ttu-id="17ced-185">x</span><span class="sxs-lookup"><span data-stu-id="17ced-185">x</span></span>     | <span data-ttu-id="17ced-186">x</span><span class="sxs-lookup"><span data-stu-id="17ced-186">x</span></span>    | <span data-ttu-id="17ced-187">x</span><span class="sxs-lookup"><span data-stu-id="17ced-187">x</span></span>     |
| <span data-ttu-id="17ced-188">. взикс</span><span class="sxs-lookup"><span data-stu-id="17ced-188">.wzyx</span></span>                 |      |      |      |      | <span data-ttu-id="17ced-189">x</span><span class="sxs-lookup"><span data-stu-id="17ced-189">x</span></span>    | <span data-ttu-id="17ced-190">x</span><span class="sxs-lookup"><span data-stu-id="17ced-190">x</span></span>    | <span data-ttu-id="17ced-191">x</span><span class="sxs-lookup"><span data-stu-id="17ced-191">x</span></span>     | <span data-ttu-id="17ced-192">x</span><span class="sxs-lookup"><span data-stu-id="17ced-192">x</span></span>    | <span data-ttu-id="17ced-193">x</span><span class="sxs-lookup"><span data-stu-id="17ced-193">x</span></span>     |
| <span data-ttu-id="17ced-194">произвольный свиззле</span><span class="sxs-lookup"><span data-stu-id="17ced-194">arbitrary swizzle</span></span>     |      |      |      |      |      | <span data-ttu-id="17ced-195">x</span><span class="sxs-lookup"><span data-stu-id="17ced-195">x</span></span>    | <span data-ttu-id="17ced-196">x</span><span class="sxs-lookup"><span data-stu-id="17ced-196">x</span></span>     | <span data-ttu-id="17ced-197">x</span><span class="sxs-lookup"><span data-stu-id="17ced-197">x</span></span>    | <span data-ttu-id="17ced-198">x</span><span class="sxs-lookup"><span data-stu-id="17ced-198">x</span></span>     |



 

<span data-ttu-id="17ced-199">\* Доступно, только если целевой маской записи является. w (. a).</span><span class="sxs-lookup"><span data-stu-id="17ced-199">\* Only available if destination write mask is .w (.a).</span></span>

## <a name="arbitrary-swizzle"></a><span data-ttu-id="17ced-200">Произвольный Свиззле</span><span class="sxs-lookup"><span data-stu-id="17ced-200">Arbitrary Swizzle</span></span>

<span data-ttu-id="17ced-201">Свиззлес можно применить к исходным регистрам в произвольном порядке; Это значит, что любой регистр источника может принимать любую маску компонента в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="17ced-201">Swizzles can be applied to source registers in an arbitrary order; that is, any source register can take any component mask, in any order.</span></span>

## <a name="replicate-swizzle"></a><span data-ttu-id="17ced-202">Репликация Свиззле</span><span class="sxs-lookup"><span data-stu-id="17ced-202">Replicate Swizzle</span></span>

<span data-ttu-id="17ced-203">Репликация свиззле копирует один компонент в другой.</span><span class="sxs-lookup"><span data-stu-id="17ced-203">Replicate swizzle copies one component to another.</span></span> <span data-ttu-id="17ced-204">Это значит, что необходимо указать только один из компонентов. x,. y,. z,. w свиззле (или. r,. g,. b,. a эквивалент).</span><span class="sxs-lookup"><span data-stu-id="17ced-204">This is, exactly one of the .x, .y, .z, .w swizzle components (or the .r, .g, .b, .a equivalents) must be specified.</span></span>

## <a name="related-topics"></a><span data-ttu-id="17ced-205">См. также</span><span class="sxs-lookup"><span data-stu-id="17ced-205">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17ced-206">Модификаторы исходных регистров исходного шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="17ced-206">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> <dt>

[<span data-ttu-id="17ced-207">реестр PS 1 1 PS 1 2 PS 1 3 PS 1 \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ 4 регистры</span><span class="sxs-lookup"><span data-stu-id="17ced-207">ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)
</dt> <dt>

[<span data-ttu-id="17ced-208">\_ \_ регистры PS 2 0</span><span class="sxs-lookup"><span data-stu-id="17ced-208">ps\_2\_0 Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-2-0.md)
</dt> <dt>

[<span data-ttu-id="17ced-209">\_ \_ регистры PS 2 x</span><span class="sxs-lookup"><span data-stu-id="17ced-209">ps\_2\_x Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-2-x.md)
</dt> <dt>

[<span data-ttu-id="17ced-210">\_ \_ регистры PS 3 0</span><span class="sxs-lookup"><span data-stu-id="17ced-210">ps\_3\_0 Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)
</dt> </dl>

 

 




