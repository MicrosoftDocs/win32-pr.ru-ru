---
title: round_pi (SM4-ASM)
description: Округление числа с плавающей точкой до целого числа с плавающей запятой. | round_pi (SM4-ASM)
ms.assetid: AA4E4C2E-A4B0-4892-8660-1EF57767F4C4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6016cc03f28852c938b1be62d3aaca39dae5dcfb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998187"
---
# <a name="round_pi-sm4---asm"></a><span data-ttu-id="877e6-104">Round \_ Pi (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="877e6-104">round\_pi (sm4 - asm)</span></span>

<span data-ttu-id="877e6-105">Округление числа с плавающей точкой до целого числа с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="877e6-105">Floating-point round to integral float.</span></span>



| <span data-ttu-id="877e6-106">округлить \_ Pi \[ \_ \] , конечный \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="877e6-106">round\_pi\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------------|



 



| <span data-ttu-id="877e6-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="877e6-107">Item</span></span>                                                            | <span data-ttu-id="877e6-108">Описание</span><span class="sxs-lookup"><span data-stu-id="877e6-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="877e6-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="877e6-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="877e6-110">\[в \] адресе результатов операции.</span><span class="sxs-lookup"><span data-stu-id="877e6-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="877e6-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="877e6-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="877e6-112">\[в \] компонентах операции.</span><span class="sxs-lookup"><span data-stu-id="877e6-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="877e6-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="877e6-113">Remarks</span></span>

<span data-ttu-id="877e6-114">Эта инструкция выполняет покомпонентное округление значений с плавающей запятой в *src0*, записывая целочисленные значения с плавающей запятой в *dest*.</span><span class="sxs-lookup"><span data-stu-id="877e6-114">This instruction performs a component-wise floating-point round of the values in *src0*, writing integral floating-point values to *dest*.</span></span>

<span data-ttu-id="877e6-115">**Округление числа \_ Пи** округляет в сторону + Infinity, обычно известное как ceil ().</span><span class="sxs-lookup"><span data-stu-id="877e6-115">**round\_pi** rounds towards +infinity, commonly known as ceil().</span></span>

<span data-ttu-id="877e6-116">В следующей таблице показаны результаты, полученные при выполнении инструкции с различными классами чисел.</span><span class="sxs-lookup"><span data-stu-id="877e6-116">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>

<span data-ttu-id="877e6-117">F означает ограничение по настоящему вещественному числу.</span><span class="sxs-lookup"><span data-stu-id="877e6-117">F means finite-real number.</span></span>



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="877e6-118">**src**</span><span class="sxs-lookup"><span data-stu-id="877e6-118">**src**</span></span>  | <span data-ttu-id="877e6-119">**-INF**</span><span class="sxs-lookup"><span data-stu-id="877e6-119">**-inf**</span></span> | <span data-ttu-id="877e6-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="877e6-120">**-F**</span></span> | <span data-ttu-id="877e6-121">**— денорма**</span><span class="sxs-lookup"><span data-stu-id="877e6-121">**-denorm**</span></span> | <span data-ttu-id="877e6-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="877e6-122">**-0**</span></span> | <span data-ttu-id="877e6-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="877e6-123">**+0**</span></span> | <span data-ttu-id="877e6-124">**+ денорма**</span><span class="sxs-lookup"><span data-stu-id="877e6-124">**+denorm**</span></span> | <span data-ttu-id="877e6-125">**+ F**</span><span class="sxs-lookup"><span data-stu-id="877e6-125">**+F**</span></span> | <span data-ttu-id="877e6-126">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="877e6-126">**+inf**</span></span> | <span data-ttu-id="877e6-127">**Не число**</span><span class="sxs-lookup"><span data-stu-id="877e6-127">**NaN**</span></span> |
| <span data-ttu-id="877e6-128">**dest**</span><span class="sxs-lookup"><span data-stu-id="877e6-128">**dest**</span></span> | <span data-ttu-id="877e6-129">-inf</span><span class="sxs-lookup"><span data-stu-id="877e6-129">-inf</span></span>     | <span data-ttu-id="877e6-130">-F</span><span class="sxs-lookup"><span data-stu-id="877e6-130">-F</span></span>     | <span data-ttu-id="877e6-131">-0</span><span class="sxs-lookup"><span data-stu-id="877e6-131">-0</span></span>          | <span data-ttu-id="877e6-132">-0</span><span class="sxs-lookup"><span data-stu-id="877e6-132">-0</span></span>     | <span data-ttu-id="877e6-133">+0</span><span class="sxs-lookup"><span data-stu-id="877e6-133">+0</span></span>     | <span data-ttu-id="877e6-134">+0</span><span class="sxs-lookup"><span data-stu-id="877e6-134">+0</span></span>          | <span data-ttu-id="877e6-135">+ F</span><span class="sxs-lookup"><span data-stu-id="877e6-135">+F</span></span>     | <span data-ttu-id="877e6-136">+inf</span><span class="sxs-lookup"><span data-stu-id="877e6-136">+inf</span></span>     | <span data-ttu-id="877e6-137">не число</span><span class="sxs-lookup"><span data-stu-id="877e6-137">NaN</span></span>     |



 

<span data-ttu-id="877e6-138">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="877e6-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="877e6-139">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="877e6-139">Vertex Shader</span></span> | <span data-ttu-id="877e6-140">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="877e6-140">Geometry Shader</span></span> | <span data-ttu-id="877e6-141">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="877e6-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="877e6-142">x</span><span class="sxs-lookup"><span data-stu-id="877e6-142">x</span></span>             | <span data-ttu-id="877e6-143">x</span><span class="sxs-lookup"><span data-stu-id="877e6-143">x</span></span>               | <span data-ttu-id="877e6-144">x</span><span class="sxs-lookup"><span data-stu-id="877e6-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="877e6-145">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="877e6-145">Minimum Shader Model</span></span>

<span data-ttu-id="877e6-146">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="877e6-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="877e6-147">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="877e6-147">Shader Model</span></span>                                              | <span data-ttu-id="877e6-148">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="877e6-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="877e6-149">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="877e6-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="877e6-150">да</span><span class="sxs-lookup"><span data-stu-id="877e6-150">yes</span></span>       |
| [<span data-ttu-id="877e6-151">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="877e6-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="877e6-152">да</span><span class="sxs-lookup"><span data-stu-id="877e6-152">yes</span></span>       |
| [<span data-ttu-id="877e6-153">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="877e6-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="877e6-154">да</span><span class="sxs-lookup"><span data-stu-id="877e6-154">yes</span></span>       |
| [<span data-ttu-id="877e6-155">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="877e6-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="877e6-156">Нет</span><span class="sxs-lookup"><span data-stu-id="877e6-156">no</span></span>        |
| [<span data-ttu-id="877e6-157">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="877e6-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="877e6-158">Нет</span><span class="sxs-lookup"><span data-stu-id="877e6-158">no</span></span>        |
| [<span data-ttu-id="877e6-159">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="877e6-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="877e6-160">Нет</span><span class="sxs-lookup"><span data-stu-id="877e6-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="877e6-161">См. также</span><span class="sxs-lookup"><span data-stu-id="877e6-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="877e6-162">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="877e6-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





