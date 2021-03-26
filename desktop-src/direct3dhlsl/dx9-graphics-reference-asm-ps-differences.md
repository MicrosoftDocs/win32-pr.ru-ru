---
title: Различия шейдера пикселей
description: Различия шейдера пикселей
ms.assetid: 11aefb26-eb82-486c-81ff-7c0cfbab1b7a
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9a74b5cc7588220fdc5173c470f7852ee9ef763d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413149"
---
# <a name="pixel-shader-differences"></a><span data-ttu-id="2e821-103">Различия шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="2e821-103">Pixel Shader Differences</span></span>

## <a name="instruction-slots"></a><span data-ttu-id="2e821-104">Слоты инструкций</span><span class="sxs-lookup"><span data-stu-id="2e821-104">Instruction Slots</span></span>

<span data-ttu-id="2e821-105">Каждая версия поддерживает разное число максимальных слотов инструкций.</span><span class="sxs-lookup"><span data-stu-id="2e821-105">Each version supports a different number of maximum instruction slots.</span></span>



| <span data-ttu-id="2e821-106">Version</span><span class="sxs-lookup"><span data-stu-id="2e821-106">Version</span></span>  | <span data-ttu-id="2e821-107">Максимальное число слотов инструкций</span><span class="sxs-lookup"><span data-stu-id="2e821-107">Maximum number of instruction slots</span></span>                                                                                   |
|----------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e821-108">PS \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="2e821-108">ps\_1\_1</span></span> | <span data-ttu-id="2e821-109">4. текстура + 8 арифметических операций</span><span class="sxs-lookup"><span data-stu-id="2e821-109">4 texture + 8 arithmetic</span></span>                                                                                              |
| <span data-ttu-id="2e821-110">PS \_ 1 \_ 2</span><span class="sxs-lookup"><span data-stu-id="2e821-110">ps\_1\_2</span></span> | <span data-ttu-id="2e821-111">4. текстура + 8 арифметических операций</span><span class="sxs-lookup"><span data-stu-id="2e821-111">4 texture + 8 arithmetic</span></span>                                                                                              |
| <span data-ttu-id="2e821-112">PS \_ 1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="2e821-112">ps\_1\_3</span></span> | <span data-ttu-id="2e821-113">4. текстура + 8 арифметических операций</span><span class="sxs-lookup"><span data-stu-id="2e821-113">4 texture + 8 arithmetic</span></span>                                                                                              |
| <span data-ttu-id="2e821-114">PS \_ 1 \_ 4</span><span class="sxs-lookup"><span data-stu-id="2e821-114">ps\_1\_4</span></span> | <span data-ttu-id="2e821-115">6 текстур + 8 арифметических операций на один этап</span><span class="sxs-lookup"><span data-stu-id="2e821-115">6 texture + 8 arithmetic per phase</span></span>                                                                                    |
| <span data-ttu-id="2e821-116">PS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2e821-116">ps\_2\_0</span></span> | <span data-ttu-id="2e821-117">32. текстура + 64, арифметический</span><span class="sxs-lookup"><span data-stu-id="2e821-117">32 texture + 64 arithmetic</span></span>                                                                                            |
| <span data-ttu-id="2e821-118">PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="2e821-118">ps\_2\_x</span></span> | <span data-ttu-id="2e821-119">96 минимум и до количества слотов в D3DCAPS9. D3DPSHADERCAPS2 \_ 0. нуминструктионслотс.</span><span class="sxs-lookup"><span data-stu-id="2e821-119">96 minimum, and up to the number of slots in D3DCAPS9.D3DPSHADERCAPS2\_0.NumInstructionSlots.</span></span> <span data-ttu-id="2e821-120">См \_ . D3DPSHADERCAPS2 0.</span><span class="sxs-lookup"><span data-stu-id="2e821-120">See D3DPSHADERCAPS2\_0.</span></span> |
| <span data-ttu-id="2e821-121">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2e821-121">ps\_3\_0</span></span> | <span data-ttu-id="2e821-122">512 минимум и до количества слотов в D3DCAPS9. MaxPixelShader30InstructionSlots.</span><span class="sxs-lookup"><span data-stu-id="2e821-122">512 minimum, and up to the number of slots in D3DCAPS9.MaxPixelShader30InstructionSlots.</span></span> <span data-ttu-id="2e821-123">См \_ . D3DPSHADERCAPS2 0.</span><span class="sxs-lookup"><span data-stu-id="2e821-123">See D3DPSHADERCAPS2\_0.</span></span>      |



 

<span data-ttu-id="2e821-124">Сведения об ограничениях шейдеров программного обеспечения см. в разделе [программные шейдеры](dx9-graphics-reference-asm-software-shaders.md).</span><span class="sxs-lookup"><span data-stu-id="2e821-124">For information about the limitations of software shaders, see [Software Shaders](dx9-graphics-reference-asm-software-shaders.md).</span></span>

## <a name="flow-control-nesting-limits"></a><span data-ttu-id="2e821-125">Ограничения вложенности управления потоком</span><span class="sxs-lookup"><span data-stu-id="2e821-125">Flow Control Nesting Limits</span></span>

-   <span data-ttu-id="2e821-126">См. раздел [ограничения управления потоком](dx9-graphics-reference-asm-ps-instructions-flow-control.md).</span><span class="sxs-lookup"><span data-stu-id="2e821-126">See [Flow Control Limitations](dx9-graphics-reference-asm-ps-instructions-flow-control.md).</span></span>

## <a name="ps_1_x-features"></a><span data-ttu-id="2e821-127">\_функции PS 1 \_ x</span><span class="sxs-lookup"><span data-stu-id="2e821-127">ps\_1\_x Features</span></span>

<span data-ttu-id="2e821-128">Новые инструкции:</span><span class="sxs-lookup"><span data-stu-id="2e821-128">New instructions:</span></span>

<span data-ttu-id="2e821-129">См [. \_ \_ инструкции по PS 1 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, \_ \_ ](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md)PS 1 4.</span><span class="sxs-lookup"><span data-stu-id="2e821-129">See [ps\_1\_1, ps\_1\_2, ps\_1\_3, ps\_1\_4 Instructions](dx9-graphics-reference-asm-ps-instructions-ps-1-x.md).</span></span>

<span data-ttu-id="2e821-130">Новые регистры:</span><span class="sxs-lookup"><span data-stu-id="2e821-130">New registers:</span></span>

<span data-ttu-id="2e821-131">См. Дополнительные сведения о [ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ регистрах PS 1 1 PS 1 2](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)PS 1 3 PS 1 4.</span><span class="sxs-lookup"><span data-stu-id="2e821-131">See [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="ps_2_0-features"></a><span data-ttu-id="2e821-132">\_функции PS 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2e821-132">ps\_2\_0 Features</span></span>

<span data-ttu-id="2e821-133">Новые функции</span><span class="sxs-lookup"><span data-stu-id="2e821-133">New features:</span></span>

-   <span data-ttu-id="2e821-134">Три новых свиззлес-. изксв,. зксив,. взикс</span><span class="sxs-lookup"><span data-stu-id="2e821-134">Three new swizzles - .yzxw, .zxyw, .wzyx</span></span>
-   <span data-ttu-id="2e821-135">Количество [временных регистров](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ), увеличенное до 12</span><span class="sxs-lookup"><span data-stu-id="2e821-135">Number of [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) increased to 12</span></span>
-   <span data-ttu-id="2e821-136">Число постоянных регистров [регистра с плавающей запятой](dx9-graphics-reference-asm-ps-registers-constant-float.md) (c \# ) увеличилось до 32</span><span class="sxs-lookup"><span data-stu-id="2e821-136">Number of [Constant Float Register](dx9-graphics-reference-asm-ps-registers-constant-float.md) registers (c\#) increased to 32</span></span>
-   <span data-ttu-id="2e821-137">Количество [регистров координат текстуры](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)(t \# ) увеличилось до 8</span><span class="sxs-lookup"><span data-stu-id="2e821-137">Number of [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)s (t\#) increased to 8</span></span>

<span data-ttu-id="2e821-138">Новые инструкции:</span><span class="sxs-lookup"><span data-stu-id="2e821-138">New instructions:</span></span>

-   <span data-ttu-id="2e821-139">Инструкции по установке — [дкл-(SM2, SM3-PS ASM)](dcl---ps.md), [дкл \_ самплертипе (SM2, SM3-PS ASM)](dcl-samplertype---ps.md)</span><span class="sxs-lookup"><span data-stu-id="2e821-139">Setup instructions - [dcl - (sm2, sm3 - ps asm)](dcl---ps.md), [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md)</span></span>
-   <span data-ttu-id="2e821-140">Арифметические инструкции [— ABS-PS](abs---ps.md), [CR-PS](crs---ps.md), [dp2add-PS](dp2add---ps.md), [exp-PS](exp---ps.md), [ФРК-PS](frc---ps.md), [log-](log---ps.md)PS, [m3x2-](m3x2---ps.md)PS [, m3x3-](m3x3---ps.md)PS, [m3x4-PS](m3x4---ps.md), [m4x3-PS](m4x3---ps.md) [, m4x4-](m4x4---ps.md)PS, [Max-](max---ps.md)PS [, min-PS](min---ps.md), [НРМ-](nrm---ps.md)PS, [Pow-](pow---ps.md)PS, [rcp](rcp---ps.md)-PS, [РСК-](rsq---ps.md)PS, [синкос-PS](sincos---ps.md)</span><span class="sxs-lookup"><span data-stu-id="2e821-140">Arithmetic instructions - [abs - ps](abs---ps.md), [crs - ps](crs---ps.md), [dp2add - ps](dp2add---ps.md), [exp - ps](exp---ps.md), [frc - ps](frc---ps.md), [log - ps](log---ps.md), [m3x2 - ps](m3x2---ps.md), [m3x3 - ps](m3x3---ps.md), [m3x4 - ps](m3x4---ps.md), [m4x3 - ps](m4x3---ps.md), [m4x4 - ps](m4x4---ps.md), [max - ps](max---ps.md), [min - ps](min---ps.md), [nrm - ps](nrm---ps.md), [pow - ps](pow---ps.md), [rcp - ps](rcp---ps.md), [rsq - ps](rsq---ps.md), [sincos - ps](sincos---ps.md)</span></span>
-   <span data-ttu-id="2e821-141">Инструкции по текстуре — [текслд-PS \_ 2 \_ 0 и up](texld---ps-2-0.md) (другой синтаксис), [текслдб-PS](texldb---ps.md), [текслдп-PS](texldp---ps.md)</span><span class="sxs-lookup"><span data-stu-id="2e821-141">Texture instructions - [texld - ps\_2\_0 and up](texld---ps-2-0.md) (different syntax), [texldb - ps](texldb---ps.md), [texldp - ps](texldp---ps.md)</span></span>

<span data-ttu-id="2e821-142">Новые регистры:</span><span class="sxs-lookup"><span data-stu-id="2e821-142">New registers:</span></span>

-   <span data-ttu-id="2e821-143">[Образцы (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \#</span><span class="sxs-lookup"><span data-stu-id="2e821-143">[Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#)</span></span>

## <a name="ps_2_x-features"></a><span data-ttu-id="2e821-144">\_функции PS 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="2e821-144">ps\_2\_x Features</span></span>

<span data-ttu-id="2e821-145">Новые возможности (см. [**D3DPSHADERCAPS2 \_ 0**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0)):</span><span class="sxs-lookup"><span data-stu-id="2e821-145">New features (See [**D3DPSHADERCAPS2\_0**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0).):</span></span>

-   <span data-ttu-id="2e821-146">Динамическое управление потоком</span><span class="sxs-lookup"><span data-stu-id="2e821-146">Dynamic flow control</span></span>
-   <span data-ttu-id="2e821-147">Статическое управление потоком</span><span class="sxs-lookup"><span data-stu-id="2e821-147">Static flow control</span></span>
-   <span data-ttu-id="2e821-148">Инструкции по вложению для динамических и статических функций управления потоком</span><span class="sxs-lookup"><span data-stu-id="2e821-148">Nesting for dynamic and static flow control instructions</span></span>
-   <span data-ttu-id="2e821-149">Число увеличенных [временных регистров](dx9-graphics-reference-asm-ps-registers-temporary.md)(r \# )</span><span class="sxs-lookup"><span data-stu-id="2e821-149">Number of [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md)s (r\#) increased</span></span>
-   <span data-ttu-id="2e821-150">Произвольный исходный свиззле</span><span class="sxs-lookup"><span data-stu-id="2e821-150">Arbitrary source swizzle</span></span>
-   <span data-ttu-id="2e821-151">Инструкции по градиенту</span><span class="sxs-lookup"><span data-stu-id="2e821-151">Gradient instructions</span></span>
-   <span data-ttu-id="2e821-152">Предикация</span><span class="sxs-lookup"><span data-stu-id="2e821-152">Predication</span></span>
-   <span data-ttu-id="2e821-153">Нет ограничения на чтение зависимой текстуры</span><span class="sxs-lookup"><span data-stu-id="2e821-153">No dependent texture read limit</span></span>
-   <span data-ttu-id="2e821-154">Предел для инструкции текстуры отсутствует</span><span class="sxs-lookup"><span data-stu-id="2e821-154">No texture instruction limit</span></span>

<span data-ttu-id="2e821-155">Новые инструкции:</span><span class="sxs-lookup"><span data-stu-id="2e821-155">New instructions:</span></span>

-   <span data-ttu-id="2e821-156">Статические инструкции по управлению потоком — [Если bool-PS](if-bool---ps.md), [Call-PS](call---ps.md), [каллнз bool-](callnz-bool---ps.md)PS, [else-PS](else---ps.md), [endif-PS](endif---ps.md), [представитель-PS](rep---ps.md), [ендреп-](endrep---ps.md)PS, [Label-PS](label---ps.md), [RET-PS](ret---ps.md)</span><span class="sxs-lookup"><span data-stu-id="2e821-156">Static flow control instructions - [if bool - ps](if-bool---ps.md), [call - ps](call---ps.md), [callnz bool - ps](callnz-bool---ps.md), [else - ps](else---ps.md), [endif - ps](endif---ps.md), [rep - ps](rep---ps.md), [endrep - ps](endrep---ps.md), [label - ps](label---ps.md), [ret - ps](ret---ps.md)</span></span>
-   <span data-ttu-id="2e821-157">Динамическое управление потоком инструкции [-break-PS](break---ps.md), Break-PS, [бреакп-PS](break-p---ps.md), [каллнз пред-PS](callnz-pred---ps.md), [if \_ comp-PS](if-comp---ps.md), [Если пред-](if-pred---ps.md)PS, [сетп \_ comp-PS](setp-comp---ps.md) [ \_ ](break-comp---ps.md)</span><span class="sxs-lookup"><span data-stu-id="2e821-157">Dynamic flow control instructions - [break - ps](break---ps.md), [break\_comp - ps](break-comp---ps.md), [breakp - ps](break-p---ps.md), [callnz pred - ps](callnz-pred---ps.md), [if\_comp - ps](if-comp---ps.md), [if pred - ps](if-pred---ps.md), [setp\_comp - ps](setp-comp---ps.md)</span></span>
-   <span data-ttu-id="2e821-158">Арифметические инструкции — [ДСКС-PS](dsx---ps.md), [ДСИ-PS](dsy---ps.md)</span><span class="sxs-lookup"><span data-stu-id="2e821-158">Arithmetic instructions - [dsx - ps](dsx---ps.md), [dsy - ps](dsy---ps.md)</span></span>
-   <span data-ttu-id="2e821-159">Текстурная инструкция- [текслдд-PS](texldd---ps.md)</span><span class="sxs-lookup"><span data-stu-id="2e821-159">Texture instruction - [texldd - ps](texldd---ps.md)</span></span>

<span data-ttu-id="2e821-160">Новые регистры:</span><span class="sxs-lookup"><span data-stu-id="2e821-160">New registers:</span></span>

-   <span data-ttu-id="2e821-161">[Регистр предиката](dx9-graphics-reference-asm-ps-registers-predicate.md) (P0)</span><span class="sxs-lookup"><span data-stu-id="2e821-161">[Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md) (p0)</span></span>

## <a name="ps_3_0-features"></a><span data-ttu-id="2e821-162">\_функции PS 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2e821-162">ps\_3\_0 Features</span></span>

<span data-ttu-id="2e821-163">Новые функции</span><span class="sxs-lookup"><span data-stu-id="2e821-163">New features:</span></span>

-   <span data-ttu-id="2e821-164">Консолидированный 10 [входных регистров](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)(v \# )</span><span class="sxs-lookup"><span data-stu-id="2e821-164">Consolidated 10 [Input Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)s (v\#)</span></span>
-   <span data-ttu-id="2e821-165">Индексируемый [входной цветовой регистр](dx9-graphics-reference-asm-ps-registers-input-color.md) (v \# ) с [регистром счетчика цикла](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (Al)</span><span class="sxs-lookup"><span data-stu-id="2e821-165">Indexable [Input Color Register](dx9-graphics-reference-asm-ps-registers-input-color.md) (v\#) with the [Loop Counter Register](dx9-graphics-reference-asm-ps-registers-loop-counter.md) (aL)</span></span>
-   <span data-ttu-id="2e821-166">Количество [временных регистров](dx9-graphics-reference-asm-ps-registers-temporary.md)(r \# ), увеличенное до 32</span><span class="sxs-lookup"><span data-stu-id="2e821-166">Number of [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md)s (r\#) increased to 32</span></span>
-   <span data-ttu-id="2e821-167">Число [постоянных регистров с плавающей запятой](dx9-graphics-reference-asm-ps-registers-constant-float.md)(c \# ) увеличилось до 224</span><span class="sxs-lookup"><span data-stu-id="2e821-167">Number of [Constant Float Register](dx9-graphics-reference-asm-ps-registers-constant-float.md)s (c\#) increased to 224</span></span>

<span data-ttu-id="2e821-168">Новые инструкции:</span><span class="sxs-lookup"><span data-stu-id="2e821-168">New instructions:</span></span>

-   <span data-ttu-id="2e821-169">Инструкция Setup — [ \_ семантика дкл (SM3-PS ASM)](dcl-usage---ps.md)</span><span class="sxs-lookup"><span data-stu-id="2e821-169">Setup instruction - [dcl\_semantics (sm3 - ps asm)](dcl-usage---ps.md)</span></span>
-   <span data-ttu-id="2e821-170">Статические инструкции потока- [Loop-PS](loop---ps.md), [ендлуп-PS](endloop---ps.md)</span><span class="sxs-lookup"><span data-stu-id="2e821-170">Static flow instructions - [loop - ps](loop---ps.md), [endloop - ps](endloop---ps.md)</span></span>
-   <span data-ttu-id="2e821-171">Арифметическая инструкция- [синкос-PS](sincos---ps.md) (новый синтаксис)</span><span class="sxs-lookup"><span data-stu-id="2e821-171">Arithmetic instruction - [sincos - ps](sincos---ps.md) (new syntax)</span></span>
-   <span data-ttu-id="2e821-172">Текстурная инструкция- [текслдл-PS](texldl---ps.md)</span><span class="sxs-lookup"><span data-stu-id="2e821-172">Texture instruction - [texldl - ps](texldl---ps.md)</span></span>

<span data-ttu-id="2e821-173">Новые регистры:</span><span class="sxs-lookup"><span data-stu-id="2e821-173">New registers:</span></span>

-   <span data-ttu-id="2e821-174">[Входной регистр](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (v \# )</span><span class="sxs-lookup"><span data-stu-id="2e821-174">[Input Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (v\#)</span></span>
-   <span data-ttu-id="2e821-175">[Регистр позиций](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (впос)</span><span class="sxs-lookup"><span data-stu-id="2e821-175">[Position Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (vPos)</span></span>
-   <span data-ttu-id="2e821-176">[Регистр лиц](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (вфаце)</span><span class="sxs-lookup"><span data-stu-id="2e821-176">[Face Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md) (vFace)</span></span>

## <a name="related-topics"></a><span data-ttu-id="2e821-177">См. также</span><span class="sxs-lookup"><span data-stu-id="2e821-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e821-178">Шейдеры пикселей</span><span class="sxs-lookup"><span data-stu-id="2e821-178">Pixel Shaders</span></span>](dx9-graphics-reference-asm-ps.md)
</dt> </dl>

 

 