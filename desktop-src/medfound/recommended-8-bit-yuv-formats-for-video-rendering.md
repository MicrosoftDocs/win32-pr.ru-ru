---
description: Рекомендуемые 8-разрядные форматы YUV для отрисовки видео
ms.assetid: 675d4c60-4c58-4f15-9bae-ffb0c389c608
title: Рекомендуемые 8-разрядные форматы YUV для отрисовки видео
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4505eb17f833040e0148ac98912f16af860b55b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811567"
---
# <a name="recommended-8-bit-yuv-formats-for-video-rendering"></a><span data-ttu-id="853d5-103">Рекомендуемые 8-разрядные форматы YUV для отрисовки видео</span><span class="sxs-lookup"><span data-stu-id="853d5-103">Recommended 8-Bit YUV Formats for Video Rendering</span></span>

<span data-ttu-id="853d5-104">Гари Салливан и Стивен Естроп</span><span class="sxs-lookup"><span data-stu-id="853d5-104">Gary Sullivan and Stephen Estrop</span></span>

<span data-ttu-id="853d5-105">Microsoft Corporation</span><span class="sxs-lookup"><span data-stu-id="853d5-105">Microsoft Corporation</span></span>

<span data-ttu-id="853d5-106">2002 апреля, Обновлено 2008 ноября</span><span class="sxs-lookup"><span data-stu-id="853d5-106">April 2002, updated November 2008</span></span>

<span data-ttu-id="853d5-107">В этом разделе описываются 8-разрядные форматы цвета YUV, Рекомендуемые для отрисовки видео в операционной системе Windows.</span><span class="sxs-lookup"><span data-stu-id="853d5-107">This topic describes the 8-bit YUV color formats that are recommended for video rendering in the Windows operating system.</span></span> <span data-ttu-id="853d5-108">В этой статье представлены методы для преобразования между форматами YUV и RGB, а также методы для избыточного отбора форматов YUV.</span><span class="sxs-lookup"><span data-stu-id="853d5-108">This article presents techniques for converting between YUV and RGB formats, and also provides techniques for upsampling YUV formats.</span></span> <span data-ttu-id="853d5-109">Эта статья предназначена для всех, кто работает с декодированием и отрисовкой видео YUV в Windows.</span><span class="sxs-lookup"><span data-stu-id="853d5-109">This article is intended for anyone working with YUV video decoding or rendering in Windows.</span></span>

## <a name="introduction"></a><span data-ttu-id="853d5-110">Введение</span><span class="sxs-lookup"><span data-stu-id="853d5-110">Introduction</span></span>

<span data-ttu-id="853d5-111">Многие форматы YUV определяются во всей видеоиндустрии.</span><span class="sxs-lookup"><span data-stu-id="853d5-111">Numerous YUV formats are defined throughout the video industry.</span></span> <span data-ttu-id="853d5-112">В этой статье указаны 8-разрядные форматы YUV, Рекомендуемые для отрисовки видео в Windows.</span><span class="sxs-lookup"><span data-stu-id="853d5-112">This article identifies the 8-bit YUV formats that are recommended for video rendering in Windows.</span></span> <span data-ttu-id="853d5-113">Поставщики декодеров и поставщики услуг показа должны поддерживать форматы, описанные в этой статье.</span><span class="sxs-lookup"><span data-stu-id="853d5-113">Decoder vendors and display vendors are encouraged to support the formats described in this article.</span></span> <span data-ttu-id="853d5-114">В этой статье не рассматриваются другие способы использования цвета YUV, такие как все еще фотографии.</span><span class="sxs-lookup"><span data-stu-id="853d5-114">This article does not address other uses of YUV color, such as still photography.</span></span>

<span data-ttu-id="853d5-115">Форматы, описанные в этой статье, используют 8 бит на пиксельное расположение для кодирования канала Y (также называемый каналом яркости) и используют 8 бит на выборку для кодирования каждого образца U или V чрома.</span><span class="sxs-lookup"><span data-stu-id="853d5-115">The formats described in this article all use 8 bits per pixel location to encode the Y channel (also called the luma channel), and use 8 bits per sample to encode each U or V chroma sample.</span></span> <span data-ttu-id="853d5-116">Однако большинство форматов YUV используют менее 24 бит на пиксель в среднем, так как они содержат меньшее число выборок и V, чем значение Y. В этой статье не рассматриваются форматы YUV с 10-или более высоким каналом Y.</span><span class="sxs-lookup"><span data-stu-id="853d5-116">However, most YUV formats use fewer than 24 bits per pixel on average, because they contain fewer samples of U and V than of Y. This article does not cover YUV formats with 10-bit or higher Y channels.</span></span>

> [!Note]  
> <span data-ttu-id="853d5-117">В рамках этой статьи термин U эквивалентен CB, а термин V эквивалентен CR.</span><span class="sxs-lookup"><span data-stu-id="853d5-117">For the purposes of this article, the term U is equivalent to Cb, and the term V is equivalent to Cr.</span></span>

 

<span data-ttu-id="853d5-118">В этой статье рассматриваются следующие темы:</span><span class="sxs-lookup"><span data-stu-id="853d5-118">This article covers the following topics:</span></span>

-   <span data-ttu-id="853d5-119">[Выборка YUV](#yuv-sampling).</span><span class="sxs-lookup"><span data-stu-id="853d5-119">[YUV Sampling](#yuv-sampling).</span></span> <span data-ttu-id="853d5-120">Описывает наиболее распространенные методы выборки YUV.</span><span class="sxs-lookup"><span data-stu-id="853d5-120">Describes the most common YUV sampling techniques.</span></span>
-   <span data-ttu-id="853d5-121">[Определения поверхности](#surface-definitions).</span><span class="sxs-lookup"><span data-stu-id="853d5-121">[Surface Definitions](#surface-definitions).</span></span> <span data-ttu-id="853d5-122">Описывает Рекомендуемые форматы YUV.</span><span class="sxs-lookup"><span data-stu-id="853d5-122">Describes the recommended YUV formats.</span></span>
-   <span data-ttu-id="853d5-123">[Цветовое пространство и преобразование частоты выборки чрома](#color-space-and-chroma-sampling-rate-conversions).</span><span class="sxs-lookup"><span data-stu-id="853d5-123">[Color Space and Chroma Sampling Rate Conversions](#color-space-and-chroma-sampling-rate-conversions).</span></span> <span data-ttu-id="853d5-124">Содержит некоторые рекомендации по преобразованию между форматами YUV и RGB и для преобразования между различными форматами YUV.</span><span class="sxs-lookup"><span data-stu-id="853d5-124">Provides some guidelines for converting between YUV and RGB formats and for converting between different YUV formats.</span></span>
-   <span data-ttu-id="853d5-125">[Определение форматов YUV в Media Foundation](#identifying-yuv-formats-in-media-foundation).</span><span class="sxs-lookup"><span data-stu-id="853d5-125">[Identifying YUV Formats in Media Foundation](#identifying-yuv-formats-in-media-foundation).</span></span> <span data-ttu-id="853d5-126">Описывает, как описать типы формата YUV в Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="853d5-126">Explains how to describe YUV format types in Media Foundation.</span></span>

## <a name="yuv-sampling"></a><span data-ttu-id="853d5-127">Выборка YUV</span><span class="sxs-lookup"><span data-stu-id="853d5-127">YUV Sampling</span></span>

<span data-ttu-id="853d5-128">Каналы чрома могут иметь меньшую частоту дискретизации, чем канал яркости, без значительной потери качества искусственного.</span><span class="sxs-lookup"><span data-stu-id="853d5-128">Chroma channels can have a lower sampling rate than the luma channel, without any dramatic loss of perceptual quality.</span></span> <span data-ttu-id="853d5-129">Нотация с именем "А:Б: C" используется для описания того, как часто вы и V выдаете выборку по оси Y:</span><span class="sxs-lookup"><span data-stu-id="853d5-129">A notation called the "A:B:C" notation is used to describe how often U and V are sampled relative to Y:</span></span>

-   <span data-ttu-id="853d5-130">4:4:4 — без понижения разрешения каналов чрома.</span><span class="sxs-lookup"><span data-stu-id="853d5-130">4:4:4 means no downsampling of the chroma channels.</span></span>
-   <span data-ttu-id="853d5-131">4:2:2 = 2:1 по горизонтали, без вертикального разрешения.</span><span class="sxs-lookup"><span data-stu-id="853d5-131">4:2:2 means 2:1 horizontal downsampling, with no vertical downsampling.</span></span> <span data-ttu-id="853d5-132">Каждая строка проверки содержит четыре образца Y для каждого из двух примеров U или V.</span><span class="sxs-lookup"><span data-stu-id="853d5-132">Every scan line contains four Y samples for every two U or V samples.</span></span>
-   <span data-ttu-id="853d5-133">4:2:0 — 2:1. понижение разрешения по горизонтали с 2:1 по вертикали.</span><span class="sxs-lookup"><span data-stu-id="853d5-133">4:2:0 means 2:1 horizontal downsampling, with 2:1 vertical downsampling.</span></span>
-   <span data-ttu-id="853d5-134">4:1:1 = 4:1 по горизонтали, без вертикального разрешения.</span><span class="sxs-lookup"><span data-stu-id="853d5-134">4:1:1 means 4:1 horizontal downsampling, with no vertical downsampling.</span></span> <span data-ttu-id="853d5-135">Каждая строка проверки содержит четыре образца по оси Y для каждого примера и V.</span><span class="sxs-lookup"><span data-stu-id="853d5-135">Every scan line contains four Y samples for each U and V sample.</span></span> <span data-ttu-id="853d5-136">4:1:1 выборка менее распространена, чем другие форматы, и не рассматривается подробно в этой статье.</span><span class="sxs-lookup"><span data-stu-id="853d5-136">4:1:1 sampling is less common than other formats, and is not discussed in detail in this article.</span></span>

<span data-ttu-id="853d5-137">На следующих диаграммах показано, как чрома выборка для каждой из ставок понижения разрешения.</span><span class="sxs-lookup"><span data-stu-id="853d5-137">The following diagrams shows how chroma is sampled for each of the downsampling rates.</span></span> <span data-ttu-id="853d5-138">Примеры яркости представлены в виде крестика, а чрома-образцы представлены кругом.</span><span class="sxs-lookup"><span data-stu-id="853d5-138">Luma samples are represented by a cross, and chroma samples are represented by a circle.</span></span>

![рис. 1.](images/yuv-sampling-grids.png)

<span data-ttu-id="853d5-141">Основная форма 4:2:2 выборки определяется в рекомендациях ITU-R BT. 601.</span><span class="sxs-lookup"><span data-stu-id="853d5-141">The dominant form of 4:2:2 sampling is defined in ITU-R Recommendation BT.601.</span></span> <span data-ttu-id="853d5-142">Существует два стандартных варианта выборки 4:2:0.</span><span class="sxs-lookup"><span data-stu-id="853d5-142">There are two common variants of 4:2:0 sampling.</span></span> <span data-ttu-id="853d5-143">Один из них используется в видео MPEG-2, а другой используется в формате MPEG-1 и в рекомендациях ITU-T в формате h. 261 и H. 263.</span><span class="sxs-lookup"><span data-stu-id="853d5-143">One of these is used in MPEG-2 video, and the other is used in MPEG-1 and in ITU-T Recommendations H.261 and H.263.</span></span>

<span data-ttu-id="853d5-144">По сравнению со схемой MPEG-1 проще выполнить преобразование между схемой MPEG-2 и таблицами выборки, определенными для форматов 4:2:2 и 4:4:4.</span><span class="sxs-lookup"><span data-stu-id="853d5-144">Compared with the MPEG-1 scheme, it is simpler to convert between the MPEG-2 scheme and the sampling grids defined for 4:2:2 and 4:4:4 formats.</span></span> <span data-ttu-id="853d5-145">По этой причине схема MPEG-2 является предпочтительной в Windows и должна рассматриваться как интерпретация формата 4:2:0 по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="853d5-145">For this reason, the MPEG-2 scheme is preferred in Windows, and should be considered the default interpretation of 4:2:0 formats.</span></span>

## <a name="surface-definitions"></a><span data-ttu-id="853d5-146">Определения Surface</span><span class="sxs-lookup"><span data-stu-id="853d5-146">Surface Definitions</span></span>

<span data-ttu-id="853d5-147">В этом разделе описываются 8-разрядные форматы YUV, Рекомендуемые для отрисовки видео.</span><span class="sxs-lookup"><span data-stu-id="853d5-147">This section describes the 8-bit YUV formats that are recommended for video rendering.</span></span> <span data-ttu-id="853d5-148">Они делятся на несколько категорий:</span><span class="sxs-lookup"><span data-stu-id="853d5-148">These fall into several categories:</span></span>

-   [<span data-ttu-id="853d5-149">форматы 4:4:4, 32 бит на пиксель</span><span class="sxs-lookup"><span data-stu-id="853d5-149">4:4:4 Formats, 32 Bits per Pixel</span></span>](#444-formats-32-bits-per-pixel)
-   [<span data-ttu-id="853d5-150">форматы 4:2:2, 16 бит на пиксель</span><span class="sxs-lookup"><span data-stu-id="853d5-150">4:2:2 Formats, 16 Bits per Pixel</span></span>](#422-formats-16-bits-per-pixel)
-   [<span data-ttu-id="853d5-151">форматы 4:2:0, 16 бит на пиксель</span><span class="sxs-lookup"><span data-stu-id="853d5-151">4:2:0 Formats, 16 Bits per Pixel</span></span>](#420-formats-16-bits-per-pixel)
-   [<span data-ttu-id="853d5-152">форматы 4:2:0, 12 бит на пиксель</span><span class="sxs-lookup"><span data-stu-id="853d5-152">4:2:0 Formats, 12 Bits per Pixel</span></span>](#420-formats-12-bits-per-pixel)

<span data-ttu-id="853d5-153">Во первых, необходимо знать о следующих понятиях, чтобы понять, что следует делать:</span><span class="sxs-lookup"><span data-stu-id="853d5-153">First, you should be aware of the following concepts in order to understand what follows:</span></span>

-   <span data-ttu-id="853d5-154">*Источник поверхности*.</span><span class="sxs-lookup"><span data-stu-id="853d5-154">*Surface origin*.</span></span> <span data-ttu-id="853d5-155">Для форматов YUV, описанных в этой статье, источник (0, 0) всегда находится в левом верхнем углу поверхности.</span><span class="sxs-lookup"><span data-stu-id="853d5-155">For the YUV formats described in this article, the origin (0,0) is always the top left corner of the surface.</span></span>
-   <span data-ttu-id="853d5-156">*Шаг*.</span><span class="sxs-lookup"><span data-stu-id="853d5-156">*Stride*.</span></span> <span data-ttu-id="853d5-157">Шаг поверхности, иногда называемый тон, — это ширина поверхности в байтах.</span><span class="sxs-lookup"><span data-stu-id="853d5-157">The stride of a surface, sometimes called the pitch, is the width of the surface in bytes.</span></span> <span data-ttu-id="853d5-158">При наличии источника поверхности в верхнем левом углу шаг всегда положительный.</span><span class="sxs-lookup"><span data-stu-id="853d5-158">Given a surface origin at the top left corner, the stride is always positive.</span></span>
-   <span data-ttu-id="853d5-159">*Выравнивание*.</span><span class="sxs-lookup"><span data-stu-id="853d5-159">*Alignment*.</span></span> <span data-ttu-id="853d5-160">Выравнивание поверхности по собственному выбору является драйвером графического экрана.</span><span class="sxs-lookup"><span data-stu-id="853d5-160">The alignment of a surface is at the discretion of the graphics display driver.</span></span> <span data-ttu-id="853d5-161">Поверхность всегда должна быть совмещена с помощью DWORD; Это значит, что отдельные строки внутри поверхности гарантированно поступают на границе 32 бит (DWORD).</span><span class="sxs-lookup"><span data-stu-id="853d5-161">The surface must always be DWORD aligned; that is, individual lines within the surface are guaranteed to originate on a 32-bit (DWORD) boundary.</span></span> <span data-ttu-id="853d5-162">Однако выравнивание может быть больше 32 бит в зависимости от потребностей оборудования.</span><span class="sxs-lookup"><span data-stu-id="853d5-162">The alignment can be larger than 32 bits, however, depending on the needs of the hardware.</span></span>
-   <span data-ttu-id="853d5-163">Упакованный формат и плоский формат.</span><span class="sxs-lookup"><span data-stu-id="853d5-163">Packed format versus planar format.</span></span> <span data-ttu-id="853d5-164">Форматы YUV делятся на *Упакованные* форматы и *плоские* форматы.</span><span class="sxs-lookup"><span data-stu-id="853d5-164">YUV formats are divided into *packed* formats and *planar* formats.</span></span> <span data-ttu-id="853d5-165">В упакованном формате компоненты Y, U и V хранятся в одном массиве.</span><span class="sxs-lookup"><span data-stu-id="853d5-165">In a packed format, the Y, U, and V components are stored in a single array.</span></span> <span data-ttu-id="853d5-166">Пиксели организованы в группы макропикселс, макет которых зависит от формата.</span><span class="sxs-lookup"><span data-stu-id="853d5-166">Pixels are organized into groups of macropixels, whose layout depends on the format.</span></span> <span data-ttu-id="853d5-167">В плоском формате компоненты Y, U и V хранятся в виде трех отдельных плоскостей.</span><span class="sxs-lookup"><span data-stu-id="853d5-167">In a planar format, the Y, U, and V components are stored as three separate planes.</span></span>

<span data-ttu-id="853d5-168">Каждый из форматов YUV, описанных в этой статье, имеет назначенный код FOURCC.</span><span class="sxs-lookup"><span data-stu-id="853d5-168">Each of the YUV formats described in this article has an assigned FOURCC code.</span></span> <span data-ttu-id="853d5-169">Код FOURCC — это 32-разрядное целое число без знака, которое создается путем сцепления четырех символов ASCII.</span><span class="sxs-lookup"><span data-stu-id="853d5-169">A FOURCC code is a 32-bit unsigned integer that is created by concatenating four ASCII characters.</span></span>

-   <span data-ttu-id="853d5-170">4:4:4 (32 бит)</span><span class="sxs-lookup"><span data-stu-id="853d5-170">4:4:4 (32 bpp)</span></span>
    -   [<span data-ttu-id="853d5-171">айув</span><span class="sxs-lookup"><span data-stu-id="853d5-171">AYUV</span></span>](#ayuv)
-   <span data-ttu-id="853d5-172">4:2:2 (16 бит)</span><span class="sxs-lookup"><span data-stu-id="853d5-172">4:2:2 (16 bpp)</span></span>
    -   [<span data-ttu-id="853d5-173">YUY2</span><span class="sxs-lookup"><span data-stu-id="853d5-173">YUY2</span></span>](#yuy2)
    -   [<span data-ttu-id="853d5-174">UYVY</span><span class="sxs-lookup"><span data-stu-id="853d5-174">UYVY</span></span>](#uyvy)
-   <span data-ttu-id="853d5-175">4:2:0 (16 бит)</span><span class="sxs-lookup"><span data-stu-id="853d5-175">4:2:0 (16 bpp)</span></span>
    -   [<span data-ttu-id="853d5-176">IMC1</span><span class="sxs-lookup"><span data-stu-id="853d5-176">IMC1</span></span>](#imc1)
    -   [<span data-ttu-id="853d5-177">IMC3</span><span class="sxs-lookup"><span data-stu-id="853d5-177">IMC3</span></span>](#imc3)
-   <span data-ttu-id="853d5-178">4:2:0 (12 бит)</span><span class="sxs-lookup"><span data-stu-id="853d5-178">4:2:0 (12 bpp)</span></span>
    -   [<span data-ttu-id="853d5-179">IMC2</span><span class="sxs-lookup"><span data-stu-id="853d5-179">IMC2</span></span>](#imc2)
    -   [<span data-ttu-id="853d5-180">IMC4</span><span class="sxs-lookup"><span data-stu-id="853d5-180">IMC4</span></span>](#imc4)
    -   [<span data-ttu-id="853d5-181">YV12</span><span class="sxs-lookup"><span data-stu-id="853d5-181">YV12</span></span>](#yv12)
    -   [<span data-ttu-id="853d5-182">NV12</span><span class="sxs-lookup"><span data-stu-id="853d5-182">NV12</span></span>](#nv12)

## <a name="444-formats-32-bits-per-pixel"></a><span data-ttu-id="853d5-183">форматы 4:4:4, 32 бит на пиксель</span><span class="sxs-lookup"><span data-stu-id="853d5-183">4:4:4 Formats, 32 Bits per Pixel</span></span>

### <a name="ayuv"></a><span data-ttu-id="853d5-184">айув</span><span class="sxs-lookup"><span data-stu-id="853d5-184">AYUV</span></span>

<span data-ttu-id="853d5-185">Рекомендуется использовать один формат 4:4:4 с кодом FOURCC АЙУВ.</span><span class="sxs-lookup"><span data-stu-id="853d5-185">A single 4:4:4 format is recommended, with the FOURCC code AYUV.</span></span> <span data-ttu-id="853d5-186">Это упакованный формат, где каждый пиксель кодируется четырьмя последовательными байтами, упорядоченным в последовательности, показанной на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="853d5-186">This is a packed format, where each pixel is encoded as four consecutive bytes, arranged in the sequence shown in the following illustration.</span></span>

![рис. 2.](images/yuvformats01.gif)

<span data-ttu-id="853d5-189">Байты, отмеченные, содержат значения для альфа.</span><span class="sxs-lookup"><span data-stu-id="853d5-189">The bytes marked A contain values for alpha.</span></span>

## <a name="422-formats-16-bits-per-pixel"></a><span data-ttu-id="853d5-190">форматы 4:2:2, 16 бит на пиксель</span><span class="sxs-lookup"><span data-stu-id="853d5-190">4:2:2 Formats, 16 Bits per Pixel</span></span>

<span data-ttu-id="853d5-191">Рекомендуется использовать два формата 4:2:2 с приведенными ниже кодами FOURCC.</span><span class="sxs-lookup"><span data-stu-id="853d5-191">Two 4:2:2 formats are recommended, with the following FOURCC codes:</span></span>

-   <span data-ttu-id="853d5-192">YUY2</span><span class="sxs-lookup"><span data-stu-id="853d5-192">YUY2</span></span>
-   <span data-ttu-id="853d5-193">UYVY</span><span class="sxs-lookup"><span data-stu-id="853d5-193">UYVY</span></span>

<span data-ttu-id="853d5-194">Оба являются упакованными форматами, где каждый макропиксел — два пиксела, закодированных четырьмя последовательными байтами.</span><span class="sxs-lookup"><span data-stu-id="853d5-194">Both are packed formats, where each macropixel is two pixels encoded as four consecutive bytes.</span></span> <span data-ttu-id="853d5-195">Это приводит к горизонтальному понижению чрома с коэффициентом 2.</span><span class="sxs-lookup"><span data-stu-id="853d5-195">This results in horizontal downsampling of the chroma by a factor of two.</span></span>

### <a name="yuy2"></a><span data-ttu-id="853d5-196">YUY2</span><span class="sxs-lookup"><span data-stu-id="853d5-196">YUY2</span></span>

<span data-ttu-id="853d5-197">В формате YUY2 данные могут рассматриваться как массив значений типа **char** без знака, где первый байт содержит первый образец Y, второй байт содержит первый экземпляр U (CB), третий байт содержит второй образец y, а четвертый байт — первый (CR) пример, как показано на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="853d5-197">In YUY2 format, the data can be treated as an array of unsigned **char** values, where the first byte contains the first Y sample, the second byte contains the first U (Cb) sample, the third byte contains the second Y sample, and the fourth byte contains the first V (Cr) sample, as shown in the following diagram.</span></span>

![рис. 3.](images/yuvformats02.gif)

<span data-ttu-id="853d5-200">Если изображение обработано как массив значений **слов** с прямым порядком байтов, то первое **слово** содержит первый образец Y в наименее значимых битах (лсбс) и первый экземпляр U (CB) в наиболее значимых битах (МСБС).</span><span class="sxs-lookup"><span data-stu-id="853d5-200">If the image is addressed as an array of little-endian **WORD** values, the first **WORD** contains the first Y sample in the least significant bits (LSBs) and the first U (Cb) sample in the most significant bits (MSBs).</span></span> <span data-ttu-id="853d5-201">Второе **слово** содержит второй пример Y в лсбс и первый пример V (CR) в МСБС.</span><span class="sxs-lookup"><span data-stu-id="853d5-201">The second **WORD** contains the second Y sample in the LSBs and the first V (Cr) sample in the MSBs.</span></span>

<span data-ttu-id="853d5-202">YUY2 — предпочтительный формат 4:2:2 пикселей для ускорения видео Microsoft DirectX (DirectX ва).</span><span class="sxs-lookup"><span data-stu-id="853d5-202">YUY2 is the preferred 4:2:2 pixel format for Microsoft DirectX Video Acceleration (DirectX VA).</span></span> <span data-ttu-id="853d5-203">Это должно быть промежуточное требование для ускорителей DirectX, поддерживающих видео 4:2:2.</span><span class="sxs-lookup"><span data-stu-id="853d5-203">It is expected to be an intermediate-term requirement for DirectX VA accelerators supporting 4:2:2 video.</span></span>

### <a name="uyvy"></a><span data-ttu-id="853d5-204">UYVY</span><span class="sxs-lookup"><span data-stu-id="853d5-204">UYVY</span></span>

<span data-ttu-id="853d5-205">Этот формат совпадает с форматом YUY2, за исключением того, что порядок байтов изменяется на обратный, то есть чрома и яркости байты перемещаются (рис. 4).</span><span class="sxs-lookup"><span data-stu-id="853d5-205">This format is the same as the YUY2 format except the byte order is reversed—that is, the chroma and luma bytes are flipped (Figure 4).</span></span> <span data-ttu-id="853d5-206">Если изображение обработано как массив из двух значений **слов** с прямым порядком байтов, первое **слово** содержит U в Лсбс и Y0 в МСБС, а второе **слово** содержит V в лсбс и Y1 в МСБС.</span><span class="sxs-lookup"><span data-stu-id="853d5-206">If the image is addressed as an array of two little-endian **WORD** values, the first **WORD** contains U in the LSBs and Y0 in the MSBs, and the second **WORD** contains V in the LSBs and Y1 in the MSBs.</span></span>

![рис. 4.](images/yuvformats03.gif)

## <a name="420-formats-16-bits-per-pixel"></a><span data-ttu-id="853d5-209">форматы 4:2:0, 16 бит на пиксель</span><span class="sxs-lookup"><span data-stu-id="853d5-209">4:2:0 Formats, 16 Bits per Pixel</span></span>

<span data-ttu-id="853d5-210">Рекомендуется использовать два формата: 4:2:0 16 – бит на пиксель (бит в пикселах) с приведенными ниже кодами FOURCC.</span><span class="sxs-lookup"><span data-stu-id="853d5-210">Two 4:2:0 16-bits per pixel (bpp) formats are recommended, with the following FOURCC codes:</span></span>

-   <span data-ttu-id="853d5-211">IMC1</span><span class="sxs-lookup"><span data-stu-id="853d5-211">IMC1</span></span>
-   <span data-ttu-id="853d5-212">IMC3</span><span class="sxs-lookup"><span data-stu-id="853d5-212">IMC3</span></span>

<span data-ttu-id="853d5-213">Оба этих формата YUV имеют плоские форматы.</span><span class="sxs-lookup"><span data-stu-id="853d5-213">Both of these YUV formats are planar formats.</span></span> <span data-ttu-id="853d5-214">Чрома каналы вычисляются с коэффициентом 2 в горизонтальном и вертикальном измерениях.</span><span class="sxs-lookup"><span data-stu-id="853d5-214">The chroma channels are subsampled by a factor of two in both the horizontal and vertical dimensions.</span></span>

### <a name="imc1"></a><span data-ttu-id="853d5-215">IMC1</span><span class="sxs-lookup"><span data-stu-id="853d5-215">IMC1</span></span>

<span data-ttu-id="853d5-216">Все примеры Y отображаются первыми в памяти как массив значений типа **char** без знака.</span><span class="sxs-lookup"><span data-stu-id="853d5-216">All of the Y samples appear first in memory as an array of unsigned **char** values.</span></span> <span data-ttu-id="853d5-217">Далее следуют все примеры версии (CR), а затем все примеры U (CB).</span><span class="sxs-lookup"><span data-stu-id="853d5-217">This is followed by all of the V (Cr) samples, and then all of the U (Cb) samples.</span></span> <span data-ttu-id="853d5-218">Плоскости V и U имеют тот же шаг, что и плоскость Y, что приводит к неиспользуемым областям памяти, как показано на рис. 5.</span><span class="sxs-lookup"><span data-stu-id="853d5-218">The V and U planes have the same stride as the Y plane, resulting in unused areas of memory, as shown in Figure 5.</span></span> <span data-ttu-id="853d5-219">Плоскости, которые вы и V должны начать с границ памяти, кратных 16 строкам.</span><span class="sxs-lookup"><span data-stu-id="853d5-219">The U and V planes must start on memory boundaries that are a multiple of 16 lines.</span></span> <span data-ttu-id="853d5-220">На рис. 5 показан источник и V для видеокадра 352 x 240.</span><span class="sxs-lookup"><span data-stu-id="853d5-220">Figure 5 shows the origin of U and V for a 352 x 240 video frame.</span></span> <span data-ttu-id="853d5-221">Начальный адрес плоскостей и плоскости V вычисляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="853d5-221">The starting address of the U and V planes are calculated as follows:</span></span>

``` syntax
BYTE* pV = pY + (((Height + 15) & ~15) * Stride);
BYTE* pU = pY + (((((Height * 3) / 2) + 15) & ~15) * Stride);
```

<span data-ttu-id="853d5-222">где *корректировка* — это байтовый указатель на начало массива памяти, как показано на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="853d5-222">where *pY* is a byte pointer to the start of the memory array, as shown in the following diagram.</span></span>

![рис. 5.](images/yuvformats04.gif)

### <a name="imc3"></a><span data-ttu-id="853d5-225">IMC3</span><span class="sxs-lookup"><span data-stu-id="853d5-225">IMC3</span></span>

<span data-ttu-id="853d5-226">Этот формат идентичен IMC1, за исключением того, что вы и V-плоскости меняются, как показано на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="853d5-226">This format is identical to IMC1, except the U and V planes are swapped, as shown in the following diagram.</span></span>

![рис. 6.](images/yuvformats05.gif)

## <a name="420-formats-12-bits-per-pixel"></a><span data-ttu-id="853d5-229">форматы 4:2:0, 12 бит на пиксель</span><span class="sxs-lookup"><span data-stu-id="853d5-229">4:2:0 Formats, 12 Bits per Pixel</span></span>

<span data-ttu-id="853d5-230">Рекомендуется использовать четыре формата 4:2:0 12-бит с кодами FOURCC:</span><span class="sxs-lookup"><span data-stu-id="853d5-230">Four 4:2:0 12-bpp formats are recommended, with the following FOURCC codes:</span></span>

-   <span data-ttu-id="853d5-231">IMC2</span><span class="sxs-lookup"><span data-stu-id="853d5-231">IMC2</span></span>
-   <span data-ttu-id="853d5-232">IMC4</span><span class="sxs-lookup"><span data-stu-id="853d5-232">IMC4</span></span>
-   <span data-ttu-id="853d5-233">YV12</span><span class="sxs-lookup"><span data-stu-id="853d5-233">YV12</span></span>
-   <span data-ttu-id="853d5-234">NV12</span><span class="sxs-lookup"><span data-stu-id="853d5-234">NV12</span></span>

<span data-ttu-id="853d5-235">Во всех этих форматах каналы чрома вычисляются с помощью коэффициента 2 в горизонтальном и вертикальном измерениях.</span><span class="sxs-lookup"><span data-stu-id="853d5-235">In all of these formats, the chroma channels are subsampled by a factor of two in both the horizontal and vertical dimensions.</span></span>

### <a name="imc2"></a><span data-ttu-id="853d5-236">IMC2</span><span class="sxs-lookup"><span data-stu-id="853d5-236">IMC2</span></span>

<span data-ttu-id="853d5-237">Этот формат совпадает с IMC1, за исключением следующего отличия: строки V (CR) и U (CB) чередуются по границам половинного шага.</span><span class="sxs-lookup"><span data-stu-id="853d5-237">This format is the same as IMC1 except for the following difference: The V (Cr) and U (Cb) lines are interleaved at half-stride boundaries.</span></span> <span data-ttu-id="853d5-238">Иными словами, каждая строка с полным шагом в области чрома начинается со строки с примерами V, за которой следуют строки U, которые начинаются со следующей границы половинного шага (рис. 7).</span><span class="sxs-lookup"><span data-stu-id="853d5-238">In other words, each full-stride line in the chroma area starts with a line of V samples, followed by a line of U samples that begins at the next half-stride boundary (Figure 7).</span></span> <span data-ttu-id="853d5-239">Этот макет позволяет более эффективно использовать адресное пространство, чем IMC1.</span><span class="sxs-lookup"><span data-stu-id="853d5-239">This layout makes more efficient use of address space than IMC1.</span></span> <span data-ttu-id="853d5-240">Он вырезает адресное пространство чрома в половину, а значит общее адресное пространство на 25 процентов.</span><span class="sxs-lookup"><span data-stu-id="853d5-240">It cuts the chroma address space in half, and thus the total address space by 25 percent.</span></span> <span data-ttu-id="853d5-241">В форматах 4:2:0 IMC2 — это второй предпочтительный формат после NV12.</span><span class="sxs-lookup"><span data-stu-id="853d5-241">Among 4:2:0 formats, IMC2 is the second-most preferred format, after NV12.</span></span> <span data-ttu-id="853d5-242">Этот процесс показан на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="853d5-242">The following image illustrates this process.</span></span>

![рис. 7.](images/yuvformats07.gif)

### <a name="imc4"></a><span data-ttu-id="853d5-245">IMC4</span><span class="sxs-lookup"><span data-stu-id="853d5-245">IMC4</span></span>

<span data-ttu-id="853d5-246">Этот формат идентичен IMC2, за исключением того, что строки U (CB) и V (CR) меняются местами, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="853d5-246">This format is identical to IMC2, except the U (Cb) and V (Cr) lines are swapped, as shown in the following illustration.</span></span>

![рис. 8.](images/yuvformats06.gif)

### <a name="yv12"></a><span data-ttu-id="853d5-249">YV12</span><span class="sxs-lookup"><span data-stu-id="853d5-249">YV12</span></span>

<span data-ttu-id="853d5-250">Все примеры Y отображаются первыми в памяти как массив значений типа **char** без знака.</span><span class="sxs-lookup"><span data-stu-id="853d5-250">All of the Y samples appear first in memory as an array of unsigned **char** values.</span></span> <span data-ttu-id="853d5-251">За этим массивом следуют все примеры V (CR).</span><span class="sxs-lookup"><span data-stu-id="853d5-251">This array is followed immediately by all of the V (Cr) samples.</span></span> <span data-ttu-id="853d5-252">Шаг в плоскости V — половина шага плоскости Y; а плоскость V содержит половину столько же линий, сколько у плоскости Y.</span><span class="sxs-lookup"><span data-stu-id="853d5-252">The stride of the V plane is half the stride of the Y plane; and the V plane contains half as many lines as the Y plane.</span></span> <span data-ttu-id="853d5-253">В плоскости V сразу идут все примеры U (CB) с тем же шагом и числом строк, что и в плоскости V, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="853d5-253">The V plane is followed immediately by all of the U (Cb) samples, with the same stride and number of lines as the V plane, as shown in the following illustration.</span></span>

![рис. 9.](images/yuvformats08.gif)

### <a name="nv12"></a><span data-ttu-id="853d5-256">NV12</span><span class="sxs-lookup"><span data-stu-id="853d5-256">NV12</span></span>

<span data-ttu-id="853d5-257">Все примеры Y отображаются первыми в памяти как массив значений **char** без знака с четным числом строк.</span><span class="sxs-lookup"><span data-stu-id="853d5-257">All of the Y samples appear first in memory as an array of unsigned **char** values with an even number of lines.</span></span> <span data-ttu-id="853d5-258">За плоскостью Y следует массив значений **char** без знака, содержащий Упакованные примеры U (CB) и V (CR).</span><span class="sxs-lookup"><span data-stu-id="853d5-258">The Y plane is followed immediately by an array of unsigned **char** values that contains packed U (Cb) and V (Cr) samples.</span></span> <span data-ttu-id="853d5-259">Если объединенный массив U-V адресован как массив значений **слов** с прямым порядком байтов, лсбс содержит значения U, а МСБС содержит значения V.</span><span class="sxs-lookup"><span data-stu-id="853d5-259">When the combined U-V array is addressed as an array of little-endian **WORD** values, the LSBs contain the U values, and the MSBs contain the V values.</span></span> <span data-ttu-id="853d5-260">NV12 — предпочтительный формат 4:2:0 пикселей для DirectX ва.</span><span class="sxs-lookup"><span data-stu-id="853d5-260">NV12 is the preferred 4:2:0 pixel format for DirectX VA.</span></span> <span data-ttu-id="853d5-261">Это должно быть промежуточное требование для ускорителей DirectX, поддерживающих видео 4:2:0.</span><span class="sxs-lookup"><span data-stu-id="853d5-261">It is expected to be an intermediate-term requirement for DirectX VA accelerators supporting 4:2:0 video.</span></span> <span data-ttu-id="853d5-262">На следующем рисунке показана плоскость Y и массив, которые содержат Упакованные образцы.</span><span class="sxs-lookup"><span data-stu-id="853d5-262">The following illustration shows the Y plane and the array that contains packed U and V samples.</span></span>

![рис. 10.](images/yuvformats09.gif)

## <a name="color-space-and-chroma-sampling-rate-conversions"></a><span data-ttu-id="853d5-265">Цветовое пространство и преобразование частоты выборки Чрома</span><span class="sxs-lookup"><span data-stu-id="853d5-265">Color Space and Chroma Sampling Rate Conversions</span></span>

<span data-ttu-id="853d5-266">В этом разделе приводятся рекомендации по преобразованию между YUV и RGB, а также для преобразования между различными форматами YUV.</span><span class="sxs-lookup"><span data-stu-id="853d5-266">This section provides guidelines for converting between YUV and RGB, and for converting between some different YUV formats.</span></span> <span data-ttu-id="853d5-267">В этом разделе мы рассмотрим две схемы кодирования RGB: *8-разрядный RGB*, также известный как sRGB или RGB с полноэкранным масштабированием, *видео* RGB или "RGB с головным пространством и кабинетом".</span><span class="sxs-lookup"><span data-stu-id="853d5-267">We consider two RGB encoding schemes in this section: *8-bit computer RGB*, also known as sRGB or "full-scale" RGB, and *studio video RGB*, or "RGB with head-room and toe-room."</span></span> <span data-ttu-id="853d5-268">Они определяются следующим образом.</span><span class="sxs-lookup"><span data-stu-id="853d5-268">These are defined as follows:</span></span>

-   <span data-ttu-id="853d5-269">Компьютер RGB использует 8 бит для каждого образца красного, зеленого и синего цветов.</span><span class="sxs-lookup"><span data-stu-id="853d5-269">Computer RGB uses 8 bits for each sample of red, green, and blue.</span></span> <span data-ttu-id="853d5-270">Черный представляется R = G = B = 0, а белый представляется R = G = B = 255.</span><span class="sxs-lookup"><span data-stu-id="853d5-270">Black is represented by R = G = B = 0, and white is represented by R = G = B = 255.</span></span>
-   <span data-ttu-id="853d5-271">В Studio Video RGB используется некоторое количество бит N для каждого образца красного, зеленого и синего, где N — 8 или более.</span><span class="sxs-lookup"><span data-stu-id="853d5-271">Studio video RGB uses some number of bits N for each sample of red, green, and blue, where N is 8 or more.</span></span> <span data-ttu-id="853d5-272">В студии видео RGB используется другой коэффициент масштабирования, отличный от значения RGB компьютера, и он имеет смещение.</span><span class="sxs-lookup"><span data-stu-id="853d5-272">Studio video RGB uses a different scaling factor than computer RGB, and it has an offset.</span></span> <span data-ttu-id="853d5-273">Черный представляется R = G = B = 16 \* 2 ^ (N-8), а белый представляется r = G = B = 235 \* 2 ^ (N-8).</span><span class="sxs-lookup"><span data-stu-id="853d5-273">Black is represented by R = G = B = 16\*2^(N-8), and white is represented by R = G = B = 235\*2^(N-8).</span></span> <span data-ttu-id="853d5-274">Однако фактические значения могут находиться за пределами этого диапазона.</span><span class="sxs-lookup"><span data-stu-id="853d5-274">However, actual values may fall outside this range.</span></span>

<span data-ttu-id="853d5-275">Видео в студии RGB — это предпочтительное определение RGB для видео в Windows, а RGB — предпочтительное определение RGB для приложений, не являющихся видеороликами.</span><span class="sxs-lookup"><span data-stu-id="853d5-275">Studio video RGB is the preferred RGB definition for video in Windows, while computer RGB is the preferred RGB definition for non-video applications.</span></span> <span data-ttu-id="853d5-276">В любой форме RGB координаты цветовой области задаются в ITU-R BT. 709 для определения первичных цветов RGB.</span><span class="sxs-lookup"><span data-stu-id="853d5-276">In either form of RGB, the chromaticity coordinates are as specified in ITU-R BT.709 for the definition of the RGB color primaries.</span></span> <span data-ttu-id="853d5-277">Координаты (x, y) R, G и B имеют значение (0,64, 0,33), (0,30, 0,60) и (0,15, 0,06) соответственно.</span><span class="sxs-lookup"><span data-stu-id="853d5-277">The (x,y) coordinates of R, G, and B are (0.64, 0.33), (0.30, 0.60), and (0.15, 0.06), respectively.</span></span> <span data-ttu-id="853d5-278">Ссылка белого — D65 с координатами (0,3127, 0,3290).</span><span class="sxs-lookup"><span data-stu-id="853d5-278">Reference white is D65 with coordinates (0.3127, 0.3290).</span></span> <span data-ttu-id="853d5-279">Номинальная гамма — 1/0.45 (приблизительно 2,2), с точным определением гаммы в ITU-R BT. 709.</span><span class="sxs-lookup"><span data-stu-id="853d5-279">Nominal gamma is 1/0.45 (approximately 2.2), with precise gamma defined in detail in ITU-R BT.709.</span></span>

<span data-ttu-id="853d5-280">**Преобразование между RGB и 4:4:4 YUV**</span><span class="sxs-lookup"><span data-stu-id="853d5-280">**Conversion between RGB and 4:4:4 YUV**</span></span>

<span data-ttu-id="853d5-281">Сначала мы рассмотрим преобразование между RGB и 4:4:4 YUV.</span><span class="sxs-lookup"><span data-stu-id="853d5-281">We first describe conversion between RGB and 4:4:4 YUV.</span></span> <span data-ttu-id="853d5-282">Чтобы преобразовать 4:2:0 или 4:2:2 YUV в RGB, мы рекомендуем преобразовать данные YUV в 4:4:4 YUV, а затем преобразовать из 4:4:4 YUV в RGB.</span><span class="sxs-lookup"><span data-stu-id="853d5-282">To convert 4:2:0 or 4:2:2 YUV to RGB, we recommend converting the YUV data to 4:4:4 YUV, and then converting from 4:4:4 YUV to RGB.</span></span> <span data-ttu-id="853d5-283">Формат АЙУВ, который является форматом 4:4:4, использует 8 бит каждый для примеров Y, U и V.</span><span class="sxs-lookup"><span data-stu-id="853d5-283">The AYUV format, which is a 4:4:4 format, uses 8 bits each for the Y, U, and V samples.</span></span> <span data-ttu-id="853d5-284">YUV можно также определить с помощью более чем 8 бит на выборку для некоторых приложений.</span><span class="sxs-lookup"><span data-stu-id="853d5-284">YUV can also be defined using more than 8 bits per sample for some applications.</span></span>

<span data-ttu-id="853d5-285">Для цифрового видео были определены два основных преобразования YUV из RGB.</span><span class="sxs-lookup"><span data-stu-id="853d5-285">Two dominant YUV conversions from RGB have been defined for digital video.</span></span> <span data-ttu-id="853d5-286">Они основаны на спецификации, известной как ITU-R рекомендует BT. 709.</span><span class="sxs-lookup"><span data-stu-id="853d5-286">Both are based on the specification known as ITU-R Recommendation BT.709.</span></span> <span data-ttu-id="853d5-287">Первое преобразование — это старая форма YUV, определенная для использования в 50-Гц в BT. 709.</span><span class="sxs-lookup"><span data-stu-id="853d5-287">The first conversion is the older YUV form defined for 50-Hz use in BT.709.</span></span> <span data-ttu-id="853d5-288">Это то же самое, что и отношение, указанное в рекомендациях ITU-R BT. 601, также известное по старому имени, КЦИР 601.</span><span class="sxs-lookup"><span data-stu-id="853d5-288">It is the same as the relation specified in ITU-R Recommendation BT.601, also known by its older name, CCIR 601.</span></span> <span data-ttu-id="853d5-289">Он должен рассматриваться в качестве предпочтительного формата YUV для стандартного разрешения ТЕЛЕПЕРЕДАЧ (720 x 576) и видео с более низким разрешением.</span><span class="sxs-lookup"><span data-stu-id="853d5-289">It should be considered the preferred YUV format for standard-definition TV resolution (720 x 576) and lower-resolution video.</span></span> <span data-ttu-id="853d5-290">Он характеризуется значениями двух констант *kr* и *KB*:</span><span class="sxs-lookup"><span data-stu-id="853d5-290">It is characterized by the values of two constants *Kr* and *Kb*:</span></span>

``` syntax
Kr = 0.299
Kb = 0.114
```

<span data-ttu-id="853d5-291">Второе преобразование — это более новая форма YUV, определенная для 60-Гц, используется в BT. 709 и должна считаться предпочтительным форматом для разрешений видео выше СДТВ.</span><span class="sxs-lookup"><span data-stu-id="853d5-291">The second conversion is the newer YUV form defined for 60-Hz use in BT.709, and should be considered the preferred format for video resolutions above SDTV.</span></span> <span data-ttu-id="853d5-292">Он характеризуется различными значениями для этих двух констант:</span><span class="sxs-lookup"><span data-stu-id="853d5-292">It is characterized by different values for these two constants:</span></span>

``` syntax
Kr = 0.2126
Kb = 0.0722
```

<span data-ttu-id="853d5-293">Преобразование из RGB в YUV определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="853d5-293">Conversion from RGB to YUV is defined by starting with the following:</span></span>

``` syntax
L = Kr * R + Kb * B + (1 - Kr - Kb) * G
```

<span data-ttu-id="853d5-294">Затем значения YUV получаются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="853d5-294">The YUV values are then obtained as follows:</span></span>

``` syntax
Y =                   floor(2^(M-8) * (219*(L-Z)/S + 16) + 0.5)
U = clip3(0, (2^M)-1, floor(2^(M-8) * (112*(B-L) / ((1-Kb)*S) + 128) + 0.5))
V = clip3(0, (2^M)-1, floor(2^(M-8) * (112*(R-L) / ((1-Kr)*S) + 128) + 0.5))
```

<span data-ttu-id="853d5-295">where</span><span class="sxs-lookup"><span data-stu-id="853d5-295">where</span></span>

-   <span data-ttu-id="853d5-296">M — это число битов на каждый пример YUV (M >= 8).</span><span class="sxs-lookup"><span data-stu-id="853d5-296">M is the number of bits per YUV sample (M >= 8).</span></span>
-   <span data-ttu-id="853d5-297">Z — это переменная Черного уровня.</span><span class="sxs-lookup"><span data-stu-id="853d5-297">Z is the black-level variable.</span></span> <span data-ttu-id="853d5-298">Для компьютера RGB Z равно 0.</span><span class="sxs-lookup"><span data-stu-id="853d5-298">For computer RGB, Z equals 0.</span></span> <span data-ttu-id="853d5-299">Для Video видео RGB Z равно 16 \* 2 ^ (N-8), где N — это число битов на пример RGB (n >= 8).</span><span class="sxs-lookup"><span data-stu-id="853d5-299">For studio video RGB, Z equals 16\*2^(N-8), where N is the number of bits per RGB sample (N >= 8).</span></span>
-   <span data-ttu-id="853d5-300">Параметр S является переменной масштабирования.</span><span class="sxs-lookup"><span data-stu-id="853d5-300">S is the scaling variable.</span></span> <span data-ttu-id="853d5-301">Для компьютеров RGB, S равняется 255.</span><span class="sxs-lookup"><span data-stu-id="853d5-301">For computer RGB, S equals 255.</span></span> <span data-ttu-id="853d5-302">Для Video видео RGB S равняется 219 \* 2 ^ (N-8).</span><span class="sxs-lookup"><span data-stu-id="853d5-302">For studio video RGB, S equals 219\*2^(N-8).</span></span>

<span data-ttu-id="853d5-303">Функция floor (x) возвращает максимальное целое число, которое меньше или равно x.</span><span class="sxs-lookup"><span data-stu-id="853d5-303">The function floor(x) returns the largest integer less than or equal to x.</span></span> <span data-ttu-id="853d5-304">Функция clip3 (x, y, z) определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="853d5-304">The function clip3(x, y, z) is defined as follows:</span></span>

``` syntax
clip3(x, y, z) = ((z < x) ? x : ((z > y) ? y : z))
```

> [!Note]  
> <span data-ttu-id="853d5-305">clip3 должен быть реализован как функция, а не как макрос препроцессора; в противном случае возникнет несколько оценок аргументов.</span><span class="sxs-lookup"><span data-stu-id="853d5-305">clip3 should be implemented as a function rather than a preprocessor macro; otherwise multiple evaluations of the arguments will occur.</span></span>

 

<span data-ttu-id="853d5-306">Пример «Y» представляет яркость, а примеры «вы» и «V» представляют цветовые отклонения в направлении синего и Красного соответственно.</span><span class="sxs-lookup"><span data-stu-id="853d5-306">The Y sample represents brightness, and the U and V samples represent the color deviations toward blue and red, respectively.</span></span> <span data-ttu-id="853d5-307">Номинальный диапазон для Y — 16 \* 2 ^ (m-8) до 235 \* 2 ^ (m-8).</span><span class="sxs-lookup"><span data-stu-id="853d5-307">The nominal range for Y is 16\*2^(M-8) to 235\*2^(M-8).</span></span> <span data-ttu-id="853d5-308">Черный представляется как 16 \* 2 ^ (m-8), а белый представляется как 235 \* 2 ^ (m-8).</span><span class="sxs-lookup"><span data-stu-id="853d5-308">Black is represented as 16\*2^(M-8), and white is represented as 235\*2^(M-8).</span></span> <span data-ttu-id="853d5-309">Номинальный диапазон для вас и V — 16 \* 2 ^ (m-8) до 240 \* 2 ^ (m-8), со значением 128 \* 2 ^ (m-8), представляющим нейтральный чрома.</span><span class="sxs-lookup"><span data-stu-id="853d5-309">The nominal range for U and V are 16\*2^(M-8) to 240\*2^(M-8), with the value 128\*2^(M-8) representing neutral chroma.</span></span> <span data-ttu-id="853d5-310">Однако фактические значения могут находиться за пределами этих диапазонов.</span><span class="sxs-lookup"><span data-stu-id="853d5-310">However, actual values may fall outside these ranges.</span></span>

<span data-ttu-id="853d5-311">Для входных данных в виде видео RGB в Studio необходимо выполнить операцию Clip, чтобы сохранить значения для вас и V в диапазоне от 0 до (2 ^ M) – 1.</span><span class="sxs-lookup"><span data-stu-id="853d5-311">For input data in the form of studio video RGB, the clip operation is necessary to keep the U and V values within the range 0 to (2^M)-1.</span></span> <span data-ttu-id="853d5-312">Если входными данными является компьютер RGB, операция Clip не требуется, поскольку формула преобразования не может формировать значения за пределами этого диапазона.</span><span class="sxs-lookup"><span data-stu-id="853d5-312">If the input is computer RGB, the clip operation is not required, because the conversion formula cannot produce values outside of this range.</span></span>

<span data-ttu-id="853d5-313">Это точные формулы без аппроксимации.</span><span class="sxs-lookup"><span data-stu-id="853d5-313">These are the exact formulas without approximation.</span></span> <span data-ttu-id="853d5-314">Все, что следует за этим документом, является производным от этих формул.</span><span class="sxs-lookup"><span data-stu-id="853d5-314">Everything that follows in this document is derived from these formulas.</span></span> <span data-ttu-id="853d5-315">В этом разделе рассматриваются следующие преобразования.</span><span class="sxs-lookup"><span data-stu-id="853d5-315">This section describes the following conversions:</span></span>

-   [<span data-ttu-id="853d5-316">Преобразование RGB888 в YUV 4:4:4</span><span class="sxs-lookup"><span data-stu-id="853d5-316">Converting RGB888 to YUV 4:4:4</span></span>](#converting-rgb888-to-yuv-444)
-   [<span data-ttu-id="853d5-317">Преобразование 8-разрядного YUV в RGB888</span><span class="sxs-lookup"><span data-stu-id="853d5-317">Converting 8-bit YUV to RGB888</span></span>](#converting-8-bit-yuv-to-rgb888)
-   [<span data-ttu-id="853d5-318">Преобразование 4:2:0 YUV в 4:2:2 YUV</span><span class="sxs-lookup"><span data-stu-id="853d5-318">Converting 4:2:0 YUV to 4:2:2 YUV</span></span>](#converting-420-yuv-to-422-yuv)
-   [<span data-ttu-id="853d5-319">Преобразование 4:2:2 YUV в 4:4:4 YUV</span><span class="sxs-lookup"><span data-stu-id="853d5-319">Converting 4:2:2 YUV to 4:4:4 YUV</span></span>](#converting-422-yuv-to-444-yuv)
-   [<span data-ttu-id="853d5-320">Преобразование 4:2:0 YUV в 4:4:4 YUV</span><span class="sxs-lookup"><span data-stu-id="853d5-320">Converting 4:2:0 YUV to 4:4:4 YUV</span></span>](#converting-420-yuv-to-444-yuv)

## <a name="converting-rgb888-to-yuv-444"></a><span data-ttu-id="853d5-321">Преобразование RGB888 в YUV 4:4:4</span><span class="sxs-lookup"><span data-stu-id="853d5-321">Converting RGB888 to YUV 4:4:4</span></span>

<span data-ttu-id="853d5-322">В случае входных данных RGB и 8-разрядных выходных данных BT. 601 YUV мы считаем, что формулы, приведенные в предыдущем разделе, могут быть примерно приблизительно ниже:</span><span class="sxs-lookup"><span data-stu-id="853d5-322">In the case of computer RGB input and 8-bit BT.601 YUV output, we believe that the formulas given in the previous section can be reasonably approximated by the following:</span></span>

``` syntax
Y = ( (  66 * R + 129 * G +  25 * B + 128) >> 8) +  16
U = ( ( -38 * R -  74 * G + 112 * B + 128) >> 8) + 128
V = ( ( 112 * R -  94 * G -  18 * B + 128) >> 8) + 128
```

<span data-ttu-id="853d5-323">Эти формулы создают 8-разрядные результаты с использованием коэффициентов, для которых требуется не более 8 разрядов (без знака).</span><span class="sxs-lookup"><span data-stu-id="853d5-323">These formulas produce 8-bit results using coefficients that require no more than 8 bits of (unsigned) precision.</span></span> <span data-ttu-id="853d5-324">Промежуточные результаты должны иметь до 16 бит точности.</span><span class="sxs-lookup"><span data-stu-id="853d5-324">Intermediate results will require up to 16 bits of precision.</span></span>

## <a name="converting-8-bit-yuv-to-rgb888"></a><span data-ttu-id="853d5-325">Преобразование 8-разрядного YUV в RGB888</span><span class="sxs-lookup"><span data-stu-id="853d5-325">Converting 8-bit YUV to RGB888</span></span>

<span data-ttu-id="853d5-326">Исходя из исходных формул RGB-YUV, один из них может наследовать следующие связи для BT. 601.</span><span class="sxs-lookup"><span data-stu-id="853d5-326">From the original RGB-to-YUV formulas, one can derive the following relationships for BT.601.</span></span>

``` syntax
Y = round( 0.256788 * R + 0.504129 * G + 0.097906 * B) +  16 
U = round(-0.148223 * R - 0.290993 * G + 0.439216 * B) + 128
V = round( 0.439216 * R - 0.367788 * G - 0.071427 * B) + 128
```

<span data-ttu-id="853d5-327">Поэтому, учитывая следующее:</span><span class="sxs-lookup"><span data-stu-id="853d5-327">Therefore, given:</span></span>

``` syntax
C = Y - 16
D = U - 128
E = V - 128
```

<span data-ttu-id="853d5-328">формулы для преобразования YUV в RGB могут быть производными следующим образом:</span><span class="sxs-lookup"><span data-stu-id="853d5-328">the formulas to convert YUV to RGB can be derived as follows:</span></span>

``` syntax
R = clip( round( 1.164383 * C                   + 1.596027 * E  ) )
G = clip( round( 1.164383 * C - (0.391762 * D) - (0.812968 * E) ) )
B = clip( round( 1.164383 * C +  2.017232 * D                   ) )
```

<span data-ttu-id="853d5-329">где `clip()` обозначает обрезку диапазона \[ 0.. 255 \] .</span><span class="sxs-lookup"><span data-stu-id="853d5-329">where `clip()` denotes clipping to a range of \[0..255\].</span></span> <span data-ttu-id="853d5-330">Мы считаем, что эти формулы могут быть достаточно приблизительными по следующему адресу:</span><span class="sxs-lookup"><span data-stu-id="853d5-330">We believe these formulas can be reasonably approximated by the following:</span></span>

``` syntax
R = clip(( 298 * C           + 409 * E + 128) >> 8)
G = clip(( 298 * C - 100 * D - 208 * E + 128) >> 8)
B = clip(( 298 * C + 516 * D           + 128) >> 8)
```

<span data-ttu-id="853d5-331">В этих формулах используются некоторые коэффициенты, для которых требуется более 8 бит точности для создания каждого 8-разрядного результата, а для промежуточных результатов потребуется более 16 разрядов точности.</span><span class="sxs-lookup"><span data-stu-id="853d5-331">These formulas use some coefficients that require more than 8 bits of precision to produce each 8-bit result, and intermediate results will require more than 16 bits of precision.</span></span>

<span data-ttu-id="853d5-332">Чтобы преобразовать 4:2:0 или 4:2:2 YUV в RGB, мы рекомендуем преобразовать данные YUV в 4:4:4 YUV, а затем преобразовать из 4:4:4 YUV в RGB.</span><span class="sxs-lookup"><span data-stu-id="853d5-332">To convert 4:2:0 or 4:2:2 YUV to RGB, we recommend converting the YUV data to 4:4:4 YUV, and then converting from 4:4:4 YUV to RGB.</span></span> <span data-ttu-id="853d5-333">В последующих разделах представлены некоторые методы преобразования форматов 4:2:0 и 4:2:2 в 4:4:4.</span><span class="sxs-lookup"><span data-stu-id="853d5-333">The sections that follow present some methods for converting 4:2:0 and 4:2:2 formats to 4:4:4.</span></span>

## <a name="converting-420-yuv-to-422-yuv"></a><span data-ttu-id="853d5-334">Преобразование 4:2:0 YUV в 4:2:2 YUV</span><span class="sxs-lookup"><span data-stu-id="853d5-334">Converting 4:2:0 YUV to 4:2:2 YUV</span></span>

<span data-ttu-id="853d5-335">Преобразование 4:2:0 YUV в 4:2:2 YUV требует вертикального преобразования с коэффициентом 2.</span><span class="sxs-lookup"><span data-stu-id="853d5-335">Converting 4:2:0 YUV to 4:2:2 YUV requires vertical upconversion by a factor of two.</span></span> <span data-ttu-id="853d5-336">В этом разделе описывается пример метода для выполнения преобразования.</span><span class="sxs-lookup"><span data-stu-id="853d5-336">This section describes an example method for performing the upconversion.</span></span> <span data-ttu-id="853d5-337">В методе предполагается, что видеоролики находятся в виде последовательного сканирования.</span><span class="sxs-lookup"><span data-stu-id="853d5-337">The method assumes that the video pictures are progressive scan.</span></span>

> [!Note]  
> <span data-ttu-id="853d5-338">В процессе преобразования просмотра с 4:2:0 по 4:2:2 возникают нетипичные проблемы, которые трудно реализовать.</span><span class="sxs-lookup"><span data-stu-id="853d5-338">The 4:2:0 to 4:2:2 interlaced scan conversion process presents atypical problems and is difficult to implement.</span></span> <span data-ttu-id="853d5-339">В этой статье не рассматриваются проблемы преобразования с чередованием развертки с 4:2:0 на 4:2:2.</span><span class="sxs-lookup"><span data-stu-id="853d5-339">This article does not address the issue of converting interlaced scan from 4:2:0 to 4:2:2.</span></span>

 

<span data-ttu-id="853d5-340">Позвольте, чтобы каждая вертикальная строка входных образцов чрома была массивом `Cin[]` в диапазоне от 0 до N – 1.</span><span class="sxs-lookup"><span data-stu-id="853d5-340">Let each vertical line of input chroma samples be an array `Cin[]` that ranges from 0 to N - 1.</span></span> <span data-ttu-id="853d5-341">Соответствующая вертикальная линия на выходном изображении будет массивом в `Cout[]` диапазоне от 0 до 2n-1.</span><span class="sxs-lookup"><span data-stu-id="853d5-341">The corresponding vertical line on the output image will be an array `Cout[]` that ranges from 0 to 2N - 1.</span></span> <span data-ttu-id="853d5-342">Чтобы преобразовать каждую вертикальную линию, выполните следующую процедуру:</span><span class="sxs-lookup"><span data-stu-id="853d5-342">To convert each vertical line, perform the following process:</span></span>

``` syntax
Cout[0]     = Cin[0];
Cout[1]     = clip((9 * (Cin[0] + Cin[1]) - (Cin[0] + Cin[2]) + 8) >> 4);
Cout[2]     = Cin[1];
Cout[3]     = clip((9 * (Cin[1] + Cin[2]) - (Cin[0] + Cin[3]) + 8) >> 4);
Cout[4]     = Cin[2]
Cout[5]     = clip((9 * (Cin[2] + Cin[3]) - (Cin[1] + Cin[4]) + 8) >> 4);
...
Cout[2*i]   = Cin[i]
Cout[2*i+1] = clip((9 * (Cin[i] + Cin[i+1]) - (Cin[i-1] + Cin[i+2]) + 8) >> 4);
...
Cout[2*N-3] = clip((9 * (Cin[N-2] + Cin[N-1]) - (Cin[N-3] + Cin[N-1]) + 8) >> 4);
Cout[2*N-2] = Cin[N-1];
Cout[2*N-1] = clip((9 * (Cin[N-1] + Cin[N-1]) - (Cin[N-2] + Cin[N-1]) + 8) >> 4);
```

<span data-ttu-id="853d5-343">где Clip () обозначает обрезание до диапазона \[ 0.. 255 \] .</span><span class="sxs-lookup"><span data-stu-id="853d5-343">where clip() denotes clipping to a range of \[0..255\].</span></span>

> [!Note]  
> <span data-ttu-id="853d5-344">Уравнения для обработки границ могут быть математически упрощены.</span><span class="sxs-lookup"><span data-stu-id="853d5-344">The equations for handling the edges can be mathematically simplified.</span></span> <span data-ttu-id="853d5-345">Они показаны в этой форме, чтобы проиллюстрировать эффект фиксации на краях изображения.</span><span class="sxs-lookup"><span data-stu-id="853d5-345">They are shown in this form to illustrate the clamping effect at the edges of the picture.</span></span>

 

<span data-ttu-id="853d5-346">По сути, этот метод вычисляет каждое отсутствующее значение путем интерполяции кривой по четырем соседним пикселям, с взвешенным приближением к значениям двух ближайших пикселов (рис. 11).</span><span class="sxs-lookup"><span data-stu-id="853d5-346">In effect, this method calculates each missing value by interpolating the curve over the four adjacent pixels, weighted toward the values of the two nearest pixels (Figure 11).</span></span> <span data-ttu-id="853d5-347">Конкретный метод интерполяции, используемый в этом примере, создает отсутствующие примеры на позициях половинного целого числа с помощью хорошо известного метода, именуемого Catmull-Rom интерполяции, также известного как интерполяция свертки в кубических выпусках.</span><span class="sxs-lookup"><span data-stu-id="853d5-347">The specific interpolation method used in this example generates missing samples at half-integer positions using a well-known method called Catmull-Rom interpolation, also known as cubic convolution interpolation.</span></span>

![рис. 11.](images/yuvformats14.gif)

<span data-ttu-id="853d5-350">В терминах обработки сигнала вертикальное преобразование в идеале должно включать в себя компенсацию сдвига на шаг с учетом вертикального смещения (относительно сетки выборке 4:2:2) между расположениями образцов 4:2:0 и расположением всех остальных образцов 4:2:2.</span><span class="sxs-lookup"><span data-stu-id="853d5-350">In signal processing terms, the vertical upconversion should ideally include a phase shift compensation to account for the half-pixel vertical offset (relative to the output 4:2:2 sampling grid) between the locations of the 4:2:0 sample lines and the location of every other 4:2:2 sample line.</span></span> <span data-ttu-id="853d5-351">Однако введение этого смещения приведет к увеличению объема обработки, необходимого для создания образцов, и сделает невозможным восстановление исходных образцов 4:2:0 из изображения с изображением 4:2:2.</span><span class="sxs-lookup"><span data-stu-id="853d5-351">However, introducing this offset would increase the amount of processing required to generate the samples, and make it impossible to reconstruct the original 4:2:0 samples from the upsampled 4:2:2 image.</span></span> <span data-ttu-id="853d5-352">Это также сделает невозможным декодирование видео непосредственно в поверхности 4:2:2, а затем использовать эти поверхности как справочные рисунки для декодирования последующих изображений в потоке.</span><span class="sxs-lookup"><span data-stu-id="853d5-352">It would also make it impossible to decode video directly into 4:2:2 surfaces and then use those surfaces as reference pictures for decoding subsequent pictures in the stream.</span></span> <span data-ttu-id="853d5-353">Таким образом, предоставленный здесь метод не учитывает точное вертикальное выравнивание образцов.</span><span class="sxs-lookup"><span data-stu-id="853d5-353">Therefore, the method provided here does not take into account the precise vertical alignment of the samples.</span></span> <span data-ttu-id="853d5-354">Это, вероятно, не является визуально вредоносным при достаточно высоком разрешении рисунков.</span><span class="sxs-lookup"><span data-stu-id="853d5-354">Doing so is probably not visually harmful at reasonably high picture resolutions.</span></span>

<span data-ttu-id="853d5-355">Если вы начинаете с 4:2:0 видео, которое использует сетку выборки, определенную в видео H. 261, H. 263 или MPEG-1, фаза выводимых 4:2:2 чрома также будет смещена по горизонталому смещению на половину пикселя относительно расстояния в сетке выборки яркости (смещение в четвертом пикселе относительно интервала в сетке выборки 4:2:2 чрома).</span><span class="sxs-lookup"><span data-stu-id="853d5-355">If you start with 4:2:0 video that uses the sampling grid defined in H.261, H.263, or MPEG-1 video, the phase of the output 4:2:2 chroma samples will also be shifted by a half-pixel horizontal offset relative to the spacing on the luma sampling grid (a quarter-pixel offset relative to the spacing of the 4:2:2 chroma sampling grid).</span></span> <span data-ttu-id="853d5-356">Тем не менее, формат MPEG-2 видео 4:2:0, скорее всего, более широко используется на компьютерах и не страдает от этой проблемы.</span><span class="sxs-lookup"><span data-stu-id="853d5-356">However, the MPEG-2 form of 4:2:0 video is probably more commonly used on PCs and does not suffer from this problem.</span></span> <span data-ttu-id="853d5-357">Более того, различие, вероятно, не является визуально вредоносным при достаточно высоком разрешении рисунков.</span><span class="sxs-lookup"><span data-stu-id="853d5-357">Moreover, the distinction is probably not visually harmful at reasonably high picture resolutions.</span></span> <span data-ttu-id="853d5-358">Попытка исправить эту проблему вызовет те же проблемы, которые обсуждаются для вертикального смещения.</span><span class="sxs-lookup"><span data-stu-id="853d5-358">Trying to correct for this problem would create the same sort of problems discussed for the vertical phase offset.</span></span>

## <a name="converting-422-yuv-to-444-yuv"></a><span data-ttu-id="853d5-359">Преобразование 4:2:2 YUV в 4:4:4 YUV</span><span class="sxs-lookup"><span data-stu-id="853d5-359">Converting 4:2:2 YUV to 4:4:4 YUV</span></span>

<span data-ttu-id="853d5-360">Преобразование 4:2:2 YUV в 4:4:4 YUV требует горизонтального преобразования с коэффициентом 2.</span><span class="sxs-lookup"><span data-stu-id="853d5-360">Converting 4:2:2 YUV to 4:4:4 YUV requires horizontal upconversion by a factor of two.</span></span> <span data-ttu-id="853d5-361">Метод, описанный ранее для вертикального преобразования, можно также применить к горизонтальному преобразованию.</span><span class="sxs-lookup"><span data-stu-id="853d5-361">The method described previously for vertical upconversion can also be applied to horizontal upconversion.</span></span> <span data-ttu-id="853d5-362">Для видео MPEG-2 и ITU-R BT. 601 этот метод будет создавать образцы с правильным выравниванием этапа.</span><span class="sxs-lookup"><span data-stu-id="853d5-362">For MPEG-2 and ITU-R BT.601 video, this method will produce samples with the correct phase alignment.</span></span>

## <a name="converting-420-yuv-to-444-yuv"></a><span data-ttu-id="853d5-363">Преобразование 4:2:0 YUV в 4:4:4 YUV</span><span class="sxs-lookup"><span data-stu-id="853d5-363">Converting 4:2:0 YUV to 4:4:4 YUV</span></span>

<span data-ttu-id="853d5-364">Чтобы преобразовать 4:2:0 YUV в 4:4:4 YUV, можно просто выполнить два описанных выше метода.</span><span class="sxs-lookup"><span data-stu-id="853d5-364">To convert 4:2:0 YUV to 4:4:4 YUV, you can simply follow the two methods described previously.</span></span> <span data-ttu-id="853d5-365">Преобразуйте образ 4:2:0 в 4:2:2, а затем преобразуйте образ 4:2:2 в 4:4:4.</span><span class="sxs-lookup"><span data-stu-id="853d5-365">Convert the 4:2:0 image to 4:2:2, and then convert the 4:2:2 image to 4:4:4.</span></span> <span data-ttu-id="853d5-366">Можно также переключить порядок двух процессов преобразования, так как порядок операций не имеет значения для визуального качества результата.</span><span class="sxs-lookup"><span data-stu-id="853d5-366">You can also switch the order of the two upconversion processes, as the order of operation does not really matter to the visual quality of the result.</span></span>

## <a name="other-yuv-formats"></a><span data-ttu-id="853d5-367">Другие форматы YUV</span><span class="sxs-lookup"><span data-stu-id="853d5-367">Other YUV Formats</span></span>

<span data-ttu-id="853d5-368">Ниже приведены некоторые другие, менее распространенные форматы YUV.</span><span class="sxs-lookup"><span data-stu-id="853d5-368">Some other, less common YUV formats include the following:</span></span>

-   <span data-ttu-id="853d5-369">AI44 — это формат палеттизед YUV с 8 битами на выборку.</span><span class="sxs-lookup"><span data-stu-id="853d5-369">AI44 is a palettized YUV format with 8 bits per sample.</span></span> <span data-ttu-id="853d5-370">Каждый пример содержит индекс в 4 наиболее значимых битах (МСБС) и альфа-значение в 4 самых значимых битах (Лсбс).</span><span class="sxs-lookup"><span data-stu-id="853d5-370">Each sample contains an index in the 4 most significant bits (MSBs) and an alpha value in the 4 least significant bits (LSBs).</span></span> <span data-ttu-id="853d5-371">Индекс ссылается на массив записей в палитре YUV, который должен быть определен в типе мультимедиа для формата.</span><span class="sxs-lookup"><span data-stu-id="853d5-371">The index refers to an array of YUV palette entries, which must be defined in the media type for the format.</span></span> <span data-ttu-id="853d5-372">Этот формат в основном используется для изображений подизображений.</span><span class="sxs-lookup"><span data-stu-id="853d5-372">This format is primarily used for subpicture images.</span></span>
-   <span data-ttu-id="853d5-373">NV11 имеет формат 4:1:1 с 12 битами на пиксель.</span><span class="sxs-lookup"><span data-stu-id="853d5-373">NV11 is a 4:1:1 planar format with 12 bits per pixel.</span></span> <span data-ttu-id="853d5-374">Примеры Y отображаются в памяти первыми.</span><span class="sxs-lookup"><span data-stu-id="853d5-374">The Y samples appear first in memory.</span></span> <span data-ttu-id="853d5-375">За плоскостью Y следует массив из упакованных образцов U (CB) и V (CR).</span><span class="sxs-lookup"><span data-stu-id="853d5-375">The Y plane is followed by an array of packed U (Cb) and V (Cr) samples.</span></span> <span data-ttu-id="853d5-376">Если комбинированный массив U-V адресован как массив значений **слов** с прямым порядком байтов, примеры U содержатся в Лсбс каждого **слова**, а примеры V содержатся в МСБС.</span><span class="sxs-lookup"><span data-stu-id="853d5-376">When the combined U-V array is addressed as an array of little-endian **WORD** values, the U samples are contained in the LSBs of each **WORD**, and the V samples are contained in the MSBs.</span></span> <span data-ttu-id="853d5-377">(Эта структура памяти похожа на NV12, хотя выборка чрома отличается.)</span><span class="sxs-lookup"><span data-stu-id="853d5-377">(This memory layout is similar to NV12 although the chroma sampling is different.)</span></span>
-   <span data-ttu-id="853d5-378">Y41P является упакованным форматом 4:1:1, где каждый четвертый пиксел по горизонтали выдается в один и тот же интервал.</span><span class="sxs-lookup"><span data-stu-id="853d5-378">Y41P is a 4:1:1 packed format, with U and V sampled every fourth pixel horizontally.</span></span> <span data-ttu-id="853d5-379">Каждый макропиксел содержит 8 пикселей в трех байтах и следующий формат байта: `U0 Y0 V0 Y1    U4 Y2 V4 Y3    Y4 Y5 Y6 Y7`</span><span class="sxs-lookup"><span data-stu-id="853d5-379">Each macropixel contains 8 pixels in three bytes, with the following byte layout: `U0 Y0 V0 Y1    U4 Y2 V4 Y3    Y4 Y5 Y6 Y7`</span></span>
-   <span data-ttu-id="853d5-380">Y41T идентичен Y41P, за исключением наименее значимого бита каждого из значений Y указывает ключ чрома (0 = прозрачный, 1 = непрозрачный).</span><span class="sxs-lookup"><span data-stu-id="853d5-380">Y41T is identical to Y41P, except the least-significant bit of each Y sample specifies the chroma key (0 = transparent, 1 = opaque).</span></span>
-   <span data-ttu-id="853d5-381">Y42T идентичен UYVY, за исключением наименее значимого бита каждого из значений Y указывает ключ чрома (0 = прозрачный, 1 = непрозрачный).</span><span class="sxs-lookup"><span data-stu-id="853d5-381">Y42T is identical to UYVY, except the least-significant bit of each Y sample specifies the chroma key (0 = transparent, 1 = opaque).</span></span>
-   <span data-ttu-id="853d5-382">ИВЮ эквивалентен ЮИВ, за исключением случаев, когда вы и V переключаются между примерами.</span><span class="sxs-lookup"><span data-stu-id="853d5-382">YVYU is equivalent to YUYV except the U and V samples are swapped.</span></span>

## <a name="identifying-yuv-formats-in-media-foundation"></a><span data-ttu-id="853d5-383">Определение форматов YUV в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="853d5-383">Identifying YUV Formats in Media Foundation</span></span>

<span data-ttu-id="853d5-384">Каждый из форматов YUV, описанных в этой статье, имеет назначенный код FOURCC.</span><span class="sxs-lookup"><span data-stu-id="853d5-384">Each of the YUV formats described in this article has an assigned FOURCC code.</span></span> <span data-ttu-id="853d5-385">Код FOURCC — это 32-разрядное целое число без знака, которое создается путем сцепления четырех символов ASCII.</span><span class="sxs-lookup"><span data-stu-id="853d5-385">A FOURCC code is a 32-bit unsigned integer that is created by concatenating four ASCII characters.</span></span>

<span data-ttu-id="853d5-386">Существуют различные макросы C/C++, упрощающие объявление значений FOURCC в исходном коде.</span><span class="sxs-lookup"><span data-stu-id="853d5-386">There are various C/C++ macros that make it easier to declare FOURCC values in source code.</span></span> <span data-ttu-id="853d5-387">Например, макрос **макефауркк** объявляется в ммсистем. h, а макрос **FCC** объявляется в авирифф. h.</span><span class="sxs-lookup"><span data-stu-id="853d5-387">For example, the **MAKEFOURCC** macro is declared in Mmsystem.h, and the **FCC** macro is declared in Aviriff.h.</span></span> <span data-ttu-id="853d5-388">Используйте их следующим образом:</span><span class="sxs-lookup"><span data-stu-id="853d5-388">Use them as follows:</span></span>

``` syntax
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
```

<span data-ttu-id="853d5-389">Кроме того, можно объявить код FOURCC непосредственно в виде строкового литерала, просто отменив порядок символов.</span><span class="sxs-lookup"><span data-stu-id="853d5-389">You can also declare a FOURCC code directly as a string literal simply by reversing the order of the characters.</span></span> <span data-ttu-id="853d5-390">Пример:</span><span class="sxs-lookup"><span data-stu-id="853d5-390">For example:</span></span>

``` syntax
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'
```

<span data-ttu-id="853d5-391">Обратный порядок необходим, так как операционная система Windows использует архитектуру с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="853d5-391">Reversing the order is necessary because the Windows operating system uses a little-endian architecture.</span></span> <span data-ttu-id="853d5-392">' Y ' = 0x59, ' U ' = 0x55, и ' 2 ' = 0x32, поэтому ' 2YUY ' является 0x32595559.</span><span class="sxs-lookup"><span data-stu-id="853d5-392">'Y' = 0x59, 'U' = 0x55, and '2' = 0x32, so '2YUY' is 0x32595559.</span></span>

<span data-ttu-id="853d5-393">В Media Foundation форматы идентифицируются по идентификатору GUID основного типа и идентификатору GUID подтипа.</span><span class="sxs-lookup"><span data-stu-id="853d5-393">In Media Foundation, formats are identified by a major type GUID and a subtype GUID.</span></span> <span data-ttu-id="853d5-394">Основной тип видеоформатов компьютера всегда Мфмедиатипе \_ видео.</span><span class="sxs-lookup"><span data-stu-id="853d5-394">The major type for computer video formats is always MFMediaType\_Video .</span></span> <span data-ttu-id="853d5-395">Подтип может быть создан путем сопоставления кода FOURCC с идентификатором GUID, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="853d5-395">The subtype can be constructed by mapping the FOURCC code to a GUID, as follows:</span></span>

``` syntax
XXXXXXXX-0000-0010-8000-00AA00389B71 
```

<span data-ttu-id="853d5-396">где `XXXXXXXX` — код FourCC.</span><span class="sxs-lookup"><span data-stu-id="853d5-396">where `XXXXXXXX` is the FOURCC code.</span></span> <span data-ttu-id="853d5-397">Таким образом, идентификатор GUID подтипа для YUY2:</span><span class="sxs-lookup"><span data-stu-id="853d5-397">Thus, the subtype GUID for YUY2 is:</span></span>

``` syntax
32595559-0000-0010-8000-00AA00389B71 
```

<span data-ttu-id="853d5-398">Константы для наиболее распространенных идентификаторов GUID формата YUV определены в файле заголовка мфапи. h.</span><span class="sxs-lookup"><span data-stu-id="853d5-398">Constants for the most common YUV format GUIDs are defined in the header file mfapi.h.</span></span> <span data-ttu-id="853d5-399">Список этих констант см. в разделе [GUID подтипа видео](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="853d5-399">For a list of these constants, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="853d5-400">См. также</span><span class="sxs-lookup"><span data-stu-id="853d5-400">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="853d5-401">Видео о YUV</span><span class="sxs-lookup"><span data-stu-id="853d5-401">About YUV Video</span></span>](about-yuv-video.md)
</dt> <dt>

[<span data-ttu-id="853d5-402">Типы видеоклипов</span><span class="sxs-lookup"><span data-stu-id="853d5-402">Video Media Types</span></span>](video-media-types.md)
</dt> </dl>

 

 



