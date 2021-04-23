---
title: Формат BC7
description: Формат BC7 — это формат сжатия текстур, используемый для высококачественного сжатия данных RGB и RGBA.
ms.assetid: DF333106-293E-4B3E-A1EB-B0BF0ADBAC72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b9b64c3d4a8b5e960077a9f33de82ff08cd4bbc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413459"
---
# <a name="bc7-format"></a><span data-ttu-id="94981-103">Формат BC7</span><span class="sxs-lookup"><span data-stu-id="94981-103">BC7 Format</span></span>

<span data-ttu-id="94981-104">Формат BC7 — это формат сжатия текстур, используемый для высококачественного сжатия данных RGB и RGBA.</span><span class="sxs-lookup"><span data-stu-id="94981-104">The BC7 format is a texture compression format used for high-quality compression of RGB and RGBA data.</span></span>

-   [<span data-ttu-id="94981-105">Сведения о формате BC7/DXGI \_ \_ BC7</span><span class="sxs-lookup"><span data-stu-id="94981-105">About BC7/DXGI\_FORMAT\_BC7</span></span>](/windows)
-   [<span data-ttu-id="94981-106">Реализация BC7</span><span class="sxs-lookup"><span data-stu-id="94981-106">BC7 Implementation</span></span>](#bc7-implementation)
-   [<span data-ttu-id="94981-107">Декодирование формата BC7</span><span class="sxs-lookup"><span data-stu-id="94981-107">Decoding the BC7 Format</span></span>](#decoding-the-bc7-format)
-   [<span data-ttu-id="94981-108">См. также</span><span class="sxs-lookup"><span data-stu-id="94981-108">Related topics</span></span>](#related-topics)

<span data-ttu-id="94981-109">Сведения о режимах блоков формата BC7 доступны в статье [Справочник по режимам формата BC7](bc7-format-mode-reference.md).</span><span class="sxs-lookup"><span data-stu-id="94981-109">For info about the block modes of the BC7 format, see [BC7 Format Mode Reference](bc7-format-mode-reference.md).</span></span>

## <a name="about-bc7dxgi_format_bc7"></a><span data-ttu-id="94981-110">Сведения о формате BC7/DXGI \_ \_ BC7</span><span class="sxs-lookup"><span data-stu-id="94981-110">About BC7/DXGI\_FORMAT\_BC7</span></span>

<span data-ttu-id="94981-111">BC7 задается следующими \_ значениями перечисления в формате DXGI:</span><span class="sxs-lookup"><span data-stu-id="94981-111">BC7 is specified by the following DXGI\_FORMAT enumeration values:</span></span>

-   <span data-ttu-id="94981-112">**DXGI \_ FORMAT \_ BC7 \_ Type**.</span><span class="sxs-lookup"><span data-stu-id="94981-112">**DXGI\_FORMAT\_BC7\_TYPELESS**.</span></span>
-   <span data-ttu-id="94981-113">**DXGI \_ FORMAT \_ BC7 \_ UNORM**.</span><span class="sxs-lookup"><span data-stu-id="94981-113">**DXGI\_FORMAT\_BC7\_UNORM**.</span></span>
-   <span data-ttu-id="94981-114">**DXGI \_ ФОРМАТ \_ BC7 \_ UNORM \_ sRGB**.</span><span class="sxs-lookup"><span data-stu-id="94981-114">**DXGI\_FORMAT\_BC7\_UNORM\_SRGB**.</span></span>

<span data-ttu-id="94981-115">Формат BC7 можно использовать для ресурсов текстуры [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (включая массивы), Texture3D или TextureCube (включая массивы).</span><span class="sxs-lookup"><span data-stu-id="94981-115">The BC7 format can be used for [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (including arrays), Texture3D, or TextureCube (including arrays) texture resources.</span></span> <span data-ttu-id="94981-116">Аналогичным образом этот формат применяется к любым поверхностям MIP-карты, связанным с этими ресурсами.</span><span class="sxs-lookup"><span data-stu-id="94981-116">Similarly, this format applies to any MIP-map surfaces associated with these resources.</span></span>

<span data-ttu-id="94981-117">В BC7 используется фиксируемый размер блоков — 16 байтов (128 битов) и фиксированный размер плитки — 4x4 текселя.</span><span class="sxs-lookup"><span data-stu-id="94981-117">BC7 uses a fixed block size of 16 bytes (128 bits) and a fixed tile size of 4x4 texels.</span></span> <span data-ttu-id="94981-118">Как и в случае с предыдущими форматами BC, изображения текстур крупнее, чем поддерживаемый размер плитки (4x4), сжимаются с использованием нескольких блоков.</span><span class="sxs-lookup"><span data-stu-id="94981-118">As with previous BC formats, texture images larger than the supported tile size (4x4) are compressed by using multiple blocks.</span></span> <span data-ttu-id="94981-119">Это же удостоверение адресации также применяется к трехмерным изображениям, MIP-картам, картам кубов и массивам текстуры.</span><span class="sxs-lookup"><span data-stu-id="94981-119">This addressing identity also applies to three-dimensional images and MIP-maps, cubemaps, and texture arrays.</span></span> <span data-ttu-id="94981-120">Все плитки изображений должны иметь один формат.</span><span class="sxs-lookup"><span data-stu-id="94981-120">All image tiles must be of the same format.</span></span>

<span data-ttu-id="94981-121">BC7 сжимает трехканальные (RGB) и четырехканальные (RGBA) изображения данных с фиксированной запятой.</span><span class="sxs-lookup"><span data-stu-id="94981-121">BC7 compresses both three-channel (RGB) and four-channel (RGBA) fixed-point data images.</span></span> <span data-ttu-id="94981-122">Как правило, источник данных имеет 8 битов на компонент цвета (канал), хотя этот формат в состоянии шифровать исходные данные с большим числом битов на компонент цвета.</span><span class="sxs-lookup"><span data-stu-id="94981-122">Typically, source data is 8 bits per color component (channel), although the format is capable of encoding source data with higher bits per color component.</span></span> <span data-ttu-id="94981-123">Все плитки изображений должны иметь один формат.</span><span class="sxs-lookup"><span data-stu-id="94981-123">All image tiles must be of the same format.</span></span>

<span data-ttu-id="94981-124">Декодер BC7 выполняет распаковку до применения фильтрации текстур.</span><span class="sxs-lookup"><span data-stu-id="94981-124">The BC7 decoder performs decompression before texture filtering is applied.</span></span>

<span data-ttu-id="94981-125">Оборудование для распаковки BC7 должно иметь битовую точность, то есть возвращать результаты, идентичные результатам, возвращаемым декодером, который описан в этом документе.</span><span class="sxs-lookup"><span data-stu-id="94981-125">BC7 decompression hardware must be bit accurate; that is, the hardware must return results that are identical to the results returned by the decoder described in this document.</span></span>

## <a name="bc7-implementation"></a><span data-ttu-id="94981-126">Реализация BC7</span><span class="sxs-lookup"><span data-stu-id="94981-126">BC7 Implementation</span></span>

<span data-ttu-id="94981-127">Реализация BC7 может указывать один из 8 режимов, при этом режим будет указан в наименее значимом бите из 16-байтового (128-битового) блока.</span><span class="sxs-lookup"><span data-stu-id="94981-127">A BC7 implementation can specify one of 8 modes, with the mode specified in the least significant bit of the 16 byte (128 bit) block.</span></span> <span data-ttu-id="94981-128">Этот режим кодируется нулевым или большим количеством битов со значением 0, за которым следует 1.</span><span class="sxs-lookup"><span data-stu-id="94981-128">The mode is encoded by zero or more bits with a value of 0 followed by a 1.</span></span>

<span data-ttu-id="94981-129">Блок BC7 может содержать несколько пар конечных точек.</span><span class="sxs-lookup"><span data-stu-id="94981-129">A BC7 block can contain multiple endpoint pairs.</span></span> <span data-ttu-id="94981-130">Для целей этой документации набор индексов, соответствующих паре конечных точек, может называться "подмножеством".</span><span class="sxs-lookup"><span data-stu-id="94981-130">For the purposes of this documentation, the set of indices that correspond to an endpoint pair may be referred to as a "subset."</span></span> <span data-ttu-id="94981-131">Кроме того, в некоторых блочных режимах представление конечной точки кодируется в форме, которая в этой документации будет называться "РБГП", где бит "P" представляет общий наименее значащий бит для цветовых компонентов конечной точки.</span><span class="sxs-lookup"><span data-stu-id="94981-131">Also, in some block modes, the endpoint representation is encoded in a form that -- again, for the purposes of this documentation -- shall be referred to as "RBGP," where the "P" bit represents a shared least significant bit for the color components of the endpoint.</span></span> <span data-ttu-id="94981-132">Например, если представление конечной точки для формата имеет вид RGB 5.5.5.1, то конечная точка интерпретируется как значение RGB 6.6.6, где состояние P-бита определяет наименее значимый бит каждого компонента.</span><span class="sxs-lookup"><span data-stu-id="94981-132">For example, if the endpoint representation for the format is "RGB 5.5.5.1," then the endpoint is interpreted as an RGB 6.6.6 value, where the state of the P-bit defines the least significant bit of each component.</span></span> <span data-ttu-id="94981-133">Аналогично, для исходных данных с альфа-каналом, если представление формата имеет значение "РГБАП 5.5.5.5.1", то конечная точка интерепретед как RGBA 6.6.6.6.</span><span class="sxs-lookup"><span data-stu-id="94981-133">Similarly, for source data with an alpha channel, if the representation for the format is "RGBAP 5.5.5.5.1," then the endpoint is interepreted as RGBA 6.6.6.6.</span></span> <span data-ttu-id="94981-134">В зависимости от режима блоков можно указать общий наименее значимый бит для обеих конечных точек подмножества по отдельности (2 P-бита на подмножество) или совместно (1 P-бит на подмножество).</span><span class="sxs-lookup"><span data-stu-id="94981-134">Depending on the block mode, you can specify the shared least significant bit for either both endpoints of a subset individually (2 P-bits per subset), or shared between endpoints of a subset (1 P-bit per subset).</span></span>

<span data-ttu-id="94981-135">Для блоков BC7, которые явно не кодируют альфа-компонент, блок BC7 состоит из битов режима, битов раздела, сжатых конечных точек, сжатых индексов и необязательного P-бита.</span><span class="sxs-lookup"><span data-stu-id="94981-135">For BC7 blocks that don't explicitly encode the alpha component, a BC7 block consists of mode bits, partition bits, compressed endpoints, compressed indices, and an optional P-bit.</span></span> <span data-ttu-id="94981-136">В этих блоках конечные точки имеют представление только RGB, а альфа-компонент декодируется как 1.0 для всех текселей в исходных данных.</span><span class="sxs-lookup"><span data-stu-id="94981-136">In these blocks the endpoints have an RGB-only representation and the alpha component is decoded as 1.0 for all texels in the source data.</span></span>

<span data-ttu-id="94981-137">Для блоков BC7 с объединенными компонентами цвета и альфа-компонентами блок состоит из битов режима, сжатых конечных точек, сжатых индексов, необязательных битов раздела и P-бита.</span><span class="sxs-lookup"><span data-stu-id="94981-137">For BC7 blocks that have combined color and alpha components, a block consists of mode bits, compressed endpoints, compressed indices, and optional partition bits and a P-bit.</span></span> <span data-ttu-id="94981-138">В этих блоках цвета конечной точки выражаются в формате RGBA, а значения альфа-компонента интерполируются вместе со значениями цветового компонента.</span><span class="sxs-lookup"><span data-stu-id="94981-138">In these blocks, the endpoint colors are expressed in RGBA format, and alpha component values are interpolated alongside the color component values.</span></span>

<span data-ttu-id="94981-139">Для блоков BC7 с отдельными компонентами цвета и альфа-компонентами блок состоит из битов режима, битов поворота, сжатых конечных точек, сжатых индексов и необязательного бита средства выбора индексов.</span><span class="sxs-lookup"><span data-stu-id="94981-139">For BC7 blocks that have separate color and alpha components, a block consists of mode bits, rotation bits, compressed endpoints, compressed indices, and an optional index selector bit.</span></span> <span data-ttu-id="94981-140">Эти блоки имеют эффективный вектор \[ R, G, B \] и скалярный альфа \[ -канал в \] отдельном формате.</span><span class="sxs-lookup"><span data-stu-id="94981-140">These blocks have an effective RGB vector \[R, G, B\] and a scalar alpha channel \[A\] separately encoded.</span></span>

<span data-ttu-id="94981-141">В следующей таблице перечислены компоненты каждого типа блоков.</span><span class="sxs-lookup"><span data-stu-id="94981-141">The following table lists the components of each block type.</span></span>



| <span data-ttu-id="94981-142">Блок BC7 содержит...</span><span class="sxs-lookup"><span data-stu-id="94981-142">BC7 block contains...</span></span>     | <span data-ttu-id="94981-143">биты режима</span><span class="sxs-lookup"><span data-stu-id="94981-143">mode bits</span></span> | <span data-ttu-id="94981-144">биты поворота</span><span class="sxs-lookup"><span data-stu-id="94981-144">rotation bits</span></span> | <span data-ttu-id="94981-145">бит средства выбора индекса</span><span class="sxs-lookup"><span data-stu-id="94981-145">index selector bit</span></span> | <span data-ttu-id="94981-146">биты разделов</span><span class="sxs-lookup"><span data-stu-id="94981-146">partition bits</span></span> | <span data-ttu-id="94981-147">сжатые конечные точки</span><span class="sxs-lookup"><span data-stu-id="94981-147">compressed endpoints</span></span> | <span data-ttu-id="94981-148">P-бит</span><span class="sxs-lookup"><span data-stu-id="94981-148">P-bit</span></span>    | <span data-ttu-id="94981-149">сжатые индексы</span><span class="sxs-lookup"><span data-stu-id="94981-149">compressed indices</span></span> |
|---------------------------|-----------|---------------|--------------------|----------------|----------------------|----------|--------------------|
| <span data-ttu-id="94981-150">только компоненты цвета</span><span class="sxs-lookup"><span data-stu-id="94981-150">color components only</span></span>     | <span data-ttu-id="94981-151">обязательно</span><span class="sxs-lookup"><span data-stu-id="94981-151">required</span></span>  | <span data-ttu-id="94981-152">Недоступно</span><span class="sxs-lookup"><span data-stu-id="94981-152">N/A</span></span>           | <span data-ttu-id="94981-153">Недоступно</span><span class="sxs-lookup"><span data-stu-id="94981-153">N/A</span></span>                | <span data-ttu-id="94981-154">обязательно</span><span class="sxs-lookup"><span data-stu-id="94981-154">required</span></span>       | <span data-ttu-id="94981-155">обязательно</span><span class="sxs-lookup"><span data-stu-id="94981-155">required</span></span>             | <span data-ttu-id="94981-156">необязательно</span><span class="sxs-lookup"><span data-stu-id="94981-156">optional</span></span> | <span data-ttu-id="94981-157">обязательно</span><span class="sxs-lookup"><span data-stu-id="94981-157">required</span></span>           |
| <span data-ttu-id="94981-158">сочетание цвет + альфа</span><span class="sxs-lookup"><span data-stu-id="94981-158">color + alpha combined</span></span>    | <span data-ttu-id="94981-159">обязательно</span><span class="sxs-lookup"><span data-stu-id="94981-159">required</span></span>  | <span data-ttu-id="94981-160">Недоступно</span><span class="sxs-lookup"><span data-stu-id="94981-160">N/A</span></span>           | <span data-ttu-id="94981-161">Недоступно</span><span class="sxs-lookup"><span data-stu-id="94981-161">N/A</span></span>                | <span data-ttu-id="94981-162">необязательно</span><span class="sxs-lookup"><span data-stu-id="94981-162">optional</span></span>       | <span data-ttu-id="94981-163">обязательно</span><span class="sxs-lookup"><span data-stu-id="94981-163">required</span></span>             | <span data-ttu-id="94981-164">необязательно</span><span class="sxs-lookup"><span data-stu-id="94981-164">optional</span></span> | <span data-ttu-id="94981-165">обязательно</span><span class="sxs-lookup"><span data-stu-id="94981-165">required</span></span>           |
| <span data-ttu-id="94981-166">цвета и альфа по отдельности</span><span class="sxs-lookup"><span data-stu-id="94981-166">color and alpha separated</span></span> | <span data-ttu-id="94981-167">обязательно</span><span class="sxs-lookup"><span data-stu-id="94981-167">required</span></span>  | <span data-ttu-id="94981-168">обязательно</span><span class="sxs-lookup"><span data-stu-id="94981-168">required</span></span>      | <span data-ttu-id="94981-169">необязательно</span><span class="sxs-lookup"><span data-stu-id="94981-169">optional</span></span>           | <span data-ttu-id="94981-170">Недоступно</span><span class="sxs-lookup"><span data-stu-id="94981-170">N/A</span></span>            | <span data-ttu-id="94981-171">обязательно</span><span class="sxs-lookup"><span data-stu-id="94981-171">required</span></span>             | <span data-ttu-id="94981-172">Недоступно</span><span class="sxs-lookup"><span data-stu-id="94981-172">N/A</span></span>      | <span data-ttu-id="94981-173">обязательно</span><span class="sxs-lookup"><span data-stu-id="94981-173">required</span></span>           |



 

<span data-ttu-id="94981-174">BC7 определяет палитру цветов по примерной линии между двумя конечными точками.</span><span class="sxs-lookup"><span data-stu-id="94981-174">BC7 defines a palette of colors on an approximate line between two endpoints.</span></span> <span data-ttu-id="94981-175">Значение режима определяет количество интерполируемых пар конечных точек на блок.</span><span class="sxs-lookup"><span data-stu-id="94981-175">The mode value determines the number of interpolating endpoint pairs per block.</span></span> <span data-ttu-id="94981-176">BC7 сохраняет один индекс палитры на тексель.</span><span class="sxs-lookup"><span data-stu-id="94981-176">BC7 stores one palette index per texel.</span></span>

<span data-ttu-id="94981-177">Для каждого подмножества индексов, соответствующего паре конечных точек, кодировщик фиксирует состояние одного бита сжатых данных индекса для этого подмножества.</span><span class="sxs-lookup"><span data-stu-id="94981-177">For each subset of indices that corresponds to a pair of endpoints, the encoder fixes the state of one bit of the compressed index data for that subset.</span></span> <span data-ttu-id="94981-178">Для этого выбирается такой порядок конечных точек, который позволяет индексу так называемого назначенного индекса "исправления" задать свой самый значимый бит равным 0, и который затем можно удалить, оставив один бит на подмножество.</span><span class="sxs-lookup"><span data-stu-id="94981-178">It does so by choosing an endpoint order that allows the index for the designated "fix-up" index to set its most significant bit to 0, and which can then be discarded, saving one bit per subset.</span></span> <span data-ttu-id="94981-179">Для режимов блоков с одним подмножеством индекс исправления — это всегда нулевой индекс.</span><span class="sxs-lookup"><span data-stu-id="94981-179">For block modes with only a single subset, the fix-up index is always index 0.</span></span>

## <a name="decoding-the-bc7-format"></a><span data-ttu-id="94981-180">Декодирование формата BC7</span><span class="sxs-lookup"><span data-stu-id="94981-180">Decoding the BC7 Format</span></span>

<span data-ttu-id="94981-181">В псевдокоде ниже показаны действия по распаковке пикселя в точке (x,y) при наличии 16-байтового блока BC7</span><span class="sxs-lookup"><span data-stu-id="94981-181">The following pseudocode outlines the steps to decompress the pixel at (x,y) given the 16 byte BC7 block.</span></span>

``` syntax
decompress_bc7(x, y, block)
{
    mode = extract_mode(block);
    
    //decode partition data from explicit partition bits
    subset_index = 0;
    num_subsets = 1;
    
    if (mode.type == 0 OR == 1 OR == 2 OR == 3 OR == 7)
    {
        num_subsets = get_num_subsets(mode.type);
        partition_set_id = extract_partition_set_id(mode, block);
        subset_index = get_partition_index(num_subsets, partition_set_id, x, y);
    }
    
    //extract raw, compressed endpoint bits
    UINT8 endpoint_array[num_subsets][4] = extract_endpoints(mode, block);
    
    //decode endpoint color and alpha for each subset
    fully_decode_endpoints(endpoint_array, mode, block);
    
    //endpoints are now complete.
    UINT8 endpoint_start[4] = endpoint_array[2 * subset_index];
    UINT8 endpoint_end[4]   = endpoint_array[2 * subset_index + 1];
        
    //Determine the palette index for this pixel
    alpha_index     = get_alpha_index(block, mode, x, y);
    alpha_bitcount  = get_alpha_bitcount(block, mode);
    color_index     = get_color_index(block, mode, x, y);
    color_bitcount  = get_color_bitcount(block, mode);

    //determine output
    UINT8 output[4];
    output.rgb = interpolate(endpoint_start.rgb, endpoint_end.rgb, color_index, color_bitcount);
    output.a   = interpolate(endpoint_start.a,   endpoint_end.a,   alpha_index, alpha_bitcount);
    
    if (mode.type == 4 OR == 5)
    {
        //Decode the 2 color rotation bits as follows:
        // 00 – Block format is Scalar(A) Vector(RGB) - no swapping
        // 01 – Block format is Scalar(R) Vector(AGB) - swap A and R
        // 10 – Block format is Scalar(G) Vector(RAB) - swap A and G
        // 11 - Block format is Scalar(B) Vector(RGA) - swap A and B
        rotation = extract_rot_bits(mode, block);
        output = swap_channels(output, rotation);
    }
    
}
```

<span data-ttu-id="94981-182">В следующем псевдокоде показаны шаги, которые позволят полностью декодировать компоненты цвета и альфа-компоненты конечной точки для каждого подмножества с 16-байтовым блоком BC7.</span><span class="sxs-lookup"><span data-stu-id="94981-182">The followoing pseudocode outlines the steps to fully decode endpoint color and alpha components for each subset given a 16-byte BC7 block.</span></span>

``` syntax
fully_decode_endpoints(endpoint_array, mode, block)
{
    //first handle modes that have P-bits
    if (mode.type == 0 OR == 1 OR == 3 OR == 6 OR == 7)
    {
        for each endpoint i
        {
            //component-wise left-shift
            endpoint_array[i].rgba = endpoint_array[i].rgba << 1;
        }
        
        //if P-bit is shared
        if (mode.type == 1) 
        {
            pbit_zero = extract_pbit_zero(mode, block);
            pbit_one = extract_pbit_one(mode, block);
            
            //rgb component-wise insert pbits
            endpoint_array[0].rgb |= pbit_zero;
            endpoint_array[1].rgb |= pbit_zero;
            endpoint_array[2].rgb |= pbit_one;
            endpoint_array[3].rgb |= pbit_one;  
        }
        else //unique P-bit per endpoint
        {  
            pbit_array = extract_pbit_array(mode, block);
            for each endpoint i
            {
                endpoint_array[i].rgba |= pbit_array[i];
            }
        }
    }

    for each endpoint i
    {
        // Color_component_precision & alpha_component_precision includes pbit
        // left shift endpoint components so that their MSB lies in bit 7
        endpoint_array[i].rgb = endpoint_array[i].rgb << (8 - color_component_precision(mode));
        endpoint_array[i].a = endpoint_array[i].a << (8 - alpha_component_precision(mode));

        // Replicate each component's MSB into the LSBs revealed by the left-shift operation above
        endpoint_array[i].rgb = endpoint_array[i].rgb | (endpoint_array[i].rgb >> color_component_precision(mode));
        endpoint_array[i].a = endpoint_array[i].a | (endpoint_array[i].a >> alpha_component_precision(mode));
    }
        
    //If this mode does not explicitly define the alpha component
    //set alpha equal to 1.0
    if (mode.type == 0 OR == 1 OR == 2 OR == 3)
    {
        for each endpoint i
        {
            endpoint_array[i].a = 255; //i.e. alpha = 1.0f
        }
    }
}
```

<span data-ttu-id="94981-183">Для создания каждого интерполированного компонента для каждого подмножества используйте следующий алгоритм: пусть c — это создаваемый компонент, e0 — это компонент конечной точки 0 подмножества, а e1 — это компонент конечной точки 1 подмножества.</span><span class="sxs-lookup"><span data-stu-id="94981-183">To generate each interpolated component for each subset, use the following algorithm: let "c" be the component to generate; let "e0" be that component of endpoint 0 of the subset; and let "e1" be that component of endpoint 1 of the subset.</span></span>

``` syntax
UINT16 aWeight2[] = {0, 21, 43, 64};
UINT16 aWeight3[] = {0, 9, 18, 27, 37, 46, 55, 64};
UINT16 aWeight4[] = {0, 4, 9, 13, 17, 21, 26, 30, 34, 38, 43, 47, 51, 55, 60, 64};

UINT8 interpolate(UINT8 e0, UINT8 e1, UINT8 index, UINT8 indexprecision)
{
    if(indexprecision == 2)
        return (UINT8) (((64 - aWeights2[index])*UINT16(e0) + aWeights2[index]*UINT16(e1) + 32) >> 6);
    else if(indexprecision == 3)
        return (UINT8) (((64 - aWeights3[index])*UINT16(e0) + aWeights3[index]*UINT16(e1) + 32) >> 6);
    else // indexprecision == 4
        return (UINT8) (((64 - aWeights4[index])*UINT16(e0) + aWeights4[index]*UINT16(e1) + 32) >> 6);
}
```

<span data-ttu-id="94981-184">В следующем псевдокоде показано извлечение индексов и число битов для компонентов цвета и альфа-компонентов.</span><span class="sxs-lookup"><span data-stu-id="94981-184">The following pseudocode illustrates how to extract indices and bit counts for color and alpha components.</span></span> <span data-ttu-id="94981-185">Блоки с отдельными компонентами цвета и альфа-компонентами также имеют два набора данных индекса: один — для векторного канала, другой — для скалярного.</span><span class="sxs-lookup"><span data-stu-id="94981-185">Blocks with separate color and alpha also have two sets of index data: one for the vector channel, and one for the scalar channel.</span></span> <span data-ttu-id="94981-186">Для режима 4 эти индексы имеют разную ширину (2 или 3 бита), и также имеется однобитовое средство выбора, указывающее, используют ли векторные или скалярные данные 3-битовые индексы.</span><span class="sxs-lookup"><span data-stu-id="94981-186">For Mode 4, these indices are of differing widths (2 or 3 bits), and there is a one-bit selector which specifies whether the vector or scalar data uses the 3-bit indices.</span></span> <span data-ttu-id="94981-187">(Извлечение количества альфа-битов аналогично извлечению количества цветовых битов, однако с обратным поведением в бите **idxMode**.)</span><span class="sxs-lookup"><span data-stu-id="94981-187">(Extracting the alpha bit count is similar to extracting color bit count but with inverse behavior based on the **idxMode** bit.)</span></span>

``` syntax
bitcount get_color_bitcount(block, mode)
{
    if (mode.type == 0 OR == 1)
        return 3;
    
    if (mode.type == 2 OR == 3 OR == 5 OR == 7)
        return 2;
    
    if (mode.type == 6)
        return 4;
        
    //The only remaining case is Mode 4 with 1-bit index selector
    idxMode = extract_idxMode(block);
    if (idxMode == 0)
        return 2;
    else
        return 3;
}
```

## <a name="related-topics"></a><span data-ttu-id="94981-188">См. также</span><span class="sxs-lookup"><span data-stu-id="94981-188">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94981-189">Сжатие блоков текстуры в Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="94981-189">Texture Block Compression in Direct3D 11</span></span>](texture-block-compression-in-direct3d-11.md)
</dt> </dl>

 

 