---
title: dcl_sampler (SM4-ASM)
description: дклный \_ образец (SM4-ASM)
ms.assetid: 285a47fa-2d47-4ba9-90b9-3f4c61d5dce1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 45b6da3bcdb027a00edeb4f009773533424efeb8
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/08/2020
ms.locfileid: "104413932"
---
# <a name="dcl_sampler-sm4---asm"></a><span data-ttu-id="1aa27-103">дклный \_ образец (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="1aa27-103">dcl\_sampler (sm4 - asm)</span></span>

<span data-ttu-id="1aa27-104">Объявляет регистр образца.</span><span class="sxs-lookup"><span data-stu-id="1aa27-104">Declares a sampler register.</span></span>



| <span data-ttu-id="1aa27-105">дклный \_ образец, режим</span><span class="sxs-lookup"><span data-stu-id="1aa27-105">dcl\_sampler sN, mode</span></span> |
|-----------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1aa27-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="1aa27-106">Item</span></span></th>
<th><span data-ttu-id="1aa27-107">Описание</span><span class="sxs-lookup"><span data-stu-id="1aa27-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1aa27-108"><span id="sN"></span><span id="sn"></span><span id="SN"></span>с<em>N</em></span><span class="sxs-lookup"><span data-stu-id="1aa27-108"><span id="sN"></span><span id="sn"></span><span id="SN"></span>s<em>N</em></span></span><br/></td>
<td><span data-ttu-id="1aa27-109">окне Регистр образцов, где <em>N</em> — это целое число, которое обозначает номер регистра.</span><span class="sxs-lookup"><span data-stu-id="1aa27-109">[in] A sampler register, where <em>N</em> is an integer that denotes the register number.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1aa27-110"><span id="mode"></span><span id="MODE"></span><em>режима</em></span><span class="sxs-lookup"><span data-stu-id="1aa27-110"><span id="mode"></span><span id="MODE"></span><em>mode</em></span></span><br/></td>
<td><span data-ttu-id="1aa27-111">окне Режим выборки, который ограничивает количество состояний образца (перечисленных в элементах <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_sampler_desc"><strong>D3D10_SAMPLER_DESC</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="1aa27-111">[in] A sampler mode, which constrains which sampler states (listed in the members of <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_sampler_desc"><strong>D3D10_SAMPLER_DESC</strong></a>) are honored.</span></span> <span data-ttu-id="1aa27-112">Режимы и состояния перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="1aa27-112">The modes and states are listed in the following table.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1aa27-113">Режим</span><span class="sxs-lookup"><span data-stu-id="1aa27-113">Mode</span></span></th>
<th><span data-ttu-id="1aa27-114">Принятые состояния образца</span><span class="sxs-lookup"><span data-stu-id="1aa27-114">Sampler States Honored</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1aa27-115">default</span><span class="sxs-lookup"><span data-stu-id="1aa27-115">default</span></span></td>
<td><span data-ttu-id="1aa27-116"><em>Filter</em> (может не использовать значения _COMPARISON или _TEXT), <em>аддрессу/V/W</em>, <em>минлод/макслод</em>, <em>миплодбиас</em>, <em>максанисотропи</em>, <em>BorderColor [4]</em></span><span class="sxs-lookup"><span data-stu-id="1aa27-116"><em>Filter</em> (may not use the _COMPARISON or _TEXT values), <em>AddressU/V/W</em>, <em>MinLOD/MaxLOD</em>, <em>MipLODBias</em>, <em>MaxAnisotropy</em>, <em>BorderColor[4]</em></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1aa27-117">сравнение</span><span class="sxs-lookup"><span data-stu-id="1aa27-117">comparison</span></span></td>
<td><span data-ttu-id="1aa27-118"><em>Filter</em>, <em>компарисонфунктион</em>, <em>аддрессу/V/W</em>, <em>минлод, макслод</em>, <em>миплодбиас</em>, <em>максанисотропи</em>, <em>BorderColor [4]</em></span><span class="sxs-lookup"><span data-stu-id="1aa27-118"><em>Filter</em>, <em>ComparisonFunction</em>, <em>AddressU/V/W</em>, <em>MinLOD,MaxLOD</em>, <em>MipLODBias</em>, <em>MaxAnisotropy</em>, <em>BorderColor[4]</em></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1aa27-119">одним</span><span class="sxs-lookup"><span data-stu-id="1aa27-119">mono</span></span></td>
<td><span data-ttu-id="1aa27-120"><em>Фильтр</em> (должен быть одним из значений _TEXT), <em>монофилтервидс</em>, <em>монофилтерхеигхт</em> (эти два состояния имеют глобальное состояние устройства), <em>минлод</em>, <em>миплодбиас</em>, <em>максанисотропи</em></span><span class="sxs-lookup"><span data-stu-id="1aa27-120"><em>Filter</em> (must be one of the _TEXT values), <em>MonoFilterWidth</em>, <em>MonoFilterHeight</em> (these two states are global device state), <em>MinLOD</em>, <em>MipLODBias</em>, <em>MaxAnisotropy</em></span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="1aa27-121">Режим позволяет ограничивать примеры инструкций, которые можно использовать. в этой таблице перечислены методы объекта-текстуры, которые поддерживаются для каждого режима.</span><span class="sxs-lookup"><span data-stu-id="1aa27-121">The mode restricts the sample instructions that can be used; this table lists the texture-object methods that are supported for each mode.</span></span>



| <span data-ttu-id="1aa27-122">Образец работы с образцом в этом режиме</span><span class="sxs-lookup"><span data-stu-id="1aa27-122">A Sampler Operating in this Mode</span></span> | <span data-ttu-id="1aa27-123">Может использовать эти Texture-Object методы</span><span class="sxs-lookup"><span data-stu-id="1aa27-123">Can Use these Texture-Object Methods</span></span>                                                                                                           |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1aa27-124">default</span><span class="sxs-lookup"><span data-stu-id="1aa27-124">default</span></span>                          | <span data-ttu-id="1aa27-125">[Sample](dx-graphics-hlsl-to-sample.md), [самплелевел](dx-graphics-hlsl-to-samplelevel.md), [самплеград](dx-graphics-hlsl-to-samplegrad.md)</span><span class="sxs-lookup"><span data-stu-id="1aa27-125">[Sample](dx-graphics-hlsl-to-sample.md), [SampleLevel](dx-graphics-hlsl-to-samplelevel.md), [SampleGrad](dx-graphics-hlsl-to-samplegrad.md)</span></span> |
| <span data-ttu-id="1aa27-126">сравнение</span><span class="sxs-lookup"><span data-stu-id="1aa27-126">comparison</span></span>                       | <span data-ttu-id="1aa27-127">[Самплекмп](dx-graphics-hlsl-to-samplecmp.md), [самплекмплевелзеро](dx-graphics-hlsl-to-samplecmplevelzero.md)</span><span class="sxs-lookup"><span data-stu-id="1aa27-127">[SampleCmp](dx-graphics-hlsl-to-samplecmp.md), [SampleCmpLevelZero](dx-graphics-hlsl-to-samplecmplevelzero.md)</span></span>                               |
| <span data-ttu-id="1aa27-128">одним</span><span class="sxs-lookup"><span data-stu-id="1aa27-128">mono</span></span>                             | [<span data-ttu-id="1aa27-129">SampleLevel</span><span class="sxs-lookup"><span data-stu-id="1aa27-129">SampleLevel</span></span>](dx-graphics-hlsl-to-samplelevel.md)                                                                                             |



 

<span data-ttu-id="1aa27-130">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="1aa27-130">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="1aa27-131">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="1aa27-131">Vertex Shader</span></span> | <span data-ttu-id="1aa27-132">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="1aa27-132">Geometry Shader</span></span> | <span data-ttu-id="1aa27-133">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="1aa27-133">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="1aa27-134">x</span><span class="sxs-lookup"><span data-stu-id="1aa27-134">x</span></span>             | <span data-ttu-id="1aa27-135">x</span><span class="sxs-lookup"><span data-stu-id="1aa27-135">x</span></span>               | <span data-ttu-id="1aa27-136">x\*</span><span class="sxs-lookup"><span data-stu-id="1aa27-136">x\*</span></span>          |



 

<span data-ttu-id="1aa27-137">\* — Использование образца в режиме Mono поддерживается только в шейдере пикселей.</span><span class="sxs-lookup"><span data-stu-id="1aa27-137">\* - Using a sampler in mono mode is supported only in a pixel shader.</span></span>

<span data-ttu-id="1aa27-138">Эта инструкция включена для облегчения отладки шейдера в сборке; нельзя создать шейдер на языке ассемблера с использованием модели шейдеров 4.</span><span class="sxs-lookup"><span data-stu-id="1aa27-138">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="1aa27-139">Например, .</span><span class="sxs-lookup"><span data-stu-id="1aa27-139">Example</span></span>

<span data-ttu-id="1aa27-140">Ниже приведен пример.</span><span class="sxs-lookup"><span data-stu-id="1aa27-140">Here is an example.</span></span>


```
dcl_sampler s3, default
```



## <a name="minimum-shader-model"></a><span data-ttu-id="1aa27-141">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="1aa27-141">Minimum Shader Model</span></span>

<span data-ttu-id="1aa27-142">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="1aa27-142">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1aa27-143">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="1aa27-143">Shader Model</span></span>                                              | <span data-ttu-id="1aa27-144">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="1aa27-144">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1aa27-145">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="1aa27-145">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1aa27-146">да</span><span class="sxs-lookup"><span data-stu-id="1aa27-146">yes</span></span>       |
| [<span data-ttu-id="1aa27-147">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="1aa27-147">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1aa27-148">да</span><span class="sxs-lookup"><span data-stu-id="1aa27-148">yes</span></span>       |
| [<span data-ttu-id="1aa27-149">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="1aa27-149">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1aa27-150">да</span><span class="sxs-lookup"><span data-stu-id="1aa27-150">yes</span></span>       |
| [<span data-ttu-id="1aa27-151">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1aa27-151">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1aa27-152">Нет</span><span class="sxs-lookup"><span data-stu-id="1aa27-152">no</span></span>        |
| [<span data-ttu-id="1aa27-153">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1aa27-153">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1aa27-154">Нет</span><span class="sxs-lookup"><span data-stu-id="1aa27-154">no</span></span>        |
| [<span data-ttu-id="1aa27-155">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1aa27-155">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1aa27-156">Нет</span><span class="sxs-lookup"><span data-stu-id="1aa27-156">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1aa27-157">См. также</span><span class="sxs-lookup"><span data-stu-id="1aa27-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1aa27-158">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1aa27-158">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

