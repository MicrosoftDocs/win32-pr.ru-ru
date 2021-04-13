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
# <a name="bc7-format"></a>Формат BC7

Формат BC7 — это формат сжатия текстур, используемый для высококачественного сжатия данных RGB и RGBA.

-   [Сведения о формате BC7/DXGI \_ \_ BC7](/windows)
-   [Реализация BC7](#bc7-implementation)
-   [Декодирование формата BC7](#decoding-the-bc7-format)
-   [См. также](#related-topics)

Сведения о режимах блоков формата BC7 доступны в статье [Справочник по режимам формата BC7](bc7-format-mode-reference.md).

## <a name="about-bc7dxgi_format_bc7"></a>Сведения о формате BC7/DXGI \_ \_ BC7

BC7 задается следующими \_ значениями перечисления в формате DXGI:

-   **DXGI \_ FORMAT \_ BC7 \_ Type**.
-   **DXGI \_ FORMAT \_ BC7 \_ UNORM**.
-   **DXGI \_ ФОРМАТ \_ BC7 \_ UNORM \_ sRGB**.

Формат BC7 можно использовать для ресурсов текстуры [Texture2D](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (включая массивы), Texture3D или TextureCube (включая массивы). Аналогичным образом этот формат применяется к любым поверхностям MIP-карты, связанным с этими ресурсами.

В BC7 используется фиксируемый размер блоков — 16 байтов (128 битов) и фиксированный размер плитки — 4x4 текселя. Как и в случае с предыдущими форматами BC, изображения текстур крупнее, чем поддерживаемый размер плитки (4x4), сжимаются с использованием нескольких блоков. Это же удостоверение адресации также применяется к трехмерным изображениям, MIP-картам, картам кубов и массивам текстуры. Все плитки изображений должны иметь один формат.

BC7 сжимает трехканальные (RGB) и четырехканальные (RGBA) изображения данных с фиксированной запятой. Как правило, источник данных имеет 8 битов на компонент цвета (канал), хотя этот формат в состоянии шифровать исходные данные с большим числом битов на компонент цвета. Все плитки изображений должны иметь один формат.

Декодер BC7 выполняет распаковку до применения фильтрации текстур.

Оборудование для распаковки BC7 должно иметь битовую точность, то есть возвращать результаты, идентичные результатам, возвращаемым декодером, который описан в этом документе.

## <a name="bc7-implementation"></a>Реализация BC7

Реализация BC7 может указывать один из 8 режимов, при этом режим будет указан в наименее значимом бите из 16-байтового (128-битового) блока. Этот режим кодируется нулевым или большим количеством битов со значением 0, за которым следует 1.

Блок BC7 может содержать несколько пар конечных точек. Для целей этой документации набор индексов, соответствующих паре конечных точек, может называться "подмножеством". Кроме того, в некоторых блочных режимах представление конечной точки кодируется в форме, которая в этой документации будет называться "РБГП", где бит "P" представляет общий наименее значащий бит для цветовых компонентов конечной точки. Например, если представление конечной точки для формата имеет вид RGB 5.5.5.1, то конечная точка интерпретируется как значение RGB 6.6.6, где состояние P-бита определяет наименее значимый бит каждого компонента. Аналогично, для исходных данных с альфа-каналом, если представление формата имеет значение "РГБАП 5.5.5.5.1", то конечная точка интерепретед как RGBA 6.6.6.6. В зависимости от режима блоков можно указать общий наименее значимый бит для обеих конечных точек подмножества по отдельности (2 P-бита на подмножество) или совместно (1 P-бит на подмножество).

Для блоков BC7, которые явно не кодируют альфа-компонент, блок BC7 состоит из битов режима, битов раздела, сжатых конечных точек, сжатых индексов и необязательного P-бита. В этих блоках конечные точки имеют представление только RGB, а альфа-компонент декодируется как 1.0 для всех текселей в исходных данных.

Для блоков BC7 с объединенными компонентами цвета и альфа-компонентами блок состоит из битов режима, сжатых конечных точек, сжатых индексов, необязательных битов раздела и P-бита. В этих блоках цвета конечной точки выражаются в формате RGBA, а значения альфа-компонента интерполируются вместе со значениями цветового компонента.

Для блоков BC7 с отдельными компонентами цвета и альфа-компонентами блок состоит из битов режима, битов поворота, сжатых конечных точек, сжатых индексов и необязательного бита средства выбора индексов. Эти блоки имеют эффективный вектор \[ R, G, B \] и скалярный альфа \[ -канал в \] отдельном формате.

В следующей таблице перечислены компоненты каждого типа блоков.



| Блок BC7 содержит...     | биты режима | биты поворота | бит средства выбора индекса | биты разделов | сжатые конечные точки | P-бит    | сжатые индексы |
|---------------------------|-----------|---------------|--------------------|----------------|----------------------|----------|--------------------|
| только компоненты цвета     | обязательно  | Недоступно           | Недоступно                | обязательно       | обязательно             | необязательно | обязательно           |
| сочетание цвет + альфа    | обязательно  | Недоступно           | Недоступно                | необязательно       | обязательно             | необязательно | обязательно           |
| цвета и альфа по отдельности | обязательно  | обязательно      | необязательно           | Недоступно            | обязательно             | Недоступно      | обязательно           |



 

BC7 определяет палитру цветов по примерной линии между двумя конечными точками. Значение режима определяет количество интерполируемых пар конечных точек на блок. BC7 сохраняет один индекс палитры на тексель.

Для каждого подмножества индексов, соответствующего паре конечных точек, кодировщик фиксирует состояние одного бита сжатых данных индекса для этого подмножества. Для этого выбирается такой порядок конечных точек, который позволяет индексу так называемого назначенного индекса "исправления" задать свой самый значимый бит равным 0, и который затем можно удалить, оставив один бит на подмножество. Для режимов блоков с одним подмножеством индекс исправления — это всегда нулевой индекс.

## <a name="decoding-the-bc7-format"></a>Декодирование формата BC7

В псевдокоде ниже показаны действия по распаковке пикселя в точке (x,y) при наличии 16-байтового блока BC7

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

В следующем псевдокоде показаны шаги, которые позволят полностью декодировать компоненты цвета и альфа-компоненты конечной точки для каждого подмножества с 16-байтовым блоком BC7.

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

Для создания каждого интерполированного компонента для каждого подмножества используйте следующий алгоритм: пусть c — это создаваемый компонент, e0 — это компонент конечной точки 0 подмножества, а e1 — это компонент конечной точки 1 подмножества.

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

В следующем псевдокоде показано извлечение индексов и число битов для компонентов цвета и альфа-компонентов. Блоки с отдельными компонентами цвета и альфа-компонентами также имеют два набора данных индекса: один — для векторного канала, другой — для скалярного. Для режима 4 эти индексы имеют разную ширину (2 или 3 бита), и также имеется однобитовое средство выбора, указывающее, используют ли векторные или скалярные данные 3-битовые индексы. (Извлечение количества альфа-битов аналогично извлечению количества цветовых битов, однако с обратным поведением в бите **idxMode**.)

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

## <a name="related-topics"></a>См. также

<dl> <dt>

[Сжатие блоков текстуры в Direct3D 11](texture-block-compression-in-direct3d-11.md)
</dt> </dl>

 

 