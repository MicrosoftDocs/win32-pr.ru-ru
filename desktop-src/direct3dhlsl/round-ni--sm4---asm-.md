---
title: round_ni (SM4-ASM)
description: Округление числа с плавающей точкой до целого числа с плавающей запятой. | round_ni (SM4-ASM)
ms.assetid: 6DEF818B-AFF9-4B44-950E-320EACE1CAC4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3daafd64e76bd8c04acf7812b096f7374befef6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104081796"
---
# <a name="round_ni-sm4---asm"></a><span data-ttu-id="57ea4-104">Round \_ Ni (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="57ea4-104">round\_ni (sm4 - asm)</span></span>

<span data-ttu-id="57ea4-105">Округление числа с плавающей точкой до целого числа с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="57ea4-105">Floating-point round to integral float.</span></span>



| <span data-ttu-id="57ea4-106">Round \_ Ni \[ \_ \] \[ . Маска \] , \[ - \] src0 \[ \_ ABS \] \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="57ea4-106">round\_ni\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------------|



 



| <span data-ttu-id="57ea4-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="57ea4-107">Item</span></span>                                                            | <span data-ttu-id="57ea4-108">Описание</span><span class="sxs-lookup"><span data-stu-id="57ea4-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="57ea4-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="57ea4-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="57ea4-110">\[в \] адресе результатов операции.</span><span class="sxs-lookup"><span data-stu-id="57ea4-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="57ea4-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="57ea4-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="57ea4-112">\[в \] компонентах операции.</span><span class="sxs-lookup"><span data-stu-id="57ea4-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="57ea4-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="57ea4-113">Remarks</span></span>

<span data-ttu-id="57ea4-114">Эта инструкция выполняет покомпонентное округление значений с плавающей запятой в *src0*, записывая целочисленные значения с плавающей запятой в *dest*.</span><span class="sxs-lookup"><span data-stu-id="57ea4-114">This instruction performs a component-wise floating-point round of the values in *src0*, writing integral floating-point values to *dest*.</span></span> <span data-ttu-id="57ea4-115">**Round \_ Ni** округляет в сторону-Infinity, обычно известное как floor ().</span><span class="sxs-lookup"><span data-stu-id="57ea4-115">**round\_ni** rounds toward -infinity, commonly known as floor().</span></span>

<span data-ttu-id="57ea4-116">В следующей таблице показаны результаты, полученные при выполнении инструкции с различными классами чисел.</span><span class="sxs-lookup"><span data-stu-id="57ea4-116">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>

<span data-ttu-id="57ea4-117">F означает ограничение по настоящему вещественному числу.</span><span class="sxs-lookup"><span data-stu-id="57ea4-117">F means finite-real number.</span></span>



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="57ea4-118">**src**</span><span class="sxs-lookup"><span data-stu-id="57ea4-118">**src**</span></span>  | <span data-ttu-id="57ea4-119">**-INF**</span><span class="sxs-lookup"><span data-stu-id="57ea4-119">**-inf**</span></span> | <span data-ttu-id="57ea4-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="57ea4-120">**-F**</span></span> | <span data-ttu-id="57ea4-121">**— денорма**</span><span class="sxs-lookup"><span data-stu-id="57ea4-121">**-denorm**</span></span> | <span data-ttu-id="57ea4-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="57ea4-122">**-0**</span></span> | <span data-ttu-id="57ea4-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="57ea4-123">**+0**</span></span> | <span data-ttu-id="57ea4-124">**+ денорма**</span><span class="sxs-lookup"><span data-stu-id="57ea4-124">**+denorm**</span></span> | <span data-ttu-id="57ea4-125">**+ F**</span><span class="sxs-lookup"><span data-stu-id="57ea4-125">**+F**</span></span> | <span data-ttu-id="57ea4-126">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="57ea4-126">**+inf**</span></span> | <span data-ttu-id="57ea4-127">**Не число**</span><span class="sxs-lookup"><span data-stu-id="57ea4-127">**NaN**</span></span> |
| <span data-ttu-id="57ea4-128">**dest**</span><span class="sxs-lookup"><span data-stu-id="57ea4-128">**dest**</span></span> | <span data-ttu-id="57ea4-129">-inf</span><span class="sxs-lookup"><span data-stu-id="57ea4-129">-inf</span></span>     | <span data-ttu-id="57ea4-130">-F</span><span class="sxs-lookup"><span data-stu-id="57ea4-130">-F</span></span>     | <span data-ttu-id="57ea4-131">-0</span><span class="sxs-lookup"><span data-stu-id="57ea4-131">-0</span></span>          | <span data-ttu-id="57ea4-132">-0</span><span class="sxs-lookup"><span data-stu-id="57ea4-132">-0</span></span>     | <span data-ttu-id="57ea4-133">+0</span><span class="sxs-lookup"><span data-stu-id="57ea4-133">+0</span></span>     | <span data-ttu-id="57ea4-134">+0</span><span class="sxs-lookup"><span data-stu-id="57ea4-134">+0</span></span>          | <span data-ttu-id="57ea4-135">+ F</span><span class="sxs-lookup"><span data-stu-id="57ea4-135">+F</span></span>     | <span data-ttu-id="57ea4-136">+inf</span><span class="sxs-lookup"><span data-stu-id="57ea4-136">+inf</span></span>     | <span data-ttu-id="57ea4-137">не число</span><span class="sxs-lookup"><span data-stu-id="57ea4-137">NaN</span></span>     |



 

<span data-ttu-id="57ea4-138">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="57ea4-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="57ea4-139">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="57ea4-139">Vertex Shader</span></span> | <span data-ttu-id="57ea4-140">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="57ea4-140">Geometry Shader</span></span> | <span data-ttu-id="57ea4-141">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="57ea4-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="57ea4-142">x</span><span class="sxs-lookup"><span data-stu-id="57ea4-142">x</span></span>             | <span data-ttu-id="57ea4-143">x</span><span class="sxs-lookup"><span data-stu-id="57ea4-143">x</span></span>               | <span data-ttu-id="57ea4-144">x</span><span class="sxs-lookup"><span data-stu-id="57ea4-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="57ea4-145">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="57ea4-145">Minimum Shader Model</span></span>

<span data-ttu-id="57ea4-146">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="57ea4-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="57ea4-147">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="57ea4-147">Shader Model</span></span>                                              | <span data-ttu-id="57ea4-148">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="57ea4-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="57ea4-149">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="57ea4-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="57ea4-150">да</span><span class="sxs-lookup"><span data-stu-id="57ea4-150">yes</span></span>       |
| [<span data-ttu-id="57ea4-151">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="57ea4-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="57ea4-152">да</span><span class="sxs-lookup"><span data-stu-id="57ea4-152">yes</span></span>       |
| [<span data-ttu-id="57ea4-153">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="57ea4-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="57ea4-154">да</span><span class="sxs-lookup"><span data-stu-id="57ea4-154">yes</span></span>       |
| [<span data-ttu-id="57ea4-155">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="57ea4-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="57ea4-156">Нет</span><span class="sxs-lookup"><span data-stu-id="57ea4-156">no</span></span>        |
| [<span data-ttu-id="57ea4-157">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="57ea4-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="57ea4-158">Нет</span><span class="sxs-lookup"><span data-stu-id="57ea4-158">no</span></span>        |
| [<span data-ttu-id="57ea4-159">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="57ea4-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="57ea4-160">Нет</span><span class="sxs-lookup"><span data-stu-id="57ea4-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="57ea4-161">См. также</span><span class="sxs-lookup"><span data-stu-id="57ea4-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57ea4-162">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="57ea4-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





