---
title: dcl_constantBuffer (SM4-ASM)
description: дкл \_ константбуффер (SM4-ASM)
ms.assetid: 164fb2a4-8782-42f0-b4ba-1f87d9c7255d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b2eeb9368af0121ee61fde5d106eb0f3b08e5acb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104133326"
---
# <a name="dcl_constantbuffer-sm4---asm"></a><span data-ttu-id="0bd73-103">дкл \_ константбуффер (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="0bd73-103">dcl\_constantBuffer (sm4 - asm)</span></span>

<span data-ttu-id="0bd73-104">Объявляет константный буфер шейдера.</span><span class="sxs-lookup"><span data-stu-id="0bd73-104">Declares a shader constant buffer.</span></span>



| <span data-ttu-id="0bd73-105">дкл \_ константбуффер *КБН \[ size \]*, *акцесспаттерн*</span><span class="sxs-lookup"><span data-stu-id="0bd73-105">dcl\_constantBuffer *cbN\[size\]*, *AccessPattern*</span></span> |
|----------------------------------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0bd73-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="0bd73-106">Item</span></span></th>
<th><span data-ttu-id="0bd73-107">Описание</span><span class="sxs-lookup"><span data-stu-id="0bd73-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0bd73-108"><span id="cbN_size_"></span><span id="cbn_size_"></span><span id="CBN_SIZE_"></span>CB<em>N [размер]</em></span><span class="sxs-lookup"><span data-stu-id="0bd73-108"><span id="cbN_size_"></span><span id="cbn_size_"></span><span id="CBN_SIZE_"></span>cb<em>N[size]</em></span></span><br/></td>
<td><span data-ttu-id="0bd73-109">окне Буфер констант шейдера, где N — это целое число, которое обозначает номер регистра константы и размер — целое число, которое обозначает количество элементов в буфере.</span><span class="sxs-lookup"><span data-stu-id="0bd73-109">[in] A shader constant buffer where N is an integer that denotes the constant-buffer-register number and size is an integer that denotes the number of elements in the buffer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0bd73-110"><span id="AccessPattern"></span><span id="accesspattern"></span><span id="ACCESSPATTERN"></span><em>акцесспаттерн</em></span><span class="sxs-lookup"><span data-stu-id="0bd73-110"><span id="AccessPattern"></span><span id="accesspattern"></span><span id="ACCESSPATTERN"></span><em>AccessPattern</em></span></span><br/></td>
<td><span data-ttu-id="0bd73-111">окне Способ доступа к буферу по коду шейдера может быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="0bd73-111">[in] The way that the buffer will be accessed by shader code, which is one of the following:</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0bd73-112">Имя</span><span class="sxs-lookup"><span data-stu-id="0bd73-112">Name</span></span></th>
<th><span data-ttu-id="0bd73-113">Описание</span><span class="sxs-lookup"><span data-stu-id="0bd73-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0bd73-114">иммедиатеиндексед</span><span class="sxs-lookup"><span data-stu-id="0bd73-114">immediateIndexed</span></span></td>
<td><span data-ttu-id="0bd73-115">Индексировать буфер с литеральным значением.</span><span class="sxs-lookup"><span data-stu-id="0bd73-115">Index the buffer with a literal value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0bd73-116">dynamic_indexed</span><span class="sxs-lookup"><span data-stu-id="0bd73-116">dynamic_indexed</span></span></td>
<td><span data-ttu-id="0bd73-117">Индексировать буфер с результатом вычисленного выражения.</span><span class="sxs-lookup"><span data-stu-id="0bd73-117">Index the buffer with the result of an evaluated expression.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="0bd73-118">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="0bd73-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="0bd73-119">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="0bd73-119">Vertex Shader</span></span> | <span data-ttu-id="0bd73-120">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="0bd73-120">Geometry Shader</span></span> | <span data-ttu-id="0bd73-121">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="0bd73-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="0bd73-122">x</span><span class="sxs-lookup"><span data-stu-id="0bd73-122">x</span></span>             | <span data-ttu-id="0bd73-123">x</span><span class="sxs-lookup"><span data-stu-id="0bd73-123">x</span></span>               | <span data-ttu-id="0bd73-124">x</span><span class="sxs-lookup"><span data-stu-id="0bd73-124">x</span></span>            |



 

<span data-ttu-id="0bd73-125">Эта инструкция включена для облегчения отладки шейдера в сборке; нельзя создать шейдер на языке ассемблера с использованием модели шейдеров 4.</span><span class="sxs-lookup"><span data-stu-id="0bd73-125">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="0bd73-126">Например, .</span><span class="sxs-lookup"><span data-stu-id="0bd73-126">Example</span></span>

<span data-ttu-id="0bd73-127">В этом примере объявляется константный буфер для Register cB0, который содержит 19 элементов.</span><span class="sxs-lookup"><span data-stu-id="0bd73-127">This example declares a constant buffer for register cb0, which has 19 elements.</span></span> <span data-ttu-id="0bd73-128">Доступ к этим элементам осуществляется с помощью литерального индекса.</span><span class="sxs-lookup"><span data-stu-id="0bd73-128">These elements are accessed with a literal index.</span></span>


```
dcl_constantbuffer  cb0[19], immediateIndexed
```



## <a name="minimum-shader-model"></a><span data-ttu-id="0bd73-129">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="0bd73-129">Minimum Shader Model</span></span>

<span data-ttu-id="0bd73-130">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="0bd73-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0bd73-131">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="0bd73-131">Shader Model</span></span>                                              | <span data-ttu-id="0bd73-132">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="0bd73-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0bd73-133">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="0bd73-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="0bd73-134">да</span><span class="sxs-lookup"><span data-stu-id="0bd73-134">yes</span></span>       |
| [<span data-ttu-id="0bd73-135">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="0bd73-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="0bd73-136">да</span><span class="sxs-lookup"><span data-stu-id="0bd73-136">yes</span></span>       |
| [<span data-ttu-id="0bd73-137">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="0bd73-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0bd73-138">да</span><span class="sxs-lookup"><span data-stu-id="0bd73-138">yes</span></span>       |
| [<span data-ttu-id="0bd73-139">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0bd73-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0bd73-140">Нет</span><span class="sxs-lookup"><span data-stu-id="0bd73-140">no</span></span>        |
| [<span data-ttu-id="0bd73-141">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0bd73-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0bd73-142">Нет</span><span class="sxs-lookup"><span data-stu-id="0bd73-142">no</span></span>        |
| [<span data-ttu-id="0bd73-143">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0bd73-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0bd73-144">Нет</span><span class="sxs-lookup"><span data-stu-id="0bd73-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="0bd73-145">См. также</span><span class="sxs-lookup"><span data-stu-id="0bd73-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bd73-146">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0bd73-146">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





