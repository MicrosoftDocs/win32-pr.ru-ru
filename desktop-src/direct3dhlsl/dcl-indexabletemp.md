---
title: dcl_indexableTemp (SM4-ASM)
description: дкл \_ индексаблетемп (SM4-ASM)
ms.assetid: 32d8e7ce-4b28-48c3-b794-56ace96394f0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1ec3ef1222cd3bf73b4ea3f9ac6e2c3e706aa18e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996987"
---
# <a name="dcl_indexabletemp-sm4---asm"></a><span data-ttu-id="56f17-103">дкл \_ индексаблетемп (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="56f17-103">dcl\_indexableTemp (sm4 - asm)</span></span>

<span data-ttu-id="56f17-104">Объявляет индексируемый временный регистр.</span><span class="sxs-lookup"><span data-stu-id="56f17-104">Declares an indexable, temporary register.</span></span>



| <span data-ttu-id="56f17-105">дкл \_ индексаблетемп x *N \[ \] , компоненткаунт*</span><span class="sxs-lookup"><span data-stu-id="56f17-105">dcl\_indexableTemp x *N\[size\], ComponentCount*</span></span> |
|-------------------------------------------------|



 



| <span data-ttu-id="56f17-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="56f17-106">Item</span></span>                                                                                                                           | <span data-ttu-id="56f17-107">Описание</span><span class="sxs-lookup"><span data-stu-id="56f17-107">Description</span></span>                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="56f17-108"><span id="N"></span><span id="n"></span>*\N*</span><span class="sxs-lookup"><span data-stu-id="56f17-108"><span id="N"></span><span id="n"></span>*N*</span></span><br/>                                                                         | <span data-ttu-id="56f17-109">\[\]целое число, обозначающее номер регистра.</span><span class="sxs-lookup"><span data-stu-id="56f17-109">\[in\] An integer that denotes the register number.</span></span><br/>                              |
| <span data-ttu-id="56f17-110"><span id="_size_"></span><span id="_SIZE_"></span>*\[изменять\]*</span><span class="sxs-lookup"><span data-stu-id="56f17-110"><span id="_size_"></span><span id="_SIZE_"></span>*\[size\]*</span></span><br/>                                                        | <span data-ttu-id="56f17-111">\[в \] необязательном целочисленном значении.</span><span class="sxs-lookup"><span data-stu-id="56f17-111">\[in\] An optional integer value.</span></span> <span data-ttu-id="56f17-112">Число элементов в массиве регистров.</span><span class="sxs-lookup"><span data-stu-id="56f17-112">The number of elements in the register array.</span></span><br/>  |
| <span data-ttu-id="56f17-113"><span id="ComponentCount"></span><span id="componentcount"></span><span id="COMPONENTCOUNT"></span>*компоненткаунт*</span><span class="sxs-lookup"><span data-stu-id="56f17-113"><span id="ComponentCount"></span><span id="componentcount"></span><span id="COMPONENTCOUNT"></span>*ComponentCount*</span></span><br/> | <span data-ttu-id="56f17-114">\[в \] необязательном целочисленном значении. Число компонентов в массиве регистров.</span><span class="sxs-lookup"><span data-stu-id="56f17-114">\[in\] An optional integer value.The number of components in the register array.</span></span><br/> |



 

<span data-ttu-id="56f17-115">Регистр содержит достаточно места для 32-разрядного значения из четырех компонентов; число элементов в массиве временных регистров (индексируемое и [неиндексируемое](dcl-temps.md)) не может превышать 4096.</span><span class="sxs-lookup"><span data-stu-id="56f17-115">A register contains enough space for a 32-bit four-component value; the number of elements in the array of temporary registers (indexable and [non-indexable](dcl-temps.md)) cannot exceed 4096.</span></span>

<span data-ttu-id="56f17-116">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="56f17-116">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="56f17-117">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="56f17-117">Vertex Shader</span></span> | <span data-ttu-id="56f17-118">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="56f17-118">Geometry Shader</span></span> | <span data-ttu-id="56f17-119">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="56f17-119">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="56f17-120">x</span><span class="sxs-lookup"><span data-stu-id="56f17-120">x</span></span>             | <span data-ttu-id="56f17-121">x</span><span class="sxs-lookup"><span data-stu-id="56f17-121">x</span></span>               | <span data-ttu-id="56f17-122">x</span><span class="sxs-lookup"><span data-stu-id="56f17-122">x</span></span>            |



 

<span data-ttu-id="56f17-123">Эта инструкция включена для облегчения отладки шейдера в сборке; нельзя создать шейдер на языке ассемблера с использованием модели шейдеров 4.</span><span class="sxs-lookup"><span data-stu-id="56f17-123">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="56f17-124">Например, .</span><span class="sxs-lookup"><span data-stu-id="56f17-124">Example</span></span>

<span data-ttu-id="56f17-125">Ниже приведено несколько примеров кода, созданного для индексируемых регистров.</span><span class="sxs-lookup"><span data-stu-id="56f17-125">Here are some examples of the code generated for indexable registers.</span></span>


```
dcl_indexableTemp x0[23], 2 ; // An indexable array of 23, 2-component, 32-bit elements
dcl_indexableTemp x1[16], 4 ; // An indexable array of 16, 4-component, 32-bit elements
```



## <a name="minimum-shader-model"></a><span data-ttu-id="56f17-126">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="56f17-126">Minimum Shader Model</span></span>

<span data-ttu-id="56f17-127">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="56f17-127">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="56f17-128">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="56f17-128">Shader Model</span></span>                                              | <span data-ttu-id="56f17-129">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="56f17-129">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="56f17-130">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="56f17-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="56f17-131">да</span><span class="sxs-lookup"><span data-stu-id="56f17-131">yes</span></span>       |
| [<span data-ttu-id="56f17-132">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="56f17-132">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="56f17-133">да</span><span class="sxs-lookup"><span data-stu-id="56f17-133">yes</span></span>       |
| [<span data-ttu-id="56f17-134">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="56f17-134">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="56f17-135">да</span><span class="sxs-lookup"><span data-stu-id="56f17-135">yes</span></span>       |
| [<span data-ttu-id="56f17-136">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="56f17-136">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="56f17-137">Нет</span><span class="sxs-lookup"><span data-stu-id="56f17-137">no</span></span>        |
| [<span data-ttu-id="56f17-138">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="56f17-138">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="56f17-139">Нет</span><span class="sxs-lookup"><span data-stu-id="56f17-139">no</span></span>        |
| [<span data-ttu-id="56f17-140">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="56f17-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="56f17-141">Нет</span><span class="sxs-lookup"><span data-stu-id="56f17-141">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="56f17-142">См. также</span><span class="sxs-lookup"><span data-stu-id="56f17-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56f17-143">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="56f17-143">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





