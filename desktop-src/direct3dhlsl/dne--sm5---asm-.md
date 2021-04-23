---
title: дне (SM5-ASM)
description: Сравнение на основе компонентов с двойной точностью без проверки на равенство.
ms.assetid: 7C69A86D-0820-4640-AF5A-2993EC77D2AA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae00e0e5f4c0269b14a7a0f330d5af8760a1312f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412186"
---
# <a name="dne-sm5---asm"></a><span data-ttu-id="f0b12-103">дне (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="f0b12-103">dne (sm5 - asm)</span></span>

<span data-ttu-id="f0b12-104">Сравнение на основе компонентов с двойной точностью без проверки на равенство.</span><span class="sxs-lookup"><span data-stu-id="f0b12-104">Component-wise double-precision not equality comparison.</span></span>



| <span data-ttu-id="f0b12-105">дне \[ \_ \] \[ . Маска \] , \[ - \] src0 \[ \_ ABS \] \[ . свиззле \] , \[ - \] src1 \[ \_ ABS \] \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="f0b12-105">dne\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="f0b12-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="f0b12-106">Item</span></span>                                                            | <span data-ttu-id="f0b12-107">Описание</span><span class="sxs-lookup"><span data-stu-id="f0b12-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="f0b12-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="f0b12-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="f0b12-109">\[в \] адресе результата операции.</span><span class="sxs-lookup"><span data-stu-id="f0b12-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="f0b12-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="f0b12-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="f0b12-111">\[в \] компонентах, сравниваемых с *src1*.</span><span class="sxs-lookup"><span data-stu-id="f0b12-111">\[in\] The components to compare with *src1*.</span></span><br/>      |
| <span data-ttu-id="f0b12-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="f0b12-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="f0b12-113">\[в \] компонентах, сравниваемых с *src0*.</span><span class="sxs-lookup"><span data-stu-id="f0b12-113">\[in\] The components to compare with *src0*.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="f0b12-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="f0b12-114">Remarks</span></span>

<span data-ttu-id="f0b12-115">Эта инструкция выполняет сравнение с плавающей запятой двойной точности (*src0* ! = *src1*) для каждого компонента и записывает результат в *dest*.</span><span class="sxs-lookup"><span data-stu-id="f0b12-115">This instruction performs the double-precision floating-point comparison (*src0* != *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="f0b12-116">Если сравнение истинно, то для этого компонента возвращается 32-бит 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="f0b12-116">If the comparison is true, then 32-bit 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="f0b12-117">В противном случае возвращается 32-bit 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="f0b12-117">Otherwise 32-bit 0x00000000 is returned.</span></span>

<span data-ttu-id="f0b12-118">Сравнение с NaN возвращает true.</span><span class="sxs-lookup"><span data-stu-id="f0b12-118">Comparison with NaN returns true.</span></span>

<span data-ttu-id="f0b12-119">Допустимые маски *приемников* — это один или два компонента.</span><span class="sxs-lookup"><span data-stu-id="f0b12-119">The valid *dest* masks are any one or two components.</span></span> <span data-ttu-id="f0b12-120">Это:. x,. y,. z,. w,. XY,. КСЗ,. КСВ,. из,. Ив,. ZW первый компонент- *приемник* в маске получает 32-разрядный результат для первого двойного сравнения.</span><span class="sxs-lookup"><span data-stu-id="f0b12-120">That is: .x, .y, .z, .w, .xy, .xz, .xw, .yz, .yw, .zw The first *dest* component in the mask receives the 32-bit result for the first double comparison.</span></span> <span data-ttu-id="f0b12-121">Второй компонент в маске, если он есть, получает 32-разрядный результат для второго двойного сравнения.</span><span class="sxs-lookup"><span data-stu-id="f0b12-121">The second component in the mask, if present, receives the 32-bit result for the second double comparison.</span></span>

<span data-ttu-id="f0b12-122">Допустимыми свиззлес для параметров источника являются. ксизв,. ксикси,. звкси,. звзв.</span><span class="sxs-lookup"><span data-stu-id="f0b12-122">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="f0b12-123">Следующие сопоставления *src* — это POST-свиззле:</span><span class="sxs-lookup"><span data-stu-id="f0b12-123">The following *src* mappings are post-swizzle:</span></span>

-   <span data-ttu-id="f0b12-124">*src0* — это двойное vec2 в (x 32LSB, y 32MSB) и (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="f0b12-124">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="f0b12-125">*src1* — это двойное vec2 в (x 32LSB, y 32MSB) и (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="f0b12-125">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="f0b12-126">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="f0b12-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f0b12-127">Вершина</span><span class="sxs-lookup"><span data-stu-id="f0b12-127">Vertex</span></span> | <span data-ttu-id="f0b12-128">Поверхности</span><span class="sxs-lookup"><span data-stu-id="f0b12-128">Hull</span></span> | <span data-ttu-id="f0b12-129">Домен</span><span class="sxs-lookup"><span data-stu-id="f0b12-129">Domain</span></span> | <span data-ttu-id="f0b12-130">Геометрия</span><span class="sxs-lookup"><span data-stu-id="f0b12-130">Geometry</span></span> | <span data-ttu-id="f0b12-131">Пиксель</span><span class="sxs-lookup"><span data-stu-id="f0b12-131">Pixel</span></span> | <span data-ttu-id="f0b12-132">Вычисления</span><span class="sxs-lookup"><span data-stu-id="f0b12-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f0b12-133">X</span><span class="sxs-lookup"><span data-stu-id="f0b12-133">X</span></span>      | <span data-ttu-id="f0b12-134">X</span><span class="sxs-lookup"><span data-stu-id="f0b12-134">X</span></span>    | <span data-ttu-id="f0b12-135">X</span><span class="sxs-lookup"><span data-stu-id="f0b12-135">X</span></span>      | <span data-ttu-id="f0b12-136">X</span><span class="sxs-lookup"><span data-stu-id="f0b12-136">X</span></span>        | <span data-ttu-id="f0b12-137">X</span><span class="sxs-lookup"><span data-stu-id="f0b12-137">X</span></span>     | <span data-ttu-id="f0b12-138">X</span><span class="sxs-lookup"><span data-stu-id="f0b12-138">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f0b12-139">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="f0b12-139">Minimum Shader Model</span></span>

<span data-ttu-id="f0b12-140">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="f0b12-140">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="f0b12-141">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="f0b12-141">Shader Model</span></span>                                              | <span data-ttu-id="f0b12-142">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="f0b12-142">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f0b12-143">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="f0b12-143">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f0b12-144">да</span><span class="sxs-lookup"><span data-stu-id="f0b12-144">yes</span></span>       |
| [<span data-ttu-id="f0b12-145">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="f0b12-145">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f0b12-146">Нет</span><span class="sxs-lookup"><span data-stu-id="f0b12-146">no</span></span>        |
| [<span data-ttu-id="f0b12-147">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="f0b12-147">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f0b12-148">Нет</span><span class="sxs-lookup"><span data-stu-id="f0b12-148">no</span></span>        |
| [<span data-ttu-id="f0b12-149">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f0b12-149">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f0b12-150">Нет</span><span class="sxs-lookup"><span data-stu-id="f0b12-150">no</span></span>        |
| [<span data-ttu-id="f0b12-151">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f0b12-151">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f0b12-152">Нет</span><span class="sxs-lookup"><span data-stu-id="f0b12-152">no</span></span>        |
| [<span data-ttu-id="f0b12-153">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f0b12-153">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f0b12-154">Нет</span><span class="sxs-lookup"><span data-stu-id="f0b12-154">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f0b12-155">См. также</span><span class="sxs-lookup"><span data-stu-id="f0b12-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0b12-156">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f0b12-156">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





