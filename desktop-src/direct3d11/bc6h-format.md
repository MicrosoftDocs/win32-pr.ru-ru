---
title: Формат BC6H
description: Формат BC6H — это формат сжатия текстуры, предназначенный для обеспечения поддержки цветовых пространств HDR в исходных данных.
ms.assetid: D6A1A729-5023-4A94-A8DB-5954D453E136
keywords:
- BC6H
- DXGI_FORMAT_BC6H
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92ea15e0275bc478c0708ce08f531d8888a3c84d
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335228"
---
# <a name="bc6h-format"></a><span data-ttu-id="17660-105">Формат BC6H</span><span class="sxs-lookup"><span data-stu-id="17660-105">BC6H Format</span></span>

<span data-ttu-id="17660-106">Формат BC6H — это формат сжатия текстуры, предназначенный для обеспечения поддержки цветовых пространств HDR в исходных данных.</span><span class="sxs-lookup"><span data-stu-id="17660-106">The BC6H format is a texture compression format designed to support high-dynamic range (HDR) color spaces in source data.</span></span>

-   [<span data-ttu-id="17660-107">Сведения о формате BC6H/DXGI \_ \_ BC6H</span><span class="sxs-lookup"><span data-stu-id="17660-107">About BC6H/DXGI\_FORMAT\_BC6H</span></span>](/windows)
-   [<span data-ttu-id="17660-108">Реализация BC6H</span><span class="sxs-lookup"><span data-stu-id="17660-108">BC6H Implementation</span></span>](#bc6h-implementation)
-   [<span data-ttu-id="17660-109">Декодирование формата BC6H</span><span class="sxs-lookup"><span data-stu-id="17660-109">Decoding the BC6H Format</span></span>](#decoding-the-bc6h-format)
-   [<span data-ttu-id="17660-110">Формат сжатых конечных точек BC6H</span><span class="sxs-lookup"><span data-stu-id="17660-110">BC6H Compressed Endpoint Format</span></span>](#bc6h-compressed-endpoint-format)
-   [<span data-ttu-id="17660-111">Расширение знака для значений конечных точек</span><span class="sxs-lookup"><span data-stu-id="17660-111">Sign Extension for Endpoint Values</span></span>](#sign-extension-for-endpoint-values)
-   [<span data-ttu-id="17660-112">Преобразование инверсии для значений конечной точки</span><span class="sxs-lookup"><span data-stu-id="17660-112">Transform Inversion for Endpoint Values</span></span>](#transform-inversion-for-endpoint-values)
-   [<span data-ttu-id="17660-113">Ункуантизатион конечных точек цвета</span><span class="sxs-lookup"><span data-stu-id="17660-113">Unquantization of Color Endpoints</span></span>](#unquantization-of-color-endpoints)
-   [<span data-ttu-id="17660-114">См. также</span><span class="sxs-lookup"><span data-stu-id="17660-114">Related topics</span></span>](#related-topics)

## <a name="about-bc6hdxgi_format_bc6h"></a><span data-ttu-id="17660-115">Сведения о формате BC6H/DXGI \_ \_ BC6H</span><span class="sxs-lookup"><span data-stu-id="17660-115">About BC6H/DXGI\_FORMAT\_BC6H</span></span>

<span data-ttu-id="17660-116">Формат BC6H обеспечивает высококачественное сжатие изображений, использующих три канала цветов HDR с 16-разрядным значением для каждого канала цвета в составе значения (16:16:16).</span><span class="sxs-lookup"><span data-stu-id="17660-116">The BC6H format provides high-quality compression for images that use three HDR color channels, with a 16-bit value for each color channel of the value (16:16:16).</span></span> <span data-ttu-id="17660-117">Альфа-канал не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="17660-117">There is no support for an alpha channel.</span></span>

<span data-ttu-id="17660-118">BC6H задается следующими \_ значениями перечисления в формате DXGI:</span><span class="sxs-lookup"><span data-stu-id="17660-118">BC6H is specified by the following DXGI\_FORMAT enumeration values:</span></span>

-   <span data-ttu-id="17660-119">**DXGI \_ FORMAT \_ BC6H \_ Type**.</span><span class="sxs-lookup"><span data-stu-id="17660-119">**DXGI\_FORMAT\_BC6H\_TYPELESS**.</span></span>
-   <span data-ttu-id="17660-120">**DXGI \_ FORMAT \_ BC6H \_ UF16**.</span><span class="sxs-lookup"><span data-stu-id="17660-120">**DXGI\_FORMAT\_BC6H\_UF16**.</span></span> <span data-ttu-id="17660-121">В этом формате BC6H не используется знаковый бит в 16-разрядных значениях канала цвета с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="17660-121">This BC6H format does not use a sign bit in the 16-bit floating point color channel values.</span></span>
-   <span data-ttu-id="17660-122">**DXGI \_ FORMAT \_ BC6H \_ SF16**. В этом формате BC6H используется бит знака в 16-битных значениях канала цвета с плавающей точкой.</span><span class="sxs-lookup"><span data-stu-id="17660-122">**DXGI\_FORMAT\_BC6H\_SF16**.This BC6H format uses a sign bit in the 16-bit floating point color channel values.</span></span>

> [!Note]  
> <span data-ttu-id="17660-123">16-разрядный формат с плавающей точкой для цветовых каналов часто называют "половинным" форматом с плавающей точкой.</span><span class="sxs-lookup"><span data-stu-id="17660-123">The 16 bit floating point format for color channels is often referred to as a "half" floating point format.</span></span> <span data-ttu-id="17660-124">Формат имеет следующее расположение битов:</span><span class="sxs-lookup"><span data-stu-id="17660-124">This format has the following bit layout:</span></span>
>
> |  <span data-ttu-id="17660-125">Формат</span><span class="sxs-lookup"><span data-stu-id="17660-125">Format</span></span>                     | <span data-ttu-id="17660-126">Разрядный макет</span><span class="sxs-lookup"><span data-stu-id="17660-126">Bit layout</span></span>                                                |
> |-----------------------|-------------------------------------------------|
> | <span data-ttu-id="17660-127">UF16 (без знака с плавающей запятой)</span><span class="sxs-lookup"><span data-stu-id="17660-127">UF16 (unsigned float)</span></span> | <span data-ttu-id="17660-128">5 разрядов экспоненты + 11 разрядов мантиссы</span><span class="sxs-lookup"><span data-stu-id="17660-128">5 exponent bits + 11 mantissa bits</span></span>              |
> | <span data-ttu-id="17660-129">SF16 (со знаком с плавающей запятой)</span><span class="sxs-lookup"><span data-stu-id="17660-129">SF16 (signed float)</span></span>   | <span data-ttu-id="17660-130">1 разряд знака + 5 разрядов экспоненты + 10 разрядов мантиссы</span><span class="sxs-lookup"><span data-stu-id="17660-130">1 sign bit + 5 exponent bits + 10 mantissa bits</span></span> |
>
> 
>
>  

 

<span data-ttu-id="17660-131">Формат BC6H можно использовать для ресурсов текстуры [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (включая массивы), Texture3D или TextureCube (включая массивы).</span><span class="sxs-lookup"><span data-stu-id="17660-131">The BC6H format can be used for [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (including arrays), Texture3D, or TextureCube (including arrays) texture resources.</span></span> <span data-ttu-id="17660-132">Аналогичным образом этот формат применяется к любым поверхностям MIP-карты, связанным с этими ресурсами.</span><span class="sxs-lookup"><span data-stu-id="17660-132">Similarly, this format applies to any MIP-map surfaces associated with these resources.</span></span>

<span data-ttu-id="17660-133">В BC6H используется фиксируемый размер блоков — 16 байтов (128 битов) и фиксированный размер плитки — 4x4 текселя.</span><span class="sxs-lookup"><span data-stu-id="17660-133">BC6H uses a fixed block size of 16 bytes (128 bits) and a fixed tile size of 4x4 texels.</span></span> <span data-ttu-id="17660-134">Как и в случае с предыдущими форматами BC, изображения текстур крупнее, чем поддерживаемый размер плитки (4x4), сжимаются с использованием нескольких блоков.</span><span class="sxs-lookup"><span data-stu-id="17660-134">As with previous BC formats, texture images larger than the supported tile size (4x4) are compressed by using multiple blocks.</span></span> <span data-ttu-id="17660-135">Это удостоверение адресации также применяется к трехмерным изображениям, MIP-картам, кубемапс и массивам текстур.</span><span class="sxs-lookup"><span data-stu-id="17660-135">This addressing identity applies also to three-dimensional images, MIP-maps, cubemaps, and texture arrays.</span></span> <span data-ttu-id="17660-136">Все плитки изображений должны иметь один формат.</span><span class="sxs-lookup"><span data-stu-id="17660-136">All image tiles must be of the same format.</span></span>

<span data-ttu-id="17660-137">Некоторые важные замечания о формате BC6H:</span><span class="sxs-lookup"><span data-stu-id="17660-137">Some important notes about the BC6H format:</span></span>

-   <span data-ttu-id="17660-138">BC6H поддерживает денормализацию чисел с плавающей запятой, но не поддерживает сущности типа INF (бесконечность) и NaN (не число).</span><span class="sxs-lookup"><span data-stu-id="17660-138">BC6H supports floating point denormalization, but does not support INF (infinity) and NaN (not a number).</span></span> <span data-ttu-id="17660-139">Исключение — это режим со знаком для BC6H ( \_ Формат DXGI \_ BC6H \_ SF16), поддерживающий-INF (отрицательная бесконечность).</span><span class="sxs-lookup"><span data-stu-id="17660-139">The exception is the signed mode of BC6H (DXGI\_FORMAT\_BC6H\_SF16), which supports -INF (negative infinity).</span></span> <span data-ttu-id="17660-140">Обратите внимание, что эта поддержка для-INF является просто артефактом самого формата и не поддерживается кодировщиками для этого формата.</span><span class="sxs-lookup"><span data-stu-id="17660-140">Note that this support for -INF is merely an artifact of the format itself, and is not specifically supported by encoders for this format.</span></span> <span data-ttu-id="17660-141">В общем случае, когда кодировщики сталкиваются с INF (положительными или отрицательными) или неоднородными входными данными, они должны \\ преобразовывать эти данные в максимально допустимое значение представления, отличного от INF, и сопоставлять NaN с 0 до сжатия.</span><span class="sxs-lookup"><span data-stu-id="17660-141">In general, when encoders encounter INF (positive or negative) or NaN input data, they should \\ convert that data to the maximum allowable non-INF representation value, and map NaN to 0 prior to compression.</span></span>
-   <span data-ttu-id="17660-142">Формат BC6H не поддерживает альфа-канал.</span><span class="sxs-lookup"><span data-stu-id="17660-142">BC6H does not support an alpha channel.</span></span>
-   <span data-ttu-id="17660-143">Декодер BC6H выполняет распаковку до того, как приступит к фильтрации текстур.</span><span class="sxs-lookup"><span data-stu-id="17660-143">The BC6H decoder performs decompression before it performs texture filtering.</span></span>
-   <span data-ttu-id="17660-144">Распаковка BC6H должна быть точной. то есть оборудование должно вернуть результаты, идентичные декодеру, описанному в этой документации.</span><span class="sxs-lookup"><span data-stu-id="17660-144">BC6H decompression must be bit accurate; that is, the hardware must return results that are identical to the decoder described in this documentation.</span></span>

## <a name="bc6h-implementation"></a><span data-ttu-id="17660-145">Реализация BC6H</span><span class="sxs-lookup"><span data-stu-id="17660-145">BC6H Implementation</span></span>

<span data-ttu-id="17660-146">Блок BC6H состоит из битов режима, сжатых конечных точек, сжатых индексов и дополнительного индекса раздела.</span><span class="sxs-lookup"><span data-stu-id="17660-146">A BC6H block consists of mode bits, compressed endpoints, compressed indices, and an optional partition index.</span></span> <span data-ttu-id="17660-147">Этот формат задает 14 разных режимов.</span><span class="sxs-lookup"><span data-stu-id="17660-147">This format specifies 14 different modes.</span></span>

<span data-ttu-id="17660-148">Цвет конечной точки хранится в виде RGB-триады.</span><span class="sxs-lookup"><span data-stu-id="17660-148">An endpoint color is stored as an RGB triplet.</span></span> <span data-ttu-id="17660-149">BC6H определяет цветовую палитру по приблизительной линии, проходящей через несколько определенных конечных точек цвета.</span><span class="sxs-lookup"><span data-stu-id="17660-149">BC6H defines a palette of colors on an approximate line across a number of defined color endpoints.</span></span> <span data-ttu-id="17660-150">Кроме того, в зависимости от режима плитка может быть разделена на два региона или обрабатываться как один регион, где плитка с двумя регионами имеет отдельный набор конечных точек цвета для каждого региона.</span><span class="sxs-lookup"><span data-stu-id="17660-150">Also, depending on the mode, a tile can be divided into two regions or treated as a single region, where a two-region tile has a separate set of color endpoints for each region.</span></span> <span data-ttu-id="17660-151">BC6H сохраняет один индекс палитры на тексель.</span><span class="sxs-lookup"><span data-stu-id="17660-151">BC6H stores one palette index per texel.</span></span>

<span data-ttu-id="17660-152">Если вы работаете с двумя регионами, число возможных разделов равно 32.</span><span class="sxs-lookup"><span data-stu-id="17660-152">In the two-region case, there are 32 possible partitions.</span></span>

## <a name="decoding-the-bc6h-format"></a><span data-ttu-id="17660-153">Декодирование формата BC6H</span><span class="sxs-lookup"><span data-stu-id="17660-153">Decoding the BC6H Format</span></span>

<span data-ttu-id="17660-154">В псевдокоде ниже изображены действия по распаковке пикселя в точке (x,y) при наличии 16-байтового блока BC6H.</span><span class="sxs-lookup"><span data-stu-id="17660-154">The pseudocode below shows the steps to decompress the pixel at (x,y) given the 16 byte BC6H block.</span></span>

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

<span data-ttu-id="17660-155">В таблице ниже указано число битов и значения для каждого из 14 возможных форматов для блоков BC6H.</span><span class="sxs-lookup"><span data-stu-id="17660-155">The following table contains the bit count and values for each of the 14 possible formats for BC6H blocks.</span></span> 

| <span data-ttu-id="17660-156">Режим</span><span class="sxs-lookup"><span data-stu-id="17660-156">Mode</span></span> | <span data-ttu-id="17660-157">Индексы разделов</span><span class="sxs-lookup"><span data-stu-id="17660-157">Partition Indices</span></span> | <span data-ttu-id="17660-158">Секция</span><span class="sxs-lookup"><span data-stu-id="17660-158">Partition</span></span> | <span data-ttu-id="17660-159">Конечные точки цвета</span><span class="sxs-lookup"><span data-stu-id="17660-159">Color Endpoints</span></span>                  | <span data-ttu-id="17660-160">Биты режима</span><span class="sxs-lookup"><span data-stu-id="17660-160">Mode Bits</span></span>      |
|------|-------------------|-----------|----------------------------------|----------------|
| <span data-ttu-id="17660-161">1</span><span class="sxs-lookup"><span data-stu-id="17660-161">1</span></span>    | <span data-ttu-id="17660-162">46 битов</span><span class="sxs-lookup"><span data-stu-id="17660-162">46 bits</span></span>           | <span data-ttu-id="17660-163">5 битов</span><span class="sxs-lookup"><span data-stu-id="17660-163">5 bits</span></span>    | <span data-ttu-id="17660-164">75 битов (10,555, 10,555, 10,555)</span><span class="sxs-lookup"><span data-stu-id="17660-164">75 bits (10.555, 10.555, 10.555)</span></span> | <span data-ttu-id="17660-165">2 бита (00)</span><span class="sxs-lookup"><span data-stu-id="17660-165">2 bits (00)</span></span>    |
| <span data-ttu-id="17660-166">2</span><span class="sxs-lookup"><span data-stu-id="17660-166">2</span></span>    | <span data-ttu-id="17660-167">46 битов</span><span class="sxs-lookup"><span data-stu-id="17660-167">46 bits</span></span>           | <span data-ttu-id="17660-168">5 битов</span><span class="sxs-lookup"><span data-stu-id="17660-168">5 bits</span></span>    | <span data-ttu-id="17660-169">75 битов (7666, 7666, 7666)</span><span class="sxs-lookup"><span data-stu-id="17660-169">75 bits (7666, 7666, 7666)</span></span>       | <span data-ttu-id="17660-170">2 бита (01)</span><span class="sxs-lookup"><span data-stu-id="17660-170">2 bits (01)</span></span>    |
| <span data-ttu-id="17660-171">3</span><span class="sxs-lookup"><span data-stu-id="17660-171">3</span></span>    | <span data-ttu-id="17660-172">46 битов</span><span class="sxs-lookup"><span data-stu-id="17660-172">46 bits</span></span>           | <span data-ttu-id="17660-173">5 битов</span><span class="sxs-lookup"><span data-stu-id="17660-173">5 bits</span></span>    | <span data-ttu-id="17660-174">72 бита (11,555, 11,444, 11,444)</span><span class="sxs-lookup"><span data-stu-id="17660-174">72 bits (11.555, 11.444, 11.444)</span></span> | <span data-ttu-id="17660-175">5 битов (00010)</span><span class="sxs-lookup"><span data-stu-id="17660-175">5 bits (00010)</span></span> |
| <span data-ttu-id="17660-176">4</span><span class="sxs-lookup"><span data-stu-id="17660-176">4</span></span>    | <span data-ttu-id="17660-177">46 битов</span><span class="sxs-lookup"><span data-stu-id="17660-177">46 bits</span></span>           | <span data-ttu-id="17660-178">5 битов</span><span class="sxs-lookup"><span data-stu-id="17660-178">5 bits</span></span>    | <span data-ttu-id="17660-179">72 бита (11,444, 11,555, 11,444)</span><span class="sxs-lookup"><span data-stu-id="17660-179">72 bits (11.444, 11.555, 11.444)</span></span> | <span data-ttu-id="17660-180">5 битов (00110)</span><span class="sxs-lookup"><span data-stu-id="17660-180">5 bits (00110)</span></span> |
| <span data-ttu-id="17660-181">5</span><span class="sxs-lookup"><span data-stu-id="17660-181">5</span></span>    | <span data-ttu-id="17660-182">46 битов</span><span class="sxs-lookup"><span data-stu-id="17660-182">46 bits</span></span>           | <span data-ttu-id="17660-183">5 битов</span><span class="sxs-lookup"><span data-stu-id="17660-183">5 bits</span></span>    | <span data-ttu-id="17660-184">72 бита (11,444, 11,444, 11,555)</span><span class="sxs-lookup"><span data-stu-id="17660-184">72 bits (11.444, 11.444, 11.555)</span></span> | <span data-ttu-id="17660-185">5 битов (01010)</span><span class="sxs-lookup"><span data-stu-id="17660-185">5 bits (01010)</span></span> |
| <span data-ttu-id="17660-186">6</span><span class="sxs-lookup"><span data-stu-id="17660-186">6</span></span>    | <span data-ttu-id="17660-187">46 битов</span><span class="sxs-lookup"><span data-stu-id="17660-187">46 bits</span></span>           | <span data-ttu-id="17660-188">5 битов</span><span class="sxs-lookup"><span data-stu-id="17660-188">5 bits</span></span>    | <span data-ttu-id="17660-189">72 бита (9555, 9555, 9555)</span><span class="sxs-lookup"><span data-stu-id="17660-189">72 bits (9555, 9555, 9555)</span></span>       | <span data-ttu-id="17660-190">5 битов (01110)</span><span class="sxs-lookup"><span data-stu-id="17660-190">5 bits (01110)</span></span> |
| <span data-ttu-id="17660-191">7</span><span class="sxs-lookup"><span data-stu-id="17660-191">7</span></span>    | <span data-ttu-id="17660-192">46 битов</span><span class="sxs-lookup"><span data-stu-id="17660-192">46 bits</span></span>           | <span data-ttu-id="17660-193">5 битов</span><span class="sxs-lookup"><span data-stu-id="17660-193">5 bits</span></span>    | <span data-ttu-id="17660-194">72 бита (8666, 8555, 8555)</span><span class="sxs-lookup"><span data-stu-id="17660-194">72 bits (8666, 8555, 8555)</span></span>       | <span data-ttu-id="17660-195">5 битов (10010)</span><span class="sxs-lookup"><span data-stu-id="17660-195">5 bits (10010)</span></span> |
| <span data-ttu-id="17660-196">8</span><span class="sxs-lookup"><span data-stu-id="17660-196">8</span></span>    | <span data-ttu-id="17660-197">46 битов</span><span class="sxs-lookup"><span data-stu-id="17660-197">46 bits</span></span>           | <span data-ttu-id="17660-198">5 битов</span><span class="sxs-lookup"><span data-stu-id="17660-198">5 bits</span></span>    | <span data-ttu-id="17660-199">72 бита (8555, 8666, 8555)</span><span class="sxs-lookup"><span data-stu-id="17660-199">72 bits (8555, 8666, 8555)</span></span>       | <span data-ttu-id="17660-200">5 битов (10110)</span><span class="sxs-lookup"><span data-stu-id="17660-200">5 bits (10110)</span></span> |
| <span data-ttu-id="17660-201">9</span><span class="sxs-lookup"><span data-stu-id="17660-201">9</span></span>    | <span data-ttu-id="17660-202">46 битов</span><span class="sxs-lookup"><span data-stu-id="17660-202">46 bits</span></span>           | <span data-ttu-id="17660-203">5 битов</span><span class="sxs-lookup"><span data-stu-id="17660-203">5 bits</span></span>    | <span data-ttu-id="17660-204">72 бита (8555, 8555, 8666)</span><span class="sxs-lookup"><span data-stu-id="17660-204">72 bits (8555, 8555, 8666)</span></span>       | <span data-ttu-id="17660-205">5 битов (11010)</span><span class="sxs-lookup"><span data-stu-id="17660-205">5 bits (11010)</span></span> |
| <span data-ttu-id="17660-206">10</span><span class="sxs-lookup"><span data-stu-id="17660-206">10</span></span>   | <span data-ttu-id="17660-207">46 битов</span><span class="sxs-lookup"><span data-stu-id="17660-207">46 bits</span></span>           | <span data-ttu-id="17660-208">5 битов</span><span class="sxs-lookup"><span data-stu-id="17660-208">5 bits</span></span>    | <span data-ttu-id="17660-209">72 бита (6666, 6666, 6666)</span><span class="sxs-lookup"><span data-stu-id="17660-209">72 bits (6666, 6666, 6666)</span></span>       | <span data-ttu-id="17660-210">5 битов (11110)</span><span class="sxs-lookup"><span data-stu-id="17660-210">5 bits (11110)</span></span> |
| <span data-ttu-id="17660-211">11</span><span class="sxs-lookup"><span data-stu-id="17660-211">11</span></span>   | <span data-ttu-id="17660-212">63 бита</span><span class="sxs-lookup"><span data-stu-id="17660-212">63 bits</span></span>           | <span data-ttu-id="17660-213">0 битов</span><span class="sxs-lookup"><span data-stu-id="17660-213">0 bits</span></span>    | <span data-ttu-id="17660-214">60 битов (10,10, 10,10, 10,10)</span><span class="sxs-lookup"><span data-stu-id="17660-214">60 bits (10.10, 10.10, 10.10)</span></span>    | <span data-ttu-id="17660-215">5 битов (00011)</span><span class="sxs-lookup"><span data-stu-id="17660-215">5 bits (00011)</span></span> |
| <span data-ttu-id="17660-216">12</span><span class="sxs-lookup"><span data-stu-id="17660-216">12</span></span>   | <span data-ttu-id="17660-217">63 бита</span><span class="sxs-lookup"><span data-stu-id="17660-217">63 bits</span></span>           | <span data-ttu-id="17660-218">0 битов</span><span class="sxs-lookup"><span data-stu-id="17660-218">0 bits</span></span>    | <span data-ttu-id="17660-219">60 битов (11,9, 11,9, 11,9)</span><span class="sxs-lookup"><span data-stu-id="17660-219">60 bits (11.9, 11.9, 11.9)</span></span>       | <span data-ttu-id="17660-220">5 битов (00111)</span><span class="sxs-lookup"><span data-stu-id="17660-220">5 bits (00111)</span></span> |
| <span data-ttu-id="17660-221">13</span><span class="sxs-lookup"><span data-stu-id="17660-221">13</span></span>   | <span data-ttu-id="17660-222">63 бита</span><span class="sxs-lookup"><span data-stu-id="17660-222">63 bits</span></span>           | <span data-ttu-id="17660-223">0 битов</span><span class="sxs-lookup"><span data-stu-id="17660-223">0 bits</span></span>    | <span data-ttu-id="17660-224">60 битов (12,8, 12,8, 12,8)</span><span class="sxs-lookup"><span data-stu-id="17660-224">60 bits (12.8, 12.8, 12.8)</span></span>       | <span data-ttu-id="17660-225">5 битов (01011)</span><span class="sxs-lookup"><span data-stu-id="17660-225">5 bits (01011)</span></span> |
| <span data-ttu-id="17660-226">14</span><span class="sxs-lookup"><span data-stu-id="17660-226">14</span></span>   | <span data-ttu-id="17660-227">63 бита</span><span class="sxs-lookup"><span data-stu-id="17660-227">63 bits</span></span>           | <span data-ttu-id="17660-228">0 битов</span><span class="sxs-lookup"><span data-stu-id="17660-228">0 bits</span></span>    | <span data-ttu-id="17660-229">60 битов (16,4, 16,4, 16,4)</span><span class="sxs-lookup"><span data-stu-id="17660-229">60 bits (16.4, 16.4, 16.4)</span></span>       | <span data-ttu-id="17660-230">5 битов (01111)</span><span class="sxs-lookup"><span data-stu-id="17660-230">5 bits (01111)</span></span> |



 

<span data-ttu-id="17660-231">Каждый формат в этой таблице можно уникально идентифицировать битами режима.</span><span class="sxs-lookup"><span data-stu-id="17660-231">Each format in this table can be uniquely identified by the mode bits.</span></span> <span data-ttu-id="17660-232">Первые десять режимов используются для плиток с двумя регионами, а поле бита режима может иметь длину два бита или пять битов.</span><span class="sxs-lookup"><span data-stu-id="17660-232">The first ten modes are used for two-region tiles, and the mode bit field can be either two or five bits long.</span></span> <span data-ttu-id="17660-233">Эти блоки также имеют поля для конечных точек сжатого цвета (72 или 75 битов), раздела (5 битов) и индексов раздела (46 битов).</span><span class="sxs-lookup"><span data-stu-id="17660-233">These blocks also have fields for the compressed color endpoints (72 or 75 bits), the partition (5 bits), and the partition indices (46 bits).</span></span>

<span data-ttu-id="17660-234">Для конечных точек сжатого цвета значения в предыдущей таблице обозначают точность сохраненных конечных точек RGB и число битов, используемых для каждого значения цвета.</span><span class="sxs-lookup"><span data-stu-id="17660-234">For the compressed color endpoints, the values in the preceding table note the precision of the stored RGB endpoints, and the number of bits used for each color value.</span></span> <span data-ttu-id="17660-235">Например, режим 3 указывает на 11 уровень точности конечной точки цвета, а число битов, используемых для хранения дельта-значений преобразованных конечных точек для красного, синего и зеленого цветов (5, 4 и 4 соответственно).</span><span class="sxs-lookup"><span data-stu-id="17660-235">For example, mode 3 specifies a color endpoint precision level of 11, and the number of bits used to store the delta values of the transformed endpoints for the red, blue and green colors (5, 4, and 4 respectively).</span></span> <span data-ttu-id="17660-236">В режиме 10 не используется дельта-сжатие. Вместо этого все четыре конечные точки цвета сохраняются явно.</span><span class="sxs-lookup"><span data-stu-id="17660-236">Mode 10 does not use delta compression, and instead stores all four color endpoints explicitly.</span></span>

<span data-ttu-id="17660-237">Последние четыре режима блока используются для плиток с одним регионом, где поле режима равно 5 битам.</span><span class="sxs-lookup"><span data-stu-id="17660-237">The last four block modes are used for one-region tiles, where the mode field is 5 bits.</span></span> <span data-ttu-id="17660-238">Эти блоки имеют поля для конечных точек (60 битов) и сжатых индексов (63 бита),</span><span class="sxs-lookup"><span data-stu-id="17660-238">These blocks have fields for the endpoints (60 bits) and the compressed indices (63 bits).</span></span> <span data-ttu-id="17660-239">В режиме 11 (как и в режиме 10) не используется дельта-сжатие. Вместо этого конечные точки цвета сохраняются явно.</span><span class="sxs-lookup"><span data-stu-id="17660-239">Mode 11 (like Mode 10) does not use delta compression, and instead stores both color endpoints explicitly.</span></span>

<span data-ttu-id="17660-240">Режимы 10011, 10111, 11011 и 11111 (не показан) зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="17660-240">Modes 10011, 10111, 11011, and 11111 (not shown) are reserved.</span></span> <span data-ttu-id="17660-241">Не используйте их в своем кодировщике.</span><span class="sxs-lookup"><span data-stu-id="17660-241">Do not use these in your encoder.</span></span> <span data-ttu-id="17660-242">Если оборудование представляет собой переданные блоки и задан один из этих режимов, полученный распакованный блок должен содержать все нули во всех каналах, кроме альфа-канала.</span><span class="sxs-lookup"><span data-stu-id="17660-242">If the hardware is passed blocks with one of these modes specified, the resulting decompressed block must contain all zeroes in all channels except for the alpha channel.</span></span>

<span data-ttu-id="17660-243">Для BC6H альфа-канал должен всегда возвращать 1,0 независимо от режима.</span><span class="sxs-lookup"><span data-stu-id="17660-243">For BC6H, the alpha channel must always return 1.0 regardless of the mode.</span></span>

### <a name="bc6h-partition-set"></a><span data-ttu-id="17660-244">Набор разделов BC6H</span><span class="sxs-lookup"><span data-stu-id="17660-244">BC6H Partition Set</span></span>

<span data-ttu-id="17660-245">Существует 32 возможных набора разделов для плитки с двумя регионами, которые определены в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="17660-245">There are 32 possible partition sets for a two-region tile, and which are defined in the table below.</span></span> <span data-ttu-id="17660-246">Каждый блок 4x4 представляет одну фигуру.</span><span class="sxs-lookup"><span data-stu-id="17660-246">Each 4x4 block represents a single shape.</span></span>

![таблица наборов разделов bc6h](images/bc6h-partition-sets.png)

<span data-ttu-id="17660-248">В этой таблице наборов разделов выделенная полужирным шрифтом и подчеркиванием запись является расположением индекса исправления для подмножества 1 (которое задается с количеством битов на 1 меньше).</span><span class="sxs-lookup"><span data-stu-id="17660-248">In this table of partition sets, the bolded and underlined entry is the location of the fix-up index for subset 1 (which is specified with one less bit).</span></span> <span data-ttu-id="17660-249">Индекс исправления для подмножества 0 — это всегда нулевой индекс, поскольку разделение на разделы всегда организовано так, чтобы нулевой индекс находился в нулевом подмножестве.</span><span class="sxs-lookup"><span data-stu-id="17660-249">The fix-up index for subset 0 is always index 0, as the partitioning is always arranged such that index 0 is always in subset 0.</span></span> <span data-ttu-id="17660-250">Порядок разделения на разделы: из верхнего левого угла до нижнего правого, перемещаясь слева направо и сверху вниз.</span><span class="sxs-lookup"><span data-stu-id="17660-250">Partition order goes from top-left to bottom-right, moving left to right and then top to bottom.</span></span>

## <a name="bc6h-compressed-endpoint-format"></a><span data-ttu-id="17660-251">Формат сжатых конечных точек BC6H</span><span class="sxs-lookup"><span data-stu-id="17660-251">BC6H Compressed Endpoint Format</span></span>

![битовые поля для форматов bc6h сжатой конечной точки](images/bc6h-headers-med.png)

<span data-ttu-id="17660-253">В этой таблице показаны битовые поля для сжатых конечных точек в качестве функции формата конечной точки, при этом каждый столбец задает кодировку, а каждая строка — битовое поле.</span><span class="sxs-lookup"><span data-stu-id="17660-253">This table shows the bit fields for the compressed endpoints as a function of the endpoint format, with each column specifying an encoding and each row specifying a bit field.</span></span> <span data-ttu-id="17660-254">В рамках этого подхода число битов для плиток с двумя регионами составляет 82, а для плиток с одним регионом — 65.</span><span class="sxs-lookup"><span data-stu-id="17660-254">This approach takes up 82 bits for two-region tiles and 65 bits for one-region tiles.</span></span> <span data-ttu-id="17660-255">Например, первые 5 бит для \[ \] кодировки 16 4 (в частности, самый правый столбец) имеют бит m \[ 4:0 \] , а следующие 10 битов — биты RW \[ 9:0 \] и т. д. с последними 6 битами, содержащими BW \[ 10:15 \] .</span><span class="sxs-lookup"><span data-stu-id="17660-255">As an example, the first 5 bits for the one-region \[16 4\] encoding above (specifically the right-most column) are bits m\[4:0\], the next 10 bits are bits rw\[9:0\], and so on with the last 6 bits containing bw\[10:15\].</span></span>

<span data-ttu-id="17660-256">Имена полей в таблице выше определяются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="17660-256">The field names in the table above are defined as follows:</span></span>

| <span data-ttu-id="17660-257">Поле</span><span class="sxs-lookup"><span data-stu-id="17660-257">Field</span></span> | <span data-ttu-id="17660-258">Переменная</span><span class="sxs-lookup"><span data-stu-id="17660-258">Variable</span></span>          |
|-------|-------------------|
| <span data-ttu-id="17660-259">М</span><span class="sxs-lookup"><span data-stu-id="17660-259">m</span></span>     | <span data-ttu-id="17660-260">mode</span><span class="sxs-lookup"><span data-stu-id="17660-260">mode</span></span>              |
| <span data-ttu-id="17660-261">d</span><span class="sxs-lookup"><span data-stu-id="17660-261">d</span></span>     | <span data-ttu-id="17660-262">индекс фигуры</span><span class="sxs-lookup"><span data-stu-id="17660-262">shape index</span></span>       |
| <span data-ttu-id="17660-263">rw</span><span class="sxs-lookup"><span data-stu-id="17660-263">rw</span></span>    | <span data-ttu-id="17660-264">ендпт \[ 0 \] . Значение \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="17660-264">endpt\[0\].A\[0\]</span></span> |
| <span data-ttu-id="17660-265">rx</span><span class="sxs-lookup"><span data-stu-id="17660-265">rx</span></span>    | <span data-ttu-id="17660-266">ендпт \[ 0 \] . Б \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="17660-266">endpt\[0\].B\[0\]</span></span> |
| <span data-ttu-id="17660-267">ry</span><span class="sxs-lookup"><span data-stu-id="17660-267">ry</span></span>    | <span data-ttu-id="17660-268">ендпт \[ 1 \] . Значение \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="17660-268">endpt\[1\].A\[0\]</span></span> |
| <span data-ttu-id="17660-269">rz</span><span class="sxs-lookup"><span data-stu-id="17660-269">rz</span></span>    | <span data-ttu-id="17660-270">ендпт \[ 1 \] . Б \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="17660-270">endpt\[1\].B\[0\]</span></span> |
| <span data-ttu-id="17660-271">gw</span><span class="sxs-lookup"><span data-stu-id="17660-271">gw</span></span>    | <span data-ttu-id="17660-272">ендпт \[ 0 \] . Значение \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="17660-272">endpt\[0\].A\[1\]</span></span> |
| <span data-ttu-id="17660-273">gx</span><span class="sxs-lookup"><span data-stu-id="17660-273">gx</span></span>    | <span data-ttu-id="17660-274">ендпт \[ 0 \] . B \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="17660-274">endpt\[0\].B\[1\]</span></span> |
| <span data-ttu-id="17660-275">gy</span><span class="sxs-lookup"><span data-stu-id="17660-275">gy</span></span>    | <span data-ttu-id="17660-276">ендпт \[ 1 \] . Значение \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="17660-276">endpt\[1\].A\[1\]</span></span> |
| <span data-ttu-id="17660-277">gz</span><span class="sxs-lookup"><span data-stu-id="17660-277">gz</span></span>    | <span data-ttu-id="17660-278">ендпт \[ 1 \] . B \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="17660-278">endpt\[1\].B\[1\]</span></span> |
| <span data-ttu-id="17660-279">bw</span><span class="sxs-lookup"><span data-stu-id="17660-279">bw</span></span>    | <span data-ttu-id="17660-280">ендпт \[ 0 \] . A \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="17660-280">endpt\[0\].A\[2\]</span></span> |
| <span data-ttu-id="17660-281">bx</span><span class="sxs-lookup"><span data-stu-id="17660-281">bx</span></span>    | <span data-ttu-id="17660-282">ендпт \[ 0 \] . B \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="17660-282">endpt\[0\].B\[2\]</span></span> |
| <span data-ttu-id="17660-283">by</span><span class="sxs-lookup"><span data-stu-id="17660-283">by</span></span>    | <span data-ttu-id="17660-284">ендпт \[ 1 \] . A \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="17660-284">endpt\[1\].A\[2\]</span></span> |
| <span data-ttu-id="17660-285">bz</span><span class="sxs-lookup"><span data-stu-id="17660-285">bz</span></span>    | <span data-ttu-id="17660-286">ендпт \[ 1 \] . B \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="17660-286">endpt\[1\].B\[2\]</span></span> |



 

<span data-ttu-id="17660-287">Ендпт \[ i \] , где i равно 0 или 1, ссылается на 0-й или первый набор конечных точек соответственно.</span><span class="sxs-lookup"><span data-stu-id="17660-287">Endpt\[i\], where i is either 0 or 1, refers to the 0th or 1st set of endpoints respectively.</span></span>

## <a name="sign-extension-for-endpoint-values"></a><span data-ttu-id="17660-288">Расширение знака для значений конечных точек</span><span class="sxs-lookup"><span data-stu-id="17660-288">Sign Extension for Endpoint Values</span></span>

<span data-ttu-id="17660-289">Для плиток с двумя регионами существует четыре значения конечных точек, для которых можно расширить знак.</span><span class="sxs-lookup"><span data-stu-id="17660-289">For two-region tiles, there are four endpoint values that can be sign extended.</span></span> <span data-ttu-id="17660-290">Ендпт \[ 0 \] . Подписывается, только если формат имеет формат со знаком; другие конечные точки подписываются только в том случае, если была преобразована конечная точка или если формат имеет формат со знаком.</span><span class="sxs-lookup"><span data-stu-id="17660-290">Endpt\[0\].A is signed only if the format is a signed format; the other endpoints are signed only if the endpoint was transformed, or if the format is a signed format.</span></span> <span data-ttu-id="17660-291">Приведенный ниже код демонстрирует алгоритм расширения знака значений конечной точки с двумя регионами.</span><span class="sxs-lookup"><span data-stu-id="17660-291">The code below demonstrates the algorithm for extending the sign of two-region endpoint values.</span></span>

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

<span data-ttu-id="17660-292">Для мозаичных плиток поведение аналогично удалено только с ендпт \[ 1 \] .</span><span class="sxs-lookup"><span data-stu-id="17660-292">For one-region tiles, the behavior is the same, only with endpt\[1\] removed.</span></span>

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

## <a name="transform-inversion-for-endpoint-values"></a><span data-ttu-id="17660-293">Преобразование инверсии для значений конечной точки</span><span class="sxs-lookup"><span data-stu-id="17660-293">Transform Inversion for Endpoint Values</span></span>

<span data-ttu-id="17660-294">Для мозаичных плиток с двумя регионами преобразование применяет обратную кодировку для кодирования разницы, добавляя базовое значение в ендпт \[ 0 \] . А — для трех других записей — всего 9 операций добавления.</span><span class="sxs-lookup"><span data-stu-id="17660-294">For two-region tiles, the transform applies the inverse of the difference encoding, adding the base value at endpt\[0\].A to the three other entries for a total of 9 add operations.</span></span> <span data-ttu-id="17660-295">На следующем рисунке базовое значение представляется в виде "A0" и имеет наивысшую точность плавающей точки.</span><span class="sxs-lookup"><span data-stu-id="17660-295">In the image below, the base value is represented as "A0" and has the highest floating point precision.</span></span> <span data-ttu-id="17660-296">"A1" "B0" и "B1" — это дельты, вычисленные на основе значения привязки, и эти значения привязки представлены с более низкой точностью.</span><span class="sxs-lookup"><span data-stu-id="17660-296">"A1," "B0," and "B1" are all deltas calculated from the anchor value, and these delta values are represented with lower precision.</span></span> <span data-ttu-id="17660-297">(A0 соответствует ендпт \[ 0 \] . A, B0 соответствует ендпт \[ 0 \] . B, a1 соответствует ендпт \[ 1 \] . A, а B1 соответствует ендпт \[ 1 \] . B.)</span><span class="sxs-lookup"><span data-stu-id="17660-297">(A0 corresponds to endpt\[0\].A, B0 corresponds to endpt\[0\].B, A1 corresponds to endpt\[1\].A, and B1 corresponds to endpt\[1\].B.)</span></span>

![расчет значений конечных точек инверсии преобразования](images/bc6h-transform-inverse.png)

<span data-ttu-id="17660-299">Для плиток с одним регионом существует только одно дельта-смещение и, следовательно, только три операции добавления.</span><span class="sxs-lookup"><span data-stu-id="17660-299">For one-region tiles there is only one delta offset, and therefore only 3 add operations.</span></span>

<span data-ttu-id="17660-300">Декомпрессор должен гарантировать, что результаты обратного преобразования не будут переполнить точность ендпт \[ 0 \] . a.</span><span class="sxs-lookup"><span data-stu-id="17660-300">The decompressor must ensure that that the results of the inverse transform will not overflow the precision of endpt\[0\].a.</span></span> <span data-ttu-id="17660-301">В случае переполнения значения, которые являются результатом обратного преобразования, должны быть заключены в оболочку из того же числа битов.</span><span class="sxs-lookup"><span data-stu-id="17660-301">In the case of an overflow, the values resulting from the inverse transform must wrap within the same number of bits.</span></span> <span data-ttu-id="17660-302">Если точность A0 — "p" битов, алгоритм преобразования выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="17660-302">If the precision of A0 is "p" bits, then the transform algorithm is:</span></span>

`B0 = (B0 + A0) & ((1 << p) - 1)`

<span data-ttu-id="17660-303">Для форматов со знаком результаты вычисления дельты также должны иметь расширение со знаком.</span><span class="sxs-lookup"><span data-stu-id="17660-303">For signed formats, the results of the delta calculation must be sign extended as well.</span></span> <span data-ttu-id="17660-304">Если в ходе операции расширение знака рассматривается расширение обоих знаков, где 0 — положительное, а 1 — отрицательное, расширение знака 0 обработает фиксацию выше.</span><span class="sxs-lookup"><span data-stu-id="17660-304">If the sign extension operation considers extending both signs, where 0 is positive and 1 is negative, then the sign extension of 0 takes care of the clamp above.</span></span> <span data-ttu-id="17660-305">Аналогично, после фиксации выше необходимо расширять знаком только значение 1 (отрицательное).</span><span class="sxs-lookup"><span data-stu-id="17660-305">Equivalently, after the clamp above, only a value of 1 (negative) needs to be sign extended.</span></span>

## <a name="unquantization-of-color-endpoints"></a><span data-ttu-id="17660-306">Ункуантизатион конечных точек цвета</span><span class="sxs-lookup"><span data-stu-id="17660-306">Unquantization of Color Endpoints</span></span>

<span data-ttu-id="17660-307">Учитывая, что конечные точки не сжаты, следующий шаг — выполнить исходное расквантование конечных точек цвета.</span><span class="sxs-lookup"><span data-stu-id="17660-307">Given the uncompressed endpoints, the next step is to perform an initial unquantization of the color endpoints.</span></span> <span data-ttu-id="17660-308">Этот процесс состоит из трех этапов.</span><span class="sxs-lookup"><span data-stu-id="17660-308">This involves three steps:</span></span>

-   <span data-ttu-id="17660-309">Расквантование цветовых палитр</span><span class="sxs-lookup"><span data-stu-id="17660-309">An unquantization of the color palettes</span></span>
-   <span data-ttu-id="17660-310">Интерполяция палитр</span><span class="sxs-lookup"><span data-stu-id="17660-310">Interpolation of the palettes</span></span>
-   <span data-ttu-id="17660-311">Завершение расквантования</span><span class="sxs-lookup"><span data-stu-id="17660-311">Unquantization finalization</span></span>

<span data-ttu-id="17660-312">Разделение процесса расквантования на две части (расквантование цветовой палитры перед интерполяцией и окончательное расквантование после интерполяции) уменьшает число необходимых операций умножения по сравнению с полным расквантованием перед интерполяцией палитры.</span><span class="sxs-lookup"><span data-stu-id="17660-312">Separating the unquantization process into two parts (color palette unquantization before interpolation and final unquantization after interpolation) reduces the number of multiplication operations required when compared to a full unquantization process before palette interpolation.</span></span>

<span data-ttu-id="17660-313">Код ниже иллюстрирует процесс извлечения оценок исходных 16-разрядных значений цвета с последующим использованием предоставленных значений веса для добавления в палитру 6 дополнительных значений цвета.</span><span class="sxs-lookup"><span data-stu-id="17660-313">The code below illustrates the process for retrieving estimates of the original 16-bit color values, and then using the supplied weight values to add 6 additional color values to the palette.</span></span> <span data-ttu-id="17660-314">Та же операция выполняется в каждом канале.</span><span class="sxs-lookup"><span data-stu-id="17660-314">The same operation is performed on each channel.</span></span>

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

<span data-ttu-id="17660-315">В следующем примере кода показан процесс интерполяции с учетом следующих соображений:</span><span class="sxs-lookup"><span data-stu-id="17660-315">The next code sample demonstrates the interpolation process, with the following observations:</span></span>

-   <span data-ttu-id="17660-316">Поскольку полный диапазон значений цвета для функции **unquantize** (ниже) — с -32 768 до 65 535, средство интерполяции реализуется с использованием 17-разрядного арифметического со знаком.</span><span class="sxs-lookup"><span data-stu-id="17660-316">Since the full range of color values for the **unquantize** function (below) are from -32768 to 65535, the interpolator is implemented using 17-bit signed arithmetic.</span></span>
-   <span data-ttu-id="17660-317">После интерполяции значения передаются в функцию **Finish \_ ункуантизе** (описывается в третьем примере в этом разделе), который применяет окончательное масштабирование.</span><span class="sxs-lookup"><span data-stu-id="17660-317">After interpolation, the values are passed to the **finish\_unquantize** function (described in the third sample in this section), which applies the final scaling.</span></span>
-   <span data-ttu-id="17660-318">Все аппаратные распаковщики должны возвращать из этих функций результаты с точными значениями разрядов.</span><span class="sxs-lookup"><span data-stu-id="17660-318">All hardware decompressors are required to return bit-accurate results with these functions.</span></span>

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

<span data-ttu-id="17660-319">метод **Finish \_ ункуантизе** вызывается после интерполяции палитры.</span><span class="sxs-lookup"><span data-stu-id="17660-319">**finish\_unquantize** is called after palette interpolation.</span></span> <span data-ttu-id="17660-320">Функция **unquantize** откладывает масштабирование на 31/32 для значений со знаком и на 31/64 для значений без знака.</span><span class="sxs-lookup"><span data-stu-id="17660-320">The **unquantize** function postpones the scaling by 31/32 for signed, 31/64 for unsigned.</span></span> <span data-ttu-id="17660-321">Это поведение необходимо, чтобы окончательное значение находилось в допустимом полудиапазоне (-0x7BFF–0x7BFF) по окончании интерполяции палитры с целью уменьшения общего количества необходимых умножений.</span><span class="sxs-lookup"><span data-stu-id="17660-321">This behavior is required to get the final value into valid half range(-0x7BFF ~ 0x7BFF) after the palette interpolation is completed in order to reduce the number of necessary multiplications.</span></span> <span data-ttu-id="17660-322">**Finish \_ ункуантизе** применяет окончательное масштабирование и возвращает **короткое значение без знака** , которое возвращается в **половину**.</span><span class="sxs-lookup"><span data-stu-id="17660-322">**finish\_unquantize** applies the final scaling and returns an **unsigned short** value that gets reinterpreted into **half**.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="17660-323">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="17660-323">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17660-324">Сжатие блоков текстуры в Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="17660-324">Texture Block Compression in Direct3D 11</span></span>](texture-block-compression-in-direct3d-11.md)
</dt> </dl>

 

 