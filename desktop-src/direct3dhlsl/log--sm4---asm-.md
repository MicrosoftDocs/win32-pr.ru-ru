---
title: log (SM4-ASM)
description: Базовый журнал на основе компонентов 2.
ms.assetid: 6D28864A-C2BA-44AF-9E78-7C2B34F5E462
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf99949e278ca302543437da346188b690789604
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104069354"
---
# <a name="log-sm4---asm"></a><span data-ttu-id="ecd47-103">log (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="ecd47-103">log (sm4 - asm)</span></span>

<span data-ttu-id="ecd47-104">Базовый журнал на основе компонентов 2.</span><span class="sxs-lookup"><span data-stu-id="ecd47-104">Component-wise log base 2.</span></span>



| <span data-ttu-id="ecd47-105">вести журнал о \[ \_ \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . свиззле</span><span class="sxs-lookup"><span data-stu-id="ecd47-105">log\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle</span></span> |
|----------------------------------------------------------|



 



| <span data-ttu-id="ecd47-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="ecd47-106">Item</span></span>                                                            | <span data-ttu-id="ecd47-107">Описание</span><span class="sxs-lookup"><span data-stu-id="ecd47-107">Description</span></span>                                                                                |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecd47-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="ecd47-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="ecd47-109">\[в \] адресе результата операции.</span><span class="sxs-lookup"><span data-stu-id="ecd47-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="ecd47-110">dest = log2 (src0)</span><span class="sxs-lookup"><span data-stu-id="ecd47-110">dest = log2(src0)</span></span><br/> |
| <span data-ttu-id="ecd47-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="ecd47-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="ecd47-112">\[в \] значении для операции.</span><span class="sxs-lookup"><span data-stu-id="ecd47-112">\[in\] The value for the operation.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="ecd47-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="ecd47-113">Remarks</span></span>

### <a name="restrictions"></a><span data-ttu-id="ecd47-114">Ограничения</span><span class="sxs-lookup"><span data-stu-id="ecd47-114">Restrictions</span></span>

-   <span data-ttu-id="ecd47-115">Соответствует теории ограничений.</span><span class="sxs-lookup"><span data-stu-id="ecd47-115">Follows limit theory.</span></span>
-   <span data-ttu-id="ecd47-116">Погрешность ошибок: Если *src0* имеет значение \[ 0,5.. 2 \] , абсолуе ошибка не должна превышать 2-21.</span><span class="sxs-lookup"><span data-stu-id="ecd47-116">Error tolerance: If *src0* is \[0.5..2\], absolue error must be no more than 2-21.</span></span> <span data-ttu-id="ecd47-117">Если *src0* имеет значение (0.0,5) или (2.. + inf \] , относительная ошибка не должна превышать 2-21.</span><span class="sxs-lookup"><span data-stu-id="ecd47-117">If *src0* is (0..0.5) or (2..+INF\], relative error must be no more than 2-21.</span></span>

<span data-ttu-id="ecd47-118">В следующей таблице показаны результаты, полученные при выполнении инструкции с различными классами чисел, предполагая, что ни переполнение, ни потеря точности не происходит.</span><span class="sxs-lookup"><span data-stu-id="ecd47-118">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="ecd47-119">F означает ограничение по настоящему вещественному числу.</span><span class="sxs-lookup"><span data-stu-id="ecd47-119">F means finite-real number.</span></span>



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="ecd47-120">**src**</span><span class="sxs-lookup"><span data-stu-id="ecd47-120">**src**</span></span>  | <span data-ttu-id="ecd47-121">**-INF**</span><span class="sxs-lookup"><span data-stu-id="ecd47-121">**-inf**</span></span> | <span data-ttu-id="ecd47-122">**-F**</span><span class="sxs-lookup"><span data-stu-id="ecd47-122">**-F**</span></span> | <span data-ttu-id="ecd47-123">**— денорма**</span><span class="sxs-lookup"><span data-stu-id="ecd47-123">**-denorm**</span></span> | <span data-ttu-id="ecd47-124">**-0**</span><span class="sxs-lookup"><span data-stu-id="ecd47-124">**-0**</span></span> | <span data-ttu-id="ecd47-125">**+0**</span><span class="sxs-lookup"><span data-stu-id="ecd47-125">**+0**</span></span> | <span data-ttu-id="ecd47-126">**+ денорма**</span><span class="sxs-lookup"><span data-stu-id="ecd47-126">**+denorm**</span></span> | <span data-ttu-id="ecd47-127">**+ F**</span><span class="sxs-lookup"><span data-stu-id="ecd47-127">**+F**</span></span> | <span data-ttu-id="ecd47-128">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="ecd47-128">**+inf**</span></span> | <span data-ttu-id="ecd47-129">**Не число**</span><span class="sxs-lookup"><span data-stu-id="ecd47-129">**NaN**</span></span> |
| <span data-ttu-id="ecd47-130">**dest**</span><span class="sxs-lookup"><span data-stu-id="ecd47-130">**dest**</span></span> | <span data-ttu-id="ecd47-131">Не число</span><span class="sxs-lookup"><span data-stu-id="ecd47-131">NaN</span></span>      | <span data-ttu-id="ecd47-132">Не число</span><span class="sxs-lookup"><span data-stu-id="ecd47-132">NaN</span></span>    | <span data-ttu-id="ecd47-133">-inf</span><span class="sxs-lookup"><span data-stu-id="ecd47-133">-inf</span></span>        | <span data-ttu-id="ecd47-134">-inf</span><span class="sxs-lookup"><span data-stu-id="ecd47-134">-inf</span></span>   | <span data-ttu-id="ecd47-135">-inf</span><span class="sxs-lookup"><span data-stu-id="ecd47-135">-inf</span></span>   | <span data-ttu-id="ecd47-136">-inf</span><span class="sxs-lookup"><span data-stu-id="ecd47-136">-inf</span></span>        | <span data-ttu-id="ecd47-137">C</span><span class="sxs-lookup"><span data-stu-id="ecd47-137">F</span></span>      | <span data-ttu-id="ecd47-138">+inf</span><span class="sxs-lookup"><span data-stu-id="ecd47-138">+inf</span></span>     | <span data-ttu-id="ecd47-139">не число</span><span class="sxs-lookup"><span data-stu-id="ecd47-139">NaN</span></span>     |



 

<span data-ttu-id="ecd47-140">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="ecd47-140">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ecd47-141">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="ecd47-141">Vertex Shader</span></span> | <span data-ttu-id="ecd47-142">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="ecd47-142">Geometry Shader</span></span> | <span data-ttu-id="ecd47-143">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="ecd47-143">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="ecd47-144">x</span><span class="sxs-lookup"><span data-stu-id="ecd47-144">x</span></span>             | <span data-ttu-id="ecd47-145">x</span><span class="sxs-lookup"><span data-stu-id="ecd47-145">x</span></span>               | <span data-ttu-id="ecd47-146">x</span><span class="sxs-lookup"><span data-stu-id="ecd47-146">x</span></span>            |



 

### <a name="minimum-shader-model"></a><span data-ttu-id="ecd47-147">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ecd47-147">Minimum Shader Model</span></span>

<span data-ttu-id="ecd47-148">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="ecd47-148">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ecd47-149">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ecd47-149">Shader Model</span></span>                                              | <span data-ttu-id="ecd47-150">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="ecd47-150">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ecd47-151">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="ecd47-151">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ecd47-152">да</span><span class="sxs-lookup"><span data-stu-id="ecd47-152">yes</span></span>       |
| [<span data-ttu-id="ecd47-153">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="ecd47-153">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ecd47-154">да</span><span class="sxs-lookup"><span data-stu-id="ecd47-154">yes</span></span>       |
| [<span data-ttu-id="ecd47-155">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="ecd47-155">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ecd47-156">да</span><span class="sxs-lookup"><span data-stu-id="ecd47-156">yes</span></span>       |
| [<span data-ttu-id="ecd47-157">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ecd47-157">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ecd47-158">Нет</span><span class="sxs-lookup"><span data-stu-id="ecd47-158">no</span></span>        |
| [<span data-ttu-id="ecd47-159">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ecd47-159">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ecd47-160">Нет</span><span class="sxs-lookup"><span data-stu-id="ecd47-160">no</span></span>        |
| [<span data-ttu-id="ecd47-161">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ecd47-161">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ecd47-162">Нет</span><span class="sxs-lookup"><span data-stu-id="ecd47-162">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ecd47-163">См. также</span><span class="sxs-lookup"><span data-stu-id="ecd47-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ecd47-164">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ecd47-164">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





