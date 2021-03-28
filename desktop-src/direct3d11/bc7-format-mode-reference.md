---
title: Справочник по режиму форматирования BC7
description: Эта документация содержит список 8 блочных режимов и битовых выделений для блоков формата сжатия BC7 текстуры.
ms.assetid: B1CEB729-6694-49BF-ACB9-FD1EFAB0B0D1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 719a223e6ac057b949d5e1222582058f637ec526
ms.sourcegitcommit: 62e758931c610782807c7c9fad284921a6c56232
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/22/2020
ms.locfileid: "104412368"
---
# <a name="bc7-format-mode-reference"></a><span data-ttu-id="467d3-103">Справочник по режиму форматирования BC7</span><span class="sxs-lookup"><span data-stu-id="467d3-103">BC7 Format Mode Reference</span></span>

<span data-ttu-id="467d3-104">Эта документация содержит список 8 блочных режимов и битовых выделений для блоков формата сжатия BC7 текстуры.</span><span class="sxs-lookup"><span data-stu-id="467d3-104">This documentation contains a list of the 8 block modes and bit allocations for BC7 texture compression format blocks.</span></span>

<span data-ttu-id="467d3-105">Цвета для каждого подмножества в блоке представляются двумя явно заданными цветами конечных точек и подмножеством интерполированных цветов между ними.</span><span class="sxs-lookup"><span data-stu-id="467d3-105">The colors for each subset within a block are represented by two explicit endpoint colors and a set of interpolated colors between them.</span></span> <span data-ttu-id="467d3-106">В зависимости от точности индекса блока каждое подмножество может иметь 4, 8 или 16 возможных цветов.</span><span class="sxs-lookup"><span data-stu-id="467d3-106">Depending on the block's index precision, each subset can have 4, 8 or 16 possible colors.</span></span>

-   [<span data-ttu-id="467d3-107">Режим 0</span><span class="sxs-lookup"><span data-stu-id="467d3-107">Mode 0</span></span>](#mode-0)
-   [<span data-ttu-id="467d3-108">Режим 1</span><span class="sxs-lookup"><span data-stu-id="467d3-108">Mode 1</span></span>](#mode-1)
-   [<span data-ttu-id="467d3-109">Режим 2</span><span class="sxs-lookup"><span data-stu-id="467d3-109">Mode 2</span></span>](#mode-2)
-   [<span data-ttu-id="467d3-110">Режим 3</span><span class="sxs-lookup"><span data-stu-id="467d3-110">Mode 3</span></span>](#mode-3)
-   [<span data-ttu-id="467d3-111">Режим 4</span><span class="sxs-lookup"><span data-stu-id="467d3-111">Mode 4</span></span>](#mode-4)
-   [<span data-ttu-id="467d3-112">Режим 5</span><span class="sxs-lookup"><span data-stu-id="467d3-112">Mode 5</span></span>](#mode-5)
-   [<span data-ttu-id="467d3-113">Режим 6</span><span class="sxs-lookup"><span data-stu-id="467d3-113">Mode 6</span></span>](#mode-6)
-   [<span data-ttu-id="467d3-114">Режим 7</span><span class="sxs-lookup"><span data-stu-id="467d3-114">Mode 7</span></span>](#mode-7)
-   [<span data-ttu-id="467d3-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="467d3-115">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="467d3-116">См. также</span><span class="sxs-lookup"><span data-stu-id="467d3-116">Related topics</span></span>](#related-topics)

## <a name="mode-0"></a><span data-ttu-id="467d3-117">Режим 0</span><span class="sxs-lookup"><span data-stu-id="467d3-117">Mode 0</span></span>

<span data-ttu-id="467d3-118">Режим BC7 0 имеет следующие характеристики:</span><span class="sxs-lookup"><span data-stu-id="467d3-118">BC7 Mode 0 has the following characteristics:</span></span>

-   <span data-ttu-id="467d3-119">Только компоненты цвета (без альфа)</span><span class="sxs-lookup"><span data-stu-id="467d3-119">Color components only (no alpha)</span></span>
-   <span data-ttu-id="467d3-120">3 подмножества на каждый блок</span><span class="sxs-lookup"><span data-stu-id="467d3-120">3 subsets per block</span></span>
-   <span data-ttu-id="467d3-121">Конечные точки RGBP 4.4.4.1 с уникальным P-битом на конечную точку</span><span class="sxs-lookup"><span data-stu-id="467d3-121">RGBP 4.4.4.1 endpoints with a unique P-bit per endpoint</span></span>
-   <span data-ttu-id="467d3-122">3-битовые индексы</span><span class="sxs-lookup"><span data-stu-id="467d3-122">3-bit indices</span></span>
-   <span data-ttu-id="467d3-123">16 разделов</span><span class="sxs-lookup"><span data-stu-id="467d3-123">16 partitions</span></span>

![структура битов режима 0](images/bc7-mode0.png)

## <a name="mode-1"></a><span data-ttu-id="467d3-125">Режим 1</span><span class="sxs-lookup"><span data-stu-id="467d3-125">Mode 1</span></span>

<span data-ttu-id="467d3-126">Режим BC7 1 имеет следующие характеристики:</span><span class="sxs-lookup"><span data-stu-id="467d3-126">BC7 Mode 1 has the following characteristics:</span></span>

-   <span data-ttu-id="467d3-127">Только компоненты цвета (без альфа)</span><span class="sxs-lookup"><span data-stu-id="467d3-127">Color components only (no alpha)</span></span>
-   <span data-ttu-id="467d3-128">2 подмножества на каждый блок</span><span class="sxs-lookup"><span data-stu-id="467d3-128">2 subsets per block</span></span>
-   <span data-ttu-id="467d3-129">Конечные точки RGBP 6.6.6.1 с общим P-битом на подмножество)</span><span class="sxs-lookup"><span data-stu-id="467d3-129">RGBP 6.6.6.1 endpoints with a shared P-bit per subset)</span></span>
-   <span data-ttu-id="467d3-130">3-битовые индексы</span><span class="sxs-lookup"><span data-stu-id="467d3-130">3-bit indices</span></span>
-   <span data-ttu-id="467d3-131">64 разделов</span><span class="sxs-lookup"><span data-stu-id="467d3-131">64 partitions</span></span>

![структура битов режима 1](images/bc7-mode1.png)

## <a name="mode-2"></a><span data-ttu-id="467d3-133">Режим 2</span><span class="sxs-lookup"><span data-stu-id="467d3-133">Mode 2</span></span>

<span data-ttu-id="467d3-134">Режим BC7 2 имеет следующие характеристики:</span><span class="sxs-lookup"><span data-stu-id="467d3-134">BC7 Mode 2 has the following characteristics:</span></span>

-   <span data-ttu-id="467d3-135">Только компоненты цвета (без альфа)</span><span class="sxs-lookup"><span data-stu-id="467d3-135">Color components only (no alpha)</span></span>
-   <span data-ttu-id="467d3-136">3 подмножества на каждый блок</span><span class="sxs-lookup"><span data-stu-id="467d3-136">3 subsets per block</span></span>
-   <span data-ttu-id="467d3-137">Конечные точки RGB 5.5.5</span><span class="sxs-lookup"><span data-stu-id="467d3-137">RGB 5.5.5 endpoints</span></span>
-   <span data-ttu-id="467d3-138">2-битовые индексы</span><span class="sxs-lookup"><span data-stu-id="467d3-138">2-bit indices</span></span>
-   <span data-ttu-id="467d3-139">64 разделов</span><span class="sxs-lookup"><span data-stu-id="467d3-139">64 partitions</span></span>

![структура битов режима 2](images/bc7-mode2.png)

## <a name="mode-3"></a><span data-ttu-id="467d3-141">Режим 3</span><span class="sxs-lookup"><span data-stu-id="467d3-141">Mode 3</span></span>

<span data-ttu-id="467d3-142">Режим BC7 3 имеет следующие характеристики:</span><span class="sxs-lookup"><span data-stu-id="467d3-142">BC7 Mode 3 has the following characteristics:</span></span>

-   <span data-ttu-id="467d3-143">Только компоненты цвета (без альфа)</span><span class="sxs-lookup"><span data-stu-id="467d3-143">Color components only (no alpha)</span></span>
-   <span data-ttu-id="467d3-144">2 подмножества на каждый блок</span><span class="sxs-lookup"><span data-stu-id="467d3-144">2 subsets per block</span></span>
-   <span data-ttu-id="467d3-145">Конечные точки RGBP 7.7.7.1 с уникальным P-битом на подмножество)</span><span class="sxs-lookup"><span data-stu-id="467d3-145">RGBP 7.7.7.1 endpoints with a unique P-bit per subset)</span></span>
-   <span data-ttu-id="467d3-146">2-битовые индексы</span><span class="sxs-lookup"><span data-stu-id="467d3-146">2-bit indices</span></span>
-   <span data-ttu-id="467d3-147">64 разделов</span><span class="sxs-lookup"><span data-stu-id="467d3-147">64 partitions</span></span>

![структура битов режима 3](images/bc7-mode3.png)

## <a name="mode-4"></a><span data-ttu-id="467d3-149">Режим 4</span><span class="sxs-lookup"><span data-stu-id="467d3-149">Mode 4</span></span>

<span data-ttu-id="467d3-150">Режим BC7 4 имеет следующие характеристики:</span><span class="sxs-lookup"><span data-stu-id="467d3-150">BC7 Mode 4 has the following characteristics:</span></span>

-   <span data-ttu-id="467d3-151">Компоненты цвета с отдельным альфа-компонентом</span><span class="sxs-lookup"><span data-stu-id="467d3-151">Color components with separate alpha component</span></span>
-   <span data-ttu-id="467d3-152">1 подмножество на блок</span><span class="sxs-lookup"><span data-stu-id="467d3-152">1 subset per block</span></span>
-   <span data-ttu-id="467d3-153">Конечные точки цвета RGB 5.5.5</span><span class="sxs-lookup"><span data-stu-id="467d3-153">RGB 5.5.5 color endpoints</span></span>
-   <span data-ttu-id="467d3-154">6-битовые конечные точки альфа</span><span class="sxs-lookup"><span data-stu-id="467d3-154">6-bit alpha endpoints</span></span>
-   <span data-ttu-id="467d3-155">16 x 2-битовых индексов</span><span class="sxs-lookup"><span data-stu-id="467d3-155">16 x 2-bit indices</span></span>
-   <span data-ttu-id="467d3-156">16 x 3-битовых индексов</span><span class="sxs-lookup"><span data-stu-id="467d3-156">16 x 3-bit indices</span></span>
-   <span data-ttu-id="467d3-157">поворот 2-битового компонента</span><span class="sxs-lookup"><span data-stu-id="467d3-157">2-bit component rotation</span></span>
-   <span data-ttu-id="467d3-158">средство выбора 1-битового индекса (используются ли 2- или 3-битовые индексы)</span><span class="sxs-lookup"><span data-stu-id="467d3-158">1-bit index selector (whether the 2- or 3-bit indices are used)</span></span>

![структура битов режима 4](images/bc7-mode4.png)

## <a name="mode-5"></a><span data-ttu-id="467d3-160">Режим 5</span><span class="sxs-lookup"><span data-stu-id="467d3-160">Mode 5</span></span>

<span data-ttu-id="467d3-161">Режим BC7 5 имеет следующие характеристики:</span><span class="sxs-lookup"><span data-stu-id="467d3-161">BC7 Mode 5 has the following characteristics:</span></span>

-   <span data-ttu-id="467d3-162">Компоненты цвета с отдельным альфа-компонентом</span><span class="sxs-lookup"><span data-stu-id="467d3-162">Color components with separate alpha component</span></span>
-   <span data-ttu-id="467d3-163">1 подмножество на блок</span><span class="sxs-lookup"><span data-stu-id="467d3-163">1 subset per block</span></span>
-   <span data-ttu-id="467d3-164">Конечные точки цвета RGB 7.7.7</span><span class="sxs-lookup"><span data-stu-id="467d3-164">RGB 7.7.7 color endpoints</span></span>
-   <span data-ttu-id="467d3-165">8-разрядные конечные точки Alpha</span><span class="sxs-lookup"><span data-stu-id="467d3-165">8-bit alpha endpoints</span></span>
-   <span data-ttu-id="467d3-166">16 x 2-битовые индексы цвета</span><span class="sxs-lookup"><span data-stu-id="467d3-166">16 x 2-bit color indices</span></span>
-   <span data-ttu-id="467d3-167">16 x 2-битовые альфа-индексы</span><span class="sxs-lookup"><span data-stu-id="467d3-167">16 x 2-bit alpha indices</span></span>
-   <span data-ttu-id="467d3-168">поворот 2-битового компонента</span><span class="sxs-lookup"><span data-stu-id="467d3-168">2-bit component rotation</span></span>

![структура битов режима 5](images/bc7-mode5.png)

## <a name="mode-6"></a><span data-ttu-id="467d3-170">Режим 6</span><span class="sxs-lookup"><span data-stu-id="467d3-170">Mode 6</span></span>

<span data-ttu-id="467d3-171">Режим BC7 6 имеет следующие характеристики:</span><span class="sxs-lookup"><span data-stu-id="467d3-171">BC7 Mode 6 has the following characteristics:</span></span>

-   <span data-ttu-id="467d3-172">Комбинированные компоненты цвета и альфа-компоненты</span><span class="sxs-lookup"><span data-stu-id="467d3-172">Combined color and alpha components</span></span>
-   <span data-ttu-id="467d3-173">Одно подмножество на блок</span><span class="sxs-lookup"><span data-stu-id="467d3-173">One subset per block</span></span>
-   <span data-ttu-id="467d3-174">Конечные точки цвета (и альфа) RGBAP 7.7.7.7.1 (уникальный P-бит на конечную точку)</span><span class="sxs-lookup"><span data-stu-id="467d3-174">RGBAP 7.7.7.7.1 color (and alpha) endpoints (unique P-bit per endpoint)</span></span>
-   <span data-ttu-id="467d3-175">16 x 4-битовых индексов</span><span class="sxs-lookup"><span data-stu-id="467d3-175">16 x 4-bit indices</span></span>

![структура битов режима 6](images/bc7-mode6.png)

## <a name="mode-7"></a><span data-ttu-id="467d3-177">Режим 7</span><span class="sxs-lookup"><span data-stu-id="467d3-177">Mode 7</span></span>

<span data-ttu-id="467d3-178">Режим BC7 7 имеет следующие характеристики:</span><span class="sxs-lookup"><span data-stu-id="467d3-178">BC7 Mode 7 has the following characteristics:</span></span>

-   <span data-ttu-id="467d3-179">Комбинированные компоненты цвета и альфа-компоненты</span><span class="sxs-lookup"><span data-stu-id="467d3-179">Combined color and alpha components</span></span>
-   <span data-ttu-id="467d3-180">2 подмножества на каждый блок</span><span class="sxs-lookup"><span data-stu-id="467d3-180">2 subsets per block</span></span>
-   <span data-ttu-id="467d3-181">Конечные точки цвета (и альфа) RGBAP 5.5.5.5.1 (уникальный P-бит на конечную точку)</span><span class="sxs-lookup"><span data-stu-id="467d3-181">RGBAP 5.5.5.5.1 color (and alpha) endpoints (unique P-bit per endpoint)</span></span>
-   <span data-ttu-id="467d3-182">2-битовые индексы</span><span class="sxs-lookup"><span data-stu-id="467d3-182">2-bit indices</span></span>
-   <span data-ttu-id="467d3-183">64 разделов</span><span class="sxs-lookup"><span data-stu-id="467d3-183">64 partitions</span></span>

![структура битов режима 7](images/bc7-mode7.png)

## <a name="remarks"></a><span data-ttu-id="467d3-185">Примечания</span><span class="sxs-lookup"><span data-stu-id="467d3-185">Remarks</span></span>

<span data-ttu-id="467d3-186">Режим 8 (наименее значимому байту присвоено значение 0x00) зарезервирован.</span><span class="sxs-lookup"><span data-stu-id="467d3-186">Mode 8 (the least significant byte is set to 0x00) is reserved.</span></span> <span data-ttu-id="467d3-187">Не используйте его в своем кодировщике.</span><span class="sxs-lookup"><span data-stu-id="467d3-187">Don't use it in your encoder.</span></span> <span data-ttu-id="467d3-188">Если передать этот режим оборудованию, возвращается блок, инициализированный до всех нулей.</span><span class="sxs-lookup"><span data-stu-id="467d3-188">If you pass this mode to the hardware, a block initialized to all zeroes is returned.</span></span>

<span data-ttu-id="467d3-189">В BC7 можно зашифровать альфа-компонент одним из следующих способов:</span><span class="sxs-lookup"><span data-stu-id="467d3-189">In BC7, you can encode the alpha component in one of the following ways:</span></span>

-   <span data-ttu-id="467d3-190">Типы блоков без явной кодировки альфа-компонента.</span><span class="sxs-lookup"><span data-stu-id="467d3-190">Block types without explicit alpha component encoding.</span></span> <span data-ttu-id="467d3-191">В этих блоках конечные точки цвета имеют только кодировку RGB, а альфа-компонент декодируется до 1.0 для всех текселей.</span><span class="sxs-lookup"><span data-stu-id="467d3-191">In these blocks, the color endpoints have an RGB-only encoding, with the alpha component decoded to 1.0 for all texels.</span></span>
-   <span data-ttu-id="467d3-192">Типы блоков с объединенными компонентами цвета и альфа-компонентами.</span><span class="sxs-lookup"><span data-stu-id="467d3-192">Block types with combined color and alpha components.</span></span> <span data-ttu-id="467d3-193">В этих блоках значения цвета конечной точки задаются в формате RGBA, а значения альфа-компонента интерполируются вместе со значениями цвета.</span><span class="sxs-lookup"><span data-stu-id="467d3-193">In these blocks, the endpoint color values are specified in the RGBA format, and the alpha component values are interpolated along with the color values.</span></span>
-   <span data-ttu-id="467d3-194">Типы блоков с отдельными компонентами цвета и альфа-компонентами.</span><span class="sxs-lookup"><span data-stu-id="467d3-194">Block types with separated color and alpha components.</span></span> <span data-ttu-id="467d3-195">В этих блоках значения цвета и альфа задаются по отдельности — каждый со своим собственным набором индексов.</span><span class="sxs-lookup"><span data-stu-id="467d3-195">In these blocks the color and alpha values are specified separately, each with their own set of indices.</span></span> <span data-ttu-id="467d3-196">В результате у них есть эффективный вектор и скалярный канал, отдельно закодированный, где вектор обычно определяет цветовые каналы \[ R, G, B, \] а скаляр указывает альфа \[ -канал а \] .</span><span class="sxs-lookup"><span data-stu-id="467d3-196">As a result, they have an effective vector and a scalar channel separately encoded, where the vector commonly specifies the color channels \[R, G, B\] and the scalar specifies the alpha channel \[A\].</span></span> <span data-ttu-id="467d3-197">В поддержку такого подхода в кодировке предоставляется отдельное 2-битовое поле, которое позволяет задать отдельную кодировку канала в виде скалярного значения.</span><span class="sxs-lookup"><span data-stu-id="467d3-197">To support this approach, a separate 2-bit field is provided in the encoding, which permits the specification of the separate channel encoding as a scalar value.</span></span> <span data-ttu-id="467d3-198">В результате блок может иметь одно из следующих четырех представлений кодировки альфа (как указано в 2-битовом поле):</span><span class="sxs-lookup"><span data-stu-id="467d3-198">As a result, the block can have one of the following four different representations of this alpha encoding (as indicated by the 2-bit field):</span></span>
    -   <span data-ttu-id="467d3-199">RGB \| A: отделение альфа-канала</span><span class="sxs-lookup"><span data-stu-id="467d3-199">RGB\|A: alpha channel separate</span></span>
    -   <span data-ttu-id="467d3-200">АГБ \| R: отдельный цветовой канал "красный"</span><span class="sxs-lookup"><span data-stu-id="467d3-200">AGB\|R: "red" color channel separate</span></span>
    -   <span data-ttu-id="467d3-201">РАБ \| G: независимый цветовой канал "зеленый"</span><span class="sxs-lookup"><span data-stu-id="467d3-201">RAB\|G: "green" color channel separate</span></span>
    -   <span data-ttu-id="467d3-202">РГА \| B: отдельный цветовой канал "синий"</span><span class="sxs-lookup"><span data-stu-id="467d3-202">RGA\|B: "blue" color channel separate</span></span>

    <span data-ttu-id="467d3-203">После декодирования декодер снова упорядочивает каналы в порядке RGBA, поэтому внутренний формат блоков невидим разработчику.</span><span class="sxs-lookup"><span data-stu-id="467d3-203">The decoder reorders the channel order back to RGBA after decoding, so the internal block format is invisible to the developer.</span></span> <span data-ttu-id="467d3-204">Блоки с отдельными компонентами цвета и альфа-компонентами также имеют два набора данных индекса: один — для векторного набора каналов, другой — для скалярного канала.</span><span class="sxs-lookup"><span data-stu-id="467d3-204">Blacks with separate color and alpha components also have two sets of index data: one for the vectored set of channels, and one for the scalar channel.</span></span> <span data-ttu-id="467d3-205">(В случае режима 4 эти индексы имеют разное значение ширины \[ 2 или 3 бита \] .</span><span class="sxs-lookup"><span data-stu-id="467d3-205">(In the case of Mode 4, these indices are of differing widths \[2 or 3 bits\].</span></span> <span data-ttu-id="467d3-206">Режим 4 также содержит 1-битовое средство выбора, указывающее, использует ли векторный или скалярный канал 3-битовые индексы.)</span><span class="sxs-lookup"><span data-stu-id="467d3-206">Mode 4 also contains a 1-bit selector that specifies whether the vector or the scalar channel uses the 3-bit indices.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="467d3-207">См. также</span><span class="sxs-lookup"><span data-stu-id="467d3-207">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="467d3-208">Формат BC7</span><span class="sxs-lookup"><span data-stu-id="467d3-208">BC7 Format</span></span>](bc7-format.md)
</dt> </dl>

 

 




