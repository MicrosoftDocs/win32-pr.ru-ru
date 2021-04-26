---
title: log (SM4-ASM)
description: Базовый журнал на основе компонентов 2.
ms.assetid: 6D28864A-C2BA-44AF-9E78-7C2B34F5E462
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88e4b89b4dcc085cf4fd4fda762d96fb71271af2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998321"
---
# <a name="log-sm4---asm"></a><span data-ttu-id="2ece9-103">log (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="2ece9-103">log (sm4 - asm)</span></span>

<span data-ttu-id="2ece9-104">Базовый журнал на основе компонентов 2.</span><span class="sxs-lookup"><span data-stu-id="2ece9-104">Component-wise log base 2.</span></span>



| <span data-ttu-id="2ece9-105">вести журнал о \[ \_ \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . свиззле</span><span class="sxs-lookup"><span data-stu-id="2ece9-105">log\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle</span></span> |
|----------------------------------------------------------|



 



| <span data-ttu-id="2ece9-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="2ece9-106">Item</span></span>                                                            | <span data-ttu-id="2ece9-107">Описание</span><span class="sxs-lookup"><span data-stu-id="2ece9-107">Description</span></span>                                                                                |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ece9-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="2ece9-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="2ece9-109">\[в \] адресе результата операции.</span><span class="sxs-lookup"><span data-stu-id="2ece9-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="2ece9-110">dest = log2 (src0)</span><span class="sxs-lookup"><span data-stu-id="2ece9-110">dest = log2(src0)</span></span><br/> |
| <span data-ttu-id="2ece9-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="2ece9-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="2ece9-112">\[в \] значении для операции.</span><span class="sxs-lookup"><span data-stu-id="2ece9-112">\[in\] The value for the operation.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="2ece9-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="2ece9-113">Remarks</span></span>

### <a name="restrictions"></a><span data-ttu-id="2ece9-114">Ограничения</span><span class="sxs-lookup"><span data-stu-id="2ece9-114">Restrictions</span></span>

-   <span data-ttu-id="2ece9-115">Соответствует теории ограничений.</span><span class="sxs-lookup"><span data-stu-id="2ece9-115">Follows limit theory.</span></span>
-   <span data-ttu-id="2ece9-116">Погрешность ошибок: Если *src0* имеет значение \[ 0,5.. 2 \] , абсолуе ошибка не должна превышать 2-21.</span><span class="sxs-lookup"><span data-stu-id="2ece9-116">Error tolerance: If *src0* is \[0.5..2\], absolue error must be no more than 2-21.</span></span> <span data-ttu-id="2ece9-117">Если *src0* имеет значение (0.0,5) или (2.. + inf \] , относительная ошибка не должна превышать 2-21.</span><span class="sxs-lookup"><span data-stu-id="2ece9-117">If *src0* is (0..0.5) or (2..+INF\], relative error must be no more than 2-21.</span></span>

<span data-ttu-id="2ece9-118">В следующей таблице показаны результаты, полученные при выполнении инструкции с различными классами чисел, предполагая, что ни переполнение, ни потеря точности не происходит.</span><span class="sxs-lookup"><span data-stu-id="2ece9-118">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="2ece9-119">F означает ограничение по настоящему вещественному числу.</span><span class="sxs-lookup"><span data-stu-id="2ece9-119">F means finite-real number.</span></span>



| <span data-ttu-id="2ece9-120">**src**</span><span class="sxs-lookup"><span data-stu-id="2ece9-120">**src**</span></span>  | <span data-ttu-id="2ece9-121">**-INF**</span><span class="sxs-lookup"><span data-stu-id="2ece9-121">**-inf**</span></span> | <span data-ttu-id="2ece9-122">**-F**</span><span class="sxs-lookup"><span data-stu-id="2ece9-122">**-F**</span></span> | <span data-ttu-id="2ece9-123">**— денорма**</span><span class="sxs-lookup"><span data-stu-id="2ece9-123">**-denorm**</span></span> | <span data-ttu-id="2ece9-124">**-0**</span><span class="sxs-lookup"><span data-stu-id="2ece9-124">**-0**</span></span> | <span data-ttu-id="2ece9-125">**+0**</span><span class="sxs-lookup"><span data-stu-id="2ece9-125">**+0**</span></span> | <span data-ttu-id="2ece9-126">**+ денорма**</span><span class="sxs-lookup"><span data-stu-id="2ece9-126">**+denorm**</span></span> | <span data-ttu-id="2ece9-127">**+ F**</span><span class="sxs-lookup"><span data-stu-id="2ece9-127">**+F**</span></span> | <span data-ttu-id="2ece9-128">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="2ece9-128">**+inf**</span></span> | <span data-ttu-id="2ece9-129">**Не число**</span><span class="sxs-lookup"><span data-stu-id="2ece9-129">**NaN**</span></span> |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="2ece9-130">**dest**</span><span class="sxs-lookup"><span data-stu-id="2ece9-130">**dest**</span></span> | <span data-ttu-id="2ece9-131">Не число</span><span class="sxs-lookup"><span data-stu-id="2ece9-131">NaN</span></span>      | <span data-ttu-id="2ece9-132">Не число</span><span class="sxs-lookup"><span data-stu-id="2ece9-132">NaN</span></span>    | <span data-ttu-id="2ece9-133">-inf</span><span class="sxs-lookup"><span data-stu-id="2ece9-133">-inf</span></span>        | <span data-ttu-id="2ece9-134">-inf</span><span class="sxs-lookup"><span data-stu-id="2ece9-134">-inf</span></span>   | <span data-ttu-id="2ece9-135">-inf</span><span class="sxs-lookup"><span data-stu-id="2ece9-135">-inf</span></span>   | <span data-ttu-id="2ece9-136">-inf</span><span class="sxs-lookup"><span data-stu-id="2ece9-136">-inf</span></span>        | <span data-ttu-id="2ece9-137">C</span><span class="sxs-lookup"><span data-stu-id="2ece9-137">F</span></span>      | <span data-ttu-id="2ece9-138">+inf</span><span class="sxs-lookup"><span data-stu-id="2ece9-138">+inf</span></span>     | <span data-ttu-id="2ece9-139">не число</span><span class="sxs-lookup"><span data-stu-id="2ece9-139">NaN</span></span>     |



 

<span data-ttu-id="2ece9-140">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="2ece9-140">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2ece9-141">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="2ece9-141">Vertex Shader</span></span> | <span data-ttu-id="2ece9-142">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="2ece9-142">Geometry Shader</span></span> | <span data-ttu-id="2ece9-143">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="2ece9-143">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="2ece9-144">x</span><span class="sxs-lookup"><span data-stu-id="2ece9-144">x</span></span>             | <span data-ttu-id="2ece9-145">x</span><span class="sxs-lookup"><span data-stu-id="2ece9-145">x</span></span>               | <span data-ttu-id="2ece9-146">x</span><span class="sxs-lookup"><span data-stu-id="2ece9-146">x</span></span>            |



 

### <a name="minimum-shader-model"></a><span data-ttu-id="2ece9-147">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="2ece9-147">Minimum Shader Model</span></span>

<span data-ttu-id="2ece9-148">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="2ece9-148">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2ece9-149">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="2ece9-149">Shader Model</span></span>                                              | <span data-ttu-id="2ece9-150">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="2ece9-150">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2ece9-151">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="2ece9-151">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2ece9-152">да</span><span class="sxs-lookup"><span data-stu-id="2ece9-152">yes</span></span>       |
| [<span data-ttu-id="2ece9-153">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="2ece9-153">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2ece9-154">да</span><span class="sxs-lookup"><span data-stu-id="2ece9-154">yes</span></span>       |
| [<span data-ttu-id="2ece9-155">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="2ece9-155">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2ece9-156">да</span><span class="sxs-lookup"><span data-stu-id="2ece9-156">yes</span></span>       |
| [<span data-ttu-id="2ece9-157">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2ece9-157">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2ece9-158">Нет</span><span class="sxs-lookup"><span data-stu-id="2ece9-158">no</span></span>        |
| [<span data-ttu-id="2ece9-159">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2ece9-159">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2ece9-160">Нет</span><span class="sxs-lookup"><span data-stu-id="2ece9-160">no</span></span>        |
| [<span data-ttu-id="2ece9-161">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2ece9-161">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2ece9-162">Нет</span><span class="sxs-lookup"><span data-stu-id="2ece9-162">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2ece9-163">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="2ece9-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ece9-164">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2ece9-164">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





