---
title: dcl_input_sv (SM4-ASM)
description: дкл \_ входной \_ ОКП (SM4-ASM)
ms.assetid: 59270148-e2eb-4525-a888-ad7e843d62a5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 650196dff224259f48d1471f3005f95ec0de9c8b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103785022"
---
# <a name="dcl_input_sv-sm4---asm"></a><span data-ttu-id="bc176-103">дкл \_ входной \_ ОКП (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="bc176-103">dcl\_input\_sv (sm4 - asm)</span></span>

<span data-ttu-id="bc176-104">Объявляет входной регистр шейдера, который ждет, что [системное значение](dx-graphics-hlsl-semantics.md) должно быть предоставлено из предыдущего этапа.</span><span class="sxs-lookup"><span data-stu-id="bc176-104">Declares a shader-input register that expects a [system-value](dx-graphics-hlsl-semantics.md) to be provided from a preceding stage.</span></span>



| <span data-ttu-id="bc176-105">дкл \_ входной \_ ОКП v *N \[ . Mask \]*, *системвалуенаме \[ , интерполатионмоде \]*</span><span class="sxs-lookup"><span data-stu-id="bc176-105">dcl\_input\_sv v *N\[.mask\]*, *systemValueName\[, interpolationMode\]*</span></span> |
|------------------------------------------------------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bc176-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="bc176-106">Item</span></span></th>
<th><span data-ttu-id="bc176-107">Описание</span><span class="sxs-lookup"><span data-stu-id="bc176-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bc176-108"><span id="vN_.mask_"></span><span id="vn_.mask_"></span><span id="VN_.MASK_"></span>v<em>N [. Маска]</em></span><span class="sxs-lookup"><span data-stu-id="bc176-108"><span id="vN_.mask_"></span><span id="vn_.mask_"></span><span id="VN_.MASK_"></span>v<em>N[.mask]</em></span></span><br/></td>
<td><span data-ttu-id="bc176-109">окне Регистр данных вершин.</span><span class="sxs-lookup"><span data-stu-id="bc176-109">[in] A vertex data register.</span></span> <br/>
<ul>
<li><span data-ttu-id="bc176-110"><em>N</em> — это целое число, определяющее номер регистра.</span><span class="sxs-lookup"><span data-stu-id="bc176-110"><em>N</em> is an integer that identifies the register number.</span></span></li>
<li><span data-ttu-id="bc176-111"><em>[. Mask]</em> — это необязательная маска компонента (. ксизв), указывающая, какие компоненты регистров следует использовать.</span><span class="sxs-lookup"><span data-stu-id="bc176-111"><em>[.mask]</em> is an optional component mask (.xyzw) that specifies which of the register components to use.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bc176-112"><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span><em>системвалуенаме</em></span><span class="sxs-lookup"><span data-stu-id="bc176-112"><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span><em>systemValueName</em></span></span><br/></td>
<td><span data-ttu-id="bc176-113">окне Имя системного значения, являющееся строкой (см. раздел <a href="dx-graphics-hlsl-semantics.md">семантика системного значения</a>) без &quot; &quot; префикса SV_.</span><span class="sxs-lookup"><span data-stu-id="bc176-113">[in] The system-value name which is a string (see <a href="dx-graphics-hlsl-semantics.md">system-value semantics</a>) without the &quot;SV_&quot; prefix.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bc176-114"><span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>интерполатионмоде</em></span><span class="sxs-lookup"><span data-stu-id="bc176-114"><span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>interpolationMode</em></span></span><br/></td>
<td><span data-ttu-id="bc176-115">[в] Необязательно.</span><span class="sxs-lookup"><span data-stu-id="bc176-115">[in] Optional.</span></span> <span data-ttu-id="bc176-116">Режим интерполяции, который влияет на способ вычисления значений во время растрирования; режим используется только в шейдере пикселей.</span><span class="sxs-lookup"><span data-stu-id="bc176-116">The interpolation mode which affects how values are calculated during rasterization; the mode is only used by a pixel shader.</span></span> <span data-ttu-id="bc176-117">Может иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="bc176-117">It can be one of the following values:</span></span> <br/>
<ul>
<li><span data-ttu-id="bc176-118">Константа — не выполнять интерполяцию между значениями регистров.</span><span class="sxs-lookup"><span data-stu-id="bc176-118">constant - do not interpolate between register values.</span></span></li>
<li><span data-ttu-id="bc176-119">линейная — линейная интерполяция между значениями регистра.</span><span class="sxs-lookup"><span data-stu-id="bc176-119">linear - interpolate linearly between register values.</span></span></li>
<li><span data-ttu-id="bc176-120">Линеарцентроид — то же, что и линейный, но центроид при множественной выборке.</span><span class="sxs-lookup"><span data-stu-id="bc176-120">linearCentroid - same as linear but centroid clamped when multisampling.</span></span></li>
<li><span data-ttu-id="bc176-121">Линеарноперспективе — то же, что и линейная, но без исправления перспективы.</span><span class="sxs-lookup"><span data-stu-id="bc176-121">linearNoperspective - same as linear but with no perspective correction.</span></span></li>
<li><span data-ttu-id="bc176-122">Линеарноперспективецентроид — то же, что и линейная, но без изменений перспективы и центроид при множественной выборки.</span><span class="sxs-lookup"><span data-stu-id="bc176-122">linearNoperspectiveCentroid - same as linear but with no perspective correction and centroid clamped when multisampling.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="bc176-123">Маска компонента для объявления системного значения может быть любым подмножеством \[ ксизв \] ; объявления не могут перекрываться (каждое объявление должно следовать за последовательностью ксизв).</span><span class="sxs-lookup"><span data-stu-id="bc176-123">A component mask for a system-value declaration can be any appropriate subset of \[xyzw\]; declarations may not overlap (each declaration must follow the sequence xyzw).</span></span> <span data-ttu-id="bc176-124">При объявлении скалярных системных значений (например, расстояния обрезки и расстояния для отбора) можно объявить несколько системных значений в одном регистре.</span><span class="sxs-lookup"><span data-stu-id="bc176-124">When declaring scalar system values (clip distance and cull distance for example), you can declare multiple system values in a single register.</span></span> <span data-ttu-id="bc176-125">В этом случае убедитесь, что другие модификаторы, такие как режимы интерполяции, совпадают.</span><span class="sxs-lookup"><span data-stu-id="bc176-125">If you do so, make sure other modifiers like the interpolation modes match.</span></span>

<span data-ttu-id="bc176-126">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="bc176-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="bc176-127">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="bc176-127">Vertex Shader</span></span> | <span data-ttu-id="bc176-128">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="bc176-128">Geometry Shader</span></span> | <span data-ttu-id="bc176-129">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="bc176-129">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="bc176-130">x</span><span class="sxs-lookup"><span data-stu-id="bc176-130">x</span></span>             | <span data-ttu-id="bc176-131">x</span><span class="sxs-lookup"><span data-stu-id="bc176-131">x</span></span>               | <span data-ttu-id="bc176-132">x</span><span class="sxs-lookup"><span data-stu-id="bc176-132">x</span></span>            |



 

<span data-ttu-id="bc176-133">Эта инструкция включена для облегчения отладки шейдера в сборке; нельзя создать шейдер на языке ассемблера с использованием модели шейдеров 4.</span><span class="sxs-lookup"><span data-stu-id="bc176-133">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="bc176-134">Например, .</span><span class="sxs-lookup"><span data-stu-id="bc176-134">Example</span></span>

<span data-ttu-id="bc176-135">Ниже приводится несколько примеров.</span><span class="sxs-lookup"><span data-stu-id="bc176-135">Here are some examples:</span></span>


```
// valid
dcl_input v0.y, linear
dcl_input_sv v0.w, clipDistance
dcl_input_sv v0.z, cullDistance
```




```
// invalid declarations
dcl_input v0.y, linear
dcl_input_sv v0.x, clipDistance  // the y component was previously declared, this declaration must use 
                                 // either the z or w component

dcl_input v0.y, linearNoPerspective                  // the interpolation mode is linear-no-perspective
dcl_input_sv v0.z, renderTargetArrayIndex, constant  // the interpolation modes is constant
                                                     // the interpolation modes must match
```



## <a name="minimum-shader-model"></a><span data-ttu-id="bc176-136">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="bc176-136">Minimum Shader Model</span></span>

<span data-ttu-id="bc176-137">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="bc176-137">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="bc176-138">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="bc176-138">Shader Model</span></span>                                              | <span data-ttu-id="bc176-139">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="bc176-139">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="bc176-140">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="bc176-140">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="bc176-141">да</span><span class="sxs-lookup"><span data-stu-id="bc176-141">yes</span></span>       |
| [<span data-ttu-id="bc176-142">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="bc176-142">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="bc176-143">да</span><span class="sxs-lookup"><span data-stu-id="bc176-143">yes</span></span>       |
| [<span data-ttu-id="bc176-144">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="bc176-144">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="bc176-145">да</span><span class="sxs-lookup"><span data-stu-id="bc176-145">yes</span></span>       |
| [<span data-ttu-id="bc176-146">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bc176-146">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="bc176-147">Нет</span><span class="sxs-lookup"><span data-stu-id="bc176-147">no</span></span>        |
| [<span data-ttu-id="bc176-148">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bc176-148">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="bc176-149">Нет</span><span class="sxs-lookup"><span data-stu-id="bc176-149">no</span></span>        |
| [<span data-ttu-id="bc176-150">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bc176-150">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="bc176-151">Нет</span><span class="sxs-lookup"><span data-stu-id="bc176-151">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="bc176-152">См. также</span><span class="sxs-lookup"><span data-stu-id="bc176-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc176-153">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bc176-153">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





