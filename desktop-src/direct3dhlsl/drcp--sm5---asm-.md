---
title: дркп (SM5-ASM)
description: Вычисление взаимной точности с двойной точностью.
ms.assetid: 499A14D6-36DB-4860-94D1-887D931E60D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b678f4e8b3464817215de9132298fdde1f6feec
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104335552"
---
# <a name="drcp-sm5---asm"></a><span data-ttu-id="0047c-103">дркп (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="0047c-103">drcp (sm5 - asm)</span></span>

<span data-ttu-id="0047c-104">Вычисление взаимной точности с двойной точностью.</span><span class="sxs-lookup"><span data-stu-id="0047c-104">Computes a component-wise double-precision reciprocal.</span></span>



| <span data-ttu-id="0047c-105">rcp No \[ \_ \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="0047c-105">rcp\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="0047c-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="0047c-106">Item</span></span>                                                            | <span data-ttu-id="0047c-107">Описание</span><span class="sxs-lookup"><span data-stu-id="0047c-107">Description</span></span>                                                                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0047c-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="0047c-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="0047c-109">\[в \] адресе результатов</span><span class="sxs-lookup"><span data-stu-id="0047c-109">\[in\] The address of the results</span></span><br/> <span data-ttu-id="0047c-110">*конечный адрес*  =  **1,0**  /  *src0*.</span><span class="sxs-lookup"><span data-stu-id="0047c-110">*dest* = **1.0** / *src0*.</span></span> <span data-ttu-id="0047c-111">Значение результата должно быть точным до 1,0 ULP</span><span class="sxs-lookup"><span data-stu-id="0047c-111">The result value must be accurate to 1.0 ULP</span></span><br/> |
| <span data-ttu-id="0047c-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="0047c-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="0047c-113">\[\]число, которое нужно взять за обратную величину.</span><span class="sxs-lookup"><span data-stu-id="0047c-113">\[in\] The number to take the reciprocal of.</span></span><br/>                                                                         |



 

## <a name="remarks"></a><span data-ttu-id="0047c-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="0047c-114">Remarks</span></span>

<span data-ttu-id="0047c-115">Инструкция ДРКП создается компилятором HLSL только при явном вызове с помощью функции RCP (), если в качестве аргумента используется Double.</span><span class="sxs-lookup"><span data-stu-id="0047c-115">The DRCP instruction is emitted by the HLSL compiler only when explicitly called via the rcp() intrinsic, when a double is used as the argument.</span></span> <span data-ttu-id="0047c-116">Точность этой инструкции должна быть 1,0 ULP.</span><span class="sxs-lookup"><span data-stu-id="0047c-116">The accuracy of this instruction is required to be 1.0 ULP.</span></span>

<span data-ttu-id="0047c-117">Шейдеры, использующие эту инструкцию, будут помечены флагом построителя текстуры, который приведет к сбою привязки, если не выполняются все следующие условия.</span><span class="sxs-lookup"><span data-stu-id="0047c-117">Shaders that use this instruction will be marked with a shader flag that will cause them to fail to bind unless all the following conditions are met.</span></span>

-   <span data-ttu-id="0047c-118">Система поддерживает DirectX 11,1.</span><span class="sxs-lookup"><span data-stu-id="0047c-118">The system supports DirectX 11.1.</span></span>
-   <span data-ttu-id="0047c-119">Система включает драйвер WDDM 1,2.</span><span class="sxs-lookup"><span data-stu-id="0047c-119">The system includes a WDDM 1.2 driver.</span></span>
-   <span data-ttu-id="0047c-120">Драйвер сообщает о поддержке этой инструкции с помощью **\_ \_ параметров D3D11 Data Feature D3D11 \_ \_ . Для Екстендеддаублесшадеринструктионс** задано значение **true**.</span><span class="sxs-lookup"><span data-stu-id="0047c-120">The driver reports support for this instruction via **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS.ExtendedDoublesShaderInstructions** set to **TRUE**.</span></span>

<span data-ttu-id="0047c-121">В следующей таблице показаны результаты, полученные при выполнении инструкции с различными классами чисел, предполагая, что ни переполнение, ни потеря точности не происходит.</span><span class="sxs-lookup"><span data-stu-id="0047c-121">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="0047c-122">В этой таблице F означает ограничение по настоящему вещественному числу.</span><span class="sxs-lookup"><span data-stu-id="0047c-122">In this table F means finite-real number.</span></span>



|               |          |        |        |        |        |          |         |
|---------------|----------|--------|--------|--------|--------|----------|---------|
| <span data-ttu-id="0047c-123">**src**-></span><span class="sxs-lookup"><span data-stu-id="0047c-123">**src**-></span></span>  | <span data-ttu-id="0047c-124">**-INF**</span><span class="sxs-lookup"><span data-stu-id="0047c-124">**-inf**</span></span> | <span data-ttu-id="0047c-125">**-F**</span><span class="sxs-lookup"><span data-stu-id="0047c-125">**-F**</span></span> | <span data-ttu-id="0047c-126">**-0**</span><span class="sxs-lookup"><span data-stu-id="0047c-126">**-0**</span></span> | <span data-ttu-id="0047c-127">**+0**</span><span class="sxs-lookup"><span data-stu-id="0047c-127">**+0**</span></span> | <span data-ttu-id="0047c-128">**+ F**</span><span class="sxs-lookup"><span data-stu-id="0047c-128">**+F**</span></span> | <span data-ttu-id="0047c-129">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="0047c-129">**+inf**</span></span> | <span data-ttu-id="0047c-130">**Не число**</span><span class="sxs-lookup"><span data-stu-id="0047c-130">**NaN**</span></span> |
| <span data-ttu-id="0047c-131">**dest**-></span><span class="sxs-lookup"><span data-stu-id="0047c-131">**dest**-></span></span> | <span data-ttu-id="0047c-132">-0</span><span class="sxs-lookup"><span data-stu-id="0047c-132">-0</span></span>       | <span data-ttu-id="0047c-133">-F</span><span class="sxs-lookup"><span data-stu-id="0047c-133">-F</span></span>     | <span data-ttu-id="0047c-134">-inf</span><span class="sxs-lookup"><span data-stu-id="0047c-134">-inf</span></span>   | <span data-ttu-id="0047c-135">+inf</span><span class="sxs-lookup"><span data-stu-id="0047c-135">+inf</span></span>   | <span data-ttu-id="0047c-136">+ F</span><span class="sxs-lookup"><span data-stu-id="0047c-136">+F</span></span>     | <span data-ttu-id="0047c-137">+0</span><span class="sxs-lookup"><span data-stu-id="0047c-137">+0</span></span>       | <span data-ttu-id="0047c-138">Не число</span><span class="sxs-lookup"><span data-stu-id="0047c-138">NaN</span></span>     |



 

<span data-ttu-id="0047c-139">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="0047c-139">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="0047c-140">Вершина</span><span class="sxs-lookup"><span data-stu-id="0047c-140">Vertex</span></span> | <span data-ttu-id="0047c-141">Поверхности</span><span class="sxs-lookup"><span data-stu-id="0047c-141">Hull</span></span> | <span data-ttu-id="0047c-142">Домен</span><span class="sxs-lookup"><span data-stu-id="0047c-142">Domain</span></span> | <span data-ttu-id="0047c-143">Геометрия</span><span class="sxs-lookup"><span data-stu-id="0047c-143">Geometry</span></span> | <span data-ttu-id="0047c-144">Пиксель</span><span class="sxs-lookup"><span data-stu-id="0047c-144">Pixel</span></span> | <span data-ttu-id="0047c-145">Вычисления</span><span class="sxs-lookup"><span data-stu-id="0047c-145">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="0047c-146">X</span><span class="sxs-lookup"><span data-stu-id="0047c-146">X</span></span>      | <span data-ttu-id="0047c-147">X</span><span class="sxs-lookup"><span data-stu-id="0047c-147">X</span></span>    | <span data-ttu-id="0047c-148">X</span><span class="sxs-lookup"><span data-stu-id="0047c-148">X</span></span>      | <span data-ttu-id="0047c-149">X</span><span class="sxs-lookup"><span data-stu-id="0047c-149">X</span></span>        | <span data-ttu-id="0047c-150">X</span><span class="sxs-lookup"><span data-stu-id="0047c-150">X</span></span>     | <span data-ttu-id="0047c-151">X</span><span class="sxs-lookup"><span data-stu-id="0047c-151">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0047c-152">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="0047c-152">Minimum Shader Model</span></span>

<span data-ttu-id="0047c-153">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="0047c-153">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="0047c-154">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="0047c-154">Shader Model</span></span>                                              | <span data-ttu-id="0047c-155">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="0047c-155">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0047c-156">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="0047c-156">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="0047c-157">да</span><span class="sxs-lookup"><span data-stu-id="0047c-157">yes</span></span>       |
| [<span data-ttu-id="0047c-158">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="0047c-158">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="0047c-159">Нет</span><span class="sxs-lookup"><span data-stu-id="0047c-159">no</span></span>        |
| [<span data-ttu-id="0047c-160">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="0047c-160">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0047c-161">Нет</span><span class="sxs-lookup"><span data-stu-id="0047c-161">no</span></span>        |
| [<span data-ttu-id="0047c-162">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0047c-162">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0047c-163">Нет</span><span class="sxs-lookup"><span data-stu-id="0047c-163">no</span></span>        |
| [<span data-ttu-id="0047c-164">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0047c-164">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0047c-165">Нет</span><span class="sxs-lookup"><span data-stu-id="0047c-165">no</span></span>        |
| [<span data-ttu-id="0047c-166">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0047c-166">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0047c-167">Нет</span><span class="sxs-lookup"><span data-stu-id="0047c-167">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="0047c-168">См. также</span><span class="sxs-lookup"><span data-stu-id="0047c-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0047c-169">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0047c-169">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





