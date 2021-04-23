---
title: Имакс (SM4-ASM)
description: Максимальное число компонентов на уровне компонента.
ms.assetid: 005468AA-577E-441F-ACD5-37A691E62CDD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc1bc6311573b1e7b39fbeaa93904203e7aae2ae
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104133298"
---
# <a name="imax-sm4---asm"></a><span data-ttu-id="7809e-103">Имакс (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="7809e-103">imax (sm4 - asm)</span></span>

<span data-ttu-id="7809e-104">Максимальное число компонентов на уровне компонента.</span><span class="sxs-lookup"><span data-stu-id="7809e-104">Component-wise integer maximum.</span></span>



| <span data-ttu-id="7809e-105">Имакс dest \[ . Mask \] , \[  - \] src0 \[ . свиззле \] , \[ - \] src1 \[ . свиззле \] ,</span><span class="sxs-lookup"><span data-stu-id="7809e-105">imax dest\[.mask\], \[ -\]src0\[.swizzle\], \[-\]src1\[.swizzle\],</span></span> |
|--------------------------------------------------------------------|



 



| <span data-ttu-id="7809e-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="7809e-106">Item</span></span>                                                            | <span data-ttu-id="7809e-107">Описание</span><span class="sxs-lookup"><span data-stu-id="7809e-107">Description</span></span>                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7809e-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="7809e-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="7809e-109">\[в \] результате операции.</span><span class="sxs-lookup"><span data-stu-id="7809e-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="7809e-110">*конечный адрес*  =  *src0*  >  *src1* ?</span><span class="sxs-lookup"><span data-stu-id="7809e-110">*dest* = *src0* > *src1* ?</span></span> <span data-ttu-id="7809e-111">*src0* : *src1*</span><span class="sxs-lookup"><span data-stu-id="7809e-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="7809e-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="7809e-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="7809e-113">\[в \] значении, сравниваемом с *src1*.</span><span class="sxs-lookup"><span data-stu-id="7809e-113">\[in\] The value to compare to *src1*.</span></span><br/>                                                       |
| <span data-ttu-id="7809e-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="7809e-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="7809e-115">\[в \] значении, сравниваемом с *src0*.</span><span class="sxs-lookup"><span data-stu-id="7809e-115">\[in\] The value to compare to *src0*.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="7809e-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="7809e-116">Remarks</span></span>

<span data-ttu-id="7809e-117">Необязательный модификатор отрицания в исходных операндах перед выполнением операции принимает 2 дополнения.</span><span class="sxs-lookup"><span data-stu-id="7809e-117">Optional negate modifier on source operands takes 2's complement before performing operation.</span></span>

<span data-ttu-id="7809e-118">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="7809e-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="7809e-119">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="7809e-119">Vertex Shader</span></span> | <span data-ttu-id="7809e-120">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="7809e-120">Geometry Shader</span></span> | <span data-ttu-id="7809e-121">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="7809e-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="7809e-122">x</span><span class="sxs-lookup"><span data-stu-id="7809e-122">x</span></span>             | <span data-ttu-id="7809e-123">x</span><span class="sxs-lookup"><span data-stu-id="7809e-123">x</span></span>               | <span data-ttu-id="7809e-124">x</span><span class="sxs-lookup"><span data-stu-id="7809e-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7809e-125">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="7809e-125">Minimum Shader Model</span></span>

<span data-ttu-id="7809e-126">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="7809e-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="7809e-127">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="7809e-127">Shader Model</span></span>                                              | <span data-ttu-id="7809e-128">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="7809e-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="7809e-129">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="7809e-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="7809e-130">да</span><span class="sxs-lookup"><span data-stu-id="7809e-130">yes</span></span>       |
| [<span data-ttu-id="7809e-131">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="7809e-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="7809e-132">да</span><span class="sxs-lookup"><span data-stu-id="7809e-132">yes</span></span>       |
| [<span data-ttu-id="7809e-133">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="7809e-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="7809e-134">да</span><span class="sxs-lookup"><span data-stu-id="7809e-134">yes</span></span>       |
| [<span data-ttu-id="7809e-135">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7809e-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="7809e-136">Нет</span><span class="sxs-lookup"><span data-stu-id="7809e-136">no</span></span>        |
| [<span data-ttu-id="7809e-137">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7809e-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="7809e-138">Нет</span><span class="sxs-lookup"><span data-stu-id="7809e-138">no</span></span>        |
| [<span data-ttu-id="7809e-139">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7809e-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="7809e-140">Нет</span><span class="sxs-lookup"><span data-stu-id="7809e-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="7809e-141">См. также</span><span class="sxs-lookup"><span data-stu-id="7809e-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7809e-142">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7809e-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





