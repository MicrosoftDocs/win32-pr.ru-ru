---
title: gather4 (SM 4.1-ASM)
description: Собирает четыре пикселей текстуры, которые будут использоваться в операции линейной фильтрации, и упаковывает их в единый регистр. | gather4 (SM 4.1-ASM)
ms.assetid: 219B25AE-CBF9-4B68-B2DB-6D8C3C5B4CEA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84387bfe027e30b338b4701ec941a9d4e1b5e242
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986440"
---
# <a name="gather4-sm41---asm"></a><span data-ttu-id="85409-104">gather4 (SM 4.1-ASM)</span><span class="sxs-lookup"><span data-stu-id="85409-104">gather4 (sm4.1 - asm)</span></span>

<span data-ttu-id="85409-105">Собирает четыре пикселей текстуры, которые будут использоваться в операции линейной фильтрации, и упаковывает их в единый регистр.</span><span class="sxs-lookup"><span data-stu-id="85409-105">Gathers the four texels that would be used in a bi-linear filtering operation and packs them into a single register.</span></span>



| <span data-ttu-id="85409-106">gather4 \[ \_ аоффимми (u, v) \] dest \[ . Mask \] , сркаддресс \[ . свиззле \] , сркресаурце \[ . свиззле \] срксамплер. r</span><span class="sxs-lookup"><span data-stu-id="85409-106">gather4\[\_aoffimmi(u,v)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\] srcSampler.r</span></span> |
|--------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="85409-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="85409-107">Item</span></span>                                                                                                               | <span data-ttu-id="85409-108">Описание</span><span class="sxs-lookup"><span data-stu-id="85409-108">Description</span></span>                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85409-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="85409-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="85409-110">\[в \] адресе результата операции.</span><span class="sxs-lookup"><span data-stu-id="85409-110">\[in\] The address of the result of the operation.</span></span><br/>                                                                                                       |
| <span data-ttu-id="85409-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*сркаддресс*</span><span class="sxs-lookup"><span data-stu-id="85409-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="85409-112">\[в \] содержит координаты текстуры.</span><span class="sxs-lookup"><span data-stu-id="85409-112">\[in\] Contains the texture coordinates.</span></span> <br/>                                                                                                                |
| <span data-ttu-id="85409-113"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*сркресаурце*</span><span class="sxs-lookup"><span data-stu-id="85409-113"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="85409-114">\[в \] регистре ресурсов.</span><span class="sxs-lookup"><span data-stu-id="85409-114">\[in\] A resource register.</span></span> <br/> <span data-ttu-id="85409-115">Свиззле позволяет свиззлед возвращаемые значения произвольно, прежде чем они будут записаны в *dest*.</span><span class="sxs-lookup"><span data-stu-id="85409-115">The swizzle allows the returned values to be swizzled arbitrarily before they are written to *dest*.</span></span> <br/>            |
| <span data-ttu-id="85409-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*срксамплер*</span><span class="sxs-lookup"><span data-stu-id="85409-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="85409-117">\[в \] регистре образца.</span><span class="sxs-lookup"><span data-stu-id="85409-117">\[in\] A sampler register.</span></span><br/> <span data-ttu-id="85409-118">Этот параметр должен иметь. r (red) свиззле, который указывает, что значение канала R скопировано в *dest*.</span><span class="sxs-lookup"><span data-stu-id="85409-118">This parameter must have a .r (red) swizzle, which indicates that the value of the R channel is copied to *dest*.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="85409-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="85409-119">Remarks</span></span>

<span data-ttu-id="85409-120">Эта операция работает только с кубической карты текстурами одного канала.</span><span class="sxs-lookup"><span data-stu-id="85409-120">This operation only works with single channel 2D or CubeMap textures.</span></span> <span data-ttu-id="85409-121">Для двумерных текстур используются только режимы адресации образца, и используется верхний уровень любой MIP пирамиды.</span><span class="sxs-lookup"><span data-stu-id="85409-121">For 2D textures only the addressing modes of the sampler are used and the top level of any mip pyramid is used.</span></span>

<span data-ttu-id="85409-122">Эта инструкция ведет себя как [Пример](sample--sm4---asm-.md) инструкции, но отфильтрованный образец не создается.</span><span class="sxs-lookup"><span data-stu-id="85409-122">This instruction behaves like the [sample](sample--sm4---asm-.md) instruction, but a filtered sample is not generated.</span></span> <span data-ttu-id="85409-123">Четыре примера, которые будут участвовать в фильтрации, помещаются в ксизв в порядке по часовой стрелке, начиная с образца в левом нижнем углу запрашиваемого расположения.</span><span class="sxs-lookup"><span data-stu-id="85409-123">The four samples that would contribute to filtering are placed into xyzw in counter clockwise order starting with the sample to the lower left of the queried location.</span></span> <span data-ttu-id="85409-124">Это то же самое, что выборка точек с помощью (u, v) дельты координат текстуры в следующих местах: (-, +), (+, +), (+,-), (-,-), где величина разностей всегда половина шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="85409-124">This is the same as point sampling with (u,v) texture coordinate deltas at the following locations: (-,+),(+,+),(+,-),(-,-), where the magnitude of the deltas are always half a texel.</span></span>

<span data-ttu-id="85409-125">Для текстур кубической карты, когда используется линейный участок, пикселей текстуры с соседней стороны.</span><span class="sxs-lookup"><span data-stu-id="85409-125">For CubeMap textures when a bi-linear footprint spans an edge texels from the neighboring face are used.</span></span> <span data-ttu-id="85409-126">Углы используют те же правила, что и **образец** инструкции. Это неизвестный угол считается средним числом углов лицевой стороны.</span><span class="sxs-lookup"><span data-stu-id="85409-126">Corners use the same rules as the **sample** instruction; that is the unkown corner is considered the average of the three impinging face corners.</span></span>

<span data-ttu-id="85409-127">Ограничения формата текстуры, применимые к **образцам** инструкций, также применяются к инструкции **gather4** .</span><span class="sxs-lookup"><span data-stu-id="85409-127">The texture format restrictions that apply to the **sample** instructions also apply to the **gather4** instruction.</span></span>

<span data-ttu-id="85409-128">Для аппаратных реализаций оптимизация в традиционной билинейной фильтрации, которая обнаруживает примеры непосредственно в пикселей текстуры и пропускает чтение пикселей текстуры, которые бы имели вес 0, не могут быть использованы вместе с **gather4**.</span><span class="sxs-lookup"><span data-stu-id="85409-128">For hardware implementations, optimizations in traditional bilinear filtering that detect samples directly on texels and skip reading of texels that would have weight 0 cannot be leveraged with **gather4**.</span></span> <span data-ttu-id="85409-129">**gather4** всегда возвращает все запрошенные пикселей текстуры.</span><span class="sxs-lookup"><span data-stu-id="85409-129">**gather4** always returns all requested texels.</span></span>

<span data-ttu-id="85409-130">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="85409-130">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="85409-131">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="85409-131">Vertex Shader</span></span> | <span data-ttu-id="85409-132">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="85409-132">Geometry Shader</span></span> | <span data-ttu-id="85409-133">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="85409-133">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="85409-134">x</span><span class="sxs-lookup"><span data-stu-id="85409-134">x</span></span>             | <span data-ttu-id="85409-135">x</span><span class="sxs-lookup"><span data-stu-id="85409-135">x</span></span>               | <span data-ttu-id="85409-136">x</span><span class="sxs-lookup"><span data-stu-id="85409-136">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="85409-137">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="85409-137">Minimum Shader Model</span></span>

<span data-ttu-id="85409-138">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="85409-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="85409-139">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="85409-139">Shader Model</span></span>                                              | <span data-ttu-id="85409-140">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="85409-140">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="85409-141">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="85409-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="85409-142">да</span><span class="sxs-lookup"><span data-stu-id="85409-142">yes</span></span>       |
| [<span data-ttu-id="85409-143">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="85409-143">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="85409-144">да</span><span class="sxs-lookup"><span data-stu-id="85409-144">yes</span></span>       |
| [<span data-ttu-id="85409-145">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="85409-145">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="85409-146">Нет</span><span class="sxs-lookup"><span data-stu-id="85409-146">no</span></span>        |
| [<span data-ttu-id="85409-147">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="85409-147">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="85409-148">Нет</span><span class="sxs-lookup"><span data-stu-id="85409-148">no</span></span>        |
| [<span data-ttu-id="85409-149">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="85409-149">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="85409-150">Нет</span><span class="sxs-lookup"><span data-stu-id="85409-150">no</span></span>        |
| [<span data-ttu-id="85409-151">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="85409-151">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="85409-152">Нет</span><span class="sxs-lookup"><span data-stu-id="85409-152">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="85409-153">См. также</span><span class="sxs-lookup"><span data-stu-id="85409-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85409-154">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="85409-154">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





