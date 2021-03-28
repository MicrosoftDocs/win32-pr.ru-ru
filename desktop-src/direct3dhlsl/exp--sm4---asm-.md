---
title: EXP (SM4-ASM)
description: 2exponent на уровне компонентов.
ms.assetid: 12EB865A-BF71-4B4B-854F-9DA056B18AE0
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 774be1230bdb02a6179ea5662ca2237c2cefc200
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104069322"
---
# <a name="exp-sm4---asm"></a><span data-ttu-id="ce95e-103">EXP (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="ce95e-103">exp (sm4 - asm)</span></span>

<span data-ttu-id="ce95e-104">2exponent на уровне компонентов.</span><span class="sxs-lookup"><span data-stu-id="ce95e-104">Component-wise 2exponent.</span></span>



| <span data-ttu-id="ce95e-105">EXP \[ \_ \] , адрес \[ , маска \] , \[ - \] src0 \[ \_ ABS \] \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="ce95e-105">exp\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------|



 



| <span data-ttu-id="ce95e-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="ce95e-106">Item</span></span>                                                            | <span data-ttu-id="ce95e-107">Описание</span><span class="sxs-lookup"><span data-stu-id="ce95e-107">Description</span></span>                                                                |
|-----------------------------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="ce95e-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="ce95e-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="ce95e-109">\[в \] результате операции.</span><span class="sxs-lookup"><span data-stu-id="ce95e-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="ce95e-110">*dest* = 2 *src0*</span><span class="sxs-lookup"><span data-stu-id="ce95e-110">*dest* = 2 *src0*</span></span><br/> |
| <span data-ttu-id="ce95e-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="ce95e-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="ce95e-112">\[в \] экспоненте.</span><span class="sxs-lookup"><span data-stu-id="ce95e-112">\[in\] The exponent.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="ce95e-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="ce95e-113">Remarks</span></span>

<span data-ttu-id="ce95e-114">Эта инструкция соответствует теории ограничений.</span><span class="sxs-lookup"><span data-stu-id="ce95e-114">This instruction follows limit theory.</span></span> <span data-ttu-id="ce95e-115">Максимальная относительная ошибка — 2-21.</span><span class="sxs-lookup"><span data-stu-id="ce95e-115">The maximum relative error is 2-21.</span></span>

<span data-ttu-id="ce95e-116">В следующей таблице показаны результаты, полученные при выполнении инструкции с различными классами чисел, предполагая, что ни переполнение, ни потеря точности не происходит.</span><span class="sxs-lookup"><span data-stu-id="ce95e-116">The following table shows the results obtained when executing the instruction with various classes of numbers, assuming that neither overflow or underflow occurs.</span></span> <span data-ttu-id="ce95e-117">В этой таблице F означает ограничение по настоящему вещественному числу.</span><span class="sxs-lookup"><span data-stu-id="ce95e-117">In this table F means finite-real number.</span></span>



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="ce95e-118">**src**</span><span class="sxs-lookup"><span data-stu-id="ce95e-118">**src**</span></span>  | <span data-ttu-id="ce95e-119">**-INF**</span><span class="sxs-lookup"><span data-stu-id="ce95e-119">**-inf**</span></span> | <span data-ttu-id="ce95e-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="ce95e-120">**-F**</span></span> | <span data-ttu-id="ce95e-121">**— денорма**</span><span class="sxs-lookup"><span data-stu-id="ce95e-121">**-denorm**</span></span> | <span data-ttu-id="ce95e-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="ce95e-122">**-0**</span></span> | <span data-ttu-id="ce95e-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="ce95e-123">**+0**</span></span> | <span data-ttu-id="ce95e-124">**+ денорма**</span><span class="sxs-lookup"><span data-stu-id="ce95e-124">**+denorm**</span></span> | <span data-ttu-id="ce95e-125">**+ F**</span><span class="sxs-lookup"><span data-stu-id="ce95e-125">**+F**</span></span> | <span data-ttu-id="ce95e-126">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="ce95e-126">**+inf**</span></span> | <span data-ttu-id="ce95e-127">**Не число**</span><span class="sxs-lookup"><span data-stu-id="ce95e-127">**NaN**</span></span> |
| <span data-ttu-id="ce95e-128">**dest**</span><span class="sxs-lookup"><span data-stu-id="ce95e-128">**dest**</span></span> | <span data-ttu-id="ce95e-129">0</span><span class="sxs-lookup"><span data-stu-id="ce95e-129">0</span></span>        | <span data-ttu-id="ce95e-130">+ F</span><span class="sxs-lookup"><span data-stu-id="ce95e-130">+F</span></span>     | <span data-ttu-id="ce95e-131">1</span><span class="sxs-lookup"><span data-stu-id="ce95e-131">1</span></span>           | <span data-ttu-id="ce95e-132">1</span><span class="sxs-lookup"><span data-stu-id="ce95e-132">1</span></span>      | <span data-ttu-id="ce95e-133">1</span><span class="sxs-lookup"><span data-stu-id="ce95e-133">1</span></span>      | <span data-ttu-id="ce95e-134">1</span><span class="sxs-lookup"><span data-stu-id="ce95e-134">1</span></span>           | <span data-ttu-id="ce95e-135">+ F</span><span class="sxs-lookup"><span data-stu-id="ce95e-135">+F</span></span>     | <span data-ttu-id="ce95e-136">+inf</span><span class="sxs-lookup"><span data-stu-id="ce95e-136">+inf</span></span>     | <span data-ttu-id="ce95e-137">не число</span><span class="sxs-lookup"><span data-stu-id="ce95e-137">NaN</span></span>     |



 

<span data-ttu-id="ce95e-138">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="ce95e-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ce95e-139">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="ce95e-139">Vertex Shader</span></span> | <span data-ttu-id="ce95e-140">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="ce95e-140">Geometry Shader</span></span> | <span data-ttu-id="ce95e-141">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="ce95e-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="ce95e-142">x</span><span class="sxs-lookup"><span data-stu-id="ce95e-142">x</span></span>             | <span data-ttu-id="ce95e-143">x</span><span class="sxs-lookup"><span data-stu-id="ce95e-143">x</span></span>               | <span data-ttu-id="ce95e-144">x</span><span class="sxs-lookup"><span data-stu-id="ce95e-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ce95e-145">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ce95e-145">Minimum Shader Model</span></span>

<span data-ttu-id="ce95e-146">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="ce95e-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ce95e-147">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="ce95e-147">Shader Model</span></span>                                              | <span data-ttu-id="ce95e-148">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="ce95e-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ce95e-149">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="ce95e-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ce95e-150">да</span><span class="sxs-lookup"><span data-stu-id="ce95e-150">yes</span></span>       |
| [<span data-ttu-id="ce95e-151">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="ce95e-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ce95e-152">да</span><span class="sxs-lookup"><span data-stu-id="ce95e-152">yes</span></span>       |
| [<span data-ttu-id="ce95e-153">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="ce95e-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ce95e-154">да</span><span class="sxs-lookup"><span data-stu-id="ce95e-154">yes</span></span>       |
| [<span data-ttu-id="ce95e-155">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ce95e-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ce95e-156">Нет</span><span class="sxs-lookup"><span data-stu-id="ce95e-156">no</span></span>        |
| [<span data-ttu-id="ce95e-157">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ce95e-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ce95e-158">Нет</span><span class="sxs-lookup"><span data-stu-id="ce95e-158">no</span></span>        |
| [<span data-ttu-id="ce95e-159">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ce95e-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ce95e-160">Нет</span><span class="sxs-lookup"><span data-stu-id="ce95e-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ce95e-161">См. также</span><span class="sxs-lookup"><span data-stu-id="ce95e-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce95e-162">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ce95e-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





