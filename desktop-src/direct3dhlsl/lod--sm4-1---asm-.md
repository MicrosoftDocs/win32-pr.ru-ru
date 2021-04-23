---
title: Лод (SM 4.1-ASM)
description: Возвращает уровень детализации (Лод), который будет использоваться для фильтрации текстур.
ms.assetid: A5931203-8CD7-4FC9-A4A4-CA981F38C7A3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1c1ca5a22a735945b76a60c175c665c5cf58fb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784947"
---
# <a name="lod-sm41---asm"></a><span data-ttu-id="25407-103">Лод (SM 4.1-ASM)</span><span class="sxs-lookup"><span data-stu-id="25407-103">lod (sm4.1 - asm)</span></span>

<span data-ttu-id="25407-104">Возвращает уровень детализации (Лод), который будет использоваться для фильтрации текстур.</span><span class="sxs-lookup"><span data-stu-id="25407-104">Returns the level of detail (LOD) that would be used for texture filtering.</span></span>



| <span data-ttu-id="25407-105">Лод dest \[ . Mask \] , сркаддресс \[ . свиззле \] , сркресаурце \[ . свиззле \] , срксамплер</span><span class="sxs-lookup"><span data-stu-id="25407-105">lod dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler</span></span> |
|--------------------------------------------------------------------------------|



 



| <span data-ttu-id="25407-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="25407-106">Item</span></span>                                                                                                               | <span data-ttu-id="25407-107">Описание</span><span class="sxs-lookup"><span data-stu-id="25407-107">Description</span></span>                                     |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="25407-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="25407-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                    | <span data-ttu-id="25407-109">\[в \] адресе результатов.</span><span class="sxs-lookup"><span data-stu-id="25407-109">\[in\] The address of the results.</span></span><br/>   |
| <span data-ttu-id="25407-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*сркаддресс*</span><span class="sxs-lookup"><span data-stu-id="25407-110"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>     | <span data-ttu-id="25407-111">\[в \] наборе координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="25407-111">\[in\] A set of texture coordinates.</span></span><br/> |
| <span data-ttu-id="25407-112"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*сркресаурце*</span><span class="sxs-lookup"><span data-stu-id="25407-112"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/> | <span data-ttu-id="25407-113">\[в \] регистре текстуры.</span><span class="sxs-lookup"><span data-stu-id="25407-113">\[in\] A texture register.</span></span><br/>           |
| <span data-ttu-id="25407-114"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*срксамплер*</span><span class="sxs-lookup"><span data-stu-id="25407-114"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>     | <span data-ttu-id="25407-115">\[в \] регистре образца.</span><span class="sxs-lookup"><span data-stu-id="25407-115">\[in\] A sampler register.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="25407-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="25407-116">Remarks</span></span>

<span data-ttu-id="25407-117">Это ведет себя как [Пример](sample--sm4---asm-.md) инструкции, но отфильтрованный образец не создается.</span><span class="sxs-lookup"><span data-stu-id="25407-117">This behaves like the [sample](sample--sm4---asm-.md) instruction, but a filtered sample is not generated.</span></span> <span data-ttu-id="25407-118">Инструкция рассчитывает следующий вектор (Клампедлод, Нонклампедлод, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="25407-118">The instruction computes the following vector (ClampedLOD, NonClampedLOD, 0, 0).</span></span> <span data-ttu-id="25407-119">Нонклампедлод — это вычисленное значение Лод, которое игнорирует любые фиксации из образца или текстуры (IE: она может возвращать отрицательные значения). Клампедлод — это вычисленное значение Лод, которое будет использоваться фактическим **образцом** инструкции.</span><span class="sxs-lookup"><span data-stu-id="25407-119">NonClampedLOD is a computed LOD value that ignores any clamping from either the sampler or the texture (ie: it can return negative values.) ClampedLOD is a computed LOD value that would be used by the actual **sample** instruction.</span></span> <span data-ttu-id="25407-120">Свиззле On *сркресаурце* позволяет свиззлед возвращаемые значения произвольно, прежде чем они записываются в место назначения.</span><span class="sxs-lookup"><span data-stu-id="25407-120">The swizzle on *srcResource* allows the returned values to be swizzled arbitrarily before they are written to the destination.</span></span>

<span data-ttu-id="25407-121">Если нет ресурса, привязанного к указанному слоту, возвращается значение 0.</span><span class="sxs-lookup"><span data-stu-id="25407-121">If there is no resource bound to the specified slot, 0 is returned.</span></span>

<span data-ttu-id="25407-122">Если в образце используется анизотропная фильтрация, Лод должен соответствовать уровню MIP дробной части, основанной на меньшей оси эллиптического пространства.</span><span class="sxs-lookup"><span data-stu-id="25407-122">If the sampler is using anisotropic filtering the LOD should correspond to the fractional mip level based on the smaller axis of the elliptical footprint.</span></span>

<span data-ttu-id="25407-123">Это допустимо для следующих типов текстур: Texture1D, Texture2D, Texture3D и Текстурекубе.</span><span class="sxs-lookup"><span data-stu-id="25407-123">This is valid for the following texture types: Texture1D, Texture2D, Texture3D and TextureCube.</span></span>

<span data-ttu-id="25407-124">Инструкция **Лод** не определяется при использовании с образцом, в котором задана Фильтрация Point MIP, в частности, любое \_ перечисление D3D10 Filter, заканчивающееся на MIP \_ Point.</span><span class="sxs-lookup"><span data-stu-id="25407-124">The **lod** instruction is not defined when used with a sampler that specifies point mip filtering, specifically, any D3D10\_FILTER enum that ends in MIP\_POINT.</span></span> <span data-ttu-id="25407-125">(Пример такой: D3D10 \_ ФИЛЬТРОВАТЬ \_ min \_ MAG \_ MIP \_ Point.)</span><span class="sxs-lookup"><span data-stu-id="25407-125">(An example of this would be D3D10\_FILTER\_MIN\_MAG\_MIP\_POINT.)</span></span>

<span data-ttu-id="25407-126">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="25407-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="25407-127">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="25407-127">Vertex Shader</span></span> | <span data-ttu-id="25407-128">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="25407-128">Geometry Shader</span></span> | <span data-ttu-id="25407-129">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="25407-129">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               |                 | <span data-ttu-id="25407-130">x</span><span class="sxs-lookup"><span data-stu-id="25407-130">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="25407-131">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="25407-131">Minimum Shader Model</span></span>

<span data-ttu-id="25407-132">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="25407-132">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="25407-133">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="25407-133">Shader Model</span></span>                                              | <span data-ttu-id="25407-134">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="25407-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="25407-135">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="25407-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="25407-136">да</span><span class="sxs-lookup"><span data-stu-id="25407-136">yes</span></span>       |
| [<span data-ttu-id="25407-137">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="25407-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="25407-138">да</span><span class="sxs-lookup"><span data-stu-id="25407-138">yes</span></span>       |
| [<span data-ttu-id="25407-139">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="25407-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="25407-140">Нет</span><span class="sxs-lookup"><span data-stu-id="25407-140">no</span></span>        |
| [<span data-ttu-id="25407-141">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="25407-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="25407-142">Нет</span><span class="sxs-lookup"><span data-stu-id="25407-142">no</span></span>        |
| [<span data-ttu-id="25407-143">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="25407-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="25407-144">Нет</span><span class="sxs-lookup"><span data-stu-id="25407-144">no</span></span>        |
| [<span data-ttu-id="25407-145">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="25407-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="25407-146">Нет</span><span class="sxs-lookup"><span data-stu-id="25407-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="25407-147">См. также</span><span class="sxs-lookup"><span data-stu-id="25407-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25407-148">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="25407-148">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





