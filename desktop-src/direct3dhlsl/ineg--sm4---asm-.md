---
title: инег (SM4-ASM)
description: 2 дополнение.
ms.assetid: 20C1EEC8-E349-4398-8EE3-EDD01EBCD4B1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec4da3e0cbb08bee7bd732a4da8175705d1e1a0f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412205"
---
# <a name="ineg-sm4---asm"></a><span data-ttu-id="35735-103">инег (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="35735-103">ineg (sm4 - asm)</span></span>

<span data-ttu-id="35735-104">2 дополнение.</span><span class="sxs-lookup"><span data-stu-id="35735-104">2's complement.</span></span>



| <span data-ttu-id="35735-105">инег dest \[ . Mask \] , src0 \[ . свиззле</span><span class="sxs-lookup"><span data-stu-id="35735-105">ineg dest\[.mask\], src0\[.swizzle</span></span> |
|------------------------------------|



 



| <span data-ttu-id="35735-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="35735-106">Item</span></span>                                                            | <span data-ttu-id="35735-107">Описание</span><span class="sxs-lookup"><span data-stu-id="35735-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="35735-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="35735-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="35735-109">\[в \] адресе результата операции.</span><span class="sxs-lookup"><span data-stu-id="35735-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="35735-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="35735-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="35735-111">\[в параметр \] содержит значения для операции.</span><span class="sxs-lookup"><span data-stu-id="35735-111">\[in\] Contains the values for the operation.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="35735-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="35735-112">Remarks</span></span>

<span data-ttu-id="35735-113">Эта инструкция выполняет дополнение 2 для каждого 32-битного значения в *src0*.</span><span class="sxs-lookup"><span data-stu-id="35735-113">This instruction performs component-wise 2's complement of each 32-bit value in *src0*.</span></span> <span data-ttu-id="35735-114">32-разрядные результаты хранятся в *dest*.</span><span class="sxs-lookup"><span data-stu-id="35735-114">The 32-bit results are stored in *dest*.</span></span>

<span data-ttu-id="35735-115">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="35735-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="35735-116">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="35735-116">Vertex Shader</span></span> | <span data-ttu-id="35735-117">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="35735-117">Geometry Shader</span></span> | <span data-ttu-id="35735-118">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="35735-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="35735-119">x</span><span class="sxs-lookup"><span data-stu-id="35735-119">x</span></span>             | <span data-ttu-id="35735-120">x</span><span class="sxs-lookup"><span data-stu-id="35735-120">x</span></span>               | <span data-ttu-id="35735-121">x</span><span class="sxs-lookup"><span data-stu-id="35735-121">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="35735-122">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="35735-122">Minimum Shader Model</span></span>

<span data-ttu-id="35735-123">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="35735-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="35735-124">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="35735-124">Shader Model</span></span>                                              | <span data-ttu-id="35735-125">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="35735-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="35735-126">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="35735-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="35735-127">да</span><span class="sxs-lookup"><span data-stu-id="35735-127">yes</span></span>       |
| [<span data-ttu-id="35735-128">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="35735-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="35735-129">да</span><span class="sxs-lookup"><span data-stu-id="35735-129">yes</span></span>       |
| [<span data-ttu-id="35735-130">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="35735-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="35735-131">да</span><span class="sxs-lookup"><span data-stu-id="35735-131">yes</span></span>       |
| [<span data-ttu-id="35735-132">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="35735-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="35735-133">Нет</span><span class="sxs-lookup"><span data-stu-id="35735-133">no</span></span>        |
| [<span data-ttu-id="35735-134">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="35735-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="35735-135">Нет</span><span class="sxs-lookup"><span data-stu-id="35735-135">no</span></span>        |
| [<span data-ttu-id="35735-136">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="35735-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="35735-137">Нет</span><span class="sxs-lookup"><span data-stu-id="35735-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="35735-138">См. также</span><span class="sxs-lookup"><span data-stu-id="35735-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35735-139">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="35735-139">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





