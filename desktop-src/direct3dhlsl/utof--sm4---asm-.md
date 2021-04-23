---
title: утоф (SM4-ASM)
description: Преобразование целого числа без знака в число с плавающей запятой.
ms.assetid: 5A52C959-7B4C-4FA1-B29C-BCAF448419F8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9283857df12a85819f0d191d13450e0311fdade
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104069378"
---
# <a name="utof-sm4---asm"></a><span data-ttu-id="b7604-103">утоф (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="b7604-103">utof (sm4 - asm)</span></span>

<span data-ttu-id="b7604-104">Преобразование целого числа без знака в число с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="b7604-104">Unsigned integer to floating point conversion.</span></span>



| <span data-ttu-id="b7604-105">утоф dest \[ . Mask \] , src0 \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="b7604-105">utof dest\[.mask\], src0\[.swizzle\]</span></span> |
|--------------------------------------|



 



| <span data-ttu-id="b7604-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="b7604-106">Item</span></span>                                                            | <span data-ttu-id="b7604-107">Описание</span><span class="sxs-lookup"><span data-stu-id="b7604-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="b7604-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="b7604-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="b7604-109">\[в \] адресе результата операции.</span><span class="sxs-lookup"><span data-stu-id="b7604-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="b7604-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="b7604-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="b7604-111">\[\]преобразуемые компоненты.</span><span class="sxs-lookup"><span data-stu-id="b7604-111">\[in\] The components to convert.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="b7604-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="b7604-112">Remarks</span></span>

<span data-ttu-id="b7604-113">*src0* должен содержать неподписанный 32-разрядный целочисленный кортеж из 4 элементов.</span><span class="sxs-lookup"><span data-stu-id="b7604-113">*src0* must contain an unsigned 32-bit integer 4-tuple.</span></span> <span data-ttu-id="b7604-114">После выполнения инструкции *dest* будет содержать кортеж из четырех точек с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="b7604-114">After the instruction executes, *dest* will contain a floating-point 4-tuple.</span></span> <span data-ttu-id="b7604-115">Преобразование выполняется для каждого компонента.</span><span class="sxs-lookup"><span data-stu-id="b7604-115">The conversion is performed per-component.</span></span>

<span data-ttu-id="b7604-116">Если целочисленное входное значение слишком велико для точного представления в формате с плавающей запятой, округление до ближайшего четного режима.</span><span class="sxs-lookup"><span data-stu-id="b7604-116">When an integer input value is too large to be represented exactly in the floating point format, round to nearest even mode.</span></span>

<span data-ttu-id="b7604-117">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="b7604-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b7604-118">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="b7604-118">Vertex Shader</span></span> | <span data-ttu-id="b7604-119">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="b7604-119">Geometry Shader</span></span> | <span data-ttu-id="b7604-120">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="b7604-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="b7604-121">x</span><span class="sxs-lookup"><span data-stu-id="b7604-121">x</span></span>             | <span data-ttu-id="b7604-122">x</span><span class="sxs-lookup"><span data-stu-id="b7604-122">x</span></span>               | <span data-ttu-id="b7604-123">x</span><span class="sxs-lookup"><span data-stu-id="b7604-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b7604-124">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="b7604-124">Minimum Shader Model</span></span>

<span data-ttu-id="b7604-125">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="b7604-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b7604-126">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="b7604-126">Shader Model</span></span>                                              | <span data-ttu-id="b7604-127">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="b7604-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b7604-128">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="b7604-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b7604-129">да</span><span class="sxs-lookup"><span data-stu-id="b7604-129">yes</span></span>       |
| [<span data-ttu-id="b7604-130">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="b7604-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b7604-131">да</span><span class="sxs-lookup"><span data-stu-id="b7604-131">yes</span></span>       |
| [<span data-ttu-id="b7604-132">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="b7604-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b7604-133">да</span><span class="sxs-lookup"><span data-stu-id="b7604-133">yes</span></span>       |
| [<span data-ttu-id="b7604-134">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b7604-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b7604-135">Нет</span><span class="sxs-lookup"><span data-stu-id="b7604-135">no</span></span>        |
| [<span data-ttu-id="b7604-136">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b7604-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b7604-137">Нет</span><span class="sxs-lookup"><span data-stu-id="b7604-137">no</span></span>        |
| [<span data-ttu-id="b7604-138">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b7604-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b7604-139">Нет</span><span class="sxs-lookup"><span data-stu-id="b7604-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b7604-140">См. также</span><span class="sxs-lookup"><span data-stu-id="b7604-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7604-141">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b7604-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





