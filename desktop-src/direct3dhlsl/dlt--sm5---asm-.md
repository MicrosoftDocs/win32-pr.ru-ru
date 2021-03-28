---
title: DLT (SM5-ASM)
description: Покомпонентное сравнение двойной точности "меньше чем".
ms.assetid: A9DE5007-4ADD-403D-A2B7-EAE475E9DCCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88fd45ebde621ed2c5f5aafc013741d6ee34c318
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983841"
---
# <a name="dlt-sm5---asm"></a><span data-ttu-id="1a327-103">DLT (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="1a327-103">dlt (sm5 - asm)</span></span>

<span data-ttu-id="1a327-104">Покомпонентное сравнение двойной точности "меньше чем".</span><span class="sxs-lookup"><span data-stu-id="1a327-104">Component-wise double-precision less-than comparison.</span></span>



| <span data-ttu-id="1a327-105">DLT \[ \_ Кот \] \[ . Маска \] , \[ - \] src0 \[ \_ ABS \] \[ . свиззле \] , \[ - \] src1 \[ \_ ABS \] \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="1a327-105">dlt\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="1a327-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="1a327-106">Item</span></span>                                                            | <span data-ttu-id="1a327-107">Описание</span><span class="sxs-lookup"><span data-stu-id="1a327-107">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="1a327-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="1a327-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="1a327-109">\[в \] адресе результатов операции.</span><span class="sxs-lookup"><span data-stu-id="1a327-109">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="1a327-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="1a327-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="1a327-111">\[в \] компонентах, сравниваемых с *src1*.</span><span class="sxs-lookup"><span data-stu-id="1a327-111">\[in\] The components to compare to *src1*.</span></span><br/>         |
| <span data-ttu-id="1a327-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="1a327-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="1a327-113">\[в \] компонентах, сравниваемых с *src0*.</span><span class="sxs-lookup"><span data-stu-id="1a327-113">\[in\] The components to compare to *src0*.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="1a327-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="1a327-114">Remarks</span></span>

<span data-ttu-id="1a327-115">Эта инструкция выполняет сравнение с плавающей запятой двойной точности (*src0*  <  *src1*) для каждого компонента и записывает результат в *dest*.</span><span class="sxs-lookup"><span data-stu-id="1a327-115">This instruction performs the double-precision floating-point comparison (*src0* < *src1*) for each component and writes the result to *dest*.</span></span>

<span data-ttu-id="1a327-116">Если сравнение истинно, то для этого компонента возвращается 32-бит 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="1a327-116">If the comparison is true, then 32-bit 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="1a327-117">В противном случае возвращается 32-bit 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="1a327-117">Otherwise 32-bit 0x00000000 is returned.</span></span>

<span data-ttu-id="1a327-118">Сравнение с NaN возвращает false.</span><span class="sxs-lookup"><span data-stu-id="1a327-118">Comparison with NaN returns false.</span></span>

<span data-ttu-id="1a327-119">Допустимые маски *приемников* — это один или два компонента.</span><span class="sxs-lookup"><span data-stu-id="1a327-119">The valid *dest* masks are any one or two components.</span></span> <span data-ttu-id="1a327-120">Это:. x,. y,. z,. w,. XY,. КСЗ,. КСВ,. из,. Ив,. ZW первый компонент- *приемник* в маске получает 32-разрядный результат для первого двойного сравнения.</span><span class="sxs-lookup"><span data-stu-id="1a327-120">That is: .x, .y, .z, .w, .xy, .xz, .xw, .yz, .yw, .zw The first *dest* component in the mask receives the 32-bit result for the first double comparison.</span></span> <span data-ttu-id="1a327-121">Второй компонент в маске (при наличии) получает 32-разрядный результат для второго двойного сравнения.</span><span class="sxs-lookup"><span data-stu-id="1a327-121">The second component in the mask (if present) receives the 32-bit result for the second double comparison.</span></span>

<span data-ttu-id="1a327-122">Допустимыми свиззлес для параметров источника являются. ксизв,. ксикси,. звкси,. звзв.</span><span class="sxs-lookup"><span data-stu-id="1a327-122">The valid swizzles for the source parameters are .xyzw, .xyxy, .zwxy, .zwzw.</span></span> <span data-ttu-id="1a327-123">Следующие сопоставления *src* — это POST-свиззле:</span><span class="sxs-lookup"><span data-stu-id="1a327-123">The following *src* mappings are post-swizzle:</span></span>

-   <span data-ttu-id="1a327-124">*src0* — это двойное vec2 в (x 32LSB, y 32MSB) и (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="1a327-124">*src0* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>
-   <span data-ttu-id="1a327-125">*src1* — это двойное vec2 в (x 32LSB, y 32MSB) и (z 32LSB, w 32MSB).</span><span class="sxs-lookup"><span data-stu-id="1a327-125">*src1* is a double vec2 across (x 32LSB, y 32MSB) and (z 32LSB, w 32MSB).</span></span>

<span data-ttu-id="1a327-126">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="1a327-126">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="1a327-127">Вершина</span><span class="sxs-lookup"><span data-stu-id="1a327-127">Vertex</span></span> | <span data-ttu-id="1a327-128">Поверхности</span><span class="sxs-lookup"><span data-stu-id="1a327-128">Hull</span></span> | <span data-ttu-id="1a327-129">Домен</span><span class="sxs-lookup"><span data-stu-id="1a327-129">Domain</span></span> | <span data-ttu-id="1a327-130">Геометрия</span><span class="sxs-lookup"><span data-stu-id="1a327-130">Geometry</span></span> | <span data-ttu-id="1a327-131">Пиксель</span><span class="sxs-lookup"><span data-stu-id="1a327-131">Pixel</span></span> | <span data-ttu-id="1a327-132">Вычисления</span><span class="sxs-lookup"><span data-stu-id="1a327-132">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="1a327-133">X</span><span class="sxs-lookup"><span data-stu-id="1a327-133">X</span></span>      | <span data-ttu-id="1a327-134">X</span><span class="sxs-lookup"><span data-stu-id="1a327-134">X</span></span>    | <span data-ttu-id="1a327-135">X</span><span class="sxs-lookup"><span data-stu-id="1a327-135">X</span></span>      | <span data-ttu-id="1a327-136">X</span><span class="sxs-lookup"><span data-stu-id="1a327-136">X</span></span>        | <span data-ttu-id="1a327-137">X</span><span class="sxs-lookup"><span data-stu-id="1a327-137">X</span></span>     | <span data-ttu-id="1a327-138">X</span><span class="sxs-lookup"><span data-stu-id="1a327-138">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1a327-139">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="1a327-139">Minimum Shader Model</span></span>

<span data-ttu-id="1a327-140">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="1a327-140">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="1a327-141">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="1a327-141">Shader Model</span></span>                                              | <span data-ttu-id="1a327-142">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="1a327-142">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1a327-143">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="1a327-143">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1a327-144">да</span><span class="sxs-lookup"><span data-stu-id="1a327-144">yes</span></span>       |
| [<span data-ttu-id="1a327-145">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="1a327-145">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1a327-146">Нет</span><span class="sxs-lookup"><span data-stu-id="1a327-146">no</span></span>        |
| [<span data-ttu-id="1a327-147">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="1a327-147">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1a327-148">Нет</span><span class="sxs-lookup"><span data-stu-id="1a327-148">no</span></span>        |
| [<span data-ttu-id="1a327-149">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1a327-149">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1a327-150">Нет</span><span class="sxs-lookup"><span data-stu-id="1a327-150">no</span></span>        |
| [<span data-ttu-id="1a327-151">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1a327-151">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1a327-152">Нет</span><span class="sxs-lookup"><span data-stu-id="1a327-152">no</span></span>        |
| [<span data-ttu-id="1a327-153">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1a327-153">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1a327-154">Нет</span><span class="sxs-lookup"><span data-stu-id="1a327-154">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1a327-155">См. также</span><span class="sxs-lookup"><span data-stu-id="1a327-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a327-156">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1a327-156">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





