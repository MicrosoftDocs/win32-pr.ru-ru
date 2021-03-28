---
title: sample_b (SM4-ASM)
description: Выборка данных из указанного элемента или текстуры с использованием указанного адреса и режима фильтрации, определенного заданным образцом. | sample_b (SM4-ASM)
ms.assetid: FC0DF03E-9C21-4E88-96ED-EEFE86017E7C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72e82696ecc5b01847f87b39cbfeba0c665bcde4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273587"
---
# <a name="sample_b-sm4---asm"></a><span data-ttu-id="b575c-104">Пример \_ б (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="b575c-104">sample\_b (sm4 - asm)</span></span>

<span data-ttu-id="b575c-105">Выборка данных из указанного элемента или текстуры с использованием указанного адреса и режима фильтрации, определенного заданным образцом.</span><span class="sxs-lookup"><span data-stu-id="b575c-105">Samples data from the specified Element/texture using the specified address and the filtering mode identified by the given sampler.</span></span>



| <span data-ttu-id="b575c-106">Пример \_ б \[ \_ аоффимми (u, v, w) \] dest \[ . Mask \] , сркаддресс \[ . свиззле \] , сркресаурце \[ . свиззле \] , срксамплер, срклодбиас. Выбор \_ компонента</span><span class="sxs-lookup"><span data-stu-id="b575c-106">sample\_b\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler, srcLODBias.select\_component</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="b575c-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="b575c-107">Item</span></span>                                                                                                               | <span data-ttu-id="b575c-108">Описание</span><span class="sxs-lookup"><span data-stu-id="b575c-108">Description</span></span>                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b575c-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="b575c-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="b575c-110">\[в \] адресе результата операции.</span><span class="sxs-lookup"><span data-stu-id="b575c-110">\[in\] The address of the result of the operation.</span></span><br/>                                                              |
| <span data-ttu-id="b575c-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*сркаддресс*</span><span class="sxs-lookup"><span data-stu-id="b575c-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="b575c-112">\[в \] наборе координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="b575c-112">\[in\] A set of texture coordinates.</span></span> <span data-ttu-id="b575c-113">Дополнительные сведения см. в [примере](sample--sm4---asm-.md) инструкции.</span><span class="sxs-lookup"><span data-stu-id="b575c-113">For more information see the [sample](sample--sm4---asm-.md) instruction.</span></span><br/> |
| <span data-ttu-id="b575c-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*сркресаурце*</span><span class="sxs-lookup"><span data-stu-id="b575c-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="b575c-115">\[в \] регистре текстуры.</span><span class="sxs-lookup"><span data-stu-id="b575c-115">\[in\] A texture register.</span></span> <span data-ttu-id="b575c-116">Дополнительные сведения см. в **примере** инструкции.</span><span class="sxs-lookup"><span data-stu-id="b575c-116">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="b575c-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*срксамплер*</span><span class="sxs-lookup"><span data-stu-id="b575c-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="b575c-118">\[в \] регистре образца.</span><span class="sxs-lookup"><span data-stu-id="b575c-118">\[in\] A sampler register.</span></span> <span data-ttu-id="b575c-119">Дополнительные сведения см. в **примере** инструкции.</span><span class="sxs-lookup"><span data-stu-id="b575c-119">For more information see the **sample** instruction.</span></span><br/>                                 |
| <span data-ttu-id="b575c-120"><span id="srcLODBias"></span><span id="srclodbias"></span><span id="SRCLODBIAS"></span>*срклодбиас*</span><span class="sxs-lookup"><span data-stu-id="b575c-120"><span id="srcLODBias"></span><span id="srclodbias"></span><span id="SRCLODBIAS"></span>*srcLODBias*</span></span><br/>     | <span data-ttu-id="b575c-121">\[\]сведения об этом параметре см. в разделе **"Примечания"** .</span><span class="sxs-lookup"><span data-stu-id="b575c-121">\[in\] See the **Remarks** section for information about this parameter.</span></span><br/>                                        |



 

## <a name="remarks"></a><span data-ttu-id="b575c-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="b575c-122">Remarks</span></span>

<span data-ttu-id="b575c-123">Исходные данные могут поступать из любого типа ресурсов, кроме буферов.</span><span class="sxs-lookup"><span data-stu-id="b575c-123">The source data may come from any Resource Type, other than Buffers.</span></span> <span data-ttu-id="b575c-124">Дополнительное смещение применяется к уровню детализации, вычисляемому в ходе выполнения инструкции.</span><span class="sxs-lookup"><span data-stu-id="b575c-124">An additional bias is applied to the level of detail computed as part of the instruction execution.</span></span>

<span data-ttu-id="b575c-125">Эта инструкция похожа на [образец](sample--sm4---asm-.md) инструкции с добавлением указанного значения *срклодбиас* к уровню детализации, вычисленному в рамках выполнения инструкции до выбора карт MIP.</span><span class="sxs-lookup"><span data-stu-id="b575c-125">This instruction behaves like the [sample](sample--sm4---asm-.md) instruction with the addition of applying the specified *srcLODBias* value to the level of detail value computed as part of the instruction execution prior to selecting the mip map(s).</span></span> <span data-ttu-id="b575c-126">Значение *срклодбиас* добавляется в ВЫЧИСЛЕНную Лод для каждого пикселя вместе со значением «выборка миплодбиас» перед срезом Минлод и макслод.</span><span class="sxs-lookup"><span data-stu-id="b575c-126">The *srcLODBias* value is added to the computed LOD on a per-pixel basis, along with the sampler MipLODBias value, prior to the clamp to MinLOD and MaxLOD.</span></span>

### <a name="restrictions"></a><span data-ttu-id="b575c-127">Ограничения</span><span class="sxs-lookup"><span data-stu-id="b575c-127">Restrictions</span></span>

-   <span data-ttu-id="b575c-128">**пример \_ б** наследует те же ограничения, что и [образец](sample--sm4---asm-.md) инструкции, а также дополнительные ограничения для дополнительного параметра.</span><span class="sxs-lookup"><span data-stu-id="b575c-128">**sample\_b** inherits the same restrictions as the [sample](sample--sm4---asm-.md) instruction, plus additional restrictions for its additional parameter.</span></span>
-   <span data-ttu-id="b575c-129">Диапазон *срклодбиас* имеет значение (-15.99 f). значения за пределами этого диапазона приведут к неопределенным результатам.</span><span class="sxs-lookup"><span data-stu-id="b575c-129">The range of *srcLODBias* is (-16.0f to 15.99f); values outside of this range will produce undefined results.</span></span>
-   <span data-ttu-id="b575c-130">*срклодбиас* должен использовать один селектор компонента, если он не является скалярным.</span><span class="sxs-lookup"><span data-stu-id="b575c-130">*srcLODBias* must use a single component selector if it is not a scalar immediate.</span></span>

<span data-ttu-id="b575c-131">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="b575c-131">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b575c-132">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="b575c-132">Vertex Shader</span></span> | <span data-ttu-id="b575c-133">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="b575c-133">Geometry Shader</span></span> | <span data-ttu-id="b575c-134">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="b575c-134">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="b575c-135">x</span><span class="sxs-lookup"><span data-stu-id="b575c-135">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b575c-136">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="b575c-136">Minimum Shader Model</span></span>

<span data-ttu-id="b575c-137">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="b575c-137">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b575c-138">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="b575c-138">Shader Model</span></span>                                              | <span data-ttu-id="b575c-139">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="b575c-139">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b575c-140">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="b575c-140">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b575c-141">да</span><span class="sxs-lookup"><span data-stu-id="b575c-141">yes</span></span>       |
| [<span data-ttu-id="b575c-142">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="b575c-142">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b575c-143">да</span><span class="sxs-lookup"><span data-stu-id="b575c-143">yes</span></span>       |
| [<span data-ttu-id="b575c-144">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="b575c-144">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b575c-145">да</span><span class="sxs-lookup"><span data-stu-id="b575c-145">yes</span></span>       |
| [<span data-ttu-id="b575c-146">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b575c-146">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b575c-147">Нет</span><span class="sxs-lookup"><span data-stu-id="b575c-147">no</span></span>        |
| [<span data-ttu-id="b575c-148">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b575c-148">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b575c-149">Нет</span><span class="sxs-lookup"><span data-stu-id="b575c-149">no</span></span>        |
| [<span data-ttu-id="b575c-150">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b575c-150">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b575c-151">Нет</span><span class="sxs-lookup"><span data-stu-id="b575c-151">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b575c-152">См. также</span><span class="sxs-lookup"><span data-stu-id="b575c-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b575c-153">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b575c-153">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





