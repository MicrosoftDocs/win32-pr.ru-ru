---
title: dcl_input (SM4-ASM)
description: '\_входные данные дкл (SM4-ASM)'
ms.assetid: 13456f2a-ee6c-42da-a9fe-670ab0fcbddf
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 400a1d47b6e0f9d82ec662553c36629deb4b1f0b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996982"
---
# <a name="dcl_input-sm4---asm"></a><span data-ttu-id="15e27-103">\_входные данные дкл (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="15e27-103">dcl\_input (sm4 - asm)</span></span>

<span data-ttu-id="15e27-104">Объявляет входной регистр шейдера.</span><span class="sxs-lookup"><span data-stu-id="15e27-104">Declares a shader-input register.</span></span>



| <span data-ttu-id="15e27-105">дкл \_ Вход v *N \[ . Mask \] \[ , интерполатионмоде \]*</span><span class="sxs-lookup"><span data-stu-id="15e27-105">dcl\_input v *N\[.mask\]\[, interpolationMode\]*</span></span> |
|-------------------------------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="15e27-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="15e27-106">Item</span></span></th>
<th><span data-ttu-id="15e27-107">Описание</span><span class="sxs-lookup"><span data-stu-id="15e27-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="15e27-108"><span id="vN_.mask_"></span><span id="vn_.mask_"></span><span id="VN_.MASK_"></span>v<em>N [. Маска]</em></span><span class="sxs-lookup"><span data-stu-id="15e27-108"><span id="vN_.mask_"></span><span id="vn_.mask_"></span><span id="VN_.MASK_"></span>v<em>N[.mask]</em></span></span><br/></td>
<td><span data-ttu-id="15e27-109">окне Регистр данных вершин.</span><span class="sxs-lookup"><span data-stu-id="15e27-109">[in] A vertex data register.</span></span> <br/>
<ul>
<li><span data-ttu-id="15e27-110"><em>N</em> — это целое число, определяющее номер регистра.</span><span class="sxs-lookup"><span data-stu-id="15e27-110"><em>N</em> is an integer that identifies the register number.</span></span></li>
<li><span data-ttu-id="15e27-111"><em>[. Mask]</em> — это необязательная маска компонента (. ксизв), указывающая, какие компоненты регистров следует использовать.</span><span class="sxs-lookup"><span data-stu-id="15e27-111"><em>[.mask]</em> is an optional component mask (.xyzw) that specifies which of the register components to use.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15e27-112"><span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>интерполатионмоде</em></span><span class="sxs-lookup"><span data-stu-id="15e27-112"><span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>interpolationMode</em></span></span><br/></td>
<td><span data-ttu-id="15e27-113">[в] Необязательно.</span><span class="sxs-lookup"><span data-stu-id="15e27-113">[in] Optional.</span></span> <span data-ttu-id="15e27-114">Режим интерполяции, который учитывается только в регистрах входных построителей текстуры.</span><span class="sxs-lookup"><span data-stu-id="15e27-114">The interpolation mode, which is only honored on pixel shader input registers.</span></span> <span data-ttu-id="15e27-115">Может иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="15e27-115">It can be one of the following values:</span></span> <br/>
<ul>
<li><span data-ttu-id="15e27-116">Константа — не выполнять интерполяцию между значениями регистров.</span><span class="sxs-lookup"><span data-stu-id="15e27-116">constant - do not interpolate between register values.</span></span></li>
<li><span data-ttu-id="15e27-117">линейная — линейная интерполяция между значениями регистра.</span><span class="sxs-lookup"><span data-stu-id="15e27-117">linear - interpolate linearly between register values.</span></span></li>
<li><span data-ttu-id="15e27-118">Линеарцентроид — то же, что и линейный, но центроид при множественной выборке.</span><span class="sxs-lookup"><span data-stu-id="15e27-118">linearCentroid - same as linear but centroid clamped when multisampling.</span></span></li>
<li><span data-ttu-id="15e27-119">Линеарноперспективе — то же, что и линейная, но без исправления перспективы.</span><span class="sxs-lookup"><span data-stu-id="15e27-119">linearNoperspective - same as linear but with no perspective correction.</span></span></li>
<li><span data-ttu-id="15e27-120">Линеарноперспективецентроид — то же, что и линейная, центроид при множественной выборке, без коррекции перспективы.</span><span class="sxs-lookup"><span data-stu-id="15e27-120">linearNoperspectiveCentroid - same as linear, centroid clamped when multisampling, no perspective correction.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="interpolation-notes"></a><span data-ttu-id="15e27-121">Примечания к интерполяции</span><span class="sxs-lookup"><span data-stu-id="15e27-121">Interpolation Notes</span></span>

<span data-ttu-id="15e27-122">По умолчанию при выполнении многовыборочного сглаживания атрибуты вершин интерполируются из пикселного центра.</span><span class="sxs-lookup"><span data-stu-id="15e27-122">By default, vertex attributes are interpolated from a pixel center when performing multisample antialiasing.</span></span> <span data-ttu-id="15e27-123">Если пиксельный центр не охватывается, то перед интерполяцией атрибут выравниваются по пикселному центру.</span><span class="sxs-lookup"><span data-stu-id="15e27-123">If a pixel center is not covered, an attribute is extrapolated to a pixel center before interpolation.</span></span>

<span data-ttu-id="15e27-124">Для пикселя, который не полностью покрывается, или атрибута, не охватывающего пиксельный центр, можно указать центроид выборку, которая вынуждает выборку будет выполняться где-то в охваченной области пикселя.</span><span class="sxs-lookup"><span data-stu-id="15e27-124">For a pixel that is not fully covered or an attribute that does not cover a pixel center, you can specify centroid sampling which forces sampling to occur somewhere within the covered area of the pixel.</span></span> <span data-ttu-id="15e27-125">Так как образец маски (если используется) применяется перед вычислением центроид, любое расположение выборки, маскированное с помощью образца маски, не может быть выбрано в качестве расположения центроид.</span><span class="sxs-lookup"><span data-stu-id="15e27-125">Because a sample mask (if used) is applied before the centroid is computed, any sample location masked out by the sample mask cannot be chosen as a centroid location.</span></span>

<span data-ttu-id="15e27-126">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="15e27-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="15e27-127">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="15e27-127">Vertex Shader</span></span> | <span data-ttu-id="15e27-128">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="15e27-128">Geometry Shader</span></span> | <span data-ttu-id="15e27-129">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="15e27-129">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="15e27-130">x</span><span class="sxs-lookup"><span data-stu-id="15e27-130">x</span></span>             | <span data-ttu-id="15e27-131">x</span><span class="sxs-lookup"><span data-stu-id="15e27-131">x</span></span>               | <span data-ttu-id="15e27-132">x</span><span class="sxs-lookup"><span data-stu-id="15e27-132">x</span></span>            |



 

<span data-ttu-id="15e27-133">Чтобы указать входные данные как системное значение, [Используйте \_ входной дкл \_ ОКП (SM4-ASM)](dcl-input-sv.md).</span><span class="sxs-lookup"><span data-stu-id="15e27-133">To identify the input as a system value, use [dcl\_input\_sv (sm4 - asm)](dcl-input-sv.md).</span></span>

<span data-ttu-id="15e27-134">Эта инструкция включена для облегчения отладки шейдера в сборке; нельзя создать шейдер на языке ассемблера с использованием модели шейдеров 4.</span><span class="sxs-lookup"><span data-stu-id="15e27-134">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="15e27-135">Например, .</span><span class="sxs-lookup"><span data-stu-id="15e27-135">Example</span></span>

<span data-ttu-id="15e27-136">Вот несколько примеров.</span><span class="sxs-lookup"><span data-stu-id="15e27-136">Here are some examples.</span></span>


```
dcl_input v3.xyz

dcl_input v0.x, linearCentroid
```



## <a name="minimum-shader-model"></a><span data-ttu-id="15e27-137">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="15e27-137">Minimum Shader Model</span></span>

<span data-ttu-id="15e27-138">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="15e27-138">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="15e27-139">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="15e27-139">Shader Model</span></span>                                              | <span data-ttu-id="15e27-140">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="15e27-140">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="15e27-141">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="15e27-141">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="15e27-142">да</span><span class="sxs-lookup"><span data-stu-id="15e27-142">yes</span></span>       |
| [<span data-ttu-id="15e27-143">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="15e27-143">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="15e27-144">да</span><span class="sxs-lookup"><span data-stu-id="15e27-144">yes</span></span>       |
| [<span data-ttu-id="15e27-145">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="15e27-145">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="15e27-146">да</span><span class="sxs-lookup"><span data-stu-id="15e27-146">yes</span></span>       |
| [<span data-ttu-id="15e27-147">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="15e27-147">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="15e27-148">Нет</span><span class="sxs-lookup"><span data-stu-id="15e27-148">no</span></span>        |
| [<span data-ttu-id="15e27-149">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="15e27-149">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="15e27-150">Нет</span><span class="sxs-lookup"><span data-stu-id="15e27-150">no</span></span>        |
| [<span data-ttu-id="15e27-151">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="15e27-151">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="15e27-152">Нет</span><span class="sxs-lookup"><span data-stu-id="15e27-152">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="15e27-153">См. также</span><span class="sxs-lookup"><span data-stu-id="15e27-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15e27-154">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="15e27-154">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





