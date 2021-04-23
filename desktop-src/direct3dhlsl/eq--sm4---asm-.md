---
title: EQ (SM4-ASM)
description: Сравнение равенства с плавающей точкой на уровне компонентов.
ms.assetid: 925578E4-0161-45A9-840F-14AA65FF4F33
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f47dc7bda7b1c61c251ace061fc75897788b968
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412123"
---
# <a name="eq-sm4---asm"></a><span data-ttu-id="1b681-103">EQ (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="1b681-103">eq (sm4 - asm)</span></span>

<span data-ttu-id="1b681-104">Сравнение равенства с плавающей точкой на уровне компонентов.</span><span class="sxs-lookup"><span data-stu-id="1b681-104">Component-wise vector floating point equality comparison.</span></span>



| <span data-ttu-id="1b681-105">EQ dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS. \] \[ свиззле \] , \[ - \] src1 \[ \_ ABS \] \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="1b681-105">eq dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------|



 



| <span data-ttu-id="1b681-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="1b681-106">Item</span></span>                                                            | <span data-ttu-id="1b681-107">Описание</span><span class="sxs-lookup"><span data-stu-id="1b681-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="1b681-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="1b681-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="1b681-109">\[в \] адресе результата операции.</span><span class="sxs-lookup"><span data-stu-id="1b681-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="1b681-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="1b681-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="1b681-111">\[в \] компоненте, комапре в *src1*.</span><span class="sxs-lookup"><span data-stu-id="1b681-111">\[in\] The component to comapre to *src1*.</span></span><br/>         |
| <span data-ttu-id="1b681-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="1b681-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="1b681-113">\[в \] компоненте, комапре в *src0*.</span><span class="sxs-lookup"><span data-stu-id="1b681-113">\[in\] The component to comapre to *src0*.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="1b681-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="1b681-114">Remarks</span></span>

<span data-ttu-id="1b681-115">Выполняет сравнение с плавающей запятой (*src0*  ==  *src1*) для каждого компонента и записывает результат в *dest*.</span><span class="sxs-lookup"><span data-stu-id="1b681-115">Performs the float comparison (*src0* == *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="1b681-116">Если сравнение истинно, для этого компонента возвращается значение 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="1b681-116">If the comparison is true, 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="1b681-117">В противном случае возвращается 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="1b681-117">Otherwise 0x0000000 is returned.</span></span>

<span data-ttu-id="1b681-118">Перед сравнением (исходные регистры с нетронутым исходным кодом) выполняется очистка.</span><span class="sxs-lookup"><span data-stu-id="1b681-118">Denorms are flushed before comparison (original source registers untouched).</span></span> <span data-ttu-id="1b681-119">+ 0 равно-0.</span><span class="sxs-lookup"><span data-stu-id="1b681-119">+0 equals -0.</span></span> <span data-ttu-id="1b681-120">Сравнение с NaN возвращает false.</span><span class="sxs-lookup"><span data-stu-id="1b681-120">Comparison with NaN returns false.</span></span>

<span data-ttu-id="1b681-121">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="1b681-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="1b681-122">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="1b681-122">Vertex Shader</span></span> | <span data-ttu-id="1b681-123">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="1b681-123">Geometry Shader</span></span> | <span data-ttu-id="1b681-124">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="1b681-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="1b681-125">x</span><span class="sxs-lookup"><span data-stu-id="1b681-125">x</span></span>             | <span data-ttu-id="1b681-126">x</span><span class="sxs-lookup"><span data-stu-id="1b681-126">x</span></span>               | <span data-ttu-id="1b681-127">x</span><span class="sxs-lookup"><span data-stu-id="1b681-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1b681-128">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="1b681-128">Minimum Shader Model</span></span>

<span data-ttu-id="1b681-129">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="1b681-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1b681-130">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="1b681-130">Shader Model</span></span>                                              | <span data-ttu-id="1b681-131">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="1b681-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1b681-132">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="1b681-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1b681-133">да</span><span class="sxs-lookup"><span data-stu-id="1b681-133">yes</span></span>       |
| [<span data-ttu-id="1b681-134">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="1b681-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1b681-135">да</span><span class="sxs-lookup"><span data-stu-id="1b681-135">yes</span></span>       |
| [<span data-ttu-id="1b681-136">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="1b681-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1b681-137">да</span><span class="sxs-lookup"><span data-stu-id="1b681-137">yes</span></span>       |
| [<span data-ttu-id="1b681-138">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1b681-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1b681-139">Нет</span><span class="sxs-lookup"><span data-stu-id="1b681-139">no</span></span>        |
| [<span data-ttu-id="1b681-140">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1b681-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1b681-141">Нет</span><span class="sxs-lookup"><span data-stu-id="1b681-141">no</span></span>        |
| [<span data-ttu-id="1b681-142">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1b681-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1b681-143">Нет</span><span class="sxs-lookup"><span data-stu-id="1b681-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1b681-144">См. также</span><span class="sxs-lookup"><span data-stu-id="1b681-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b681-145">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1b681-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





