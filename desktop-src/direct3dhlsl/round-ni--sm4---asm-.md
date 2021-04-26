---
title: round_ni (SM4-ASM)
description: Округление числа с плавающей точкой до целого числа с плавающей запятой. | round_ni (SM4-ASM)
ms.assetid: 6DEF818B-AFF9-4B44-950E-320EACE1CAC4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2487715bbb2596653b1ca985a2e0390457feecbf
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998581"
---
# <a name="round_ni-sm4---asm"></a><span data-ttu-id="d9fcc-104">Round \_ Ni (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="d9fcc-104">round\_ni (sm4 - asm)</span></span>

<span data-ttu-id="d9fcc-105">Округление числа с плавающей точкой до целого числа с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="d9fcc-105">Floating-point round to integral float.</span></span>



| <span data-ttu-id="d9fcc-106">Round \_ Ni \[ \_ \] \[ . Маска \] , \[ - \] src0 \[ \_ ABS \] \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="d9fcc-106">round\_ni\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------------|



 



| <span data-ttu-id="d9fcc-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="d9fcc-107">Item</span></span>                                                            | <span data-ttu-id="d9fcc-108">Описание</span><span class="sxs-lookup"><span data-stu-id="d9fcc-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="d9fcc-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="d9fcc-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="d9fcc-110">\[в \] адресе результатов операции.</span><span class="sxs-lookup"><span data-stu-id="d9fcc-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="d9fcc-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="d9fcc-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="d9fcc-112">\[в \] компонентах операции.</span><span class="sxs-lookup"><span data-stu-id="d9fcc-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="d9fcc-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="d9fcc-113">Remarks</span></span>

<span data-ttu-id="d9fcc-114">Эта инструкция выполняет покомпонентное округление значений с плавающей запятой в *src0*, записывая целочисленные значения с плавающей запятой в *dest*.</span><span class="sxs-lookup"><span data-stu-id="d9fcc-114">This instruction performs a component-wise floating-point round of the values in *src0*, writing integral floating-point values to *dest*.</span></span> <span data-ttu-id="d9fcc-115">**Round \_ Ni** округляет в сторону-Infinity, обычно известное как floor ().</span><span class="sxs-lookup"><span data-stu-id="d9fcc-115">**round\_ni** rounds toward -infinity, commonly known as floor().</span></span>

<span data-ttu-id="d9fcc-116">В следующей таблице показаны результаты, полученные при выполнении инструкции с различными классами чисел.</span><span class="sxs-lookup"><span data-stu-id="d9fcc-116">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>

<span data-ttu-id="d9fcc-117">F означает ограничение по настоящему вещественному числу.</span><span class="sxs-lookup"><span data-stu-id="d9fcc-117">F means finite-real number.</span></span>



| <span data-ttu-id="d9fcc-118">**src**</span><span class="sxs-lookup"><span data-stu-id="d9fcc-118">**src**</span></span>  | <span data-ttu-id="d9fcc-119">**-INF**</span><span class="sxs-lookup"><span data-stu-id="d9fcc-119">**-inf**</span></span> | <span data-ttu-id="d9fcc-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="d9fcc-120">**-F**</span></span> | <span data-ttu-id="d9fcc-121">**— денорма**</span><span class="sxs-lookup"><span data-stu-id="d9fcc-121">**-denorm**</span></span> | <span data-ttu-id="d9fcc-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="d9fcc-122">**-0**</span></span> | <span data-ttu-id="d9fcc-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="d9fcc-123">**+0**</span></span> | <span data-ttu-id="d9fcc-124">**+ денорма**</span><span class="sxs-lookup"><span data-stu-id="d9fcc-124">**+denorm**</span></span> | <span data-ttu-id="d9fcc-125">**+ F**</span><span class="sxs-lookup"><span data-stu-id="d9fcc-125">**+F**</span></span> | <span data-ttu-id="d9fcc-126">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="d9fcc-126">**+inf**</span></span> | <span data-ttu-id="d9fcc-127">**Не число**</span><span class="sxs-lookup"><span data-stu-id="d9fcc-127">**NaN**</span></span> |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="d9fcc-128">**dest**</span><span class="sxs-lookup"><span data-stu-id="d9fcc-128">**dest**</span></span> | <span data-ttu-id="d9fcc-129">-inf</span><span class="sxs-lookup"><span data-stu-id="d9fcc-129">-inf</span></span>     | <span data-ttu-id="d9fcc-130">-F</span><span class="sxs-lookup"><span data-stu-id="d9fcc-130">-F</span></span>     | <span data-ttu-id="d9fcc-131">-0</span><span class="sxs-lookup"><span data-stu-id="d9fcc-131">-0</span></span>          | <span data-ttu-id="d9fcc-132">-0</span><span class="sxs-lookup"><span data-stu-id="d9fcc-132">-0</span></span>     | <span data-ttu-id="d9fcc-133">+0</span><span class="sxs-lookup"><span data-stu-id="d9fcc-133">+0</span></span>     | <span data-ttu-id="d9fcc-134">+0</span><span class="sxs-lookup"><span data-stu-id="d9fcc-134">+0</span></span>          | <span data-ttu-id="d9fcc-135">+ F</span><span class="sxs-lookup"><span data-stu-id="d9fcc-135">+F</span></span>     | <span data-ttu-id="d9fcc-136">+inf</span><span class="sxs-lookup"><span data-stu-id="d9fcc-136">+inf</span></span>     | <span data-ttu-id="d9fcc-137">не число</span><span class="sxs-lookup"><span data-stu-id="d9fcc-137">NaN</span></span>     |



 

<span data-ttu-id="d9fcc-138">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="d9fcc-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d9fcc-139">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="d9fcc-139">Vertex Shader</span></span> | <span data-ttu-id="d9fcc-140">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="d9fcc-140">Geometry Shader</span></span> | <span data-ttu-id="d9fcc-141">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="d9fcc-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="d9fcc-142">x</span><span class="sxs-lookup"><span data-stu-id="d9fcc-142">x</span></span>             | <span data-ttu-id="d9fcc-143">x</span><span class="sxs-lookup"><span data-stu-id="d9fcc-143">x</span></span>               | <span data-ttu-id="d9fcc-144">x</span><span class="sxs-lookup"><span data-stu-id="d9fcc-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d9fcc-145">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="d9fcc-145">Minimum Shader Model</span></span>

<span data-ttu-id="d9fcc-146">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="d9fcc-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d9fcc-147">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="d9fcc-147">Shader Model</span></span>                                              | <span data-ttu-id="d9fcc-148">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="d9fcc-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d9fcc-149">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="d9fcc-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d9fcc-150">да</span><span class="sxs-lookup"><span data-stu-id="d9fcc-150">yes</span></span>       |
| [<span data-ttu-id="d9fcc-151">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="d9fcc-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d9fcc-152">да</span><span class="sxs-lookup"><span data-stu-id="d9fcc-152">yes</span></span>       |
| [<span data-ttu-id="d9fcc-153">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="d9fcc-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d9fcc-154">да</span><span class="sxs-lookup"><span data-stu-id="d9fcc-154">yes</span></span>       |
| [<span data-ttu-id="d9fcc-155">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d9fcc-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d9fcc-156">Нет</span><span class="sxs-lookup"><span data-stu-id="d9fcc-156">no</span></span>        |
| [<span data-ttu-id="d9fcc-157">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d9fcc-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d9fcc-158">Нет</span><span class="sxs-lookup"><span data-stu-id="d9fcc-158">no</span></span>        |
| [<span data-ttu-id="d9fcc-159">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d9fcc-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d9fcc-160">Нет</span><span class="sxs-lookup"><span data-stu-id="d9fcc-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d9fcc-161">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="d9fcc-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9fcc-162">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d9fcc-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





