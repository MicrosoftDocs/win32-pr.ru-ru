---
title: синкос — VS
description: Вычисляет синус и косинус в радианах. | синкос — VS
ms.assetid: 733a3980-ceaf-43dc-a862-923c369e4a65
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ca70a319852346c6e75ba544489d033a861d4c3b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104000244"
---
# <a name="sincos---vs"></a><span data-ttu-id="2f5a2-104">синкос — VS</span><span class="sxs-lookup"><span data-stu-id="2f5a2-104">sincos - vs</span></span>

<span data-ttu-id="2f5a2-105">Вычисляет синус и косинус в радианах.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-105">Computes sine and cosine, in radians.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f5a2-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2f5a2-106">Syntax</span></span>

### <a name="vs_2_0-and-vs_2_x"></a><span data-ttu-id="2f5a2-107">VS \_ 2 \_ 0 и VS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="2f5a2-107">vs\_2\_0 and vs\_2\_x</span></span>



| <span data-ttu-id="2f5a2-108">синкос DST. x</span><span class="sxs-lookup"><span data-stu-id="2f5a2-108">sincos dst.{x\</span></span>|<span data-ttu-id="2f5a2-109">&</span><span class="sxs-lookup"><span data-stu-id="2f5a2-109">y\</span></span>|<span data-ttu-id="2f5a2-110">XY}, src0. x</span><span class="sxs-lookup"><span data-stu-id="2f5a2-110">xy}, src0.{x\</span></span>|<span data-ttu-id="2f5a2-111">&</span><span class="sxs-lookup"><span data-stu-id="2f5a2-111">y\</span></span>|<span data-ttu-id="2f5a2-112">гармошкой</span><span class="sxs-lookup"><span data-stu-id="2f5a2-112">z\</span></span>|<span data-ttu-id="2f5a2-113">w}, src1, src2</span><span class="sxs-lookup"><span data-stu-id="2f5a2-113">w}, src1, src2</span></span> |
|------------------------------------------------------|



 

<span data-ttu-id="2f5a2-114">Где:</span><span class="sxs-lookup"><span data-stu-id="2f5a2-114">Where:</span></span>

-   <span data-ttu-id="2f5a2-115">DST — это регистр назначения, который должен быть [временным регистром](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ).</span><span class="sxs-lookup"><span data-stu-id="2f5a2-115">dst is the destination register and has to be a [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md) (r\#).</span></span> <span data-ttu-id="2f5a2-116">Регистр назначения должен иметь ровно одну из трех масок:. x \| . y \| . XY.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-116">The destination register must have exactly one of the following three masks: .x \| .y \| .xy.</span></span>
-   <span data-ttu-id="2f5a2-117">src0 — это исходный регистр, который предоставляет угол ввода, который должен быть в пределах \[ -Pi, + PI \] .</span><span class="sxs-lookup"><span data-stu-id="2f5a2-117">src0 is a source register that provides the input angle, which must be within \[-pi, +pi\].</span></span> <span data-ttu-id="2f5a2-118">{x \| y \| z \| w} — это требуемая репликация свиззле.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-118">{x\|y\|z\|w} is the required replicate swizzle.</span></span>
-   <span data-ttu-id="2f5a2-119">src1 и src2 являются исходными регистрами и должны быть двумя разными [константами регистра с плавающей запятой](dx9-graphics-reference-asm-vs-registers-constant-float.md) (c \# ).</span><span class="sxs-lookup"><span data-stu-id="2f5a2-119">src1 and src2 are source registers and must be two different [Constant Float Register](dx9-graphics-reference-asm-vs-registers-constant-float.md) (c\#).</span></span> <span data-ttu-id="2f5a2-120">Значения src1 и src2 должны относиться к макросам [**D3DSINCOSCONST1**](/windows/desktop/direct3d9/d3dsincosconst1) и [**D3DSINCOSCONST2**](/windows/desktop/direct3d9/d3dsincosconst2) соответственно.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-120">The values of src1 and src2 must be that of the macros [**D3DSINCOSCONST1**](/windows/desktop/direct3d9/d3dsincosconst1) and [**D3DSINCOSCONST2**](/windows/desktop/direct3d9/d3dsincosconst2) respectively.</span></span>

### <a name="vs_3_0"></a><span data-ttu-id="2f5a2-121">VS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2f5a2-121">vs\_3\_0</span></span>



| <span data-ttu-id="2f5a2-122">синкос DST. x</span><span class="sxs-lookup"><span data-stu-id="2f5a2-122">sincos dst.{x\</span></span>|<span data-ttu-id="2f5a2-123">&</span><span class="sxs-lookup"><span data-stu-id="2f5a2-123">y\</span></span>|<span data-ttu-id="2f5a2-124">XY}, src0. x</span><span class="sxs-lookup"><span data-stu-id="2f5a2-124">xy}, src0.{x\</span></span>|<span data-ttu-id="2f5a2-125">&</span><span class="sxs-lookup"><span data-stu-id="2f5a2-125">y\</span></span>|<span data-ttu-id="2f5a2-126">гармошкой</span><span class="sxs-lookup"><span data-stu-id="2f5a2-126">z\</span></span>|<span data-ttu-id="2f5a2-127">Белая</span><span class="sxs-lookup"><span data-stu-id="2f5a2-127">w}</span></span> |
|------------------------------------------|



 

<span data-ttu-id="2f5a2-128">Где:</span><span class="sxs-lookup"><span data-stu-id="2f5a2-128">Where:</span></span>

-   <span data-ttu-id="2f5a2-129">DST — это регистр назначения, который должен быть [временным регистром](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ).</span><span class="sxs-lookup"><span data-stu-id="2f5a2-129">dst is a destination register and has to be a [Temporary Register](dx9-graphics-reference-asm-vs-registers-temporary.md) (r\#).</span></span> <span data-ttu-id="2f5a2-130">Регистр назначения должен иметь ровно одну из трех масок:. x \| . y \| . XY.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-130">The destination register must have exactly one of the following three masks: .x \| .y \| .xy.</span></span>
-   <span data-ttu-id="2f5a2-131">src0 — это исходный регистр, который предоставляет угол ввода, который должен быть в пределах \[ -Pi, + PI \] .</span><span class="sxs-lookup"><span data-stu-id="2f5a2-131">src0 is a source register that provides the input angle, which must be within \[-pi, +pi\].</span></span> <span data-ttu-id="2f5a2-132">{x \| y \| z \| w} — это требуемая репликация свиззле.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-132">{x\|y\|z\|w} is the required replicate swizzle.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f5a2-133">Примечания</span><span class="sxs-lookup"><span data-stu-id="2f5a2-133">Remarks</span></span>



| <span data-ttu-id="2f5a2-134">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="2f5a2-134">Vertex shader versions</span></span> | <span data-ttu-id="2f5a2-135">1\_1</span><span class="sxs-lookup"><span data-stu-id="2f5a2-135">1\_1</span></span> | <span data-ttu-id="2f5a2-136">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2f5a2-136">2\_0</span></span> | <span data-ttu-id="2f5a2-137">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="2f5a2-137">2\_x</span></span> | <span data-ttu-id="2f5a2-138">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="2f5a2-138">2\_sw</span></span> | <span data-ttu-id="2f5a2-139">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2f5a2-139">3\_0</span></span> | <span data-ttu-id="2f5a2-140">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="2f5a2-140">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="2f5a2-141">синкос</span><span class="sxs-lookup"><span data-stu-id="2f5a2-141">sincos</span></span>                 |      | <span data-ttu-id="2f5a2-142">x</span><span class="sxs-lookup"><span data-stu-id="2f5a2-142">x</span></span>    | <span data-ttu-id="2f5a2-143">x</span><span class="sxs-lookup"><span data-stu-id="2f5a2-143">x</span></span>    | <span data-ttu-id="2f5a2-144">x</span><span class="sxs-lookup"><span data-stu-id="2f5a2-144">x</span></span>     | <span data-ttu-id="2f5a2-145">x</span><span class="sxs-lookup"><span data-stu-id="2f5a2-145">x</span></span>    | <span data-ttu-id="2f5a2-146">x</span><span class="sxs-lookup"><span data-stu-id="2f5a2-146">x</span></span>     |



 

### <a name="vs_2_0-and-vs_2_x-remarks"></a><span data-ttu-id="2f5a2-147">\_Примечания vs 2 \_ 0 и VS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="2f5a2-147">vs\_2\_0 and vs\_2\_x Remarks</span></span>

<span data-ttu-id="2f5a2-148">Для VS \_ 2 \_ 0 и VS \_ 2 \_ x синкос можно использовать с затенения, но с одним ограничением на свиззле [регистра предиката](dx9-graphics-reference-asm-vs-registers-predicate.md) (P0): допускается только репликация свиззле (. x \| . y \| . z \| . w).</span><span class="sxs-lookup"><span data-stu-id="2f5a2-148">For vs\_2\_0 and vs\_2\_x, sincos can be used with predication, but with one restriction to the swizzle of the [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md) (p0): only replicate swizzle (.x \| .y \| .z \| .w) is allowed.</span></span>

<span data-ttu-id="2f5a2-149">Для VS \_ 2 \_ 0 и VS \_ 2 \_ x инструкция работает следующим образом: (V = скалярное значение из src0 с реплицируемой свиззле):</span><span class="sxs-lookup"><span data-stu-id="2f5a2-149">For vs\_2\_0 and vs\_2\_x, the instruction operates as follows: (V = the scalar value from src0 with a replicate swizzle):</span></span>

-   <span data-ttu-id="2f5a2-150">Если маска записи —. x:</span><span class="sxs-lookup"><span data-stu-id="2f5a2-150">If the write mask is .x:</span></span>
    ```
    dest.x = cos( V )
    dest.y is undefined when the instruction completes
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="2f5a2-151">Если маска записи —. y:</span><span class="sxs-lookup"><span data-stu-id="2f5a2-151">If the write mask is .y:</span></span>
    ```
    dest.x is undefined when the instruction completes
    dest.y = sin( V )
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="2f5a2-152">Если маска записи имеет значение. XY:</span><span class="sxs-lookup"><span data-stu-id="2f5a2-152">If the write mask is .xy:</span></span>
    ```
    dest.x = cos( V )
    dest.y = sin( V )
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

### <a name="vs_3_0-remarks"></a><span data-ttu-id="2f5a2-153">\_Примечание VS 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2f5a2-153">vs\_3\_0 Remarks</span></span>

<span data-ttu-id="2f5a2-154">Для VS \_ 3 \_ 0 синкос можно использовать с затенения без каких бы то ни было ограничений.</span><span class="sxs-lookup"><span data-stu-id="2f5a2-154">For vs\_3\_0, sincos can be used with predication without any restriction.</span></span> <span data-ttu-id="2f5a2-155">См. раздел [Регистрация предиката](dx9-graphics-reference-asm-vs-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="2f5a2-155">See [Predicate Register](dx9-graphics-reference-asm-vs-registers-predicate.md).</span></span>

<span data-ttu-id="2f5a2-156">Для VS \_ 3 \_ 0 Инструкция работает следующим образом: (V = скалярное значение из src0 с репликацией свиззле).</span><span class="sxs-lookup"><span data-stu-id="2f5a2-156">For vs\_3\_0, the instruction operates as follows: (V = the scalar value from src0 with a replicate swizzle)</span></span>

-   <span data-ttu-id="2f5a2-157">Если маска записи —. x:</span><span class="sxs-lookup"><span data-stu-id="2f5a2-157">If the write mask is .x:</span></span>
    ```
    dest.x = cos( V )
    dest.y is not touched by the instruction
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="2f5a2-158">Если маска записи —. y:</span><span class="sxs-lookup"><span data-stu-id="2f5a2-158">If the write mask is .y:</span></span>
    ```
    dest.x is not touched by the instruction
    dest.y = sin( V )
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="2f5a2-159">Если маска записи имеет значение. XY:</span><span class="sxs-lookup"><span data-stu-id="2f5a2-159">If the write mask is .xy:</span></span>
    ```
    dest.x = cos( V )
    dest.y = sin( V )
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

<span data-ttu-id="2f5a2-160">Приложение может сопоставлять произвольный угол (в радианах) с Range \[ -Pi, + PI, \] используя следующий псевдокод шейдера:</span><span class="sxs-lookup"><span data-stu-id="2f5a2-160">The application can map an arbitrary angle (in radians) to the range \[-pi, +pi\] using the following shader pseudocode:</span></span>


```
def c0, pi, 0.5, 2*pi, 1/(2*pi)
mad r0.x, input_angle, c0.w, c0.y
frc r0.x, r0.x
mad r0.x, r0.x, c0.z, -c0.x
```



## <a name="related-topics"></a><span data-ttu-id="2f5a2-161">См. также</span><span class="sxs-lookup"><span data-stu-id="2f5a2-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f5a2-162">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="2f5a2-162">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
