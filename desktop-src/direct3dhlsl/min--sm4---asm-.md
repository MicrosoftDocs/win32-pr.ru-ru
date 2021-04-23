---
title: min (SM4-ASM)
description: Минимальное количество перемещаемых компонентов.
ms.assetid: 8EDD5503-76D5-4078-BFBA-1DA9260C6E68
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e584aee077735b717bf76d148d4d0db4357a7d95
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104133338"
---
# <a name="min-sm4---asm"></a><span data-ttu-id="d7fb8-103">min (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="d7fb8-103">min (sm4 - asm)</span></span>

<span data-ttu-id="d7fb8-104">Минимальное количество перемещаемых компонентов.</span><span class="sxs-lookup"><span data-stu-id="d7fb8-104">Component-wise float minimum.</span></span>



| <span data-ttu-id="d7fb8-105">мин \[ \_ \] \[ . \] , \[ - \] src0 \[ \_ ABS. \] \[ свиззле \] , \[ - \] src1 \[ \_ ABS \] \[ . свиззле \] ,</span><span class="sxs-lookup"><span data-stu-id="d7fb8-105">min\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\],</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="d7fb8-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="d7fb8-106">Item</span></span>                                                            | <span data-ttu-id="d7fb8-107">Описание</span><span class="sxs-lookup"><span data-stu-id="d7fb8-107">Description</span></span>                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7fb8-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="d7fb8-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="d7fb8-109">\[в \] результате операции.</span><span class="sxs-lookup"><span data-stu-id="d7fb8-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="d7fb8-110">*конечный адрес*  =  *src0*  <  *src1* ?</span><span class="sxs-lookup"><span data-stu-id="d7fb8-110">*dest* = *src0* < *src1* ?</span></span> <span data-ttu-id="d7fb8-111">*src0* : *src1*</span><span class="sxs-lookup"><span data-stu-id="d7fb8-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="d7fb8-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="d7fb8-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="d7fb8-113">\[в \] компонентах, сравниваемых с *src1*.</span><span class="sxs-lookup"><span data-stu-id="d7fb8-113">\[in\] The components to compare to *src1*.</span></span><br/>                                                  |
| <span data-ttu-id="d7fb8-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="d7fb8-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="d7fb8-115">\[в \] компонентах, сравниваемых с *src0*.</span><span class="sxs-lookup"><span data-stu-id="d7fb8-115">\[in\] The components to compare to *src0*.</span></span><br/>                                                  |



 

## <a name="remarks"></a><span data-ttu-id="d7fb8-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="d7fb8-116">Remarks</span></span>

><span data-ttu-id="d7fb8-117">= используется вместо >, поэтому если min (x, y) = x, то Max (x, y) = y.</span><span class="sxs-lookup"><span data-stu-id="d7fb8-117">= is used instead of > so that if min(x,y) = x then max(x,y) = y.</span></span>

<span data-ttu-id="d7fb8-118">NaN имеет особую обработку.</span><span class="sxs-lookup"><span data-stu-id="d7fb8-118">NaN has special handling.</span></span> <span data-ttu-id="d7fb8-119">Если один исходный операнд равен NaN, то возвращается другой исходный операнд и выбирается для каждого компонента.</span><span class="sxs-lookup"><span data-stu-id="d7fb8-119">If one source operand is NaN, then the other source operand is returned and the choice is made per-component.</span></span> <span data-ttu-id="d7fb8-120">Если оба значения равны NaN, возвращается любое представление NaN.</span><span class="sxs-lookup"><span data-stu-id="d7fb8-120">If both are NaN, any NaN representation is returned.</span></span> <span data-ttu-id="d7fb8-121">Это соответствует новым правилам IEEE 754R.</span><span class="sxs-lookup"><span data-stu-id="d7fb8-121">This conforms to new IEEE 754R rules.</span></span>

<span data-ttu-id="d7fb8-122">Перед сравнением выполняется сброс депоставлений с сохранением знака.</span><span class="sxs-lookup"><span data-stu-id="d7fb8-122">Denorms are flushed, with the sign preserved, before comparison.</span></span> <span data-ttu-id="d7fb8-123">Однако результат, записанный в *dest* , может быть или не может быть сброшен.</span><span class="sxs-lookup"><span data-stu-id="d7fb8-123">However, the result written to *dest* may or may not be denorm flushed.</span></span>

<span data-ttu-id="d7fb8-124">В следующей таблице показаны результаты, полученные при выполнении инструкции с различными классами чисел, предполагая, что ни переполнение, ни потеря точности не происходит.</span><span class="sxs-lookup"><span data-stu-id="d7fb8-124">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="d7fb8-125">F означает конечное вещественное число.</span><span class="sxs-lookup"><span data-stu-id="d7fb8-125">F means finite real number.</span></span>



|                    |          |              |          |         |
|--------------------|----------|--------------|----------|---------|
| <span data-ttu-id="d7fb8-126">**src0 src1 — >**</span><span class="sxs-lookup"><span data-stu-id="d7fb8-126">**src0 src1->**</span></span> | <span data-ttu-id="d7fb8-127">**-INF**</span><span class="sxs-lookup"><span data-stu-id="d7fb8-127">**-inf**</span></span> | <span data-ttu-id="d7fb8-128">**Ж**</span><span class="sxs-lookup"><span data-stu-id="d7fb8-128">**F**</span></span>        | <span data-ttu-id="d7fb8-129">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="d7fb8-129">**+inf**</span></span> | <span data-ttu-id="d7fb8-130">**Не число**</span><span class="sxs-lookup"><span data-stu-id="d7fb8-130">**NaN**</span></span> |
| <span data-ttu-id="d7fb8-131">**-INF**</span><span class="sxs-lookup"><span data-stu-id="d7fb8-131">**-inf**</span></span>           | <span data-ttu-id="d7fb8-132">-inf</span><span class="sxs-lookup"><span data-stu-id="d7fb8-132">-inf</span></span>     | <span data-ttu-id="d7fb8-133">-inf</span><span class="sxs-lookup"><span data-stu-id="d7fb8-133">-inf</span></span>         | <span data-ttu-id="d7fb8-134">-inf</span><span class="sxs-lookup"><span data-stu-id="d7fb8-134">-inf</span></span>     | <span data-ttu-id="d7fb8-135">-inf</span><span class="sxs-lookup"><span data-stu-id="d7fb8-135">-inf</span></span>    |
| <span data-ttu-id="d7fb8-136">**Ж**</span><span class="sxs-lookup"><span data-stu-id="d7fb8-136">**F**</span></span>              | <span data-ttu-id="d7fb8-137">-inf</span><span class="sxs-lookup"><span data-stu-id="d7fb8-137">-inf</span></span>     | <span data-ttu-id="d7fb8-138">src0 или src1</span><span class="sxs-lookup"><span data-stu-id="d7fb8-138">src0 or src1</span></span> | <span data-ttu-id="d7fb8-139">src0</span><span class="sxs-lookup"><span data-stu-id="d7fb8-139">src0</span></span>     | <span data-ttu-id="d7fb8-140">src0</span><span class="sxs-lookup"><span data-stu-id="d7fb8-140">src0</span></span>    |
| <span data-ttu-id="d7fb8-141">**-INF**</span><span class="sxs-lookup"><span data-stu-id="d7fb8-141">**-inf**</span></span>           | <span data-ttu-id="d7fb8-142">-inf</span><span class="sxs-lookup"><span data-stu-id="d7fb8-142">-inf</span></span>     | <span data-ttu-id="d7fb8-143">src1</span><span class="sxs-lookup"><span data-stu-id="d7fb8-143">src1</span></span>         | <span data-ttu-id="d7fb8-144">+inf</span><span class="sxs-lookup"><span data-stu-id="d7fb8-144">+inf</span></span>     | <span data-ttu-id="d7fb8-145">+inf</span><span class="sxs-lookup"><span data-stu-id="d7fb8-145">+inf</span></span>    |
| <span data-ttu-id="d7fb8-146">**Не число**</span><span class="sxs-lookup"><span data-stu-id="d7fb8-146">**NaN**</span></span>            | <span data-ttu-id="d7fb8-147">-inf</span><span class="sxs-lookup"><span data-stu-id="d7fb8-147">-inf</span></span>     | <span data-ttu-id="d7fb8-148">src1</span><span class="sxs-lookup"><span data-stu-id="d7fb8-148">src1</span></span>         | <span data-ttu-id="d7fb8-149">+inf</span><span class="sxs-lookup"><span data-stu-id="d7fb8-149">+inf</span></span>     | <span data-ttu-id="d7fb8-150">не число</span><span class="sxs-lookup"><span data-stu-id="d7fb8-150">NaN</span></span>     |



 

<span data-ttu-id="d7fb8-151">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="d7fb8-151">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d7fb8-152">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="d7fb8-152">Vertex Shader</span></span> | <span data-ttu-id="d7fb8-153">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="d7fb8-153">Geometry Shader</span></span> | <span data-ttu-id="d7fb8-154">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="d7fb8-154">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="d7fb8-155">x</span><span class="sxs-lookup"><span data-stu-id="d7fb8-155">x</span></span>             | <span data-ttu-id="d7fb8-156">x</span><span class="sxs-lookup"><span data-stu-id="d7fb8-156">x</span></span>               | <span data-ttu-id="d7fb8-157">x</span><span class="sxs-lookup"><span data-stu-id="d7fb8-157">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d7fb8-158">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="d7fb8-158">Minimum Shader Model</span></span>

<span data-ttu-id="d7fb8-159">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="d7fb8-159">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d7fb8-160">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="d7fb8-160">Shader Model</span></span>                                              | <span data-ttu-id="d7fb8-161">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="d7fb8-161">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d7fb8-162">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="d7fb8-162">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d7fb8-163">да</span><span class="sxs-lookup"><span data-stu-id="d7fb8-163">yes</span></span>       |
| [<span data-ttu-id="d7fb8-164">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="d7fb8-164">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d7fb8-165">да</span><span class="sxs-lookup"><span data-stu-id="d7fb8-165">yes</span></span>       |
| [<span data-ttu-id="d7fb8-166">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="d7fb8-166">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d7fb8-167">да</span><span class="sxs-lookup"><span data-stu-id="d7fb8-167">yes</span></span>       |
| [<span data-ttu-id="d7fb8-168">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d7fb8-168">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d7fb8-169">Нет</span><span class="sxs-lookup"><span data-stu-id="d7fb8-169">no</span></span>        |
| [<span data-ttu-id="d7fb8-170">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d7fb8-170">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d7fb8-171">Нет</span><span class="sxs-lookup"><span data-stu-id="d7fb8-171">no</span></span>        |
| [<span data-ttu-id="d7fb8-172">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d7fb8-172">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d7fb8-173">Нет</span><span class="sxs-lookup"><span data-stu-id="d7fb8-173">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d7fb8-174">См. также</span><span class="sxs-lookup"><span data-stu-id="d7fb8-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7fb8-175">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d7fb8-175">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





