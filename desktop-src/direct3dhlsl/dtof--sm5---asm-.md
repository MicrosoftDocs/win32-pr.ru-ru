---
title: дтоф (SM5-ASM)
description: Компонентное преобразование из данных с плавающей запятой двойной точности в данные с плавающей запятой одиночной точности.
ms.assetid: 1D2EF05C-06EF-44F0-AA0F-22D3057FF43E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a66e72cf4c2cb1ac49adc492a586b4cbb9eef3b4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335464"
---
# <a name="dtof-sm5---asm"></a><span data-ttu-id="19f8e-103">дтоф (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="19f8e-103">dtof (sm5 - asm)</span></span>

<span data-ttu-id="19f8e-104">Компонентное преобразование из данных с плавающей запятой двойной точности в данные с плавающей запятой одиночной точности.</span><span class="sxs-lookup"><span data-stu-id="19f8e-104">Component-wise conversion from double-precision floating-point data to single-precision floating-point data.</span></span>



| <span data-ttu-id="19f8e-105">дтоф dest \[ . Mask \] , \[ - \] src \[ . свиззле \] ,</span><span class="sxs-lookup"><span data-stu-id="19f8e-105">dtof dest\[.mask\], \[-\]src\[.swizzle\],</span></span> |
|-------------------------------------------|



 



| <span data-ttu-id="19f8e-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="19f8e-106">Item</span></span>                                                            | <span data-ttu-id="19f8e-107">Описание</span><span class="sxs-lookup"><span data-stu-id="19f8e-107">Description</span></span>                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="19f8e-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="19f8e-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="19f8e-109">\[в \] адрес преобразованных данных.</span><span class="sxs-lookup"><span data-stu-id="19f8e-109">\[in\] The address of the converted data.</span></span><br/> |
| <span data-ttu-id="19f8e-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="19f8e-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="19f8e-111">\[\]преобразуемые данные.</span><span class="sxs-lookup"><span data-stu-id="19f8e-111">\[in\] The data to be converted.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="19f8e-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="19f8e-112">Remarks</span></span>

<span data-ttu-id="19f8e-113">Каждый компонент источника преобразуется из представления двойной точности в представление с одиночной точностью с использованием округления до ближайшего числа.</span><span class="sxs-lookup"><span data-stu-id="19f8e-113">Each component of the source is converted from the double-precision representation to the single-precision representation using round-to-nearest-even rounding.</span></span>

<span data-ttu-id="19f8e-114">Допустимый свиззлес для параметра source:. ксизв,. ксикси,. звкси,. звзв.</span><span class="sxs-lookup"><span data-stu-id="19f8e-114">The valid swizzles for the source parameter are .xyzw, .xyxy, .zwxy, .zwzw.</span></span>

<span data-ttu-id="19f8e-115">Допустимые маски *приемников* — это один или два компонента.</span><span class="sxs-lookup"><span data-stu-id="19f8e-115">The valid *dest* masks are any one or two components.</span></span> <span data-ttu-id="19f8e-116">Это:. x,. y,. z,. w,. XY,. КСЗ,. КСВ,. из,. Ив,. ZW результат первого преобразования переходит к первому компоненту маски, а результат второго компонента переходит во второй компонент маски, если он есть.</span><span class="sxs-lookup"><span data-stu-id="19f8e-116">That is: .x, .y, .z, .w, .xy, .xz, .xw, .yz, .yw, .zw The result of the first conversion goes to the first component in the mask, and the result of the second component goes in the second component in the mask, if present.</span></span>

<span data-ttu-id="19f8e-117">компоненты *dest* — float32.</span><span class="sxs-lookup"><span data-stu-id="19f8e-117">*dest* components are float32.</span></span>

<span data-ttu-id="19f8e-118">*src* — это двойное vec2 в (x 32LSB, y 32MSB) и (z 32LSB, w 32MSB) POST свиззле.</span><span class="sxs-lookup"><span data-stu-id="19f8e-118">*src* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB) post swizzle.</span></span>

<span data-ttu-id="19f8e-119">Для преобразований типа float32<->, реализации могут либо учитывать значение float32, либо могут сбрасывать их.</span><span class="sxs-lookup"><span data-stu-id="19f8e-119">For float32<->double conversions, implementations may either honor float32 denorms or may flush them.</span></span>

<span data-ttu-id="19f8e-120">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="19f8e-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="19f8e-121">Вершина</span><span class="sxs-lookup"><span data-stu-id="19f8e-121">Vertex</span></span> | <span data-ttu-id="19f8e-122">Поверхности</span><span class="sxs-lookup"><span data-stu-id="19f8e-122">Hull</span></span> | <span data-ttu-id="19f8e-123">Домен</span><span class="sxs-lookup"><span data-stu-id="19f8e-123">Domain</span></span> | <span data-ttu-id="19f8e-124">Геометрия</span><span class="sxs-lookup"><span data-stu-id="19f8e-124">Geometry</span></span> | <span data-ttu-id="19f8e-125">Пиксель</span><span class="sxs-lookup"><span data-stu-id="19f8e-125">Pixel</span></span> | <span data-ttu-id="19f8e-126">Вычисления</span><span class="sxs-lookup"><span data-stu-id="19f8e-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="19f8e-127">X</span><span class="sxs-lookup"><span data-stu-id="19f8e-127">X</span></span>      | <span data-ttu-id="19f8e-128">X</span><span class="sxs-lookup"><span data-stu-id="19f8e-128">X</span></span>    | <span data-ttu-id="19f8e-129">X</span><span class="sxs-lookup"><span data-stu-id="19f8e-129">X</span></span>      | <span data-ttu-id="19f8e-130">X</span><span class="sxs-lookup"><span data-stu-id="19f8e-130">X</span></span>        | <span data-ttu-id="19f8e-131">X</span><span class="sxs-lookup"><span data-stu-id="19f8e-131">X</span></span>     | <span data-ttu-id="19f8e-132">X</span><span class="sxs-lookup"><span data-stu-id="19f8e-132">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="19f8e-133">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="19f8e-133">Minimum Shader Model</span></span>

<span data-ttu-id="19f8e-134">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="19f8e-134">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="19f8e-135">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="19f8e-135">Shader Model</span></span>                                              | <span data-ttu-id="19f8e-136">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="19f8e-136">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="19f8e-137">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="19f8e-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="19f8e-138">да</span><span class="sxs-lookup"><span data-stu-id="19f8e-138">yes</span></span>       |
| [<span data-ttu-id="19f8e-139">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="19f8e-139">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="19f8e-140">Нет</span><span class="sxs-lookup"><span data-stu-id="19f8e-140">no</span></span>        |
| [<span data-ttu-id="19f8e-141">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="19f8e-141">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="19f8e-142">Нет</span><span class="sxs-lookup"><span data-stu-id="19f8e-142">no</span></span>        |
| [<span data-ttu-id="19f8e-143">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="19f8e-143">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="19f8e-144">Нет</span><span class="sxs-lookup"><span data-stu-id="19f8e-144">no</span></span>        |
| [<span data-ttu-id="19f8e-145">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="19f8e-145">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="19f8e-146">Нет</span><span class="sxs-lookup"><span data-stu-id="19f8e-146">no</span></span>        |
| [<span data-ttu-id="19f8e-147">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="19f8e-147">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="19f8e-148">Нет</span><span class="sxs-lookup"><span data-stu-id="19f8e-148">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="19f8e-149">См. также</span><span class="sxs-lookup"><span data-stu-id="19f8e-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19f8e-150">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="19f8e-150">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





