---
title: синкос-PS
description: Вычисляет синус и косинус в радианах. | синкос-PS
ms.assetid: 639237ea-1b7a-4959-9093-78f134c11863
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1e7ccdca91af206862384ae14cf25a85d0817814
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998138"
---
# <a name="sincos---ps"></a><span data-ttu-id="78968-104">синкос-PS</span><span class="sxs-lookup"><span data-stu-id="78968-104">sincos - ps</span></span>

<span data-ttu-id="78968-105">Вычисляет синус и косинус в радианах.</span><span class="sxs-lookup"><span data-stu-id="78968-105">Computes sine and cosine, in radians.</span></span>

## <a name="syntax"></a><span data-ttu-id="78968-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="78968-106">Syntax</span></span>

### <a name="ps_2_0-and-ps_2_x"></a><span data-ttu-id="78968-107">PS \_ 2 \_ 0 и PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="78968-107">ps\_2\_0 and ps\_2\_x</span></span>



| <span data-ttu-id="78968-108">синкос DST. x</span><span class="sxs-lookup"><span data-stu-id="78968-108">sincos dst.{x\</span></span>|<span data-ttu-id="78968-109">&</span><span class="sxs-lookup"><span data-stu-id="78968-109">y\</span></span>|<span data-ttu-id="78968-110">XY}, src0. x</span><span class="sxs-lookup"><span data-stu-id="78968-110">xy}, src0.{x\</span></span>|<span data-ttu-id="78968-111">&</span><span class="sxs-lookup"><span data-stu-id="78968-111">y\</span></span>|<span data-ttu-id="78968-112">гармошкой</span><span class="sxs-lookup"><span data-stu-id="78968-112">z\</span></span>|<span data-ttu-id="78968-113">w}, src1, src2</span><span class="sxs-lookup"><span data-stu-id="78968-113">w}, src1, src2</span></span> |
|------------------------------------------------------|



 

<span data-ttu-id="78968-114">Где:</span><span class="sxs-lookup"><span data-stu-id="78968-114">Where:</span></span>

-   <span data-ttu-id="78968-115">DST — это регистр назначения, который должен быть [временным регистром](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ).</span><span class="sxs-lookup"><span data-stu-id="78968-115">dst is the destination register and has to be a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#).</span></span> <span data-ttu-id="78968-116">Регистр назначения должен иметь ровно одну из трех масок:. x \| . y \| . XY.</span><span class="sxs-lookup"><span data-stu-id="78968-116">The destination register must have exactly one of the following three masks: .x \| .y \| .xy.</span></span>
-   <span data-ttu-id="78968-117">src0 — это исходный регистр, который предоставляет угол ввода, который должен быть в пределах \[ -Pi, + PI \] .</span><span class="sxs-lookup"><span data-stu-id="78968-117">src0 is a source register that provides the input angle, which must be within \[-pi, +pi\].</span></span> <span data-ttu-id="78968-118">{x \| y \| z \| w} — это требуемая репликация свиззле.</span><span class="sxs-lookup"><span data-stu-id="78968-118">{x\|y\|z\|w} is the required replicate swizzle.</span></span>
-   <span data-ttu-id="78968-119">src1 и src2 являются исходными регистрами и должны быть двумя разными [константами с плавающей запятой](dx9-graphics-reference-asm-ps-registers-constant-float.md)(c \# ).</span><span class="sxs-lookup"><span data-stu-id="78968-119">src1 and src2 are source registers and must be two different [Constant Float Register](dx9-graphics-reference-asm-ps-registers-constant-float.md)s (c\#).</span></span> <span data-ttu-id="78968-120">Значения src1 и src2 должны относиться к макросам [**D3DSINCOSCONST1**](/windows/desktop/direct3d9/d3dsincosconst1) и [**D3DSINCOSCONST2**](/windows/desktop/direct3d9/d3dsincosconst2) соответственно.</span><span class="sxs-lookup"><span data-stu-id="78968-120">The values of src1 and src2 must be that of the macros [**D3DSINCOSCONST1**](/windows/desktop/direct3d9/d3dsincosconst1) and [**D3DSINCOSCONST2**](/windows/desktop/direct3d9/d3dsincosconst2) respectively.</span></span>

### <a name="ps_3_0"></a><span data-ttu-id="78968-121">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="78968-121">ps\_3\_0</span></span>



| <span data-ttu-id="78968-122">синкос DST. x</span><span class="sxs-lookup"><span data-stu-id="78968-122">sincos dst.{x\</span></span>|<span data-ttu-id="78968-123">&</span><span class="sxs-lookup"><span data-stu-id="78968-123">y\</span></span>|<span data-ttu-id="78968-124">XY}, src0. x</span><span class="sxs-lookup"><span data-stu-id="78968-124">xy}, src0.{x\</span></span>|<span data-ttu-id="78968-125">&</span><span class="sxs-lookup"><span data-stu-id="78968-125">y\</span></span>|<span data-ttu-id="78968-126">гармошкой</span><span class="sxs-lookup"><span data-stu-id="78968-126">z\</span></span>|<span data-ttu-id="78968-127">Белая</span><span class="sxs-lookup"><span data-stu-id="78968-127">w}</span></span> |
|------------------------------------------|



 

<span data-ttu-id="78968-128">Где:</span><span class="sxs-lookup"><span data-stu-id="78968-128">Where:</span></span>

-   <span data-ttu-id="78968-129">DST — это регистр назначения, который должен быть [временным регистром](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ).</span><span class="sxs-lookup"><span data-stu-id="78968-129">dst is a destination register and has to be a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#).</span></span> <span data-ttu-id="78968-130">Регистр назначения должен иметь ровно одну из трех масок:. x \| . y \| . XY.</span><span class="sxs-lookup"><span data-stu-id="78968-130">The destination register must have exactly one of the following three masks: .x \| .y \| .xy.</span></span>
-   <span data-ttu-id="78968-131">src0 — это исходный регистр, который предоставляет угол ввода, который должен быть в пределах \[ -Pi, + PI \] .</span><span class="sxs-lookup"><span data-stu-id="78968-131">src0 is a source register that provides the input angle, which must be within \[-pi, +pi\].</span></span> <span data-ttu-id="78968-132">{x \| y \| z \| w} — это требуемая репликация свиззле.</span><span class="sxs-lookup"><span data-stu-id="78968-132">{x\|y\|z\|w} is the required replicate swizzle.</span></span>

## <a name="remarks"></a><span data-ttu-id="78968-133">Примечания</span><span class="sxs-lookup"><span data-stu-id="78968-133">Remarks</span></span>



| <span data-ttu-id="78968-134">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="78968-134">Pixel shader versions</span></span> | <span data-ttu-id="78968-135">1\_1</span><span class="sxs-lookup"><span data-stu-id="78968-135">1\_1</span></span> | <span data-ttu-id="78968-136">1\_2</span><span class="sxs-lookup"><span data-stu-id="78968-136">1\_2</span></span> | <span data-ttu-id="78968-137">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="78968-137">1\_3</span></span> | <span data-ttu-id="78968-138">1\_4</span><span class="sxs-lookup"><span data-stu-id="78968-138">1\_4</span></span> | <span data-ttu-id="78968-139">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="78968-139">2\_0</span></span> | <span data-ttu-id="78968-140">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="78968-140">2\_x</span></span> | <span data-ttu-id="78968-141">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="78968-141">2\_sw</span></span> | <span data-ttu-id="78968-142">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="78968-142">3\_0</span></span> | <span data-ttu-id="78968-143">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="78968-143">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="78968-144">синкос</span><span class="sxs-lookup"><span data-stu-id="78968-144">sincos</span></span>                |      |      |      |      | <span data-ttu-id="78968-145">x</span><span class="sxs-lookup"><span data-stu-id="78968-145">x</span></span>    | <span data-ttu-id="78968-146">x</span><span class="sxs-lookup"><span data-stu-id="78968-146">x</span></span>    | <span data-ttu-id="78968-147">x</span><span class="sxs-lookup"><span data-stu-id="78968-147">x</span></span>     | <span data-ttu-id="78968-148">x</span><span class="sxs-lookup"><span data-stu-id="78968-148">x</span></span>    | <span data-ttu-id="78968-149">x</span><span class="sxs-lookup"><span data-stu-id="78968-149">x</span></span>     |



 

### <a name="ps_2_0-and-ps_2_x"></a><span data-ttu-id="78968-150">PS \_ 2 \_ 0 и PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="78968-150">ps\_2\_0 and ps\_2\_x</span></span>

<span data-ttu-id="78968-151">Для PS \_ 2 \_ 0 и PS \_ 2 \_ x синкос можно использовать с затенения, но с одним ограничением на свиззле [регистра предиката](dx9-graphics-reference-asm-ps-registers-predicate.md) (P0): допускается только репликация свиззле (. x \| . y \| . z \| . w).</span><span class="sxs-lookup"><span data-stu-id="78968-151">For ps\_2\_0 and ps\_2\_x, sincos can be used with predication, but with one restriction to the swizzle of the [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md) (p0): only replicate swizzle (.x \| .y \| .z \| .w) is allowed.</span></span>

<span data-ttu-id="78968-152">Для PS \_ 2 \_ 0 и PS \_ 2 \_ x инструкция работает следующим образом (V = скалярное значение из src0 с реплицируемой свиззле):</span><span class="sxs-lookup"><span data-stu-id="78968-152">For ps\_2\_0 and ps\_2\_x, the instruction operates as follows (V = the scalar value from src0 with a replicate swizzle):</span></span>

-   <span data-ttu-id="78968-153">Если маска записи —. x:</span><span class="sxs-lookup"><span data-stu-id="78968-153">If the write mask is .x:</span></span>
    ```
    dest.x = cos(V)
    dest.y is undefined when the instruction completes
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="78968-154">Если маска записи —. y:</span><span class="sxs-lookup"><span data-stu-id="78968-154">If the write mask is .y:</span></span>
    ```
    dest.x is undefined when the instruction completes
    dest.y = sin(V)
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="78968-155">Если маска записи имеет значение. XY:</span><span class="sxs-lookup"><span data-stu-id="78968-155">If the write mask is .xy:</span></span>
    ```
    dest.x = cos(V)
    dest.y = sin(V)
    dest.z is undefined when the instruction completes
    dest.w is not touched by the instruction
    ```

    

### <a name="ps_3_0"></a><span data-ttu-id="78968-156">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="78968-156">ps\_3\_0</span></span>

<span data-ttu-id="78968-157">Для PS \_ 3 \_ 0 синкос можно использовать с затенения без каких бы то ни было ограничений.</span><span class="sxs-lookup"><span data-stu-id="78968-157">For ps\_3\_0, sincos can be used with predication without any restriction.</span></span> <span data-ttu-id="78968-158">См. раздел [Регистрация предиката](dx9-graphics-reference-asm-ps-registers-predicate.md).</span><span class="sxs-lookup"><span data-stu-id="78968-158">See [Predicate Register](dx9-graphics-reference-asm-ps-registers-predicate.md).</span></span>

<span data-ttu-id="78968-159">Для PS \_ 3 \_ 0 Инструкция работает следующим образом (V = скалярное значение из src0 с реплицируемой свиззле):</span><span class="sxs-lookup"><span data-stu-id="78968-159">For ps\_3\_0, the instruction operates as follows (V = the scalar value from src0 with a replicate swizzle):</span></span>

-   <span data-ttu-id="78968-160">Если маска записи —. x:</span><span class="sxs-lookup"><span data-stu-id="78968-160">If the write mask is .x:</span></span>
    ```
    dest.x = cos(V)
    dest.y is not touched by the instruction
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="78968-161">Если маска записи —. y:</span><span class="sxs-lookup"><span data-stu-id="78968-161">If the write mask is .y:</span></span>
    ```
    dest.x is not touched by the instruction
    dest.y = sin(V)
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

-   <span data-ttu-id="78968-162">Если маска записи имеет значение. XY:</span><span class="sxs-lookup"><span data-stu-id="78968-162">If the write mask is .xy:</span></span>
    ```
    dest.x = cos(V)
    dest.y = sin(V)
    dest.z is not touched by the instruction
    dest.w is not touched by the instruction
    ```

    

<span data-ttu-id="78968-163">Приложение может сопоставлять произвольный угол (в радианах) с Range \[ -Pi, + PI, \] используя следующий псевдокод шейдера:</span><span class="sxs-lookup"><span data-stu-id="78968-163">The application can map an arbitrary angle (in radians) to the range \[-pi, +pi\] using the following shader pseudocode:</span></span>


```
def c0, pi, 0.5, 2*pi, 1/(2*pi)
mad r0.x, input_angle, c0.w, c0.y
frc r0.x, r0.x
mad r0.x, r0.x, c0.z, -c0.x
```



## <a name="related-topics"></a><span data-ttu-id="78968-164">См. также</span><span class="sxs-lookup"><span data-stu-id="78968-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78968-165">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="78968-165">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 
