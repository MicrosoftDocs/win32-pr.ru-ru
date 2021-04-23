---
title: dcl_output (SM4-ASM)
description: '\_выходные данные дкл (SM4-ASM)'
ms.assetid: 47e707ad-3ca4-477e-9eb8-3ec462abe864
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4391a30e172ef28133b8fe09a99bae7f77c971af
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983905"
---
# <a name="dcl_output-sm4---asm"></a><span data-ttu-id="4d956-103">\_выходные данные дкл (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="4d956-103">dcl\_output (sm4 - asm)</span></span>

<span data-ttu-id="4d956-104">Объявляет регистр вывода шейдера.</span><span class="sxs-lookup"><span data-stu-id="4d956-104">Declares a shader-output register.</span></span>



| <span data-ttu-id="4d956-105">дкл \_ выходные данные o *N \[ . \] Mask*</span><span class="sxs-lookup"><span data-stu-id="4d956-105">dcl\_output o *N\[.mask\]*</span></span> |
|---------------------------|



 



| <span data-ttu-id="4d956-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="4d956-106">Item</span></span>                                                                           | <span data-ttu-id="4d956-107">Описание</span><span class="sxs-lookup"><span data-stu-id="4d956-107">Description</span></span>                                                                                                  |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d956-108"><span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*</span><span class="sxs-lookup"><span data-stu-id="4d956-108"><span id="oN"></span><span id="on"></span><span id="ON"></span>o *N*</span></span><br/> | <span data-ttu-id="4d956-109">\[в \] реестре выходных данных; *N* — это целое число, которое обозначает номер регистра.</span><span class="sxs-lookup"><span data-stu-id="4d956-109">\[in\] An output data register; *N* is an integer that denotes the register number.</span></span><br/>               |
| <span data-ttu-id="4d956-110"><span id="_.mask_"></span><span id="_.MASK_"></span>*\[. Mask\]*</span><span class="sxs-lookup"><span data-stu-id="4d956-110"><span id="_.mask_"></span><span id="_.MASK_"></span>*\[.mask\]*</span></span><br/>     | <span data-ttu-id="4d956-111">\[\]необязательно.</span><span class="sxs-lookup"><span data-stu-id="4d956-111">\[in\] Optional.</span></span> <span data-ttu-id="4d956-112">Маска компонента (. ксизв), указывающая, какие компоненты регистров следует использовать.</span><span class="sxs-lookup"><span data-stu-id="4d956-112">A component mask (.xyzw) that specifies which of the register components to use.</span></span><br/> |



 

<span data-ttu-id="4d956-113">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="4d956-113">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="4d956-114">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="4d956-114">Vertex Shader</span></span> | <span data-ttu-id="4d956-115">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="4d956-115">Geometry Shader</span></span> | <span data-ttu-id="4d956-116">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="4d956-116">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="4d956-117">x</span><span class="sxs-lookup"><span data-stu-id="4d956-117">x</span></span>             | <span data-ttu-id="4d956-118">x</span><span class="sxs-lookup"><span data-stu-id="4d956-118">x</span></span>               | <span data-ttu-id="4d956-119">x</span><span class="sxs-lookup"><span data-stu-id="4d956-119">x</span></span>            |



 

<span data-ttu-id="4d956-120">Эта инструкция включена для облегчения отладки шейдера в сборке; нельзя создать шейдер на языке ассемблера с использованием модели шейдеров 4.</span><span class="sxs-lookup"><span data-stu-id="4d956-120">This instruction is included to aid in debugging a shader in assembly; you cannot author a shader in assembly language using Shader Model 4.</span></span>

## <a name="example"></a><span data-ttu-id="4d956-121">Например, .</span><span class="sxs-lookup"><span data-stu-id="4d956-121">Example</span></span>

<span data-ttu-id="4d956-122">Вот несколько примеров.</span><span class="sxs-lookup"><span data-stu-id="4d956-122">Here are some examples.</span></span>


```
dcl_output o0.xyz
dcl_output o1
dcl_output o2.xw
```



## <a name="minimum-shader-model"></a><span data-ttu-id="4d956-123">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="4d956-123">Minimum Shader Model</span></span>

<span data-ttu-id="4d956-124">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="4d956-124">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4d956-125">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="4d956-125">Shader Model</span></span>                                              | <span data-ttu-id="4d956-126">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="4d956-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="4d956-127">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="4d956-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="4d956-128">да</span><span class="sxs-lookup"><span data-stu-id="4d956-128">yes</span></span>       |
| [<span data-ttu-id="4d956-129">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="4d956-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="4d956-130">да</span><span class="sxs-lookup"><span data-stu-id="4d956-130">yes</span></span>       |
| [<span data-ttu-id="4d956-131">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="4d956-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4d956-132">да</span><span class="sxs-lookup"><span data-stu-id="4d956-132">yes</span></span>       |
| [<span data-ttu-id="4d956-133">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4d956-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4d956-134">Нет</span><span class="sxs-lookup"><span data-stu-id="4d956-134">no</span></span>        |
| [<span data-ttu-id="4d956-135">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4d956-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4d956-136">Нет</span><span class="sxs-lookup"><span data-stu-id="4d956-136">no</span></span>        |
| [<span data-ttu-id="4d956-137">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4d956-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4d956-138">Нет</span><span class="sxs-lookup"><span data-stu-id="4d956-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="4d956-139">См. также</span><span class="sxs-lookup"><span data-stu-id="4d956-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d956-140">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4d956-140">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





