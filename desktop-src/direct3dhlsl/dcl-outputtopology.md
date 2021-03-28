---
title: dcl_outputTopology (SM4-ASM)
description: дкл \_ аутпуттопологи (SM4-ASM)
ms.assetid: a03a6feb-ec34-4655-a68c-a91e31e7140b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e3b305d195ca09a1ef95c99624b47a50058021ca
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103785010"
---
# <a name="dcl_outputtopology-sm4---asm"></a><span data-ttu-id="45b30-103">дкл \_ аутпуттопологи (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="45b30-103">dcl\_outputTopology (sm4 - asm)</span></span>

<span data-ttu-id="45b30-104">Объявляет выходные данные Geometry-шейдеров примитивного типа.</span><span class="sxs-lookup"><span data-stu-id="45b30-104">Declares the primitive type geometry-shader output data.</span></span>



| <span data-ttu-id="45b30-105">\_ *тип* аутпуттопологи дкл</span><span class="sxs-lookup"><span data-stu-id="45b30-105">dcl\_outputTopology *Type*</span></span> |
|----------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="45b30-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="45b30-106">Item</span></span></th>
<th><span data-ttu-id="45b30-107">Описание</span><span class="sxs-lookup"><span data-stu-id="45b30-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="45b30-108"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Тип</em></span><span class="sxs-lookup"><span data-stu-id="45b30-108"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Type</em></span></span><br/></td>
<td><span data-ttu-id="45b30-109">окне Топология выходных примитивов, которая может иметь одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="45b30-109">[in] An output primitive topology, which is one of the following values:</span></span> <br/>
<ul>
<li><span data-ttu-id="45b30-110"><em>поинтлист</em></span><span class="sxs-lookup"><span data-stu-id="45b30-110"><em>pointlist</em></span></span></li>
<li><span data-ttu-id="45b30-111"><em>линестрип</em></span><span class="sxs-lookup"><span data-stu-id="45b30-111"><em>linestrip</em></span></span></li>
<li><span data-ttu-id="45b30-112"><em>трианглестрип</em></span><span class="sxs-lookup"><span data-stu-id="45b30-112"><em>trianglestrip</em></span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="45b30-113">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="45b30-113">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="45b30-114">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="45b30-114">Vertex Shader</span></span> | <span data-ttu-id="45b30-115">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="45b30-115">Geometry Shader</span></span> | <span data-ttu-id="45b30-116">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="45b30-116">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="45b30-117">x</span><span class="sxs-lookup"><span data-stu-id="45b30-117">x</span></span>               |              |



 

<span data-ttu-id="45b30-118">Эта инструкция включена для облегчения отладки шейдера в сборке; нельзя создать шейдер на языке ассемблера с использованием модели шейдеров 4.</span><span class="sxs-lookup"><span data-stu-id="45b30-118">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="45b30-119">Например, .</span><span class="sxs-lookup"><span data-stu-id="45b30-119">Example</span></span>

<span data-ttu-id="45b30-120">Ниже приведен пример.</span><span class="sxs-lookup"><span data-stu-id="45b30-120">Here is an example.</span></span>


```
dcl_outputTopology trianglestrip
```



## <a name="minimum-shader-model"></a><span data-ttu-id="45b30-121">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="45b30-121">Minimum Shader Model</span></span>

<span data-ttu-id="45b30-122">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="45b30-122">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="45b30-123">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="45b30-123">Shader Model</span></span>                                              | <span data-ttu-id="45b30-124">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="45b30-124">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="45b30-125">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="45b30-125">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="45b30-126">да</span><span class="sxs-lookup"><span data-stu-id="45b30-126">yes</span></span>       |
| [<span data-ttu-id="45b30-127">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="45b30-127">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="45b30-128">да</span><span class="sxs-lookup"><span data-stu-id="45b30-128">yes</span></span>       |
| [<span data-ttu-id="45b30-129">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="45b30-129">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="45b30-130">да</span><span class="sxs-lookup"><span data-stu-id="45b30-130">yes</span></span>       |
| [<span data-ttu-id="45b30-131">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="45b30-131">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="45b30-132">Нет</span><span class="sxs-lookup"><span data-stu-id="45b30-132">no</span></span>        |
| [<span data-ttu-id="45b30-133">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="45b30-133">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="45b30-134">Нет</span><span class="sxs-lookup"><span data-stu-id="45b30-134">no</span></span>        |
| [<span data-ttu-id="45b30-135">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="45b30-135">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="45b30-136">Нет</span><span class="sxs-lookup"><span data-stu-id="45b30-136">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="45b30-137">См. также</span><span class="sxs-lookup"><span data-stu-id="45b30-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45b30-138">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="45b30-138">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





