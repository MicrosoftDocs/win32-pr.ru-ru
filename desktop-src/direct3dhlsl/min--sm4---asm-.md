---
title: min (SM4-ASM)
description: Минимальное количество перемещаемых компонентов.
ms.assetid: 8EDD5503-76D5-4078-BFBA-1DA9260C6E68
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8791589b77edc66eeab4b48f10f4a9b16b5cb2d9
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993901"
---
# <a name="min-sm4---asm"></a><span data-ttu-id="4133f-103">min (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="4133f-103">min (sm4 - asm)</span></span>

<span data-ttu-id="4133f-104">Минимальное количество перемещаемых компонентов.</span><span class="sxs-lookup"><span data-stu-id="4133f-104">Component-wise float minimum.</span></span>



| <span data-ttu-id="4133f-105">мин \[ \_ \] \[ . \] , \[ - \] src0 \[ \_ ABS. \] \[ свиззле \] , \[ - \] src1 \[ \_ ABS \] \[ . свиззле \] ,</span><span class="sxs-lookup"><span data-stu-id="4133f-105">min\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\],</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="4133f-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="4133f-106">Item</span></span>                                                            | <span data-ttu-id="4133f-107">Описание</span><span class="sxs-lookup"><span data-stu-id="4133f-107">Description</span></span>                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4133f-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="4133f-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="4133f-109">\[в \] результате операции.</span><span class="sxs-lookup"><span data-stu-id="4133f-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="4133f-110">*конечный адрес*  =  *src0*  <  *src1* ?</span><span class="sxs-lookup"><span data-stu-id="4133f-110">*dest* = *src0* < *src1* ?</span></span> <span data-ttu-id="4133f-111">*src0* : *src1*</span><span class="sxs-lookup"><span data-stu-id="4133f-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="4133f-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="4133f-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="4133f-113">\[в \] компонентах, сравниваемых с *src1*.</span><span class="sxs-lookup"><span data-stu-id="4133f-113">\[in\] The components to compare to *src1*.</span></span><br/>                                                  |
| <span data-ttu-id="4133f-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="4133f-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="4133f-115">\[в \] компонентах, сравниваемых с *src0*.</span><span class="sxs-lookup"><span data-stu-id="4133f-115">\[in\] The components to compare to *src0*.</span></span><br/>                                                  |



 

## <a name="remarks"></a><span data-ttu-id="4133f-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="4133f-116">Remarks</span></span>

><span data-ttu-id="4133f-117">= используется вместо >, поэтому если min (x, y) = x, то Max (x, y) = y.</span><span class="sxs-lookup"><span data-stu-id="4133f-117">= is used instead of > so that if min(x,y) = x then max(x,y) = y.</span></span>

<span data-ttu-id="4133f-118">NaN имеет особую обработку.</span><span class="sxs-lookup"><span data-stu-id="4133f-118">NaN has special handling.</span></span> <span data-ttu-id="4133f-119">Если один исходный операнд равен NaN, то возвращается другой исходный операнд и выбирается для каждого компонента.</span><span class="sxs-lookup"><span data-stu-id="4133f-119">If one source operand is NaN, then the other source operand is returned and the choice is made per-component.</span></span> <span data-ttu-id="4133f-120">Если оба значения равны NaN, возвращается любое представление NaN.</span><span class="sxs-lookup"><span data-stu-id="4133f-120">If both are NaN, any NaN representation is returned.</span></span> <span data-ttu-id="4133f-121">Это соответствует новым правилам IEEE 754R.</span><span class="sxs-lookup"><span data-stu-id="4133f-121">This conforms to new IEEE 754R rules.</span></span>

<span data-ttu-id="4133f-122">Перед сравнением выполняется сброс депоставлений с сохранением знака.</span><span class="sxs-lookup"><span data-stu-id="4133f-122">Denorms are flushed, with the sign preserved, before comparison.</span></span> <span data-ttu-id="4133f-123">Однако результат, записанный в *dest* , может быть или не может быть сброшен.</span><span class="sxs-lookup"><span data-stu-id="4133f-123">However, the result written to *dest* may or may not be denorm flushed.</span></span>

<span data-ttu-id="4133f-124">В следующей таблице показаны результаты, полученные при выполнении инструкции с различными классами чисел, предполагая, что ни переполнение, ни потеря точности не происходит.</span><span class="sxs-lookup"><span data-stu-id="4133f-124">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="4133f-125">F означает конечное вещественное число.</span><span class="sxs-lookup"><span data-stu-id="4133f-125">F means finite real number.</span></span>



| <span data-ttu-id="4133f-126">**src0 src1 — >**</span><span class="sxs-lookup"><span data-stu-id="4133f-126">**src0 src1->**</span></span> | <span data-ttu-id="4133f-127">**-INF**</span><span class="sxs-lookup"><span data-stu-id="4133f-127">**-inf**</span></span> | <span data-ttu-id="4133f-128">**Ж**</span><span class="sxs-lookup"><span data-stu-id="4133f-128">**F**</span></span>        | <span data-ttu-id="4133f-129">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="4133f-129">**+inf**</span></span> | <span data-ttu-id="4133f-130">**Не число**</span><span class="sxs-lookup"><span data-stu-id="4133f-130">**NaN**</span></span> |
|--------------------|----------|--------------|----------|---------|
| <span data-ttu-id="4133f-131">**-INF**</span><span class="sxs-lookup"><span data-stu-id="4133f-131">**-inf**</span></span>           | <span data-ttu-id="4133f-132">-inf</span><span class="sxs-lookup"><span data-stu-id="4133f-132">-inf</span></span>     | <span data-ttu-id="4133f-133">-inf</span><span class="sxs-lookup"><span data-stu-id="4133f-133">-inf</span></span>         | <span data-ttu-id="4133f-134">-inf</span><span class="sxs-lookup"><span data-stu-id="4133f-134">-inf</span></span>     | <span data-ttu-id="4133f-135">-inf</span><span class="sxs-lookup"><span data-stu-id="4133f-135">-inf</span></span>    |
| <span data-ttu-id="4133f-136">**Ж**</span><span class="sxs-lookup"><span data-stu-id="4133f-136">**F**</span></span>              | <span data-ttu-id="4133f-137">-inf</span><span class="sxs-lookup"><span data-stu-id="4133f-137">-inf</span></span>     | <span data-ttu-id="4133f-138">src0 или src1</span><span class="sxs-lookup"><span data-stu-id="4133f-138">src0 or src1</span></span> | <span data-ttu-id="4133f-139">src0</span><span class="sxs-lookup"><span data-stu-id="4133f-139">src0</span></span>     | <span data-ttu-id="4133f-140">src0</span><span class="sxs-lookup"><span data-stu-id="4133f-140">src0</span></span>    |
| <span data-ttu-id="4133f-141">**-INF**</span><span class="sxs-lookup"><span data-stu-id="4133f-141">**-inf**</span></span>           | <span data-ttu-id="4133f-142">-inf</span><span class="sxs-lookup"><span data-stu-id="4133f-142">-inf</span></span>     | <span data-ttu-id="4133f-143">src1</span><span class="sxs-lookup"><span data-stu-id="4133f-143">src1</span></span>         | <span data-ttu-id="4133f-144">+inf</span><span class="sxs-lookup"><span data-stu-id="4133f-144">+inf</span></span>     | <span data-ttu-id="4133f-145">+inf</span><span class="sxs-lookup"><span data-stu-id="4133f-145">+inf</span></span>    |
| <span data-ttu-id="4133f-146">**Не число**</span><span class="sxs-lookup"><span data-stu-id="4133f-146">**NaN**</span></span>            | <span data-ttu-id="4133f-147">-inf</span><span class="sxs-lookup"><span data-stu-id="4133f-147">-inf</span></span>     | <span data-ttu-id="4133f-148">src1</span><span class="sxs-lookup"><span data-stu-id="4133f-148">src1</span></span>         | <span data-ttu-id="4133f-149">+inf</span><span class="sxs-lookup"><span data-stu-id="4133f-149">+inf</span></span>     | <span data-ttu-id="4133f-150">не число</span><span class="sxs-lookup"><span data-stu-id="4133f-150">NaN</span></span>     |



 

<span data-ttu-id="4133f-151">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="4133f-151">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="4133f-152">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="4133f-152">Vertex Shader</span></span> | <span data-ttu-id="4133f-153">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="4133f-153">Geometry Shader</span></span> | <span data-ttu-id="4133f-154">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="4133f-154">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="4133f-155">x</span><span class="sxs-lookup"><span data-stu-id="4133f-155">x</span></span>             | <span data-ttu-id="4133f-156">x</span><span class="sxs-lookup"><span data-stu-id="4133f-156">x</span></span>               | <span data-ttu-id="4133f-157">x</span><span class="sxs-lookup"><span data-stu-id="4133f-157">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="4133f-158">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="4133f-158">Minimum Shader Model</span></span>

<span data-ttu-id="4133f-159">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="4133f-159">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4133f-160">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="4133f-160">Shader Model</span></span>                                              | <span data-ttu-id="4133f-161">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="4133f-161">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="4133f-162">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="4133f-162">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="4133f-163">да</span><span class="sxs-lookup"><span data-stu-id="4133f-163">yes</span></span>       |
| [<span data-ttu-id="4133f-164">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="4133f-164">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="4133f-165">да</span><span class="sxs-lookup"><span data-stu-id="4133f-165">yes</span></span>       |
| [<span data-ttu-id="4133f-166">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="4133f-166">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="4133f-167">да</span><span class="sxs-lookup"><span data-stu-id="4133f-167">yes</span></span>       |
| [<span data-ttu-id="4133f-168">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4133f-168">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="4133f-169">Нет</span><span class="sxs-lookup"><span data-stu-id="4133f-169">no</span></span>        |
| [<span data-ttu-id="4133f-170">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4133f-170">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="4133f-171">Нет</span><span class="sxs-lookup"><span data-stu-id="4133f-171">no</span></span>        |
| [<span data-ttu-id="4133f-172">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4133f-172">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="4133f-173">Нет</span><span class="sxs-lookup"><span data-stu-id="4133f-173">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="4133f-174">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="4133f-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4133f-175">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4133f-175">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





