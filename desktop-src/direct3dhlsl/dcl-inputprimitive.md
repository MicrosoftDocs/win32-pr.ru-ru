---
title: dcl_inputPrimitive (SM4-ASM)
description: дкл \_ инпутпримитиве (SM4-ASM)
ms.assetid: 86672fd3-7955-45ac-a8b2-a9cc8d1e8805
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 76c131b7c4225c0b30ad1183e4da1fe6c0561754
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103987091"
---
# <a name="dcl_inputprimitive-sm4---asm"></a><span data-ttu-id="8262f-103">дкл \_ инпутпримитиве (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="8262f-103">dcl\_inputPrimitive (sm4 - asm)</span></span>

<span data-ttu-id="8262f-104">Объявляет тип-примитив для входных данных шейдера Geometry.</span><span class="sxs-lookup"><span data-stu-id="8262f-104">Declares the primitive type for geometry-shader inputs.</span></span>



| <span data-ttu-id="8262f-105">\_ *тип* инпутпримитиве дкл</span><span class="sxs-lookup"><span data-stu-id="8262f-105">dcl\_inputPrimitive *type*</span></span> |
|----------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8262f-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="8262f-106">Item</span></span></th>
<th><span data-ttu-id="8262f-107">Описание</span><span class="sxs-lookup"><span data-stu-id="8262f-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8262f-108"><span id="type"></span><span id="TYPE"></span><em>Тип</em></span><span class="sxs-lookup"><span data-stu-id="8262f-108"><span id="type"></span><span id="TYPE"></span><em>type</em></span></span><br/></td>
<td><span data-ttu-id="8262f-109">окне Тип примитива input-Data, который является одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="8262f-109">[in] Input-data primitive type, which is one of the following:</span></span> <br/>
<ul>
<li><span data-ttu-id="8262f-110"><em>точка</em> - Список точек</span><span class="sxs-lookup"><span data-stu-id="8262f-110"><em>point</em> - point list</span></span></li>
<li><span data-ttu-id="8262f-111"><em>строка</em> - список строк</span><span class="sxs-lookup"><span data-stu-id="8262f-111"><em>line</em> - line list</span></span></li>
<li><span data-ttu-id="8262f-112"><em>треугольник</em> - список треугольников</span><span class="sxs-lookup"><span data-stu-id="8262f-112"><em>triangle</em> - triangle list</span></span></li>
<li><span data-ttu-id="8262f-113"><em>line_adj</em> - строковый список с соседями данных</span><span class="sxs-lookup"><span data-stu-id="8262f-113"><em>line_adj</em> - line list with adjacency data</span></span></li>
<li><span data-ttu-id="8262f-114"><em>triangle_adj</em> - список треугольников с смежными данными</span><span class="sxs-lookup"><span data-stu-id="8262f-114"><em>triangle_adj</em> - triangle list with adjacency data</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="8262f-115">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="8262f-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="8262f-116">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="8262f-116">Vertex Shader</span></span> | <span data-ttu-id="8262f-117">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="8262f-117">Geometry Shader</span></span> | <span data-ttu-id="8262f-118">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="8262f-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="8262f-119">x</span><span class="sxs-lookup"><span data-stu-id="8262f-119">x</span></span>               |              |



 

<span data-ttu-id="8262f-120">Эта инструкция включена для облегчения отладки шейдера в сборке; нельзя создать шейдер на языке ассемблера с использованием модели шейдеров 4.</span><span class="sxs-lookup"><span data-stu-id="8262f-120">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="8262f-121">Например, .</span><span class="sxs-lookup"><span data-stu-id="8262f-121">Example</span></span>

<span data-ttu-id="8262f-122">Ниже приведен пример.</span><span class="sxs-lookup"><span data-stu-id="8262f-122">Here is an example.</span></span>


```
dcl_inputPrimitive triangle
```



## <a name="minimum-shader-model"></a><span data-ttu-id="8262f-123">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="8262f-123">Minimum Shader Model</span></span>

<span data-ttu-id="8262f-124">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="8262f-124">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8262f-125">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="8262f-125">Shader Model</span></span>                                              | <span data-ttu-id="8262f-126">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="8262f-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="8262f-127">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="8262f-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="8262f-128">да</span><span class="sxs-lookup"><span data-stu-id="8262f-128">yes</span></span>       |
| [<span data-ttu-id="8262f-129">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="8262f-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="8262f-130">да</span><span class="sxs-lookup"><span data-stu-id="8262f-130">yes</span></span>       |
| [<span data-ttu-id="8262f-131">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="8262f-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8262f-132">да</span><span class="sxs-lookup"><span data-stu-id="8262f-132">yes</span></span>       |
| [<span data-ttu-id="8262f-133">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8262f-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8262f-134">Нет</span><span class="sxs-lookup"><span data-stu-id="8262f-134">no</span></span>        |
| [<span data-ttu-id="8262f-135">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8262f-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8262f-136">Нет</span><span class="sxs-lookup"><span data-stu-id="8262f-136">no</span></span>        |
| [<span data-ttu-id="8262f-137">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8262f-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8262f-138">Нет</span><span class="sxs-lookup"><span data-stu-id="8262f-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="8262f-139">См. также</span><span class="sxs-lookup"><span data-stu-id="8262f-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8262f-140">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8262f-140">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





