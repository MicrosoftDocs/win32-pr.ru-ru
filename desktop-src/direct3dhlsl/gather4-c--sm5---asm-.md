---
title: gather4_c (SM5-ASM)
description: То же, что и gather4, за исключением того, что этот инструтион выполняет сравнение с пикселей текстуры, как и в примере \_ c.
ms.assetid: 6265151A-36CE-4D31-B7B2-233CEEBDCF87
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35414aa2cd4d9f0686ab7a5cc17b94caa960cec1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996935"
---
# <a name="gather4_c-sm5---asm"></a><span data-ttu-id="d9bdb-103">gather4 \_ c (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="d9bdb-103">gather4\_c (sm5 - asm)</span></span>

<span data-ttu-id="d9bdb-104">То же, что и [**gather4**](gather4--sm5---asm-.md), за исключением того, что этот инструтион выполняет сравнение с пикселей текстуры, как и в [**примере \_ c**](sample-c--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="d9bdb-104">Same as [**gather4**](gather4--sm5---asm-.md), except this instrution performs comparison on texels, similar to [**sample\_c**](sample-c--sm4---asm-.md).</span></span>



| <span data-ttu-id="d9bdb-105">gather4 \_ c \[ \_ аоффимми (u, v) \] dest \[ . Mask \] , сркаддресс \[ . свиззле \] , сркресаурце \[ . свиззле \] , срксамплер \[ . R \] , сркреференцевалуе</span><span class="sxs-lookup"><span data-stu-id="d9bdb-105">gather4\_c\[\_aoffimmi(u,v)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler\[.R\], srcReferenceValue</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="d9bdb-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="d9bdb-106">Item</span></span>                                                                                                                                       | <span data-ttu-id="d9bdb-107">Описание</span><span class="sxs-lookup"><span data-stu-id="d9bdb-107">Description</span></span>                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9bdb-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="d9bdb-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                                            | <span data-ttu-id="d9bdb-109">\[в \] адресе результата операции</span><span class="sxs-lookup"><span data-stu-id="d9bdb-109">\[in\] The address of the result of the operation</span></span><br/>                                    |
| <span data-ttu-id="d9bdb-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*сркаддресс*</span><span class="sxs-lookup"><span data-stu-id="d9bdb-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>                             | <span data-ttu-id="d9bdb-111">\[в \] наборе координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="d9bdb-111">\[in\] A set of texture coordinates.</span></span><br/>                                                 |
| <span data-ttu-id="d9bdb-112"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*сркресаурце*</span><span class="sxs-lookup"><span data-stu-id="d9bdb-112"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/>                         | <span data-ttu-id="d9bdb-113">\[в \] регистре текстуры.</span><span class="sxs-lookup"><span data-stu-id="d9bdb-113">\[in\] A texture register.</span></span><br/>                                                           |
| <span data-ttu-id="d9bdb-114"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*срксамплер*</span><span class="sxs-lookup"><span data-stu-id="d9bdb-114"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>                             | <span data-ttu-id="d9bdb-115">\[в \] регистре образца.</span><span class="sxs-lookup"><span data-stu-id="d9bdb-115">\[in\] A sampler register.</span></span><br/>                                                           |
| <span data-ttu-id="d9bdb-116"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*сркреференцевалуе*</span><span class="sxs-lookup"><span data-stu-id="d9bdb-116"><span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*</span></span><br/> | <span data-ttu-id="d9bdb-117">\[в \] регистре с выбранным одним компонентом, который используется в сравнении.</span><span class="sxs-lookup"><span data-stu-id="d9bdb-117">\[in\] A register with a single component selected, which is used in the comparison.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d9bdb-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="d9bdb-118">Remarks</span></span>

<span data-ttu-id="d9bdb-119">Описание того, как *сркреференцевалуе* сравнивается со всеми полученными шаг текселя, см. в [**образце \_ c**](sample-c--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="d9bdb-119">See [**sample\_c**](sample-c--sm4---asm-.md) for a description of how *srcReferenceValue* gets compared against each fetched texel.</span></span> <span data-ttu-id="d9bdb-120">В отличие от **образца \_ c**, **gather4 \_ c** возвращает каждый результат сравнения, а не фильтрует их.</span><span class="sxs-lookup"><span data-stu-id="d9bdb-120">Unlike **sample\_c**, **gather4\_c** returns each comparison result, rather than filtering them.</span></span>

<span data-ttu-id="d9bdb-121">Для Текстурекубеных углов, где есть три реальных пикселей текстуры, и четвертый должен быть синтезирован, синтез должен быть создан после шага сравнения.</span><span class="sxs-lookup"><span data-stu-id="d9bdb-121">For TextureCube corners, where there are three real texels and a fourth must be synthesized, the synthesis must occur after the comparison step.</span></span> <span data-ttu-id="d9bdb-122">Это означает, что возвращаемый результат сравнения для синтесизед шаг текселя может быть равен 0, 0,33, 0,66 или 1.</span><span class="sxs-lookup"><span data-stu-id="d9bdb-122">This means the returned comparison result for the syntesized texel can be 0, 0.33 , 0.66 , or 1.</span></span> <span data-ttu-id="d9bdb-123">Некоторые реализации могут возвращать только 0 или 1 для синтезированного шаг текселя.</span><span class="sxs-lookup"><span data-stu-id="d9bdb-123">Some implementations may only return either 0 or 1 for the synthesized texel.</span></span> <span data-ttu-id="d9bdb-124">Помимо этого списка возможных результатов, метод для синтезирования шаг текселя не определен.</span><span class="sxs-lookup"><span data-stu-id="d9bdb-124">Aside from this listing of possible results, the method for synthesizing the texel is unspecified.</span></span>

<span data-ttu-id="d9bdb-125">Для форматов с компонентами float32, если значение, которое извлекается, нормализовано, или +-INF, оно используется в операции сравнения без изменений.</span><span class="sxs-lookup"><span data-stu-id="d9bdb-125">For formats with float32 components, if the value being fetched is normalized, or +-INF, it is used in the comparison operation untouched.</span></span> <span data-ttu-id="d9bdb-126">NaN используется в операции сравнения как NaN, но точное битовое представление NaN может быть изменено.</span><span class="sxs-lookup"><span data-stu-id="d9bdb-126">NaN is used in the comparison operation as NaN, but the exact bit representation of the NaN may be changed.</span></span> <span data-ttu-id="d9bdb-127">При сравнении денормы сбрасываются в ноль.</span><span class="sxs-lookup"><span data-stu-id="d9bdb-127">Denorms are flushed to zero going into the comparison.</span></span> <span data-ttu-id="d9bdb-128">Для Текстурекубес некоторые синтезы отсутствующих 4-го шаг текселя должны происходить в углах, поэтому понятие возвращаемых битов, не измененных для синтезированного шаг текселя, не применяется.</span><span class="sxs-lookup"><span data-stu-id="d9bdb-128">For TextureCubes, some synthesis of the missing 4th texel must occur at corners, so the notion of returning bits unchanged for the synthesized texel does not apply.</span></span>

<span data-ttu-id="d9bdb-129">Форматы, поддерживаемые для *gather4 \_ c* , совпадают с форматами, поддерживаемыми в *образце \_ c*.</span><span class="sxs-lookup"><span data-stu-id="d9bdb-129">Formats supported for *gather4\_c* are same as those supported for *sample\_c*.</span></span> <span data-ttu-id="d9bdb-130">Это форматы с одним компонентом, поэтому. R на *срксамплер*, а не произвольный свиззле.</span><span class="sxs-lookup"><span data-stu-id="d9bdb-130">These are single-component formats, thus the .R on *srcSampler*, rather than an arbitrary swizzle.</span></span> <span data-ttu-id="d9bdb-131">**gather4 \_ c** на несвязанном ресурсе возвращает 0.</span><span class="sxs-lookup"><span data-stu-id="d9bdb-131">**gather4\_c** on an unbound resource returns 0.</span></span>

<span data-ttu-id="d9bdb-132">Используйте эту инструкцию для фильтрации пользовательских теневых карт.</span><span class="sxs-lookup"><span data-stu-id="d9bdb-132">Use this instruction for custom shadow map filtering.</span></span>

<span data-ttu-id="d9bdb-133">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="d9bdb-133">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d9bdb-134">Вершина</span><span class="sxs-lookup"><span data-stu-id="d9bdb-134">Vertex</span></span> | <span data-ttu-id="d9bdb-135">Поверхности</span><span class="sxs-lookup"><span data-stu-id="d9bdb-135">Hull</span></span> | <span data-ttu-id="d9bdb-136">Домен</span><span class="sxs-lookup"><span data-stu-id="d9bdb-136">Domain</span></span> | <span data-ttu-id="d9bdb-137">Геометрия</span><span class="sxs-lookup"><span data-stu-id="d9bdb-137">Geometry</span></span> | <span data-ttu-id="d9bdb-138">Пиксель</span><span class="sxs-lookup"><span data-stu-id="d9bdb-138">Pixel</span></span> | <span data-ttu-id="d9bdb-139">Вычисления</span><span class="sxs-lookup"><span data-stu-id="d9bdb-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="d9bdb-140">X</span><span class="sxs-lookup"><span data-stu-id="d9bdb-140">X</span></span>      | <span data-ttu-id="d9bdb-141">X</span><span class="sxs-lookup"><span data-stu-id="d9bdb-141">X</span></span>    | <span data-ttu-id="d9bdb-142">X</span><span class="sxs-lookup"><span data-stu-id="d9bdb-142">X</span></span>      | <span data-ttu-id="d9bdb-143">X</span><span class="sxs-lookup"><span data-stu-id="d9bdb-143">X</span></span>        | <span data-ttu-id="d9bdb-144">X</span><span class="sxs-lookup"><span data-stu-id="d9bdb-144">X</span></span>     | <span data-ttu-id="d9bdb-145">X</span><span class="sxs-lookup"><span data-stu-id="d9bdb-145">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d9bdb-146">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="d9bdb-146">Minimum Shader Model</span></span>

<span data-ttu-id="d9bdb-147">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="d9bdb-147">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="d9bdb-148">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="d9bdb-148">Shader Model</span></span>                                              | <span data-ttu-id="d9bdb-149">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="d9bdb-149">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d9bdb-150">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="d9bdb-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d9bdb-151">да</span><span class="sxs-lookup"><span data-stu-id="d9bdb-151">yes</span></span>       |
| [<span data-ttu-id="d9bdb-152">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="d9bdb-152">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d9bdb-153">Нет</span><span class="sxs-lookup"><span data-stu-id="d9bdb-153">no</span></span>        |
| [<span data-ttu-id="d9bdb-154">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="d9bdb-154">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d9bdb-155">Нет</span><span class="sxs-lookup"><span data-stu-id="d9bdb-155">no</span></span>        |
| [<span data-ttu-id="d9bdb-156">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d9bdb-156">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d9bdb-157">Нет</span><span class="sxs-lookup"><span data-stu-id="d9bdb-157">no</span></span>        |
| [<span data-ttu-id="d9bdb-158">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d9bdb-158">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d9bdb-159">Нет</span><span class="sxs-lookup"><span data-stu-id="d9bdb-159">no</span></span>        |
| [<span data-ttu-id="d9bdb-160">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d9bdb-160">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d9bdb-161">Нет</span><span class="sxs-lookup"><span data-stu-id="d9bdb-161">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d9bdb-162">См. также</span><span class="sxs-lookup"><span data-stu-id="d9bdb-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9bdb-163">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d9bdb-163">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





