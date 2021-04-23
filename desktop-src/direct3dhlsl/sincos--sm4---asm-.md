---
title: синкос (SM4-ASM)
description: Компонентная Sin (тета) и cos (тета) для тета в радианах.
ms.assetid: 81FDEC8F-2C1C-4C60-A6DA-699C798F8316
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2dd8fc3b011758f071cdcd273e34eb8a7f6421f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996863"
---
# <a name="sincos-sm4---asm"></a><span data-ttu-id="4a580-103">синкос (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="4a580-103">sincos (sm4 - asm)</span></span>

<span data-ttu-id="4a580-104">Компонентная Sin (тета) и cos (тета) для тета в радианах.</span><span class="sxs-lookup"><span data-stu-id="4a580-104">Component-wise sin(theta) and cos(theta) for theta in radians.</span></span>



| <span data-ttu-id="4a580-105">синкос \[ \_ \] дестсин \[ . Mask \] , десткос \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="4a580-105">sincos\[\_sat\] destSIN\[.mask\], destCOS\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------------------------------|



 



| <span data-ttu-id="4a580-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="4a580-106">Item</span></span>                                                                                               | <span data-ttu-id="4a580-107">Описание</span><span class="sxs-lookup"><span data-stu-id="4a580-107">Description</span></span>                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="4a580-108"><span id="destSIN"></span><span id="destsin"></span><span id="DESTSIN"></span>*дестсин*</span><span class="sxs-lookup"><span data-stu-id="4a580-108"><span id="destSIN"></span><span id="destsin"></span><span id="DESTSIN"></span>*destSIN*</span></span><br/> | <span data-ttu-id="4a580-109">\[в \] адресе Sin (*src0*), вычисленном для каждого компонента.</span><span class="sxs-lookup"><span data-stu-id="4a580-109">\[in\] The address of sin(*src0*), computed per component.</span></span><br/> |
| <span data-ttu-id="4a580-110"><span id="destCOS"></span><span id="destcos"></span><span id="DESTCOS"></span>*десткос*</span><span class="sxs-lookup"><span data-stu-id="4a580-110"><span id="destCOS"></span><span id="destcos"></span><span id="DESTCOS"></span>*destCOS*</span></span><br/> | <span data-ttu-id="4a580-111">\[в \] адресе cos (*src0*), вычисленном для каждого компонента.</span><span class="sxs-lookup"><span data-stu-id="4a580-111">\[in\] The address of cos(*src0*), computed per component.</span></span><br/> |
| <span data-ttu-id="4a580-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="4a580-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                    | <span data-ttu-id="4a580-113">\[в \] компонентах, для которых вычисляются Sin и COS.</span><span class="sxs-lookup"><span data-stu-id="4a580-113">\[in\] The components for which to compute sin and cos.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="4a580-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="4a580-114">Remarks</span></span>

<span data-ttu-id="4a580-115">Если результат не требуется, можно указать *дестсин* и *десткос* как NULL вместо указания регистра.</span><span class="sxs-lookup"><span data-stu-id="4a580-115">If the result is not needed, you can specify *destSIN* and *destCOS* as NULL instead of specifying a register.</span></span>

<span data-ttu-id="4a580-116">Значения тета могут быть любыми значениями с плавающей запятой в стандарте IEEE 32.</span><span class="sxs-lookup"><span data-stu-id="4a580-116">Theta values can be any IEEE 32-bit floating point values.</span></span>

<span data-ttu-id="4a580-117">Максимальная абсолютная ошибка — 0,0008 в интервале от-100 \* Pi до + 100 \* Pi.</span><span class="sxs-lookup"><span data-stu-id="4a580-117">The maximum absolute error is 0.0008 in the interval from -100\*Pi to +100\*Pi.</span></span>

<span data-ttu-id="4a580-118">В следующей таблице показаны результаты, полученные при выполнении инструкции с различными классами чисел.</span><span class="sxs-lookup"><span data-stu-id="4a580-118">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>

<span data-ttu-id="4a580-119">F означает ограничение по настоящему вещественному числу.</span><span class="sxs-lookup"><span data-stu-id="4a580-119">F means finite-real number.</span></span>



|             |          |              |             |        |        |             |              |          |         |
|-------------|----------|--------------|-------------|--------|--------|-------------|--------------|----------|---------|
| <span data-ttu-id="4a580-120">**src**</span><span class="sxs-lookup"><span data-stu-id="4a580-120">**src**</span></span>     | <span data-ttu-id="4a580-121">**-INF**</span><span class="sxs-lookup"><span data-stu-id="4a580-121">**-inf**</span></span> | <span data-ttu-id="4a580-122">**-F**</span><span class="sxs-lookup"><span data-stu-id="4a580-122">**-F**</span></span>       | <span data-ttu-id="4a580-123">**— денорма**</span><span class="sxs-lookup"><span data-stu-id="4a580-123">**-denorm**</span></span> | <span data-ttu-id="4a580-124">**-0**</span><span class="sxs-lookup"><span data-stu-id="4a580-124">**-0**</span></span> | <span data-ttu-id="4a580-125">**+0**</span><span class="sxs-lookup"><span data-stu-id="4a580-125">**+0**</span></span> | <span data-ttu-id="4a580-126">**+ денорма**</span><span class="sxs-lookup"><span data-stu-id="4a580-126">**+denorm**</span></span> | <span data-ttu-id="4a580-127">**+ F**</span><span class="sxs-lookup"><span data-stu-id="4a580-127">**+F**</span></span>       | <span data-ttu-id="4a580-128">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="4a580-128">**+inf**</span></span> | <span data-ttu-id="4a580-129">**Не число**</span><span class="sxs-lookup"><span data-stu-id="4a580-129">**NaN**</span></span> |
| <span data-ttu-id="4a580-130">**дестсин**</span><span class="sxs-lookup"><span data-stu-id="4a580-130">**destSIN**</span></span> | <span data-ttu-id="4a580-131">не число</span><span class="sxs-lookup"><span data-stu-id="4a580-131">NaN</span></span>      | <span data-ttu-id="4a580-132">\[от-1 до + 1\]</span><span class="sxs-lookup"><span data-stu-id="4a580-132">\[-1 to +1\]</span></span> | <span data-ttu-id="4a580-133">-0</span><span class="sxs-lookup"><span data-stu-id="4a580-133">-0</span></span>          | <span data-ttu-id="4a580-134">-0</span><span class="sxs-lookup"><span data-stu-id="4a580-134">-0</span></span>     | <span data-ttu-id="4a580-135">+0</span><span class="sxs-lookup"><span data-stu-id="4a580-135">+0</span></span>     | <span data-ttu-id="4a580-136">+0</span><span class="sxs-lookup"><span data-stu-id="4a580-136">+0</span></span>          | <span data-ttu-id="4a580-137">\[от-1 до + 1\]</span><span class="sxs-lookup"><span data-stu-id="4a580-137">\[-1 to +1\]</span></span> | <span data-ttu-id="4a580-138">Не число</span><span class="sxs-lookup"><span data-stu-id="4a580-138">NaN</span></span>      | <span data-ttu-id="4a580-139">Не число</span><span class="sxs-lookup"><span data-stu-id="4a580-139">NaN</span></span>     |
| <span data-ttu-id="4a580-140">**десткос**</span><span class="sxs-lookup"><span data-stu-id="4a580-140">**destCOS**</span></span> | <span data-ttu-id="4a580-141">не число</span><span class="sxs-lookup"><span data-stu-id="4a580-141">NaN</span></span>      | <span data-ttu-id="4a580-142">\[от-1 до + 1\]</span><span class="sxs-lookup"><span data-stu-id="4a580-142">\[-1 to +1\]</span></span> | <span data-ttu-id="4a580-143">+1</span><span class="sxs-lookup"><span data-stu-id="4a580-143">+1</span></span>          | <span data-ttu-id="4a580-144">+1</span><span class="sxs-lookup"><span data-stu-id="4a580-144">+1</span></span>     | <span data-ttu-id="4a580-145">+1</span><span class="sxs-lookup"><span data-stu-id="4a580-145">+1</span></span>     | <span data-ttu-id="4a580-146">+1</span><span class="sxs-lookup"><span data-stu-id="4a580-146">+1</span></span>          | <span data-ttu-id="4a580-147">\[от-1 до + 1\]</span><span class="sxs-lookup"><span data-stu-id="4a580-147">\[-1 to +1\]</span></span> | <span data-ttu-id="4a580-148">Не число</span><span class="sxs-lookup"><span data-stu-id="4a580-148">NaN</span></span>      | <span data-ttu-id="4a580-149">Не число</span><span class="sxs-lookup"><span data-stu-id="4a580-149">NaN</span></span>     |



 

<span data-ttu-id="4a580-150">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="4a580-150">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="4a580-151">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="4a580-151">Vertex Shader</span></span> | <span data-ttu-id="4a580-152">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="4a580-152">Geometry Shader</span></span> | <span data-ttu-id="4a580-153">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="4a580-153">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="4a580-154">x</span><span class="sxs-lookup"><span data-stu-id="4a580-154">x</span></span>             | <span data-ttu-id="4a580-155">x</span><span class="sxs-lookup"><span data-stu-id="4a580-155">x</span></span>               | <span data-ttu-id="4a580-156">x</span><span class="sxs-lookup"><span data-stu-id="4a580-156">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4a580-157">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="4a580-157">Minimum Shader Model</span></span>

<span data-ttu-id="4a580-158">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="4a580-158">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4a580-159">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="4a580-159">Shader Model</span></span>                                              | <span data-ttu-id="4a580-160">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="4a580-160">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="4a580-161">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="4a580-161">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="4a580-162">да</span><span class="sxs-lookup"><span data-stu-id="4a580-162">yes</span></span>       |
| [<span data-ttu-id="4a580-163">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="4a580-163">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="4a580-164">да</span><span class="sxs-lookup"><span data-stu-id="4a580-164">yes</span></span>       |
| [<span data-ttu-id="4a580-165">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="4a580-165">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4a580-166">да</span><span class="sxs-lookup"><span data-stu-id="4a580-166">yes</span></span>       |
| [<span data-ttu-id="4a580-167">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4a580-167">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4a580-168">Нет</span><span class="sxs-lookup"><span data-stu-id="4a580-168">no</span></span>        |
| [<span data-ttu-id="4a580-169">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4a580-169">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4a580-170">Нет</span><span class="sxs-lookup"><span data-stu-id="4a580-170">no</span></span>        |
| [<span data-ttu-id="4a580-171">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4a580-171">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4a580-172">Нет</span><span class="sxs-lookup"><span data-stu-id="4a580-172">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="4a580-173">См. также</span><span class="sxs-lookup"><span data-stu-id="4a580-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a580-174">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4a580-174">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





