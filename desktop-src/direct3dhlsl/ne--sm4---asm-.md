---
title: NE (SM4-ASM)
description: Сравнение на уровне компонентов с плавающей запятой "не равно".
ms.assetid: 5BED97D3-8FF6-4F1C-819B-DC8B4A4F2CCA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0e53ff726047bd1870e6c836f4508bdf87001b3
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412181"
---
# <a name="ne-sm4---asm"></a><span data-ttu-id="c7272-103">NE (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="c7272-103">ne (sm4 - asm)</span></span>

<span data-ttu-id="c7272-104">Сравнение на уровне компонентов с плавающей запятой "не равно".</span><span class="sxs-lookup"><span data-stu-id="c7272-104">Component-wise vector floating point not-equal comparison.</span></span>



| <span data-ttu-id="c7272-105">Ne dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS. \] \[ свиззле \] , \[ - \] src1 \[ \_ ABS \] \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="c7272-105">ne dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------|



 



| <span data-ttu-id="c7272-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="c7272-106">Item</span></span>                                                            | <span data-ttu-id="c7272-107">Описание</span><span class="sxs-lookup"><span data-stu-id="c7272-107">Description</span></span>                                            |
|-----------------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="c7272-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="c7272-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="c7272-109">\[в \] результате операции.</span><span class="sxs-lookup"><span data-stu-id="c7272-109">\[in\] The result of the operation.</span></span><br/>         |
| <span data-ttu-id="c7272-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="c7272-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="c7272-111">\[в \] компонентах, сравниваемых с *src1*.</span><span class="sxs-lookup"><span data-stu-id="c7272-111">\[in\] The components to compare to *src1*.</span></span><br/> |
| <span data-ttu-id="c7272-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="c7272-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="c7272-113">\[в \] компонентах, сравниваемых с *src0*.</span><span class="sxs-lookup"><span data-stu-id="c7272-113">\[in\] The components to compare to *src0*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c7272-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="c7272-114">Remarks</span></span>

<span data-ttu-id="c7272-115">Эта инструкция выполняет сравнение с плавающей запятой (*src0* ! = *src1*) для каждого компонента и записывает результат в *dest*.</span><span class="sxs-lookup"><span data-stu-id="c7272-115">This instruction performs the float comparison (*src0* != *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="c7272-116">Если сравнение истинно, то для этого компонента возвращается значение 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="c7272-116">If the comparison is true, then 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="c7272-117">В противном случае возвращается 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="c7272-117">Otherwise 0x0000000 is returned.</span></span>

<span data-ttu-id="c7272-118">Перед сравнением с нетронутыми исходными регистрами источников выполняется очистка.</span><span class="sxs-lookup"><span data-stu-id="c7272-118">Denorms are flushed before comparison with original source registers untouched.</span></span>

<span data-ttu-id="c7272-119">+ 0 равно-0.</span><span class="sxs-lookup"><span data-stu-id="c7272-119">+0 equals -0.</span></span>

<span data-ttu-id="c7272-120">Сравнение с NaN возвращает true.</span><span class="sxs-lookup"><span data-stu-id="c7272-120">Comparison with NaN returns true.</span></span>

<span data-ttu-id="c7272-121">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="c7272-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="c7272-122">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="c7272-122">Vertex Shader</span></span> | <span data-ttu-id="c7272-123">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="c7272-123">Geometry Shader</span></span> | <span data-ttu-id="c7272-124">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="c7272-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="c7272-125">x</span><span class="sxs-lookup"><span data-stu-id="c7272-125">x</span></span>             | <span data-ttu-id="c7272-126">x</span><span class="sxs-lookup"><span data-stu-id="c7272-126">x</span></span>               | <span data-ttu-id="c7272-127">x</span><span class="sxs-lookup"><span data-stu-id="c7272-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="c7272-128">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="c7272-128">Minimum Shader Model</span></span>

<span data-ttu-id="c7272-129">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="c7272-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c7272-130">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="c7272-130">Shader Model</span></span>                                              | <span data-ttu-id="c7272-131">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="c7272-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c7272-132">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="c7272-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c7272-133">да</span><span class="sxs-lookup"><span data-stu-id="c7272-133">yes</span></span>       |
| [<span data-ttu-id="c7272-134">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="c7272-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c7272-135">да</span><span class="sxs-lookup"><span data-stu-id="c7272-135">yes</span></span>       |
| [<span data-ttu-id="c7272-136">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="c7272-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c7272-137">да</span><span class="sxs-lookup"><span data-stu-id="c7272-137">yes</span></span>       |
| [<span data-ttu-id="c7272-138">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c7272-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c7272-139">Нет</span><span class="sxs-lookup"><span data-stu-id="c7272-139">no</span></span>        |
| [<span data-ttu-id="c7272-140">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c7272-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c7272-141">Нет</span><span class="sxs-lookup"><span data-stu-id="c7272-141">no</span></span>        |
| [<span data-ttu-id="c7272-142">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c7272-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c7272-143">Нет</span><span class="sxs-lookup"><span data-stu-id="c7272-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c7272-144">См. также</span><span class="sxs-lookup"><span data-stu-id="c7272-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7272-145">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c7272-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





