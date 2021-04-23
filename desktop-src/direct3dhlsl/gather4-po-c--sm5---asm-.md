---
title: gather4_po_c (SM5-ASM)
description: Ведет себя так же, как gather4 \_ PO, за исключением того, что выполняет сравнение пикселей текстуры, как в примере \_ c.
ms.assetid: B128EEF3-3440-4F00-9792-20FB1AE075E9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36b07dcad08b4d117a453a3c97e461e6b9b4cab6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412212"
---
# <a name="gather4_po_c-sm5---asm"></a><span data-ttu-id="e43bb-103">gather4 \_ PO \_ c (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="e43bb-103">gather4\_po\_c (sm5 - asm)</span></span>

<span data-ttu-id="e43bb-104">Ведет себя так же, как [**gather4 \_ PO**](gather4-po--sm5---asm-.md), за исключением того, что выполняет сравнение пикселей текстуры, как в [**примере \_ c**](sample-c--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="e43bb-104">Behaves the same as [**gather4\_po**](gather4-po--sm5---asm-.md), except performs comparison on texels, similar to [**sample\_c**](sample-c--sm4---asm-.md).</span></span>



| <span data-ttu-id="e43bb-105">gather4 \_ ЗП \_ c dest \[ . Mask \] , сркаддресс \[ . свиззле \] , сркоффсет \[ . свиззле \] , сркресаурце \[ . свиззле \] , срксамплер \[ . R \] , сркреференцевалуе</span><span class="sxs-lookup"><span data-stu-id="e43bb-105">gather4\_po\_c dest\[.mask\], srcAddress\[.swizzle\], srcOffset\[.swizzle\], srcResource\[.swizzle\], srcSampler\[.R\], srcReferenceValue</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="e43bb-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="e43bb-106">Item</span></span>                                                                                                                                       | <span data-ttu-id="e43bb-107">Описание</span><span class="sxs-lookup"><span data-stu-id="e43bb-107">Description</span></span>                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="e43bb-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="e43bb-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                                            | <span data-ttu-id="e43bb-109">\[в \] адресе результата операции.</span><span class="sxs-lookup"><span data-stu-id="e43bb-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="e43bb-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*сркаддресс*</span><span class="sxs-lookup"><span data-stu-id="e43bb-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>                             | <span data-ttu-id="e43bb-111">\[в \] наборе координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="e43bb-111">\[in\] A set of texture coordinates.</span></span><br/>               |
| <span data-ttu-id="e43bb-112"><span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*сркоффсет*</span><span class="sxs-lookup"><span data-stu-id="e43bb-112"><span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*srcOffset*</span></span><br/>                                 | <span data-ttu-id="e43bb-113">\[в \] смещении.</span><span class="sxs-lookup"><span data-stu-id="e43bb-113">\[in\] The offset.</span></span><br/>                                 |
| <span data-ttu-id="e43bb-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*сркресаурце*</span><span class="sxs-lookup"><span data-stu-id="e43bb-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/>                         | <span data-ttu-id="e43bb-115">\[в \] регистре текстуры.</span><span class="sxs-lookup"><span data-stu-id="e43bb-115">\[in\] A texture register.</span></span><br/>                         |
| <span data-ttu-id="e43bb-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*срксамплер*</span><span class="sxs-lookup"><span data-stu-id="e43bb-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>                             | <span data-ttu-id="e43bb-117">\[в \] регистре образца.</span><span class="sxs-lookup"><span data-stu-id="e43bb-117">\[in\] A sampler register.</span></span><br/>                         |
| <span data-ttu-id="e43bb-118"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*сркреференцевалуе*</span><span class="sxs-lookup"><span data-stu-id="e43bb-118"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span></span><br/> | <span data-ttu-id="e43bb-119">\[в \] выбранном отдельном компоненте.</span><span class="sxs-lookup"><span data-stu-id="e43bb-119">\[in\] Single component selected.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="e43bb-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="e43bb-120">Remarks</span></span>

<span data-ttu-id="e43bb-121">Сведения о сравнении *сркреференцевалуе* с каждым выбранным шаг текселя см. [**\_ в примере c**](sample-c--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="e43bb-121">See [**sample\_c**](sample-c--sm4---asm-.md) for information about how *srcReferenceValue* is compared against each fetched texel.</span></span> <span data-ttu-id="e43bb-122">В отличие от **образца \_ c**, *gather4 \_ PO \_ c* возвращает каждый результат сравнения, а не фильтрует их.</span><span class="sxs-lookup"><span data-stu-id="e43bb-122">Unlike **sample\_c**, *gather4\_po\_c* returns each comparison result, rather than filtering them.</span></span>

<span data-ttu-id="e43bb-123">Эта инструкция, например **gather4 \_ PO**, работает только с 2D-текстурами.</span><span class="sxs-lookup"><span data-stu-id="e43bb-123">This instruction, like **gather4\_po**, only works with 2D textures.</span></span> <span data-ttu-id="e43bb-124">Это в отличие от [**gather4 \_ c**](gather4-c--sm5---asm-.md), которое также работает с текстурекубес.</span><span class="sxs-lookup"><span data-stu-id="e43bb-124">This is unlike [**gather4\_c**](gather4-c--sm5---asm-.md), which also works with TextureCubes.</span></span>

<span data-ttu-id="e43bb-125">Для форматов с компонентами float32, если значение, которое извлекается, нормализовано, или +-INF, оно используется в операции сравнения без изменений.</span><span class="sxs-lookup"><span data-stu-id="e43bb-125">For formats with float32 components, if the value being fetched is normalized, or +-INF, it is used in the comparison operation untouched.</span></span> <span data-ttu-id="e43bb-126">NaN используется в операции сравнения как NaN, но точное битовое представление NaN может быть изменено.</span><span class="sxs-lookup"><span data-stu-id="e43bb-126">NaN is used in the comparison operation as NaN, but the exact bit representation of the NaN may be changed.</span></span> <span data-ttu-id="e43bb-127">При сравнении денормы сбрасываются в ноль.</span><span class="sxs-lookup"><span data-stu-id="e43bb-127">Denorms are flushed to zero going into the comparison.</span></span> <span data-ttu-id="e43bb-128">Для Текстурекубес некоторые синтезы отсутствующих 4-го шаг текселя должны происходить в углах, поэтому понятие возвращаемых битов, не измененных для синтезированного шаг текселя, не применяется.</span><span class="sxs-lookup"><span data-stu-id="e43bb-128">For TextureCubes, some synthesis of the missing 4th texel must occur at corners, so the notion of returning bits unchanged for the synthesized texel does not apply.</span></span>

<span data-ttu-id="e43bb-129">Форматы, поддерживаемые для **gather4 \_ PO \_ c** , совпадают с форматами, поддерживаемыми в **образце \_ c**.</span><span class="sxs-lookup"><span data-stu-id="e43bb-129">Formats supported for **gather4\_po\_c** are same as those supported for **sample\_c**.</span></span> <span data-ttu-id="e43bb-130">Это форматы с одним компонентом, поэтому. R на Срксамплер, а не произвольный свиззле.</span><span class="sxs-lookup"><span data-stu-id="e43bb-130">These are single-component formats, thus the .R on srcSampler, rather than an arbitrary swizzle.</span></span>

<span data-ttu-id="e43bb-131">**gather4 \_ PO \_** в с несвязанным ресурсом возвращает 0.</span><span class="sxs-lookup"><span data-stu-id="e43bb-131">**gather4\_po\_c** on an unbound resource returns 0.</span></span>

<span data-ttu-id="e43bb-132">Используйте этот метод для фильтрации теневых карт.</span><span class="sxs-lookup"><span data-stu-id="e43bb-132">Use this method for shadow map filtering.</span></span>

<span data-ttu-id="e43bb-133">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="e43bb-133">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e43bb-134">Вершина</span><span class="sxs-lookup"><span data-stu-id="e43bb-134">Vertex</span></span> | <span data-ttu-id="e43bb-135">Поверхности</span><span class="sxs-lookup"><span data-stu-id="e43bb-135">Hull</span></span> | <span data-ttu-id="e43bb-136">Домен</span><span class="sxs-lookup"><span data-stu-id="e43bb-136">Domain</span></span> | <span data-ttu-id="e43bb-137">Геометрия</span><span class="sxs-lookup"><span data-stu-id="e43bb-137">Geometry</span></span> | <span data-ttu-id="e43bb-138">Пиксель</span><span class="sxs-lookup"><span data-stu-id="e43bb-138">Pixel</span></span> | <span data-ttu-id="e43bb-139">Вычисления</span><span class="sxs-lookup"><span data-stu-id="e43bb-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e43bb-140">X</span><span class="sxs-lookup"><span data-stu-id="e43bb-140">X</span></span>      | <span data-ttu-id="e43bb-141">X</span><span class="sxs-lookup"><span data-stu-id="e43bb-141">X</span></span>    | <span data-ttu-id="e43bb-142">X</span><span class="sxs-lookup"><span data-stu-id="e43bb-142">X</span></span>      | <span data-ttu-id="e43bb-143">X</span><span class="sxs-lookup"><span data-stu-id="e43bb-143">X</span></span>        | <span data-ttu-id="e43bb-144">X</span><span class="sxs-lookup"><span data-stu-id="e43bb-144">X</span></span>     | <span data-ttu-id="e43bb-145">X</span><span class="sxs-lookup"><span data-stu-id="e43bb-145">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e43bb-146">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="e43bb-146">Minimum Shader Model</span></span>

<span data-ttu-id="e43bb-147">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="e43bb-147">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="e43bb-148">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="e43bb-148">Shader Model</span></span>                                              | <span data-ttu-id="e43bb-149">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="e43bb-149">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e43bb-150">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="e43bb-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e43bb-151">да</span><span class="sxs-lookup"><span data-stu-id="e43bb-151">yes</span></span>       |
| [<span data-ttu-id="e43bb-152">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="e43bb-152">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e43bb-153">Нет</span><span class="sxs-lookup"><span data-stu-id="e43bb-153">no</span></span>        |
| [<span data-ttu-id="e43bb-154">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="e43bb-154">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e43bb-155">Нет</span><span class="sxs-lookup"><span data-stu-id="e43bb-155">no</span></span>        |
| [<span data-ttu-id="e43bb-156">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e43bb-156">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e43bb-157">Нет</span><span class="sxs-lookup"><span data-stu-id="e43bb-157">no</span></span>        |
| [<span data-ttu-id="e43bb-158">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e43bb-158">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e43bb-159">Нет</span><span class="sxs-lookup"><span data-stu-id="e43bb-159">no</span></span>        |
| [<span data-ttu-id="e43bb-160">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e43bb-160">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e43bb-161">Нет</span><span class="sxs-lookup"><span data-stu-id="e43bb-161">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e43bb-162">См. также</span><span class="sxs-lookup"><span data-stu-id="e43bb-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e43bb-163">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e43bb-163">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





