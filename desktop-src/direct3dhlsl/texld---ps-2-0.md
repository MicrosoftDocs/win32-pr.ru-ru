---
title: текслд — ps_2_0 и выше
description: Пример текстуры в определенном образце с использованием предоставленных координат текстуры. Эта инструкция отличается от инструкции текслд-PS \_ 1 \_ 4, используемой в Pixel Shader версии 1 \_ 4.
ms.assetid: 2b0d02b4-d9dd-4388-aa86-03b27bc4fdc8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b71990e230290403bca2a5af11eeca11b093402f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533272"
---
# <a name="texld---ps_2_0-and-up"></a><span data-ttu-id="96084-104">текслд-PS \_ 2 \_ 0 и выше</span><span class="sxs-lookup"><span data-stu-id="96084-104">texld - ps\_2\_0 and up</span></span>

<span data-ttu-id="96084-105">Пример текстуры в определенном образце с использованием предоставленных координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="96084-105">Sample a texture at a particular sampler, using provided texture coordinates.</span></span> <span data-ttu-id="96084-106">Эта инструкция отличается от инструкции [текслд-PS \_ 1 \_ 4](texld---ps-1-4.md) , используемой в Pixel Shader версии 1 \_ 4.</span><span class="sxs-lookup"><span data-stu-id="96084-106">This instruction is different from the [texld - ps\_1\_4](texld---ps-1-4.md) instruction used in pixel shader version 1\_4.</span></span>

## <a name="syntax"></a><span data-ttu-id="96084-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="96084-107">Syntax</span></span>



| <span data-ttu-id="96084-108">текслд DST, src0, src1</span><span class="sxs-lookup"><span data-stu-id="96084-108">texld dst, src0, src1</span></span> |
|-----------------------|



 

<span data-ttu-id="96084-109">Где:</span><span class="sxs-lookup"><span data-stu-id="96084-109">Where:</span></span>

-   <span data-ttu-id="96084-110">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="96084-110">dst is a destination register.</span></span>
-   <span data-ttu-id="96084-111">src0 — это исходный регистр, предоставляющий координаты текстуры для образца текстуры.</span><span class="sxs-lookup"><span data-stu-id="96084-111">src0 is a source register that provides the texture coordinates for the texture sample.</span></span>
-   <span data-ttu-id="96084-112">src1 определяет [образец (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) \# , где \# указывает, какой номер образца текстуры следует вычислить.</span><span class="sxs-lookup"><span data-stu-id="96084-112">src1 identifies the [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), where \# specifies which texture sampler number to sample.</span></span> <span data-ttu-id="96084-113">Этот образец связан с текстурой и состоянием выборки, определенным в [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span><span class="sxs-lookup"><span data-stu-id="96084-113">The sampler has associated with it a texture and a sampler state defined by [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).</span></span>

### <a name="ps_2_0-and-ps_2_x"></a><span data-ttu-id="96084-114">PS \_ 2 \_ 0 и PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="96084-114">ps\_2\_0 and ps\_2\_x</span></span>

<span data-ttu-id="96084-115">DST должен быть [временным регистром](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ), и допускается только ксизв маска (маска по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="96084-115">dst must be a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) and only .xyzw mask (default mask) is allowed.</span></span>

<span data-ttu-id="96084-116">src0 должен быть либо [регистром координаты текстуры](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t \# ), либо [временным регистром](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ) без модификатора или свиззле.</span><span class="sxs-lookup"><span data-stu-id="96084-116">src0 must be either a [Texture Coordinate Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (t\#) or a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#), with no modifier or swizzle.</span></span>

<span data-ttu-id="96084-117">src1 должны быть [образцами (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) без \# модификатора или свиззле.</span><span class="sxs-lookup"><span data-stu-id="96084-117">src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), with no modifier or swizzle.</span></span>

<span data-ttu-id="96084-118">Если \_ \_ бит крепления D3DD3DPSHADERCAPS2 0 нодепендентреадлимит не установлен (в D3DPSHADERCAPS2 \_ 0), данная инструкция текстуры ([текслд](texld---ps-1-4.md), [текслдп](texldp---ps.md), [текслдб-PS](texldb---ps.md), [текслдд](texldd---ps.md) ) может быть зависеть от третьего порядка.</span><span class="sxs-lookup"><span data-stu-id="96084-118">If the D3DD3DPSHADERCAPS2\_0\_NODEPENDENTREADLIMIT cap bit is not set (in D3DPSHADERCAPS2\_0), a given texture instruction ([texld](texld---ps-1-4.md), [texldp](texldp---ps.md), [texldb - ps](texldb---ps.md), [texldd](texldd---ps.md) ) may be dependent upon, at most, third order.</span></span> <span data-ttu-id="96084-119">Инструкция текстуры, зависимая от первого порядка, представляет собой текстурную инструкцию, в которой одно из следующих:</span><span class="sxs-lookup"><span data-stu-id="96084-119">A first-order dependent texture instruction is a texture instruction in which either:</span></span>

-   <span data-ttu-id="96084-120">src0 — это [временный регистр](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ).</span><span class="sxs-lookup"><span data-stu-id="96084-120">src0 is a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#).</span></span>
-   <span data-ttu-id="96084-121">летнее время было записано еще раз.</span><span class="sxs-lookup"><span data-stu-id="96084-121">dst was previously written, now being written again.</span></span>

<span data-ttu-id="96084-122">Инструкция текстуры, зависимая от второго порядка, определяется как Текстурная инструкция, которая считывает или выполняет запись [во временный регистр](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ), содержимое которого перед выполнением инструкции текстуры зависят (возможно, косвенно) от результата инструкции текстуры, зависящей от первого заказа.</span><span class="sxs-lookup"><span data-stu-id="96084-122">A second-order dependent texture instruction is defined as a texture instruction that reads or writes to a [Temporary Register](dx9-graphics-reference-asm-ps-registers-temporary.md) (r\#) whose contents, before executing the texture instruction, depend (perhaps indirectly) on the outcome of a first-order dependent texture instruction.</span></span> <span data-ttu-id="96084-123">Инструкция текстуры, зависимая от (<sup>n),</sup>является производной от (n-1)-<sup>го</sup>порядка текстуры.</span><span class="sxs-lookup"><span data-stu-id="96084-123">An (n)<sup>th</sup>-order dependent texture instruction derives from an (n - 1)<sup>th</sup>-order texture instruction.</span></span>

### <a name="ps_3_0"></a><span data-ttu-id="96084-124">PS \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="96084-124">ps\_3\_0</span></span>

<span data-ttu-id="96084-125">src1 должны быть [образцами (Direct3D 9 ASM-PS)](dx9-graphics-reference-asm-ps-registers-sampler.md) без \# модификатора.</span><span class="sxs-lookup"><span data-stu-id="96084-125">src1 must be a [Sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s\#), with no modifier.</span></span> <span data-ttu-id="96084-126">Свиззле разрешен в src0 или src1.</span><span class="sxs-lookup"><span data-stu-id="96084-126">Swizzle is allowed on src0 or src1.</span></span> <span data-ttu-id="96084-127">Свиззле применяется к текстуре курдинтатес перед поиском текстур.</span><span class="sxs-lookup"><span data-stu-id="96084-127">The swizzle is applied to the texture coordintates before texture lookup.</span></span>

## <a name="remarks"></a><span data-ttu-id="96084-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="96084-128">Remarks</span></span>

<span data-ttu-id="96084-129">Эта инструкция поддерживается в следующих версиях:</span><span class="sxs-lookup"><span data-stu-id="96084-129">This instruction is supported in the following versions:</span></span>



| <span data-ttu-id="96084-130">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="96084-130">Pixel shader versions</span></span> | <span data-ttu-id="96084-131">1\_1</span><span class="sxs-lookup"><span data-stu-id="96084-131">1\_1</span></span> | <span data-ttu-id="96084-132">1\_2</span><span class="sxs-lookup"><span data-stu-id="96084-132">1\_2</span></span> | <span data-ttu-id="96084-133">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="96084-133">1\_3</span></span> | <span data-ttu-id="96084-134">1\_4</span><span class="sxs-lookup"><span data-stu-id="96084-134">1\_4</span></span> | <span data-ttu-id="96084-135">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="96084-135">2\_0</span></span> | <span data-ttu-id="96084-136">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="96084-136">2\_x</span></span> | <span data-ttu-id="96084-137">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="96084-137">2\_sw</span></span> | <span data-ttu-id="96084-138">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="96084-138">3\_0</span></span> | <span data-ttu-id="96084-139">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="96084-139">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="96084-140">текслд</span><span class="sxs-lookup"><span data-stu-id="96084-140">texld</span></span>                 |      |      |      |      | <span data-ttu-id="96084-141">x</span><span class="sxs-lookup"><span data-stu-id="96084-141">x</span></span>    | <span data-ttu-id="96084-142">x</span><span class="sxs-lookup"><span data-stu-id="96084-142">x</span></span>    | <span data-ttu-id="96084-143">x</span><span class="sxs-lookup"><span data-stu-id="96084-143">x</span></span>     | <span data-ttu-id="96084-144">x</span><span class="sxs-lookup"><span data-stu-id="96084-144">x</span></span>    | <span data-ttu-id="96084-145">x</span><span class="sxs-lookup"><span data-stu-id="96084-145">x</span></span>     |



 

<span data-ttu-id="96084-146">Количество координат, необходимых для выполнения образца текстуры для src0, зависит от того, как был объявлен src1, а также от компонента. w.</span><span class="sxs-lookup"><span data-stu-id="96084-146">The number of coordinates required for src0 to perform the texture sample depends on how src1 was declared, plus the .w component.</span></span> <span data-ttu-id="96084-147">Типы образцов объявляются с помощью [дкл \_ самплертипе (SM2, SM3-PS ASM)](dcl-samplertype---ps.md).</span><span class="sxs-lookup"><span data-stu-id="96084-147">Sampler types are declared with [dcl\_samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md).</span></span> <span data-ttu-id="96084-148">Если src1 объявлен как 2D-образец, src0 должен содержать координаты координат; Если src1 объявляется как образец куба или как образец объема, то src0 должен содержать координаты. xyz.</span><span class="sxs-lookup"><span data-stu-id="96084-148">If src1 is declared as a 2D sampler, then src0 must contain .xy coordinates; if src1 is declared as either a cube sampler or a volume sampler, then src0 must contain .xyz coordinates.</span></span> <span data-ttu-id="96084-149">Выборка текстуры с меньшей размерностью, чем есть в координатах текстуры, разрешена, так как дополнительные компоненты координат текстуры игнорируются.</span><span class="sxs-lookup"><span data-stu-id="96084-149">Sampling a texture with fewer dimensions than are present in the texture coordinate is allowed since the extra texture coordinate component(s) are ignored.</span></span>

<span data-ttu-id="96084-150">Если исходная текстура содержит менее четырех компонентов, значения по умолчанию помещаются в отсутствующие компоненты.</span><span class="sxs-lookup"><span data-stu-id="96084-150">If the source texture contains fewer than four components, defaults are placed in the missing components.</span></span> <span data-ttu-id="96084-151">Значения по умолчанию зависят от формата текстуры, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="96084-151">Defaults depend on the texture format as shown in the following table:</span></span>



| <span data-ttu-id="96084-152">Формат текстуры</span><span class="sxs-lookup"><span data-stu-id="96084-152">Texture Format</span></span>                                                                                          | <span data-ttu-id="96084-153">Значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="96084-153">Default Values</span></span>       |
|---------------------------------------------------------------------------------------------------------|----------------------|
| <span data-ttu-id="96084-154">D3DFMT \_ R5G6B5, D3DFMT \_ R8G8B8, D3DFMT \_ 8, D3DFMT \_ L16, D3DFMT \_ R3G3B2, D3DFMT \_ CxV8U8, D3DFMT \_ L6V5U5</span><span class="sxs-lookup"><span data-stu-id="96084-154">D3DFMT\_R5G6B5, D3DFMT\_R8G8B8, D3DFMT\_L8, D3DFMT\_L16, D3DFMT\_R3G3B2, D3DFMT\_CxV8U8, D3DFMT\_L6V5U5</span></span> | <span data-ttu-id="96084-155">A = 1,0</span><span class="sxs-lookup"><span data-stu-id="96084-155">A = 1.0</span></span>              |
| <span data-ttu-id="96084-156">D3DFMT \_ V8U8, D3DFMT \_ V16U16, D3DFMT \_ G16R16, D3DFMT \_ G16R16F, D3DFMT \_ G32R32F</span><span class="sxs-lookup"><span data-stu-id="96084-156">D3DFMT\_V8U8, D3DFMT\_V16U16, D3DFMT\_G16R16, D3DFMT\_G16R16F, D3DFMT\_G32R32F</span></span>                          | <span data-ttu-id="96084-157">B = A = 1,0</span><span class="sxs-lookup"><span data-stu-id="96084-157">B = A = 1.0</span></span>          |
| <span data-ttu-id="96084-158">D3DFMT \_ A8</span><span class="sxs-lookup"><span data-stu-id="96084-158">D3DFMT\_A8</span></span>                                                                                              | <span data-ttu-id="96084-159">R = G = B = 0,0</span><span class="sxs-lookup"><span data-stu-id="96084-159">R = G = B = 0.0</span></span>      |
| <span data-ttu-id="96084-160">D3DFMT \_ R16F, D3DFMT \_ R32F</span><span class="sxs-lookup"><span data-stu-id="96084-160">D3DFMT\_R16F, D3DFMT\_R32F</span></span>                                                                              | <span data-ttu-id="96084-161">G = B = A = 1,0</span><span class="sxs-lookup"><span data-stu-id="96084-161">G = B = A = 1.0</span></span>      |
| <span data-ttu-id="96084-162">Все форматы глубины и трафарета</span><span class="sxs-lookup"><span data-stu-id="96084-162">All depth/stencil formats</span></span>                                                                               | <span data-ttu-id="96084-163">R = B = 0,0, A = 1,0</span><span class="sxs-lookup"><span data-stu-id="96084-163">R = B = 0.0, A = 1.0</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="96084-164">См. также</span><span class="sxs-lookup"><span data-stu-id="96084-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96084-165">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="96084-165">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 