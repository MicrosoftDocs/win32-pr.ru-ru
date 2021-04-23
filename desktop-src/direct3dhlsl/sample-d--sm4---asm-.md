---
title: sample_d (SM4-ASM)
description: Выборка данных из указанного элемента или текстуры с использованием указанного адреса и режима фильтрации, определенного заданным образцом. | sample_d (SM4-ASM)
ms.assetid: 9CF57C4A-C0D1-4D57-A5EE-62BBBB291438
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abe2d3ad310c18ff2bb10e101c95e0267d534fed
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998186"
---
# <a name="sample_d-sm4---asm"></a><span data-ttu-id="47e9a-104">Пример \_ d (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="47e9a-104">sample\_d (sm4 - asm)</span></span>

<span data-ttu-id="47e9a-105">Выборка данных из указанного элемента или текстуры с использованием указанного адреса и режима фильтрации, определенного заданным образцом.</span><span class="sxs-lookup"><span data-stu-id="47e9a-105">Samples data from the specified Element/texture using the specified address and the filtering mode identified by the given sampler.</span></span>



| <span data-ttu-id="47e9a-106">ссампле \_ d \[ \_ аоффимми (u, v, w) \] dest \[ . Mask \] , сркаддресс \[ . свиззле \] , сркресаурце \[ . свиззле \] , срксамплер, сркксдеривативес \[ . swizzle \] , srcYDerivatives \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="47e9a-106">ssample\_d\[\_aoffimmi(u,v,w)\] dest\[.mask\], srcAddress\[.swizzle\], srcResource\[.swizzle\], srcSampler, srcXDerivatives\[.swizzle\], srcYDerivatives\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="47e9a-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="47e9a-107">Item</span></span>                                                                                                                               | <span data-ttu-id="47e9a-108">Описание</span><span class="sxs-lookup"><span data-stu-id="47e9a-108">Description</span></span>                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47e9a-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="47e9a-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/>                                                                    | <span data-ttu-id="47e9a-110">\[в \] адресе результатов операции.</span><span class="sxs-lookup"><span data-stu-id="47e9a-110">\[in\] The address of the results of the operation.</span></span><br/>                                                                  |
| <span data-ttu-id="47e9a-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*сркаддресс*</span><span class="sxs-lookup"><span data-stu-id="47e9a-111"><span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*</span></span><br/>                     | <span data-ttu-id="47e9a-112">\[в \] наборе координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="47e9a-112">\[in\] A set of texture coordinates.</span></span> <span data-ttu-id="47e9a-113">Дополнительные сведения см. в [примере](sample--sm4---asm-.md) инструкции.</span><span class="sxs-lookup"><span data-stu-id="47e9a-113">For more information see the [sample](sample--sm4---asm-.md) instruction.</span></span><br/>      |
| <span data-ttu-id="47e9a-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*сркресаурце*</span><span class="sxs-lookup"><span data-stu-id="47e9a-114"><span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*</span></span><br/>                 | <span data-ttu-id="47e9a-115">\[в \] регистре текстуры.</span><span class="sxs-lookup"><span data-stu-id="47e9a-115">\[in\] A texture register.</span></span> <span data-ttu-id="47e9a-116">Дополнительные сведения см. в **примере** инструкции.</span><span class="sxs-lookup"><span data-stu-id="47e9a-116">For more information see the **sample** instruction.</span></span><br/>                                      |
| <span data-ttu-id="47e9a-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*срксамплер*</span><span class="sxs-lookup"><span data-stu-id="47e9a-117"><span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*</span></span><br/>                     | <span data-ttu-id="47e9a-118">\[в \] регистре образца.</span><span class="sxs-lookup"><span data-stu-id="47e9a-118">\[in\] A sampler register.</span></span> <span data-ttu-id="47e9a-119">Дополнительные сведения см. в **примере** инструкции.</span><span class="sxs-lookup"><span data-stu-id="47e9a-119">For more information see the **sample** instruction.</span></span><br/>                                      |
| <span data-ttu-id="47e9a-120"><span id="srcXDerivatives"></span><span id="srcxderivatives"></span><span id="SRCXDERIVATIVES"></span>*сркксдеривативес*</span><span class="sxs-lookup"><span data-stu-id="47e9a-120"><span id="srcXDerivatives"></span><span id="srcxderivatives"></span><span id="SRCXDERIVATIVES"></span>*srcXDerivatives*</span></span><br/> | <span data-ttu-id="47e9a-121">\[в \] производных источниках для исходного адреса в направлении по оси x.</span><span class="sxs-lookup"><span data-stu-id="47e9a-121">\[in\] The derivatives for the source address in the x direction.</span></span> <span data-ttu-id="47e9a-122">Дополнительные сведения см. в разделе **Примечания**.</span><span class="sxs-lookup"><span data-stu-id="47e9a-122">For more information, see the **Remarks** section.</span></span><br/> |
| <span data-ttu-id="47e9a-123"><span id="srcYDerivatives"></span><span id="srcyderivatives"></span><span id="SRCYDERIVATIVES"></span>*срцидеривативес*</span><span class="sxs-lookup"><span data-stu-id="47e9a-123"><span id="srcYDerivatives"></span><span id="srcyderivatives"></span><span id="SRCYDERIVATIVES"></span>*srcYDerivatives*</span></span><br/> | <span data-ttu-id="47e9a-124">\[в \] производных источниках для исходного адреса в направлении y.</span><span class="sxs-lookup"><span data-stu-id="47e9a-124">\[in\] The derivatives for the source address in the y direction.</span></span> <span data-ttu-id="47e9a-125">Дополнительные сведения см. в разделе **Примечания**.</span><span class="sxs-lookup"><span data-stu-id="47e9a-125">For more information, see the **Remarks** section.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="47e9a-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="47e9a-126">Remarks</span></span>

<span data-ttu-id="47e9a-127">Эта инструкция ведет себя как [Пример](sample--sm4---asm-.md) инструкции, за исключением того, что производные от адреса источника в направлении x и направление y предоставляются дополнительными параметрами, *сркксдеривативес* и *срцидеривативес* соответственно.</span><span class="sxs-lookup"><span data-stu-id="47e9a-127">This instruction behaves like the [sample](sample--sm4---asm-.md) instruction, except that derivatives for the source address in the x direction and the y direction are provided by extra parameters, *srcXDerivatives* and *srcYDerivatives*, respectively.</span></span> <span data-ttu-id="47e9a-128">Эти производные данные находятся в нормализованном пространстве координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="47e9a-128">These derivatives are in normalized texture coordinate space.</span></span>

<span data-ttu-id="47e9a-129">Компоненты r, g и b *сркксдеривативес* (POS-свиззле) предоставляют du/DX, DV/DX и DW/DX.</span><span class="sxs-lookup"><span data-stu-id="47e9a-129">The r, g and b components of *srcXDerivatives* (POS-swizzle) provide du/dx, dv/dx and dw/dx.</span></span> <span data-ttu-id="47e9a-130">Компонент "a" (POS-свиззле) не учитывается.</span><span class="sxs-lookup"><span data-stu-id="47e9a-130">The 'a' component (POS-swizzle) is ignored.</span></span>

<span data-ttu-id="47e9a-131">Компоненты r, g и b *срцидеривативес* (POS-свиззле) предоставляют du/dy, DV/dy, DW/dy.</span><span class="sxs-lookup"><span data-stu-id="47e9a-131">The r, g and b components of *srcYDerivatives* (POS-swizzle) provide du/dy, dv/dy and dw/dy.</span></span> <span data-ttu-id="47e9a-132">Компонент "a" (POS-свиззле) не учитывается.</span><span class="sxs-lookup"><span data-stu-id="47e9a-132">The 'a' component (POS-swizzle) is ignored.</span></span>

<span data-ttu-id="47e9a-133">В отличие от **примера** инструкции, которой разрешено совместно использовать одно ВЫЧИСЛЕНие Лод в отметке 2x2, **пример \_ d** должен вычислять Лод полностью независимо друг от друга при использовании в шейдере пикселей.</span><span class="sxs-lookup"><span data-stu-id="47e9a-133">Unlike the **sample** instruction, which is permitted to share a single LOD calculation across a 2x2 stamp, **sample\_d** must calculate LOD completely independently, per-pixel when used in the Pixel Shader.</span></span>

<span data-ttu-id="47e9a-134">Если производные входные данные для **примера \_ d** поступили от производных инструкций по вычислению в шейдере пикселей, а значения включают INF/NaN, поведение **образца \_ d** может не соответствовать **образцу** инструкции, которая неявно вычисляет производную.</span><span class="sxs-lookup"><span data-stu-id="47e9a-134">If the derivative inputs to **sample\_d** came from derivative calculation instructions in the Pixel Shader and the values include INF/NaN, the behavior of **sample\_d** may not match the **sample** instruction, which implicitly computes the derivative.</span></span> <span data-ttu-id="47e9a-135">Значения INF/NaN могут повлиять на вычисление Лод по-разному.</span><span class="sxs-lookup"><span data-stu-id="47e9a-135">The INF/NaN values may affect the LOD calculation differently.</span></span>

<span data-ttu-id="47e9a-136">При попытке получить из входного слота, к которому не привязано ничего, возвращается значение 0 для всех компонентов.</span><span class="sxs-lookup"><span data-stu-id="47e9a-136">Fetching from an input slot that has nothing bound to it returns 0 for all components.</span></span>

### <a name="restrictions"></a><span data-ttu-id="47e9a-137">Ограничения</span><span class="sxs-lookup"><span data-stu-id="47e9a-137">Restrictions</span></span>

-   <span data-ttu-id="47e9a-138">**образец \_ d** наследует те же ограничения, что и **образец** инструкции, а также дополнительное ограничение для дополнительных параметров.</span><span class="sxs-lookup"><span data-stu-id="47e9a-138">**sample\_d** inherits the same restrictions as the **sample** instruction, plus additional an restriction below for its additional parameters.</span></span>
-   <span data-ttu-id="47e9a-139">*сркксдеривативес* и *срцидеривативес* должны быть временными (r \# /x \# ), константбуффер (CB \# ), входными (v \# ) или непосредственными значениями.</span><span class="sxs-lookup"><span data-stu-id="47e9a-139">*srcXDerivatives* and *srcYDerivatives* must be temp (r\#/x\#), constantBuffer (cb\#), input (v\#) registers or immediate value(s).</span></span>

<span data-ttu-id="47e9a-140">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="47e9a-140">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="47e9a-141">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="47e9a-141">Vertex Shader</span></span> | <span data-ttu-id="47e9a-142">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="47e9a-142">Geometry Shader</span></span> | <span data-ttu-id="47e9a-143">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="47e9a-143">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="47e9a-144">X</span><span class="sxs-lookup"><span data-stu-id="47e9a-144">X</span></span>             | <span data-ttu-id="47e9a-145">X</span><span class="sxs-lookup"><span data-stu-id="47e9a-145">X</span></span>               | <span data-ttu-id="47e9a-146">x</span><span class="sxs-lookup"><span data-stu-id="47e9a-146">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="47e9a-147">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="47e9a-147">Minimum Shader Model</span></span>

<span data-ttu-id="47e9a-148">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="47e9a-148">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="47e9a-149">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="47e9a-149">Shader Model</span></span>                                              | <span data-ttu-id="47e9a-150">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="47e9a-150">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="47e9a-151">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="47e9a-151">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="47e9a-152">да</span><span class="sxs-lookup"><span data-stu-id="47e9a-152">yes</span></span>       |
| [<span data-ttu-id="47e9a-153">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="47e9a-153">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="47e9a-154">да</span><span class="sxs-lookup"><span data-stu-id="47e9a-154">yes</span></span>       |
| [<span data-ttu-id="47e9a-155">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="47e9a-155">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="47e9a-156">да</span><span class="sxs-lookup"><span data-stu-id="47e9a-156">yes</span></span>       |
| [<span data-ttu-id="47e9a-157">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="47e9a-157">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="47e9a-158">Нет</span><span class="sxs-lookup"><span data-stu-id="47e9a-158">no</span></span>        |
| [<span data-ttu-id="47e9a-159">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="47e9a-159">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="47e9a-160">Нет</span><span class="sxs-lookup"><span data-stu-id="47e9a-160">no</span></span>        |
| [<span data-ttu-id="47e9a-161">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="47e9a-161">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="47e9a-162">Нет</span><span class="sxs-lookup"><span data-stu-id="47e9a-162">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="47e9a-163">См. также</span><span class="sxs-lookup"><span data-stu-id="47e9a-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47e9a-164">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="47e9a-164">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





