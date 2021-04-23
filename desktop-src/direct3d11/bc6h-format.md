---
title: Формат BC6H
description: Формат BC6H — это формат сжатия текстуры, предназначенный для обеспечения поддержки цветовых пространств HDR в исходных данных.
ms.assetid: D6A1A729-5023-4A94-A8DB-5954D453E136
keywords:
- BC6H
- DXGI_FORMAT_BC6H
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ed4b934df742a4d2c99e20b52b7172b64e598dc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070361"
---
# <a name="bc6h-format"></a><span data-ttu-id="577ed-105">Формат BC6H</span><span class="sxs-lookup"><span data-stu-id="577ed-105">BC6H Format</span></span>

<span data-ttu-id="577ed-106">Формат BC6H — это формат сжатия текстуры, предназначенный для обеспечения поддержки цветовых пространств HDR в исходных данных.</span><span class="sxs-lookup"><span data-stu-id="577ed-106">The BC6H format is a texture compression format designed to support high-dynamic range (HDR) color spaces in source data.</span></span>

-   [<span data-ttu-id="577ed-107">Сведения о формате BC6H/DXGI \_ \_ BC6H</span><span class="sxs-lookup"><span data-stu-id="577ed-107">About BC6H/DXGI\_FORMAT\_BC6H</span></span>](/windows)
-   [<span data-ttu-id="577ed-108">Реализация BC6H</span><span class="sxs-lookup"><span data-stu-id="577ed-108">BC6H Implementation</span></span>](#bc6h-implementation)
-   [<span data-ttu-id="577ed-109">Декодирование формата BC6H</span><span class="sxs-lookup"><span data-stu-id="577ed-109">Decoding the BC6H Format</span></span>](#decoding-the-bc6h-format)
-   [<span data-ttu-id="577ed-110">Формат сжатых конечных точек BC6H</span><span class="sxs-lookup"><span data-stu-id="577ed-110">BC6H Compressed Endpoint Format</span></span>](#bc6h-compressed-endpoint-format)
-   [<span data-ttu-id="577ed-111">Расширение знака для значений конечных точек</span><span class="sxs-lookup"><span data-stu-id="577ed-111">Sign Extension for Endpoint Values</span></span>](#sign-extension-for-endpoint-values)
-   [<span data-ttu-id="577ed-112">Преобразование инверсии для значений конечной точки</span><span class="sxs-lookup"><span data-stu-id="577ed-112">Transform Inversion for Endpoint Values</span></span>](#transform-inversion-for-endpoint-values)
-   [<span data-ttu-id="577ed-113">Ункуантизатион конечных точек цвета</span><span class="sxs-lookup"><span data-stu-id="577ed-113">Unquantization of Color Endpoints</span></span>](#unquantization-of-color-endpoints)
-   [<span data-ttu-id="577ed-114">См. также</span><span class="sxs-lookup"><span data-stu-id="577ed-114">Related topics</span></span>](#related-topics)

## <a name="about-bc6hdxgi_format_bc6h"></a><span data-ttu-id="577ed-115">Сведения о формате BC6H/DXGI \_ \_ BC6H</span><span class="sxs-lookup"><span data-stu-id="577ed-115">About BC6H/DXGI\_FORMAT\_BC6H</span></span>

<span data-ttu-id="577ed-116">Формат BC6H обеспечивает высококачественное сжатие изображений, использующих три канала цветов HDR с 16-разрядным значением для каждого канала цвета в составе значения (16:16:16).</span><span class="sxs-lookup"><span data-stu-id="577ed-116">The BC6H format provides high-quality compression for images that use three HDR color channels, with a 16-bit value for each color channel of the value (16:16:16).</span></span> <span data-ttu-id="577ed-117">Альфа-канал не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="577ed-117">There is no support for an alpha channel.</span></span>

<span data-ttu-id="577ed-118">BC6H задается следующими \_ значениями перечисления в формате DXGI:</span><span class="sxs-lookup"><span data-stu-id="577ed-118">BC6H is specified by the following DXGI\_FORMAT enumeration values:</span></span>

-   <span data-ttu-id="577ed-119">**DXGI \_ FORMAT \_ BC6H \_ Type**.</span><span class="sxs-lookup"><span data-stu-id="577ed-119">**DXGI\_FORMAT\_BC6H\_TYPELESS**.</span></span>
-   <span data-ttu-id="577ed-120">**DXGI \_ FORMAT \_ BC6H \_ UF16**.</span><span class="sxs-lookup"><span data-stu-id="577ed-120">**DXGI\_FORMAT\_BC6H\_UF16**.</span></span> <span data-ttu-id="577ed-121">В этом формате BC6H не используется знаковый бит в 16-разрядных значениях канала цвета с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="577ed-121">This BC6H format does not use a sign bit in the 16-bit floating point color channel values.</span></span>
-   <span data-ttu-id="577ed-122">**DXGI \_ FORMAT \_ BC6H \_ SF16**. В этом формате BC6H используется бит знака в 16-битных значениях канала цвета с плавающей точкой.</span><span class="sxs-lookup"><span data-stu-id="577ed-122">**DXGI\_FORMAT\_BC6H\_SF16**.This BC6H format uses a sign bit in the 16-bit floating point color channel values.</span></span>

> [!Note]  
> <span data-ttu-id="577ed-123">16-разрядный формат с плавающей точкой для цветовых каналов часто называют "половинным" форматом с плавающей точкой.</span><span class="sxs-lookup"><span data-stu-id="577ed-123">The 16 bit floating point format for color channels is often referred to as a "half" floating point format.</span></span> <span data-ttu-id="577ed-124">Формат имеет следующее расположение битов:</span><span class="sxs-lookup"><span data-stu-id="577ed-124">This format has the following bit layout:</span></span>
>
> |                       |                                                 |
> |-----------------------|-------------------------------------------------|
> | <span data-ttu-id="577ed-125">UF16 (без знака с плавающей запятой)</span><span class="sxs-lookup"><span data-stu-id="577ed-125">UF16 (unsigned float)</span></span> | <span data-ttu-id="577ed-126">5 разрядов экспоненты + 11 разрядов мантиссы</span><span class="sxs-lookup"><span data-stu-id="577ed-126">5 exponent bits + 11 mantissa bits</span></span>              |
> | <span data-ttu-id="577ed-127">SF16 (со знаком с плавающей запятой)</span><span class="sxs-lookup"><span data-stu-id="577ed-127">SF16 (signed float)</span></span>   | <span data-ttu-id="577ed-128">1 разряд знака + 5 разрядов экспоненты + 10 разрядов мантиссы</span><span class="sxs-lookup"><span data-stu-id="577ed-128">1 sign bit + 5 exponent bits + 10 mantissa bits</span></span> |
>
> 
>
>  

 

<span data-ttu-id="577ed-129">Формат BC6H можно использовать для ресурсов текстуры [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (включая массивы), Texture3D или TextureCube (включая массивы).</span><span class="sxs-lookup"><span data-stu-id="577ed-129">The BC6H format can be used for [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (including arrays), Texture3D, or TextureCube (including arrays) texture resources.</span></span> <span data-ttu-id="577ed-130">Аналогичным образом этот формат применяется к любым поверхностям MIP-карты, связанным с этими ресурсами.</span><span class="sxs-lookup"><span data-stu-id="577ed-130">Similarly, this format applies to any MIP-map surfaces associated with these resources.</span></span>

<span data-ttu-id="577ed-131">В BC6H используется фиксируемый размер блоков — 16 байтов (128 битов) и фиксированный размер плитки — 4x4 текселя.</span><span class="sxs-lookup"><span data-stu-id="577ed-131">BC6H uses a fixed block size of 16 bytes (128 bits) and a fixed tile size of 4x4 texels.</span></span> <span data-ttu-id="577ed-132">Как и в случае с предыдущими форматами BC, изображения текстур крупнее, чем поддерживаемый размер плитки (4x4), сжимаются с использованием нескольких блоков.</span><span class="sxs-lookup"><span data-stu-id="577ed-132">As with previous BC formats, texture images larger than the supported tile size (4x4) are compressed by using multiple blocks.</span></span> <span data-ttu-id="577ed-133">Это удостоверение адресации также применяется к трехмерным изображениям, MIP-картам, кубемапс и массивам текстур.</span><span class="sxs-lookup"><span data-stu-id="577ed-133">This addressing identity applies also to three-dimensional images, MIP-maps, cubemaps, and texture arrays.</span></span> <span data-ttu-id="577ed-134">Все плитки изображений должны иметь один формат.</span><span class="sxs-lookup"><span data-stu-id="577ed-134">All image tiles must be of the same format.</span></span>

<span data-ttu-id="577ed-135">Некоторые важные замечания о формате BC6H:</span><span class="sxs-lookup"><span data-stu-id="577ed-135">Some important notes about the BC6H format:</span></span>

-   <span data-ttu-id="577ed-136">BC6H поддерживает денормализацию чисел с плавающей запятой, но не поддерживает сущности типа INF (бесконечность) и NaN (не число).</span><span class="sxs-lookup"><span data-stu-id="577ed-136">BC6H supports floating point denormalization, but does not support INF (infinity) and NaN (not a number).</span></span> <span data-ttu-id="577ed-137">Исключение — это режим со знаком для BC6H ( \_ Формат DXGI \_ BC6H \_ SF16), поддерживающий-INF (отрицательная бесконечность).</span><span class="sxs-lookup"><span data-stu-id="577ed-137">The exception is the signed mode of BC6H (DXGI\_FORMAT\_BC6H\_SF16), which supports -INF (negative infinity).</span></span> <span data-ttu-id="577ed-138">Обратите внимание, что эта поддержка для-INF является просто артефактом самого формата и не поддерживается кодировщиками для этого формата.</span><span class="sxs-lookup"><span data-stu-id="577ed-138">Note that this support for -INF is merely an artifact of the format itself, and is not specifically supported by encoders for this format.</span></span> <span data-ttu-id="577ed-139">В общем случае, когда кодировщики сталкиваются с INF (положительными или отрицательными) или неоднородными входными данными, они должны \\ преобразовывать эти данные в максимально допустимое значение представления, отличного от INF, и сопоставлять NaN с 0 до сжатия.</span><span class="sxs-lookup"><span data-stu-id="577ed-139">In general, when encoders encounter INF (positive or negative) or NaN input data, they should \\ convert that data to the maximum allowable non-INF representation value, and map NaN to 0 prior to compression.</span></span>
-   <span data-ttu-id="577ed-140">Формат BC6H не поддерживает альфа-канал.</span><span class="sxs-lookup"><span data-stu-id="577ed-140">BC6H does not support an alpha channel.</span></span>
-   <span data-ttu-id="577ed-141">Декодер BC6H выполняет распаковку до того, как приступит к фильтрации текстур.</span><span class="sxs-lookup"><span data-stu-id="577ed-141">The BC6H decoder performs decompression before it performs texture filtering.</span></span>
-   <span data-ttu-id="577ed-142">Распаковка BC6H должна быть точной. то есть оборудование должно вернуть результаты, идентичные декодеру, описанному в этой документации.</span><span class="sxs-lookup"><span data-stu-id="577ed-142">BC6H decompression must be bit accurate; that is, the hardware must return results that are identical to the decoder described in this documentation.</span></span>

## <a name="bc6h-implementation"></a><span data-ttu-id="577ed-143">Реализация BC6H</span><span class="sxs-lookup"><span data-stu-id="577ed-143">BC6H Implementation</span></span>

<span data-ttu-id="577ed-144">Блок BC6H состоит из битов режима, сжатых конечных точек, сжатых индексов и дополнительного индекса раздела.</span><span class="sxs-lookup"><span data-stu-id="577ed-144">A BC6H block consists of mode bits, compressed endpoints, compressed indices, and an optional partition index.</span></span> <span data-ttu-id="577ed-145">Этот формат задает 14 разных режимов.</span><span class="sxs-lookup"><span data-stu-id="577ed-145">This format specifies 14 different modes.</span></span>

<span data-ttu-id="577ed-146">Цвет конечной точки хранится в виде RGB-триады.</span><span class="sxs-lookup"><span data-stu-id="577ed-146">An endpoint color is stored as an RGB triplet.</span></span> <span data-ttu-id="577ed-147">BC6H определяет цветовую палитру по приблизительной линии, проходящей через несколько определенных конечных точек цвета.</span><span class="sxs-lookup"><span data-stu-id="577ed-147">BC6H defines a palette of colors on an approximate line across a number of defined color endpoints.</span></span> <span data-ttu-id="577ed-148">Кроме того, в зависимости от режима плитка может быть разделена на два региона или обрабатываться как один регион, где плитка с двумя регионами имеет отдельный набор конечных точек цвета для каждого региона.</span><span class="sxs-lookup"><span data-stu-id="577ed-148">Also, depending on the mode, a tile can be divided into two regions or treated as a single region, where a two-region tile has a separate set of color endpoints for each region.</span></span> <span data-ttu-id="577ed-149">BC6H сохраняет один индекс палитры на тексель.</span><span class="sxs-lookup"><span data-stu-id="577ed-149">BC6H stores one palette index per texel.</span></span>

<span data-ttu-id="577ed-150">Если вы работаете с двумя регионами, число возможных разделов равно 32.</span><span class="sxs-lookup"><span data-stu-id="577ed-150">In the two-region case, there are 32 possible partitions.</span></span>

## <a name="decoding-the-bc6h-format"></a><span data-ttu-id="577ed-151">Декодирование формата BC6H</span><span class="sxs-lookup"><span data-stu-id="577ed-151">Decoding the BC6H Format</span></span>

<span data-ttu-id="577ed-152">В псевдокоде ниже изображены действия по распаковке пикселя в точке (x,y) при наличии 16-байтового блока BC6H.</span><span class="sxs-lookup"><span data-stu-id="577ed-152">The pseudocode below shows the steps to decompress the pixel at (x,y) given the 16 byte BC6H block.</span></span>

``` syntax
decompress_bc6h(x, y, block)
{
    mode = extract_mode(block);
    endpoints;
    index;
    
    if(mode.type == ONE)
    {
        endpoints = extract_compressed_endpoints(mode, block);
        index = extract_index_ONE(x, y, block);
    }
    else //mode.type == TWO
    {
        partition = extract_partition(block);
        region = get_region(partition, x, y);
        endpoints = extract_compressed_endpoints(mode, region, block);
        index = extract_index_TWO(x, y, partition, block);
    }
    
    unquantize(endpoints);
    color = interpolate(index, endpoints);
    finish_unquantize(color);
}
```

<span data-ttu-id="577ed-153">В таблице ниже указано число битов и значения для каждого из 14 возможных форматов для блоков BC6H.</span><span class="sxs-lookup"><span data-stu-id="577ed-153">The following table contains the bit count and values for each of the 14 possible formats for BC6H blocks.</span></span> 

| <span data-ttu-id="577ed-154">Режим</span><span class="sxs-lookup"><span data-stu-id="577ed-154">Mode</span></span> | <span data-ttu-id="577ed-155">Индексы разделов</span><span class="sxs-lookup"><span data-stu-id="577ed-155">Partition Indices</span></span> | <span data-ttu-id="577ed-156">Секция</span><span class="sxs-lookup"><span data-stu-id="577ed-156">Partition</span></span> | <span data-ttu-id="577ed-157">Конечные точки цвета</span><span class="sxs-lookup"><span data-stu-id="577ed-157">Color Endpoints</span></span>                  | <span data-ttu-id="577ed-158">Биты режима</span><span class="sxs-lookup"><span data-stu-id="577ed-158">Mode Bits</span></span>      |
|------|-------------------|-----------|----------------------------------|----------------|
| <span data-ttu-id="577ed-159">1</span><span class="sxs-lookup"><span data-stu-id="577ed-159">1</span></span>    | <span data-ttu-id="577ed-160">46 битов</span><span class="sxs-lookup"><span data-stu-id="577ed-160">46 bits</span></span>           | <span data-ttu-id="577ed-161">5 битов</span><span class="sxs-lookup"><span data-stu-id="577ed-161">5 bits</span></span>    | <span data-ttu-id="577ed-162">75 битов (10,555, 10,555, 10,555)</span><span class="sxs-lookup"><span data-stu-id="577ed-162">75 bits (10.555, 10.555, 10.555)</span></span> | <span data-ttu-id="577ed-163">2 бита (00)</span><span class="sxs-lookup"><span data-stu-id="577ed-163">2 bits (00)</span></span>    |
| <span data-ttu-id="577ed-164">2</span><span class="sxs-lookup"><span data-stu-id="577ed-164">2</span></span>    | <span data-ttu-id="577ed-165">46 битов</span><span class="sxs-lookup"><span data-stu-id="577ed-165">46 bits</span></span>           | <span data-ttu-id="577ed-166">5 битов</span><span class="sxs-lookup"><span data-stu-id="577ed-166">5 bits</span></span>    | <span data-ttu-id="577ed-167">75 битов (7666, 7666, 7666)</span><span class="sxs-lookup"><span data-stu-id="577ed-167">75 bits (7666, 7666, 7666)</span></span>       | <span data-ttu-id="577ed-168">2 бита (01)</span><span class="sxs-lookup"><span data-stu-id="577ed-168">2 bits (01)</span></span>    |
| <span data-ttu-id="577ed-169">3</span><span class="sxs-lookup"><span data-stu-id="577ed-169">3</span></span>    | <span data-ttu-id="577ed-170">46 битов</span><span class="sxs-lookup"><span data-stu-id="577ed-170">46 bits</span></span>           | <span data-ttu-id="577ed-171">5 битов</span><span class="sxs-lookup"><span data-stu-id="577ed-171">5 bits</span></span>    | <span data-ttu-id="577ed-172">72 бита (11,555, 11,444, 11,444)</span><span class="sxs-lookup"><span data-stu-id="577ed-172">72 bits (11.555, 11.444, 11.444)</span></span> | <span data-ttu-id="577ed-173">5 битов (00010)</span><span class="sxs-lookup"><span data-stu-id="577ed-173">5 bits (00010)</span></span> |
| <span data-ttu-id="577ed-174">4</span><span class="sxs-lookup"><span data-stu-id="577ed-174">4</span></span>    | <span data-ttu-id="577ed-175">46 битов</span><span class="sxs-lookup"><span data-stu-id="577ed-175">46 bits</span></span>           | <span data-ttu-id="577ed-176">5 битов</span><span class="sxs-lookup"><span data-stu-id="577ed-176">5 bits</span></span>    | <span data-ttu-id="577ed-177">72 бита (11,444, 11,555, 11,444)</span><span class="sxs-lookup"><span data-stu-id="577ed-177">72 bits (11.444, 11.555, 11.444)</span></span> | <span data-ttu-id="577ed-178">5 битов (00110)</span><span class="sxs-lookup"><span data-stu-id="577ed-178">5 bits (00110)</span></span> |
| <span data-ttu-id="577ed-179">5</span><span class="sxs-lookup"><span data-stu-id="577ed-179">5</span></span>    | <span data-ttu-id="577ed-180">46 битов</span><span class="sxs-lookup"><span data-stu-id="577ed-180">46 bits</span></span>           | <span data-ttu-id="577ed-181">5 битов</span><span class="sxs-lookup"><span data-stu-id="577ed-181">5 bits</span></span>    | <span data-ttu-id="577ed-182">72 бита (11,444, 11,444, 11,555)</span><span class="sxs-lookup"><span data-stu-id="577ed-182">72 bits (11.444, 11.444, 11.555)</span></span> | <span data-ttu-id="577ed-183">5 битов (01010)</span><span class="sxs-lookup"><span data-stu-id="577ed-183">5 bits (01010)</span></span> |
| <span data-ttu-id="577ed-184">6</span><span class="sxs-lookup"><span data-stu-id="577ed-184">6</span></span>    | <span data-ttu-id="577ed-185">46 битов</span><span class="sxs-lookup"><span data-stu-id="577ed-185">46 bits</span></span>           | <span data-ttu-id="577ed-186">5 битов</span><span class="sxs-lookup"><span data-stu-id="577ed-186">5 bits</span></span>    | <span data-ttu-id="577ed-187">72 бита (9555, 9555, 9555)</span><span class="sxs-lookup"><span data-stu-id="577ed-187">72 bits (9555, 9555, 9555)</span></span>       | <span data-ttu-id="577ed-188">5 битов (01110)</span><span class="sxs-lookup"><span data-stu-id="577ed-188">5 bits (01110)</span></span> |
| <span data-ttu-id="577ed-189">7</span><span class="sxs-lookup"><span data-stu-id="577ed-189">7</span></span>    | <span data-ttu-id="577ed-190">46 битов</span><span class="sxs-lookup"><span data-stu-id="577ed-190">46 bits</span></span>           | <span data-ttu-id="577ed-191">5 битов</span><span class="sxs-lookup"><span data-stu-id="577ed-191">5 bits</span></span>    | <span data-ttu-id="577ed-192">72 бита (8666, 8555, 8555)</span><span class="sxs-lookup"><span data-stu-id="577ed-192">72 bits (8666, 8555, 8555)</span></span>       | <span data-ttu-id="577ed-193">5 битов (10010)</span><span class="sxs-lookup"><span data-stu-id="577ed-193">5 bits (10010)</span></span> |
| <span data-ttu-id="577ed-194">8</span><span class="sxs-lookup"><span data-stu-id="577ed-194">8</span></span>    | <span data-ttu-id="577ed-195">46 битов</span><span class="sxs-lookup"><span data-stu-id="577ed-195">46 bits</span></span>           | <span data-ttu-id="577ed-196">5 битов</span><span class="sxs-lookup"><span data-stu-id="577ed-196">5 bits</span></span>    | <span data-ttu-id="577ed-197">72 бита (8555, 8666, 8555)</span><span class="sxs-lookup"><span data-stu-id="577ed-197">72 bits (8555, 8666, 8555)</span></span>       | <span data-ttu-id="577ed-198">5 битов (10110)</span><span class="sxs-lookup"><span data-stu-id="577ed-198">5 bits (10110)</span></span> |
| <span data-ttu-id="577ed-199">9</span><span class="sxs-lookup"><span data-stu-id="577ed-199">9</span></span>    | <span data-ttu-id="577ed-200">46 битов</span><span class="sxs-lookup"><span data-stu-id="577ed-200">46 bits</span></span>           | <span data-ttu-id="577ed-201">5 битов</span><span class="sxs-lookup"><span data-stu-id="577ed-201">5 bits</span></span>    | <span data-ttu-id="577ed-202">72 бита (8555, 8555, 8666)</span><span class="sxs-lookup"><span data-stu-id="577ed-202">72 bits (8555, 8555, 8666)</span></span>       | <span data-ttu-id="577ed-203">5 битов (11010)</span><span class="sxs-lookup"><span data-stu-id="577ed-203">5 bits (11010)</span></span> |
| <span data-ttu-id="577ed-204">10</span><span class="sxs-lookup"><span data-stu-id="577ed-204">10</span></span>   | <span data-ttu-id="577ed-205">46 битов</span><span class="sxs-lookup"><span data-stu-id="577ed-205">46 bits</span></span>           | <span data-ttu-id="577ed-206">5 битов</span><span class="sxs-lookup"><span data-stu-id="577ed-206">5 bits</span></span>    | <span data-ttu-id="577ed-207">72 бита (6666, 6666, 6666)</span><span class="sxs-lookup"><span data-stu-id="577ed-207">72 bits (6666, 6666, 6666)</span></span>       | <span data-ttu-id="577ed-208">5 битов (11110)</span><span class="sxs-lookup"><span data-stu-id="577ed-208">5 bits (11110)</span></span> |
| <span data-ttu-id="577ed-209">11</span><span class="sxs-lookup"><span data-stu-id="577ed-209">11</span></span>   | <span data-ttu-id="577ed-210">63 бита</span><span class="sxs-lookup"><span data-stu-id="577ed-210">63 bits</span></span>           | <span data-ttu-id="577ed-211">0 битов</span><span class="sxs-lookup"><span data-stu-id="577ed-211">0 bits</span></span>    | <span data-ttu-id="577ed-212">60 битов (10,10, 10,10, 10,10)</span><span class="sxs-lookup"><span data-stu-id="577ed-212">60 bits (10.10, 10.10, 10.10)</span></span>    | <span data-ttu-id="577ed-213">5 битов (00011)</span><span class="sxs-lookup"><span data-stu-id="577ed-213">5 bits (00011)</span></span> |
| <span data-ttu-id="577ed-214">12</span><span class="sxs-lookup"><span data-stu-id="577ed-214">12</span></span>   | <span data-ttu-id="577ed-215">63 бита</span><span class="sxs-lookup"><span data-stu-id="577ed-215">63 bits</span></span>           | <span data-ttu-id="577ed-216">0 битов</span><span class="sxs-lookup"><span data-stu-id="577ed-216">0 bits</span></span>    | <span data-ttu-id="577ed-217">60 битов (11,9, 11,9, 11,9)</span><span class="sxs-lookup"><span data-stu-id="577ed-217">60 bits (11.9, 11.9, 11.9)</span></span>       | <span data-ttu-id="577ed-218">5 битов (00111)</span><span class="sxs-lookup"><span data-stu-id="577ed-218">5 bits (00111)</span></span> |
| <span data-ttu-id="577ed-219">13</span><span class="sxs-lookup"><span data-stu-id="577ed-219">13</span></span>   | <span data-ttu-id="577ed-220">63 бита</span><span class="sxs-lookup"><span data-stu-id="577ed-220">63 bits</span></span>           | <span data-ttu-id="577ed-221">0 битов</span><span class="sxs-lookup"><span data-stu-id="577ed-221">0 bits</span></span>    | <span data-ttu-id="577ed-222">60 битов (12,8, 12,8, 12,8)</span><span class="sxs-lookup"><span data-stu-id="577ed-222">60 bits (12.8, 12.8, 12.8)</span></span>       | <span data-ttu-id="577ed-223">5 битов (01011)</span><span class="sxs-lookup"><span data-stu-id="577ed-223">5 bits (01011)</span></span> |
| <span data-ttu-id="577ed-224">14</span><span class="sxs-lookup"><span data-stu-id="577ed-224">14</span></span>   | <span data-ttu-id="577ed-225">63 бита</span><span class="sxs-lookup"><span data-stu-id="577ed-225">63 bits</span></span>           | <span data-ttu-id="577ed-226">0 битов</span><span class="sxs-lookup"><span data-stu-id="577ed-226">0 bits</span></span>    | <span data-ttu-id="577ed-227">60 битов (16,4, 16,4, 16,4)</span><span class="sxs-lookup"><span data-stu-id="577ed-227">60 bits (16.4, 16.4, 16.4)</span></span>       | <span data-ttu-id="577ed-228">5 битов (01111)</span><span class="sxs-lookup"><span data-stu-id="577ed-228">5 bits (01111)</span></span> |



 

<span data-ttu-id="577ed-229">Каждый формат в этой таблице можно уникально идентифицировать битами режима.</span><span class="sxs-lookup"><span data-stu-id="577ed-229">Each format in this table can be uniquely identified by the mode bits.</span></span> <span data-ttu-id="577ed-230">Первые десять режимов используются для плиток с двумя регионами, а поле бита режима может иметь длину два бита или пять битов.</span><span class="sxs-lookup"><span data-stu-id="577ed-230">The first ten modes are used for two-region tiles, and the mode bit field can be either two or five bits long.</span></span> <span data-ttu-id="577ed-231">Эти блоки также имеют поля для конечных точек сжатого цвета (72 или 75 битов), раздела (5 битов) и индексов раздела (46 битов).</span><span class="sxs-lookup"><span data-stu-id="577ed-231">These blocks also have fields for the compressed color endpoints (72 or 75 bits), the partition (5 bits), and the partition indices (46 bits).</span></span>

<span data-ttu-id="577ed-232">Для конечных точек сжатого цвета значения в предыдущей таблице обозначают точность сохраненных конечных точек RGB и число битов, используемых для каждого значения цвета.</span><span class="sxs-lookup"><span data-stu-id="577ed-232">For the compressed color endpoints, the values in the preceding table note the precision of the stored RGB endpoints, and the number of bits used for each color value.</span></span> <span data-ttu-id="577ed-233">Например, режим 3 указывает на 11 уровень точности конечной точки цвета, а число битов, используемых для хранения дельта-значений преобразованных конечных точек для красного, синего и зеленого цветов (5, 4 и 4 соответственно).</span><span class="sxs-lookup"><span data-stu-id="577ed-233">For example, mode 3 specifies a color endpoint precision level of 11, and the number of bits used to store the delta values of the transformed endpoints for the red, blue and green colors (5, 4, and 4 respectively).</span></span> <span data-ttu-id="577ed-234">В режиме 10 не используется дельта-сжатие. Вместо этого все четыре конечные точки цвета сохраняются явно.</span><span class="sxs-lookup"><span data-stu-id="577ed-234">Mode 10 does not use delta compression, and instead stores all four color endpoints explicitly.</span></span>

<span data-ttu-id="577ed-235">Последние четыре режима блока используются для плиток с одним регионом, где поле режима равно 5 битам.</span><span class="sxs-lookup"><span data-stu-id="577ed-235">The last four block modes are used for one-region tiles, where the mode field is 5 bits.</span></span> <span data-ttu-id="577ed-236">Эти блоки имеют поля для конечных точек (60 битов) и сжатых индексов (63 бита),</span><span class="sxs-lookup"><span data-stu-id="577ed-236">These blocks have fields for the endpoints (60 bits) and the compressed indices (63 bits).</span></span> <span data-ttu-id="577ed-237">В режиме 11 (как и в режиме 10) не используется дельта-сжатие. Вместо этого конечные точки цвета сохраняются явно.</span><span class="sxs-lookup"><span data-stu-id="577ed-237">Mode 11 (like Mode 10) does not use delta compression, and instead stores both color endpoints explicitly.</span></span>

<span data-ttu-id="577ed-238">Режимы 10011, 10111, 11011 и 11111 (не показан) зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="577ed-238">Modes 10011, 10111, 11011, and 11111 (not shown) are reserved.</span></span> <span data-ttu-id="577ed-239">Не используйте их в своем кодировщике.</span><span class="sxs-lookup"><span data-stu-id="577ed-239">Do not use these in your encoder.</span></span> <span data-ttu-id="577ed-240">Если оборудование представляет собой переданные блоки и задан один из этих режимов, полученный распакованный блок должен содержать все нули во всех каналах, кроме альфа-канала.</span><span class="sxs-lookup"><span data-stu-id="577ed-240">If the hardware is passed blocks with one of these modes specified, the resulting decompressed block must contain all zeroes in all channels except for the alpha channel.</span></span>

<span data-ttu-id="577ed-241">Для BC6H альфа-канал должен всегда возвращать 1,0 независимо от режима.</span><span class="sxs-lookup"><span data-stu-id="577ed-241">For BC6H, the alpha channel must always return 1.0 regardless of the mode.</span></span>

### <a name="bc6h-partition-set"></a><span data-ttu-id="577ed-242">Набор разделов BC6H</span><span class="sxs-lookup"><span data-stu-id="577ed-242">BC6H Partition Set</span></span>

<span data-ttu-id="577ed-243">Существует 32 возможных набора разделов для плитки с двумя регионами, которые определены в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="577ed-243">There are 32 possible partition sets for a two-region tile, and which are defined in the table below.</span></span> <span data-ttu-id="577ed-244">Каждый блок 4x4 представляет одну фигуру.</span><span class="sxs-lookup"><span data-stu-id="577ed-244">Each 4x4 block represents a single shape.</span></span>

![таблица наборов разделов bc6h](images/bc6h-partition-sets.png)

<span data-ttu-id="577ed-246">В этой таблице наборов разделов выделенная полужирным шрифтом и подчеркиванием запись является расположением индекса исправления для подмножества 1 (которое задается с количеством битов на 1 меньше).</span><span class="sxs-lookup"><span data-stu-id="577ed-246">In this table of partition sets, the bolded and underlined entry is the location of the fix-up index for subset 1 (which is specified with one less bit).</span></span> <span data-ttu-id="577ed-247">Индекс исправления для подмножества 0 — это всегда нулевой индекс, поскольку разделение на разделы всегда организовано так, чтобы нулевой индекс находился в нулевом подмножестве.</span><span class="sxs-lookup"><span data-stu-id="577ed-247">The fix-up index for subset 0 is always index 0, as the partitioning is always arranged such that index 0 is always in subset 0.</span></span> <span data-ttu-id="577ed-248">Порядок разделения на разделы: из верхнего левого угла до нижнего правого, перемещаясь слева направо и сверху вниз.</span><span class="sxs-lookup"><span data-stu-id="577ed-248">Partition order goes from top-left to bottom-right, moving left to right and then top to bottom.</span></span>

## <a name="bc6h-compressed-endpoint-format"></a><span data-ttu-id="577ed-249">Формат сжатых конечных точек BC6H</span><span class="sxs-lookup"><span data-stu-id="577ed-249">BC6H Compressed Endpoint Format</span></span>

![битовые поля для форматов bc6h сжатой конечной точки](images/bc6h-headers-med.png)

<span data-ttu-id="577ed-251">В этой таблице показаны битовые поля для сжатых конечных точек в качестве функции формата конечной точки, при этом каждый столбец задает кодировку, а каждая строка — битовое поле.</span><span class="sxs-lookup"><span data-stu-id="577ed-251">This table shows the bit fields for the compressed endpoints as a function of the endpoint format, with each column specifying an encoding and each row specifying a bit field.</span></span> <span data-ttu-id="577ed-252">В рамках этого подхода число битов для плиток с двумя регионами составляет 82, а для плиток с одним регионом — 65.</span><span class="sxs-lookup"><span data-stu-id="577ed-252">This approach takes up 82 bits for two-region tiles and 65 bits for one-region tiles.</span></span> <span data-ttu-id="577ed-253">Например, первые 5 бит для \[ \] кодировки 16 4 (в частности, самый правый столбец) имеют бит m \[ 4:0 \] , а следующие 10 битов — биты RW \[ 9:0 \] и т. д. с последними 6 битами, содержащими BW \[ 10:15 \] .</span><span class="sxs-lookup"><span data-stu-id="577ed-253">As an example, the first 5 bits for the one-region \[16 4\] encoding above (specifically the right-most column) are bits m\[4:0\], the next 10 bits are bits rw\[9:0\], and so on with the last 6 bits containing bw\[10:15\].</span></span>

<span data-ttu-id="577ed-254">Имена полей в таблице выше определяются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="577ed-254">The field names in the table above are defined as follows:</span></span>

| <span data-ttu-id="577ed-255">Поле</span><span class="sxs-lookup"><span data-stu-id="577ed-255">Field</span></span> | <span data-ttu-id="577ed-256">Переменная</span><span class="sxs-lookup"><span data-stu-id="577ed-256">Variable</span></span>          |
|-------|-------------------|
| <span data-ttu-id="577ed-257">m</span><span class="sxs-lookup"><span data-stu-id="577ed-257">m</span></span>     | <span data-ttu-id="577ed-258">mode</span><span class="sxs-lookup"><span data-stu-id="577ed-258">mode</span></span>              |
| <span data-ttu-id="577ed-259">d</span><span class="sxs-lookup"><span data-stu-id="577ed-259">d</span></span>     | <span data-ttu-id="577ed-260">индекс фигуры</span><span class="sxs-lookup"><span data-stu-id="577ed-260">shape index</span></span>       |
| <span data-ttu-id="577ed-261">rw</span><span class="sxs-lookup"><span data-stu-id="577ed-261">rw</span></span>    | <span data-ttu-id="577ed-262">ендпт \[ 0 \] . Значение \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="577ed-262">endpt\[0\].A\[0\]</span></span> |
| <span data-ttu-id="577ed-263">rx</span><span class="sxs-lookup"><span data-stu-id="577ed-263">rx</span></span>    | <span data-ttu-id="577ed-264">ендпт \[ 0 \] . Б \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="577ed-264">endpt\[0\].B\[0\]</span></span> |
| <span data-ttu-id="577ed-265">ry</span><span class="sxs-lookup"><span data-stu-id="577ed-265">ry</span></span>    | <span data-ttu-id="577ed-266">ендпт \[ 1 \] . Значение \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="577ed-266">endpt\[1\].A\[0\]</span></span> |
| <span data-ttu-id="577ed-267">rz</span><span class="sxs-lookup"><span data-stu-id="577ed-267">rz</span></span>    | <span data-ttu-id="577ed-268">ендпт \[ 1 \] . Б \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="577ed-268">endpt\[1\].B\[0\]</span></span> |
| <span data-ttu-id="577ed-269">gw</span><span class="sxs-lookup"><span data-stu-id="577ed-269">gw</span></span>    | <span data-ttu-id="577ed-270">ендпт \[ 0 \] . Значение \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="577ed-270">endpt\[0\].A\[1\]</span></span> |
| <span data-ttu-id="577ed-271">gx</span><span class="sxs-lookup"><span data-stu-id="577ed-271">gx</span></span>    | <span data-ttu-id="577ed-272">ендпт \[ 0 \] . B \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="577ed-272">endpt\[0\].B\[1\]</span></span> |
| <span data-ttu-id="577ed-273">gy</span><span class="sxs-lookup"><span data-stu-id="577ed-273">gy</span></span>    | <span data-ttu-id="577ed-274">ендпт \[ 1 \] . Значение \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="577ed-274">endpt\[1\].A\[1\]</span></span> |
| <span data-ttu-id="577ed-275">gz</span><span class="sxs-lookup"><span data-stu-id="577ed-275">gz</span></span>    | <span data-ttu-id="577ed-276">ендпт \[ 1 \] . B \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="577ed-276">endpt\[1\].B\[1\]</span></span> |
| <span data-ttu-id="577ed-277">bw</span><span class="sxs-lookup"><span data-stu-id="577ed-277">bw</span></span>    | <span data-ttu-id="577ed-278">ендпт \[ 0 \] . A \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="577ed-278">endpt\[0\].A\[2\]</span></span> |
| <span data-ttu-id="577ed-279">bx</span><span class="sxs-lookup"><span data-stu-id="577ed-279">bx</span></span>    | <span data-ttu-id="577ed-280">ендпт \[ 0 \] . B \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="577ed-280">endpt\[0\].B\[2\]</span></span> |
| <span data-ttu-id="577ed-281">by</span><span class="sxs-lookup"><span data-stu-id="577ed-281">by</span></span>    | <span data-ttu-id="577ed-282">ендпт \[ 1 \] . A \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="577ed-282">endpt\[1\].A\[2\]</span></span> |
| <span data-ttu-id="577ed-283">bz</span><span class="sxs-lookup"><span data-stu-id="577ed-283">bz</span></span>    | <span data-ttu-id="577ed-284">ендпт \[ 1 \] . B \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="577ed-284">endpt\[1\].B\[2\]</span></span> |



 

<span data-ttu-id="577ed-285">Ендпт \[ i \] , где i равно 0 или 1, ссылается на 0-й или первый набор конечных точек соответственно.</span><span class="sxs-lookup"><span data-stu-id="577ed-285">Endpt\[i\], where i is either 0 or 1, refers to the 0th or 1st set of endpoints respectively.</span></span>

## <a name="sign-extension-for-endpoint-values"></a><span data-ttu-id="577ed-286">Расширение знака для значений конечных точек</span><span class="sxs-lookup"><span data-stu-id="577ed-286">Sign Extension for Endpoint Values</span></span>

<span data-ttu-id="577ed-287">Для плиток с двумя регионами существует четыре значения конечных точек, для которых можно расширить знак.</span><span class="sxs-lookup"><span data-stu-id="577ed-287">For two-region tiles, there are four endpoint values that can be sign extended.</span></span> <span data-ttu-id="577ed-288">Ендпт \[ 0 \] . Подписывается, только если формат имеет формат со знаком; другие конечные точки подписываются только в том случае, если была преобразована конечная точка или если формат имеет формат со знаком.</span><span class="sxs-lookup"><span data-stu-id="577ed-288">Endpt\[0\].A is signed only if the format is a signed format; the other endpoints are signed only if the endpoint was transformed, or if the format is a signed format.</span></span> <span data-ttu-id="577ed-289">Приведенный ниже код демонстрирует алгоритм расширения знака значений конечной точки с двумя регионами.</span><span class="sxs-lookup"><span data-stu-id="577ed-289">The code below demonstrates the algorithm for extending the sign of two-region endpoint values.</span></span>

``` syntax
static void sign_extend_two_region(Pattern &p, IntEndpts endpts[NREGIONS_TWO])
{
    for (int i=0; i<NCHANNELS; ++i)
    {
      if (BC6H::FORMAT == SIGNED_F16)
        endpts[0].A[i] = SIGN_EXTEND(endpts[0].A[i], p.chan[i].prec);
      if (p.transformed || BC6H::FORMAT == SIGNED_F16)
      {
        endpts[0].B[i] = SIGN_EXTEND(endpts[0].B[i], p.chan[i].delta[0]);
        endpts[1].A[i] = SIGN_EXTEND(endpts[1].A[i], p.chan[i].delta[1]);
        endpts[1].B[i] = SIGN_EXTEND(endpts[1].B[i], p.chan[i].delta[2]);
      }
    }
}
```

<span data-ttu-id="577ed-290">Для мозаичных плиток поведение аналогично удалено только с ендпт \[ 1 \] .</span><span class="sxs-lookup"><span data-stu-id="577ed-290">For one-region tiles, the behavior is the same, only with endpt\[1\] removed.</span></span>

``` syntax
static void sign_extend_one_region(Pattern &p, IntEndpts endpts[NREGIONS_ONE])
{
    for (int i=0; i<NCHANNELS; ++i)
    {
    if (BC6H::FORMAT == SIGNED_F16)
        endpts[0].A[i] = SIGN_EXTEND(endpts[0].A[i], p.chan[i].prec);
    if (p.transformed || BC6H::FORMAT == SIGNED_F16) 
        endpts[0].B[i] = SIGN_EXTEND(endpts[0].B[i], p.chan[i].delta[0]);
    }
}
```

## <a name="transform-inversion-for-endpoint-values"></a><span data-ttu-id="577ed-291">Преобразование инверсии для значений конечной точки</span><span class="sxs-lookup"><span data-stu-id="577ed-291">Transform Inversion for Endpoint Values</span></span>

<span data-ttu-id="577ed-292">Для мозаичных плиток с двумя регионами преобразование применяет обратную кодировку для кодирования разницы, добавляя базовое значение в ендпт \[ 0 \] . А — для трех других записей — всего 9 операций добавления.</span><span class="sxs-lookup"><span data-stu-id="577ed-292">For two-region tiles, the transform applies the inverse of the difference encoding, adding the base value at endpt\[0\].A to the three other entries for a total of 9 add operations.</span></span> <span data-ttu-id="577ed-293">На следующем рисунке базовое значение представляется в виде "A0" и имеет наивысшую точность плавающей точки.</span><span class="sxs-lookup"><span data-stu-id="577ed-293">In the image below, the base value is represented as "A0" and has the highest floating point precision.</span></span> <span data-ttu-id="577ed-294">"A1" "B0" и "B1" — это дельты, вычисленные на основе значения привязки, и эти значения привязки представлены с более низкой точностью.</span><span class="sxs-lookup"><span data-stu-id="577ed-294">"A1," "B0," and "B1" are all deltas calculated from the anchor value, and these delta values are represented with lower precision.</span></span> <span data-ttu-id="577ed-295">(A0 соответствует ендпт \[ 0 \] . A, B0 соответствует ендпт \[ 0 \] . B, a1 соответствует ендпт \[ 1 \] . A, а B1 соответствует ендпт \[ 1 \] . B.)</span><span class="sxs-lookup"><span data-stu-id="577ed-295">(A0 corresponds to endpt\[0\].A, B0 corresponds to endpt\[0\].B, A1 corresponds to endpt\[1\].A, and B1 corresponds to endpt\[1\].B.)</span></span>

![расчет значений конечных точек инверсии преобразования](images/bc6h-transform-inverse.png)

<span data-ttu-id="577ed-297">Для плиток с одним регионом существует только одно дельта-смещение и, следовательно, только три операции добавления.</span><span class="sxs-lookup"><span data-stu-id="577ed-297">For one-region tiles there is only one delta offset, and therefore only 3 add operations.</span></span>

<span data-ttu-id="577ed-298">Декомпрессор должен гарантировать, что результаты обратного преобразования не будут переполнить точность ендпт \[ 0 \] . a.</span><span class="sxs-lookup"><span data-stu-id="577ed-298">The decompressor must ensure that that the results of the inverse transform will not overflow the precision of endpt\[0\].a.</span></span> <span data-ttu-id="577ed-299">В случае переполнения значения, которые являются результатом обратного преобразования, должны быть заключены в оболочку из того же числа битов.</span><span class="sxs-lookup"><span data-stu-id="577ed-299">In the case of an overflow, the values resulting from the inverse transform must wrap within the same number of bits.</span></span> <span data-ttu-id="577ed-300">Если точность A0 — "p" битов, алгоритм преобразования выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="577ed-300">If the precision of A0 is "p" bits, then the transform algorithm is:</span></span>

`B0 = (B0 + A0) & ((1 << p) - 1)`

<span data-ttu-id="577ed-301">Для форматов со знаком результаты вычисления дельты также должны иметь расширение со знаком.</span><span class="sxs-lookup"><span data-stu-id="577ed-301">For signed formats, the results of the delta calculation must be sign extended as well.</span></span> <span data-ttu-id="577ed-302">Если в ходе операции расширение знака рассматривается расширение обоих знаков, где 0 — положительное, а 1 — отрицательное, расширение знака 0 обработает фиксацию выше.</span><span class="sxs-lookup"><span data-stu-id="577ed-302">If the sign extension operation considers extending both signs, where 0 is positive and 1 is negative, then the sign extension of 0 takes care of the clamp above.</span></span> <span data-ttu-id="577ed-303">Аналогично, после фиксации выше необходимо расширять знаком только значение 1 (отрицательное).</span><span class="sxs-lookup"><span data-stu-id="577ed-303">Equivalently, after the clamp above, only a value of 1 (negative) needs to be sign extended.</span></span>

## <a name="unquantization-of-color-endpoints"></a><span data-ttu-id="577ed-304">Ункуантизатион конечных точек цвета</span><span class="sxs-lookup"><span data-stu-id="577ed-304">Unquantization of Color Endpoints</span></span>

<span data-ttu-id="577ed-305">Учитывая, что конечные точки не сжаты, следующий шаг — выполнить исходное расквантование конечных точек цвета.</span><span class="sxs-lookup"><span data-stu-id="577ed-305">Given the uncompressed endpoints, the next step is to perform an initial unquantization of the color endpoints.</span></span> <span data-ttu-id="577ed-306">Этот процесс состоит из трех этапов.</span><span class="sxs-lookup"><span data-stu-id="577ed-306">This involves three steps:</span></span>

-   <span data-ttu-id="577ed-307">Расквантование цветовых палитр</span><span class="sxs-lookup"><span data-stu-id="577ed-307">An unquantization of the color palettes</span></span>
-   <span data-ttu-id="577ed-308">Интерполяция палитр</span><span class="sxs-lookup"><span data-stu-id="577ed-308">Interpolation of the palettes</span></span>
-   <span data-ttu-id="577ed-309">Завершение расквантования</span><span class="sxs-lookup"><span data-stu-id="577ed-309">Unquantization finalization</span></span>

<span data-ttu-id="577ed-310">Разделение процесса расквантования на две части (расквантование цветовой палитры перед интерполяцией и окончательное расквантование после интерполяции) уменьшает число необходимых операций умножения по сравнению с полным расквантованием перед интерполяцией палитры.</span><span class="sxs-lookup"><span data-stu-id="577ed-310">Separating the unquantization process into two parts (color palette unquantization before interpolation and final unquantization after interpolation) reduces the number of multiplication operations required when compared to a full unquantization process before palette interpolation.</span></span>

<span data-ttu-id="577ed-311">Код ниже иллюстрирует процесс извлечения оценок исходных 16-разрядных значений цвета с последующим использованием предоставленных значений веса для добавления в палитру 6 дополнительных значений цвета.</span><span class="sxs-lookup"><span data-stu-id="577ed-311">The code below illustrates the process for retrieving estimates of the original 16-bit color values, and then using the supplied weight values to add 6 additional color values to the palette.</span></span> <span data-ttu-id="577ed-312">Та же операция выполняется в каждом канале.</span><span class="sxs-lookup"><span data-stu-id="577ed-312">The same operation is performed on each channel.</span></span>

``` syntax
int aWeight3[] = {0, 9, 18, 27, 37, 46, 55, 64};
int aWeight4[] = {0, 4, 9, 13, 17, 21, 26, 30, 34, 38, 43, 47, 51, 55, 60, 64};

// c1, c2: endpoints of a component
void generate_palette_unquantized(UINT8 uNumIndices, int c1, int c2, int prec, UINT16 palette[NINDICES])
{
    int* aWeights;
    if(uNumIndices == 8)
        aWeights = aWeight3;
    else  // uNumIndices == 16
        aWeights = aWeight4;

    int a = unquantize(c1, prec); 
    int b = unquantize(c2, prec);

    // interpolate
    for(int i = 0; i < uNumIndices; ++i)
        palette[i] = finish_unquantize((a * (64 - aWeights[i]) + b * aWeights[i] + 32) >> 6);
}
```

<span data-ttu-id="577ed-313">В следующем примере кода показан процесс интерполяции с учетом следующих соображений:</span><span class="sxs-lookup"><span data-stu-id="577ed-313">The next code sample demonstrates the interpolation process, with the following observations:</span></span>

-   <span data-ttu-id="577ed-314">Поскольку полный диапазон значений цвета для функции **unquantize** (ниже) — с -32 768 до 65 535, средство интерполяции реализуется с использованием 17-разрядного арифметического со знаком.</span><span class="sxs-lookup"><span data-stu-id="577ed-314">Since the full range of color values for the **unquantize** function (below) are from -32768 to 65535, the interpolator is implemented using 17-bit signed arithmetic.</span></span>
-   <span data-ttu-id="577ed-315">После интерполяции значения передаются в функцию **Finish \_ ункуантизе** (описывается в третьем примере в этом разделе), который применяет окончательное масштабирование.</span><span class="sxs-lookup"><span data-stu-id="577ed-315">After interpolation, the values are passed to the **finish\_unquantize** function (described in the third sample in this section), which applies the final scaling.</span></span>
-   <span data-ttu-id="577ed-316">Все аппаратные распаковщики должны возвращать из этих функций результаты с точными значениями разрядов.</span><span class="sxs-lookup"><span data-stu-id="577ed-316">All hardware decompressors are required to return bit-accurate results with these functions.</span></span>

``` syntax
int unquantize(int comp, int uBitsPerComp)
{
    int unq, s = 0;
    switch(BC6H::FORMAT)
    {
    case UNSIGNED_F16:
        if(uBitsPerComp >= 15)
            unq = comp;
        else if(comp == 0)
            unq = 0;
        else if(comp == ((1 << uBitsPerComp) - 1))
            unq = 0xFFFF;
        else
            unq = ((comp << 16) + 0x8000) >> uBitsPerComp;
        break;

    case SIGNED_F16:
        if(uBitsPerComp >= 16)
            unq = comp;
        else
        {
            if(comp < 0)
            {
                s = 1;
                comp = -comp;
            }

            if(comp == 0)
                unq = 0;
            else if(comp >= ((1 << (uBitsPerComp - 1)) - 1))
                unq = 0x7FFF;
            else
                unq = ((comp << 15) + 0x4000) >> (uBitsPerComp-1);

            if(s)
                unq = -unq;
        }
        break;
    }
    return unq;
}
```

<span data-ttu-id="577ed-317">метод **Finish \_ ункуантизе** вызывается после интерполяции палитры.</span><span class="sxs-lookup"><span data-stu-id="577ed-317">**finish\_unquantize** is called after palette interpolation.</span></span> <span data-ttu-id="577ed-318">Функция **unquantize** откладывает масштабирование на 31/32 для значений со знаком и на 31/64 для значений без знака.</span><span class="sxs-lookup"><span data-stu-id="577ed-318">The **unquantize** function postpones the scaling by 31/32 for signed, 31/64 for unsigned.</span></span> <span data-ttu-id="577ed-319">Это поведение необходимо, чтобы окончательное значение находилось в допустимом полудиапазоне (-0x7BFF–0x7BFF) по окончании интерполяции палитры с целью уменьшения общего количества необходимых умножений.</span><span class="sxs-lookup"><span data-stu-id="577ed-319">This behavior is required to get the final value into valid half range(-0x7BFF ~ 0x7BFF) after the palette interpolation is completed in order to reduce the number of necessary multiplications.</span></span> <span data-ttu-id="577ed-320">**Finish \_ ункуантизе** применяет окончательное масштабирование и возвращает **короткое значение без знака** , которое возвращается в **половину**.</span><span class="sxs-lookup"><span data-stu-id="577ed-320">**finish\_unquantize** applies the final scaling and returns an **unsigned short** value that gets reinterpreted into **half**.</span></span>

``` syntax
unsigned short finish_unquantize(int comp)
{
    if(BC6H::FORMAT == UNSIGNED_F16)
    {
        comp = (comp * 31) >> 6;                                         // scale the magnitude by 31/64
        return (unsigned short) comp;
    }
    else // (BC6H::FORMAT == SIGNED_F16)
    {
        comp = (comp < 0) ? -(((-comp) * 31) >> 5) : (comp * 31) >> 5;   // scale the magnitude by 31/32
        int s = 0;
        if(comp < 0)
        {
            s = 0x8000;
            comp = -comp;
        }
        return (unsigned short) (s | comp);
    }
}
```

## <a name="related-topics"></a><span data-ttu-id="577ed-321">См. также</span><span class="sxs-lookup"><span data-stu-id="577ed-321">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="577ed-322">Сжатие блоков текстуры в Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="577ed-322">Texture Block Compression in Direct3D 11</span></span>](texture-block-compression-in-direct3d-11.md)
</dt> </dl>

 

 