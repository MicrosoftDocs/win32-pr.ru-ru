---
title: DP4 (SM4-ASM)
description: 4-мерный вектор точки — произведение компонентов RGBA, POS-свиззле.
ms.assetid: A41EC054-0060-49CA-90FB-A096E63DD27D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57a91a253d4e8b53bc044e658c3fe75d8f7547da
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103987079"
---
# <a name="dp4-sm4---asm"></a><span data-ttu-id="39004-103">DP4 (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="39004-103">dp4 (sm4 - asm)</span></span>

<span data-ttu-id="39004-104">4-мерный вектор точки — произведение компонентов RGBA, POS-свиззле.</span><span class="sxs-lookup"><span data-stu-id="39004-104">4-dimensional vector dot-product of components rgba, POS-swizzle.</span></span>



| <span data-ttu-id="39004-105">DP4 \[ \_ \] \[ . Маска \] , \[ - \] src0 \[ \_ ABS \] \[ . свиззле \] , \[ - \] src1 \[ \_ ABS \] \[ . свиззле \] ,</span><span class="sxs-lookup"><span data-stu-id="39004-105">dp4\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\],</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="39004-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="39004-106">Item</span></span>                                                            | <span data-ttu-id="39004-107">Описание</span><span class="sxs-lookup"><span data-stu-id="39004-107">Description</span></span>                                                                                                                                                  |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39004-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="39004-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="39004-109">\[в \] результате операции.</span><span class="sxs-lookup"><span data-stu-id="39004-109">\[in\] The result of the operation.</span></span> <br/> <span data-ttu-id="39004-110">*конечный адрес*  =  *src0. r* \* *src1. r*  +  *src0. g* \* *src1. g*  +  *src0. b* \* *src1. b* +  *src0. a* \* *src1. a*</span><span class="sxs-lookup"><span data-stu-id="39004-110">*dest* = *src0.r* \* *src1.r* + *src0.g* \* *src1.g* + *src0.b* \* *src1.b*+ *src0.a* \* *src1.a*</span></span><br/> |
| <span data-ttu-id="39004-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="39004-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="39004-112">\[в \] компонентах в выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="39004-112">\[in\] The components in the opertation.</span></span><br/>                                                                                                          |
| <span data-ttu-id="39004-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="39004-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="39004-114">\[в \] компонентах в выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="39004-114">\[in\] The components in the opertation.</span></span><br/>                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="39004-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="39004-115">Remarks</span></span>

<span data-ttu-id="39004-116">Скалярный результат реплицируется в компоненты в маске записи.</span><span class="sxs-lookup"><span data-stu-id="39004-116">Scalar result replicated to components in write mask.</span></span>

<span data-ttu-id="39004-117">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="39004-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="39004-118">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="39004-118">Vertex Shader</span></span> | <span data-ttu-id="39004-119">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="39004-119">Geometry Shader</span></span> | <span data-ttu-id="39004-120">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="39004-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="39004-121">x</span><span class="sxs-lookup"><span data-stu-id="39004-121">x</span></span>             | <span data-ttu-id="39004-122">x</span><span class="sxs-lookup"><span data-stu-id="39004-122">x</span></span>               | <span data-ttu-id="39004-123">x</span><span class="sxs-lookup"><span data-stu-id="39004-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="39004-124">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="39004-124">Minimum Shader Model</span></span>

<span data-ttu-id="39004-125">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="39004-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="39004-126">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="39004-126">Shader Model</span></span>                                              | <span data-ttu-id="39004-127">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="39004-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="39004-128">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="39004-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="39004-129">да</span><span class="sxs-lookup"><span data-stu-id="39004-129">yes</span></span>       |
| [<span data-ttu-id="39004-130">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="39004-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="39004-131">да</span><span class="sxs-lookup"><span data-stu-id="39004-131">yes</span></span>       |
| [<span data-ttu-id="39004-132">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="39004-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="39004-133">да</span><span class="sxs-lookup"><span data-stu-id="39004-133">yes</span></span>       |
| [<span data-ttu-id="39004-134">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="39004-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="39004-135">Нет</span><span class="sxs-lookup"><span data-stu-id="39004-135">no</span></span>        |
| [<span data-ttu-id="39004-136">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="39004-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="39004-137">Нет</span><span class="sxs-lookup"><span data-stu-id="39004-137">no</span></span>        |
| [<span data-ttu-id="39004-138">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="39004-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="39004-139">Нет</span><span class="sxs-lookup"><span data-stu-id="39004-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="39004-140">См. также</span><span class="sxs-lookup"><span data-stu-id="39004-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39004-141">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="39004-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





