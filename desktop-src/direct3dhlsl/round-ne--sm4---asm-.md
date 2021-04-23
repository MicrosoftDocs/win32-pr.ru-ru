---
title: round_ne (SM4-ASM)
description: Округление числа с плавающей точкой до целого числа с плавающей запятой. | round_ne (SM4-ASM)
ms.assetid: 2D1A0786-F7DB-4D69-9F56-82ECD1EE7ABA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1c6f5e332453318dc0ad1a7806c3506343ff3b6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986485"
---
# <a name="round_ne-sm4---asm"></a><span data-ttu-id="69e29-104">Round \_ NE (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="69e29-104">round\_ne (sm4 - asm)</span></span>

<span data-ttu-id="69e29-105">Округление числа с плавающей точкой до целого числа с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="69e29-105">Floating-point round to integral float.</span></span>



| <span data-ttu-id="69e29-106">Round \_ Ne \[ \_ \] — dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="69e29-106">round\_ne\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|------------------------------------------------------------------|



 



| <span data-ttu-id="69e29-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="69e29-107">Item</span></span>                                                            | <span data-ttu-id="69e29-108">Описание</span><span class="sxs-lookup"><span data-stu-id="69e29-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="69e29-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="69e29-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="69e29-110">\[в \] адресе результатов операции.</span><span class="sxs-lookup"><span data-stu-id="69e29-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="69e29-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="69e29-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="69e29-112">\[в \] компонентах операции.</span><span class="sxs-lookup"><span data-stu-id="69e29-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="69e29-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="69e29-113">Remarks</span></span>

<span data-ttu-id="69e29-114">Эта инструкция выполняет покомпонентное округление значений с плавающей запятой в *src0*, записывая целочисленные значения с плавающей запятой в *dest*.</span><span class="sxs-lookup"><span data-stu-id="69e29-114">This instruction performs a component-wise floating-point round of the values in *src0*, writing integral floating-point values to *dest*.</span></span> <span data-ttu-id="69e29-115">**Round \_ Ne** округляет до ближайшего четного значения.</span><span class="sxs-lookup"><span data-stu-id="69e29-115">**round\_ne** rounds towards nearest even.</span></span>

<span data-ttu-id="69e29-116">В следующей таблице показаны результаты, полученные при выполнении инструкции с различными классами чисел.</span><span class="sxs-lookup"><span data-stu-id="69e29-116">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>

<span data-ttu-id="69e29-117">F означает ограничение по настоящему вещественному числу.</span><span class="sxs-lookup"><span data-stu-id="69e29-117">F means finite-real number.</span></span>



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| <span data-ttu-id="69e29-118">**src**</span><span class="sxs-lookup"><span data-stu-id="69e29-118">**src**</span></span>  | <span data-ttu-id="69e29-119">**-INF**</span><span class="sxs-lookup"><span data-stu-id="69e29-119">**-inf**</span></span> | <span data-ttu-id="69e29-120">**-F**</span><span class="sxs-lookup"><span data-stu-id="69e29-120">**-F**</span></span> | <span data-ttu-id="69e29-121">**— денорма**</span><span class="sxs-lookup"><span data-stu-id="69e29-121">**-denorm**</span></span> | <span data-ttu-id="69e29-122">**-0**</span><span class="sxs-lookup"><span data-stu-id="69e29-122">**-0**</span></span> | <span data-ttu-id="69e29-123">**+0**</span><span class="sxs-lookup"><span data-stu-id="69e29-123">**+0**</span></span> | <span data-ttu-id="69e29-124">**+ денорма**</span><span class="sxs-lookup"><span data-stu-id="69e29-124">**+denorm**</span></span> | <span data-ttu-id="69e29-125">**+ F**</span><span class="sxs-lookup"><span data-stu-id="69e29-125">**+F**</span></span> | <span data-ttu-id="69e29-126">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="69e29-126">**+inf**</span></span> | <span data-ttu-id="69e29-127">**Не число**</span><span class="sxs-lookup"><span data-stu-id="69e29-127">**NaN**</span></span> |
| <span data-ttu-id="69e29-128">**dest**</span><span class="sxs-lookup"><span data-stu-id="69e29-128">**dest**</span></span> | <span data-ttu-id="69e29-129">-inf</span><span class="sxs-lookup"><span data-stu-id="69e29-129">-inf</span></span>     | <span data-ttu-id="69e29-130">-F</span><span class="sxs-lookup"><span data-stu-id="69e29-130">-F</span></span>     | <span data-ttu-id="69e29-131">-0</span><span class="sxs-lookup"><span data-stu-id="69e29-131">-0</span></span>          | <span data-ttu-id="69e29-132">-0</span><span class="sxs-lookup"><span data-stu-id="69e29-132">-0</span></span>     | <span data-ttu-id="69e29-133">+0</span><span class="sxs-lookup"><span data-stu-id="69e29-133">+0</span></span>     | <span data-ttu-id="69e29-134">+0</span><span class="sxs-lookup"><span data-stu-id="69e29-134">+0</span></span>          | <span data-ttu-id="69e29-135">+ F</span><span class="sxs-lookup"><span data-stu-id="69e29-135">+F</span></span>     | <span data-ttu-id="69e29-136">+inf</span><span class="sxs-lookup"><span data-stu-id="69e29-136">+inf</span></span>     | <span data-ttu-id="69e29-137">не число</span><span class="sxs-lookup"><span data-stu-id="69e29-137">NaN</span></span>     |



 

<span data-ttu-id="69e29-138">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="69e29-138">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="69e29-139">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="69e29-139">Vertex Shader</span></span> | <span data-ttu-id="69e29-140">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="69e29-140">Geometry Shader</span></span> | <span data-ttu-id="69e29-141">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="69e29-141">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="69e29-142">x</span><span class="sxs-lookup"><span data-stu-id="69e29-142">x</span></span>             | <span data-ttu-id="69e29-143">x</span><span class="sxs-lookup"><span data-stu-id="69e29-143">x</span></span>               | <span data-ttu-id="69e29-144">x</span><span class="sxs-lookup"><span data-stu-id="69e29-144">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="69e29-145">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="69e29-145">Minimum Shader Model</span></span>

<span data-ttu-id="69e29-146">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="69e29-146">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="69e29-147">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="69e29-147">Shader Model</span></span>                                              | <span data-ttu-id="69e29-148">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="69e29-148">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="69e29-149">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="69e29-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="69e29-150">да</span><span class="sxs-lookup"><span data-stu-id="69e29-150">yes</span></span>       |
| [<span data-ttu-id="69e29-151">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="69e29-151">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="69e29-152">да</span><span class="sxs-lookup"><span data-stu-id="69e29-152">yes</span></span>       |
| [<span data-ttu-id="69e29-153">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="69e29-153">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="69e29-154">да</span><span class="sxs-lookup"><span data-stu-id="69e29-154">yes</span></span>       |
| [<span data-ttu-id="69e29-155">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="69e29-155">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="69e29-156">Нет</span><span class="sxs-lookup"><span data-stu-id="69e29-156">no</span></span>        |
| [<span data-ttu-id="69e29-157">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="69e29-157">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="69e29-158">Нет</span><span class="sxs-lookup"><span data-stu-id="69e29-158">no</span></span>        |
| [<span data-ttu-id="69e29-159">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="69e29-159">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="69e29-160">Нет</span><span class="sxs-lookup"><span data-stu-id="69e29-160">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="69e29-161">См. также</span><span class="sxs-lookup"><span data-stu-id="69e29-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69e29-162">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="69e29-162">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





