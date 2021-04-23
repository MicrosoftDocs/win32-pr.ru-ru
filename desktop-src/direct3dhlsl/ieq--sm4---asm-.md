---
title: ИЕК (SM4-ASM)
description: Сравнение равенства целочисленных значений на уровне компонента.
ms.assetid: AD010554-80DC-4D2D-B04C-2638276DDC34
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 579a47ffe38b8322b748f6ba64ce9bbbc26a5bd9
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996954"
---
# <a name="ieq-sm4---asm"></a><span data-ttu-id="1b6f0-103">ИЕК (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="1b6f0-103">ieq (sm4 - asm)</span></span>

<span data-ttu-id="1b6f0-104">Сравнение равенства целочисленных значений на уровне компонента.</span><span class="sxs-lookup"><span data-stu-id="1b6f0-104">Component-wise vector integer equality comparison.</span></span>



| <span data-ttu-id="1b6f0-105">dest \[ . Mask \] , src0 \[ . свиззле \] , src1 \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="1b6f0-105">dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|---------------------------------------------------|



 



| <span data-ttu-id="1b6f0-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="1b6f0-106">Item</span></span>                                                            | <span data-ttu-id="1b6f0-107">Описание</span><span class="sxs-lookup"><span data-stu-id="1b6f0-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="1b6f0-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="1b6f0-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="1b6f0-109">\[в \] адресе результата операции.</span><span class="sxs-lookup"><span data-stu-id="1b6f0-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="1b6f0-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="1b6f0-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="1b6f0-111">\[в \] значении для сравнения с *src1*.</span><span class="sxs-lookup"><span data-stu-id="1b6f0-111">\[in\] The value to compare with *src1*.</span></span><br/>           |
| <span data-ttu-id="1b6f0-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="1b6f0-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="1b6f0-113">\[в \] значении для сравнения с *src0*.</span><span class="sxs-lookup"><span data-stu-id="1b6f0-113">\[in\] The value to compare with *src0*.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="1b6f0-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="1b6f0-114">Remarks</span></span>

<span data-ttu-id="1b6f0-115">Эта инструкция выполняет сравнение целых чисел (*src0*  ==  *src1*) для каждого компонента и записывает результат в *dest*.</span><span class="sxs-lookup"><span data-stu-id="1b6f0-115">This instruction performs the integer comparison (*src0* == *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="1b6f0-116">Если сравнение истинно, то для этого компонента возвращается значение 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="1b6f0-116">If the comparison is true, then 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="1b6f0-117">В противном случае возвращается 0x0000000</span><span class="sxs-lookup"><span data-stu-id="1b6f0-117">Otherwise 0x0000000 is returned</span></span>

<span data-ttu-id="1b6f0-118">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="1b6f0-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="1b6f0-119">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="1b6f0-119">Vertex Shader</span></span> | <span data-ttu-id="1b6f0-120">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="1b6f0-120">Geometry Shader</span></span> | <span data-ttu-id="1b6f0-121">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="1b6f0-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="1b6f0-122">x</span><span class="sxs-lookup"><span data-stu-id="1b6f0-122">x</span></span>             | <span data-ttu-id="1b6f0-123">x</span><span class="sxs-lookup"><span data-stu-id="1b6f0-123">x</span></span>               | <span data-ttu-id="1b6f0-124">x</span><span class="sxs-lookup"><span data-stu-id="1b6f0-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1b6f0-125">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="1b6f0-125">Minimum Shader Model</span></span>

<span data-ttu-id="1b6f0-126">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="1b6f0-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1b6f0-127">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="1b6f0-127">Shader Model</span></span>                                              | <span data-ttu-id="1b6f0-128">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="1b6f0-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1b6f0-129">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="1b6f0-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1b6f0-130">да</span><span class="sxs-lookup"><span data-stu-id="1b6f0-130">yes</span></span>       |
| [<span data-ttu-id="1b6f0-131">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="1b6f0-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1b6f0-132">да</span><span class="sxs-lookup"><span data-stu-id="1b6f0-132">yes</span></span>       |
| [<span data-ttu-id="1b6f0-133">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="1b6f0-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1b6f0-134">да</span><span class="sxs-lookup"><span data-stu-id="1b6f0-134">yes</span></span>       |
| [<span data-ttu-id="1b6f0-135">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1b6f0-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1b6f0-136">Нет</span><span class="sxs-lookup"><span data-stu-id="1b6f0-136">no</span></span>        |
| [<span data-ttu-id="1b6f0-137">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1b6f0-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1b6f0-138">Нет</span><span class="sxs-lookup"><span data-stu-id="1b6f0-138">no</span></span>        |
| [<span data-ttu-id="1b6f0-139">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1b6f0-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1b6f0-140">Нет</span><span class="sxs-lookup"><span data-stu-id="1b6f0-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1b6f0-141">См. также</span><span class="sxs-lookup"><span data-stu-id="1b6f0-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b6f0-142">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1b6f0-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





