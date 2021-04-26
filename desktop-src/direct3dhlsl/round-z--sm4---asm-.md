---
title: round_z (SM4-ASM)
description: Округление числа с плавающей точкой до целого числа с плавающей запятой. | round_z (SM4-ASM)
ms.assetid: 97C0E0F2-2571-4A94-BB04-B0CDBA0B5C0C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc874c6d0a1f26902086af300784c55950b71569
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997131"
---
# <a name="round_z-sm4---asm"></a><span data-ttu-id="f11d5-104">Round \_ z (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="f11d5-104">round\_z (sm4 - asm)</span></span>

<span data-ttu-id="f11d5-105">Округление числа с плавающей точкой до целого числа с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="f11d5-105">Floating-point round to integral float.</span></span>



| <span data-ttu-id="f11d5-106">Скругление \_ z \[ \_ \] , назначение \[ маски \] , \[ - \] src0 \[ \_ ABS \] \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="f11d5-106">round\_z\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|-----------------------------------------------------------------|



 



| <span data-ttu-id="f11d5-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="f11d5-107">Item</span></span>                                                            | <span data-ttu-id="f11d5-108">Описание</span><span class="sxs-lookup"><span data-stu-id="f11d5-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="f11d5-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="f11d5-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="f11d5-110">\[в \] адресе результатов операции.</span><span class="sxs-lookup"><span data-stu-id="f11d5-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="f11d5-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="f11d5-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="f11d5-112">\[в \] компонентах операции.</span><span class="sxs-lookup"><span data-stu-id="f11d5-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="f11d5-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="f11d5-113">Remarks</span></span>

<span data-ttu-id="f11d5-114">Эта инструкция выполняет покомпонентное округление значений с плавающей запятой в *src0*, записывая целочисленные значения с плавающей запятой в *dest*.</span><span class="sxs-lookup"><span data-stu-id="f11d5-114">This instruction performs a component-wise floating-point round of the values in *src0*, writing integral floating-point values to *dest*.</span></span>

<span data-ttu-id="f11d5-115">**Округление \_ z** округляет в сторону нуля.</span><span class="sxs-lookup"><span data-stu-id="f11d5-115">**round\_z** rounds towards zero.</span></span>

<span data-ttu-id="f11d5-116">В следующей таблице показаны результаты, полученные при выполнении инструкции с различными классами чисел.</span><span class="sxs-lookup"><span data-stu-id="f11d5-116">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>



| <span data-ttu-id="f11d5-117">**src**</span><span class="sxs-lookup"><span data-stu-id="f11d5-117">**src**</span></span>  | <span data-ttu-id="f11d5-118">**-INF**</span><span class="sxs-lookup"><span data-stu-id="f11d5-118">**-inf**</span></span> | <span data-ttu-id="f11d5-119">**-F**</span><span class="sxs-lookup"><span data-stu-id="f11d5-119">**-F**</span></span> | <span data-ttu-id="f11d5-120">**— денорма**</span><span class="sxs-lookup"><span data-stu-id="f11d5-120">**-denorm**</span></span> | <span data-ttu-id="f11d5-121">**-0**</span><span class="sxs-lookup"><span data-stu-id="f11d5-121">**-0**</span></span> | <span data-ttu-id="f11d5-122">**+0**</span><span class="sxs-lookup"><span data-stu-id="f11d5-122">**+0**</span></span> | <span data-ttu-id="f11d5-123">**+ денорма**</span><span class="sxs-lookup"><span data-stu-id="f11d5-123">**+denorm**</span></span> | <span data-ttu-id="f11d5-124">**+ F**</span><span class="sxs-lookup"><span data-stu-id="f11d5-124">**+F**</span></span> | <span data-ttu-id="f11d5-125">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="f11d5-125">**+inf**</span></span> | <span data-ttu-id="f11d5-126">**Не число**</span><span class="sxs-lookup"><span data-stu-id="f11d5-126">**NaN**</span></span> |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="f11d5-127">**dest**</span><span class="sxs-lookup"><span data-stu-id="f11d5-127">**dest**</span></span> | <span data-ttu-id="f11d5-128">-inf</span><span class="sxs-lookup"><span data-stu-id="f11d5-128">-inf</span></span>     | <span data-ttu-id="f11d5-129">-F</span><span class="sxs-lookup"><span data-stu-id="f11d5-129">-F</span></span>     | <span data-ttu-id="f11d5-130">-0</span><span class="sxs-lookup"><span data-stu-id="f11d5-130">-0</span></span>          | <span data-ttu-id="f11d5-131">-0</span><span class="sxs-lookup"><span data-stu-id="f11d5-131">-0</span></span>     | <span data-ttu-id="f11d5-132">+0</span><span class="sxs-lookup"><span data-stu-id="f11d5-132">+0</span></span>     | <span data-ttu-id="f11d5-133">+0</span><span class="sxs-lookup"><span data-stu-id="f11d5-133">+0</span></span>          | <span data-ttu-id="f11d5-134">+ F</span><span class="sxs-lookup"><span data-stu-id="f11d5-134">+F</span></span>     | <span data-ttu-id="f11d5-135">+inf</span><span class="sxs-lookup"><span data-stu-id="f11d5-135">+inf</span></span>     | <span data-ttu-id="f11d5-136">не число</span><span class="sxs-lookup"><span data-stu-id="f11d5-136">NaN</span></span>     |



 

<span data-ttu-id="f11d5-137">F означает ограничение по настоящему вещественному числу.</span><span class="sxs-lookup"><span data-stu-id="f11d5-137">F means finite-real number.</span></span>

<span data-ttu-id="f11d5-138">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="f11d5-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f11d5-139">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="f11d5-139">Vertex Shader</span></span> | <span data-ttu-id="f11d5-140">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="f11d5-140">Geometry Shader</span></span> | <span data-ttu-id="f11d5-141">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="f11d5-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="f11d5-142">x</span><span class="sxs-lookup"><span data-stu-id="f11d5-142">x</span></span>             | <span data-ttu-id="f11d5-143">x</span><span class="sxs-lookup"><span data-stu-id="f11d5-143">x</span></span>               | <span data-ttu-id="f11d5-144">x</span><span class="sxs-lookup"><span data-stu-id="f11d5-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f11d5-145">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="f11d5-145">Minimum Shader Model</span></span>

<span data-ttu-id="f11d5-146">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="f11d5-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f11d5-147">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="f11d5-147">Shader Model</span></span>                                              | <span data-ttu-id="f11d5-148">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="f11d5-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f11d5-149">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="f11d5-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f11d5-150">да</span><span class="sxs-lookup"><span data-stu-id="f11d5-150">yes</span></span>       |
| [<span data-ttu-id="f11d5-151">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="f11d5-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f11d5-152">да</span><span class="sxs-lookup"><span data-stu-id="f11d5-152">yes</span></span>       |
| [<span data-ttu-id="f11d5-153">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="f11d5-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f11d5-154">да</span><span class="sxs-lookup"><span data-stu-id="f11d5-154">yes</span></span>       |
| [<span data-ttu-id="f11d5-155">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f11d5-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f11d5-156">Нет</span><span class="sxs-lookup"><span data-stu-id="f11d5-156">no</span></span>        |
| [<span data-ttu-id="f11d5-157">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f11d5-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f11d5-158">Нет</span><span class="sxs-lookup"><span data-stu-id="f11d5-158">no</span></span>        |
| [<span data-ttu-id="f11d5-159">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f11d5-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f11d5-160">Нет</span><span class="sxs-lookup"><span data-stu-id="f11d5-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f11d5-161">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="f11d5-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f11d5-162">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f11d5-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





