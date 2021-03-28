---
title: UMAX (SM4-ASM)
description: Максимальное значение целого числа без знака на уровне компонента.
ms.assetid: 86BCF7A7-99CA-481B-82B4-E0BA30963344
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceb1fda620facce31132f56ed888d18022ca27ec
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412176"
---
# <a name="umax-sm4---asm"></a><span data-ttu-id="4d2b0-103">UMAX (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="4d2b0-103">umax (sm4 - asm)</span></span>

<span data-ttu-id="4d2b0-104">Максимальное значение целого числа без знака на уровне компонента.</span><span class="sxs-lookup"><span data-stu-id="4d2b0-104">Component-wise unsigned integer maximum.</span></span>



| <span data-ttu-id="4d2b0-105">Компания UMAX dest \[ . Mask \] , src0 \[ . свиззле \] , src1 \[ . свиззле \] ,</span><span class="sxs-lookup"><span data-stu-id="4d2b0-105">umax dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\],</span></span> |
|---------------------------------------------------------|



 



| <span data-ttu-id="4d2b0-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="4d2b0-106">Item</span></span>                                                            | <span data-ttu-id="4d2b0-107">Описание</span><span class="sxs-lookup"><span data-stu-id="4d2b0-107">Description</span></span>                                                                                                            |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d2b0-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="4d2b0-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="4d2b0-109">\[в \] адресе результата операции.</span><span class="sxs-lookup"><span data-stu-id="4d2b0-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="4d2b0-110">*конечный адрес*  =  *src0*  >  *src1* ?</span><span class="sxs-lookup"><span data-stu-id="4d2b0-110">*dest* = *src0* > *src1* ?</span></span> <span data-ttu-id="4d2b0-111">*src0* : *src1*</span><span class="sxs-lookup"><span data-stu-id="4d2b0-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="4d2b0-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="4d2b0-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="4d2b0-113">\[в \] значении, сравниваемом с *src1*.</span><span class="sxs-lookup"><span data-stu-id="4d2b0-113">\[in\] The value to compare to *src1*.</span></span><br/>                                                                      |
| <span data-ttu-id="4d2b0-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="4d2b0-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="4d2b0-115">\[в \] значении, сравниваемом с *src0*.</span><span class="sxs-lookup"><span data-stu-id="4d2b0-115">\[in\] The value to compare to *src0*.</span></span><br/>                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="4d2b0-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="4d2b0-116">Remarks</span></span>

<span data-ttu-id="4d2b0-117">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="4d2b0-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="4d2b0-118">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="4d2b0-118">Vertex Shader</span></span> | <span data-ttu-id="4d2b0-119">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="4d2b0-119">Geometry Shader</span></span> | <span data-ttu-id="4d2b0-120">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="4d2b0-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="4d2b0-121">x</span><span class="sxs-lookup"><span data-stu-id="4d2b0-121">x</span></span>             | <span data-ttu-id="4d2b0-122">x</span><span class="sxs-lookup"><span data-stu-id="4d2b0-122">x</span></span>               | <span data-ttu-id="4d2b0-123">x</span><span class="sxs-lookup"><span data-stu-id="4d2b0-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4d2b0-124">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="4d2b0-124">Minimum Shader Model</span></span>

<span data-ttu-id="4d2b0-125">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="4d2b0-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4d2b0-126">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="4d2b0-126">Shader Model</span></span>                                              | <span data-ttu-id="4d2b0-127">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="4d2b0-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="4d2b0-128">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="4d2b0-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="4d2b0-129">да</span><span class="sxs-lookup"><span data-stu-id="4d2b0-129">yes</span></span>       |
| [<span data-ttu-id="4d2b0-130">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="4d2b0-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="4d2b0-131">да</span><span class="sxs-lookup"><span data-stu-id="4d2b0-131">yes</span></span>       |
| [<span data-ttu-id="4d2b0-132">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="4d2b0-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4d2b0-133">да</span><span class="sxs-lookup"><span data-stu-id="4d2b0-133">yes</span></span>       |
| [<span data-ttu-id="4d2b0-134">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4d2b0-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4d2b0-135">Нет</span><span class="sxs-lookup"><span data-stu-id="4d2b0-135">no</span></span>        |
| [<span data-ttu-id="4d2b0-136">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4d2b0-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4d2b0-137">Нет</span><span class="sxs-lookup"><span data-stu-id="4d2b0-137">no</span></span>        |
| [<span data-ttu-id="4d2b0-138">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4d2b0-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4d2b0-139">Нет</span><span class="sxs-lookup"><span data-stu-id="4d2b0-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="4d2b0-140">См. также</span><span class="sxs-lookup"><span data-stu-id="4d2b0-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d2b0-141">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4d2b0-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





