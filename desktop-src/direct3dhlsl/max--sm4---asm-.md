---
title: Max (SM4-ASM)
description: Максимальное количество перемещаемых компонентов.
ms.assetid: 005468AA-577E-441F-ACD5-37A691E62CDD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f64d88c581828f2563f6d5d8a6c57de6400f9bbf
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994731"
---
# <a name="max-sm4---asm"></a><span data-ttu-id="74765-103">Max (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="74765-103">max (sm4 - asm)</span></span>

<span data-ttu-id="74765-104">Максимальное количество перемещаемых компонентов.</span><span class="sxs-lookup"><span data-stu-id="74765-104">Component-wise float maximum.</span></span>



| <span data-ttu-id="74765-105">Максимальная длина \[ \_ \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . свиззле \] , \[ - \] src1 \[ \_ ABS \] \[ . свиззле \] ,</span><span class="sxs-lookup"><span data-stu-id="74765-105">max\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\],</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="74765-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="74765-106">Item</span></span>                                                            | <span data-ttu-id="74765-107">Описание</span><span class="sxs-lookup"><span data-stu-id="74765-107">Description</span></span>                                                                                               |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74765-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="74765-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="74765-109">\[в \] результате операции.</span><span class="sxs-lookup"><span data-stu-id="74765-109">\[in\] The result of the operation.</span></span> <br/> <span data-ttu-id="74765-110">*конечный адрес*  =  *src0*  >=  *src1* ?</span><span class="sxs-lookup"><span data-stu-id="74765-110">*dest* = *src0* >= *src1* ?</span></span> <span data-ttu-id="74765-111">*src0* : *src1*</span><span class="sxs-lookup"><span data-stu-id="74765-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="74765-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="74765-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="74765-113">\[в \] компонентах, сравниваемых с *src1*.</span><span class="sxs-lookup"><span data-stu-id="74765-113">\[in\] The components to compare to *src1*.</span></span><br/>                                                    |
| <span data-ttu-id="74765-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="74765-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="74765-115">\[в \] компонентах, сравниваемых с *src0*.</span><span class="sxs-lookup"><span data-stu-id="74765-115">\[in\] The components to compare to *src0*.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="74765-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="74765-116">Remarks</span></span>

><span data-ttu-id="74765-117">= используется вместо >, поэтому если min (x, y) = x, то Max (x, y) = y.</span><span class="sxs-lookup"><span data-stu-id="74765-117">= is used instead of > so that if min(x,y) = x then max(x,y) = y.</span></span>

<span data-ttu-id="74765-118">NaN имеет особую обработку.</span><span class="sxs-lookup"><span data-stu-id="74765-118">NaN has special handling.</span></span> <span data-ttu-id="74765-119">Если один исходный операнд равен NaN, то возвращается другой исходный операнд и выбирается для каждого компонента.</span><span class="sxs-lookup"><span data-stu-id="74765-119">If one source operand is NaN, then the other source operand is returned and the choice is made per-component.</span></span> <span data-ttu-id="74765-120">Если оба значения равны NaN, возвращается любое представление NaN.</span><span class="sxs-lookup"><span data-stu-id="74765-120">If both are NaN, any NaN representation is returned.</span></span>

<span data-ttu-id="74765-121">Перед сравнением операции записи сбрасываются с сохранением знака.</span><span class="sxs-lookup"><span data-stu-id="74765-121">Denorms are flushed with sign preserved before the comparison.</span></span> <span data-ttu-id="74765-122">Однако результат, записанный в *dest* , может быть или не может быть сброшен.</span><span class="sxs-lookup"><span data-stu-id="74765-122">However, the result written to *dest* may or may not be denorm flushed.</span></span>

<span data-ttu-id="74765-123">В следующей таблице показаны результаты, полученные при выполнении инструкции с различными классами чисел, предполагая, что ни переполнение, ни потеря точности не происходит.</span><span class="sxs-lookup"><span data-stu-id="74765-123">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="74765-124">F означает конечное вещественное число.</span><span class="sxs-lookup"><span data-stu-id="74765-124">F means finite real number.</span></span>



| <span data-ttu-id="74765-125">**src0 src1 — >**</span><span class="sxs-lookup"><span data-stu-id="74765-125">**src0 src1->**</span></span> | <span data-ttu-id="74765-126">**-INF**</span><span class="sxs-lookup"><span data-stu-id="74765-126">**-inf**</span></span> | <span data-ttu-id="74765-127">**Ж**</span><span class="sxs-lookup"><span data-stu-id="74765-127">**F**</span></span>        | <span data-ttu-id="74765-128">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="74765-128">**+inf**</span></span> | <span data-ttu-id="74765-129">**Не число**</span><span class="sxs-lookup"><span data-stu-id="74765-129">**NaN**</span></span> |
|--------------------|----------|--------------|----------|---------|
| <span data-ttu-id="74765-130">**-INF**</span><span class="sxs-lookup"><span data-stu-id="74765-130">**-inf**</span></span>           | <span data-ttu-id="74765-131">-inf</span><span class="sxs-lookup"><span data-stu-id="74765-131">-inf</span></span>     | <span data-ttu-id="74765-132">src1</span><span class="sxs-lookup"><span data-stu-id="74765-132">src1</span></span>         | <span data-ttu-id="74765-133">+inf</span><span class="sxs-lookup"><span data-stu-id="74765-133">+inf</span></span>     | <span data-ttu-id="74765-134">-inf</span><span class="sxs-lookup"><span data-stu-id="74765-134">-inf</span></span>    |
| <span data-ttu-id="74765-135">**Ж**</span><span class="sxs-lookup"><span data-stu-id="74765-135">**F**</span></span>              | <span data-ttu-id="74765-136">src0</span><span class="sxs-lookup"><span data-stu-id="74765-136">src0</span></span>     | <span data-ttu-id="74765-137">src0 или src1</span><span class="sxs-lookup"><span data-stu-id="74765-137">src0 or src1</span></span> | <span data-ttu-id="74765-138">+inf</span><span class="sxs-lookup"><span data-stu-id="74765-138">+inf</span></span>     | <span data-ttu-id="74765-139">src0</span><span class="sxs-lookup"><span data-stu-id="74765-139">src0</span></span>    |
| <span data-ttu-id="74765-140">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="74765-140">**+inf**</span></span>           | <span data-ttu-id="74765-141">+inf</span><span class="sxs-lookup"><span data-stu-id="74765-141">+inf</span></span>     | <span data-ttu-id="74765-142">+inf</span><span class="sxs-lookup"><span data-stu-id="74765-142">+inf</span></span>         | <span data-ttu-id="74765-143">+inf</span><span class="sxs-lookup"><span data-stu-id="74765-143">+inf</span></span>     | <span data-ttu-id="74765-144">+inf</span><span class="sxs-lookup"><span data-stu-id="74765-144">+inf</span></span>    |
| <span data-ttu-id="74765-145">**Не число**</span><span class="sxs-lookup"><span data-stu-id="74765-145">**NaN**</span></span>            | <span data-ttu-id="74765-146">-inf</span><span class="sxs-lookup"><span data-stu-id="74765-146">-inf</span></span>     | <span data-ttu-id="74765-147">src1</span><span class="sxs-lookup"><span data-stu-id="74765-147">src1</span></span>         | <span data-ttu-id="74765-148">+inf</span><span class="sxs-lookup"><span data-stu-id="74765-148">+inf</span></span>     | <span data-ttu-id="74765-149">не число</span><span class="sxs-lookup"><span data-stu-id="74765-149">NaN</span></span>     |



 

<span data-ttu-id="74765-150">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="74765-150">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="74765-151">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="74765-151">Vertex Shader</span></span> | <span data-ttu-id="74765-152">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="74765-152">Geometry Shader</span></span> | <span data-ttu-id="74765-153">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="74765-153">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="74765-154">x</span><span class="sxs-lookup"><span data-stu-id="74765-154">x</span></span>             | <span data-ttu-id="74765-155">x</span><span class="sxs-lookup"><span data-stu-id="74765-155">x</span></span>               | <span data-ttu-id="74765-156">x</span><span class="sxs-lookup"><span data-stu-id="74765-156">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="74765-157">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="74765-157">Minimum Shader Model</span></span>

<span data-ttu-id="74765-158">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="74765-158">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="74765-159">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="74765-159">Shader Model</span></span>                                              | <span data-ttu-id="74765-160">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="74765-160">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="74765-161">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="74765-161">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="74765-162">да</span><span class="sxs-lookup"><span data-stu-id="74765-162">yes</span></span>       |
| [<span data-ttu-id="74765-163">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="74765-163">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="74765-164">да</span><span class="sxs-lookup"><span data-stu-id="74765-164">yes</span></span>       |
| [<span data-ttu-id="74765-165">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="74765-165">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="74765-166">да</span><span class="sxs-lookup"><span data-stu-id="74765-166">yes</span></span>       |
| [<span data-ttu-id="74765-167">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="74765-167">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="74765-168">Нет</span><span class="sxs-lookup"><span data-stu-id="74765-168">no</span></span>        |
| [<span data-ttu-id="74765-169">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="74765-169">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="74765-170">Нет</span><span class="sxs-lookup"><span data-stu-id="74765-170">no</span></span>        |
| [<span data-ttu-id="74765-171">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="74765-171">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="74765-172">Нет</span><span class="sxs-lookup"><span data-stu-id="74765-172">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="74765-173">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="74765-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74765-174">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="74765-174">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





