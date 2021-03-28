---
title: sample_c_lz (SM4-ASM)
description: Выполняет фильтр сравнения. Эта инструкция ведет себя как образец \_ c, за исключением того, что Лод имеет значение 0, а производные не учитываются.
ms.assetid: 5F11F091-AF2F-4293-88C7-824F11FE01E4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24ec2889dd3ea4c86af51c8e36bf2e302c6ad4dd
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412171"
---
# <a name="sample_c_lz-sm4---asm"></a><span data-ttu-id="67f27-104">Пример \_ c \_ LZ (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="67f27-104">sample\_c\_lz (sm4 - asm)</span></span>

<span data-ttu-id="67f27-105">Выполняет фильтр сравнения.</span><span class="sxs-lookup"><span data-stu-id="67f27-105">Performs a comparison filter.</span></span> <span data-ttu-id="67f27-106">Эта инструкция ведет себя как [образец \_ c](sample-c--sm4---asm-.md), за исключением того, что Лод имеет значение 0, а производные не учитываются.</span><span class="sxs-lookup"><span data-stu-id="67f27-106">This instruction behaves like [sample\_c](sample-c--sm4---asm-.md), except LOD is 0, and derivatives are ignored.</span></span>



| <span data-ttu-id="67f27-107">образец \_ c \_ LZ \[ \_ аоффимми (u, v, w) \] dest \[ . Mask \] , сркаддресс \[ . свиззле \] , сркресаурце. r,//должен быть. r свиззле срксамплер, сркреференцевалуе//один выбранный компонент</span><span class="sxs-lookup"><span data-stu-id="67f27-107">sample\_c\_lz\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource.r, // must be .r swizzle srcSampler, srcReferenceValue // single component selected</span></span> |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="67f27-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="67f27-108">Item</span></span>                                                                                                                                       | <span data-ttu-id="67f27-109">Описание</span><span class="sxs-lookup"><span data-stu-id="67f27-109">Description</span></span>                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67f27-110"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="67f27-110"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                                            | <span data-ttu-id="67f27-111">\[в \] адресе результатов операции.</span><span class="sxs-lookup"><span data-stu-id="67f27-111">\[in\] The address of the results of the operation.</span></span><br/>                                                             |
| <span data-ttu-id="67f27-112"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*сркаддресс*</span><span class="sxs-lookup"><span data-stu-id="67f27-112"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>                             | <span data-ttu-id="67f27-113">\[в \] наборе координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="67f27-113">\[in\] A set of texture coordinates.</span></span> <span data-ttu-id="67f27-114">Дополнительные сведения см. в [примере](sample--sm4---asm-.md) инструкции.</span><span class="sxs-lookup"><span data-stu-id="67f27-114">For more information see the [sample](sample--sm4---asm-.md) instruction.</span></span><br/> |
| <span data-ttu-id="67f27-115"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*сркресаурце*</span><span class="sxs-lookup"><span data-stu-id="67f27-115"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/>                         | <span data-ttu-id="67f27-116">\[в \] регистре текстуры.</span><span class="sxs-lookup"><span data-stu-id="67f27-116">\[in\] A texture register.</span></span> <span data-ttu-id="67f27-117">Дополнительные сведения см. в **примере** инструкции.</span><span class="sxs-lookup"><span data-stu-id="67f27-117">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="67f27-118"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*срксамплер*</span><span class="sxs-lookup"><span data-stu-id="67f27-118"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>                             | <span data-ttu-id="67f27-119">\[в \] регистре образца.</span><span class="sxs-lookup"><span data-stu-id="67f27-119">\[in\] A sampler register.</span></span> <span data-ttu-id="67f27-120">Дополнительные сведения см. в **примере** инструкции.</span><span class="sxs-lookup"><span data-stu-id="67f27-120">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="67f27-121"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*сркреференцевалуе*</span><span class="sxs-lookup"><span data-stu-id="67f27-121"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span></span><br/> | <span data-ttu-id="67f27-122">\[в \] регистре с выбранным одним компонентом, который используется в сравнении.</span><span class="sxs-lookup"><span data-stu-id="67f27-122">\[in\] A register with a single component selected, which is used in the comparison.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="67f27-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="67f27-123">Remarks</span></span>

<span data-ttu-id="67f27-124">«LZ» означает нулевой уровень.</span><span class="sxs-lookup"><span data-stu-id="67f27-124">The "lz" stands for level-zero.</span></span> <span data-ttu-id="67f27-125">Поскольку производные не пропускаются, эта инструкция доступна в шейдерах, отличных от шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="67f27-125">Because derivatives are ignored, this instruction is available in shaders other than the Pixel Shader.</span></span>

<span data-ttu-id="67f27-126">Если эта инструкция используется с текстурой мипмаппед, Лод 0 получает выборку, если только в образце не имеется ЛОДого среза, который помещает Лод в другое место, или если имеется Лод смещение, которое было бы просто смещением, начинающимся с 0.</span><span class="sxs-lookup"><span data-stu-id="67f27-126">If this instruction is used with a mipmapped texture, LOD 0 gets sampled, unless the sampler has an LOD clamp which places the LOD somewhere else, or if there is an LOD Bias, which would simply bias starting from 0.</span></span> <span data-ttu-id="67f27-127">Поскольку производные не учитываются, анизотропная фильтрация ведет себя как фильтрация исотропик.</span><span class="sxs-lookup"><span data-stu-id="67f27-127">Because derivatives are ignored, anisotropic filtering behaves as isotropic filtering.</span></span>

<span data-ttu-id="67f27-128">В пиксельных шейдерах эту инструкцию можно использовать внутри различных элементов управления потоком, когда координаты текстуры наследуются в шейдере, в отличие от **образца \_ c**.</span><span class="sxs-lookup"><span data-stu-id="67f27-128">In Pixel Shaders, this instruction can be used inside varying flow control when the texture coordinates are derived in the shader, unlike **sample\_c**.</span></span>

<span data-ttu-id="67f27-129">При попытке получить из входного слота, к которому не привязано ничего, возвращается значение 0 для всех компонентов.</span><span class="sxs-lookup"><span data-stu-id="67f27-129">Fetching from an input slot that has nothing bound to it returns 0 for all components.</span></span>

<span data-ttu-id="67f27-130">Эта инструкция доступна во всех шейдерах, а не только в шейдере пикселей, для обеспечения согласованности.</span><span class="sxs-lookup"><span data-stu-id="67f27-130">This instruction is available in all shaders, not just the Pixel Shader, for consistency.</span></span>



| <span data-ttu-id="67f27-131">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="67f27-131">Vertex Shader</span></span> | <span data-ttu-id="67f27-132">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="67f27-132">Geometry Shader</span></span> | <span data-ttu-id="67f27-133">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="67f27-133">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="67f27-134">X</span><span class="sxs-lookup"><span data-stu-id="67f27-134">X</span></span>             | <span data-ttu-id="67f27-135">X</span><span class="sxs-lookup"><span data-stu-id="67f27-135">X</span></span>               | <span data-ttu-id="67f27-136">x</span><span class="sxs-lookup"><span data-stu-id="67f27-136">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="67f27-137">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="67f27-137">Minimum Shader Model</span></span>

<span data-ttu-id="67f27-138">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="67f27-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="67f27-139">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="67f27-139">Shader Model</span></span>                                              | <span data-ttu-id="67f27-140">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="67f27-140">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="67f27-141">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="67f27-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="67f27-142">да</span><span class="sxs-lookup"><span data-stu-id="67f27-142">yes</span></span>       |
| [<span data-ttu-id="67f27-143">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="67f27-143">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="67f27-144">да</span><span class="sxs-lookup"><span data-stu-id="67f27-144">yes</span></span>       |
| [<span data-ttu-id="67f27-145">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="67f27-145">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="67f27-146">да</span><span class="sxs-lookup"><span data-stu-id="67f27-146">yes</span></span>       |
| [<span data-ttu-id="67f27-147">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="67f27-147">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="67f27-148">Нет</span><span class="sxs-lookup"><span data-stu-id="67f27-148">no</span></span>        |
| [<span data-ttu-id="67f27-149">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="67f27-149">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="67f27-150">Нет</span><span class="sxs-lookup"><span data-stu-id="67f27-150">no</span></span>        |
| [<span data-ttu-id="67f27-151">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="67f27-151">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="67f27-152">Нет</span><span class="sxs-lookup"><span data-stu-id="67f27-152">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="67f27-153">См. также</span><span class="sxs-lookup"><span data-stu-id="67f27-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67f27-154">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="67f27-154">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





