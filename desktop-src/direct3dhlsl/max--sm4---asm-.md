---
title: Max (SM4-ASM)
description: Максимальное количество перемещаемых компонентов.
ms.assetid: 005468AA-577E-441F-ACD5-37A691E62CDD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f24618897eacf250f2b924f6dde3745a32a7172
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412142"
---
# <a name="max-sm4---asm"></a><span data-ttu-id="e99cf-103">Max (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="e99cf-103">max (sm4 - asm)</span></span>

<span data-ttu-id="e99cf-104">Максимальное количество перемещаемых компонентов.</span><span class="sxs-lookup"><span data-stu-id="e99cf-104">Component-wise float maximum.</span></span>



| <span data-ttu-id="e99cf-105">Максимальная длина \[ \_ \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . свиззле \] , \[ - \] src1 \[ \_ ABS \] \[ . свиззле \] ,</span><span class="sxs-lookup"><span data-stu-id="e99cf-105">max\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\],</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="e99cf-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="e99cf-106">Item</span></span>                                                            | <span data-ttu-id="e99cf-107">Описание</span><span class="sxs-lookup"><span data-stu-id="e99cf-107">Description</span></span>                                                                                               |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e99cf-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="e99cf-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="e99cf-109">\[в \] результате операции.</span><span class="sxs-lookup"><span data-stu-id="e99cf-109">\[in\] The result of the operation.</span></span> <br/> <span data-ttu-id="e99cf-110">*конечный адрес*  =  *src0*  >=  *src1* ?</span><span class="sxs-lookup"><span data-stu-id="e99cf-110">*dest* = *src0* >= *src1* ?</span></span> <span data-ttu-id="e99cf-111">*src0* : *src1*</span><span class="sxs-lookup"><span data-stu-id="e99cf-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="e99cf-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="e99cf-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="e99cf-113">\[в \] компонентах, сравниваемых с *src1*.</span><span class="sxs-lookup"><span data-stu-id="e99cf-113">\[in\] The components to compare to *src1*.</span></span><br/>                                                    |
| <span data-ttu-id="e99cf-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="e99cf-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="e99cf-115">\[в \] компонентах, сравниваемых с *src0*.</span><span class="sxs-lookup"><span data-stu-id="e99cf-115">\[in\] The components to compare to *src0*.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="e99cf-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="e99cf-116">Remarks</span></span>

><span data-ttu-id="e99cf-117">= используется вместо >, поэтому если min (x, y) = x, то Max (x, y) = y.</span><span class="sxs-lookup"><span data-stu-id="e99cf-117">= is used instead of > so that if min(x,y) = x then max(x,y) = y.</span></span>

<span data-ttu-id="e99cf-118">NaN имеет особую обработку.</span><span class="sxs-lookup"><span data-stu-id="e99cf-118">NaN has special handling.</span></span> <span data-ttu-id="e99cf-119">Если один исходный операнд равен NaN, то возвращается другой исходный операнд и выбирается для каждого компонента.</span><span class="sxs-lookup"><span data-stu-id="e99cf-119">If one source operand is NaN, then the other source operand is returned and the choice is made per-component.</span></span> <span data-ttu-id="e99cf-120">Если оба значения равны NaN, возвращается любое представление NaN.</span><span class="sxs-lookup"><span data-stu-id="e99cf-120">If both are NaN, any NaN representation is returned.</span></span>

<span data-ttu-id="e99cf-121">Перед сравнением операции записи сбрасываются с сохранением знака.</span><span class="sxs-lookup"><span data-stu-id="e99cf-121">Denorms are flushed with sign preserved before the comparison.</span></span> <span data-ttu-id="e99cf-122">Однако результат, записанный в *dest* , может быть или не может быть сброшен.</span><span class="sxs-lookup"><span data-stu-id="e99cf-122">However, the result written to *dest* may or may not be denorm flushed.</span></span>

<span data-ttu-id="e99cf-123">В следующей таблице показаны результаты, полученные при выполнении инструкции с различными классами чисел, предполагая, что ни переполнение, ни потеря точности не происходит.</span><span class="sxs-lookup"><span data-stu-id="e99cf-123">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="e99cf-124">F означает конечное вещественное число.</span><span class="sxs-lookup"><span data-stu-id="e99cf-124">F means finite real number.</span></span>



|                    |          |              |          |         |
|--------------------|----------|--------------|----------|---------|
| <span data-ttu-id="e99cf-125">**src0 src1 — >**</span><span class="sxs-lookup"><span data-stu-id="e99cf-125">**src0 src1->**</span></span> | <span data-ttu-id="e99cf-126">**-INF**</span><span class="sxs-lookup"><span data-stu-id="e99cf-126">**-inf**</span></span> | <span data-ttu-id="e99cf-127">**Ж**</span><span class="sxs-lookup"><span data-stu-id="e99cf-127">**F**</span></span>        | <span data-ttu-id="e99cf-128">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="e99cf-128">**+inf**</span></span> | <span data-ttu-id="e99cf-129">**Не число**</span><span class="sxs-lookup"><span data-stu-id="e99cf-129">**NaN**</span></span> |
| <span data-ttu-id="e99cf-130">**-INF**</span><span class="sxs-lookup"><span data-stu-id="e99cf-130">**-inf**</span></span>           | <span data-ttu-id="e99cf-131">-inf</span><span class="sxs-lookup"><span data-stu-id="e99cf-131">-inf</span></span>     | <span data-ttu-id="e99cf-132">src1</span><span class="sxs-lookup"><span data-stu-id="e99cf-132">src1</span></span>         | <span data-ttu-id="e99cf-133">+inf</span><span class="sxs-lookup"><span data-stu-id="e99cf-133">+inf</span></span>     | <span data-ttu-id="e99cf-134">-inf</span><span class="sxs-lookup"><span data-stu-id="e99cf-134">-inf</span></span>    |
| <span data-ttu-id="e99cf-135">**Ж**</span><span class="sxs-lookup"><span data-stu-id="e99cf-135">**F**</span></span>              | <span data-ttu-id="e99cf-136">src0</span><span class="sxs-lookup"><span data-stu-id="e99cf-136">src0</span></span>     | <span data-ttu-id="e99cf-137">src0 или src1</span><span class="sxs-lookup"><span data-stu-id="e99cf-137">src0 or src1</span></span> | <span data-ttu-id="e99cf-138">+inf</span><span class="sxs-lookup"><span data-stu-id="e99cf-138">+inf</span></span>     | <span data-ttu-id="e99cf-139">src0</span><span class="sxs-lookup"><span data-stu-id="e99cf-139">src0</span></span>    |
| <span data-ttu-id="e99cf-140">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="e99cf-140">**+inf**</span></span>           | <span data-ttu-id="e99cf-141">+inf</span><span class="sxs-lookup"><span data-stu-id="e99cf-141">+inf</span></span>     | <span data-ttu-id="e99cf-142">+inf</span><span class="sxs-lookup"><span data-stu-id="e99cf-142">+inf</span></span>         | <span data-ttu-id="e99cf-143">+inf</span><span class="sxs-lookup"><span data-stu-id="e99cf-143">+inf</span></span>     | <span data-ttu-id="e99cf-144">+inf</span><span class="sxs-lookup"><span data-stu-id="e99cf-144">+inf</span></span>    |
| <span data-ttu-id="e99cf-145">**Не число**</span><span class="sxs-lookup"><span data-stu-id="e99cf-145">**NaN**</span></span>            | <span data-ttu-id="e99cf-146">-inf</span><span class="sxs-lookup"><span data-stu-id="e99cf-146">-inf</span></span>     | <span data-ttu-id="e99cf-147">src1</span><span class="sxs-lookup"><span data-stu-id="e99cf-147">src1</span></span>         | <span data-ttu-id="e99cf-148">+inf</span><span class="sxs-lookup"><span data-stu-id="e99cf-148">+inf</span></span>     | <span data-ttu-id="e99cf-149">не число</span><span class="sxs-lookup"><span data-stu-id="e99cf-149">NaN</span></span>     |



 

<span data-ttu-id="e99cf-150">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="e99cf-150">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e99cf-151">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="e99cf-151">Vertex Shader</span></span> | <span data-ttu-id="e99cf-152">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="e99cf-152">Geometry Shader</span></span> | <span data-ttu-id="e99cf-153">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="e99cf-153">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="e99cf-154">x</span><span class="sxs-lookup"><span data-stu-id="e99cf-154">x</span></span>             | <span data-ttu-id="e99cf-155">x</span><span class="sxs-lookup"><span data-stu-id="e99cf-155">x</span></span>               | <span data-ttu-id="e99cf-156">x</span><span class="sxs-lookup"><span data-stu-id="e99cf-156">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e99cf-157">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="e99cf-157">Minimum Shader Model</span></span>

<span data-ttu-id="e99cf-158">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="e99cf-158">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e99cf-159">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="e99cf-159">Shader Model</span></span>                                              | <span data-ttu-id="e99cf-160">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="e99cf-160">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e99cf-161">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="e99cf-161">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e99cf-162">да</span><span class="sxs-lookup"><span data-stu-id="e99cf-162">yes</span></span>       |
| [<span data-ttu-id="e99cf-163">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="e99cf-163">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e99cf-164">да</span><span class="sxs-lookup"><span data-stu-id="e99cf-164">yes</span></span>       |
| [<span data-ttu-id="e99cf-165">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="e99cf-165">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e99cf-166">да</span><span class="sxs-lookup"><span data-stu-id="e99cf-166">yes</span></span>       |
| [<span data-ttu-id="e99cf-167">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e99cf-167">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e99cf-168">Нет</span><span class="sxs-lookup"><span data-stu-id="e99cf-168">no</span></span>        |
| [<span data-ttu-id="e99cf-169">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e99cf-169">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e99cf-170">Нет</span><span class="sxs-lookup"><span data-stu-id="e99cf-170">no</span></span>        |
| [<span data-ttu-id="e99cf-171">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e99cf-171">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e99cf-172">Нет</span><span class="sxs-lookup"><span data-stu-id="e99cf-172">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e99cf-173">См. также</span><span class="sxs-lookup"><span data-stu-id="e99cf-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e99cf-174">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e99cf-174">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





