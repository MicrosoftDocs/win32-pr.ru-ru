---
title: дек (SM5-ASM)
description: Сравнение равенства с двойной точностью на уровне компонентов.
ms.assetid: 99806989-D3A0-43F4-832A-5F1BD9C59A11
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ed263deec975815f29050d2de0a877a312258c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104532873"
---
# <a name="deq-sm5---asm"></a><span data-ttu-id="2d762-103">дек (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="2d762-103">deq (sm5 - asm)</span></span>

<span data-ttu-id="2d762-104">Сравнение равенства с двойной точностью на уровне компонентов.</span><span class="sxs-lookup"><span data-stu-id="2d762-104">Component-wise double-precision equality comparison.</span></span>



| <span data-ttu-id="2d762-105">Дек \[ \_ \] \[ . Маска \] , \[ - \] src0 \[ \_ ABS \] \[ . свиззле \] , \[ - \] src1 \[ \_ ABS \] \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="2d762-105">deq\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="2d762-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="2d762-106">Item</span></span>                                                            | <span data-ttu-id="2d762-107">Описание</span><span class="sxs-lookup"><span data-stu-id="2d762-107">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="2d762-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="2d762-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="2d762-109">\[в \] адресе результатов операции.</span><span class="sxs-lookup"><span data-stu-id="2d762-109">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="2d762-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="2d762-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="2d762-111">\[в \] компонентах, сравниваемых с *src1*.</span><span class="sxs-lookup"><span data-stu-id="2d762-111">\[in\] The components to compare to *src1*.</span></span><br/>         |
| <span data-ttu-id="2d762-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="2d762-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="2d762-113">\[в \] компонентах, сравниваемых с *src0*.</span><span class="sxs-lookup"><span data-stu-id="2d762-113">\[in\] The components to compare to *src0*.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="2d762-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="2d762-114">Remarks</span></span>

<span data-ttu-id="2d762-115">Эта инструкция выполняет сравнение с плавающей запятой двойной точности (*src0*  ==  *src1*) для каждого компонента и записывает результат в *dest*.</span><span class="sxs-lookup"><span data-stu-id="2d762-115">This instruction performs the double-precision floating-point comparison (*src0* == *src1*) for each component and writes the result to *dest*.</span></span>

<span data-ttu-id="2d762-116">Если сравнение истинно, то для этого компонента возвращается 32-бит 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="2d762-116">If the comparison is true, then 32-bit 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="2d762-117">В противном случае возвращается 32-bit 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="2d762-117">Otherwise 32-bit 0x00000000 is returned.</span></span>

<span data-ttu-id="2d762-118">Сравнение с NaN возвращает false.</span><span class="sxs-lookup"><span data-stu-id="2d762-118">Comparison with NaN returns false.</span></span>

<span data-ttu-id="2d762-119">Допустимые маски *приемников* — один или два компонента.</span><span class="sxs-lookup"><span data-stu-id="2d762-119">The valid *dest* masks are any one or 2 components.</span></span> <span data-ttu-id="2d762-120">Это:. x,. y,. z,. w,. XY,. КСЗ,. КСВ,. из,. Ив,. ZW первый компонент- *приемник* в маске получает 32-разрядный результат для первого двойного сравнения.</span><span class="sxs-lookup"><span data-stu-id="2d762-120">That is: .x, .y, .z, .w, .xy, .xz, .xw, .yz, .yw, .zw The first *dest* component in the mask receives the 32-bit result for the first double comparison.</span></span> <span data-ttu-id="2d762-121">Второй компонент в маске, если он есть, получает 32-разрядный результат для второго двойного сравнения.</span><span class="sxs-lookup"><span data-stu-id="2d762-121">The second component in the mask, if present, receives the 32-bit result for the second double comparison.</span></span>

<span data-ttu-id="2d762-122">Допустимыми свиззлес для параметров источника являются. ксизв,. ксикси,. звкси,. звзв.</span><span class="sxs-lookup"><span data-stu-id="2d762-122">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="2d762-123">Следующие сопоставления *src* — это POST-свиззле:</span><span class="sxs-lookup"><span data-stu-id="2d762-123">The following *src* mappings are post-swizzle:</span></span>

-   <span data-ttu-id="2d762-124">*src0* — это двойное vec2 в (x 32LSB, y 32MSB) и (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="2d762-124">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="2d762-125">*src1* — это двойное vec2 в (x 32LSB, y 32MSB) и (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="2d762-125">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="2d762-126">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="2d762-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2d762-127">Вершина</span><span class="sxs-lookup"><span data-stu-id="2d762-127">Vertex</span></span> | <span data-ttu-id="2d762-128">Поверхности</span><span class="sxs-lookup"><span data-stu-id="2d762-128">Hull</span></span> | <span data-ttu-id="2d762-129">Домен</span><span class="sxs-lookup"><span data-stu-id="2d762-129">Domain</span></span> | <span data-ttu-id="2d762-130">Геометрия</span><span class="sxs-lookup"><span data-stu-id="2d762-130">Geometry</span></span> | <span data-ttu-id="2d762-131">Пиксель</span><span class="sxs-lookup"><span data-stu-id="2d762-131">Pixel</span></span> | <span data-ttu-id="2d762-132">Вычисления</span><span class="sxs-lookup"><span data-stu-id="2d762-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="2d762-133">X</span><span class="sxs-lookup"><span data-stu-id="2d762-133">X</span></span>      | <span data-ttu-id="2d762-134">X</span><span class="sxs-lookup"><span data-stu-id="2d762-134">X</span></span>    | <span data-ttu-id="2d762-135">X</span><span class="sxs-lookup"><span data-stu-id="2d762-135">X</span></span>      | <span data-ttu-id="2d762-136">X</span><span class="sxs-lookup"><span data-stu-id="2d762-136">X</span></span>        | <span data-ttu-id="2d762-137">X</span><span class="sxs-lookup"><span data-stu-id="2d762-137">X</span></span>     | <span data-ttu-id="2d762-138">X</span><span class="sxs-lookup"><span data-stu-id="2d762-138">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2d762-139">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="2d762-139">Minimum Shader Model</span></span>

<span data-ttu-id="2d762-140">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="2d762-140">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="2d762-141">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="2d762-141">Shader Model</span></span>                                              | <span data-ttu-id="2d762-142">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="2d762-142">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2d762-143">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="2d762-143">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2d762-144">да</span><span class="sxs-lookup"><span data-stu-id="2d762-144">yes</span></span>       |
| [<span data-ttu-id="2d762-145">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="2d762-145">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2d762-146">Нет</span><span class="sxs-lookup"><span data-stu-id="2d762-146">no</span></span>        |
| [<span data-ttu-id="2d762-147">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="2d762-147">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2d762-148">Нет</span><span class="sxs-lookup"><span data-stu-id="2d762-148">no</span></span>        |
| [<span data-ttu-id="2d762-149">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2d762-149">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2d762-150">Нет</span><span class="sxs-lookup"><span data-stu-id="2d762-150">no</span></span>        |
| [<span data-ttu-id="2d762-151">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2d762-151">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2d762-152">Нет</span><span class="sxs-lookup"><span data-stu-id="2d762-152">no</span></span>        |
| [<span data-ttu-id="2d762-153">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2d762-153">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2d762-154">Нет</span><span class="sxs-lookup"><span data-stu-id="2d762-154">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2d762-155">См. также</span><span class="sxs-lookup"><span data-stu-id="2d762-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d762-156">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2d762-156">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





