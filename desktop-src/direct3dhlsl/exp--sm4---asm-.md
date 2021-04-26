---
title: EXP (SM4-ASM)
description: 2exponent на уровне компонентов.
ms.assetid: 12EB865A-BF71-4B4B-854F-9DA056B18AE0
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b24c74394a5e8ac7a6c945e2c9b63e6f242daa1
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999081"
---
# <a name="exp-sm4---asm"></a><span data-ttu-id="9270d-103">EXP (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="9270d-103">exp (sm4 - asm)</span></span>

<span data-ttu-id="9270d-104">2exponent на уровне компонентов.</span><span class="sxs-lookup"><span data-stu-id="9270d-104">Component-wise 2exponent.</span></span>



| <span data-ttu-id="9270d-105">EXP \[ \_ \] , адрес \[ , маска \] , \[ - \] src0 \[ \_ ABS \] \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="9270d-105">exp\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="9270d-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="9270d-106">Item</span></span>                                                            | <span data-ttu-id="9270d-107">Описание</span><span class="sxs-lookup"><span data-stu-id="9270d-107">Description</span></span>                                                                |
|-----------------------------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="9270d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="9270d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="9270d-109">\[в \] результате операции.</span><span class="sxs-lookup"><span data-stu-id="9270d-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="9270d-110">*dest* = 2 *src0*</span><span class="sxs-lookup"><span data-stu-id="9270d-110">*dest* = 2 *src0*</span></span><br/> |
| <span data-ttu-id="9270d-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="9270d-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="9270d-112">\[в \] экспоненте.</span><span class="sxs-lookup"><span data-stu-id="9270d-112">\[in\] The exponent.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="9270d-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="9270d-113">Remarks</span></span>

<span data-ttu-id="9270d-114">Эта инструкция соответствует теории ограничений.</span><span class="sxs-lookup"><span data-stu-id="9270d-114">This instruction follows limit theory.</span></span> <span data-ttu-id="9270d-115">Максимальная относительная ошибка — 2-21.</span><span class="sxs-lookup"><span data-stu-id="9270d-115">The maximum relative error is 2-21.</span></span>

<span data-ttu-id="9270d-116">В следующей таблице показаны результаты, полученные при выполнении инструкции с различными классами чисел, предполагая, что ни переполнение, ни потеря точности не происходит.</span><span class="sxs-lookup"><span data-stu-id="9270d-116">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="9270d-117">В этой таблице F означает ограничение по настоящему вещественному числу.</span><span class="sxs-lookup"><span data-stu-id="9270d-117">In this table F means finite-real number.</span></span>



| <span data-ttu-id="9270d-118">**src**</span><span class="sxs-lookup"><span data-stu-id="9270d-118">**src**</span></span>  | <span data-ttu-id="9270d-119">**-INF**</span><span class="sxs-lookup"><span data-stu-id="9270d-119">**-inf**</span></span> | <span data-ttu-id="9270d-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="9270d-120">**-F**</span></span> | <span data-ttu-id="9270d-121">**— денорма**</span><span class="sxs-lookup"><span data-stu-id="9270d-121">**-denorm**</span></span> | <span data-ttu-id="9270d-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="9270d-122">**-0**</span></span> | <span data-ttu-id="9270d-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="9270d-123">**+0**</span></span> | <span data-ttu-id="9270d-124">**+ денорма**</span><span class="sxs-lookup"><span data-stu-id="9270d-124">**+denorm**</span></span> | <span data-ttu-id="9270d-125">**+ F**</span><span class="sxs-lookup"><span data-stu-id="9270d-125">**+F**</span></span> | <span data-ttu-id="9270d-126">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="9270d-126">**+inf**</span></span> | <span data-ttu-id="9270d-127">**Не число**</span><span class="sxs-lookup"><span data-stu-id="9270d-127">**NaN**</span></span> |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="9270d-128">**dest**</span><span class="sxs-lookup"><span data-stu-id="9270d-128">**dest**</span></span> | <span data-ttu-id="9270d-129">0</span><span class="sxs-lookup"><span data-stu-id="9270d-129">0</span></span>        | <span data-ttu-id="9270d-130">+ F</span><span class="sxs-lookup"><span data-stu-id="9270d-130">+F</span></span>     | <span data-ttu-id="9270d-131">1</span><span class="sxs-lookup"><span data-stu-id="9270d-131">1</span></span>           | <span data-ttu-id="9270d-132">1</span><span class="sxs-lookup"><span data-stu-id="9270d-132">1</span></span>      | <span data-ttu-id="9270d-133">1</span><span class="sxs-lookup"><span data-stu-id="9270d-133">1</span></span>      | <span data-ttu-id="9270d-134">1</span><span class="sxs-lookup"><span data-stu-id="9270d-134">1</span></span>           | <span data-ttu-id="9270d-135">+ F</span><span class="sxs-lookup"><span data-stu-id="9270d-135">+F</span></span>     | <span data-ttu-id="9270d-136">+inf</span><span class="sxs-lookup"><span data-stu-id="9270d-136">+inf</span></span>     | <span data-ttu-id="9270d-137">не число</span><span class="sxs-lookup"><span data-stu-id="9270d-137">NaN</span></span>     |



 

<span data-ttu-id="9270d-138">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="9270d-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9270d-139">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="9270d-139">Vertex Shader</span></span> | <span data-ttu-id="9270d-140">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="9270d-140">Geometry Shader</span></span> | <span data-ttu-id="9270d-141">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="9270d-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="9270d-142">x</span><span class="sxs-lookup"><span data-stu-id="9270d-142">x</span></span>             | <span data-ttu-id="9270d-143">x</span><span class="sxs-lookup"><span data-stu-id="9270d-143">x</span></span>               | <span data-ttu-id="9270d-144">x</span><span class="sxs-lookup"><span data-stu-id="9270d-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9270d-145">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="9270d-145">Minimum Shader Model</span></span>

<span data-ttu-id="9270d-146">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="9270d-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="9270d-147">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="9270d-147">Shader Model</span></span>                                              | <span data-ttu-id="9270d-148">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="9270d-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9270d-149">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="9270d-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9270d-150">да</span><span class="sxs-lookup"><span data-stu-id="9270d-150">yes</span></span>       |
| [<span data-ttu-id="9270d-151">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="9270d-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9270d-152">да</span><span class="sxs-lookup"><span data-stu-id="9270d-152">yes</span></span>       |
| [<span data-ttu-id="9270d-153">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="9270d-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9270d-154">да</span><span class="sxs-lookup"><span data-stu-id="9270d-154">yes</span></span>       |
| [<span data-ttu-id="9270d-155">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9270d-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9270d-156">Нет</span><span class="sxs-lookup"><span data-stu-id="9270d-156">no</span></span>        |
| [<span data-ttu-id="9270d-157">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9270d-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9270d-158">Нет</span><span class="sxs-lookup"><span data-stu-id="9270d-158">no</span></span>        |
| [<span data-ttu-id="9270d-159">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9270d-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9270d-160">Нет</span><span class="sxs-lookup"><span data-stu-id="9270d-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9270d-161">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="9270d-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9270d-162">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9270d-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





