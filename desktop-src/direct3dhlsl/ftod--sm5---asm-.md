---
title: фтод (SM5-ASM)
description: Компонентное преобразование из данных с плавающей запятой одиночной точности в данные двойной точности с плавающей запятой.
ms.assetid: 95297556-41ED-4ED0-8F9A-16B7A440AF25
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6790735745805426d32aefcc5d5d771ade644e43
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335568"
---
# <a name="ftod-sm5---asm"></a><span data-ttu-id="ad02b-103">фтод (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="ad02b-103">ftod (sm5 - asm)</span></span>

<span data-ttu-id="ad02b-104">Компонентное преобразование из данных с плавающей запятой одиночной точности в данные двойной точности с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="ad02b-104">Component-wise conversion from single-precision floating-point data to double-precision floating-point data.</span></span>



| <span data-ttu-id="ad02b-105">фтод dest \[ . Mask \] , \[ - \] src \[ . свиззле \] ,</span><span class="sxs-lookup"><span data-stu-id="ad02b-105">ftod dest\[.mask\], \[-\]src\[.swizzle\],</span></span> |
|-------------------------------------------|



 



| <span data-ttu-id="ad02b-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="ad02b-106">Item</span></span>                                                            | <span data-ttu-id="ad02b-107">Описание</span><span class="sxs-lookup"><span data-stu-id="ad02b-107">Description</span></span>                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ad02b-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="ad02b-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="ad02b-109">\[в \] адрес преобразованных данных.</span><span class="sxs-lookup"><span data-stu-id="ad02b-109">\[in\] The address of the converted data.</span></span><br/> |
| <span data-ttu-id="ad02b-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="ad02b-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="ad02b-111">\[\]преобразуемые данные.</span><span class="sxs-lookup"><span data-stu-id="ad02b-111">\[in\] The data to be converted.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="ad02b-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="ad02b-112">Remarks</span></span>

<span data-ttu-id="ad02b-113">Каждый компонент источника преобразуется из представления с одиночной точностью в представление двойной точности.</span><span class="sxs-lookup"><span data-stu-id="ad02b-113">Each component of the source is converted from the single-precision representation to the double-precision representation.</span></span>

<span data-ttu-id="ad02b-114">Допустимые маски *приемников* : XY, ZW и. ксизв.</span><span class="sxs-lookup"><span data-stu-id="ad02b-114">The valid *dest* masks are .xy, .zw, and .xyzw.</span></span> <span data-ttu-id="ad02b-115">. XY получает результат первого преобразования, а. ZW получает результат второго преобразования.</span><span class="sxs-lookup"><span data-stu-id="ad02b-115">.xy receives the result of the first conversion, and .zw receives the result of the second conversion.</span></span>

<span data-ttu-id="ad02b-116">*dest* — это двойное vec2 в (x 32LSB, y 32MSB) и (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="ad02b-116">*dest* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="ad02b-117">*src* — это vec2 с плавающей запятой в пределах x и y (ZW игнорируется) (POST свиззле).</span><span class="sxs-lookup"><span data-stu-id="ad02b-117">*src* is a float vec2 across x and y (zw ignored) (post swizzle).</span></span>

<span data-ttu-id="ad02b-118">Для преобразований типа float32<->, реализации могут либо учитывать значение float32, либо могут сбрасывать их.</span><span class="sxs-lookup"><span data-stu-id="ad02b-118">For float32<->double conversions, implementations may either honor float32 denorms or may flush them.</span></span>

<span data-ttu-id="ad02b-119">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="ad02b-119">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ad02b-120">Вершина</span><span class="sxs-lookup"><span data-stu-id="ad02b-120">Vertex</span></span> | <span data-ttu-id="ad02b-121">Поверхности</span><span class="sxs-lookup"><span data-stu-id="ad02b-121">Hull</span></span> | <span data-ttu-id="ad02b-122">Домен</span><span class="sxs-lookup"><span data-stu-id="ad02b-122">Domain</span></span> | <span data-ttu-id="ad02b-123">Геометрия</span><span class="sxs-lookup"><span data-stu-id="ad02b-123">Geometry</span></span> | <span data-ttu-id="ad02b-124">Пиксель</span><span class="sxs-lookup"><span data-stu-id="ad02b-124">Pixel</span></span> | <span data-ttu-id="ad02b-125">Вычисления</span><span class="sxs-lookup"><span data-stu-id="ad02b-125">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ad02b-126">X</span><span class="sxs-lookup"><span data-stu-id="ad02b-126">X</span></span>      | <span data-ttu-id="ad02b-127">X</span><span class="sxs-lookup"><span data-stu-id="ad02b-127">X</span></span>    | <span data-ttu-id="ad02b-128">X</span><span class="sxs-lookup"><span data-stu-id="ad02b-128">X</span></span>      | <span data-ttu-id="ad02b-129">X</span><span class="sxs-lookup"><span data-stu-id="ad02b-129">X</span></span>        | <span data-ttu-id="ad02b-130">X</span><span class="sxs-lookup"><span data-stu-id="ad02b-130">X</span></span>     | <span data-ttu-id="ad02b-131">X</span><span class="sxs-lookup"><span data-stu-id="ad02b-131">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ad02b-132">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ad02b-132">Minimum Shader Model</span></span>

<span data-ttu-id="ad02b-133">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="ad02b-133">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="ad02b-134">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ad02b-134">Shader Model</span></span>                                              | <span data-ttu-id="ad02b-135">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="ad02b-135">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ad02b-136">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="ad02b-136">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ad02b-137">да</span><span class="sxs-lookup"><span data-stu-id="ad02b-137">yes</span></span>       |
| [<span data-ttu-id="ad02b-138">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="ad02b-138">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ad02b-139">Нет</span><span class="sxs-lookup"><span data-stu-id="ad02b-139">no</span></span>        |
| [<span data-ttu-id="ad02b-140">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="ad02b-140">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ad02b-141">Нет</span><span class="sxs-lookup"><span data-stu-id="ad02b-141">no</span></span>        |
| [<span data-ttu-id="ad02b-142">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ad02b-142">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ad02b-143">Нет</span><span class="sxs-lookup"><span data-stu-id="ad02b-143">no</span></span>        |
| [<span data-ttu-id="ad02b-144">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ad02b-144">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ad02b-145">Нет</span><span class="sxs-lookup"><span data-stu-id="ad02b-145">no</span></span>        |
| [<span data-ttu-id="ad02b-146">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ad02b-146">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ad02b-147">Нет</span><span class="sxs-lookup"><span data-stu-id="ad02b-147">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ad02b-148">См. также</span><span class="sxs-lookup"><span data-stu-id="ad02b-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad02b-149">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ad02b-149">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





