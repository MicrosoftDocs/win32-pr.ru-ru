---
title: dcl_output_siv (SM4-ASM)
description: дкл \_ OUTPUT \_ Сив (SM4-ASM)
ms.assetid: 5a87a113-7413-48ef-9a6a-13eb185650be
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df57ea991b9177dc081443301e426560834df894
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996975"
---
# <a name="dcl_output_siv-sm4---asm"></a><span data-ttu-id="c1ff7-103">дкл \_ OUTPUT \_ Сив (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="c1ff7-103">dcl\_output\_siv (sm4 - asm)</span></span>

<span data-ttu-id="c1ff7-104">Объявляет выходной регистр, который содержит параметр [System-value](dx-graphics-hlsl-semantics.md) .</span><span class="sxs-lookup"><span data-stu-id="c1ff7-104">Declares an output register that contains a [system-value](dx-graphics-hlsl-semantics.md) parameter.</span></span>



| <span data-ttu-id="c1ff7-105">дкл \_ OUTPUT \_ Сив On \[ *. маскируетs* \] , *системвалуе*</span><span class="sxs-lookup"><span data-stu-id="c1ff7-105">dcl\_output\_siv oN\[*.masks*\], *systemValue*</span></span> |
|------------------------------------------------|



 



| <span data-ttu-id="c1ff7-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="c1ff7-106">Item</span></span>                                                                                                                               | <span data-ttu-id="c1ff7-107">Описание</span><span class="sxs-lookup"><span data-stu-id="c1ff7-107">Description</span></span>                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1ff7-108"><span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*</span><span class="sxs-lookup"><span data-stu-id="c1ff7-108"><span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*</span></span><br/>                                                     | <span data-ttu-id="c1ff7-109">\[в \] реестре выходных данных; *N* — это целое число, которое обозначает номер регистра.</span><span class="sxs-lookup"><span data-stu-id="c1ff7-109">\[in\] An output data register; *N* is an integer that denotes the register number.</span></span><br/>                                                      |
| <span data-ttu-id="c1ff7-110"><span id="_.mask_"></span><span id="_.MASK_"></span>*\[. Mask\]*</span><span class="sxs-lookup"><span data-stu-id="c1ff7-110"><span id="_.mask_"></span><span id="_.MASK_"></span>*\[.mask\]*</span></span><br/>                                                         | <span data-ttu-id="c1ff7-111">\[\]необязательно.</span><span class="sxs-lookup"><span data-stu-id="c1ff7-111">\[in\] Optional.</span></span> <span data-ttu-id="c1ff7-112">Маска компонента (. ксизв), указывающая, какие компоненты регистров следует использовать.</span><span class="sxs-lookup"><span data-stu-id="c1ff7-112">A component mask (.xyzw) that specifies which of the register components to use.</span></span><br/>                                        |
| <span data-ttu-id="c1ff7-113"><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span>*системвалуенаме*</span><span class="sxs-lookup"><span data-stu-id="c1ff7-113"><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span>*systemValueName*</span></span><br/> | <span data-ttu-id="c1ff7-114">\[в \] имени системного значения, которое является строкой (см. раздел [семантика системного значения](dx-graphics-hlsl-semantics.md)) без \_ префикса «ОКП».</span><span class="sxs-lookup"><span data-stu-id="c1ff7-114">\[in\] The system-value name which is a string (see [system-value semantics](dx-graphics-hlsl-semantics.md)) without the "SV\_" prefix.</span></span><br/> |



 

<span data-ttu-id="c1ff7-115">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="c1ff7-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c1ff7-116">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="c1ff7-116">Vertex Shader</span></span> | <span data-ttu-id="c1ff7-117">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="c1ff7-117">Geometry Shader</span></span> | <span data-ttu-id="c1ff7-118">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="c1ff7-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="c1ff7-119">x</span><span class="sxs-lookup"><span data-stu-id="c1ff7-119">x</span></span>             | <span data-ttu-id="c1ff7-120">x</span><span class="sxs-lookup"><span data-stu-id="c1ff7-120">x</span></span>               |              |



 

<span data-ttu-id="c1ff7-121">Эта инструкция включена для облегчения отладки шейдера в сборке; нельзя создать шейдер на языке ассемблера с использованием модели шейдеров 4.</span><span class="sxs-lookup"><span data-stu-id="c1ff7-121">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="c1ff7-122">Например, .</span><span class="sxs-lookup"><span data-stu-id="c1ff7-122">Example</span></span>

<span data-ttu-id="c1ff7-123">Вот несколько примеров.</span><span class="sxs-lookup"><span data-stu-id="c1ff7-123">Here are some examples.</span></span>


```
dcl_output o[0].y
dcl_output_siv o[0].w, clipDistance
dcl_output_siv o[0].z, cullDistance
```



## <a name="minimum-shader-model"></a><span data-ttu-id="c1ff7-124">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="c1ff7-124">Minimum Shader Model</span></span>

<span data-ttu-id="c1ff7-125">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="c1ff7-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c1ff7-126">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="c1ff7-126">Shader Model</span></span>                                              | <span data-ttu-id="c1ff7-127">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="c1ff7-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c1ff7-128">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="c1ff7-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c1ff7-129">да</span><span class="sxs-lookup"><span data-stu-id="c1ff7-129">yes</span></span>       |
| [<span data-ttu-id="c1ff7-130">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="c1ff7-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c1ff7-131">да</span><span class="sxs-lookup"><span data-stu-id="c1ff7-131">yes</span></span>       |
| [<span data-ttu-id="c1ff7-132">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="c1ff7-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c1ff7-133">да</span><span class="sxs-lookup"><span data-stu-id="c1ff7-133">yes</span></span>       |
| [<span data-ttu-id="c1ff7-134">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c1ff7-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c1ff7-135">Нет</span><span class="sxs-lookup"><span data-stu-id="c1ff7-135">no</span></span>        |
| [<span data-ttu-id="c1ff7-136">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c1ff7-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c1ff7-137">Нет</span><span class="sxs-lookup"><span data-stu-id="c1ff7-137">no</span></span>        |
| [<span data-ttu-id="c1ff7-138">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c1ff7-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c1ff7-139">Нет</span><span class="sxs-lookup"><span data-stu-id="c1ff7-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c1ff7-140">См. также</span><span class="sxs-lookup"><span data-stu-id="c1ff7-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1ff7-141">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c1ff7-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





