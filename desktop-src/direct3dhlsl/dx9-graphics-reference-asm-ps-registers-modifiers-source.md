---
title: Модификаторы исходных регистров исходного шейдера пикселей
description: Используйте модификаторы исходного регистра, чтобы изменить значение, считанное из регистра, перед выполнением инструкции.
ms.assetid: b45d0919-7878-4184-ad4a-5623aae9d1f1
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a9dd4476dd7a1a885edb2e62a29b5127f5ff0a14
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129681"
---
# <a name="pixel-shader-source-register-modifiers"></a><span data-ttu-id="cc8b8-103">Модификаторы исходных регистров исходного шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="cc8b8-103">Pixel Shader Source Register Modifiers</span></span>

<span data-ttu-id="cc8b8-104">Используйте модификаторы исходного регистра, чтобы изменить значение, считанное из регистра, перед выполнением инструкции.</span><span class="sxs-lookup"><span data-stu-id="cc8b8-104">Use source register modifiers to change the value read from a register before an instruction runs.</span></span> <span data-ttu-id="cc8b8-105">Содержимое регистра источника остается неизменным.</span><span class="sxs-lookup"><span data-stu-id="cc8b8-105">The contents of a source register are left unchanged.</span></span> <span data-ttu-id="cc8b8-106">Модификаторы полезны для настройки диапазона регистрируемых данных в процессе подготовки к использованию инструкции.</span><span class="sxs-lookup"><span data-stu-id="cc8b8-106">Modifiers are useful for adjusting the range of register data in preparation for the instruction.</span></span> <span data-ttu-id="cc8b8-107">Набор модификаторов, именуемых селекторами, копирует или реплицирует данные из одного канала (r, g, b, a) в другие каналы.</span><span class="sxs-lookup"><span data-stu-id="cc8b8-107">A set of modifiers called selectors copies or replicates the data from a single channel (r,g,b,a) into the other channels.</span></span>

## <a name="ps_1_1---ps_1_4"></a><span data-ttu-id="cc8b8-108">PS \_ 1 \_ 1 — PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="cc8b8-108">ps\_1\_1 - ps\_1\_4</span></span>

<span data-ttu-id="cc8b8-109">В этой таблице указаны версии, поддерживающие каждый модификатор.</span><span class="sxs-lookup"><span data-stu-id="cc8b8-109">This table identifies the versions that support each modifier:</span></span>



| <span data-ttu-id="cc8b8-110">Модификаторы исходного регистра</span><span class="sxs-lookup"><span data-stu-id="cc8b8-110">Source register modifiers</span></span>                                                                                    | <span data-ttu-id="cc8b8-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cc8b8-111">Syntax</span></span>         | <span data-ttu-id="cc8b8-112">Версия 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="cc8b8-112">Version 1\_1</span></span> | <span data-ttu-id="cc8b8-113">Версия 1 \_ 2</span><span class="sxs-lookup"><span data-stu-id="cc8b8-113">Version 1\_2</span></span>     | <span data-ttu-id="cc8b8-114">Версия 1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="cc8b8-114">Version 1\_3</span></span>     | <span data-ttu-id="cc8b8-115">Версия 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="cc8b8-115">Version 1\_4</span></span>     |
|--------------------------------------------------------------------------------------------------------------|----------------|---------|------|------|------|
| [<span data-ttu-id="cc8b8-116">часов</span><span class="sxs-lookup"><span data-stu-id="cc8b8-116">bias</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-bias.md)                                           | <span data-ttu-id="cc8b8-117">зарегистрировать \_ смещение</span><span class="sxs-lookup"><span data-stu-id="cc8b8-117">register\_bias</span></span> | <span data-ttu-id="cc8b8-118">X</span><span class="sxs-lookup"><span data-stu-id="cc8b8-118">X</span></span>       | <span data-ttu-id="cc8b8-119">X</span><span class="sxs-lookup"><span data-stu-id="cc8b8-119">X</span></span>    | <span data-ttu-id="cc8b8-120">X</span><span class="sxs-lookup"><span data-stu-id="cc8b8-120">X</span></span>    | <span data-ttu-id="cc8b8-121">X</span><span class="sxs-lookup"><span data-stu-id="cc8b8-121">X</span></span>    |
| [<span data-ttu-id="cc8b8-122">зеркаль</span><span class="sxs-lookup"><span data-stu-id="cc8b8-122">invert</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md)                                       | <span data-ttu-id="cc8b8-123">1. регистрация</span><span class="sxs-lookup"><span data-stu-id="cc8b8-123">1 - register</span></span>   | <span data-ttu-id="cc8b8-124">X</span><span class="sxs-lookup"><span data-stu-id="cc8b8-124">X</span></span>       | <span data-ttu-id="cc8b8-125">X</span><span class="sxs-lookup"><span data-stu-id="cc8b8-125">X</span></span>    | <span data-ttu-id="cc8b8-126">X</span><span class="sxs-lookup"><span data-stu-id="cc8b8-126">X</span></span>    | <span data-ttu-id="cc8b8-127">X</span><span class="sxs-lookup"><span data-stu-id="cc8b8-127">X</span></span>    |
| [<span data-ttu-id="cc8b8-128">Negate</span><span class="sxs-lookup"><span data-stu-id="cc8b8-128">negate</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-negate.md)                                       | <span data-ttu-id="cc8b8-129">\- зарегистрировать</span><span class="sxs-lookup"><span data-stu-id="cc8b8-129">\- register</span></span>    | <span data-ttu-id="cc8b8-130">X</span><span class="sxs-lookup"><span data-stu-id="cc8b8-130">X</span></span>       | <span data-ttu-id="cc8b8-131">X</span><span class="sxs-lookup"><span data-stu-id="cc8b8-131">X</span></span>    | <span data-ttu-id="cc8b8-132">X</span><span class="sxs-lookup"><span data-stu-id="cc8b8-132">X</span></span>    | <span data-ttu-id="cc8b8-133">X</span><span class="sxs-lookup"><span data-stu-id="cc8b8-133">X</span></span>    |
| [<span data-ttu-id="cc8b8-134">масштабировать по 2</span><span class="sxs-lookup"><span data-stu-id="cc8b8-134">scale by 2</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md)                                 | <span data-ttu-id="cc8b8-135">Регистр \_ x2</span><span class="sxs-lookup"><span data-stu-id="cc8b8-135">register\_x2</span></span>   |         |      |      | <span data-ttu-id="cc8b8-136">X</span><span class="sxs-lookup"><span data-stu-id="cc8b8-136">X</span></span>    |
| [<span data-ttu-id="cc8b8-137">Масштабирование со знаком</span><span class="sxs-lookup"><span data-stu-id="cc8b8-137">signed scaling</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md)                         | <span data-ttu-id="cc8b8-138">регистрация \_ bx2</span><span class="sxs-lookup"><span data-stu-id="cc8b8-138">register\_bx2</span></span>  | <span data-ttu-id="cc8b8-139">X</span><span class="sxs-lookup"><span data-stu-id="cc8b8-139">X</span></span>       | <span data-ttu-id="cc8b8-140">X</span><span class="sxs-lookup"><span data-stu-id="cc8b8-140">X</span></span>    | <span data-ttu-id="cc8b8-141">X</span><span class="sxs-lookup"><span data-stu-id="cc8b8-141">X</span></span>    | <span data-ttu-id="cc8b8-142">X</span><span class="sxs-lookup"><span data-stu-id="cc8b8-142">X</span></span>    |
| [<span data-ttu-id="cc8b8-143">Модификаторы текслд и текскрд</span><span class="sxs-lookup"><span data-stu-id="cc8b8-143">texld and texcrd modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-ps-1-4.md)                   | <span data-ttu-id="cc8b8-144">регистрация \_ d\*</span><span class="sxs-lookup"><span data-stu-id="cc8b8-144">register\_d\*</span></span>  | <span data-ttu-id="cc8b8-145">X</span><span class="sxs-lookup"><span data-stu-id="cc8b8-145">X</span></span>       | <span data-ttu-id="cc8b8-146">X</span><span class="sxs-lookup"><span data-stu-id="cc8b8-146">X</span></span>    | <span data-ttu-id="cc8b8-147">X</span><span class="sxs-lookup"><span data-stu-id="cc8b8-147">X</span></span>    | <span data-ttu-id="cc8b8-148">X</span><span class="sxs-lookup"><span data-stu-id="cc8b8-148">X</span></span>    |
| [<span data-ttu-id="cc8b8-149">исходный регистр группирующие</span><span class="sxs-lookup"><span data-stu-id="cc8b8-149">source register swizzling</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) | <span data-ttu-id="cc8b8-150">Register. ксизв</span><span class="sxs-lookup"><span data-stu-id="cc8b8-150">register.xyzw</span></span>  | <span data-ttu-id="cc8b8-151">X</span><span class="sxs-lookup"><span data-stu-id="cc8b8-151">X</span></span>       | <span data-ttu-id="cc8b8-152">X</span><span class="sxs-lookup"><span data-stu-id="cc8b8-152">X</span></span>    | <span data-ttu-id="cc8b8-153">X</span><span class="sxs-lookup"><span data-stu-id="cc8b8-153">X</span></span>    | <span data-ttu-id="cc8b8-154">X</span><span class="sxs-lookup"><span data-stu-id="cc8b8-154">X</span></span>    |



 

<span data-ttu-id="cc8b8-155">Модификаторы исходного регистра можно использовать только в арифметических инструкциях.</span><span class="sxs-lookup"><span data-stu-id="cc8b8-155">Source register modifiers can be used only on arithmetic instructions.</span></span> <span data-ttu-id="cc8b8-156">Их нельзя использовать в инструкциях по адресам текстур.</span><span class="sxs-lookup"><span data-stu-id="cc8b8-156">They cannot be used on texture address instructions.</span></span> <span data-ttu-id="cc8b8-157">Исключением является модификатор масштабирования на [2](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md) .</span><span class="sxs-lookup"><span data-stu-id="cc8b8-157">The exception to this is the [scale by 2](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md) modifier.</span></span> <span data-ttu-id="cc8b8-158">Для версии 1 \_ 1 со знаком Scale можно использовать исходный аргумент любой \* инструкции тексм.</span><span class="sxs-lookup"><span data-stu-id="cc8b8-158">For version 1\_1, signed scale can be used on the source argument of any texm\* instruction.</span></span> <span data-ttu-id="cc8b8-159">Для версии 1 \_ 2 или 1 \_ 3 со знаком Scale можно использовать в аргументе Source любой инструкции адреса текстуры.</span><span class="sxs-lookup"><span data-stu-id="cc8b8-159">For version 1\_2 or 1\_3, signed scale can be used on the source argument of any texture address instruction.</span></span>

<span data-ttu-id="cc8b8-160">Некоторые ограничения для определенных модификаторов:</span><span class="sxs-lookup"><span data-stu-id="cc8b8-160">Some modifier specific restrictions:</span></span>

-   <span data-ttu-id="cc8b8-161">Отрицание можно сочетать с модификатором смещения, подписанного масштабирования или scalex2.</span><span class="sxs-lookup"><span data-stu-id="cc8b8-161">Negate can be combined with either the bias, signed scaling, or scalex2 modifier.</span></span> <span data-ttu-id="cc8b8-162">При объединении обратная работа выполняется в последнюю очередь.</span><span class="sxs-lookup"><span data-stu-id="cc8b8-162">When combined, negate is run last.</span></span>
-   <span data-ttu-id="cc8b8-163">Инвертировать нельзя использовать вместе с любым другим модификатором.</span><span class="sxs-lookup"><span data-stu-id="cc8b8-163">Invert cannot be combined with any other modifier.</span></span>
-   <span data-ttu-id="cc8b8-164">Инверсия, отрицания, смещение, масштабирование со знаком и scalex2 можно сочетать с любыми селекторами.</span><span class="sxs-lookup"><span data-stu-id="cc8b8-164">Invert, negate, bias, signed scaling, and scalex2 can be combined with any of the selectors.</span></span>
-   <span data-ttu-id="cc8b8-165">Модификаторы исходного регистра не следует использовать в регистрах констант, так как они приводят к неопределенным результатам.</span><span class="sxs-lookup"><span data-stu-id="cc8b8-165">Source register modifiers should not be used on constant registers because they will cause undefined results.</span></span> <span data-ttu-id="cc8b8-166">Для версии 1 \_ 4 модификаторы константы не допускаются и не проходят проверку.</span><span class="sxs-lookup"><span data-stu-id="cc8b8-166">For version 1\_4, modifiers on constants are not allowed and will fail validation.</span></span>

## <a name="ps_2_0-and-above"></a><span data-ttu-id="cc8b8-167">PS \_ 2 \_ и выше</span><span class="sxs-lookup"><span data-stu-id="cc8b8-167">ps\_2\_0 and Above</span></span>

<span data-ttu-id="cc8b8-168">Для версии PS \_ 2 \_ 0 и выше число модификаторов было упрощено.</span><span class="sxs-lookup"><span data-stu-id="cc8b8-168">For version ps\_2\_0 and up, the number of modifiers has been simplified.</span></span>

### <a name="negate"></a><span data-ttu-id="cc8b8-169">Negate</span><span class="sxs-lookup"><span data-stu-id="cc8b8-169">Negate</span></span>

<span data-ttu-id="cc8b8-170">Инвертирует содержимое регистра источника.</span><span class="sxs-lookup"><span data-stu-id="cc8b8-170">Negate the contents of the source register.</span></span>



| <span data-ttu-id="cc8b8-171">Модификатор компонента</span><span class="sxs-lookup"><span data-stu-id="cc8b8-171">Component modifier</span></span> | <span data-ttu-id="cc8b8-172">Описание</span><span class="sxs-lookup"><span data-stu-id="cc8b8-172">Description</span></span>     |
|--------------------|-----------------|
| <span data-ttu-id="cc8b8-173">\- Cерверный</span><span class="sxs-lookup"><span data-stu-id="cc8b8-173">\- r</span></span>               | <span data-ttu-id="cc8b8-174">Отрицание источника</span><span class="sxs-lookup"><span data-stu-id="cc8b8-174">Source negation</span></span> |



 

<span data-ttu-id="cc8b8-175">Модификатор отрицания не может использоваться во втором регистре источника следующих инструкций: [m3x2-PS](m3x2---ps.md), [m3x3-PS](m3x3---ps.md), [m3x4-PS](m3x4---ps.md), [m4x3-PS](m4x3---ps.md)и [m4x4-PS](m4x4---ps.md).</span><span class="sxs-lookup"><span data-stu-id="cc8b8-175">The negate modifier cannot be used on second source register of these instructions: [m3x2 - ps](m3x2---ps.md), [m3x3 - ps](m3x3---ps.md), [m3x4 - ps](m3x4---ps.md), [m4x3 - ps](m4x3---ps.md), and [m4x4 - ps](m4x4---ps.md).</span></span>



| <span data-ttu-id="cc8b8-176">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="cc8b8-176">Pixel shader versions</span></span> | <span data-ttu-id="cc8b8-177">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cc8b8-177">2\_0</span></span> | <span data-ttu-id="cc8b8-178">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="cc8b8-178">2\_x</span></span> | <span data-ttu-id="cc8b8-179">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="cc8b8-179">2\_sw</span></span> | <span data-ttu-id="cc8b8-180">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cc8b8-180">3\_0</span></span> | <span data-ttu-id="cc8b8-181">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="cc8b8-181">3\_sw</span></span> |
|-----------------------|------|------|-------|------|-------|
| \-                    | <span data-ttu-id="cc8b8-182">x</span><span class="sxs-lookup"><span data-stu-id="cc8b8-182">x</span></span>    | <span data-ttu-id="cc8b8-183">x</span><span class="sxs-lookup"><span data-stu-id="cc8b8-183">x</span></span>    | <span data-ttu-id="cc8b8-184">x</span><span class="sxs-lookup"><span data-stu-id="cc8b8-184">x</span></span>     | <span data-ttu-id="cc8b8-185">x</span><span class="sxs-lookup"><span data-stu-id="cc8b8-185">x</span></span>    | <span data-ttu-id="cc8b8-186">x</span><span class="sxs-lookup"><span data-stu-id="cc8b8-186">x</span></span>     |



 

### <a name="absolute-value"></a><span data-ttu-id="cc8b8-187">Абсолютное значение</span><span class="sxs-lookup"><span data-stu-id="cc8b8-187">Absolute Value</span></span>

<span data-ttu-id="cc8b8-188">Получение абсолютного значения регистра.</span><span class="sxs-lookup"><span data-stu-id="cc8b8-188">Take the absolute value of the register.</span></span>



| <span data-ttu-id="cc8b8-189">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="cc8b8-189">Pixel shader versions</span></span> | <span data-ttu-id="cc8b8-190">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cc8b8-190">2\_0</span></span> | <span data-ttu-id="cc8b8-191">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="cc8b8-191">2\_x</span></span> | <span data-ttu-id="cc8b8-192">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="cc8b8-192">2\_sw</span></span> | <span data-ttu-id="cc8b8-193">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="cc8b8-193">3\_0</span></span> | <span data-ttu-id="cc8b8-194">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="cc8b8-194">3\_sw</span></span> |
|-----------------------|------|------|-------|------|-------|
| <span data-ttu-id="cc8b8-195">abs</span><span class="sxs-lookup"><span data-stu-id="cc8b8-195">abs</span></span>                   |      |      |       | <span data-ttu-id="cc8b8-196">x</span><span class="sxs-lookup"><span data-stu-id="cc8b8-196">x</span></span>    | <span data-ttu-id="cc8b8-197">x</span><span class="sxs-lookup"><span data-stu-id="cc8b8-197">x</span></span>     |



 

<span data-ttu-id="cc8b8-198">Если шейдер версии 3 считывает из одного или нескольких регистров с плавающей запятой (c \# ), одно из следующих должно быть истинным.</span><span class="sxs-lookup"><span data-stu-id="cc8b8-198">If any version 3 shader reads from one or more constant float registers (c\#), one of the following must be true.</span></span>

-   <span data-ttu-id="cc8b8-199">Все константные регистры с плавающей запятой должны использовать модификатор ABS.</span><span class="sxs-lookup"><span data-stu-id="cc8b8-199">All of the constant floating-point registers must use the abs modifier.</span></span>
-   <span data-ttu-id="cc8b8-200">Ни один из постоянных регистров с плавающей запятой не может использовать модификатор ABS.</span><span class="sxs-lookup"><span data-stu-id="cc8b8-200">None of the constant floating-point registers can use the abs modifier.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cc8b8-201">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="cc8b8-201">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc8b8-202">Модификаторы регистра для шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="cc8b8-202">Pixel Shader Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers.md)
</dt> </dl>

 

 




