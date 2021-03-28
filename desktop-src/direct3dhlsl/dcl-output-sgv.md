---
title: dcl_output_sgv (SM4-ASM)
description: дкл \_ OUTPUT \_ СГВ (SM4-ASM)
ms.assetid: 0723541e-a97d-4b31-aaba-e7d1172137a6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7cfc5da7724a7e661f84ae5e7b293e5e84b61f15
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412237"
---
# <a name="dcl_output_sgv-sm4---asm"></a><span data-ttu-id="3cbfd-103">дкл \_ OUTPUT \_ СГВ (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="3cbfd-103">dcl\_output\_sgv (sm4 - asm)</span></span>

<span data-ttu-id="3cbfd-104">Объявляет выходной регистр, который содержит параметр [System-value](dx-graphics-hlsl-semantics.md) .</span><span class="sxs-lookup"><span data-stu-id="3cbfd-104">Declares an output register that contains a [system-value](dx-graphics-hlsl-semantics.md) parameter.</span></span>



| <span data-ttu-id="3cbfd-105">дкл \_ выходной \_ СГВ On *\[ . Mask \]*, *системвалуе*</span><span class="sxs-lookup"><span data-stu-id="3cbfd-105">dcl\_output\_sgv oN *\[.mask\]*, *systemValue*</span></span> |
|-----------------------------------------------|



 



| <span data-ttu-id="3cbfd-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="3cbfd-106">Item</span></span>                                                                                                                               | <span data-ttu-id="3cbfd-107">Описание</span><span class="sxs-lookup"><span data-stu-id="3cbfd-107">Description</span></span>                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cbfd-108"><span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*</span><span class="sxs-lookup"><span data-stu-id="3cbfd-108"><span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*</span></span><br/>                                                     | <span data-ttu-id="3cbfd-109">\[в \] реестре выходных данных; *N* — это целое число, которое обозначает номер регистра.</span><span class="sxs-lookup"><span data-stu-id="3cbfd-109">\[in\] An output data register; *N* is an integer that denotes the register number.</span></span><br/>                                                      |
| <span data-ttu-id="3cbfd-110"><span id="_.mask_"></span><span id="_.MASK_"></span>*\[. Mask\]*</span><span class="sxs-lookup"><span data-stu-id="3cbfd-110"><span id="_.mask_"></span><span id="_.MASK_"></span>*\[.mask\]*</span></span><br/>                                                         | <span data-ttu-id="3cbfd-111">\[\]необязательно.</span><span class="sxs-lookup"><span data-stu-id="3cbfd-111">\[in\] Optional.</span></span> <span data-ttu-id="3cbfd-112">Маска компонента (. ксизв), указывающая, какие компоненты регистров следует использовать.</span><span class="sxs-lookup"><span data-stu-id="3cbfd-112">A component mask (.xyzw) that specifies which of the register components to use.</span></span><br/>                                        |
| <span data-ttu-id="3cbfd-113"><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span>*системвалуенаме*</span><span class="sxs-lookup"><span data-stu-id="3cbfd-113"><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span>*systemValueName*</span></span><br/> | <span data-ttu-id="3cbfd-114">\[в \] имени системного значения, которое является строкой (см. раздел [семантика системного значения](dx-graphics-hlsl-semantics.md)) без \_ префикса «ОКП».</span><span class="sxs-lookup"><span data-stu-id="3cbfd-114">\[in\] The system-value name which is a string (see [system-value semantics](dx-graphics-hlsl-semantics.md)) without the "SV\_" prefix.</span></span><br/> |



 

<span data-ttu-id="3cbfd-115">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="3cbfd-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="3cbfd-116">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="3cbfd-116">Vertex Shader</span></span> | <span data-ttu-id="3cbfd-117">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="3cbfd-117">Geometry Shader</span></span> | <span data-ttu-id="3cbfd-118">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="3cbfd-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="3cbfd-119">x</span><span class="sxs-lookup"><span data-stu-id="3cbfd-119">x</span></span>               |              |



 

<span data-ttu-id="3cbfd-120">Эта инструкция включена для облегчения отладки шейдера в сборке; нельзя создать шейдер на языке ассемблера с использованием модели шейдеров 4.</span><span class="sxs-lookup"><span data-stu-id="3cbfd-120">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="3cbfd-121">Например, .</span><span class="sxs-lookup"><span data-stu-id="3cbfd-121">Example</span></span>

<span data-ttu-id="3cbfd-122">Ниже приведен пример.</span><span class="sxs-lookup"><span data-stu-id="3cbfd-122">Here is an example.</span></span>


```
dcl_output_sgv o4.x, primitiveID
```



## <a name="minimum-shader-model"></a><span data-ttu-id="3cbfd-123">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="3cbfd-123">Minimum Shader Model</span></span>

<span data-ttu-id="3cbfd-124">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="3cbfd-124">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3cbfd-125">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="3cbfd-125">Shader Model</span></span>                                              | <span data-ttu-id="3cbfd-126">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="3cbfd-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="3cbfd-127">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="3cbfd-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="3cbfd-128">да</span><span class="sxs-lookup"><span data-stu-id="3cbfd-128">yes</span></span>       |
| [<span data-ttu-id="3cbfd-129">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="3cbfd-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="3cbfd-130">да</span><span class="sxs-lookup"><span data-stu-id="3cbfd-130">yes</span></span>       |
| [<span data-ttu-id="3cbfd-131">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="3cbfd-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="3cbfd-132">да</span><span class="sxs-lookup"><span data-stu-id="3cbfd-132">yes</span></span>       |
| [<span data-ttu-id="3cbfd-133">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3cbfd-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="3cbfd-134">Нет</span><span class="sxs-lookup"><span data-stu-id="3cbfd-134">no</span></span>        |
| [<span data-ttu-id="3cbfd-135">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3cbfd-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="3cbfd-136">Нет</span><span class="sxs-lookup"><span data-stu-id="3cbfd-136">no</span></span>        |
| [<span data-ttu-id="3cbfd-137">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3cbfd-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="3cbfd-138">Нет</span><span class="sxs-lookup"><span data-stu-id="3cbfd-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="3cbfd-139">См. также</span><span class="sxs-lookup"><span data-stu-id="3cbfd-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3cbfd-140">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3cbfd-140">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





