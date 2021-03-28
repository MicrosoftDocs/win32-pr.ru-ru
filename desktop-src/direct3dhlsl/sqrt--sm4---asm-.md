---
title: Sqrt (SM4-ASM)
description: Компонентный квадратный корень.
ms.assetid: B860D656-7F01-484F-909F-A5C9A61C52C3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0a12afaf5b2366dac15c953d509a6814b48a6b9
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412183"
---
# <a name="sqrt-sm4---asm"></a><span data-ttu-id="748fa-103">Sqrt (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="748fa-103">sqrt (sm4 - asm)</span></span>

<span data-ttu-id="748fa-104">Компонентный квадратный корень.</span><span class="sxs-lookup"><span data-stu-id="748fa-104">Component-wise square root.</span></span>



| <span data-ttu-id="748fa-105">sqrt: \[ \_ \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="748fa-105">sqrt\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="748fa-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="748fa-106">Item</span></span>                                                            | <span data-ttu-id="748fa-107">Описание</span><span class="sxs-lookup"><span data-stu-id="748fa-107">Description</span></span>                                                                     |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="748fa-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="748fa-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="748fa-109">\[в \] результате операции.</span><span class="sxs-lookup"><span data-stu-id="748fa-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="748fa-110">*dest* = Sqrt (*src0*)</span><span class="sxs-lookup"><span data-stu-id="748fa-110">*dest* = sqrt(*src0*)</span></span><br/> |
| <span data-ttu-id="748fa-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="748fa-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="748fa-112">\[в \] компонентах, для которых необходимо взять квадратный корень.</span><span class="sxs-lookup"><span data-stu-id="748fa-112">\[in\] The components for which to take the square root.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="748fa-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="748fa-113">Remarks</span></span>

<span data-ttu-id="748fa-114">Точность равна 1 ulp.</span><span class="sxs-lookup"><span data-stu-id="748fa-114">Precision is 1 ulp.</span></span>

<span data-ttu-id="748fa-115">В следующей таблице показаны результаты, полученные при выполнении инструкции с различными классами чисел, предполагая, что ни переполнение, ни потеря точности не происходит.</span><span class="sxs-lookup"><span data-stu-id="748fa-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="748fa-116">F означает ограничение по настоящему вещественному числу.</span><span class="sxs-lookup"><span data-stu-id="748fa-116">F means finite-real number.</span></span>



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
|          | <span data-ttu-id="748fa-117">**-INF**</span><span class="sxs-lookup"><span data-stu-id="748fa-117">**-inf**</span></span> | <span data-ttu-id="748fa-118">**-F**</span><span class="sxs-lookup"><span data-stu-id="748fa-118">**-F**</span></span> | <span data-ttu-id="748fa-119">**— денорма**</span><span class="sxs-lookup"><span data-stu-id="748fa-119">**-denorm**</span></span> | <span data-ttu-id="748fa-120">**-0**</span><span class="sxs-lookup"><span data-stu-id="748fa-120">**-0**</span></span> | <span data-ttu-id="748fa-121">**+0**</span><span class="sxs-lookup"><span data-stu-id="748fa-121">**+0**</span></span> | <span data-ttu-id="748fa-122">**+ денорма**</span><span class="sxs-lookup"><span data-stu-id="748fa-122">**+denorm**</span></span> | <span data-ttu-id="748fa-123">**+ F**</span><span class="sxs-lookup"><span data-stu-id="748fa-123">**+F**</span></span> | <span data-ttu-id="748fa-124">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="748fa-124">**+inf**</span></span> | <span data-ttu-id="748fa-125">**Не число**</span><span class="sxs-lookup"><span data-stu-id="748fa-125">**NaN**</span></span> |
| <span data-ttu-id="748fa-126">**dest**</span><span class="sxs-lookup"><span data-stu-id="748fa-126">**dest**</span></span> | <span data-ttu-id="748fa-127">Не число</span><span class="sxs-lookup"><span data-stu-id="748fa-127">NaN</span></span>      | <span data-ttu-id="748fa-128">Не число</span><span class="sxs-lookup"><span data-stu-id="748fa-128">NaN</span></span>    | <span data-ttu-id="748fa-129">-0</span><span class="sxs-lookup"><span data-stu-id="748fa-129">-0</span></span>          | <span data-ttu-id="748fa-130">-0</span><span class="sxs-lookup"><span data-stu-id="748fa-130">-0</span></span>     | <span data-ttu-id="748fa-131">+0</span><span class="sxs-lookup"><span data-stu-id="748fa-131">+0</span></span>     | <span data-ttu-id="748fa-132">+0</span><span class="sxs-lookup"><span data-stu-id="748fa-132">+0</span></span>          | <span data-ttu-id="748fa-133">+ F</span><span class="sxs-lookup"><span data-stu-id="748fa-133">+F</span></span>     | <span data-ttu-id="748fa-134">+inf</span><span class="sxs-lookup"><span data-stu-id="748fa-134">+inf</span></span>     | <span data-ttu-id="748fa-135">не число</span><span class="sxs-lookup"><span data-stu-id="748fa-135">NaN</span></span>     |



 

<span data-ttu-id="748fa-136">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="748fa-136">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="748fa-137">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="748fa-137">Vertex Shader</span></span> | <span data-ttu-id="748fa-138">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="748fa-138">Geometry Shader</span></span> | <span data-ttu-id="748fa-139">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="748fa-139">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="748fa-140">x</span><span class="sxs-lookup"><span data-stu-id="748fa-140">x</span></span>             | <span data-ttu-id="748fa-141">x</span><span class="sxs-lookup"><span data-stu-id="748fa-141">x</span></span>               | <span data-ttu-id="748fa-142">x</span><span class="sxs-lookup"><span data-stu-id="748fa-142">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="748fa-143">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="748fa-143">Minimum Shader Model</span></span>

<span data-ttu-id="748fa-144">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="748fa-144">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="748fa-145">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="748fa-145">Shader Model</span></span>                                              | <span data-ttu-id="748fa-146">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="748fa-146">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="748fa-147">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="748fa-147">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="748fa-148">да</span><span class="sxs-lookup"><span data-stu-id="748fa-148">yes</span></span>       |
| [<span data-ttu-id="748fa-149">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="748fa-149">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="748fa-150">да</span><span class="sxs-lookup"><span data-stu-id="748fa-150">yes</span></span>       |
| [<span data-ttu-id="748fa-151">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="748fa-151">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="748fa-152">да</span><span class="sxs-lookup"><span data-stu-id="748fa-152">yes</span></span>       |
| [<span data-ttu-id="748fa-153">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="748fa-153">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="748fa-154">Нет</span><span class="sxs-lookup"><span data-stu-id="748fa-154">no</span></span>        |
| [<span data-ttu-id="748fa-155">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="748fa-155">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="748fa-156">Нет</span><span class="sxs-lookup"><span data-stu-id="748fa-156">no</span></span>        |
| [<span data-ttu-id="748fa-157">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="748fa-157">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="748fa-158">Нет</span><span class="sxs-lookup"><span data-stu-id="748fa-158">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="748fa-159">См. также</span><span class="sxs-lookup"><span data-stu-id="748fa-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="748fa-160">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="748fa-160">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





