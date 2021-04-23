---
title: gather4 (SM5-ASM)
description: Собирает четыре пикселей текстуры, которые будут использоваться в операции линейной фильтрации, и упаковывает их в единый регистр. | gather4 (SM5-ASM)
ms.assetid: 5F93BB70-7696-48E4-BCD3-91D5D42FF63E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5657265738f12331afc7596286f02170de2a635
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273470"
---
# <a name="gather4-sm5---asm"></a><span data-ttu-id="9dd9e-104">gather4 (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="9dd9e-104">gather4 (sm5 - asm)</span></span>

<span data-ttu-id="9dd9e-105">Собирает четыре пикселей текстуры, которые будут использоваться в операции линейной фильтрации, и упаковывает их в единый регистр.</span><span class="sxs-lookup"><span data-stu-id="9dd9e-105">Gathers the four texels that would be used in a bi-linear filtering operation and packs them into a single register.</span></span> <span data-ttu-id="9dd9e-106">Эта инструкция работает только с текстурами 2D или кубической карты, включая массивы.</span><span class="sxs-lookup"><span data-stu-id="9dd9e-106">This instruction only works with 2D or CubeMap textures, including arrays.</span></span> <span data-ttu-id="9dd9e-107">Используются только режимы адресации образца, и используется верхний уровень любой MIP пирамиды.</span><span class="sxs-lookup"><span data-stu-id="9dd9e-107">Only the addressing modes of the sampler are used and the top level of any mip pyramid is used.</span></span>



| <span data-ttu-id="9dd9e-108">gather4 \[ \_ аоффимми (u, v) \] dest \[ . Mask \] , сркаддресс \[ . свиззле \] , сркресаурце \[ . свиззле \] , срксамплер \[ . Select \_ Component\]</span><span class="sxs-lookup"><span data-stu-id="9dd9e-108">gather4\[\_aoffimmi(u,v)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler\[.select\_component\]</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="9dd9e-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="9dd9e-109">Item</span></span>                                                                                                               | <span data-ttu-id="9dd9e-110">Описание</span><span class="sxs-lookup"><span data-stu-id="9dd9e-110">Description</span></span>                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="9dd9e-111"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="9dd9e-111"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="9dd9e-112">\[в \] адресе результатов операции.</span><span class="sxs-lookup"><span data-stu-id="9dd9e-112">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="9dd9e-113"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*сркаддресс*</span><span class="sxs-lookup"><span data-stu-id="9dd9e-113"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="9dd9e-114">\[в \] наборе координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="9dd9e-114">\[in\] A set of texture coordinates.</span></span><br/>                |
| <span data-ttu-id="9dd9e-115"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*сркресаурце*</span><span class="sxs-lookup"><span data-stu-id="9dd9e-115"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="9dd9e-116">\[в \] регистре текстуры.</span><span class="sxs-lookup"><span data-stu-id="9dd9e-116">\[in\] A texture register.</span></span><br/>                          |
| <span data-ttu-id="9dd9e-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*срксамплер*</span><span class="sxs-lookup"><span data-stu-id="9dd9e-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="9dd9e-118">\[в \] регистре образца.</span><span class="sxs-lookup"><span data-stu-id="9dd9e-118">\[in\] A sampler register.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="9dd9e-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="9dd9e-119">Remarks</span></span>

<span data-ttu-id="9dd9e-120">Эта инструкция ведет себя как [**Пример**](sample--sm4---asm-.md) инструкции, но отфильтрованный образец не создается.</span><span class="sxs-lookup"><span data-stu-id="9dd9e-120">This instruction behaves like the [**sample**](sample--sm4---asm-.md) instruction, but a filtered sample is not generated.</span></span> <span data-ttu-id="9dd9e-121">Четыре примера, которые будут участвовать в фильтрации, помещаются в ксизв в порядке по часовой стрелке, начиная с образца в левом нижнем углу запрашиваемого расположения.</span><span class="sxs-lookup"><span data-stu-id="9dd9e-121">The four samples that would contribute to filtering are placed into xyzw in counter clockwise order starting with the sample to the lower left of the queried location.</span></span> <span data-ttu-id="9dd9e-122">Это то же самое, что выборка точек с помощью (u, v) дельты координат текстуры в следующих местах: (-, +), (+, +), (+,-), (-,-), где величина разностей всегда половина шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="9dd9e-122">This is the same as point sampling with (u,v) texture coordinate deltas at the following locations: (-,+),(+,+),(+,-),(-,-), where the magnitude of the deltas are always half a texel.</span></span>

<span data-ttu-id="9dd9e-123">Для текстур кубической карты при горизонтальном объеме, занимаемом пограничным, пикселей текстурыся от соседней грани.</span><span class="sxs-lookup"><span data-stu-id="9dd9e-123">For CubeMap textures, when a bi-linear footprint spans an edge, texels from the neighboring face are used.</span></span> <span data-ttu-id="9dd9e-124">Углы используют те же правила, что и [**образец**](sample--sm4---asm-.md) инструкции. Это значит, что неизвестный угол считается средним числом углов лицевой стороны.</span><span class="sxs-lookup"><span data-stu-id="9dd9e-124">Corners use the same rules as the [**sample**](sample--sm4---asm-.md) instruction; that is, the unknown corner is considered the average of the three impinging face corners.</span></span>

<span data-ttu-id="9dd9e-125">Существуют ограничения формата текстуры, применяемые к **gather4** , которые выражаются в списке Формат.</span><span class="sxs-lookup"><span data-stu-id="9dd9e-125">There are texture format restrictions that apply to **gather4** which are expressed in the format list.</span></span>

<span data-ttu-id="9dd9e-126">Свиззле On *сркресаурце* позволяет свиззлед возвращаемые значения произвольно, прежде чем они записываются в место назначения.</span><span class="sxs-lookup"><span data-stu-id="9dd9e-126">The swizzle on *srcResource* allows the returned values to be swizzled arbitrarily before they are written to the destination.</span></span>

<span data-ttu-id="9dd9e-127">Компонент. Select \_ в *срксамплер* выбирает, какой компонент исходной текстуры (r/g/b/a) считывает 4 пикселей текстуры из.</span><span class="sxs-lookup"><span data-stu-id="9dd9e-127">The .select\_component on *srcSampler* chooses which component of the source texture (r/g/b/a) to read 4 texels from.</span></span>

<span data-ttu-id="9dd9e-128">Для форматов с компонентами float32, если извлекаемое значение нормализовано, денормализовано, +-0 или +-INF, оно возвращается в шейдер без изменений.</span><span class="sxs-lookup"><span data-stu-id="9dd9e-128">For formats with float32 components, if the value being fetched is normalized, denormalized, +-0 or +-INF, it is returned to the shader unaltered.</span></span> <span data-ttu-id="9dd9e-129">NaN возвращается как NaN, но точное битовое представление NaN может быть изменено.</span><span class="sxs-lookup"><span data-stu-id="9dd9e-129">NaN is returned as NaN, but the exact bit representation of the NaN may be changed.</span></span> <span data-ttu-id="9dd9e-130">Для Текстурекубес некоторые синтезы отсутствующих 4-го шаг текселя должны происходить в углах, поэтому возвращение битов без изменений для синтезированного шаг текселя не применяется, а также может быть сброшен.</span><span class="sxs-lookup"><span data-stu-id="9dd9e-130">For TextureCubes, some synthesis of the missing 4th texel must occur at corners, so returning bits unchanged for the synthesized texel does not apply, and denorms could be flushed.</span></span>

<span data-ttu-id="9dd9e-131">Для аппаратных реализаций оптимизация в традиционной билинейной фильтрации, которая обнаруживает примеры непосредственно в пикселей текстуры и пропускает чтение пикселей текстуры, которые бы имели вес 0, не могут быть использованы в этой инструкции.</span><span class="sxs-lookup"><span data-stu-id="9dd9e-131">For hardware implementations, optimizations in traditional bilinear filtering that detect samples directly on texels and skip reading of texels that would have weight 0 cannot be leveraged with this instruction.</span></span> <span data-ttu-id="9dd9e-132">*gather4* всегда возвращает все запрошенные пикселей текстуры.</span><span class="sxs-lookup"><span data-stu-id="9dd9e-132">*gather4* always returns all requested texels.</span></span>

<span data-ttu-id="9dd9e-133">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="9dd9e-133">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9dd9e-134">Вершина</span><span class="sxs-lookup"><span data-stu-id="9dd9e-134">Vertex</span></span> | <span data-ttu-id="9dd9e-135">Поверхности</span><span class="sxs-lookup"><span data-stu-id="9dd9e-135">Hull</span></span> | <span data-ttu-id="9dd9e-136">Домен</span><span class="sxs-lookup"><span data-stu-id="9dd9e-136">Domain</span></span> | <span data-ttu-id="9dd9e-137">Геометрия</span><span class="sxs-lookup"><span data-stu-id="9dd9e-137">Geometry</span></span> | <span data-ttu-id="9dd9e-138">Пиксель</span><span class="sxs-lookup"><span data-stu-id="9dd9e-138">Pixel</span></span> | <span data-ttu-id="9dd9e-139">Вычисления</span><span class="sxs-lookup"><span data-stu-id="9dd9e-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="9dd9e-140">X</span><span class="sxs-lookup"><span data-stu-id="9dd9e-140">X</span></span>      | <span data-ttu-id="9dd9e-141">X</span><span class="sxs-lookup"><span data-stu-id="9dd9e-141">X</span></span>    | <span data-ttu-id="9dd9e-142">X</span><span class="sxs-lookup"><span data-stu-id="9dd9e-142">X</span></span>      | <span data-ttu-id="9dd9e-143">X</span><span class="sxs-lookup"><span data-stu-id="9dd9e-143">X</span></span>        | <span data-ttu-id="9dd9e-144">X</span><span class="sxs-lookup"><span data-stu-id="9dd9e-144">X</span></span>     | <span data-ttu-id="9dd9e-145">X</span><span class="sxs-lookup"><span data-stu-id="9dd9e-145">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9dd9e-146">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="9dd9e-146">Minimum Shader Model</span></span>

<span data-ttu-id="9dd9e-147">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="9dd9e-147">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="9dd9e-148">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="9dd9e-148">Shader Model</span></span>                                              | <span data-ttu-id="9dd9e-149">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="9dd9e-149">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9dd9e-150">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="9dd9e-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9dd9e-151">да</span><span class="sxs-lookup"><span data-stu-id="9dd9e-151">yes</span></span>       |
| [<span data-ttu-id="9dd9e-152">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="9dd9e-152">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9dd9e-153">Нет</span><span class="sxs-lookup"><span data-stu-id="9dd9e-153">no</span></span>        |
| [<span data-ttu-id="9dd9e-154">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="9dd9e-154">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9dd9e-155">Нет</span><span class="sxs-lookup"><span data-stu-id="9dd9e-155">no</span></span>        |
| [<span data-ttu-id="9dd9e-156">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9dd9e-156">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9dd9e-157">Нет</span><span class="sxs-lookup"><span data-stu-id="9dd9e-157">no</span></span>        |
| [<span data-ttu-id="9dd9e-158">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9dd9e-158">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9dd9e-159">Нет</span><span class="sxs-lookup"><span data-stu-id="9dd9e-159">no</span></span>        |
| [<span data-ttu-id="9dd9e-160">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9dd9e-160">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9dd9e-161">Нет</span><span class="sxs-lookup"><span data-stu-id="9dd9e-161">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9dd9e-162">См. также</span><span class="sxs-lookup"><span data-stu-id="9dd9e-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9dd9e-163">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9dd9e-163">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





