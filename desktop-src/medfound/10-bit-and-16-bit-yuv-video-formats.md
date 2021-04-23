---
description: В этом разделе описываются 10-и 16-разрядные форматы YUV, Рекомендуемые для записи, обработки и отображения видео в операционной системе Microsoft Windows.
ms.assetid: fcaaaa6f-f886-4f6e-9c3c-e513ccc90d37
title: 10-битные и 16-битные видеоформаты YUV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bbc357653848cd51ce6f56ebd8a1da3e5f60403
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145616"
---
# <a name="10-bit-and-16-bit-yuv-video-formats"></a><span data-ttu-id="dd570-103">10-битные и 16-битные видеоформаты YUV</span><span class="sxs-lookup"><span data-stu-id="dd570-103">10-bit and 16-bit YUV Video Formats</span></span>

<span data-ttu-id="dd570-104">В этом разделе описываются 10-и 16-разрядные форматы YUV, Рекомендуемые для записи, обработки и отображения видео в операционной системе Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="dd570-104">This topic describes the 10- and 16-bit YUV formats that are recommended for capturing, processing, and displaying video in the Microsoft Windows operating system.</span></span>

<span data-ttu-id="dd570-105">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="dd570-105">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="dd570-106">Обзор</span><span class="sxs-lookup"><span data-stu-id="dd570-106">Overview</span></span>](#overview)
-   [<span data-ttu-id="dd570-107">Коды FOURCC для 10-и 16-разрядных YUV</span><span class="sxs-lookup"><span data-stu-id="dd570-107">FOURCC Codes For 10-Bit and 16-Bit YUV</span></span>](#fourcc-codes-for-10-bit-and-16-bit-yuv)
-   [<span data-ttu-id="dd570-108">Определения Surface</span><span class="sxs-lookup"><span data-stu-id="dd570-108">Surface Definitions</span></span>](#surface-definitions)
    -   [<span data-ttu-id="dd570-109">форматы 4:2:0</span><span class="sxs-lookup"><span data-stu-id="dd570-109">4:2:0 Formats</span></span>](#420-formats)
    -   [<span data-ttu-id="dd570-110">форматы 4:2:2</span><span class="sxs-lookup"><span data-stu-id="dd570-110">4:2:2 Formats</span></span>](#422-formats)
    -   [<span data-ttu-id="dd570-111">форматы 4:4:4</span><span class="sxs-lookup"><span data-stu-id="dd570-111">4:4:4 Formats</span></span>](#444-formats)
-   [<span data-ttu-id="dd570-112">Предпочтительные форматы YUV</span><span class="sxs-lookup"><span data-stu-id="dd570-112">Preferred YUV Formats</span></span>](#preferred-yuv-formats)
-   [<span data-ttu-id="dd570-113">См. также</span><span class="sxs-lookup"><span data-stu-id="dd570-113">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="dd570-114">Обзор</span><span class="sxs-lookup"><span data-stu-id="dd570-114">Overview</span></span>

<span data-ttu-id="dd570-115">В этих форматах используется представление с фиксированной запятой как для канала яркости, так и для каналов чрома (К'б и К'р).</span><span class="sxs-lookup"><span data-stu-id="dd570-115">These formats use a fixed-point representation for both the luma channel and the chroma (C'b and C'r) channels.</span></span> <span data-ttu-id="dd570-116">Примерами значений являются масштабируемые 8-разрядные значения с коэффициентом масштабирования 2 ^ (n − 8), где n — 10 или 16, в соответствии с разделами 7.7-7,8 и 7.11-7.12 SMPTE 274M.</span><span class="sxs-lookup"><span data-stu-id="dd570-116">Sample values are scaled 8-bit values, using a scaling factor of 2^(n − 8), where n is either 10 or 16, as per sections 7.7-7.8 and 7.11-7.12 of SMPTE 274M.</span></span> <span data-ttu-id="dd570-117">Преобразование точности можно выполнить с помощью простых сдвигов битов.</span><span class="sxs-lookup"><span data-stu-id="dd570-117">Precision conversions can be performed using simple bit shifts.</span></span> <span data-ttu-id="dd570-118">Например, если белая точка 8-разрядного формата — 235, соответствующий 10-разрядный формат имеет белую точку в 940 (235 × 4).</span><span class="sxs-lookup"><span data-stu-id="dd570-118">For example, if the white point of an 8-bit format is 235, the corresponding 10-bit format has a white point at 940 (235 × 4).</span></span>

<span data-ttu-id="dd570-119">В 16-разрядных представлениях, описанных здесь, используются значения **слов** с прямым порядком байтов для каждого канала.</span><span class="sxs-lookup"><span data-stu-id="dd570-119">The 16-bit representations described here use little-endian **WORD** values for each channel.</span></span> <span data-ttu-id="dd570-120">10-битные форматы также используют 16 бит для каждого канала, при этом младшие 6 бит устанавливаются в ноль, как показано на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="dd570-120">The 10-bit formats also use 16 bits for each channel, with the lowest 6 bits set to zero, as shown in the following diagram.</span></span>

![Схема, показывающая 10-разрядное представление](images/ee3aae23-4f0a-47d0-a46c-f3d7d94205e6.gif)

<span data-ttu-id="dd570-122">Поскольку 10-разрядные и 16-разрядные представления одного и того же формата YUV имеют одинаковый макет памяти, можно привести к преобразованию 10-разрядного представления в 16-представление без потери точности.</span><span class="sxs-lookup"><span data-stu-id="dd570-122">Because the 10-bit and 16-bit representations of the same YUV format have the same memory layout, it is possible to cast a 10-bit representation to a 16-representation with no loss of precision.</span></span> <span data-ttu-id="dd570-123">Можно также привести 16-разрядное представление к 10-разрядному представлению.</span><span class="sxs-lookup"><span data-stu-id="dd570-123">It is also possible to cast a 16-bit representation down to a 10-bit representation.</span></span> <span data-ttu-id="dd570-124">(Форматы Y416 и Y410 являются исключением из этого общего правила, так как они не имеют общего макета памяти.)</span><span class="sxs-lookup"><span data-stu-id="dd570-124">(The Y416 and Y410 formats are an exception to this general rule, however, because they do not share the same memory layout.)</span></span>

<span data-ttu-id="dd570-125">Когда графическое оборудование считывает поверхность, содержащую 10-битное представление, она должна игнорировать 6 младших битов каждого канала.</span><span class="sxs-lookup"><span data-stu-id="dd570-125">When the graphics hardware reads a surface that contains a 10-bit representation, it should ignore the low-order 6 bits of each channel.</span></span> <span data-ttu-id="dd570-126">Однако если поверхность содержит допустимые 16-разрядные данные, ее необходимо определить как 16-разрядную поверхность.</span><span class="sxs-lookup"><span data-stu-id="dd570-126">If a surface contains valid 16-bit data, however, it should be identified as a 16-bit surface.</span></span>

<span data-ttu-id="dd570-127">В форматах, содержащих альфа-канал, полностью прозрачная точка имеет альфа-значение 0, а полностью непрозрачный пиксель имеет значение альфа (2 ^ n) – 1, где n — число альфа-битов.</span><span class="sxs-lookup"><span data-stu-id="dd570-127">In the formats that contain alpha, a completely transparent pixel has an alpha value of zero, and a completely opaque pixel has an alpha value of (2^n) – 1, where n is the number of alpha bits.</span></span> <span data-ttu-id="dd570-128">Предполагается, что альфа-канал является линейным значением, которое применяется к каждому компоненту после того, как компонент был преобразован в нормализованную линейную форму.</span><span class="sxs-lookup"><span data-stu-id="dd570-128">Alpha is assumed to be a linear value that is applied to each component after the component has been converted into its normalized linear form.</span></span>

<span data-ttu-id="dd570-129">Для изображений в видеопамяти драйвер графики выбирает выравнивание памяти для поверхности.</span><span class="sxs-lookup"><span data-stu-id="dd570-129">For images in video memory, the graphics driver selects the memory alignment of the surface.</span></span> <span data-ttu-id="dd570-130">Поверхность должна быть совмещена с **параметром DWORD** .</span><span class="sxs-lookup"><span data-stu-id="dd570-130">The surface must be **DWORD** aligned.</span></span> <span data-ttu-id="dd570-131">Это значит, что отдельные строки внутри поверхности гарантированно начинаются с 32-разрядной границы, хотя выравнивание может быть больше 32 бит.</span><span class="sxs-lookup"><span data-stu-id="dd570-131">That is, individual lines within a surface are guaranteed to start at a 32-bit boundary, although the alignment can be larger than 32 bits.</span></span> <span data-ttu-id="dd570-132">Источник (0, 0) всегда находится в левом верхнем углу поверхности.</span><span class="sxs-lookup"><span data-stu-id="dd570-132">The origin (0,0) is always the upper-left corner of the surface.</span></span>

<span data-ttu-id="dd570-133">В рамках этой документации термин *U* эквивалентен *CB*, а термин *V* эквивалентен *CR*.</span><span class="sxs-lookup"><span data-stu-id="dd570-133">For the purposes of this documentation, the term *U* is equivalent to *Cb*, and the term *V* is equivalent to *Cr*.</span></span>

## <a name="fourcc-codes-for-10-bit-and-16-bit-yuv"></a><span data-ttu-id="dd570-134">Коды FOURCC для 10-и 16-разрядных YUV</span><span class="sxs-lookup"><span data-stu-id="dd570-134">FOURCC Codes For 10-Bit and 16-Bit YUV</span></span>

<span data-ttu-id="dd570-135">Коды FOURCC для форматов, описанных здесь, используют следующее соглашение:</span><span class="sxs-lookup"><span data-stu-id="dd570-135">The FOURCC codes for the formats described here use the following convention:</span></span>

-   <span data-ttu-id="dd570-136">Если используется формат "плоский", первым символом в коде FOURCC будет "P".</span><span class="sxs-lookup"><span data-stu-id="dd570-136">If the format is planar, the first character in the FOURCC code is 'P'.</span></span> <span data-ttu-id="dd570-137">Если формат упакован, первый символ — Y.</span><span class="sxs-lookup"><span data-stu-id="dd570-137">If the format is packed, the first character is 'Y'.</span></span>
-   <span data-ttu-id="dd570-138">Второй символ в коде FOURCC определяется выборкой чрома, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="dd570-138">The second character in the FOURCC code is determined by the chroma sampling, as shown in the following table.</span></span>

    

    | <span data-ttu-id="dd570-139">Выборка чрома</span><span class="sxs-lookup"><span data-stu-id="dd570-139">Chroma sampling</span></span> | <span data-ttu-id="dd570-140">Буква кода FOURCC</span><span class="sxs-lookup"><span data-stu-id="dd570-140">FOURCC code letter</span></span> |
    |-----------------|--------------------|
    | <span data-ttu-id="dd570-141">4:4:4</span><span class="sxs-lookup"><span data-stu-id="dd570-141">4:4:4</span></span>           | <span data-ttu-id="dd570-142">четырех</span><span class="sxs-lookup"><span data-stu-id="dd570-142">'4'</span></span>                |
    | <span data-ttu-id="dd570-143">4:2:2</span><span class="sxs-lookup"><span data-stu-id="dd570-143">4:2:2</span></span>           | <span data-ttu-id="dd570-144">открыт</span><span class="sxs-lookup"><span data-stu-id="dd570-144">'2'</span></span>                |
    | <span data-ttu-id="dd570-145">4:2:1</span><span class="sxs-lookup"><span data-stu-id="dd570-145">4:2:1</span></span>           | <span data-ttu-id="dd570-146">1</span><span class="sxs-lookup"><span data-stu-id="dd570-146">'1'</span></span>                |
    | <span data-ttu-id="dd570-147">4:2:0</span><span class="sxs-lookup"><span data-stu-id="dd570-147">4:2:0</span></span>           | <span data-ttu-id="dd570-148">"0"</span><span class="sxs-lookup"><span data-stu-id="dd570-148">'0'</span></span>                |

    

     

-   <span data-ttu-id="dd570-149">Последние два символа в FOURCC указывают количество бит на канал, либо "16" для 16 бит, либо "10" для 10 бит.</span><span class="sxs-lookup"><span data-stu-id="dd570-149">The final two characters in the FOURCC indicate the number of bits per channel, either '16' for 16 bits or '10' for 10 bits.</span></span>

<span data-ttu-id="dd570-150">При использовании этой схемы были определены следующие коды FOURCC.</span><span class="sxs-lookup"><span data-stu-id="dd570-150">Using this scheme, the following FOURCC codes have been defined.</span></span> <span data-ttu-id="dd570-151">В настоящее время не определены форматы 4:2:1 для 10-разрядных или 16-разрядных YUV.</span><span class="sxs-lookup"><span data-stu-id="dd570-151">No 4:2:1 formats for 10-bit or 16-bit YUV have been defined at this time.</span></span>



| <span data-ttu-id="dd570-152">FOURCC</span><span class="sxs-lookup"><span data-stu-id="dd570-152">FOURCC</span></span> | <span data-ttu-id="dd570-153">Описание</span><span class="sxs-lookup"><span data-stu-id="dd570-153">Description</span></span>            |
|--------|------------------------|
| <span data-ttu-id="dd570-154">P016</span><span class="sxs-lookup"><span data-stu-id="dd570-154">P016</span></span>   | <span data-ttu-id="dd570-155">Плоская, 4:2:0, 16-разрядная.</span><span class="sxs-lookup"><span data-stu-id="dd570-155">Planar, 4:2:0, 16-bit.</span></span> |
| <span data-ttu-id="dd570-156">P010</span><span class="sxs-lookup"><span data-stu-id="dd570-156">P010</span></span>   | <span data-ttu-id="dd570-157">Плоская, 4:2:0, 10-разрядная.</span><span class="sxs-lookup"><span data-stu-id="dd570-157">Planar, 4:2:0, 10-bit.</span></span> |
| <span data-ttu-id="dd570-158">P216</span><span class="sxs-lookup"><span data-stu-id="dd570-158">P216</span></span>   | <span data-ttu-id="dd570-159">Плоская, 4:2:2, 16-разрядная.</span><span class="sxs-lookup"><span data-stu-id="dd570-159">Planar, 4:2:2, 16-bit.</span></span> |
| <span data-ttu-id="dd570-160">P210</span><span class="sxs-lookup"><span data-stu-id="dd570-160">P210</span></span>   | <span data-ttu-id="dd570-161">Плоская, 4:2:2, 10-разрядная.</span><span class="sxs-lookup"><span data-stu-id="dd570-161">Planar, 4:2:2, 10-bit.</span></span> |
| <span data-ttu-id="dd570-162">Y216</span><span class="sxs-lookup"><span data-stu-id="dd570-162">Y216</span></span>   | <span data-ttu-id="dd570-163">Упакованный, 4:2:2, 16-разрядный.</span><span class="sxs-lookup"><span data-stu-id="dd570-163">Packed, 4:2:2, 16-bit.</span></span> |
| <span data-ttu-id="dd570-164">Y210</span><span class="sxs-lookup"><span data-stu-id="dd570-164">Y210</span></span>   | <span data-ttu-id="dd570-165">Упакованный, 4:2:2, 10-разрядный.</span><span class="sxs-lookup"><span data-stu-id="dd570-165">Packed, 4:2:2, 10-bit.</span></span> |
| <span data-ttu-id="dd570-166">Y416</span><span class="sxs-lookup"><span data-stu-id="dd570-166">Y416</span></span>   | <span data-ttu-id="dd570-167">Упакованный, 4:4:4, 16-разрядный</span><span class="sxs-lookup"><span data-stu-id="dd570-167">Packed, 4:4:4, 16-bit</span></span>  |
| <span data-ttu-id="dd570-168">Y410</span><span class="sxs-lookup"><span data-stu-id="dd570-168">Y410</span></span>   | <span data-ttu-id="dd570-169">Упакованный, 4:4:4, 10-разрядный.</span><span class="sxs-lookup"><span data-stu-id="dd570-169">Packed, 4:4:4, 10-bit.</span></span> |



 

<span data-ttu-id="dd570-170">Идентификаторы GUID подтипа также определены из этих Фаурккс; см. раздел [GUID подтипа видео](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="dd570-170">Subtype GUIDs have also been defined from these FOURCCs; see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="surface-definitions"></a><span data-ttu-id="dd570-171">Определения Surface</span><span class="sxs-lookup"><span data-stu-id="dd570-171">Surface Definitions</span></span>

<span data-ttu-id="dd570-172">В этом разделе описывается структура памяти для каждого формата.</span><span class="sxs-lookup"><span data-stu-id="dd570-172">This section describes the memory layout of each format.</span></span> <span data-ttu-id="dd570-173">В приведенных ниже описаниях термин **слово** ссылается на 16-битное значение с прямым порядком байтов, а термин **DWORD** — на 32-разрядное значение с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="dd570-173">In the descriptions that follow, the term **WORD** refers to a little-endian 16-bit value, and the term **DWORD** refers to a little-endian 32-bit value.</span></span>

### <a name="420-formats"></a><span data-ttu-id="dd570-174">форматы 4:2:0</span><span class="sxs-lookup"><span data-stu-id="dd570-174">4:2:0 Formats</span></span>

<span data-ttu-id="dd570-175">Определены два формата 4:2:0 с кодами FOURCC P016 и P010.</span><span class="sxs-lookup"><span data-stu-id="dd570-175">Two 4:2:0 formats are defined, with the FOURCC codes P016 and P010.</span></span> <span data-ttu-id="dd570-176">Они используют один и тот же макет памяти, но P016 использует 16 бит на канал, а P010 использует 10 бит на канал.</span><span class="sxs-lookup"><span data-stu-id="dd570-176">They share the same memory layout, but P016 uses 16 bits per channel and P010 uses 10 bits per channel.</span></span>

### <a name="p016-and-p010"></a><span data-ttu-id="dd570-177">P016 и P010</span><span class="sxs-lookup"><span data-stu-id="dd570-177">P016 and P010</span></span>

<span data-ttu-id="dd570-178">В этих двух форматах все примеры Y отображаются первыми в памяти как массив **слов** s с четным числом строк.</span><span class="sxs-lookup"><span data-stu-id="dd570-178">In these two formats, all Y samples appear first in memory as an array of **WORD** s with an even number of lines.</span></span> <span data-ttu-id="dd570-179">Шаг поверхности может быть больше, чем ширина плоскости Y.</span><span class="sxs-lookup"><span data-stu-id="dd570-179">The surface stride can be larger than the width of the Y plane.</span></span> <span data-ttu-id="dd570-180">За этим массивом следует сразу массив **слов** s, содержащий чередующиеся примеры и V, как показано на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="dd570-180">This array is followed immediately by an array of **WORD** s that contains interleaved U and V samples, as shown in the following diagram.</span></span>

![Схема, демонстрирующая макет p016 и P010 пикселей](images/1e1c4d66-6172-4d3a-bd25-4b5caa67edcd.gif)

<span data-ttu-id="dd570-182">Если комбинированный массив U-V адресован как массив **DWORD**, наименее важное слово (ЛСВ) содержит значение U, а наиболее значимое слово (МСВ) содержит значение V.</span><span class="sxs-lookup"><span data-stu-id="dd570-182">If the combined U-V array is addressed as an array of **DWORD** s, the least significant word (LSW) contains the U value and the most significant word (MSW) contains the V value.</span></span> <span data-ttu-id="dd570-183">Шаг комбинированной плоскости U-V равен значению шага плоскости Y.</span><span class="sxs-lookup"><span data-stu-id="dd570-183">The stride of the combined U-V plane is equal to the stride of the Y plane.</span></span> <span data-ttu-id="dd570-184">Плоскость U-V имеет половину столько линий, сколько в плоскости Y.</span><span class="sxs-lookup"><span data-stu-id="dd570-184">The U-V plane has half as many lines as the Y plane.</span></span>

<span data-ttu-id="dd570-185">Эти два формата являются предпочтительными 4:2:0 форматами плоских пикселей для представлений YUV с более высокой точностью.</span><span class="sxs-lookup"><span data-stu-id="dd570-185">These two formats are the preferred 4:2:0 planar pixel formats for higher precision YUV representations.</span></span> <span data-ttu-id="dd570-186">Они должны быть промежуточным требованием для ускорителей DirectX Video Acceleration (ДКСВА), поддерживающих 10-разрядное или 16-разрядное видео 4:2:0.</span><span class="sxs-lookup"><span data-stu-id="dd570-186">They are expected to be an intermediate-term requirement for DirectX Video Acceleration (DXVA) accelerators that support 10-bit or 16-bit 4:2:0 video.</span></span>

### <a name="422-formats"></a><span data-ttu-id="dd570-187">форматы 4:2:2</span><span class="sxs-lookup"><span data-stu-id="dd570-187">4:2:2 Formats</span></span>

<span data-ttu-id="dd570-188">Определены четыре формата 4:2:2, два плоских и двух упакованных.</span><span class="sxs-lookup"><span data-stu-id="dd570-188">Four 4:2:2 formats are defined, two planar and two packed.</span></span> <span data-ttu-id="dd570-189">У них есть следующие коды FOURCC:</span><span class="sxs-lookup"><span data-stu-id="dd570-189">They have the following FOURCC codes:</span></span>

-   <span data-ttu-id="dd570-190">P216</span><span class="sxs-lookup"><span data-stu-id="dd570-190">P216</span></span>
-   <span data-ttu-id="dd570-191">P210</span><span class="sxs-lookup"><span data-stu-id="dd570-191">P210</span></span>
-   <span data-ttu-id="dd570-192">Y216</span><span class="sxs-lookup"><span data-stu-id="dd570-192">Y216</span></span>
-   <span data-ttu-id="dd570-193">Y210</span><span class="sxs-lookup"><span data-stu-id="dd570-193">Y210</span></span>

### <a name="p216-and-p210"></a><span data-ttu-id="dd570-194">P216 и P210</span><span class="sxs-lookup"><span data-stu-id="dd570-194">P216 and P210</span></span>

<span data-ttu-id="dd570-195">В этих двух плоских форматах все примеры Y отображаются первыми в памяти как массив **слов** s с четным числом строк.</span><span class="sxs-lookup"><span data-stu-id="dd570-195">In these two planar formats, all Y samples appear first in memory as an array of **WORD** s with an even number of lines.</span></span> <span data-ttu-id="dd570-196">Шаг поверхности может быть больше, чем ширина плоскости Y.</span><span class="sxs-lookup"><span data-stu-id="dd570-196">The surface stride can be larger than the width of the Y plane.</span></span> <span data-ttu-id="dd570-197">За этим массивом следует сразу массив **слов** s, содержащий чередующиеся примеры и V, как показано на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="dd570-197">This array is followed immediately by an array of **WORD** s that contains interleaved U and V samples, as shown in the following diagram.</span></span>

![Схема, демонстрирующая макет p216 и P210 пикселей](images/ff672fef-218f-4722-b806-d06c77fe8cfa.gif)

<span data-ttu-id="dd570-199">Если объединенный массив U-V адресован как массив **DWORD**, ЛСВ содержит значение U, а МСВ содержит значение V.</span><span class="sxs-lookup"><span data-stu-id="dd570-199">If the combined U-V array is addressed as an array of **DWORD** s, the LSW contains the U value and the MSW contains the V value.</span></span> <span data-ttu-id="dd570-200">Шаг комбинированной плоскости U-V равен значению шага плоскости Y.</span><span class="sxs-lookup"><span data-stu-id="dd570-200">The stride of the combined U-V plane is equal to the stride of the Y plane.</span></span> <span data-ttu-id="dd570-201">Плоскость U-V имеет то же количество линий, что и плоскость Y.</span><span class="sxs-lookup"><span data-stu-id="dd570-201">The U-V plane has the same number of lines as the Y plane.</span></span>

<span data-ttu-id="dd570-202">Эти два формата являются предпочтительными 4:2:2 форматами плоских пикселей для представлений YUV с более высокой точностью.</span><span class="sxs-lookup"><span data-stu-id="dd570-202">These two formats are the preferred 4:2:2 planar pixel formats for higher precision YUV representations.</span></span> <span data-ttu-id="dd570-203">Они должны быть промежуточным требованием для ускорителей DirectX Video Acceleration (ДКСВА), поддерживающих 10-разрядное или 16-разрядное видео 4:2:2.</span><span class="sxs-lookup"><span data-stu-id="dd570-203">They are expected to be an intermediate-term requirement for DirectX Video Acceleration (DXVA) accelerators that support 10-bit or 16-bit 4:2:2 video.</span></span>

### <a name="y216-and-y210"></a><span data-ttu-id="dd570-204">Y216 и Y210</span><span class="sxs-lookup"><span data-stu-id="dd570-204">Y216 and Y210</span></span>

<span data-ttu-id="dd570-205">В этих двух упакованных форматах каждая пара пикселей хранится в виде массива из четырех **слов** s, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="dd570-205">In these two packed formats, each pair of pixels is stored as an array of four **WORD** s, as shown in the following illustration.</span></span>

![Схема, показывающая макет пикселей y216 и Y210.](images/6f68aeeb-18ca-48ee-82c4-5b79d5510e9f.gif)

<span data-ttu-id="dd570-207">Первое **слово** в массиве содержит первый пример y в паре, второе **слово** содержит пример U, третье **слово** содержит второй пример y, а четвертое **слово** содержит образец V.</span><span class="sxs-lookup"><span data-stu-id="dd570-207">The first **WORD** in the array contains the first Y sample in the pair, the second **WORD** contains the U sample, the third **WORD** contains the second Y sample, and the fourth **WORD** contains the V sample.</span></span>

<span data-ttu-id="dd570-208">Y210 идентичен Y216, за исключением того, что каждый пример содержит только 10 бит значимых данных.</span><span class="sxs-lookup"><span data-stu-id="dd570-208">Y210 is identical to Y216 except that each sample contains only 10 bits of significant data.</span></span> <span data-ttu-id="dd570-209">Минимальное количество значащих 6 бит равно нулю, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="dd570-209">The least significant 6 bits are set to zero, as described previously.</span></span>

### <a name="444-formats"></a><span data-ttu-id="dd570-210">форматы 4:4:4</span><span class="sxs-lookup"><span data-stu-id="dd570-210">4:4:4 Formats</span></span>

<span data-ttu-id="dd570-211">Определены два формата 4:4:4 с кодами FOURCC Y410 и Y416.</span><span class="sxs-lookup"><span data-stu-id="dd570-211">Two 4:4:4 formats are defined, with the FOURCC codes Y410 and Y416.</span></span> <span data-ttu-id="dd570-212">Оба являются упакованными форматами.</span><span class="sxs-lookup"><span data-stu-id="dd570-212">Both are packed formats.</span></span>

### <a name="y410"></a><span data-ttu-id="dd570-213">Y410</span><span class="sxs-lookup"><span data-stu-id="dd570-213">Y410</span></span>

<span data-ttu-id="dd570-214">Этот формат представляет собой упакованное 10-разрядное представление, включающее 2 бита альфа-канала.</span><span class="sxs-lookup"><span data-stu-id="dd570-214">This format is a packed 10-bit representation that includes 2 bits of alpha.</span></span> <span data-ttu-id="dd570-215">Каждый пиксель кодируется как одиночный **DWORD** с макетом памяти, показанным на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="dd570-215">Each pixel is encoded as a single **DWORD** with the memory layout shown in the following diagram.</span></span>

![Диаграмма, демонстрирующая макет y410 пикселей.](images/f8a71437-e3f1-4331-be30-f766c028d648.gif)

<span data-ttu-id="dd570-217">Биты 0-9 содержат пример U, биты 10-19 содержат пример Y, биты 20-29 содержат пример V, а BITS 30-31 содержат альфа-значение.</span><span class="sxs-lookup"><span data-stu-id="dd570-217">Bits 0-9 contain the U sample, bits 10-19 contain the Y sample, bits 20-29 contain the V sample, and bits 30-31 contain the alpha value.</span></span> <span data-ttu-id="dd570-218">Чтобы указать, что пиксель полностью непрозрачен, приложение должно установить два альфа-бита равными 0x03.</span><span class="sxs-lookup"><span data-stu-id="dd570-218">To indicate that a pixel is fully opaque, an application must set the two alpha bits equal to 0x03.</span></span>

### <a name="y416"></a><span data-ttu-id="dd570-219">Y416</span><span class="sxs-lookup"><span data-stu-id="dd570-219">Y416</span></span>

<span data-ttu-id="dd570-220">Этот формат представляет собой упакованное 16-разрядное представление, включающее 16 бит альфа-канала.</span><span class="sxs-lookup"><span data-stu-id="dd570-220">This format is a packed 16-bit representation that includes 16 bits of alpha.</span></span> <span data-ttu-id="dd570-221">Каждый пиксель кодируется в виде пары **DWORD** s, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="dd570-221">Each pixel is encoded as a pair of **DWORD** s, as shown in the following illustration.</span></span>

![Диаграмма, демонстрирующая макет y416 пикселей.](images/c928523a-25d3-4712-9aec-5b492b51435f.gif)

<span data-ttu-id="dd570-223">Биты 0-15 содержат пример U, биты 16-31 содержат пример Y, биты 32-47 содержат пример V, а BITS 48-63 содержат альфа-значение.</span><span class="sxs-lookup"><span data-stu-id="dd570-223">Bits 0-15 contain the U sample, bits 16-31 contain the Y sample, bits 32-47 contain the V sample, and bits 48-63 contain the alpha value.</span></span>

<span data-ttu-id="dd570-224">Чтобы указать, что пиксель полностью непрозрачен, приложение должно установить два альфа-бита равными 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="dd570-224">To indicate that a pixel is fully opaque, an application must set the two alpha bits equal to 0xFFFF.</span></span> <span data-ttu-id="dd570-225">Этот формат предназначен главным образом в качестве промежуточного формата во время обработки образа во избежание накопления ошибок.</span><span class="sxs-lookup"><span data-stu-id="dd570-225">This format is intended primarily as an intermediate format during image processing to avoid the accumulation of errors.</span></span>

## <a name="preferred-yuv-formats"></a><span data-ttu-id="dd570-226">Предпочтительные форматы YUV</span><span class="sxs-lookup"><span data-stu-id="dd570-226">Preferred YUV Formats</span></span>

<span data-ttu-id="dd570-227">В следующей таблице перечислены Предпочтительные форматы YUV, включая 8-разрядные форматы.</span><span class="sxs-lookup"><span data-stu-id="dd570-227">The following table lists the preferred YUV formats, including 8-bit formats.</span></span>



| <span data-ttu-id="dd570-228">Формат</span><span class="sxs-lookup"><span data-stu-id="dd570-228">Format</span></span> | <span data-ttu-id="dd570-229">Выборка чрома</span><span class="sxs-lookup"><span data-stu-id="dd570-229">Chroma sampling</span></span> | <span data-ttu-id="dd570-230">Упакованная или плоская</span><span class="sxs-lookup"><span data-stu-id="dd570-230">Packed or planar</span></span> | <span data-ttu-id="dd570-231">Бит на канал</span><span class="sxs-lookup"><span data-stu-id="dd570-231">Bits per channel</span></span> |
|--------|-----------------|------------------|------------------|
| <span data-ttu-id="dd570-232">айув</span><span class="sxs-lookup"><span data-stu-id="dd570-232">AYUV</span></span>   | <span data-ttu-id="dd570-233">4:4:4</span><span class="sxs-lookup"><span data-stu-id="dd570-233">4:4:4</span></span>           | <span data-ttu-id="dd570-234">Распаковывается</span><span class="sxs-lookup"><span data-stu-id="dd570-234">Packed</span></span>           | <span data-ttu-id="dd570-235">8</span><span class="sxs-lookup"><span data-stu-id="dd570-235">8</span></span>                |
| <span data-ttu-id="dd570-236">Y410</span><span class="sxs-lookup"><span data-stu-id="dd570-236">Y410</span></span>   | <span data-ttu-id="dd570-237">4:4:4</span><span class="sxs-lookup"><span data-stu-id="dd570-237">4:4:4</span></span>           | <span data-ttu-id="dd570-238">Распаковывается</span><span class="sxs-lookup"><span data-stu-id="dd570-238">Packed</span></span>           | <span data-ttu-id="dd570-239">10</span><span class="sxs-lookup"><span data-stu-id="dd570-239">10</span></span>               |
| <span data-ttu-id="dd570-240">Y416</span><span class="sxs-lookup"><span data-stu-id="dd570-240">Y416</span></span>   | <span data-ttu-id="dd570-241">4:4:4</span><span class="sxs-lookup"><span data-stu-id="dd570-241">4:4:4</span></span>           | <span data-ttu-id="dd570-242">Распаковывается</span><span class="sxs-lookup"><span data-stu-id="dd570-242">Packed</span></span>           | <span data-ttu-id="dd570-243">16</span><span class="sxs-lookup"><span data-stu-id="dd570-243">16</span></span>               |
| <span data-ttu-id="dd570-244">AI44</span><span class="sxs-lookup"><span data-stu-id="dd570-244">AI44</span></span>   | <span data-ttu-id="dd570-245">4:4:4</span><span class="sxs-lookup"><span data-stu-id="dd570-245">4:4:4</span></span>           | <span data-ttu-id="dd570-246">Распаковывается</span><span class="sxs-lookup"><span data-stu-id="dd570-246">Packed</span></span>           | <span data-ttu-id="dd570-247">палеттизед</span><span class="sxs-lookup"><span data-stu-id="dd570-247">Palettized</span></span>       |
| <span data-ttu-id="dd570-248">YUY2</span><span class="sxs-lookup"><span data-stu-id="dd570-248">YUY2</span></span>   | <span data-ttu-id="dd570-249">4:2:2</span><span class="sxs-lookup"><span data-stu-id="dd570-249">4:2:2</span></span>           | <span data-ttu-id="dd570-250">Распаковывается</span><span class="sxs-lookup"><span data-stu-id="dd570-250">Packed</span></span>           | <span data-ttu-id="dd570-251">8</span><span class="sxs-lookup"><span data-stu-id="dd570-251">8</span></span>                |
| <span data-ttu-id="dd570-252">Y210</span><span class="sxs-lookup"><span data-stu-id="dd570-252">Y210</span></span>   | <span data-ttu-id="dd570-253">4:2:2</span><span class="sxs-lookup"><span data-stu-id="dd570-253">4:2:2</span></span>           | <span data-ttu-id="dd570-254">Распаковывается</span><span class="sxs-lookup"><span data-stu-id="dd570-254">Packed</span></span>           | <span data-ttu-id="dd570-255">10</span><span class="sxs-lookup"><span data-stu-id="dd570-255">10</span></span>               |
| <span data-ttu-id="dd570-256">Y216</span><span class="sxs-lookup"><span data-stu-id="dd570-256">Y216</span></span>   | <span data-ttu-id="dd570-257">4:2:2</span><span class="sxs-lookup"><span data-stu-id="dd570-257">4:2:2</span></span>           | <span data-ttu-id="dd570-258">Распаковывается</span><span class="sxs-lookup"><span data-stu-id="dd570-258">Packed</span></span>           | <span data-ttu-id="dd570-259">16</span><span class="sxs-lookup"><span data-stu-id="dd570-259">16</span></span>               |
| <span data-ttu-id="dd570-260">P210</span><span class="sxs-lookup"><span data-stu-id="dd570-260">P210</span></span>   | <span data-ttu-id="dd570-261">4:2:2</span><span class="sxs-lookup"><span data-stu-id="dd570-261">4:2:2</span></span>           | <span data-ttu-id="dd570-262">Планарные</span><span class="sxs-lookup"><span data-stu-id="dd570-262">Planar</span></span>           | <span data-ttu-id="dd570-263">10</span><span class="sxs-lookup"><span data-stu-id="dd570-263">10</span></span>               |
| <span data-ttu-id="dd570-264">P216</span><span class="sxs-lookup"><span data-stu-id="dd570-264">P216</span></span>   | <span data-ttu-id="dd570-265">4:2:2</span><span class="sxs-lookup"><span data-stu-id="dd570-265">4:2:2</span></span>           | <span data-ttu-id="dd570-266">Планарные</span><span class="sxs-lookup"><span data-stu-id="dd570-266">Planar</span></span>           | <span data-ttu-id="dd570-267">16</span><span class="sxs-lookup"><span data-stu-id="dd570-267">16</span></span>               |
| <span data-ttu-id="dd570-268">NV12</span><span class="sxs-lookup"><span data-stu-id="dd570-268">NV12</span></span>   | <span data-ttu-id="dd570-269">4:2:0</span><span class="sxs-lookup"><span data-stu-id="dd570-269">4:2:0</span></span>           | <span data-ttu-id="dd570-270">Планарные</span><span class="sxs-lookup"><span data-stu-id="dd570-270">Planar</span></span>           | <span data-ttu-id="dd570-271">8</span><span class="sxs-lookup"><span data-stu-id="dd570-271">8</span></span>                |
| <span data-ttu-id="dd570-272">P010</span><span class="sxs-lookup"><span data-stu-id="dd570-272">P010</span></span>   | <span data-ttu-id="dd570-273">4:2:0</span><span class="sxs-lookup"><span data-stu-id="dd570-273">4:2:0</span></span>           | <span data-ttu-id="dd570-274">Планарные</span><span class="sxs-lookup"><span data-stu-id="dd570-274">Planar</span></span>           | <span data-ttu-id="dd570-275">10</span><span class="sxs-lookup"><span data-stu-id="dd570-275">10</span></span>               |
| <span data-ttu-id="dd570-276">P016</span><span class="sxs-lookup"><span data-stu-id="dd570-276">P016</span></span>   | <span data-ttu-id="dd570-277">4:2:0</span><span class="sxs-lookup"><span data-stu-id="dd570-277">4:2:0</span></span>           | <span data-ttu-id="dd570-278">Планарные</span><span class="sxs-lookup"><span data-stu-id="dd570-278">Planar</span></span>           | <span data-ttu-id="dd570-279">16</span><span class="sxs-lookup"><span data-stu-id="dd570-279">16</span></span>               |
| <span data-ttu-id="dd570-280">NV11</span><span class="sxs-lookup"><span data-stu-id="dd570-280">NV11</span></span>   | <span data-ttu-id="dd570-281">4:1:1</span><span class="sxs-lookup"><span data-stu-id="dd570-281">4:1:1</span></span>           | <span data-ttu-id="dd570-282">Планарные</span><span class="sxs-lookup"><span data-stu-id="dd570-282">Planar</span></span>           | <span data-ttu-id="dd570-283">8</span><span class="sxs-lookup"><span data-stu-id="dd570-283">8</span></span>                |



 

<span data-ttu-id="dd570-284">Если объект поддерживает определенную глубину битов и чрома схему выборки, рекомендуется, чтобы он поддерживал соответствующие форматы YUV, перечисленные в этой таблице.</span><span class="sxs-lookup"><span data-stu-id="dd570-284">It is recommended that if an object supports a given bit depth and chroma sampling scheme, it should support the corresponding YUV formats listed in this table.</span></span> <span data-ttu-id="dd570-285">(Объекты могут поддерживать дополнительные форматы, не указанные здесь.)</span><span class="sxs-lookup"><span data-stu-id="dd570-285">(Objects might support additional formats not listed here.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd570-286">См. также</span><span class="sxs-lookup"><span data-stu-id="dd570-286">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd570-287">Рекомендуемые 8-разрядные форматы YUV для отрисовки видео</span><span class="sxs-lookup"><span data-stu-id="dd570-287">Recommended 8-Bit YUV Formats for Video Rendering</span></span>](recommended-8-bit-yuv-formats-for-video-rendering.md)
</dt> <dt>

[<span data-ttu-id="dd570-288">Идентификаторы GUID для подтипов видео</span><span class="sxs-lookup"><span data-stu-id="dd570-288">Video Subtype GUIDs</span></span>](video-subtype-guids.md)
</dt> <dt>

[<span data-ttu-id="dd570-289">Типы видеоклипов</span><span class="sxs-lookup"><span data-stu-id="dd570-289">Video Media Types</span></span>](video-media-types.md)
</dt> </dl>

 

 



