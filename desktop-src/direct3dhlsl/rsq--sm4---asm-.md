---
title: РСК (SM4-ASM)
description: Поэлементный квадратный корень на уровне компонентов.
ms.assetid: CDA3C2DF-2793-4CE3-87CE-4E0AA945A1BB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1528e9f187ff7d4fb6074d42a1c574686f3b22f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998171"
---
# <a name="rsq-sm4---asm"></a><span data-ttu-id="d3f7c-103">РСК (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="d3f7c-103">rsq (sm4 - asm)</span></span>

<span data-ttu-id="d3f7c-104">Поэлементный квадратный корень на уровне компонентов.</span><span class="sxs-lookup"><span data-stu-id="d3f7c-104">Component-wise reciprocal square root.</span></span>



| <span data-ttu-id="d3f7c-105">РСК \[ \_ \] \[ . Маска \] , \[ - \] src0 \[ \_ ABS \] \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="d3f7c-105">rsq\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="d3f7c-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="d3f7c-106">Item</span></span>                                                            | <span data-ttu-id="d3f7c-107">Описание</span><span class="sxs-lookup"><span data-stu-id="d3f7c-107">Description</span></span>                                                                                      |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3f7c-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="d3f7c-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="d3f7c-109">\[в \] содержит результаты операции.</span><span class="sxs-lookup"><span data-stu-id="d3f7c-109">\[in\] Contains the results of the operation.</span></span><br/> <span data-ttu-id="d3f7c-110">*dest* = 1.0 f/Sqrt (*src0*)</span><span class="sxs-lookup"><span data-stu-id="d3f7c-110">*dest* = 1.0f / sqrt(*src0*)</span></span><br/> |
| <span data-ttu-id="d3f7c-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="d3f7c-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="d3f7c-112">\[в \] компонентах для операции.</span><span class="sxs-lookup"><span data-stu-id="d3f7c-112">\[in\] The components for the operation.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="d3f7c-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="d3f7c-113">Remarks</span></span>

<span data-ttu-id="d3f7c-114">Максимальная относительная ошибка — 2-21.</span><span class="sxs-lookup"><span data-stu-id="d3f7c-114">The maximum relative error is 2-21.</span></span>

<span data-ttu-id="d3f7c-115">В следующей таблице показаны результаты, полученные при выполнении инструкции с различными классами чисел, предполагая, что ни переполнение, ни потеря точности не происходит.</span><span class="sxs-lookup"><span data-stu-id="d3f7c-115">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span>

<span data-ttu-id="d3f7c-116">F означает ограничение по настоящему вещественному числу.</span><span class="sxs-lookup"><span data-stu-id="d3f7c-116">F means finite-real number.</span></span>



| <span data-ttu-id="d3f7c-117">**src**</span><span class="sxs-lookup"><span data-stu-id="d3f7c-117">**src**</span></span>  | <span data-ttu-id="d3f7c-118">**-INF**</span><span class="sxs-lookup"><span data-stu-id="d3f7c-118">**-inf**</span></span> | <span data-ttu-id="d3f7c-119">**-F**</span><span class="sxs-lookup"><span data-stu-id="d3f7c-119">**-F**</span></span> | <span data-ttu-id="d3f7c-120">**— денорма**</span><span class="sxs-lookup"><span data-stu-id="d3f7c-120">**-denorm**</span></span> | <span data-ttu-id="d3f7c-121">**-0**</span><span class="sxs-lookup"><span data-stu-id="d3f7c-121">**-0**</span></span> | <span data-ttu-id="d3f7c-122">**+0**</span><span class="sxs-lookup"><span data-stu-id="d3f7c-122">**+0**</span></span> | <span data-ttu-id="d3f7c-123">**+ денорма**</span><span class="sxs-lookup"><span data-stu-id="d3f7c-123">**+denorm**</span></span> | <span data-ttu-id="d3f7c-124">**+ F**</span><span class="sxs-lookup"><span data-stu-id="d3f7c-124">**+F**</span></span> | <span data-ttu-id="d3f7c-125">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="d3f7c-125">**+inf**</span></span> | <span data-ttu-id="d3f7c-126">**Не число**</span><span class="sxs-lookup"><span data-stu-id="d3f7c-126">**NaN**</span></span> |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="d3f7c-127">**dest**</span><span class="sxs-lookup"><span data-stu-id="d3f7c-127">**dest**</span></span> | <span data-ttu-id="d3f7c-128">Не число</span><span class="sxs-lookup"><span data-stu-id="d3f7c-128">NaN</span></span>      | <span data-ttu-id="d3f7c-129">Не число</span><span class="sxs-lookup"><span data-stu-id="d3f7c-129">NaN</span></span>    | <span data-ttu-id="d3f7c-130">-inf</span><span class="sxs-lookup"><span data-stu-id="d3f7c-130">-inf</span></span>        | <span data-ttu-id="d3f7c-131">-inf</span><span class="sxs-lookup"><span data-stu-id="d3f7c-131">-inf</span></span>   | <span data-ttu-id="d3f7c-132">+inf</span><span class="sxs-lookup"><span data-stu-id="d3f7c-132">+inf</span></span>   | <span data-ttu-id="d3f7c-133">+inf</span><span class="sxs-lookup"><span data-stu-id="d3f7c-133">+inf</span></span>        | <span data-ttu-id="d3f7c-134">+ F</span><span class="sxs-lookup"><span data-stu-id="d3f7c-134">+F</span></span>     | <span data-ttu-id="d3f7c-135">+0</span><span class="sxs-lookup"><span data-stu-id="d3f7c-135">+0</span></span>       | <span data-ttu-id="d3f7c-136">Не число</span><span class="sxs-lookup"><span data-stu-id="d3f7c-136">NaN</span></span>     |



 

<span data-ttu-id="d3f7c-137">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="d3f7c-137">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d3f7c-138">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="d3f7c-138">Vertex Shader</span></span> | <span data-ttu-id="d3f7c-139">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="d3f7c-139">Geometry Shader</span></span> | <span data-ttu-id="d3f7c-140">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="d3f7c-140">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="d3f7c-141">x</span><span class="sxs-lookup"><span data-stu-id="d3f7c-141">x</span></span>             | <span data-ttu-id="d3f7c-142">x</span><span class="sxs-lookup"><span data-stu-id="d3f7c-142">x</span></span>               | <span data-ttu-id="d3f7c-143">x</span><span class="sxs-lookup"><span data-stu-id="d3f7c-143">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d3f7c-144">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="d3f7c-144">Minimum Shader Model</span></span>

<span data-ttu-id="d3f7c-145">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="d3f7c-145">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d3f7c-146">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="d3f7c-146">Shader Model</span></span>                                              | <span data-ttu-id="d3f7c-147">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="d3f7c-147">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d3f7c-148">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="d3f7c-148">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d3f7c-149">да</span><span class="sxs-lookup"><span data-stu-id="d3f7c-149">yes</span></span>       |
| [<span data-ttu-id="d3f7c-150">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="d3f7c-150">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d3f7c-151">да</span><span class="sxs-lookup"><span data-stu-id="d3f7c-151">yes</span></span>       |
| [<span data-ttu-id="d3f7c-152">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="d3f7c-152">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d3f7c-153">да</span><span class="sxs-lookup"><span data-stu-id="d3f7c-153">yes</span></span>       |
| [<span data-ttu-id="d3f7c-154">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d3f7c-154">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d3f7c-155">Нет</span><span class="sxs-lookup"><span data-stu-id="d3f7c-155">no</span></span>        |
| [<span data-ttu-id="d3f7c-156">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d3f7c-156">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d3f7c-157">Нет</span><span class="sxs-lookup"><span data-stu-id="d3f7c-157">no</span></span>        |
| [<span data-ttu-id="d3f7c-158">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d3f7c-158">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d3f7c-159">Нет</span><span class="sxs-lookup"><span data-stu-id="d3f7c-159">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d3f7c-160">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="d3f7c-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3f7c-161">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d3f7c-161">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





