---
title: текслдп-PS
description: Предполагаемая Инструкция по загрузке текстуры. Эта инструкция делит входную координату текстуры на четвертый элемент (. a или. w) непосредственно перед выборкой.
ms.assetid: 82e62ba3-a9f5-4afb-8dca-4c54a00843eb
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 045caf6ec922183893df252488946546602d2459
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104339153"
---
# <a name="texldp---ps"></a><span data-ttu-id="9266f-104">текслдп-PS</span><span class="sxs-lookup"><span data-stu-id="9266f-104">texldp - ps</span></span>

<span data-ttu-id="9266f-105">Предполагаемая Инструкция по загрузке текстуры.</span><span class="sxs-lookup"><span data-stu-id="9266f-105">Projected texture load instruction.</span></span> <span data-ttu-id="9266f-106">Эта инструкция делит входную координату текстуры на четвертый элемент (. a или. w) непосредственно перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="9266f-106">This instruction divides the input texture coordinate by the fourth element (.a or .w) just before sampling.</span></span>

## <a name="syntax"></a><span data-ttu-id="9266f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9266f-107">Syntax</span></span>



| <span data-ttu-id="9266f-108">текслдп DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="9266f-108">texldp dst, src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="9266f-109">где</span><span class="sxs-lookup"><span data-stu-id="9266f-109">where</span></span>

-   <span data-ttu-id="9266f-110">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="9266f-110">dst is the destination register.</span></span>
-   <span data-ttu-id="9266f-111">src0 — это исходный регистр, предоставляющий координаты текстуры для образца текстуры.</span><span class="sxs-lookup"><span data-stu-id="9266f-111">src0 is a source register that provides the texture coordinates for the texture sample.</span></span> <span data-ttu-id="9266f-112">См. раздел [регистрация координат текстуры](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span><span class="sxs-lookup"><span data-stu-id="9266f-112">See [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span></span>
-   <span data-ttu-id="9266f-113">src1 определяет [образец (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# , где \# указывает, какой номер образца текстуры следует вычислить.</span><span class="sxs-lookup"><span data-stu-id="9266f-113">src1 identifies the [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), where \# specifies which texture sampler number to sample.</span></span> <span data-ttu-id="9266f-114">Этот образец связан с текстурой и состоянием выборки, определенным в [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span><span class="sxs-lookup"><span data-stu-id="9266f-114">The sampler has associated with it a texture and a sampler state defined by [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span></span>

<span data-ttu-id="9266f-115">Набор ограничений при использовании текслдп см. в разделе [текслд](texld---ps-2-0.md).</span><span class="sxs-lookup"><span data-stu-id="9266f-115">For the set of restrictions when using texldp, see [texld](texld---ps-2-0.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9266f-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="9266f-116">Remarks</span></span>

<span data-ttu-id="9266f-117">текслдп выполняет проекцию координат, считанных из src0, перед выполнением примера.</span><span class="sxs-lookup"><span data-stu-id="9266f-117">texldp performs projection on the coordinates read from src0 before performing the sample.</span></span> <span data-ttu-id="9266f-118">Каждая координата текстуры делится на src0. w, а затем текстура выдается в виде выборки.</span><span class="sxs-lookup"><span data-stu-id="9266f-118">Each texture coordinate is divided by src0.w, then the texture is sampled.</span></span> <span data-ttu-id="9266f-119">По завершении текслдп содержимое src0 не изменяется (если только DST не является одним и тем же регистром).</span><span class="sxs-lookup"><span data-stu-id="9266f-119">When texldp completes, the contents of src0 are unaffected (unless dst is the same register).</span></span> <span data-ttu-id="9266f-120">В качестве альтернативы использованию текслдп можно вручную выполнить деление проекции в шейдере.</span><span class="sxs-lookup"><span data-stu-id="9266f-120">An alternative to using texldp is to manually perform the projection division in the shader.</span></span> <span data-ttu-id="9266f-121">Однако выполнение деления в коде шейдера обычно выполняется медленнее, чем при выполнении инструкции текслдп, поэтому по возможности избегайте таких дополнительных математических вычислений.</span><span class="sxs-lookup"><span data-stu-id="9266f-121">However, performing the division in shader code is usually slower than when performed by the texldp instruction, so avoid such additional math when possible.</span></span>

<span data-ttu-id="9266f-122">Количество координат, необходимых для выполнения образца текстуры для src0, зависит от того, как был объявлен src1, а также от компонента. w.</span><span class="sxs-lookup"><span data-stu-id="9266f-122">The number of coordinates required for src0 to perform the texture sample depends on how src1 was declared, plus the .w component.</span></span> <span data-ttu-id="9266f-123">Типы образцов объявляются с помощью [дкл \_ самплертипе (SM2, SM3-PS ASM)](dcl-samplertype---ps.md).</span><span class="sxs-lookup"><span data-stu-id="9266f-123">Sampler types are declared with [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md).</span></span> <span data-ttu-id="9266f-124">Если src1 объявлен как 2D-образец, src0 должен содержать координаты. ксив; Если src1 объявляется как образец куба или как образец тома, src0 должен содержать координаты. ксизв.</span><span class="sxs-lookup"><span data-stu-id="9266f-124">If src1 is declared as a 2D sampler, then src0 must contain .xyw coordinates; if src1 is declared as either a cube sampler or a volume sampler, then src0 must contain .xyzw coordinates.</span></span> <span data-ttu-id="9266f-125">Допускается выборка двухмерной текстуры с помощью координат. ксизв (координата. z игнорируется).</span><span class="sxs-lookup"><span data-stu-id="9266f-125">Sampling a 2D texture with .xyzw coordinates is allowed (the .z coordinate is ignored).</span></span>

<span data-ttu-id="9266f-126">Если исходная текстура содержит менее четырех компонентов, значения по умолчанию помещаются в отсутствующие компоненты.</span><span class="sxs-lookup"><span data-stu-id="9266f-126">If the source texture contains fewer than four components, defaults are placed in the missing components.</span></span> <span data-ttu-id="9266f-127">Значения по умолчанию зависят от формата текстуры, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="9266f-127">Defaults depend on the texture format as shown in the following table.</span></span>



| <span data-ttu-id="9266f-128">Формат текстуры</span><span class="sxs-lookup"><span data-stu-id="9266f-128">Texture Format</span></span>                                                                                          | <span data-ttu-id="9266f-129">Значения по умолчанию для отсутствующих компонентов</span><span class="sxs-lookup"><span data-stu-id="9266f-129">Default Values for missing components</span></span> |
|---------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span data-ttu-id="9266f-130">D3DFMT \_ R5G6B5, D3DFMT \_ R8G8B8, D3DFMT \_ 8, D3DFMT \_ L16, D3DFMT \_ R3G3B2, D3DFMT \_ CxV8U8, D3DFMT \_ L6V5U5</span><span class="sxs-lookup"><span data-stu-id="9266f-130">D3DFMT\_R5G6B5, D3DFMT\_R8G8B8, D3DFMT\_L8, D3DFMT\_L16, D3DFMT\_R3G3B2, D3DFMT\_CxV8U8, D3DFMT\_L6V5U5</span></span> | <span data-ttu-id="9266f-131">A = 1,0</span><span class="sxs-lookup"><span data-stu-id="9266f-131">A = 1.0</span></span>                               |
| <span data-ttu-id="9266f-132">D3DFMT \_ V8U8, D3DFMT \_ V16U16, D3DFMT \_ G16R16, D3DFMT \_ G16R16F, D3DFMT \_ G32R32F</span><span class="sxs-lookup"><span data-stu-id="9266f-132">D3DFMT\_V8U8, D3DFMT\_V16U16, D3DFMT\_G16R16, D3DFMT\_G16R16F, D3DFMT\_G32R32F</span></span>                          | <span data-ttu-id="9266f-133">B = A = 1,0</span><span class="sxs-lookup"><span data-stu-id="9266f-133">B = A = 1.0</span></span>                           |
| <span data-ttu-id="9266f-134">D3DFMT \_ A8</span><span class="sxs-lookup"><span data-stu-id="9266f-134">D3DFMT\_A8</span></span>                                                                                              | <span data-ttu-id="9266f-135">R = G = B = 0,0</span><span class="sxs-lookup"><span data-stu-id="9266f-135">R = G = B = 0.0</span></span>                       |
| <span data-ttu-id="9266f-136">D3DFMT \_ R16F, D3DFMT \_ R32F</span><span class="sxs-lookup"><span data-stu-id="9266f-136">D3DFMT\_R16F, D3DFMT\_R32F</span></span>                                                                              | <span data-ttu-id="9266f-137">G = B = A = 1,0</span><span class="sxs-lookup"><span data-stu-id="9266f-137">G = B = A = 1.0</span></span>                       |
| <span data-ttu-id="9266f-138">Все форматы глубины и трафарета</span><span class="sxs-lookup"><span data-stu-id="9266f-138">All depth/stencil formats</span></span>                                                                               | <span data-ttu-id="9266f-139">R = B = 0,0, A = 1,0</span><span class="sxs-lookup"><span data-stu-id="9266f-139">R = B = 0.0, A = 1.0</span></span>                  |



 

<span data-ttu-id="9266f-140">Эта инструкция поддерживается в следующих версиях:</span><span class="sxs-lookup"><span data-stu-id="9266f-140">This instruction is supported in the following versions:</span></span>



| <span data-ttu-id="9266f-141">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="9266f-141">Pixel shader versions</span></span> | <span data-ttu-id="9266f-142">1\_1</span><span class="sxs-lookup"><span data-stu-id="9266f-142">1\_1</span></span> | <span data-ttu-id="9266f-143">1\_2</span><span class="sxs-lookup"><span data-stu-id="9266f-143">1\_2</span></span> | <span data-ttu-id="9266f-144">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="9266f-144">1\_3</span></span> | <span data-ttu-id="9266f-145">1\_4</span><span class="sxs-lookup"><span data-stu-id="9266f-145">1\_4</span></span> | <span data-ttu-id="9266f-146">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9266f-146">2\_0</span></span> | <span data-ttu-id="9266f-147">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="9266f-147">2\_x</span></span> | <span data-ttu-id="9266f-148">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="9266f-148">2\_sw</span></span> | <span data-ttu-id="9266f-149">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9266f-149">3\_0</span></span> | <span data-ttu-id="9266f-150">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="9266f-150">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="9266f-151">текслдп</span><span class="sxs-lookup"><span data-stu-id="9266f-151">texldp</span></span>                |      |      |      |      | <span data-ttu-id="9266f-152">x</span><span class="sxs-lookup"><span data-stu-id="9266f-152">x</span></span>    | <span data-ttu-id="9266f-153">x</span><span class="sxs-lookup"><span data-stu-id="9266f-153">x</span></span>    | <span data-ttu-id="9266f-154">x</span><span class="sxs-lookup"><span data-stu-id="9266f-154">x</span></span>     | <span data-ttu-id="9266f-155">x</span><span class="sxs-lookup"><span data-stu-id="9266f-155">x</span></span>    | <span data-ttu-id="9266f-156">x</span><span class="sxs-lookup"><span data-stu-id="9266f-156">x</span></span>     |



 

### <a name="ps_2_0-and-ps_2_x"></a><span data-ttu-id="9266f-157">PS \_ 2 \_ 0 и PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="9266f-157">ps\_2\_0 and ps\_2\_x</span></span>

<span data-ttu-id="9266f-158">DST должен быть [временным регистром](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ), и допускается только ксизв маска (маска по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="9266f-158">dst must be a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) and only .xyzw mask (default mask) is allowed.</span></span>

<span data-ttu-id="9266f-159">src0 должен быть либо [регистром координаты текстуры](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t \# ), либо [временным регистром](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) без модификатора или свиззле.</span><span class="sxs-lookup"><span data-stu-id="9266f-159">src0 must be either a [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t\#) or a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#), with no modifier or swizzle.</span></span>

<span data-ttu-id="9266f-160">src1 должны быть [образцами (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) без \# модификатора или свиззле.</span><span class="sxs-lookup"><span data-stu-id="9266f-160">src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), with no modifier or swizzle.</span></span>

<span data-ttu-id="9266f-161">Если \_ \_ бит крепления D3DD3DPSHADERCAPS2 0 нодепендентреадлимит не установлен (в D3DPSHADERCAPS2 \_ 0), данная инструкция текстуры ([текслд](texld---ps-1-4.md), текслдп, [текслдб-PS](texldb---ps.md), [текслдд](texldd---ps.md) ) может быть зависеть от третьего порядка.</span><span class="sxs-lookup"><span data-stu-id="9266f-161">If the D3DD3DPSHADERCAPS2\_0\_NODEPENDENTREADLIMIT cap bit is not set (in D3DPSHADERCAPS2\_0), a given texture instruction ([texld](texld---ps-1-4.md), texldp, [texldb - ps](texldb---ps.md), [texldd](texldd---ps.md) ) may be dependent upon, at most, third order.</span></span> <span data-ttu-id="9266f-162">Инструкция текстуры, зависимая от первого порядка, представляет собой текстурную инструкцию, в которой одно из следующих:</span><span class="sxs-lookup"><span data-stu-id="9266f-162">A first-order dependent texture instruction is a texture instruction in which either:</span></span>

-   <span data-ttu-id="9266f-163">src0 является [временным регистром](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# )</span><span class="sxs-lookup"><span data-stu-id="9266f-163">src0 is a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#)</span></span>
-   <span data-ttu-id="9266f-164">летнее время было записано еще раз.</span><span class="sxs-lookup"><span data-stu-id="9266f-164">dst was previously written, now being written again.</span></span>

<span data-ttu-id="9266f-165">Инструкция текстуры, зависимая от второго порядка, определяется как Текстурная инструкция, которая считывает или выполняет запись [во временный регистр](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ), содержимое которого перед выполнением инструкции текстуры зависят (возможно, косвенно) от результата инструкции текстуры, зависящей от первого заказа.</span><span class="sxs-lookup"><span data-stu-id="9266f-165">A second-order dependent texture instruction is defined as a texture instruction that reads or writes to a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) whose contents, before executing the texture instruction, depend (perhaps indirectly) on the outcome of a first-order dependent texture instruction.</span></span> <span data-ttu-id="9266f-166">Инструкция текстуры, зависимая от (<sup>n),</sup>является производной от (n-1)-<sup>го</sup>порядка текстуры.</span><span class="sxs-lookup"><span data-stu-id="9266f-166">An (n)<sup>th</sup>-order dependent texture instruction derives from an (n - 1)<sup>th</sup>-order texture instruction.</span></span>

### <a name="ps_3_0"></a><span data-ttu-id="9266f-167">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="9266f-167">ps\_3\_0</span></span>

<span data-ttu-id="9266f-168">Для PS \_ 3 \_ 0 src1 должен быть [образца (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# без модификатора.</span><span class="sxs-lookup"><span data-stu-id="9266f-168">For ps\_3\_0, src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), with no modifier.</span></span> <span data-ttu-id="9266f-169">Свиззле разрешено для src1, и при применении результаты поиска текстур предварительно свиззлед перед записью в летнее время.</span><span class="sxs-lookup"><span data-stu-id="9266f-169">Swizzle is allowed on src1, and when applied, the texture lookup results are pre-swizzled before written to dst.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9266f-170">См. также</span><span class="sxs-lookup"><span data-stu-id="9266f-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9266f-171">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="9266f-171">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 