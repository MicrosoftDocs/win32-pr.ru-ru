---
description: Видеокодеки Windows Media Audio и Video представляют собой коллекцию объектов, которые можно использовать для сжатия и распаковки цифровых мультимедийных данных.
ms.assetid: 74de2e75-b1ee-436d-8d78-efe366ab7aa6
title: Кодеки Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ec98f98fbd0561b291dfc4cc18e4270bf363baf
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105693884"
---
# <a name="windows-media-codecs"></a><span data-ttu-id="9b9b2-103">Кодеки Windows Media</span><span class="sxs-lookup"><span data-stu-id="9b9b2-103">Windows Media Codecs</span></span>

<span data-ttu-id="9b9b2-104">Видеокодеки Windows Media Audio и Video представляют собой коллекцию объектов, которые можно использовать для сжатия и распаковки цифровых мультимедийных данных.</span><span class="sxs-lookup"><span data-stu-id="9b9b2-104">The Windows Media Audio and Video codecs are a collection of objects that you can use to compress and decompress digital media data.</span></span> <span data-ttu-id="9b9b2-105">Каждый кодек состоит из двух объектов: кодировщика и декодера.</span><span class="sxs-lookup"><span data-stu-id="9b9b2-105">Each codec consists of two objects, an encoder and a decoder.</span></span> <span data-ttu-id="9b9b2-106">В этой части документации описывается использование функций кодеков аудио и видео Windows Media для создания и использования сжатых потоков данных.</span><span class="sxs-lookup"><span data-stu-id="9b9b2-106">This part of the documentation describes how to use the features of the Windows Media Audio and Video codecs to produce and consume compressed data streams.</span></span>

> [!Note]  
> <span data-ttu-id="9b9b2-107">Эта документация предназначена главным образом для разработчиков, желающих использовать кодеки Windows Media в своих мультимедийных приложениях на основе C++.</span><span class="sxs-lookup"><span data-stu-id="9b9b2-107">This documentation is primarily for developers who want to use Windows Media codecs in their C++-based media applications.</span></span> <span data-ttu-id="9b9b2-108">Технический обзор возможностей кодеков Windows Media см. в разделе [о кодеках Windows Media](about-the-windows-media-codecs.md).</span><span class="sxs-lookup"><span data-stu-id="9b9b2-108">For a technical overview of the features of the Windows Media codecs, see [About the Windows Media Codecs](about-the-windows-media-codecs.md).</span></span>

 

<span data-ttu-id="9b9b2-109">Термин *кодек* — это слияние терминов программы сжатия и распаковки.</span><span class="sxs-lookup"><span data-stu-id="9b9b2-109">The term *codec* is an amalgamation of the terms compressor and decompressor.</span></span> <span data-ttu-id="9b9b2-110">Кодек обычно реализуется как пара COM-объектов: один для кодирования содержимого, а другой для декодирования содержимого.</span><span class="sxs-lookup"><span data-stu-id="9b9b2-110">A codec is usually implemented as a pair of COM objects: one for encoding content, and another for decoding content.</span></span> <span data-ttu-id="9b9b2-111">В некоторых случаях COM-объекты занимают одну и ту же динамически связанную библиотеку (DLL).</span><span class="sxs-lookup"><span data-stu-id="9b9b2-111">In some cases the COM objects occupy the same dynamically linked library (DLL).</span></span>

<span data-ttu-id="9b9b2-112">Каждый объект кодека реализует два отдельных, но схожих интерфейса:</span><span class="sxs-lookup"><span data-stu-id="9b9b2-112">Every codec object implements two separate but similar interfaces:</span></span>



| <span data-ttu-id="9b9b2-113">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="9b9b2-113">Interface</span></span>                              | <span data-ttu-id="9b9b2-114">Описание</span><span class="sxs-lookup"><span data-stu-id="9b9b2-114">Description</span></span>                                 |
|----------------------------------------|---------------------------------------------|
| [<span data-ttu-id="9b9b2-115">**имфтрансформ**</span><span class="sxs-lookup"><span data-stu-id="9b9b2-115">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)   | <span data-ttu-id="9b9b2-116">Совместимо с Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="9b9b2-116">Compatible with Microsoft Media Foundation.</span></span> |
| [<span data-ttu-id="9b9b2-117">**имедиаобжект**</span><span class="sxs-lookup"><span data-stu-id="9b9b2-117">**IMediaObject**</span></span>](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) | <span data-ttu-id="9b9b2-118">Совместимо с DirectShow.</span><span class="sxs-lookup"><span data-stu-id="9b9b2-118">Compatible with DirectShow.</span></span>                 |



 

<span data-ttu-id="9b9b2-119">Для аудио и видео могут использоваться не только различные кодеки, но и разные кодеки для различных видов содержимого, которые можно поместить в аудио-или видеофайл.</span><span class="sxs-lookup"><span data-stu-id="9b9b2-119">Not only are there different codecs for audio and for video, but also different codecs for different kinds of content that you might want to put into an audio or video file.</span></span> <span data-ttu-id="9b9b2-120">Алгоритмы, используемые для сжатия и распаковки данных для произносимых слов, отличаются от алгоритмов, используемых для сжатия и распаковки музыкальных данных.</span><span class="sxs-lookup"><span data-stu-id="9b9b2-120">The algorithms used to compress and decompress data for spoken words differ from the algorithms used to compress and decompress music data.</span></span>

## <a name="codec-descriptions"></a><span data-ttu-id="9b9b2-121">Описания кодеков</span><span class="sxs-lookup"><span data-stu-id="9b9b2-121">Codec Descriptions</span></span>

<span data-ttu-id="9b9b2-122">В следующей таблице описаны предполагаемые варианты использования кодеков Windows Media.</span><span class="sxs-lookup"><span data-stu-id="9b9b2-122">The following table describes the intended uses of the Windows Media codecs.</span></span>



| <span data-ttu-id="9b9b2-123">Кодек</span><span class="sxs-lookup"><span data-stu-id="9b9b2-123">Codec</span></span>                                                                     | <span data-ttu-id="9b9b2-124">Описание</span><span class="sxs-lookup"><span data-stu-id="9b9b2-124">Description</span></span>                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9b9b2-125">Windows Media Audio</span><span class="sxs-lookup"><span data-stu-id="9b9b2-125">Windows Media Audio</span></span>](windowsmediaaudioencoder.md)                       | <span data-ttu-id="9b9b2-126">Аудиокодек, поддерживающий три категории закодированного содержимого: Standard, Professional и без потерь.</span><span class="sxs-lookup"><span data-stu-id="9b9b2-126">An audio codec that supports three categories of encoded content: Standard, Professional, and Lossless.</span></span>                                                                                                                                                                                      |
| [<span data-ttu-id="9b9b2-127">Windows Media Audio Voice</span><span class="sxs-lookup"><span data-stu-id="9b9b2-127">Windows Media Audio Voice</span></span>](windowsmediaaudiovoiceencoder.md)            | <span data-ttu-id="9b9b2-128">Аудиокодек, оптимизированный для кодирования человеческого голоса при высоком коэффициенте сжатия.</span><span class="sxs-lookup"><span data-stu-id="9b9b2-128">Audio codec optimized for encoding the human voice at high compression ratios.</span></span> <span data-ttu-id="9b9b2-129">Это предпочтительный кодек для потоков, состоящих в основном на произнесенных словах.</span><span class="sxs-lookup"><span data-stu-id="9b9b2-129">This is the preferred codec for streams consisting mostly of spoken words.</span></span> <span data-ttu-id="9b9b2-130">Для содержимого, которое является смешанной музыкой и речью, этот кодек может динамически изменить используемый алгоритм кодирования, чтобы получить оптимальное качество.</span><span class="sxs-lookup"><span data-stu-id="9b9b2-130">For content that is mixed music and speech, this codec can dynamically change the encoding algorithm used, to get optimal quality.</span></span> |
| [<span data-ttu-id="9b9b2-131">Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="9b9b2-131">Windows Media Video 9</span></span>](windowsmediavideo9encoder.md)                    | <span data-ttu-id="9b9b2-132">Видеокодек, который поддерживает четыре категории закодированного содержимого: простой профиль, основной профиль, расширенный профиль и образ.</span><span class="sxs-lookup"><span data-stu-id="9b9b2-132">A video codec that supports four categories of encoded content: Simple Profile, Main Profile, Advanced Profile, and Image..</span></span>                                                                                                                                                                  |
| [<span data-ttu-id="9b9b2-133">Экран Windows Media видео 9</span><span class="sxs-lookup"><span data-stu-id="9b9b2-133">Windows Media Video 9 Screen</span></span>](usingthewindowsmediavideo9screencodec.md) | <span data-ttu-id="9b9b2-134">Видеокодек, оптимизированный для кодирования последовательных снимков экрана от компьютерных мониторов.</span><span class="sxs-lookup"><span data-stu-id="9b9b2-134">Video codec optimized for encoding sequential screen shots from computer monitors.</span></span> <span data-ttu-id="9b9b2-135">Этот кодек часто используется для обучения программного обеспечения или поддержки путем записи образов мониторов во время использования компьютерных приложений.</span><span class="sxs-lookup"><span data-stu-id="9b9b2-135">This codec is often used for software training or support by recording monitor images while computer applications are being used.</span></span>                                                                         |



 

<span data-ttu-id="9b9b2-136">Последние версии объектов кодека также обеспечивают доступ к некоторым старым кодекам, включая Windows Media Video 7 и 8, Windows Media Screen 7, старые кодеки Microsoft MPEG-4 и кодеки ISO MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="9b9b2-136">The most recent versions of the codec objects also enable access to some legacy codecs, including Windows Media Video 7 and 8, Windows Media Screen 7, the older Microsoft MPEG-4 codecs, and the Microsoft ISO MPEG-4 codecs.</span></span>

> [!Note]  
> <span data-ttu-id="9b9b2-137">Эта документация не охватывает устаревшие кодеки. Он охватывает только текущие версии кодеков.</span><span class="sxs-lookup"><span data-stu-id="9b9b2-137">This documentation does not cover these legacy codecs; it covers only the current versions of codecs.</span></span>

 

<span data-ttu-id="9b9b2-138">Для старых кодеков используйте те же процедуры, что и при использовании текущих кодеков. Однако помните, что не все функции поддерживаются во всех кодеках.</span><span class="sxs-lookup"><span data-stu-id="9b9b2-138">For older codecs, use the same procedures as when using the current codecs; however, remember that not all features are supported in all codecs.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9b9b2-139">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="9b9b2-139">In this section</span></span>

-   [<span data-ttu-id="9b9b2-140">О кодеках Windows Media</span><span class="sxs-lookup"><span data-stu-id="9b9b2-140">About the Windows Media Codecs</span></span>](about-the-windows-media-codecs.md)
-   [<span data-ttu-id="9b9b2-141">Использование кодеков и объектов DSP</span><span class="sxs-lookup"><span data-stu-id="9b9b2-141">Using the Codec and DSP Objects</span></span>](decidinghowtousethewindowsmediaaudioandvideocodecs.md)
-   [<span data-ttu-id="9b9b2-142">Методы кодирования</span><span class="sxs-lookup"><span data-stu-id="9b9b2-142">Encoding Methods</span></span>](encodingmethods.md)
-   [<span data-ttu-id="9b9b2-143">Реализация кодека</span><span class="sxs-lookup"><span data-stu-id="9b9b2-143">Codec Implementation</span></span>](codecimplementation.md)
-   [<span data-ttu-id="9b9b2-144">Модель буфера для контейнера утечки</span><span class="sxs-lookup"><span data-stu-id="9b9b2-144">The Leaky Bucket Buffer Model</span></span>](the-leaky-bucket-buffer-model.md)
-   [<span data-ttu-id="9b9b2-145">Работа с кодеками дмос</span><span class="sxs-lookup"><span data-stu-id="9b9b2-145">Working with Codec DMOs</span></span>](workingwithcodecdmos.md)
-   [<span data-ttu-id="9b9b2-146">Работа с кодеками МФТС</span><span class="sxs-lookup"><span data-stu-id="9b9b2-146">Working with Codec MFTs</span></span>](workingwithcodecmfts.md)
-   [<span data-ttu-id="9b9b2-147">Работа с аудио</span><span class="sxs-lookup"><span data-stu-id="9b9b2-147">Working with Audio</span></span>](workingwithaudio.md)
-   [<span data-ttu-id="9b9b2-148">Работа с видео</span><span class="sxs-lookup"><span data-stu-id="9b9b2-148">Working with Video</span></span>](workingwithvideo.md)
-   [<span data-ttu-id="9b9b2-149">Хранение сжатых файлов мультимедиа в AVI</span><span class="sxs-lookup"><span data-stu-id="9b9b2-149">Storing Compressed Media in AVI Files</span></span>](storingcompressedmediainavifiles.md)
-   [<span data-ttu-id="9b9b2-150">Использование кодирования VBR</span><span class="sxs-lookup"><span data-stu-id="9b9b2-150">Using VBR Encoding</span></span>](usingvbrencoding.md)
-   [<span data-ttu-id="9b9b2-151">Использование кодировки Two-Pass</span><span class="sxs-lookup"><span data-stu-id="9b9b2-151">Using Two-Pass Encoding</span></span>](usingtwoencodingpasses.md)
-   [<span data-ttu-id="9b9b2-152">Получение статистики кодировки</span><span class="sxs-lookup"><span data-stu-id="9b9b2-152">Getting Encoding Statistics</span></span>](gettingencodingstatistics.md)
-   [<span data-ttu-id="9b9b2-153">Использование модулей обработки данных</span><span class="sxs-lookup"><span data-stu-id="9b9b2-153">Using Data Unit Extensions</span></span>](usingdataunitextensions.md)
-   [<span data-ttu-id="9b9b2-154">Константы кодеков и DSP Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="9b9b2-154">Codec and DSP IPropertyBag Constants</span></span>](codecanddspproperties.md)
-   [<span data-ttu-id="9b9b2-155">Средство синтаксического анализа оглавления</span><span class="sxs-lookup"><span data-stu-id="9b9b2-155">Table of Contents Parser</span></span>](toc-parser.md)
-   [<span data-ttu-id="9b9b2-156">Часто задаваемые вопросы о кодеке Windows Media</span><span class="sxs-lookup"><span data-stu-id="9b9b2-156">Windows Media Codec FAQ</span></span>](frequentlyaskedquestions.md)

## <a name="related-topics"></a><span data-ttu-id="9b9b2-157">См. также</span><span class="sxs-lookup"><span data-stu-id="9b9b2-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b9b2-158">Media Foundationое программное руководством</span><span class="sxs-lookup"><span data-stu-id="9b9b2-158">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> <dt>

<span data-ttu-id="9b9b2-159">[Мультимедийные технологии для Windows](/previous-versions/bg125389(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="9b9b2-159">[Media Technologies for Windows](/previous-versions/bg125389(v=msdn.10))</span></span>
</dt> </dl>

 

 
