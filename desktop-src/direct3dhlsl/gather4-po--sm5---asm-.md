---
title: gather4_po (SM5-ASM)
description: Вариант gather4, но вместо поддержки немедленного смещения \-8.. 7 \ смещение поступает в качестве параметра инструкции, а также имеет больший диапазон \-32.. 31 \.
ms.assetid: A77A32B4-BD4F-46E7-9999-13EAA8A26974
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9197fee97645333d37d589db36c3774852b12229
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983873"
---
# <a name="gather4_po-sm5---asm"></a><span data-ttu-id="1a682-103">gather4 \_ PO (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="1a682-103">gather4\_po (sm5 - asm)</span></span>

<span data-ttu-id="1a682-104">Вариант [gather4](gather4--sm5---asm-.md), но вместо поддержки немедленного смещения \[ -8.. 7 \] смещение поступает в качестве параметра инструкции, а также имеет больший диапазон \[ -32.. 31 \] .</span><span class="sxs-lookup"><span data-stu-id="1a682-104">A variant of [gather4](gather4--sm5---asm-.md), but instead of supporting an immediate offset \[-8..7\], the offset comes as a parameter to the instruction, and also has larger range of \[-32..31\].</span></span>



| <span data-ttu-id="1a682-105">gather4 \_ PO \[ . Маска \] , сркаддресс \[ . свиззле \] , сркоффсет \[ . свиззле \] , сркресаурце \[ . свиззле \] , срксамплер \[ . Select \_ Component\]</span><span class="sxs-lookup"><span data-stu-id="1a682-105">gather4\_po dest\[.mask\], srcAddress\[.swizzle\], srcOffset\[.swizzle\], srcResource\[.swizzle\], srcSampler\[.select\_component\]</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="1a682-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="1a682-106">Item</span></span>                                                                                                               | <span data-ttu-id="1a682-107">Описание</span><span class="sxs-lookup"><span data-stu-id="1a682-107">Description</span></span>                                                   |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="1a682-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="1a682-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="1a682-109">\[в \] адресе результата операции.</span><span class="sxs-lookup"><span data-stu-id="1a682-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="1a682-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*сркаддресс*</span><span class="sxs-lookup"><span data-stu-id="1a682-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="1a682-111">\[в \] наборе координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="1a682-111">\[in\] A set of texture coordinates.</span></span><br/>               |
| <span data-ttu-id="1a682-112"><span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*сркоффсет*</span><span class="sxs-lookup"><span data-stu-id="1a682-112"><span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*srcOffset*</span></span><br/>         | <span data-ttu-id="1a682-113">\[в \] смещении.</span><span class="sxs-lookup"><span data-stu-id="1a682-113">\[in\] The offset.</span></span><br/>                                 |
| <span data-ttu-id="1a682-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*сркресаурце*</span><span class="sxs-lookup"><span data-stu-id="1a682-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="1a682-115">\[в \] регистре текстуры.</span><span class="sxs-lookup"><span data-stu-id="1a682-115">\[in\] A texture register.</span></span><br/>                         |
| <span data-ttu-id="1a682-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*срксамплер*</span><span class="sxs-lookup"><span data-stu-id="1a682-116"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="1a682-117">\[в \] регистре образца.</span><span class="sxs-lookup"><span data-stu-id="1a682-117">\[in\] A sampler register.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="1a682-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="1a682-118">Remarks</span></span>

<span data-ttu-id="1a682-119">Первые два компонента параметра смещения 4 вектора предоставляют 32-разрядное смещение целых чисел.</span><span class="sxs-lookup"><span data-stu-id="1a682-119">The first two components of the 4-vector offset parameter supply 32-bit integer offsets.</span></span> <span data-ttu-id="1a682-120">Другие компоненты этого параметра игнорируются.</span><span class="sxs-lookup"><span data-stu-id="1a682-120">The other components of this parameter are ignored.</span></span>

<span data-ttu-id="1a682-121">6-младшие значащие биты каждого значения смещения учитываются как значение со знаком, а возвращает \[ — 32.. 31 \] диапазон.</span><span class="sxs-lookup"><span data-stu-id="1a682-121">The 6 least significant bits of each offset value is honored as a signed value, yielding \[-32..31\] range.</span></span>

<span data-ttu-id="1a682-122">Эта инструкция работает только с 2D-текстурами, в отличие от **gather4**, которая также работает с текстурекубес.</span><span class="sxs-lookup"><span data-stu-id="1a682-122">This instruction only works with 2D textures, unlike **gather4**, which also works with TextureCubes.</span></span>

<span data-ttu-id="1a682-123">Единственными режимами, принятыми в этом образце, являются режимы адресации.</span><span class="sxs-lookup"><span data-stu-id="1a682-123">The only modes honored in the sampler are the addressing modes.</span></span> <span data-ttu-id="1a682-124">Используется только наиболее детализированное MIP в представлении ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1a682-124">Only the most detailed mip in the resource view is used.</span></span>

<span data-ttu-id="1a682-125">Если адрес попадает в центр шаг текселя, это не значит, что другие пикселей текстуры могут быть обнулены.</span><span class="sxs-lookup"><span data-stu-id="1a682-125">If the address falls on a texel center, this does not mean the other texels can be zeroed out.</span></span>

<span data-ttu-id="1a682-126">Параметр *срксамплер* включает \[ . Выберите \_ компонент \] , который позволяет получить один компонент текстуры, включая возврат значений по умолчанию для отсутствующих компонентов.</span><span class="sxs-lookup"><span data-stu-id="1a682-126">The *srcSampler* parameter includes \[.select\_component\], allowing any single component of a texture to be retrieved, including returning defaults for missing components.</span></span>

<span data-ttu-id="1a682-127">Для форматов с компонентами float32, если извлекаемое значение нормализовано, денормализовано, +-0 или +-INF, оно возвращается в шейдер без изменений.</span><span class="sxs-lookup"><span data-stu-id="1a682-127">For formats with float32 components, if the value being fetched is normalized, denormalized, +-0 or +-INF, it is returned to the shader unaltered.</span></span> <span data-ttu-id="1a682-128">NaN возвращается как NaN, но точное битовое представление NaN может быть изменено.</span><span class="sxs-lookup"><span data-stu-id="1a682-128">NaN is returned as NaN, but the exact bit representation of the NaN may be changed.</span></span> <span data-ttu-id="1a682-129">Для Текстурекубес некоторые синтезы отсутствующих 4-го шаг текселя должны происходить в углах, поэтому понятие возвращаемых битов не меняется для синтезированного шаг текселя не применяется, а денорма может быть сброшена.</span><span class="sxs-lookup"><span data-stu-id="1a682-129">For TextureCubes, some synthesis of the missing 4th texel must occur at corners, so the notion of returning bits unchanged for the synthesized texel does not apply, and denorms could be flushed.</span></span>

<span data-ttu-id="1a682-130">Используйте эту инструкцию, чтобы расширить диапазон смещений **gather4** до большего и программируемого.</span><span class="sxs-lookup"><span data-stu-id="1a682-130">Use this instruction to extend offset range of **gather4** to be larger and programmable.</span></span> <span data-ttu-id="1a682-131">Суффикс "PO" в имени означает "Программируемое смещение".</span><span class="sxs-lookup"><span data-stu-id="1a682-131">The "po" suffix on the name means "programmable offset".</span></span>

<span data-ttu-id="1a682-132">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="1a682-132">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="1a682-133">Вершина</span><span class="sxs-lookup"><span data-stu-id="1a682-133">Vertex</span></span> | <span data-ttu-id="1a682-134">Поверхности</span><span class="sxs-lookup"><span data-stu-id="1a682-134">Hull</span></span> | <span data-ttu-id="1a682-135">Домен</span><span class="sxs-lookup"><span data-stu-id="1a682-135">Domain</span></span> | <span data-ttu-id="1a682-136">Геометрия</span><span class="sxs-lookup"><span data-stu-id="1a682-136">Geometry</span></span> | <span data-ttu-id="1a682-137">Пиксель</span><span class="sxs-lookup"><span data-stu-id="1a682-137">Pixel</span></span> | <span data-ttu-id="1a682-138">Вычисления</span><span class="sxs-lookup"><span data-stu-id="1a682-138">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="1a682-139">X</span><span class="sxs-lookup"><span data-stu-id="1a682-139">X</span></span>      | <span data-ttu-id="1a682-140">X</span><span class="sxs-lookup"><span data-stu-id="1a682-140">X</span></span>    | <span data-ttu-id="1a682-141">X</span><span class="sxs-lookup"><span data-stu-id="1a682-141">X</span></span>      | <span data-ttu-id="1a682-142">X</span><span class="sxs-lookup"><span data-stu-id="1a682-142">X</span></span>        | <span data-ttu-id="1a682-143">X</span><span class="sxs-lookup"><span data-stu-id="1a682-143">X</span></span>     | <span data-ttu-id="1a682-144">X</span><span class="sxs-lookup"><span data-stu-id="1a682-144">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1a682-145">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="1a682-145">Minimum Shader Model</span></span>

<span data-ttu-id="1a682-146">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="1a682-146">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="1a682-147">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="1a682-147">Shader Model</span></span>                                              | <span data-ttu-id="1a682-148">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="1a682-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1a682-149">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="1a682-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1a682-150">да</span><span class="sxs-lookup"><span data-stu-id="1a682-150">yes</span></span>       |
| [<span data-ttu-id="1a682-151">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="1a682-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1a682-152">Нет</span><span class="sxs-lookup"><span data-stu-id="1a682-152">no</span></span>        |
| [<span data-ttu-id="1a682-153">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="1a682-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1a682-154">Нет</span><span class="sxs-lookup"><span data-stu-id="1a682-154">no</span></span>        |
| [<span data-ttu-id="1a682-155">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1a682-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1a682-156">Нет</span><span class="sxs-lookup"><span data-stu-id="1a682-156">no</span></span>        |
| [<span data-ttu-id="1a682-157">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1a682-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1a682-158">Нет</span><span class="sxs-lookup"><span data-stu-id="1a682-158">no</span></span>        |
| [<span data-ttu-id="1a682-159">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1a682-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1a682-160">Нет</span><span class="sxs-lookup"><span data-stu-id="1a682-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1a682-161">См. также</span><span class="sxs-lookup"><span data-stu-id="1a682-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a682-162">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1a682-162">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





