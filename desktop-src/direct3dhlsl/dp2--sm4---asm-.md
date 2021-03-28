---
title: DP2 (SM4-ASM)
description: 2-мерный вектор точки — продукт компонентов RG, POS-свиззле.
ms.assetid: E35F6A8B-6D8E-4660-B0F3-95B76BC19229
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4073def6cb315dc0268d1ce8e3f28039b9b2a69
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412152"
---
# <a name="dp2-sm4---asm"></a><span data-ttu-id="feec0-103">DP2 (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="feec0-103">dp2 (sm4 - asm)</span></span>

<span data-ttu-id="feec0-104">2-мерный вектор точки — продукт компонентов RG, POS-свиззле.</span><span class="sxs-lookup"><span data-stu-id="feec0-104">2-dimensional vector dot-product of components rg, POS-swizzle.</span></span>



| <span data-ttu-id="feec0-105">DP2 \[ \_ \] \[ . Маска \] , \[ - \] src0 \[ \_ ABS \] \[ . свиззле \] , \[ - \] src1 \[ \_ ABS \] \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="feec0-105">dp2\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="feec0-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="feec0-106">Item</span></span>                                                            | <span data-ttu-id="feec0-107">Описание</span><span class="sxs-lookup"><span data-stu-id="feec0-107">Description</span></span>                                                                                                                    |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="feec0-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="feec0-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="feec0-109">\[в \] адресе результата операции.</span><span class="sxs-lookup"><span data-stu-id="feec0-109">\[in\] The address of the result of the operation.</span></span> <br/> <span data-ttu-id="feec0-110">*конечный адрес*  =  *src0. r* \* *src1. r*  +  *src0. g* \* *src1. g*</span><span class="sxs-lookup"><span data-stu-id="feec0-110">*dest* = *src0.r* \* *src1.r* + *src0.g* \* *src1.g*</span></span><br/> |
| <span data-ttu-id="feec0-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="feec0-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="feec0-112">\[в \] компонентах операции.</span><span class="sxs-lookup"><span data-stu-id="feec0-112">\[in\] The components in the operation.</span></span><br/>                                                                             |
| <span data-ttu-id="feec0-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="feec0-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="feec0-114">\[в \] компонентах операции.</span><span class="sxs-lookup"><span data-stu-id="feec0-114">\[in\] The components in the operation.</span></span><br/>                                                                             |



 

## <a name="remarks"></a><span data-ttu-id="feec0-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="feec0-115">Remarks</span></span>

<span data-ttu-id="feec0-116">Скалярный результат реплицируется в компоненты в маске записи.</span><span class="sxs-lookup"><span data-stu-id="feec0-116">Scalar result replicated to components in write mask.</span></span>

<span data-ttu-id="feec0-117">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="feec0-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="feec0-118">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="feec0-118">Vertex Shader</span></span> | <span data-ttu-id="feec0-119">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="feec0-119">Geometry Shader</span></span> | <span data-ttu-id="feec0-120">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="feec0-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="feec0-121">x</span><span class="sxs-lookup"><span data-stu-id="feec0-121">x</span></span>             | <span data-ttu-id="feec0-122">x</span><span class="sxs-lookup"><span data-stu-id="feec0-122">x</span></span>               | <span data-ttu-id="feec0-123">x</span><span class="sxs-lookup"><span data-stu-id="feec0-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="feec0-124">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="feec0-124">Minimum Shader Model</span></span>

<span data-ttu-id="feec0-125">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="feec0-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="feec0-126">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="feec0-126">Shader Model</span></span>                                              | <span data-ttu-id="feec0-127">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="feec0-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="feec0-128">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="feec0-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="feec0-129">да</span><span class="sxs-lookup"><span data-stu-id="feec0-129">yes</span></span>       |
| [<span data-ttu-id="feec0-130">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="feec0-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="feec0-131">да</span><span class="sxs-lookup"><span data-stu-id="feec0-131">yes</span></span>       |
| [<span data-ttu-id="feec0-132">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="feec0-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="feec0-133">да</span><span class="sxs-lookup"><span data-stu-id="feec0-133">yes</span></span>       |
| [<span data-ttu-id="feec0-134">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="feec0-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="feec0-135">Нет</span><span class="sxs-lookup"><span data-stu-id="feec0-135">no</span></span>        |
| [<span data-ttu-id="feec0-136">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="feec0-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="feec0-137">Нет</span><span class="sxs-lookup"><span data-stu-id="feec0-137">no</span></span>        |
| [<span data-ttu-id="feec0-138">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="feec0-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="feec0-139">Нет</span><span class="sxs-lookup"><span data-stu-id="feec0-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="feec0-140">См. также</span><span class="sxs-lookup"><span data-stu-id="feec0-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="feec0-141">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="feec0-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





