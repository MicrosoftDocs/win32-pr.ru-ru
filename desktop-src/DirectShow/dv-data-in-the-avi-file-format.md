---
description: Данные DV в формате AVI
ms.assetid: ae1ec184-afc3-4ec1-9b92-f53656293446
title: Данные DV в формате AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65f1393bfe4bbee4d080d90755f33cfa7f4a7fa4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495546"
---
# <a name="dv-data-in-the-avi-file-format"></a><span data-ttu-id="1177f-103">Данные DV в формате AVI</span><span class="sxs-lookup"><span data-stu-id="1177f-103">DV Data in the AVI File Format</span></span>

<span data-ttu-id="1177f-104">Корпорация Майкрософт указала формат хранения данных цифрового видео (DV) в AVI-файлах.</span><span class="sxs-lookup"><span data-stu-id="1177f-104">Microsoft has specified the format for storage of digital video (DV) data in AVI files.</span></span> <span data-ttu-id="1177f-105">Соответствие этой спецификации обеспечит совместимость файлов AVI, созданных в этом формате, с будущими версиями архитектуры Digital Video для Виндовсплатформ.</span><span class="sxs-lookup"><span data-stu-id="1177f-105">Conforming to this specification will ensure that the AVI files authored in this format will be compatible with future versions of the DirectShow digital video architecture for the Windowsplatform.</span></span>

<span data-ttu-id="1177f-106">В этой статье описывается формат файлов AVI, содержащих данные DV.</span><span class="sxs-lookup"><span data-stu-id="1177f-106">This article describes the format of AVI files containing DV data.</span></span> <span data-ttu-id="1177f-107">Определенные Фаурккс (коды из четырех символов) для потоков с чередованием DV и DV Streaming/декомпрессора.</span><span class="sxs-lookup"><span data-stu-id="1177f-107">Specific FOURCCs (four-character codes) for interleaved DV data streams and DV compressor/decompressor stream handlers are defined.</span></span> <span data-ttu-id="1177f-108">Структура формата потока для DV-данных определена.</span><span class="sxs-lookup"><span data-stu-id="1177f-108">The stream format structure for DV data is defined.</span></span> <span data-ttu-id="1177f-109">Указаны два способа хранения данных DV в формате AVI.</span><span class="sxs-lookup"><span data-stu-id="1177f-109">Specifications for two methods of storing DV data in the AVI file format are specified.</span></span>

<span data-ttu-id="1177f-110">Предполагается, что читатель знаком с форматом данных DV.</span><span class="sxs-lookup"><span data-stu-id="1177f-110">It is assumed that the reader is familiar with the DV data format.</span></span> <span data-ttu-id="1177f-111">(Этот формат определяется в *спецификации цифровой видеомагнитофона*, также называемой синей книгой.)</span><span class="sxs-lookup"><span data-stu-id="1177f-111">(This format is defined in the *Specification of Consumer-use Digital VCRs*, also called the Blue Book.)</span></span>

<span data-ttu-id="1177f-112">Существует два типа видеофайлов в формате AVI: AVI-файлы, которые содержат один поток данных DV, называемый файлами *типа 1* ; и AVI-файлы, содержащие DV-видео в виде потока VID и DV Audio как потоки "аудс", называются файлами *типа 2* .</span><span class="sxs-lookup"><span data-stu-id="1177f-112">There are two types of DV AVI files: AVI files that contain one DV data stream, called *type-1* files; and AVI files that contain DV video as a 'vids' stream and DV audio as 'auds' streams, called *type-2* files.</span></span>

<span data-ttu-id="1177f-113">**AVI-файлы, содержащие один поток данных DV (тип 1)**</span><span class="sxs-lookup"><span data-stu-id="1177f-113">**AVI Files Containing One DV Data Stream (Type-1)**</span></span>

<span data-ttu-id="1177f-114">Чередующиеся DV-данные могут храниться в собственном формате в виде одного потока в файле AVI Metallica.</span><span class="sxs-lookup"><span data-stu-id="1177f-114">Interleaved DV data can be stored in its native format as a single stream within an AVI RIFF file.</span></span> <span data-ttu-id="1177f-115">Это имеет преимущество использования минимального объема хранилища данных для DV.</span><span class="sxs-lookup"><span data-stu-id="1177f-115">This has the advantage of using the minimum amount of data storage for DV.</span></span> <span data-ttu-id="1177f-116">Основное недостатком является то, что этот формат файла не обратно совместим с видео для Windows, так как он не содержит видео «VID» или «аудс».</span><span class="sxs-lookup"><span data-stu-id="1177f-116">The primary disadvantage is that this file format is not backward-compatible with Video for Windows, because it doesn't contain either a video 'vids' or an audio 'auds' stream.</span></span> <span data-ttu-id="1177f-117">Поддержка обеспечивается для потока с чередованием DV с использованием видеофильтров [DV мультиплексор](dv-muxer-filter.md) и [DV](dv-splitter-filter.md) , поставляемых с DirectShow.</span><span class="sxs-lookup"><span data-stu-id="1177f-117">Support is provided for the interleaved DV stream through the [DV Muxer](dv-muxer-filter.md) and [DV Splitter](dv-splitter-filter.md) filters provided with DirectShow.</span></span>

<span data-ttu-id="1177f-118">DV-данные могут храниться в одном потоке в файле AVI Metallica путем указания иавс (с чередованием аудио-и видеопотоков) FOURCC (код с четырьмя символами) в элементе **фкктипе** , а также любого из двхд в элементе **двсл** в фрагменте заголовка потока фаурккс.</span><span class="sxs-lookup"><span data-stu-id="1177f-118">DV data can be stored in a single stream within an AVI RIFF file by specifying the 'iavs' (interleaved audio and video stream) FOURCC (four-character code) in the **fccType** member and either of the 'dvsd', 'dvhd', or 'dvsl' FOURCCs in the **fccHandler** member of the 'strh' stream header chunk.</span></span> <span data-ttu-id="1177f-119">Количество кадров в секунду для потока видео должно быть указано в элементах **дврате** и **двскале** , а общее число видеоблоков в блоке "Мови" в элементе **двленгс** .</span><span class="sxs-lookup"><span data-stu-id="1177f-119">The frames per second of the video stream must be specified in the **dwRate** and **dwScale** members and the total number of video blocks in the 'movi' chunk in the **dwLength** member.</span></span>

<span data-ttu-id="1177f-120">Обработчик потока "двсд" FOURCC указывает, что данные DV определены в части 2 *спецификации цифровых видеомагнитофонов*.</span><span class="sxs-lookup"><span data-stu-id="1177f-120">The 'dvsd' stream handler FOURCC specifies that the DV data is as defined in Part 2 of the *Specification of Consumer-use Digital VCRs*.</span></span> <span data-ttu-id="1177f-121">Видео имеет формат 525 строк с частотой 29,97 Гц (525-60) или 625 строки с частотой 25,00 Гц (625-50).</span><span class="sxs-lookup"><span data-stu-id="1177f-121">Video is in the format of 525 lines at 29.97 Hz (525-60) or 625 lines at 25.00 Hz (625-50).</span></span>

<span data-ttu-id="1177f-122">Обработчик потока "двхд" FOURCC указывает, что данные DV определены в части 3 *спецификации цифровых видеомагнитофонов*.</span><span class="sxs-lookup"><span data-stu-id="1177f-122">The 'dvhd' stream handler FOURCC specifies that the DV data is as defined in Part 3 of the *Specification of Consumer-use Digital VCRs*.</span></span> <span data-ttu-id="1177f-123">Видео имеет формат 1125 строк с частотой 30,00 Гц (1125-60) или 1250 строки с частотой 25,00 Гц (1250-50).</span><span class="sxs-lookup"><span data-stu-id="1177f-123">Video is in the format of 1125 lines at 30.00 Hz (1125-60) or 1250 lines at 25.00 Hz (1250-50).</span></span>

<span data-ttu-id="1177f-124">Обработчик потока "двсл" FOURCC указывает, что данные DV определены в части 6 *спецификации цифровых видеомагнитофонов*.</span><span class="sxs-lookup"><span data-stu-id="1177f-124">The 'dvsl' stream handler FOURCC specifies that the DV data is as defined in Part 6 of *Specification of Consumer-use Digital VCRs*.</span></span> <span data-ttu-id="1177f-125">Видео имеет формат SD (Security) с высоким уровнем сжатия (SDL).</span><span class="sxs-lookup"><span data-stu-id="1177f-125">Video is in the format of high-compression SD (SDL).</span></span>

> [!Note]  
> <span data-ttu-id="1177f-126">Оставшаяся часть этой статьи содержит определения для потоков "двсд".</span><span class="sxs-lookup"><span data-stu-id="1177f-126">The remainder of this article provides definitions for 'dvsd' streams.</span></span>

 

<span data-ttu-id="1177f-127">После фрагмента заголовка потока должен следовать фрагмент формата потока [**двинфо**](/windows/desktop/api/strmif/ns-strmif-dvinfo) .</span><span class="sxs-lookup"><span data-stu-id="1177f-127">The stream header chunk must be followed by a [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) stream format chunk.</span></span>

<span data-ttu-id="1177f-128">Фактические данные DV хранятся \# \# в виде фрагментов "DC" в блоке "Мови" ( \# \# в формате представляет идентификатор потока).</span><span class="sxs-lookup"><span data-stu-id="1177f-128">The actual DV data is stored as '\#\#dc' chunks in the 'movi' chunk (the \#\# in the format represents the stream identifier).</span></span> <span data-ttu-id="1177f-129">Каждый блок содержит один кадр данных: 10 или 12 цифр DV DIF для систем 525-60 или 625-50 соответственно.</span><span class="sxs-lookup"><span data-stu-id="1177f-129">Each chunk contains one frame of data, either 10 or 12 DV DIF sequences for 525-60 or 625-50 systems, respectively.</span></span> <span data-ttu-id="1177f-130">Формат последовательности DIF DV SD (' двсд '), определяемый в части 2 *спецификации цифровой видеомагнитофона*.</span><span class="sxs-lookup"><span data-stu-id="1177f-130">The DV SD ('dvsd') DIF sequence format is defined in Part 2 of the *Specification of Consumer-use Digital VCRs*.</span></span>

<span data-ttu-id="1177f-131">В следующем примере показана форма AIFF Metallica для файла AVI с одним потоком данных DV, развернутой с помощью завершенных фрагментов заголовка.</span><span class="sxs-lookup"><span data-stu-id="1177f-131">The following example shows the AIFF RIFF form for an AVI file with one DV data stream, expanded with completed header chunks.</span></span>


```C++
00000000 RIFF (0FAE35D4) 'AVI '
0000000C     LIST (00000106) 'hdrl'
00000018         avih (00000038)
                     dwMicroSecPerFrame    : 33367
                     dwMaxBytesPerSec      : 3728000
                     dwPaddingGranularity  : 0
                     dwFlags               : 0x810 HASINDEX | TRUSTCKTYPE
                     dwTotalFrames         : 2192
                     dwInitialFrames       : 0
                     dwStreams             : 1
                     dwSuggestedBufferSize : 120000
                     dwWidth               : 720
                     dwHeight              : 480
                     dwReserved            : 0x0
00000058         LIST (0000006C) 'strl'
00000064             strh (00000038)
                         fccType               : 'iavs'
                         fccHandler            : 'dvsd'
                         dwFlags               : 0x0
                         wPriority             : 0
                         wLanguage             : 0x0 undefined
                         dwInitialFrames       : 0
                         dwScale               : 100 (29.970 Frames/Sec)
                         dwRate                : 2997
                         dwStart               : 0
                         dwLength              : 2192
                         dwSuggestedBufferSize : 120000
                         dwQuality             : 0
                         dwSampleSize          : 0
                         rcFrame               : 0,0,720,480
000000A4             strf (00000020)
                         dwDVAAuxSrc     : 0x........
                         dwDVAAuxCtl     : 0x........
                         dwDVAAuxSrc1    : 0x........
                         dwDVAAuxCtl1    : 0x........
                         dwDVVAuxSrc     : 0x........
                         dwDVVAuxCtl     : 0x........
                         dwDVReserved[2] : 0,0
000000CC     LIST (0FADAC00) 'movi'
0FADACD4     idx1 (00008900)
```



<span data-ttu-id="1177f-132">**AVI-файлы, содержащие видеопотоки DV и DV Audio (тип 2)**</span><span class="sxs-lookup"><span data-stu-id="1177f-132">**AVI Files Containing DV Video and DV Audio Streams (Type-2)**</span></span>

<span data-ttu-id="1177f-133">Чередующиеся DV-данные можно разделить на видеопоток, а один — на четыре звуковых потока в файле AVI Metallica.</span><span class="sxs-lookup"><span data-stu-id="1177f-133">Interleaved DV data can be split into a video stream and one to four audio streams within an AVI RIFF file.</span></span> <span data-ttu-id="1177f-134">Это имеет преимущество обратной совместимости с видео для Windows, так как оно содержит поток стандартного видео "VID" и, по крайней мере, один стандартный поток звука "аудс", основной недостаток заключается в том, что этот формат файла требует, чтобы аудиоданные были избыточно сохранены в виде звуковых потоков.</span><span class="sxs-lookup"><span data-stu-id="1177f-134">This has the advantage of being backward-compatible with Video for Windows, because it contains a standard video 'vids' stream and at least one standard audio 'auds' stream The primary disadvantage is that this file format requires the audio data to be redundantly stored as audio streams.</span></span> <span data-ttu-id="1177f-135">Поток "Video" фактически является машинным потоком данных с чередованием.</span><span class="sxs-lookup"><span data-stu-id="1177f-135">The "video" stream is actually the native interleaved DV data stream.</span></span> <span data-ttu-id="1177f-136">Однако в качестве стандартного потока VID с типом обработчика "двсд" используется [видеодекодер DV](dv-video-decoder-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="1177f-136">However, as a standard 'vids' stream with a handler type of 'dvsd', the [DV Video Decoder](dv-video-decoder-filter.md) is used.</span></span> <span data-ttu-id="1177f-137">Этот формат также требует использования фильтра [разделителя DV](dv-splitter-filter.md) для разбиения "записанных" файлов перед их записью в виде AVI.</span><span class="sxs-lookup"><span data-stu-id="1177f-137">This format also requires using the [DV Splitter](dv-splitter-filter.md) filter to split "captured" files before writing them as AVI files.</span></span>

<span data-ttu-id="1177f-138">DV-данные могут храниться в виде видеопотока с отдельным числом звуковых потоков в файле AVI Metallica.</span><span class="sxs-lookup"><span data-stu-id="1177f-138">DV data can be stored as a video stream with a separate number of audio streams in an AVI RIFF file.</span></span> <span data-ttu-id="1177f-139">Поток видео указывается с помощью заголовка стандартного видеопотока (значение элемента **фкктипе** — "VID").</span><span class="sxs-lookup"><span data-stu-id="1177f-139">The video stream is specified with a standard video stream header (the **fccType** member value is 'vids').</span></span> <span data-ttu-id="1177f-140">Элемент **фкчандлер** указан как "двсд", "двхд" или "двсл".</span><span class="sxs-lookup"><span data-stu-id="1177f-140">The **fccHandler** member is specified as 'dvsd', 'dvhd', or 'dvsl'.</span></span> <span data-ttu-id="1177f-141">Количество кадров в секунду для потока видео должно быть указано в элементах **дврате** и **двскале** , а общее число видеоблоков в блоке "Мови" в элементе **двленгс** .</span><span class="sxs-lookup"><span data-stu-id="1177f-141">The frames per second of the video stream must be specified in the **dwRate** and **dwScale** members and the total number of video blocks in the 'movi' chunk in the **dwLength** member.</span></span>

<span data-ttu-id="1177f-142">В этом файле AVI, который содержит DV-видео в виде потока VID и DV Audio в виде потоков "аудс" DV, фрагмент формата видеопотока является стандартной структурой [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="1177f-142">In this AVI file containing DV video as a 'vids' stream and DV audio as 'auds' streams form of DV, the video stream format chunk is a standard [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span> <span data-ttu-id="1177f-143">Фрагмент формата потока можно дополнительно расширить для включения фрагмента [**двинфо**](/windows/desktop/api/strmif/ns-strmif-dvinfo) , увеличивая размер фрагмента в формате потока от 40 байт (размер структуры **битмапинфохеадер** ) до 72 байт (размер **битмапинфохеадер** плюс **двинфо** структуры) и сразу после структуры данных **битмапинфохеадер** с помощью структуры данных **двинфо** .</span><span class="sxs-lookup"><span data-stu-id="1177f-143">The stream format chunk can be optionally extended to include the [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) chunk, by increasing the stream format chunk size from 40 bytes (size of the **BITMAPINFOHEADER** structure) to 72 bytes (size of **BITMAPINFOHEADER** plus **DVINFO** structures) and immediately following the **BITMAPINFOHEADER** data structure with a **DVINFO** data structure.</span></span>

<span data-ttu-id="1177f-144">Аудио-поток (ы) указан со стандартным заголовком аудиопотока (значение элемента **фкктипе** — "аудс").</span><span class="sxs-lookup"><span data-stu-id="1177f-144">The audio stream(s) is specified with a standard audio stream header (the **fccType** member value is 'auds').</span></span> <span data-ttu-id="1177f-145">Элемент **фкчандлер** не используется для звуковых потоков.</span><span class="sxs-lookup"><span data-stu-id="1177f-145">The **fccHandler** member is not used for audio streams.</span></span>

<span data-ttu-id="1177f-146">Видеоданные DV хранятся в виде \# \# фрагментов "DC", как определено в предыдущем ОПИСАНии AVI-файла с одной DV-видеоданными, а звуковые данные хранятся в виде \# \# фрагментов "WB" в блоке "Мови".</span><span class="sxs-lookup"><span data-stu-id="1177f-146">The DV video data is stored as '\#\#dc' chunks, as defined in the preceding description of an AVI file with one DV data, and the audio data is stored as '\#\#wb' chunks in the 'movi' chunk.</span></span>

> [!Note]  
> <span data-ttu-id="1177f-147">*Спецификация цифровой видеомагнитофона* может быть недоступна в некоторых языках и странах.</span><span class="sxs-lookup"><span data-stu-id="1177f-147">The *Specification of Consumer-use Digital VCRs* may not be available in some languages and countries.</span></span>

 

<span data-ttu-id="1177f-148">В следующем примере показана форма AIFF Metallica для AVI-файла, содержащего DV-видео в виде потока VID и DV Audio в виде потоков "аудс", развернутых с помощью завершенных фрагментов заголовка (включая дополнительные данные [**двинфо**](/windows/desktop/api/strmif/ns-strmif-dvinfo) , следующие за [**битмапинфо**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) во вложенном фрагменте "стрф" для потока "VID").</span><span class="sxs-lookup"><span data-stu-id="1177f-148">The following example shows the AIFF RIFF form for an AVI file containing DV video as a 'vids' stream and DV audio as 'auds' streams expanded with completed header chunks (including optional [**DVINFO**](/windows/desktop/api/strmif/ns-strmif-dvinfo) data following the [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) in the 'strf' sub-chunk for the 'vids' stream).</span></span>


```C++
00000000 RIFF (103E2920) 'AVI '
0000000C     LIST (00000146) 'hdrl'
00000018         avih (00000038)
                     dwMicroSecPerFrame    : 33367
                     dwMaxBytesPerSec      : 3728000
                     dwPaddingGranularity  : 0
                     dwFlags               : 0x810 HASINDEX | TRUSTCKTYPE
                     dwTotalFrames         : 2192
                     dwInitialFrames       : 0
                     dwStreams             : 2
                     dwSuggestedBufferSize : 120000
                     dwWidth               : 720
                     dwHeight              : 480
                     dwReserved            : 0x0
00000058         LIST (00000094) 'strl'
00000064             strh (00000038)
                         fccType               : 'vids'
                         fccHandler            : 'dvsd'
                         dwFlags               : 0x0
                         wPriority             : 0
                         wLanguage             : 0x0 undefined
                         dwInitialFrames       : 0
                         dwScale               : 100 (29.970 Frames/Sec)
                         dwRate                : 2997
                         dwStart               : 0
                         dwLength              : 2192
                         dwSuggestedBufferSize : 120000
                         dwQuality             : 0
                         dwSampleSize          : 0
                         rcFrame               : 0,0,720,480
000000A4             strf (00000048)
                         biSize          : 40
                         biWidth         : 720
                         biHeight        : 480
                         biPlanes        : 1
                         biBitCount      : 24
                         biCompression   : 0x64737664 'dvsd'
                         biSizeImage     : 120000
                         biXPelsPerMeter : 0
                         biYPelsPerMeter : 0
                         biClrUsed       : 0
                         biClrImportant  : 0
                         dwDVAAuxSrc     : 0x........
                         dwDVAAuxCtl     : 0x........
                         dwDVAAuxSrc1    : 0x........
                         dwDVAAuxCtl1    : 0x........
                         dwDVVAuxSrc     : 0x........
                         dwDVVAuxCtl     : 0x........
                         dwDVReserved[2] : 0,0
000000F4         LIST (0000005E) 'strl'
00000100             strh (00000038)
                         fccType               : 'auds'
                         fccHandler            : '    '
                         dwFlags               : 0x0
                         wPriority             : 0
                         wLanguage             : 0x0 undefined
                         dwInitialFrames       : 0
                         dwScale               : 1 (32000.000 Samples/Sec)
                         dwRate                : 32000
                         dwStart               : 0
                         dwLength              : 2340474
                         dwSuggestedBufferSize : 4272
                         dwQuality             : 0
                         dwSampleSize          : 4
                         rcFrame               : 0,0,0,0
00000140             strf (00000012)
                         wFormatTag      : 1 PCM
                         nChannels       : 2
                         nSamplesPerSec  : 32000
                         nAvgBytesPerSec : 128000
                         nBlockAlign     : 4
                         wBitsPerSample  : 16
                         cbSize          : 0
00000814     LIST (103D0EF4) 'movi'
103D1710     idx1 (00011210)
```



## <a name="related-topics"></a><span data-ttu-id="1177f-149">См. также</span><span class="sxs-lookup"><span data-stu-id="1177f-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1177f-150">Формат файла AVI</span><span class="sxs-lookup"><span data-stu-id="1177f-150">AVI File Format</span></span>](avi-file-format.md)
</dt> </dl>

 

 
