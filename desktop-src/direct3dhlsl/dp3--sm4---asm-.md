---
title: DP3 (SM4-ASM)
description: Трехмерная векторная точка — произведение компонентов RGB, POS-свиззле.
ms.assetid: 8E6EA6CD-B5BB-4D64-8846-F7B9F7135582
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2598053abed93675107f15af762e0844d4938fbf
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103889992"
---
# <a name="dp3-sm4---asm"></a><span data-ttu-id="a0529-103">DP3 (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="a0529-103">dp3 (sm4 - asm)</span></span>

<span data-ttu-id="a0529-104">Трехмерная векторная точка — произведение компонентов RGB, POS-свиззле.</span><span class="sxs-lookup"><span data-stu-id="a0529-104">3-dimensional vector dot-product of components rgb, POS-swizzle.</span></span>



| <span data-ttu-id="a0529-105">DP3 \[ \_ \] \[ . Маска \] , \[ - \] src0 \[ \_ ABS \] \[ . свиззле \] , \[ - \] src1 \[ \_ ABS \] \[ . свиззле \] ,</span><span class="sxs-lookup"><span data-stu-id="a0529-105">dp3\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\],</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="a0529-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="a0529-106">Item</span></span>                                                            | <span data-ttu-id="a0529-107">Описание</span><span class="sxs-lookup"><span data-stu-id="a0529-107">Description</span></span>                                                                                                                           |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0529-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="a0529-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="a0529-109">\[в \] результате операции.</span><span class="sxs-lookup"><span data-stu-id="a0529-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="a0529-110">*конечный адрес*  =  *src0. r* \* *src1. r*  +  *src0. g* \* *src1. g*  +  *src0. b* \* *src1. b*</span><span class="sxs-lookup"><span data-stu-id="a0529-110">*dest* = *src0.r* \* *src1.r* + *src0.g* \* *src1.g* + *src0.b* \* *src1.b*</span></span><br/> |
| <span data-ttu-id="a0529-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="a0529-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="a0529-112">\[в \] компонентах в выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="a0529-112">\[in\] The components in the opertation.</span></span><br/>                                                                                   |
| <span data-ttu-id="a0529-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="a0529-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="a0529-114">\[в \] компонентах в выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="a0529-114">\[in\] The components in the opertation.</span></span><br/>                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="a0529-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="a0529-115">Remarks</span></span>

<span data-ttu-id="a0529-116">Скалярный результат реплицируется в компоненты в маске записи.</span><span class="sxs-lookup"><span data-stu-id="a0529-116">Scalar result replicated to components in write mask.</span></span>

<span data-ttu-id="a0529-117">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="a0529-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="a0529-118">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="a0529-118">Vertex Shader</span></span> | <span data-ttu-id="a0529-119">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="a0529-119">Geometry Shader</span></span> | <span data-ttu-id="a0529-120">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="a0529-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="a0529-121">x</span><span class="sxs-lookup"><span data-stu-id="a0529-121">x</span></span>             | <span data-ttu-id="a0529-122">x</span><span class="sxs-lookup"><span data-stu-id="a0529-122">x</span></span>               | <span data-ttu-id="a0529-123">x</span><span class="sxs-lookup"><span data-stu-id="a0529-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a0529-124">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="a0529-124">Minimum Shader Model</span></span>

<span data-ttu-id="a0529-125">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="a0529-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a0529-126">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="a0529-126">Shader Model</span></span>                                              | <span data-ttu-id="a0529-127">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="a0529-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a0529-128">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="a0529-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a0529-129">да</span><span class="sxs-lookup"><span data-stu-id="a0529-129">yes</span></span>       |
| [<span data-ttu-id="a0529-130">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="a0529-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a0529-131">да</span><span class="sxs-lookup"><span data-stu-id="a0529-131">yes</span></span>       |
| [<span data-ttu-id="a0529-132">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="a0529-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a0529-133">да</span><span class="sxs-lookup"><span data-stu-id="a0529-133">yes</span></span>       |
| [<span data-ttu-id="a0529-134">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a0529-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a0529-135">Нет</span><span class="sxs-lookup"><span data-stu-id="a0529-135">no</span></span>        |
| [<span data-ttu-id="a0529-136">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a0529-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a0529-137">Нет</span><span class="sxs-lookup"><span data-stu-id="a0529-137">no</span></span>        |
| [<span data-ttu-id="a0529-138">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a0529-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a0529-139">Нет</span><span class="sxs-lookup"><span data-stu-id="a0529-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a0529-140">См. также</span><span class="sxs-lookup"><span data-stu-id="a0529-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0529-141">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a0529-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





