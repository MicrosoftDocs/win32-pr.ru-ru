---
title: lt (SM4-ASM)
description: Компонентно-ориентированный вектор с плавающей точкой меньше, чем сравнение.
ms.assetid: DB10F654-4A98-4ED8-A3B4-CA9FE1DFE6CD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67a727987e4eaee017137d62dbe12f8581540876
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335528"
---
# <a name="lt-sm4---asm"></a><span data-ttu-id="f1cc2-103">lt (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="f1cc2-103">lt (sm4 - asm)</span></span>

<span data-ttu-id="f1cc2-104">Компонентно-ориентированный вектор с плавающей точкой меньше, чем сравнение.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-104">Component-wise vector floating point less-than comparison.</span></span>



| <span data-ttu-id="f1cc2-105">lt dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS. \] \[ свиззле \] , \[ - \] src1 \[ \_ ABS \] \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="f1cc2-105">lt dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------|



 



| <span data-ttu-id="f1cc2-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="f1cc2-106">Item</span></span>                                                            | <span data-ttu-id="f1cc2-107">Описание</span><span class="sxs-lookup"><span data-stu-id="f1cc2-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="f1cc2-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="f1cc2-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="f1cc2-109">\[в \] адресе результата операции.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="f1cc2-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="f1cc2-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="f1cc2-111">\[в \] значении, сравниваемом с *src1*.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-111">\[in\] The value to compare to *src1*.</span></span><br/>             |
| <span data-ttu-id="f1cc2-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="f1cc2-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="f1cc2-113">\[в \] значении, сравниваемом с *src0*.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-113">\[in\] The value to compare to *src0*.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="f1cc2-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="f1cc2-114">Remarks</span></span>

<span data-ttu-id="f1cc2-115">Эта инструкция выполняет сравнение с плавающей запятой (*src0*  <  *src1*) для каждого компонента и записывает результат в *dest*.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-115">This instruction performs the float comparison (*src0* < *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="f1cc2-116">Если сравнение истинно, то для этого компонента возвращается значение 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-116">If the comparison is true, then 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="f1cc2-117">В противном случае возвращается 0x0000000</span><span class="sxs-lookup"><span data-stu-id="f1cc2-117">Otherwise 0x0000000 is returned</span></span>

<span data-ttu-id="f1cc2-118">Перед сравнением выполняется очистка. исходные регистры исходного кода не затрагиваются.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-118">Denorms are flushed before comparison; original source registers are untouched.</span></span>

<span data-ttu-id="f1cc2-119">+ 0 равно-0.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-119">+0 equals -0.</span></span>

<span data-ttu-id="f1cc2-120">Сравнение с NaN возвращает false.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-120">Comparison with NaN returns false.</span></span>

<span data-ttu-id="f1cc2-121">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="f1cc2-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f1cc2-122">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="f1cc2-122">Vertex Shader</span></span> | <span data-ttu-id="f1cc2-123">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="f1cc2-123">Geometry Shader</span></span> | <span data-ttu-id="f1cc2-124">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="f1cc2-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="f1cc2-125">x</span><span class="sxs-lookup"><span data-stu-id="f1cc2-125">x</span></span>             | <span data-ttu-id="f1cc2-126">x</span><span class="sxs-lookup"><span data-stu-id="f1cc2-126">x</span></span>               | <span data-ttu-id="f1cc2-127">x</span><span class="sxs-lookup"><span data-stu-id="f1cc2-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f1cc2-128">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="f1cc2-128">Minimum Shader Model</span></span>

<span data-ttu-id="f1cc2-129">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f1cc2-130">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="f1cc2-130">Shader Model</span></span>                                              | <span data-ttu-id="f1cc2-131">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="f1cc2-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f1cc2-132">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="f1cc2-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f1cc2-133">да</span><span class="sxs-lookup"><span data-stu-id="f1cc2-133">yes</span></span>       |
| [<span data-ttu-id="f1cc2-134">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="f1cc2-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f1cc2-135">да</span><span class="sxs-lookup"><span data-stu-id="f1cc2-135">yes</span></span>       |
| [<span data-ttu-id="f1cc2-136">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="f1cc2-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f1cc2-137">да</span><span class="sxs-lookup"><span data-stu-id="f1cc2-137">yes</span></span>       |
| [<span data-ttu-id="f1cc2-138">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f1cc2-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f1cc2-139">Нет</span><span class="sxs-lookup"><span data-stu-id="f1cc2-139">no</span></span>        |
| [<span data-ttu-id="f1cc2-140">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f1cc2-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f1cc2-141">Нет</span><span class="sxs-lookup"><span data-stu-id="f1cc2-141">no</span></span>        |
| [<span data-ttu-id="f1cc2-142">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f1cc2-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f1cc2-143">Нет</span><span class="sxs-lookup"><span data-stu-id="f1cc2-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f1cc2-144">См. также</span><span class="sxs-lookup"><span data-stu-id="f1cc2-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1cc2-145">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f1cc2-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





