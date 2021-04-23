---
title: dcl_indexRange (SM4-ASM)
description: дкл \_ индексранже (SM4-ASM)
ms.assetid: 88af30f3-dbf9-4556-b170-a7371680f9b9
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5b0e2c250afd4ce52729a4c4bffeee0f33e4be6b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983909"
---
# <a name="dcl_indexrange-sm4---asm"></a><span data-ttu-id="74dc6-103">дкл \_ индексранже (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="74dc6-103">dcl\_indexRange (sm4 - asm)</span></span>

<span data-ttu-id="74dc6-104">Объявляет диапазон регистров, доступ к которым будет осуществляться по индексу (целочисленное значение, вычисленное в шейдере).</span><span class="sxs-lookup"><span data-stu-id="74dc6-104">Declares a range of registers that will be accessed by index (an integer computed in the shader).</span></span>



| <span data-ttu-id="74dc6-105">дкл \_ Индексранже *минрегистерм*, *максрегистерн*</span><span class="sxs-lookup"><span data-stu-id="74dc6-105">dcl\_indexRange *minRegisterM*, *maxRegisterN*</span></span> |
|------------------------------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="74dc6-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="74dc6-106">Item</span></span></th>
<th><span data-ttu-id="74dc6-107">Описание</span><span class="sxs-lookup"><span data-stu-id="74dc6-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="74dc6-108"><span id="minRegisterM"></span><span id="minregisterm"></span><span id="MINREGISTERM"></span><em>минрегистерм</em></span><span class="sxs-lookup"><span data-stu-id="74dc6-108"><span id="minRegisterM"></span><span id="minregisterm"></span><span id="MINREGISTERM"></span><em>minRegisterM</em></span></span><br/></td>
<td><span data-ttu-id="74dc6-109">окне Первый регистр для доступа по индексу.</span><span class="sxs-lookup"><span data-stu-id="74dc6-109">[in] The first register to access by index.</span></span> <br/>
<ul>
<li><span data-ttu-id="74dc6-110"><em>минрегистер</em> имеет значение <strong>v</strong> для входного регистра вершинного или построителя текстуры или <strong>o</strong> для выходного регистра вершинного шейдера.</span><span class="sxs-lookup"><span data-stu-id="74dc6-110"><em>minRegister</em> is either <strong>v</strong> for a vertex or pixel shader input register, or <strong>o</strong> for a vertex shader output register.</span></span></li>
<li><span data-ttu-id="74dc6-111"><em>M</em> — это целое число, которое обозначает номер регистра.</span><span class="sxs-lookup"><span data-stu-id="74dc6-111"><em>M</em> is an integer that denotes the register number.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74dc6-112"><span id="maxRegisterN"></span><span id="maxregistern"></span><span id="MAXREGISTERN"></span><em>максрегистерн</em></span><span class="sxs-lookup"><span data-stu-id="74dc6-112"><span id="maxRegisterN"></span><span id="maxregistern"></span><span id="MAXREGISTERN"></span><em>maxRegisterN</em></span></span><br/></td>
<td><span data-ttu-id="74dc6-113">окне Последняя регистрация для доступа по индексу.</span><span class="sxs-lookup"><span data-stu-id="74dc6-113">[in] The last register to access by index.</span></span> <span data-ttu-id="74dc6-114">Используется та же форма, что и <em>минрегистер</em> , за исключением <em>N</em> — номер регистра.</span><span class="sxs-lookup"><span data-stu-id="74dc6-114">Same form as <em>minRegister</em> except <em>N</em> is the register number.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="74dc6-115">На все регистры распространяются следующие ограничения.</span><span class="sxs-lookup"><span data-stu-id="74dc6-115">The following restrictions apply to all registers:</span></span>

-   <span data-ttu-id="74dc6-116">Регистры min и Max должны быть одного типа и иметь одинаковые маски компонентов (при объявлении масок).</span><span class="sxs-lookup"><span data-stu-id="74dc6-116">The min and max registers must be the same type and have the same component masks (if masks are declared).</span></span>
-   <span data-ttu-id="74dc6-117">Регистр может иметь несколько диапазонов индекса, если они не перекрываются.</span><span class="sxs-lookup"><span data-stu-id="74dc6-117">A register may have multiple index ranges, as long as they do no not overlap.</span></span>
-   <span data-ttu-id="74dc6-118">Минимальное число регистров должно быть меньше максимального.</span><span class="sxs-lookup"><span data-stu-id="74dc6-118">The min register number must be less than the max register number.</span></span>
-   <span data-ttu-id="74dc6-119">Регистр индекса не может содержать [системное значение](dx-graphics-hlsl-semantics.md).</span><span class="sxs-lookup"><span data-stu-id="74dc6-119">An index register cannot contain a [system-value](dx-graphics-hlsl-semantics.md).</span></span>
-   <span data-ttu-id="74dc6-120">Индексирование регистра за пределами определения максимального индекса приводит к неопределенным результатам.</span><span class="sxs-lookup"><span data-stu-id="74dc6-120">Indexing a register outside of the max index declaration produces undefined results.</span></span>

<span data-ttu-id="74dc6-121">Входные регистры шейдера пикселей должны использовать один и тот же режим интерполяции. выходные регистры шейдера пикселей не индексируются.</span><span class="sxs-lookup"><span data-stu-id="74dc6-121">Pixel shader input registers must use the same interpolation mode; pixel shader output registers are not indexable.</span></span>

<span data-ttu-id="74dc6-122">Входной регистр шейдера geometry имеет два измерения (ось вершин, ось атрибутов); диапазон индексов применяется только к оси атрибутов, так как ось вершин всегда полностью индексируется.</span><span class="sxs-lookup"><span data-stu-id="74dc6-122">A geometry shader input register has two dimensions (vertex axis, attribute axis); the index range applies only to the attribute axis because the vertex axis is always fully indexable.</span></span>

<span data-ttu-id="74dc6-123">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="74dc6-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="74dc6-124">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="74dc6-124">Vertex Shader</span></span> | <span data-ttu-id="74dc6-125">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="74dc6-125">Geometry Shader</span></span> | <span data-ttu-id="74dc6-126">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="74dc6-126">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="74dc6-127">x</span><span class="sxs-lookup"><span data-stu-id="74dc6-127">x</span></span>             | <span data-ttu-id="74dc6-128">x</span><span class="sxs-lookup"><span data-stu-id="74dc6-128">x</span></span>               | <span data-ttu-id="74dc6-129">x</span><span class="sxs-lookup"><span data-stu-id="74dc6-129">x</span></span>            |



 

<span data-ttu-id="74dc6-130">Эта инструкция включена для облегчения отладки шейдера в сборке; нельзя создать шейдер на языке ассемблера с использованием модели шейдеров 4.</span><span class="sxs-lookup"><span data-stu-id="74dc6-130">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="74dc6-131">Например, .</span><span class="sxs-lookup"><span data-stu-id="74dc6-131">Example</span></span>

<span data-ttu-id="74dc6-132">Ниже приведен пример.</span><span class="sxs-lookup"><span data-stu-id="74dc6-132">Here is an example.</span></span>


```
dcl_indexRange v1, v3
dcl_indexRange v4, v9
```



## <a name="minimum-shader-model"></a><span data-ttu-id="74dc6-133">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="74dc6-133">Minimum Shader Model</span></span>

<span data-ttu-id="74dc6-134">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="74dc6-134">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="74dc6-135">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="74dc6-135">Shader Model</span></span>                                              | <span data-ttu-id="74dc6-136">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="74dc6-136">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="74dc6-137">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="74dc6-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="74dc6-138">да</span><span class="sxs-lookup"><span data-stu-id="74dc6-138">yes</span></span>       |
| [<span data-ttu-id="74dc6-139">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="74dc6-139">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="74dc6-140">да</span><span class="sxs-lookup"><span data-stu-id="74dc6-140">yes</span></span>       |
| [<span data-ttu-id="74dc6-141">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="74dc6-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="74dc6-142">да</span><span class="sxs-lookup"><span data-stu-id="74dc6-142">yes</span></span>       |
| [<span data-ttu-id="74dc6-143">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="74dc6-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="74dc6-144">Нет</span><span class="sxs-lookup"><span data-stu-id="74dc6-144">no</span></span>        |
| [<span data-ttu-id="74dc6-145">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="74dc6-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="74dc6-146">Нет</span><span class="sxs-lookup"><span data-stu-id="74dc6-146">no</span></span>        |
| [<span data-ttu-id="74dc6-147">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="74dc6-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="74dc6-148">Нет</span><span class="sxs-lookup"><span data-stu-id="74dc6-148">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="74dc6-149">См. также</span><span class="sxs-lookup"><span data-stu-id="74dc6-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74dc6-150">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="74dc6-150">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





