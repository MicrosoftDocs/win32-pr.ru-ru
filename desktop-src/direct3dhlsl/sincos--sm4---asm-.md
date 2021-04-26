---
title: синкос (SM4-ASM)
description: Компонентная Sin (тета) и cos (тета) для тета в радианах.
ms.assetid: 81FDEC8F-2C1C-4C60-A6DA-699C798F8316
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c03118ff9a1fc2d958eaa6eb1a550a6dbf672a2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997021"
---
# <a name="sincos-sm4---asm"></a><span data-ttu-id="0204f-103">синкос (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="0204f-103">sincos (sm4 - asm)</span></span>

<span data-ttu-id="0204f-104">Компонентная Sin (тета) и cos (тета) для тета в радианах.</span><span class="sxs-lookup"><span data-stu-id="0204f-104">Component-wise sin(theta) and cos(theta) for theta in radians.</span></span>



| <span data-ttu-id="0204f-105">синкос \[ \_ \] дестсин \[ . Mask \] , десткос \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="0204f-105">sincos\[\_sat\] destSIN\[.mask\], destCOS\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------------------------------|



 



| <span data-ttu-id="0204f-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="0204f-106">Item</span></span>                                                                                               | <span data-ttu-id="0204f-107">Описание</span><span class="sxs-lookup"><span data-stu-id="0204f-107">Description</span></span>                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="0204f-108"><span id="destSIN"></span><span id="destsin"></span><span id="DESTSIN"></span>*дестсин*</span><span class="sxs-lookup"><span data-stu-id="0204f-108"><span id="destSIN"></span><span id="destsin"></span><span id="DESTSIN"></span>*destSIN*</span></span><br/> | <span data-ttu-id="0204f-109">\[в \] адресе Sin (*src0*), вычисленном для каждого компонента.</span><span class="sxs-lookup"><span data-stu-id="0204f-109">\[in\] The address of sin(*src0*), computed per component.</span></span><br/> |
| <span data-ttu-id="0204f-110"><span id="destCOS"></span><span id="destcos"></span><span id="DESTCOS"></span>*десткос*</span><span class="sxs-lookup"><span data-stu-id="0204f-110"><span id="destCOS"></span><span id="destcos"></span><span id="DESTCOS"></span>*destCOS*</span></span><br/> | <span data-ttu-id="0204f-111">\[в \] адресе cos (*src0*), вычисленном для каждого компонента.</span><span class="sxs-lookup"><span data-stu-id="0204f-111">\[in\] The address of cos(*src0*), computed per component.</span></span><br/> |
| <span data-ttu-id="0204f-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="0204f-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                    | <span data-ttu-id="0204f-113">\[в \] компонентах, для которых вычисляются Sin и COS.</span><span class="sxs-lookup"><span data-stu-id="0204f-113">\[in\] The components for which to compute sin and cos.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="0204f-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="0204f-114">Remarks</span></span>

<span data-ttu-id="0204f-115">Если результат не требуется, можно указать *дестсин* и *десткос* как NULL вместо указания регистра.</span><span class="sxs-lookup"><span data-stu-id="0204f-115">If the result is not needed, you can specify *destSIN* and *destCOS* as NULL instead of specifying a register.</span></span>

<span data-ttu-id="0204f-116">Значения тета могут быть любыми значениями с плавающей запятой в стандарте IEEE 32.</span><span class="sxs-lookup"><span data-stu-id="0204f-116">Theta values can be any IEEE 32-bit floating point values.</span></span>

<span data-ttu-id="0204f-117">Максимальная абсолютная ошибка — 0,0008 в интервале от-100 \* Pi до + 100 \* Pi.</span><span class="sxs-lookup"><span data-stu-id="0204f-117">The maximum absolute error is 0.0008 in the interval from -100\*Pi to +100\*Pi.</span></span>

<span data-ttu-id="0204f-118">В следующей таблице показаны результаты, полученные при выполнении инструкции с различными классами чисел.</span><span class="sxs-lookup"><span data-stu-id="0204f-118">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>

<span data-ttu-id="0204f-119">F означает ограничение по настоящему вещественному числу.</span><span class="sxs-lookup"><span data-stu-id="0204f-119">F means finite-real number.</span></span>



| <span data-ttu-id="0204f-120">**src**</span><span class="sxs-lookup"><span data-stu-id="0204f-120">**src**</span></span>     | <span data-ttu-id="0204f-121">**-INF**</span><span class="sxs-lookup"><span data-stu-id="0204f-121">**-inf**</span></span> | <span data-ttu-id="0204f-122">**-F**</span><span class="sxs-lookup"><span data-stu-id="0204f-122">**-F**</span></span>       | <span data-ttu-id="0204f-123">**— денорма**</span><span class="sxs-lookup"><span data-stu-id="0204f-123">**-denorm**</span></span> | <span data-ttu-id="0204f-124">**-0**</span><span class="sxs-lookup"><span data-stu-id="0204f-124">**-0**</span></span> | <span data-ttu-id="0204f-125">**+0**</span><span class="sxs-lookup"><span data-stu-id="0204f-125">**+0**</span></span> | <span data-ttu-id="0204f-126">**+ денорма**</span><span class="sxs-lookup"><span data-stu-id="0204f-126">**+denorm**</span></span> | <span data-ttu-id="0204f-127">**+ F**</span><span class="sxs-lookup"><span data-stu-id="0204f-127">**+F**</span></span>       | <span data-ttu-id="0204f-128">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="0204f-128">**+inf**</span></span> | <span data-ttu-id="0204f-129">**Не число**</span><span class="sxs-lookup"><span data-stu-id="0204f-129">**NaN**</span></span> |
|-------------|----------|--------------|-------------|--------|--------|-------------|--------------|----------|---------|
| <span data-ttu-id="0204f-130">**дестсин**</span><span class="sxs-lookup"><span data-stu-id="0204f-130">**destSIN**</span></span> | <span data-ttu-id="0204f-131">не число</span><span class="sxs-lookup"><span data-stu-id="0204f-131">NaN</span></span>      | <span data-ttu-id="0204f-132">\[от-1 до + 1\]</span><span class="sxs-lookup"><span data-stu-id="0204f-132">\[-1 to +1\]</span></span> | <span data-ttu-id="0204f-133">-0</span><span class="sxs-lookup"><span data-stu-id="0204f-133">-0</span></span>          | <span data-ttu-id="0204f-134">-0</span><span class="sxs-lookup"><span data-stu-id="0204f-134">-0</span></span>     | <span data-ttu-id="0204f-135">+0</span><span class="sxs-lookup"><span data-stu-id="0204f-135">+0</span></span>     | <span data-ttu-id="0204f-136">+0</span><span class="sxs-lookup"><span data-stu-id="0204f-136">+0</span></span>          | <span data-ttu-id="0204f-137">\[от-1 до + 1\]</span><span class="sxs-lookup"><span data-stu-id="0204f-137">\[-1 to +1\]</span></span> | <span data-ttu-id="0204f-138">Не число</span><span class="sxs-lookup"><span data-stu-id="0204f-138">NaN</span></span>      | <span data-ttu-id="0204f-139">Не число</span><span class="sxs-lookup"><span data-stu-id="0204f-139">NaN</span></span>     |
| <span data-ttu-id="0204f-140">**десткос**</span><span class="sxs-lookup"><span data-stu-id="0204f-140">**destCOS**</span></span> | <span data-ttu-id="0204f-141">не число</span><span class="sxs-lookup"><span data-stu-id="0204f-141">NaN</span></span>      | <span data-ttu-id="0204f-142">\[от-1 до + 1\]</span><span class="sxs-lookup"><span data-stu-id="0204f-142">\[-1 to +1\]</span></span> | <span data-ttu-id="0204f-143">+1</span><span class="sxs-lookup"><span data-stu-id="0204f-143">+1</span></span>          | <span data-ttu-id="0204f-144">+1</span><span class="sxs-lookup"><span data-stu-id="0204f-144">+1</span></span>     | <span data-ttu-id="0204f-145">+1</span><span class="sxs-lookup"><span data-stu-id="0204f-145">+1</span></span>     | <span data-ttu-id="0204f-146">+1</span><span class="sxs-lookup"><span data-stu-id="0204f-146">+1</span></span>          | <span data-ttu-id="0204f-147">\[от-1 до + 1\]</span><span class="sxs-lookup"><span data-stu-id="0204f-147">\[-1 to +1\]</span></span> | <span data-ttu-id="0204f-148">Не число</span><span class="sxs-lookup"><span data-stu-id="0204f-148">NaN</span></span>      | <span data-ttu-id="0204f-149">Не число</span><span class="sxs-lookup"><span data-stu-id="0204f-149">NaN</span></span>     |



 

<span data-ttu-id="0204f-150">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="0204f-150">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="0204f-151">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="0204f-151">Vertex Shader</span></span> | <span data-ttu-id="0204f-152">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="0204f-152">Geometry Shader</span></span> | <span data-ttu-id="0204f-153">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="0204f-153">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="0204f-154">x</span><span class="sxs-lookup"><span data-stu-id="0204f-154">x</span></span>             | <span data-ttu-id="0204f-155">x</span><span class="sxs-lookup"><span data-stu-id="0204f-155">x</span></span>               | <span data-ttu-id="0204f-156">x</span><span class="sxs-lookup"><span data-stu-id="0204f-156">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0204f-157">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="0204f-157">Minimum Shader Model</span></span>

<span data-ttu-id="0204f-158">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="0204f-158">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0204f-159">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="0204f-159">Shader Model</span></span>                                              | <span data-ttu-id="0204f-160">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="0204f-160">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0204f-161">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="0204f-161">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="0204f-162">да</span><span class="sxs-lookup"><span data-stu-id="0204f-162">yes</span></span>       |
| [<span data-ttu-id="0204f-163">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="0204f-163">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="0204f-164">да</span><span class="sxs-lookup"><span data-stu-id="0204f-164">yes</span></span>       |
| [<span data-ttu-id="0204f-165">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="0204f-165">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0204f-166">да</span><span class="sxs-lookup"><span data-stu-id="0204f-166">yes</span></span>       |
| [<span data-ttu-id="0204f-167">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0204f-167">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0204f-168">Нет</span><span class="sxs-lookup"><span data-stu-id="0204f-168">no</span></span>        |
| [<span data-ttu-id="0204f-169">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0204f-169">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0204f-170">Нет</span><span class="sxs-lookup"><span data-stu-id="0204f-170">no</span></span>        |
| [<span data-ttu-id="0204f-171">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0204f-171">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0204f-172">Нет</span><span class="sxs-lookup"><span data-stu-id="0204f-172">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="0204f-173">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="0204f-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0204f-174">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0204f-174">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





