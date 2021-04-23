---
title: итоф (SM4-ASM)
description: Преобразование целого числа со знаком в плавающую точку.
ms.assetid: 60652168-25FA-4084-8CC1-73F12984ECED
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f9d262f65801cd2caa0e6432b335ce32fff0d4e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103890016"
---
# <a name="itof-sm4---asm"></a><span data-ttu-id="57a95-103">итоф (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="57a95-103">itof (sm4 - asm)</span></span>

<span data-ttu-id="57a95-104">Преобразование целого числа со знаком в плавающую точку.</span><span class="sxs-lookup"><span data-stu-id="57a95-104">Signed integer to floating point conversion.</span></span>



| <span data-ttu-id="57a95-105">итоф dest \[ . Mask \] , \[ - \] src0 \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="57a95-105">itof dest\[.mask\], \[-\]src0\[.swizzle\]</span></span> |
|-------------------------------------------|



 



| <span data-ttu-id="57a95-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="57a95-106">Item</span></span>                                                            | <span data-ttu-id="57a95-107">Описание</span><span class="sxs-lookup"><span data-stu-id="57a95-107">Description</span></span>                                             |
|-----------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="57a95-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="57a95-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="57a95-109">\[в \] содержит результат операции.</span><span class="sxs-lookup"><span data-stu-id="57a95-109">\[in\] Contains the result of the operation.</span></span><br/> |
| <span data-ttu-id="57a95-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="57a95-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="57a95-111">\[в \] содержит значение для преобразования.</span><span class="sxs-lookup"><span data-stu-id="57a95-111">\[in\] Contains the value to convert.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="57a95-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="57a95-112">Remarks</span></span>

<span data-ttu-id="57a95-113">Эта инструкция по преобразованию целого числа со знаком в число с плавающей запятой предполагает, что *src0* содержит 32-разрядное целое число с подписью 4.</span><span class="sxs-lookup"><span data-stu-id="57a95-113">This signed integer-to-float conversion instruction assumes that *src0* contains a signed 32-bit integer 4-tuple.</span></span> <span data-ttu-id="57a95-114">После выполнения инструкции *dest* будет содержать кортеж из четырех точек с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="57a95-114">After the instruction executes, *dest* will contain a floating-point 4-tuple.</span></span>

<span data-ttu-id="57a95-115">Преобразование выполняется для каждого компонента.</span><span class="sxs-lookup"><span data-stu-id="57a95-115">The conversion is performed per-component.</span></span>

<span data-ttu-id="57a95-116">Если значение целочисленного ввода слишком велико для точного представления в формате с плавающей запятой, округление до ближайшего четного режима настоятельно рекомендуется, но не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="57a95-116">When an integer input value is too large in magnitude to be represented exactly in the floating point format, rounding to nearest even mode is strongly recommended but not required.</span></span>

<span data-ttu-id="57a95-117">Необязательный модификатор отрицания для исходного операнда перед выполнением арифметической операции принимает 2 дополнения.</span><span class="sxs-lookup"><span data-stu-id="57a95-117">The optional negate modifier on source operand takes 2's complement before performing arithmetic operation.</span></span>

<span data-ttu-id="57a95-118">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="57a95-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="57a95-119">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="57a95-119">Vertex Shader</span></span> | <span data-ttu-id="57a95-120">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="57a95-120">Geometry Shader</span></span> | <span data-ttu-id="57a95-121">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="57a95-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="57a95-122">x</span><span class="sxs-lookup"><span data-stu-id="57a95-122">x</span></span>             | <span data-ttu-id="57a95-123">x</span><span class="sxs-lookup"><span data-stu-id="57a95-123">x</span></span>               | <span data-ttu-id="57a95-124">x</span><span class="sxs-lookup"><span data-stu-id="57a95-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="57a95-125">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="57a95-125">Minimum Shader Model</span></span>

<span data-ttu-id="57a95-126">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="57a95-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="57a95-127">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="57a95-127">Shader Model</span></span>                                              | <span data-ttu-id="57a95-128">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="57a95-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="57a95-129">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="57a95-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="57a95-130">да</span><span class="sxs-lookup"><span data-stu-id="57a95-130">yes</span></span>       |
| [<span data-ttu-id="57a95-131">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="57a95-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="57a95-132">да</span><span class="sxs-lookup"><span data-stu-id="57a95-132">yes</span></span>       |
| [<span data-ttu-id="57a95-133">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="57a95-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="57a95-134">да</span><span class="sxs-lookup"><span data-stu-id="57a95-134">yes</span></span>       |
| [<span data-ttu-id="57a95-135">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="57a95-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="57a95-136">Нет</span><span class="sxs-lookup"><span data-stu-id="57a95-136">no</span></span>        |
| [<span data-ttu-id="57a95-137">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="57a95-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="57a95-138">Нет</span><span class="sxs-lookup"><span data-stu-id="57a95-138">no</span></span>        |
| [<span data-ttu-id="57a95-139">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="57a95-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="57a95-140">Нет</span><span class="sxs-lookup"><span data-stu-id="57a95-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="57a95-141">См. также</span><span class="sxs-lookup"><span data-stu-id="57a95-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57a95-142">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="57a95-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





