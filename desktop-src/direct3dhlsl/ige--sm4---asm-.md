---
title: иже (SM4-ASM)
description: Сравнение на уровне компонентов целочисленного сравнения "больше или равно".
ms.assetid: 3A3225D1-9A3D-4928-9041-38CB6DE16E2A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8709ebedb054dffe227340f2ccd3de572d92ffce
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104133303"
---
# <a name="ige-sm4---asm"></a><span data-ttu-id="fecfd-103">иже (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="fecfd-103">ige (sm4 - asm)</span></span>

<span data-ttu-id="fecfd-104">Сравнение на уровне компонентов целочисленного сравнения "больше или равно".</span><span class="sxs-lookup"><span data-stu-id="fecfd-104">Component-wise vector integer greater-than-or-equal comparison.</span></span>



| <span data-ttu-id="fecfd-105">иже dest \[ . Mask \] , src0 \[ . свиззле \] , src1 \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="fecfd-105">ige dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|-------------------------------------------------------|



 



| <span data-ttu-id="fecfd-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="fecfd-106">Item</span></span>                                                            | <span data-ttu-id="fecfd-107">Описание</span><span class="sxs-lookup"><span data-stu-id="fecfd-107">Description</span></span>                                           |
|-----------------------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="fecfd-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="fecfd-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="fecfd-109">\[в \] результате операции.</span><span class="sxs-lookup"><span data-stu-id="fecfd-109">\[in\] The result of the operation.</span></span><br/>        |
| <span data-ttu-id="fecfd-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="fecfd-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="fecfd-111">\[в \] компоненте для сравнения с *src1*.</span><span class="sxs-lookup"><span data-stu-id="fecfd-111">\[in\] The component to compare to *src1*.</span></span><br/> |
| <span data-ttu-id="fecfd-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="fecfd-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="fecfd-113">\[в \] компоненте для сравнения с *src0*.</span><span class="sxs-lookup"><span data-stu-id="fecfd-113">\[in\] The component to compare to *src0*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fecfd-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="fecfd-114">Remarks</span></span>

<span data-ttu-id="fecfd-115">Выполняет сравнение целых чисел (*src0*  >=  *src1*) для каждого компонента и записывает результат в *dest*.</span><span class="sxs-lookup"><span data-stu-id="fecfd-115">Performs the integer comparison (*src0* >= *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="fecfd-116">Если сравнение истинно, то для этого компонента возвращается значение 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="fecfd-116">If the comparison is true, then 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="fecfd-117">В противном случае возвращается 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="fecfd-117">Otherwise 0x0000000 is returned.</span></span>

<span data-ttu-id="fecfd-118">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="fecfd-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="fecfd-119">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="fecfd-119">Vertex Shader</span></span> | <span data-ttu-id="fecfd-120">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="fecfd-120">Geometry Shader</span></span> | <span data-ttu-id="fecfd-121">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="fecfd-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="fecfd-122">x</span><span class="sxs-lookup"><span data-stu-id="fecfd-122">x</span></span>             | <span data-ttu-id="fecfd-123">x</span><span class="sxs-lookup"><span data-stu-id="fecfd-123">x</span></span>               | <span data-ttu-id="fecfd-124">x</span><span class="sxs-lookup"><span data-stu-id="fecfd-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="fecfd-125">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="fecfd-125">Minimum Shader Model</span></span>

<span data-ttu-id="fecfd-126">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="fecfd-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="fecfd-127">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="fecfd-127">Shader Model</span></span>                                              | <span data-ttu-id="fecfd-128">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="fecfd-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="fecfd-129">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="fecfd-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="fecfd-130">да</span><span class="sxs-lookup"><span data-stu-id="fecfd-130">yes</span></span>       |
| [<span data-ttu-id="fecfd-131">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="fecfd-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="fecfd-132">да</span><span class="sxs-lookup"><span data-stu-id="fecfd-132">yes</span></span>       |
| [<span data-ttu-id="fecfd-133">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="fecfd-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="fecfd-134">да</span><span class="sxs-lookup"><span data-stu-id="fecfd-134">yes</span></span>       |
| [<span data-ttu-id="fecfd-135">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fecfd-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="fecfd-136">Нет</span><span class="sxs-lookup"><span data-stu-id="fecfd-136">no</span></span>        |
| [<span data-ttu-id="fecfd-137">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fecfd-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="fecfd-138">Нет</span><span class="sxs-lookup"><span data-stu-id="fecfd-138">no</span></span>        |
| [<span data-ttu-id="fecfd-139">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fecfd-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="fecfd-140">Нет</span><span class="sxs-lookup"><span data-stu-id="fecfd-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="fecfd-141">См. также</span><span class="sxs-lookup"><span data-stu-id="fecfd-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fecfd-142">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fecfd-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





