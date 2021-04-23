---
title: sample_l (SM4-ASM)
description: Выборка данных из указанного элемента или текстуры с использованием указанного адреса и режима фильтрации, определенного заданным образцом. | sample_l (SM4-ASM)
ms.assetid: D285F63E-1026-45F1-9959-6F5AB2A27C95
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5acd83d81e4648cc9eae5f8e0166013dcca512a8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353362"
---
# <a name="sample_l-sm4---asm"></a><span data-ttu-id="ea9d2-104">Пример \_ l (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="ea9d2-104">sample\_l (sm4 - asm)</span></span>

<span data-ttu-id="ea9d2-105">Выборка данных из указанного элемента или текстуры с использованием указанного адреса и режима фильтрации, определенного заданным образцом.</span><span class="sxs-lookup"><span data-stu-id="ea9d2-105">Samples data from the specified Element/texture using the specified address and the filtering mode identified by the given sampler.</span></span>



| <span data-ttu-id="ea9d2-106">Пример \_ l \[ \_ аоффимми (u, v, w) \] dest \[ . Mask \] , сркаддресс \[ . свиззле \] , сркресаурце \[ . свиззле \] , срксамплер, срклод. Выбор \_ компонента</span><span class="sxs-lookup"><span data-stu-id="ea9d2-106">sample\_l\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler, srcLOD.select\_component</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="ea9d2-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="ea9d2-107">Item</span></span>                                                                                                               | <span data-ttu-id="ea9d2-108">Описание</span><span class="sxs-lookup"><span data-stu-id="ea9d2-108">Description</span></span>                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea9d2-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="ea9d2-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="ea9d2-110">\[в \] адресе результатов операции.</span><span class="sxs-lookup"><span data-stu-id="ea9d2-110">\[in\] The address of the results of the operation.</span></span><br/>                                                             |
| <span data-ttu-id="ea9d2-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*сркаддресс*</span><span class="sxs-lookup"><span data-stu-id="ea9d2-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="ea9d2-112">\[в \] наборе координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="ea9d2-112">\[in\] A set of texture coordinates.</span></span> <span data-ttu-id="ea9d2-113">Дополнительные сведения см. в [примере](sample--sm4---asm-.md) инструкции.</span><span class="sxs-lookup"><span data-stu-id="ea9d2-113">For more information see the [sample](sample--sm4---asm-.md) instruction.</span></span><br/> |
| <span data-ttu-id="ea9d2-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*сркресаурце*</span><span class="sxs-lookup"><span data-stu-id="ea9d2-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="ea9d2-115">\[в \] регистре текстуры.</span><span class="sxs-lookup"><span data-stu-id="ea9d2-115">\[in\] A texture register.</span></span> <span data-ttu-id="ea9d2-116">Дополнительные сведения см. в **примере** инструкции.</span><span class="sxs-lookup"><span data-stu-id="ea9d2-116">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="ea9d2-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*срксамплер*</span><span class="sxs-lookup"><span data-stu-id="ea9d2-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="ea9d2-118">\[в \] регистре образца.</span><span class="sxs-lookup"><span data-stu-id="ea9d2-118">\[in\] A sampler register.</span></span> <span data-ttu-id="ea9d2-119">Дополнительные сведения см. в **примере** инструкции.</span><span class="sxs-lookup"><span data-stu-id="ea9d2-119">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="ea9d2-120"><span id="srcLOD"></span><span id="srclod"></span><span id="SRCLOD"></span>*срклод*</span><span class="sxs-lookup"><span data-stu-id="ea9d2-120"><span id="srcLOD"></span><span id="srclod"></span><span id="SRCLOD"></span>*srcLOD*</span></span><br/>                     | <span data-ttu-id="ea9d2-121">\[в \] Лод.</span><span class="sxs-lookup"><span data-stu-id="ea9d2-121">\[in\] The LOD.</span></span><br/>                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="ea9d2-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="ea9d2-122">Remarks</span></span>

<span data-ttu-id="ea9d2-123">Эта инструкция идентична [образцу](sample--sm4---asm-.md), за исключением того, что Лод предоставляется напрямую приложением в качестве скалярного значения, что не представляет анизотропную конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="ea9d2-123">This instruction is identical to [sample](sample--sm4---asm-.md), except that LOD is provided directly by the application as a scalar value, representing no anisotropy.</span></span> <span data-ttu-id="ea9d2-124">Эта инструкция доступна на всех стадиях шейдера прогаммабле.</span><span class="sxs-lookup"><span data-stu-id="ea9d2-124">This instruction is available in all progammable Shader stages.</span></span>

<span data-ttu-id="ea9d2-125">в **примере \_ l** показан пример текстуры с использованием *срклод* для Лод.</span><span class="sxs-lookup"><span data-stu-id="ea9d2-125">**sample\_l** samples the texture using *srcLOD* to be the LOD.</span></span> <span data-ttu-id="ea9d2-126">Если значение Лод <равно 0, то выбирается зеро'с (самая большая схема) с примененным фильтром увеличения (если применимо на основе режима фильтрации).</span><span class="sxs-lookup"><span data-stu-id="ea9d2-126">If the LOD value is <= 0, the zero'th (biggest map) is chosen, with the magnify filter applied (if applicable based on the filter mode).</span></span> <span data-ttu-id="ea9d2-127">Поскольку *срклод* — это значение с плавающей запятой, значение дробной части используется для интерполяции между двумя уровнями MIP, если фильтр уменьшение является линейным или с анизотропной фильтрацией.</span><span class="sxs-lookup"><span data-stu-id="ea9d2-127">Because *srcLOD* is a floating point value, the fractional value is used to interpolate between two mip levels, if the minify filter is LINEAR or with anisotropic filtering.</span></span>

<span data-ttu-id="ea9d2-128">в **примере \_ l** не учитываются производные от адресов, поэтому поведение фильтрации является исключительно исотропик.</span><span class="sxs-lookup"><span data-stu-id="ea9d2-128">**sample\_l** ignores address derivatives, so filtering behavior is purely isotropic.</span></span> <span data-ttu-id="ea9d2-129">Поскольку производные не учитываются, анизотропная фильтрация ведет себя как фильтрация исотропик.</span><span class="sxs-lookup"><span data-stu-id="ea9d2-129">Because derivatives are ignored, anisotropic filtering behaves as isotropic filtering.</span></span>

<span data-ttu-id="ea9d2-130">Соблюдаются состояния образцов МИПЛОДБИАС и MAX/МИНМИПЛЕВЕЛ.</span><span class="sxs-lookup"><span data-stu-id="ea9d2-130">Sampler states MIPLODBIAS and MAX/MINMIPLEVEL are honored.</span></span>

<span data-ttu-id="ea9d2-131">При использовании в шейдере пикселей **пример \_ l** подразумевает, что выбор Лод относится к каждому пикселю без воздействия на соседние пиксели, например в той же метке 2x2.</span><span class="sxs-lookup"><span data-stu-id="ea9d2-131">When used in the Pixel Shader, **sample\_l** implies that the choice of LOD is per-pixel, with no effect from neighboring pixels, for example in the same 2x2 stamp.</span></span>

<span data-ttu-id="ea9d2-132">При попытке получить из входного слота, к которому не привязано ничего, возвращается значение 0 для всех компонентов.</span><span class="sxs-lookup"><span data-stu-id="ea9d2-132">Fetching from an input slot that has nothing bound to it returns 0 for all components.</span></span>

<span data-ttu-id="ea9d2-133">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="ea9d2-133">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ea9d2-134">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="ea9d2-134">Vertex Shader</span></span> | <span data-ttu-id="ea9d2-135">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="ea9d2-135">Geometry Shader</span></span> | <span data-ttu-id="ea9d2-136">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="ea9d2-136">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="ea9d2-137">X</span><span class="sxs-lookup"><span data-stu-id="ea9d2-137">X</span></span>             | <span data-ttu-id="ea9d2-138">X</span><span class="sxs-lookup"><span data-stu-id="ea9d2-138">X</span></span>               | <span data-ttu-id="ea9d2-139">x</span><span class="sxs-lookup"><span data-stu-id="ea9d2-139">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ea9d2-140">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ea9d2-140">Minimum Shader Model</span></span>

<span data-ttu-id="ea9d2-141">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="ea9d2-141">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ea9d2-142">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ea9d2-142">Shader Model</span></span>                                              | <span data-ttu-id="ea9d2-143">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="ea9d2-143">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ea9d2-144">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="ea9d2-144">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ea9d2-145">да</span><span class="sxs-lookup"><span data-stu-id="ea9d2-145">yes</span></span>       |
| [<span data-ttu-id="ea9d2-146">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="ea9d2-146">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ea9d2-147">да</span><span class="sxs-lookup"><span data-stu-id="ea9d2-147">yes</span></span>       |
| [<span data-ttu-id="ea9d2-148">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="ea9d2-148">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ea9d2-149">да</span><span class="sxs-lookup"><span data-stu-id="ea9d2-149">yes</span></span>       |
| [<span data-ttu-id="ea9d2-150">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ea9d2-150">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ea9d2-151">Нет</span><span class="sxs-lookup"><span data-stu-id="ea9d2-151">no</span></span>        |
| [<span data-ttu-id="ea9d2-152">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ea9d2-152">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ea9d2-153">Нет</span><span class="sxs-lookup"><span data-stu-id="ea9d2-153">no</span></span>        |
| [<span data-ttu-id="ea9d2-154">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ea9d2-154">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ea9d2-155">Нет</span><span class="sxs-lookup"><span data-stu-id="ea9d2-155">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ea9d2-156">См. также</span><span class="sxs-lookup"><span data-stu-id="ea9d2-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea9d2-157">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ea9d2-157">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





