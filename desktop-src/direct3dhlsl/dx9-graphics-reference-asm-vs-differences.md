---
title: Различия шейдеров вершин
description: Различия шейдеров вершин
ms.assetid: 94fe4033-94c0-4561-b0fd-1fb85d8f796b
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1c74603f9eab4ea91e9220bbaa172c0262aeda99
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070135"
---
# <a name="vertex-shader-differences"></a><span data-ttu-id="11af4-103">Различия шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="11af4-103">Vertex Shader Differences</span></span>

## <a name="instruction-slots"></a><span data-ttu-id="11af4-104">Слоты инструкций</span><span class="sxs-lookup"><span data-stu-id="11af4-104">Instruction Slots</span></span>

<span data-ttu-id="11af4-105">Каждая версия поддерживает разное число максимальных слотов инструкций.</span><span class="sxs-lookup"><span data-stu-id="11af4-105">Each version supports a differing number of maximum instruction slots.</span></span>



| <span data-ttu-id="11af4-106">Version</span><span class="sxs-lookup"><span data-stu-id="11af4-106">Version</span></span>  | <span data-ttu-id="11af4-107">Максимальное число слотов инструкций</span><span class="sxs-lookup"><span data-stu-id="11af4-107">Maximum number of instruction slots</span></span>                                                                                               |
|----------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11af4-108">VS \_ 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="11af4-108">vs\_1\_1</span></span> | <span data-ttu-id="11af4-109">128</span><span class="sxs-lookup"><span data-stu-id="11af4-109">128</span></span>                                                                                                                               |
| <span data-ttu-id="11af4-110">VS \_ 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="11af4-110">vs\_2\_0</span></span> | <span data-ttu-id="11af4-111">256</span><span class="sxs-lookup"><span data-stu-id="11af4-111">256</span></span>                                                                                                                               |
| <span data-ttu-id="11af4-112">VS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="11af4-112">vs\_2\_x</span></span> | <span data-ttu-id="11af4-113">256</span><span class="sxs-lookup"><span data-stu-id="11af4-113">256</span></span>                                                                                                                               |
| <span data-ttu-id="11af4-114">VS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="11af4-114">vs\_3\_0</span></span> | <span data-ttu-id="11af4-115">512 минимум и до количества слотов в D3DCAPS9. MaxVertexShader30InstructionSlots.</span><span class="sxs-lookup"><span data-stu-id="11af4-115">512 minimum, and up to the number of slots in D3DCAPS9.MaxVertexShader30InstructionSlots.</span></span> <span data-ttu-id="11af4-116">См. [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="11af4-116">See [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9).</span></span> |



 

<span data-ttu-id="11af4-117">Сведения об ограничениях шейдеров программного обеспечения см. в разделе [программные шейдеры](dx9-graphics-reference-asm-software-shaders.md).</span><span class="sxs-lookup"><span data-stu-id="11af4-117">For information about the limitations of software shaders, see [Software Shaders](dx9-graphics-reference-asm-software-shaders.md).</span></span>

## <a name="flow-control-nesting-limits"></a><span data-ttu-id="11af4-118">Ограничения вложенности управления потоком</span><span class="sxs-lookup"><span data-stu-id="11af4-118">Flow Control Nesting Limits</span></span>

-   <span data-ttu-id="11af4-119">См. раздел [ограничения вложений управления потоком](dx9-graphics-reference-asm-vs-instructions-flow-control.md).</span><span class="sxs-lookup"><span data-stu-id="11af4-119">See [Flow Control Nesting Limits](dx9-graphics-reference-asm-vs-instructions-flow-control.md).</span></span>

## <a name="vs_1_1-features"></a><span data-ttu-id="11af4-120">\_функции VS 1 \_ 1</span><span class="sxs-lookup"><span data-stu-id="11af4-120">vs\_1\_1 Features</span></span>

<span data-ttu-id="11af4-121">Новые инструкции:</span><span class="sxs-lookup"><span data-stu-id="11af4-121">New instructions:</span></span>

<span data-ttu-id="11af4-122">См. [инструкции — VS \_ 1 \_ 1](dx9-graphics-reference-asm-vs-instructions-vs-1-1.md).</span><span class="sxs-lookup"><span data-stu-id="11af4-122">See [Instructions - vs\_1\_1](dx9-graphics-reference-asm-vs-instructions-vs-1-1.md).</span></span>

<span data-ttu-id="11af4-123">Новые регистры:</span><span class="sxs-lookup"><span data-stu-id="11af4-123">New registers:</span></span>

<span data-ttu-id="11af4-124">См. раздел [регистры-VS \_ 1 \_ 1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md).</span><span class="sxs-lookup"><span data-stu-id="11af4-124">See [Registers - vs\_1\_1](dx9-graphics-reference-asm-vs-registers-vs-1-1.md).</span></span>

## <a name="vs_2_0-features"></a><span data-ttu-id="11af4-125">\_функции vs 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="11af4-125">vs\_2\_0 Features</span></span>

<span data-ttu-id="11af4-126">Новые функции</span><span class="sxs-lookup"><span data-stu-id="11af4-126">New features:</span></span>

-   <span data-ttu-id="11af4-127">Статическое управление потоком</span><span class="sxs-lookup"><span data-stu-id="11af4-127">Static flow control</span></span>
-   <span data-ttu-id="11af4-128">Доступны все четыре компонента [регистра адресов](dx9-graphics-reference-asm-vs-registers-address.md) (a0).</span><span class="sxs-lookup"><span data-stu-id="11af4-128">All four components of the [Address Register](dx9-graphics-reference-asm-vs-registers-address.md) (a0) are available.</span></span>

<span data-ttu-id="11af4-129">Новые инструкции:</span><span class="sxs-lookup"><span data-stu-id="11af4-129">New instructions:</span></span>

-   <span data-ttu-id="11af4-130">Инструкции по установке — [дефб-VS](defb---vs.md), [дефи-VS](defi---vs.md)</span><span class="sxs-lookup"><span data-stu-id="11af4-130">Setup instructions - [defb - vs](defb---vs.md), [defi - vs](defi---vs.md)</span></span>
-   <span data-ttu-id="11af4-131">Арифметические инструкции — [ABS-VS](abs---vs.md), [CR-VS](crs---vs.md), [ЛРП-VS](lrp---vs.md), [МОВА-VS](mova---vs.md), [НРМ-VS](nrm---vs.md), [Pow-VS](pow---vs.md), [СГН-VS](sgn---vs.md), [синкос-VS](sincos---vs.md)</span><span class="sxs-lookup"><span data-stu-id="11af4-131">Arithmetic instructions - [abs - vs](abs---vs.md), [crs - vs](crs---vs.md), [lrp - vs](lrp---vs.md), [mova - vs](mova---vs.md), [nrm - vs](nrm---vs.md), [pow - vs](pow---vs.md), [sgn - vs](sgn---vs.md), [sincos - vs](sincos---vs.md)</span></span>
-   <span data-ttu-id="11af4-132">Статические инструкции по управлению потоком — [вызов-VS](call---vs.md), [каллнз bool-VS](callnz-bool---vs.md), [else-VS](else---vs.md), [endif-VS](endif---vs.md), [ендлуп-VS](endloop---vs.md), [ендреп-VS](endrep---vs.md), [Если bool-VS](if-bool---vs.md), [Label-VS](label---vs.md), [цикл-VS](loop---vs.md), [представитель-VS](rep---vs.md), [RET-VS](ret---vs.md)</span><span class="sxs-lookup"><span data-stu-id="11af4-132">Static flow control instructions - [call - vs](call---vs.md), [callnz bool - vs](callnz-bool---vs.md), [else - vs](else---vs.md), [endif - vs](endif---vs.md), [endloop - vs](endloop---vs.md), [endrep - vs](endrep---vs.md), [if bool - vs](if-bool---vs.md), [label - vs](label---vs.md), [loop - vs](loop---vs.md), [rep - vs](rep---vs.md), [ret - vs](ret---vs.md)</span></span>

<span data-ttu-id="11af4-133">Новые регистры:</span><span class="sxs-lookup"><span data-stu-id="11af4-133">New registers:</span></span>

-   <span data-ttu-id="11af4-134">[Константный логический регистр](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) (b \# )</span><span class="sxs-lookup"><span data-stu-id="11af4-134">[Constant Boolean Register](dx9-graphics-reference-asm-vs-registers-constant-boolean.md) (b\#)</span></span>
-   <span data-ttu-id="11af4-135">[Постоянный целочисленный регистр](dx9-graphics-reference-asm-vs-registers-constant-integer.md) (i \# )</span><span class="sxs-lookup"><span data-stu-id="11af4-135">[Constant Integer Register](dx9-graphics-reference-asm-vs-registers-constant-integer.md) (i\#)</span></span>
-   <span data-ttu-id="11af4-136">[Регистр счетчика циклов](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (Al)</span><span class="sxs-lookup"><span data-stu-id="11af4-136">[Loop Counter Register](dx9-graphics-reference-asm-vs-registers-loop-counter.md) (aL)</span></span>

## <a name="vs_2_x-features"></a><span data-ttu-id="11af4-137">\_функции vs 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="11af4-137">vs\_2\_x Features</span></span>

<span data-ttu-id="11af4-138">Новые возможности (D3DCAPS9. VS20Caps):</span><span class="sxs-lookup"><span data-stu-id="11af4-138">New features (D3DCAPS9.VS20Caps):</span></span>

-   <span data-ttu-id="11af4-139">Динамическое управление потоком</span><span class="sxs-lookup"><span data-stu-id="11af4-139">Dynamic flow control</span></span>
-   <span data-ttu-id="11af4-140">Инструкции по вложению для динамических и статических функций управления потоком</span><span class="sxs-lookup"><span data-stu-id="11af4-140">Nesting for dynamic and static flow control instructions</span></span>
-   <span data-ttu-id="11af4-141">Число увеличенных [временных регистров](dx9-graphics-reference-asm-vs-registers-temporary.md)(r \# )</span><span class="sxs-lookup"><span data-stu-id="11af4-141">Number of [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md)s (r\#) increased</span></span>
-   <span data-ttu-id="11af4-142">Предикация</span><span class="sxs-lookup"><span data-stu-id="11af4-142">Predication</span></span>

<span data-ttu-id="11af4-143">Новые инструкции:</span><span class="sxs-lookup"><span data-stu-id="11af4-143">New Instructions:</span></span>

-   <span data-ttu-id="11af4-144">Инструкции по динамическому управлению потоком — [break-VS](break---vs.md), [break \_ -VS](break-comp---vs.md), [бреакп-VS](breakp---vs.md), [каллнз "пред-](callnz-pred---vs.md)VS", if-VS,, [Если "пред](if-pred---vs.md)-VS", " [сетп \_ comp-](setp-comp---vs.md) VS" [ \_ ](if-comp---vs.md)</span><span class="sxs-lookup"><span data-stu-id="11af4-144">Dynamic flow control instructions - [break - vs](break---vs.md), [break\_comp - vs](break-comp---vs.md), [breakp - vs](breakp---vs.md), [callnz pred - vs](callnz-pred---vs.md), [if\_comp - vs](if-comp---vs.md), [if pred - vs](if-pred---vs.md), [setp\_comp - vs](setp-comp---vs.md)</span></span>

<span data-ttu-id="11af4-145">Новые регистры:</span><span class="sxs-lookup"><span data-stu-id="11af4-145">New registers:</span></span>

-   <span data-ttu-id="11af4-146">[Регистр предиката](dx9-graphics-reference-asm-vs-registers-predicate.md) (P0)</span><span class="sxs-lookup"><span data-stu-id="11af4-146">[Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md) (p0)</span></span>

## <a name="vs_3_0-features"></a><span data-ttu-id="11af4-147">\_функции VS 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="11af4-147">vs\_3\_0 Features</span></span>

<span data-ttu-id="11af4-148">Новые возможности:</span><span class="sxs-lookup"><span data-stu-id="11af4-148">New features :</span></span>

-   <span data-ttu-id="11af4-149">Поиск текстур</span><span class="sxs-lookup"><span data-stu-id="11af4-149">Texture lookup</span></span>
-   <span data-ttu-id="11af4-150">Индексируемые [выходные регистры](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o \# )</span><span class="sxs-lookup"><span data-stu-id="11af4-150">Indexable [Output Registers](dx9-graphics-reference-asm-vs-registers-vs-3-0.md) (o\#)</span></span>
-   <span data-ttu-id="11af4-151">Количество [временных регистров](dx9-graphics-reference-asm-vs-registers-temporary.md)(r \# ), увеличенное до 32</span><span class="sxs-lookup"><span data-stu-id="11af4-151">Number of [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md)s (r\#) increased to 32</span></span>

<span data-ttu-id="11af4-152">Новые инструкции:</span><span class="sxs-lookup"><span data-stu-id="11af4-152">New instructions:</span></span>

-   <span data-ttu-id="11af4-153">Инструкция Setup- [дкл \_ самплертипе (SM3-VS ASM)](dcl-samplertype---vs.md)</span><span class="sxs-lookup"><span data-stu-id="11af4-153">Setup instruction - [dcl\_samplerType (sm3 - vs asm)](dcl-samplertype---vs.md)</span></span>
-   <span data-ttu-id="11af4-154">Текстурная инструкция — [текслдл-VS](texldl---vs.md)</span><span class="sxs-lookup"><span data-stu-id="11af4-154">Texture instruction - [texldl - vs](texldl---vs.md)</span></span>

<span data-ttu-id="11af4-155">Новые регистры:</span><span class="sxs-lookup"><span data-stu-id="11af4-155">New registers:</span></span>

-   <span data-ttu-id="11af4-156">[Образцы (Direct3D 9 ASM-VS)](dx9-graphics-reference-asm-vs-registers-sampler.md) \#</span><span class="sxs-lookup"><span data-stu-id="11af4-156">[Sampler (Direct3D 9 asm-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md) (s\#)</span></span>

## <a name="related-topics"></a><span data-ttu-id="11af4-157">См. также</span><span class="sxs-lookup"><span data-stu-id="11af4-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11af4-158">Шейдеры вершин</span><span class="sxs-lookup"><span data-stu-id="11af4-158">Vertex Shaders</span></span>](dx9-graphics-reference-asm-vs.md)
</dt> </dl>

 

 