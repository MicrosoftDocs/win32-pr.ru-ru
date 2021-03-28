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
ms.openlocfilehash: 12cfee533a71408a445d97a63bbd8b76b281236b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332616"
---
# <a name="pixel-shader-source-register-modifiers"></a><span data-ttu-id="0f28a-103">Модификаторы исходных регистров исходного шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="0f28a-103">Pixel Shader Source Register Modifiers</span></span>

<span data-ttu-id="0f28a-104">Используйте модификаторы исходного регистра, чтобы изменить значение, считанное из регистра, перед выполнением инструкции.</span><span class="sxs-lookup"><span data-stu-id="0f28a-104">Use source register modifiers to change the value read from a register before an instruction runs.</span></span> <span data-ttu-id="0f28a-105">Содержимое регистра источника остается неизменным.</span><span class="sxs-lookup"><span data-stu-id="0f28a-105">The contents of a source register are left unchanged.</span></span> <span data-ttu-id="0f28a-106">Модификаторы полезны для настройки диапазона регистрируемых данных в процессе подготовки к использованию инструкции.</span><span class="sxs-lookup"><span data-stu-id="0f28a-106">Modifiers are useful for adjusting the range of register data in preparation for the instruction.</span></span> <span data-ttu-id="0f28a-107">Набор модификаторов, именуемых селекторами, копирует или реплицирует данные из одного канала (r, g, b, a) в другие каналы.</span><span class="sxs-lookup"><span data-stu-id="0f28a-107">A set of modifiers called selectors copies or replicates the data from a single channel (r,g,b,a) into the other channels.</span></span>

## <a name="ps_1_1---ps_1_4"></a><span data-ttu-id="0f28a-108">PS \_ 1 \_ 1 — PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="0f28a-108">ps\_1\_1 - ps\_1\_4</span></span>

<span data-ttu-id="0f28a-109">В этой таблице указаны версии, поддерживающие каждый модификатор.</span><span class="sxs-lookup"><span data-stu-id="0f28a-109">This table identifies the versions that support each modifier:</span></span>



| <span data-ttu-id="0f28a-110">Модификаторы исходного регистра</span><span class="sxs-lookup"><span data-stu-id="0f28a-110">Source register modifiers</span></span>                                                                                    | <span data-ttu-id="0f28a-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0f28a-111">Syntax</span></span>         | <span data-ttu-id="0f28a-112">Version</span><span class="sxs-lookup"><span data-stu-id="0f28a-112">Version</span></span> |      |      |      |     |     |
|--------------------------------------------------------------------------------------------------------------|----------------|---------|------|------|------|-----|-----|
|                                                                                                              |                | <span data-ttu-id="0f28a-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="0f28a-113">1\_1</span></span>    | <span data-ttu-id="0f28a-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="0f28a-114">1\_2</span></span> | <span data-ttu-id="0f28a-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="0f28a-115">1\_3</span></span> | <span data-ttu-id="0f28a-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="0f28a-116">1\_4</span></span> |     |     |
| [<span data-ttu-id="0f28a-117">часов</span><span class="sxs-lookup"><span data-stu-id="0f28a-117">bias</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-bias.md)                                           | <span data-ttu-id="0f28a-118">зарегистрировать \_ смещение</span><span class="sxs-lookup"><span data-stu-id="0f28a-118">register\_bias</span></span> | <span data-ttu-id="0f28a-119">X</span><span class="sxs-lookup"><span data-stu-id="0f28a-119">X</span></span>       | <span data-ttu-id="0f28a-120">X</span><span class="sxs-lookup"><span data-stu-id="0f28a-120">X</span></span>    | <span data-ttu-id="0f28a-121">X</span><span class="sxs-lookup"><span data-stu-id="0f28a-121">X</span></span>    | <span data-ttu-id="0f28a-122">X</span><span class="sxs-lookup"><span data-stu-id="0f28a-122">X</span></span>    |     |     |
| [<span data-ttu-id="0f28a-123">зеркаль</span><span class="sxs-lookup"><span data-stu-id="0f28a-123">invert</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md)                                       | <span data-ttu-id="0f28a-124">1. регистрация</span><span class="sxs-lookup"><span data-stu-id="0f28a-124">1 - register</span></span>   | <span data-ttu-id="0f28a-125">X</span><span class="sxs-lookup"><span data-stu-id="0f28a-125">X</span></span>       | <span data-ttu-id="0f28a-126">X</span><span class="sxs-lookup"><span data-stu-id="0f28a-126">X</span></span>    | <span data-ttu-id="0f28a-127">X</span><span class="sxs-lookup"><span data-stu-id="0f28a-127">X</span></span>    | <span data-ttu-id="0f28a-128">X</span><span class="sxs-lookup"><span data-stu-id="0f28a-128">X</span></span>    |     |     |
| [<span data-ttu-id="0f28a-129">negate</span><span class="sxs-lookup"><span data-stu-id="0f28a-129">negate</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-negate.md)                                       | <span data-ttu-id="0f28a-130">\- зарегистрировать</span><span class="sxs-lookup"><span data-stu-id="0f28a-130">\- register</span></span>    | <span data-ttu-id="0f28a-131">X</span><span class="sxs-lookup"><span data-stu-id="0f28a-131">X</span></span>       | <span data-ttu-id="0f28a-132">X</span><span class="sxs-lookup"><span data-stu-id="0f28a-132">X</span></span>    | <span data-ttu-id="0f28a-133">X</span><span class="sxs-lookup"><span data-stu-id="0f28a-133">X</span></span>    | <span data-ttu-id="0f28a-134">X</span><span class="sxs-lookup"><span data-stu-id="0f28a-134">X</span></span>    |     |     |
| [<span data-ttu-id="0f28a-135">масштабировать по 2</span><span class="sxs-lookup"><span data-stu-id="0f28a-135">scale by 2</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md)                                 | <span data-ttu-id="0f28a-136">Регистр \_ x2</span><span class="sxs-lookup"><span data-stu-id="0f28a-136">register\_x2</span></span>   |         |      |      | <span data-ttu-id="0f28a-137">X</span><span class="sxs-lookup"><span data-stu-id="0f28a-137">X</span></span>    |     |     |
| [<span data-ttu-id="0f28a-138">Масштабирование со знаком</span><span class="sxs-lookup"><span data-stu-id="0f28a-138">signed scaling</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md)                         | <span data-ttu-id="0f28a-139">регистрация \_ bx2</span><span class="sxs-lookup"><span data-stu-id="0f28a-139">register\_bx2</span></span>  | <span data-ttu-id="0f28a-140">X</span><span class="sxs-lookup"><span data-stu-id="0f28a-140">X</span></span>       | <span data-ttu-id="0f28a-141">X</span><span class="sxs-lookup"><span data-stu-id="0f28a-141">X</span></span>    | <span data-ttu-id="0f28a-142">X</span><span class="sxs-lookup"><span data-stu-id="0f28a-142">X</span></span>    | <span data-ttu-id="0f28a-143">X</span><span class="sxs-lookup"><span data-stu-id="0f28a-143">X</span></span>    |     |     |
| [<span data-ttu-id="0f28a-144">Модификаторы текслд и текскрд</span><span class="sxs-lookup"><span data-stu-id="0f28a-144">texld and texcrd modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-ps-1-4.md)                   | <span data-ttu-id="0f28a-145">регистрация \_ d\*</span><span class="sxs-lookup"><span data-stu-id="0f28a-145">register\_d\*</span></span>  | <span data-ttu-id="0f28a-146">X</span><span class="sxs-lookup"><span data-stu-id="0f28a-146">X</span></span>       | <span data-ttu-id="0f28a-147">X</span><span class="sxs-lookup"><span data-stu-id="0f28a-147">X</span></span>    | <span data-ttu-id="0f28a-148">X</span><span class="sxs-lookup"><span data-stu-id="0f28a-148">X</span></span>    | <span data-ttu-id="0f28a-149">X</span><span class="sxs-lookup"><span data-stu-id="0f28a-149">X</span></span>    |     |     |
| [<span data-ttu-id="0f28a-150">исходный регистр группирующие</span><span class="sxs-lookup"><span data-stu-id="0f28a-150">source register swizzling</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md) | <span data-ttu-id="0f28a-151">Register. ксизв</span><span class="sxs-lookup"><span data-stu-id="0f28a-151">register.xyzw</span></span>  | <span data-ttu-id="0f28a-152">X</span><span class="sxs-lookup"><span data-stu-id="0f28a-152">X</span></span>       | <span data-ttu-id="0f28a-153">X</span><span class="sxs-lookup"><span data-stu-id="0f28a-153">X</span></span>    | <span data-ttu-id="0f28a-154">X</span><span class="sxs-lookup"><span data-stu-id="0f28a-154">X</span></span>    | <span data-ttu-id="0f28a-155">X</span><span class="sxs-lookup"><span data-stu-id="0f28a-155">X</span></span>    |     |     |



 

<span data-ttu-id="0f28a-156">Модификаторы исходного регистра можно использовать только в арифметических инструкциях.</span><span class="sxs-lookup"><span data-stu-id="0f28a-156">Source register modifiers can be used only on arithmetic instructions.</span></span> <span data-ttu-id="0f28a-157">Их нельзя использовать в инструкциях по адресам текстур.</span><span class="sxs-lookup"><span data-stu-id="0f28a-157">They cannot be used on texture address instructions.</span></span> <span data-ttu-id="0f28a-158">Исключением является модификатор масштабирования на [2](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md) .</span><span class="sxs-lookup"><span data-stu-id="0f28a-158">The exception to this is the [scale by 2](dx9-graphics-reference-asm-ps-registers-modifiers-scale-x2.md) modifier.</span></span> <span data-ttu-id="0f28a-159">Для версии 1 \_ 1 со знаком Scale можно использовать исходный аргумент любой \* инструкции тексм.</span><span class="sxs-lookup"><span data-stu-id="0f28a-159">For version 1\_1, signed scale can be used on the source argument of any texm\* instruction.</span></span> <span data-ttu-id="0f28a-160">Для версии 1 \_ 2 или 1 \_ 3 со знаком Scale можно использовать в аргументе Source любой инструкции адреса текстуры.</span><span class="sxs-lookup"><span data-stu-id="0f28a-160">For version 1\_2 or 1\_3, signed scale can be used on the source argument of any texture address instruction.</span></span>

<span data-ttu-id="0f28a-161">Некоторые ограничения для определенных модификаторов:</span><span class="sxs-lookup"><span data-stu-id="0f28a-161">Some modifier specific restrictions:</span></span>

-   <span data-ttu-id="0f28a-162">Отрицание можно сочетать с модификатором смещения, подписанного масштабирования или scalex2.</span><span class="sxs-lookup"><span data-stu-id="0f28a-162">Negate can be combined with either the bias, signed scaling, or scalex2 modifier.</span></span> <span data-ttu-id="0f28a-163">При объединении обратная работа выполняется в последнюю очередь.</span><span class="sxs-lookup"><span data-stu-id="0f28a-163">When combined, negate is run last.</span></span>
-   <span data-ttu-id="0f28a-164">Инвертировать нельзя использовать вместе с любым другим модификатором.</span><span class="sxs-lookup"><span data-stu-id="0f28a-164">Invert cannot be combined with any other modifier.</span></span>
-   <span data-ttu-id="0f28a-165">Инверсия, отрицания, смещение, масштабирование со знаком и scalex2 можно сочетать с любыми селекторами.</span><span class="sxs-lookup"><span data-stu-id="0f28a-165">Invert, negate, bias, signed scaling, and scalex2 can be combined with any of the selectors.</span></span>
-   <span data-ttu-id="0f28a-166">Модификаторы исходного регистра не следует использовать в регистрах констант, так как они приводят к неопределенным результатам.</span><span class="sxs-lookup"><span data-stu-id="0f28a-166">Source register modifiers should not be used on constant registers because they will cause undefined results.</span></span> <span data-ttu-id="0f28a-167">Для версии 1 \_ 4 модификаторы константы не допускаются и не проходят проверку.</span><span class="sxs-lookup"><span data-stu-id="0f28a-167">For version 1\_4, modifiers on constants are not allowed and will fail validation.</span></span>

## <a name="ps_2_0-and-above"></a><span data-ttu-id="0f28a-168">PS \_ 2 \_ и выше</span><span class="sxs-lookup"><span data-stu-id="0f28a-168">ps\_2\_0 and Above</span></span>

<span data-ttu-id="0f28a-169">Для версии PS \_ 2 \_ 0 и выше число модификаторов было упрощено.</span><span class="sxs-lookup"><span data-stu-id="0f28a-169">For version ps\_2\_0 and up, the number of modifiers has been simplified.</span></span>

### <a name="negate"></a><span data-ttu-id="0f28a-170">Negate</span><span class="sxs-lookup"><span data-stu-id="0f28a-170">Negate</span></span>

<span data-ttu-id="0f28a-171">Инвертирует содержимое регистра источника.</span><span class="sxs-lookup"><span data-stu-id="0f28a-171">Negate the contents of the source register.</span></span>



| <span data-ttu-id="0f28a-172">Модификатор компонента</span><span class="sxs-lookup"><span data-stu-id="0f28a-172">Component modifier</span></span> | <span data-ttu-id="0f28a-173">Описание</span><span class="sxs-lookup"><span data-stu-id="0f28a-173">Description</span></span>     |
|--------------------|-----------------|
| <span data-ttu-id="0f28a-174">\- Cерверный</span><span class="sxs-lookup"><span data-stu-id="0f28a-174">\- r</span></span>               | <span data-ttu-id="0f28a-175">Отрицание источника</span><span class="sxs-lookup"><span data-stu-id="0f28a-175">Source negation</span></span> |



 

<span data-ttu-id="0f28a-176">Модификатор отрицания не может использоваться во втором регистре источника следующих инструкций: [m3x2-PS](m3x2---ps.md), [m3x3-PS](m3x3---ps.md), [m3x4-PS](m3x4---ps.md), [m4x3-PS](m4x3---ps.md)и [m4x4-PS](m4x4---ps.md).</span><span class="sxs-lookup"><span data-stu-id="0f28a-176">The negate modifier cannot be used on second source register of these instructions: [m3x2 - ps](m3x2---ps.md), [m3x3 - ps](m3x3---ps.md), [m3x4 - ps](m3x4---ps.md), [m4x3 - ps](m4x3---ps.md), and [m4x4 - ps](m4x4---ps.md).</span></span>



| <span data-ttu-id="0f28a-177">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="0f28a-177">Pixel shader versions</span></span> | <span data-ttu-id="0f28a-178">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0f28a-178">2\_0</span></span> | <span data-ttu-id="0f28a-179">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="0f28a-179">2\_x</span></span> | <span data-ttu-id="0f28a-180">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0f28a-180">2\_sw</span></span> | <span data-ttu-id="0f28a-181">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0f28a-181">3\_0</span></span> | <span data-ttu-id="0f28a-182">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0f28a-182">3\_sw</span></span> |
|-----------------------|------|------|-------|------|-------|
| \-                    | <span data-ttu-id="0f28a-183">x</span><span class="sxs-lookup"><span data-stu-id="0f28a-183">x</span></span>    | <span data-ttu-id="0f28a-184">x</span><span class="sxs-lookup"><span data-stu-id="0f28a-184">x</span></span>    | <span data-ttu-id="0f28a-185">x</span><span class="sxs-lookup"><span data-stu-id="0f28a-185">x</span></span>     | <span data-ttu-id="0f28a-186">x</span><span class="sxs-lookup"><span data-stu-id="0f28a-186">x</span></span>    | <span data-ttu-id="0f28a-187">x</span><span class="sxs-lookup"><span data-stu-id="0f28a-187">x</span></span>     |



 

### <a name="absolute-value"></a><span data-ttu-id="0f28a-188">Абсолютное значение</span><span class="sxs-lookup"><span data-stu-id="0f28a-188">Absolute Value</span></span>

<span data-ttu-id="0f28a-189">Получение абсолютного значения регистра.</span><span class="sxs-lookup"><span data-stu-id="0f28a-189">Take the absolute value of the register.</span></span>



| <span data-ttu-id="0f28a-190">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="0f28a-190">Pixel shader versions</span></span> | <span data-ttu-id="0f28a-191">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0f28a-191">2\_0</span></span> | <span data-ttu-id="0f28a-192">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="0f28a-192">2\_x</span></span> | <span data-ttu-id="0f28a-193">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0f28a-193">2\_sw</span></span> | <span data-ttu-id="0f28a-194">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0f28a-194">3\_0</span></span> | <span data-ttu-id="0f28a-195">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0f28a-195">3\_sw</span></span> |
|-----------------------|------|------|-------|------|-------|
| <span data-ttu-id="0f28a-196">abs</span><span class="sxs-lookup"><span data-stu-id="0f28a-196">abs</span></span>                   |      |      |       | <span data-ttu-id="0f28a-197">x</span><span class="sxs-lookup"><span data-stu-id="0f28a-197">x</span></span>    | <span data-ttu-id="0f28a-198">x</span><span class="sxs-lookup"><span data-stu-id="0f28a-198">x</span></span>     |



 

<span data-ttu-id="0f28a-199">Если шейдер версии 3 считывает из одного или нескольких регистров с плавающей запятой (c \# ), одно из следующих должно быть истинным.</span><span class="sxs-lookup"><span data-stu-id="0f28a-199">If any version 3 shader reads from one or more constant float registers (c\#), one of the following must be true.</span></span>

-   <span data-ttu-id="0f28a-200">Все константные регистры с плавающей запятой должны использовать модификатор ABS.</span><span class="sxs-lookup"><span data-stu-id="0f28a-200">All of the constant floating-point registers must use the abs modifier.</span></span>
-   <span data-ttu-id="0f28a-201">Ни один из постоянных регистров с плавающей запятой не может использовать модификатор ABS.</span><span class="sxs-lookup"><span data-stu-id="0f28a-201">None of the constant floating-point registers can use the abs modifier.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0f28a-202">См. также</span><span class="sxs-lookup"><span data-stu-id="0f28a-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f28a-203">Модификаторы регистра для шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="0f28a-203">Pixel Shader Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers.md)
</dt> </dl>

 

 




