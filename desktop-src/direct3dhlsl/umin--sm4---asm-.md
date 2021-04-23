---
title: Умин (SM4-ASM)
description: Минимальное целое число без знака на уровне компонента.
ms.assetid: 134B128F-7B47-4819-A576-80766EDB14C9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 059b9660e4969b252c867a009a920259c92bff18
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104133310"
---
# <a name="umin-sm4---asm"></a><span data-ttu-id="54a90-103">Умин (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="54a90-103">umin (sm4 - asm)</span></span>

<span data-ttu-id="54a90-104">Минимальное целое число без знака на уровне компонента.</span><span class="sxs-lookup"><span data-stu-id="54a90-104">Component-wise unsigned integer minimum.</span></span>



| <span data-ttu-id="54a90-105">Умин dest \[ . Mask \] , src0 \[ . свиззле \] , src1 \[ . свиззле \] ,</span><span class="sxs-lookup"><span data-stu-id="54a90-105">umin dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\],</span></span> |
|---------------------------------------------------------|



 



| <span data-ttu-id="54a90-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="54a90-106">Item</span></span>                                                            | <span data-ttu-id="54a90-107">Описание</span><span class="sxs-lookup"><span data-stu-id="54a90-107">Description</span></span>                                                                                                            |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54a90-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="54a90-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="54a90-109">\[в \] адресе результата операции.</span><span class="sxs-lookup"><span data-stu-id="54a90-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="54a90-110">*конечный адрес*  =  *src0*  <  *src1* ?</span><span class="sxs-lookup"><span data-stu-id="54a90-110">*dest* = *src0* < *src1* ?</span></span> <span data-ttu-id="54a90-111">*src0* : *src1*</span><span class="sxs-lookup"><span data-stu-id="54a90-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="54a90-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="54a90-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="54a90-113">\[в \] значении, сравниваемом с *src1*.</span><span class="sxs-lookup"><span data-stu-id="54a90-113">\[in\] The value to compare to *src1*.</span></span><br/>                                                                      |
| <span data-ttu-id="54a90-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="54a90-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="54a90-115">\[в \] значении, сравниваемом с *src0*.</span><span class="sxs-lookup"><span data-stu-id="54a90-115">\[in\] The value to compare to *src0*.</span></span><br/>                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="54a90-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="54a90-116">Remarks</span></span>

<span data-ttu-id="54a90-117">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="54a90-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="54a90-118">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="54a90-118">Vertex Shader</span></span> | <span data-ttu-id="54a90-119">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="54a90-119">Geometry Shader</span></span> | <span data-ttu-id="54a90-120">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="54a90-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="54a90-121">x</span><span class="sxs-lookup"><span data-stu-id="54a90-121">x</span></span>             | <span data-ttu-id="54a90-122">x</span><span class="sxs-lookup"><span data-stu-id="54a90-122">x</span></span>               | <span data-ttu-id="54a90-123">x</span><span class="sxs-lookup"><span data-stu-id="54a90-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="54a90-124">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="54a90-124">Minimum Shader Model</span></span>

<span data-ttu-id="54a90-125">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="54a90-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="54a90-126">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="54a90-126">Shader Model</span></span>                                              | <span data-ttu-id="54a90-127">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="54a90-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="54a90-128">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="54a90-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="54a90-129">да</span><span class="sxs-lookup"><span data-stu-id="54a90-129">yes</span></span>       |
| [<span data-ttu-id="54a90-130">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="54a90-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="54a90-131">да</span><span class="sxs-lookup"><span data-stu-id="54a90-131">yes</span></span>       |
| [<span data-ttu-id="54a90-132">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="54a90-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="54a90-133">да</span><span class="sxs-lookup"><span data-stu-id="54a90-133">yes</span></span>       |
| [<span data-ttu-id="54a90-134">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="54a90-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="54a90-135">Нет</span><span class="sxs-lookup"><span data-stu-id="54a90-135">no</span></span>        |
| [<span data-ttu-id="54a90-136">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="54a90-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="54a90-137">Нет</span><span class="sxs-lookup"><span data-stu-id="54a90-137">no</span></span>        |
| [<span data-ttu-id="54a90-138">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="54a90-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="54a90-139">Нет</span><span class="sxs-lookup"><span data-stu-id="54a90-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="54a90-140">См. также</span><span class="sxs-lookup"><span data-stu-id="54a90-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54a90-141">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="54a90-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





