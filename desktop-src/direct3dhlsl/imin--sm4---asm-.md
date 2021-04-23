---
title: Имин (SM4-ASM)
description: Минимальное число компонентов на уровне компонента.
ms.assetid: 8EDD5503-76D5-4078-BFBA-1DA9260C6E68
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 942384e7a988e4919a483e09c75e476d5a6917ba
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412210"
---
# <a name="imin-sm4---asm"></a><span data-ttu-id="cea96-103">Имин (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="cea96-103">imin (sm4 - asm)</span></span>

<span data-ttu-id="cea96-104">Минимальное число компонентов на уровне компонента.</span><span class="sxs-lookup"><span data-stu-id="cea96-104">Component-wise integer minimum.</span></span>



| <span data-ttu-id="cea96-105">Имин dest \[ . Mask \] , \[  - \] src0 \[ . свиззле \] , \[ - \] src1 \[ . свиззле \] ,</span><span class="sxs-lookup"><span data-stu-id="cea96-105">imin dest\[.mask\], \[ -\]src0\[.swizzle\], \[-\]src1\[.swizzle\],</span></span> |
|--------------------------------------------------------------------|



 



| <span data-ttu-id="cea96-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="cea96-106">Item</span></span>                                                            | <span data-ttu-id="cea96-107">Описание</span><span class="sxs-lookup"><span data-stu-id="cea96-107">Description</span></span>                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cea96-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="cea96-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="cea96-109">\[в \] результате операции.</span><span class="sxs-lookup"><span data-stu-id="cea96-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="cea96-110">*конечный адрес*  =  *src0*  <  *src1* ?</span><span class="sxs-lookup"><span data-stu-id="cea96-110">*dest* = *src0* < *src1* ?</span></span> <span data-ttu-id="cea96-111">*src0* : *src1*</span><span class="sxs-lookup"><span data-stu-id="cea96-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="cea96-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="cea96-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="cea96-113">\[в \] значении, сравниваемом с *src1*.</span><span class="sxs-lookup"><span data-stu-id="cea96-113">\[in\] The value to compare to *src1*.</span></span><br/>                                                       |
| <span data-ttu-id="cea96-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="cea96-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="cea96-115">\[в \] значении, сравниваемом с *src0*.</span><span class="sxs-lookup"><span data-stu-id="cea96-115">\[in\] The value to compare to *src0*.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="cea96-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="cea96-116">Remarks</span></span>

<span data-ttu-id="cea96-117">Необязательный модификатор отрицания в исходных операндах перед выполнением операции принимает 2 дополнения.</span><span class="sxs-lookup"><span data-stu-id="cea96-117">Optional negate modifier on source operands takes 2's complement before performing operation.</span></span>

<span data-ttu-id="cea96-118">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="cea96-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="cea96-119">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="cea96-119">Vertex Shader</span></span> | <span data-ttu-id="cea96-120">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="cea96-120">Geometry Shader</span></span> | <span data-ttu-id="cea96-121">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="cea96-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="cea96-122">x</span><span class="sxs-lookup"><span data-stu-id="cea96-122">x</span></span>             | <span data-ttu-id="cea96-123">x</span><span class="sxs-lookup"><span data-stu-id="cea96-123">x</span></span>               | <span data-ttu-id="cea96-124">x</span><span class="sxs-lookup"><span data-stu-id="cea96-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="cea96-125">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="cea96-125">Minimum Shader Model</span></span>

<span data-ttu-id="cea96-126">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="cea96-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="cea96-127">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="cea96-127">Shader Model</span></span>                                              | <span data-ttu-id="cea96-128">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="cea96-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="cea96-129">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="cea96-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="cea96-130">да</span><span class="sxs-lookup"><span data-stu-id="cea96-130">yes</span></span>       |
| [<span data-ttu-id="cea96-131">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="cea96-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="cea96-132">да</span><span class="sxs-lookup"><span data-stu-id="cea96-132">yes</span></span>       |
| [<span data-ttu-id="cea96-133">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="cea96-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="cea96-134">да</span><span class="sxs-lookup"><span data-stu-id="cea96-134">yes</span></span>       |
| [<span data-ttu-id="cea96-135">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cea96-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="cea96-136">Нет</span><span class="sxs-lookup"><span data-stu-id="cea96-136">no</span></span>        |
| [<span data-ttu-id="cea96-137">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cea96-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="cea96-138">Нет</span><span class="sxs-lookup"><span data-stu-id="cea96-138">no</span></span>        |
| [<span data-ttu-id="cea96-139">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cea96-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="cea96-140">Нет</span><span class="sxs-lookup"><span data-stu-id="cea96-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="cea96-141">См. также</span><span class="sxs-lookup"><span data-stu-id="cea96-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cea96-142">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cea96-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





