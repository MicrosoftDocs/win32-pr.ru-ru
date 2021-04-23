---
title: текслдб-PS
description: Инструкция по загрузке смещенной текстуры. В этой инструкции используется четвертый элемент (. a или. w) для смещения уровня детализации для выборки текстуры непосредственно перед выборкой.
ms.assetid: cafd72c9-b7bb-4e3f-8a8c-de26a4446864
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 912c4c61f6c1f2b6bef46c7c5b6ea17223df5eb8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134018"
---
# <a name="texldb---ps"></a><span data-ttu-id="ef568-104">текслдб-PS</span><span class="sxs-lookup"><span data-stu-id="ef568-104">texldb - ps</span></span>

<span data-ttu-id="ef568-105">Инструкция по загрузке смещенной текстуры.</span><span class="sxs-lookup"><span data-stu-id="ef568-105">Biased texture load instruction.</span></span> <span data-ttu-id="ef568-106">В этой инструкции используется четвертый элемент (. a или. w) для смещения уровня детализации для выборки текстуры непосредственно перед выборкой.</span><span class="sxs-lookup"><span data-stu-id="ef568-106">This instruction uses the fourth element (.a or .w) to bias the texture-sampling level-of-detail just before sampling.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef568-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ef568-107">Syntax</span></span>



| <span data-ttu-id="ef568-108">текслдб DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="ef568-108">texldb dst, src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="ef568-109">Где:</span><span class="sxs-lookup"><span data-stu-id="ef568-109">Where:</span></span>

-   <span data-ttu-id="ef568-110">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="ef568-110">dst is the destination register.</span></span>
-   <span data-ttu-id="ef568-111">src0 — это исходный регистр, предоставляющий координаты текстуры для образца текстуры.</span><span class="sxs-lookup"><span data-stu-id="ef568-111">src0 is a source register that provides the texture coordinates for the texture sample.</span></span> <span data-ttu-id="ef568-112">См. раздел [регистрация координат текстуры](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span><span class="sxs-lookup"><span data-stu-id="ef568-112">See [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md).</span></span>
-   <span data-ttu-id="ef568-113">src1 определяет [образец (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# , где \# указывает, какой номер образца текстуры следует вычислить.</span><span class="sxs-lookup"><span data-stu-id="ef568-113">src1 identifies the [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), where \# specifies which texture sampler number to sample.</span></span> <span data-ttu-id="ef568-114">Этот образец связан с текстурой и состоянием выборки, определенным в [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span><span class="sxs-lookup"><span data-stu-id="ef568-114">The sampler has associated with it a texture and a sampler state defined by [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span></span>

<span data-ttu-id="ef568-115">Ограничения при использовании текслдб см. в описании инструкций [текслд-PS \_ 2 \_ 0 и up](texld---ps-2-0.md) .</span><span class="sxs-lookup"><span data-stu-id="ef568-115">For the restrictions when using texldb, see the [texld - ps\_2\_0 and up](texld---ps-2-0.md) instruction.</span></span>

### <a name="ps_2_0-and-ps_2_x"></a><span data-ttu-id="ef568-116">PS \_ 2 \_ 0 и PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="ef568-116">ps\_2\_0 and ps\_2\_x</span></span>

<span data-ttu-id="ef568-117">DST должен быть [временным регистром](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ), и допускается только ксизв маска (маска по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="ef568-117">dst must be a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) and only .xyzw mask (default mask) is allowed.</span></span>

<span data-ttu-id="ef568-118">src0 должен быть либо [регистром координаты текстуры](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t \# ), либо [временным регистром](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) без модификатора или свиззле.</span><span class="sxs-lookup"><span data-stu-id="ef568-118">src0 must be either a [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t\#) or a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#), with no modifier or swizzle.</span></span>

<span data-ttu-id="ef568-119">src1 должны быть [образцами (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) без \# модификатора или свиззле.</span><span class="sxs-lookup"><span data-stu-id="ef568-119">src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), with no modifier or swizzle.</span></span>

<span data-ttu-id="ef568-120">Если \_ \_ бит крепления D3DD3DPSHADERCAPS2 0 нодепендентреадлимит не установлен (в D3DPSHADERCAPS2 \_ 0), данная инструкция текстуры (текслд, текслдп, текслдб, текслдд) может быть зависеть от третьего порядка.</span><span class="sxs-lookup"><span data-stu-id="ef568-120">If the D3DD3DPSHADERCAPS2\_0\_NODEPENDENTREADLIMIT cap bit is not set (in D3DPSHADERCAPS2\_0), a given texture instruction (texld, texldp, texldb, texldd) may be dependent upon, at most, third order.</span></span> <span data-ttu-id="ef568-121">Инструкция текстуры, зависимая от первого порядка, представляет собой текстурную инструкцию, в которой одно из следующих:</span><span class="sxs-lookup"><span data-stu-id="ef568-121">A first-order dependent texture instruction is a texture instruction in which either:</span></span>

-   <span data-ttu-id="ef568-122">src0 — это [временный регистр](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ).</span><span class="sxs-lookup"><span data-stu-id="ef568-122">src0 is a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#).</span></span>
-   <span data-ttu-id="ef568-123">летнее время было записано еще раз.</span><span class="sxs-lookup"><span data-stu-id="ef568-123">dst was previously written, now being written again.</span></span>

<span data-ttu-id="ef568-124">Инструкция текстуры, зависимая от второго порядка, определяется как Текстурная инструкция, которая считывает или выполняет запись [во временный регистр](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ), содержимое которого перед выполнением инструкции текстуры зависят (возможно, косвенно) от результата инструкции текстуры, зависящей от первого заказа.</span><span class="sxs-lookup"><span data-stu-id="ef568-124">A second-order dependent texture instruction is defined as a texture instruction that reads or writes to a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) whose contents, before executing the texture instruction, depend (perhaps indirectly) on the outcome of a first-order dependent texture instruction.</span></span> <span data-ttu-id="ef568-125">Инструкция текстуры, зависимая от (<sup>n),</sup>является производной от (n-1)-<sup>го</sup>порядка текстуры.</span><span class="sxs-lookup"><span data-stu-id="ef568-125">An (n)<sup>th</sup>-order dependent texture instruction derives from an (n - 1)<sup>th</sup>-order texture instruction.</span></span>

### <a name="ps_3_0"></a><span data-ttu-id="ef568-126">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ef568-126">ps\_3\_0</span></span>

<span data-ttu-id="ef568-127">src1 должны быть [образцами (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) без \# модификатора.</span><span class="sxs-lookup"><span data-stu-id="ef568-127">src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), with no modifier.</span></span> <span data-ttu-id="ef568-128">Свиззле разрешено для src1, и при применении результаты поиска текстур предварительно свиззлед перед записью в летнее время.</span><span class="sxs-lookup"><span data-stu-id="ef568-128">Swizzle is allowed on src1, and when applied, the texture lookup results are pre-swizzled before written to dst.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef568-129">Примечания</span><span class="sxs-lookup"><span data-stu-id="ef568-129">Remarks</span></span>



| <span data-ttu-id="ef568-130">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="ef568-130">Pixel shader versions</span></span> | <span data-ttu-id="ef568-131">1\_1</span><span class="sxs-lookup"><span data-stu-id="ef568-131">1\_1</span></span> | <span data-ttu-id="ef568-132">1\_2</span><span class="sxs-lookup"><span data-stu-id="ef568-132">1\_2</span></span> | <span data-ttu-id="ef568-133">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="ef568-133">1\_3</span></span> | <span data-ttu-id="ef568-134">1\_4</span><span class="sxs-lookup"><span data-stu-id="ef568-134">1\_4</span></span> | <span data-ttu-id="ef568-135">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ef568-135">2\_0</span></span> | <span data-ttu-id="ef568-136">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="ef568-136">2\_x</span></span> | <span data-ttu-id="ef568-137">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="ef568-137">2\_sw</span></span> | <span data-ttu-id="ef568-138">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="ef568-138">3\_0</span></span> | <span data-ttu-id="ef568-139">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="ef568-139">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="ef568-140">текслдб</span><span class="sxs-lookup"><span data-stu-id="ef568-140">texldb</span></span>                |      |      |      |      | <span data-ttu-id="ef568-141">x</span><span class="sxs-lookup"><span data-stu-id="ef568-141">x</span></span>    | <span data-ttu-id="ef568-142">x</span><span class="sxs-lookup"><span data-stu-id="ef568-142">x</span></span>    | <span data-ttu-id="ef568-143">x</span><span class="sxs-lookup"><span data-stu-id="ef568-143">x</span></span>     | <span data-ttu-id="ef568-144">x</span><span class="sxs-lookup"><span data-stu-id="ef568-144">x</span></span>    | <span data-ttu-id="ef568-145">x</span><span class="sxs-lookup"><span data-stu-id="ef568-145">x</span></span>     |



 

<span data-ttu-id="ef568-146">текслдб отменяет уровень детализации mipmap, вычисленный обычным образом как часть примера процесса с помощью значения (со знаком) в src0. w.</span><span class="sxs-lookup"><span data-stu-id="ef568-146">texldb biases the mipmap level-of-detail, computed normally as part of the sample process by the (signed) value in src0.w.</span></span> <span data-ttu-id="ef568-147">Положительные значения смещения приведут к тому, что выбирается меньшая MIP-карты, и наоборот.</span><span class="sxs-lookup"><span data-stu-id="ef568-147">Positive bias values will result in smaller mipmaps being selected and vice versa.</span></span> <span data-ttu-id="ef568-148">Для PS \_ 2 \_ 0 и PS \_ 2 \_ x значения смещения могут находиться в диапазоне от \[ -3,0, + 3,0 \] .</span><span class="sxs-lookup"><span data-stu-id="ef568-148">For ps\_2\_0 and ps\_2\_x, bias values can be within the range \[-3.0, +3.0\].</span></span> <span data-ttu-id="ef568-149">Для PS \_ 3 \_ 0 значения смещения могут находиться в диапазоне от \[ -16,0, + 15,0 \] .</span><span class="sxs-lookup"><span data-stu-id="ef568-149">For ps\_3\_0, bias values can be within the range \[-16.0, +15.0\].</span></span> <span data-ttu-id="ef568-150">Значения смещения за пределами этих диапазонов приводят к неопределенным результатам.</span><span class="sxs-lookup"><span data-stu-id="ef568-150">Bias values outside these ranges produce undefined results.</span></span> <span data-ttu-id="ef568-151">Состояние образца D3DSAMP \_ мипмаплодбиас по-прежнему соблюдается, а к нему добавляется сдвиг текслдб, но для каждого пикселя.</span><span class="sxs-lookup"><span data-stu-id="ef568-151">The sampler state D3DSAMP\_MIPMAPLODBIAS is still honored, and the texldb bias is added to this, but on a per-pixel basis.</span></span> <span data-ttu-id="ef568-152">После того как пересмещенный уровень детализации будет вычислен, D3DSAMP \_ максмиплевел по-прежнему соблюдается и выполняется образец текстуры.</span><span class="sxs-lookup"><span data-stu-id="ef568-152">After the biased level-of-detail is computed, D3DSAMP\_MAXMIPLEVEL is still honored and the texture sample occurs.</span></span> <span data-ttu-id="ef568-153">После текслдб содержимое src0 не изменяется (если только DST не является одним и тем же регистром).</span><span class="sxs-lookup"><span data-stu-id="ef568-153">After texldb, the contents of src0 are unaffected (unless dst is the same register).</span></span>

<span data-ttu-id="ef568-154">Количество координат, необходимых для выполнения образца текстуры для src0, зависит от того, как был объявлен src1, а также от компонента. w.</span><span class="sxs-lookup"><span data-stu-id="ef568-154">The number of coordinates required for src0 to perform the texture sample depends on how src1 was declared, plus the .w component.</span></span> <span data-ttu-id="ef568-155">Типы образцов объявляются с помощью [дкл \_ самплертипе (SM2, SM3-PS ASM)](dcl-samplertype---ps.md).</span><span class="sxs-lookup"><span data-stu-id="ef568-155">Sampler types are declared with [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md).</span></span> <span data-ttu-id="ef568-156">Если src1 объявлен как 2D-образец, src0 должен содержать координаты. ксив; Если src1 объявляется как образец куба или как образец тома, src0 должен содержать координаты. ксизв.</span><span class="sxs-lookup"><span data-stu-id="ef568-156">If src1 is declared as a 2D sampler, then src0 must contain .xyw coordinates; if src1 is declared as either a cube sampler or a volume sampler, then src0 must contain .xyzw coordinates.</span></span> <span data-ttu-id="ef568-157">Допускается выборка двухмерной текстуры с помощью координат. ксизв (координата. z игнорируется).</span><span class="sxs-lookup"><span data-stu-id="ef568-157">Sampling a 2D texture with .xyzw coordinates is allowed (the .z coordinate is ignored).</span></span>

<span data-ttu-id="ef568-158">Если исходная текстура содержит менее четырех компонентов, значения по умолчанию помещаются в отсутствующие компоненты.</span><span class="sxs-lookup"><span data-stu-id="ef568-158">If the source texture contains fewer than four components, defaults are placed in the missing components.</span></span> <span data-ttu-id="ef568-159">Значения по умолчанию зависят от формата текстуры, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="ef568-159">Defaults depend on the texture format as shown in the following table:</span></span>



| <span data-ttu-id="ef568-160">Формат текстуры</span><span class="sxs-lookup"><span data-stu-id="ef568-160">Texture Format</span></span>                                                                                          | <span data-ttu-id="ef568-161">Значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ef568-161">Default Values</span></span>       |
|---------------------------------------------------------------------------------------------------------|----------------------|
| <span data-ttu-id="ef568-162">D3DFMT \_ R5G6B5, D3DFMT \_ R8G8B8, D3DFMT \_ 8, D3DFMT \_ L16, D3DFMT \_ R3G3B2, D3DFMT \_ CxV8U8, D3DFMT \_ L6V5U5</span><span class="sxs-lookup"><span data-stu-id="ef568-162">D3DFMT\_R5G6B5, D3DFMT\_R8G8B8, D3DFMT\_L8, D3DFMT\_L16, D3DFMT\_R3G3B2, D3DFMT\_CxV8U8, D3DFMT\_L6V5U5</span></span> | <span data-ttu-id="ef568-163">A = 1,0</span><span class="sxs-lookup"><span data-stu-id="ef568-163">A = 1.0</span></span>              |
| <span data-ttu-id="ef568-164">D3DFMT \_ V8U8, D3DFMT \_ V16U16, D3DFMT \_ G16R16, D3DFMT \_ G16R16F, D3DFMT \_ G32R32F</span><span class="sxs-lookup"><span data-stu-id="ef568-164">D3DFMT\_V8U8, D3DFMT\_V16U16, D3DFMT\_G16R16, D3DFMT\_G16R16F, D3DFMT\_G32R32F</span></span>                          | <span data-ttu-id="ef568-165">B = A = 1,0</span><span class="sxs-lookup"><span data-stu-id="ef568-165">B = A = 1.0</span></span>          |
| <span data-ttu-id="ef568-166">D3DFMT \_ A8</span><span class="sxs-lookup"><span data-stu-id="ef568-166">D3DFMT\_A8</span></span>                                                                                              | <span data-ttu-id="ef568-167">R = G = B = 0,0</span><span class="sxs-lookup"><span data-stu-id="ef568-167">R = G = B = 0.0</span></span>      |
| <span data-ttu-id="ef568-168">D3DFMT \_ R16F, D3DFMT \_ R32F</span><span class="sxs-lookup"><span data-stu-id="ef568-168">D3DFMT\_R16F, D3DFMT\_R32F</span></span>                                                                              | <span data-ttu-id="ef568-169">G = B = A = 1,0</span><span class="sxs-lookup"><span data-stu-id="ef568-169">G = B = A = 1.0</span></span>      |
| <span data-ttu-id="ef568-170">Все форматы глубины и трафарета</span><span class="sxs-lookup"><span data-stu-id="ef568-170">All depth/stencil formats</span></span>                                                                               | <span data-ttu-id="ef568-171">R = B = 0,0, A = 1,0</span><span class="sxs-lookup"><span data-stu-id="ef568-171">R = B = 0.0, A = 1.0</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ef568-172">См. также</span><span class="sxs-lookup"><span data-stu-id="ef568-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef568-173">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="ef568-173">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 