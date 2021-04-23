---
description: В этом разделе представлен обзор API-интерфейсов кодирования файлов, предоставляемых в Microsoft Media Foundation.
ms.assetid: 69dbef63-e272-4ad2-8d04-ae9366f79b33
title: Общие сведения о кодировке в Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81882bd6da43f4040614347b662d988844c7b7a6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104554616"
---
# <a name="overview-of-encoding-in-media-foundation"></a><span data-ttu-id="1d7f8-103">Общие сведения о кодировке в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1d7f8-103">Overview of Encoding in Media Foundation</span></span>

<span data-ttu-id="1d7f8-104">В этом разделе представлен обзор API-интерфейсов кодирования файлов, предоставляемых в Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="1d7f8-104">This topic is an overview of the file encoding APIs provided in Microsoft Media Foundation.</span></span>

## <a name="terminology"></a><span data-ttu-id="1d7f8-105">Терминология</span><span class="sxs-lookup"><span data-stu-id="1d7f8-105">Terminology</span></span>

<span data-ttu-id="1d7f8-106">*Кодирование* — это общий термин, охватывающий несколько различных процессов:</span><span class="sxs-lookup"><span data-stu-id="1d7f8-106">*Encoding* is a general term that covers several distinct processes:</span></span>

1.  <span data-ttu-id="1d7f8-107">Кодирование аудио-или видеопотока в сжатые форматы.</span><span class="sxs-lookup"><span data-stu-id="1d7f8-107">Encoding an audio or video stream into a compressed formats.</span></span> <span data-ttu-id="1d7f8-108">Например, кодирование видео-потока в H. 264 Video.</span><span class="sxs-lookup"><span data-stu-id="1d7f8-108">For example, encoding a video stream to H.264 video.</span></span>
2.  <span data-ttu-id="1d7f8-109">Мультиплексирование ("мультиплексированием") одного или нескольких потоков в однобайтовый поток.</span><span class="sxs-lookup"><span data-stu-id="1d7f8-109">Multiplexing ("muxing") one or more streams into a single byte stream.</span></span> <span data-ttu-id="1d7f8-110">Как правило, входящие потоки кодируются первыми.</span><span class="sxs-lookup"><span data-stu-id="1d7f8-110">Typically, the incoming streams are encoded first.</span></span> <span data-ttu-id="1d7f8-111">Этот шаг может содержать паккетизинг закодированных потоков.</span><span class="sxs-lookup"><span data-stu-id="1d7f8-111">This step might involve packetizing the encoded streams.</span></span>
3.  <span data-ttu-id="1d7f8-112">Запись мультиплексированного потока байтов в файл, например в файл формата MP4 или Advanced Systems (ASF).</span><span class="sxs-lookup"><span data-stu-id="1d7f8-112">Writing a multiplexed byte stream to a file, such as an MP4 or Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="1d7f8-113">Кроме того, мультиплексированный поток может быть отправлен по сети.</span><span class="sxs-lookup"><span data-stu-id="1d7f8-113">Alternatively, the multiplexed stream can be sent over the network.</span></span>

<span data-ttu-id="1d7f8-114">На следующей схеме показаны три процесса:</span><span class="sxs-lookup"><span data-stu-id="1d7f8-114">The following diagram shows these three processes:</span></span>

![Схема, демонстрирующая процессы кодирования и мультиплексирования](images/encoding03.png)

<span data-ttu-id="1d7f8-116">К вариантам этого процесса относятся Перекодировка и ремуксинг:</span><span class="sxs-lookup"><span data-stu-id="1d7f8-116">Variations of this process include transcoding and remuxing:</span></span>

-   <span data-ttu-id="1d7f8-117">*Перекодирование* означает декодирование существующего файла, повторное кодирование потоков и повторное мультиплексирование закодированных потоков.</span><span class="sxs-lookup"><span data-stu-id="1d7f8-117">*Transcoding* means decoding an existing file, re-encoding the streams, and re-multiplexing the encoded streams.</span></span> <span data-ttu-id="1d7f8-118">Перекодирование может быть выполнено для преобразования файла из одного типа кодирования в другой. Например, для преобразования видео H. 264 в Windows Media Video (WMV).</span><span class="sxs-lookup"><span data-stu-id="1d7f8-118">Transcoding might be done to convert a file from one encoding type to another; for example, to convert H.264 video to Windows Media Video (WMV).</span></span> <span data-ttu-id="1d7f8-119">Это также можно сделать для изменения скорости закодированных битов; Размер кадра видео; Частота кадров; или другие параметры форматирования.</span><span class="sxs-lookup"><span data-stu-id="1d7f8-119">It can also be done to change the encoded bit rate; the video frame size; the frame rate; or other format parameters.</span></span>
-   <span data-ttu-id="1d7f8-120">*Ремультиплексирование* или *ремуксинг* означает демультиплексирование файла и повторное мультиплексирование потоков без шага декодирования/кодирования.</span><span class="sxs-lookup"><span data-stu-id="1d7f8-120">*Remultiplexing* or *remuxing* means demultiplexing a file and re-multiplexing the streams, with no decode/encode step.</span></span> <span data-ttu-id="1d7f8-121">Это может быть сделано для изменения способа мультиплексирования аудио-и видеосигналов, удаления потока или объединения потоков из двух разных исходных файлов.</span><span class="sxs-lookup"><span data-stu-id="1d7f8-121">This might be done to change how the audio/video packets are multiplexed, to remove a stream, or to combine streams from two different source files.</span></span>
-   <span data-ttu-id="1d7f8-122">Преобразование — это особый случай перекодирования *, при котором* битовая частота изменяется без изменения типа сжатия.</span><span class="sxs-lookup"><span data-stu-id="1d7f8-122">*Transrating* is a special case of transcoding, where the bit-rate is changed without changing the compression type.</span></span> <span data-ttu-id="1d7f8-123">Например, вы можете преобразовать файл высокой разрядной скорости в более низкую разрядную скорость.</span><span class="sxs-lookup"><span data-stu-id="1d7f8-123">For example, you might convert a high-bit-rate file to a lower bit-rate.</span></span> <span data-ttu-id="1d7f8-124">Как правило, при синхронизации мультимедийного содержимого с компьютера на портативное устройство используется типичный сценарий.</span><span class="sxs-lookup"><span data-stu-id="1d7f8-124">A typical scenario in which transrating might be used is when synchronizing media content from a PC to a portable device.</span></span> <span data-ttu-id="1d7f8-125">Если портативное устройство не поддерживает высокую скорость передачи, перед копированием на переносное устройство может быть выполнено переоценка файла.</span><span class="sxs-lookup"><span data-stu-id="1d7f8-125">If the portable device does not support a high bit rate, the file might be transrated before it is copied to the portable device.</span></span>

<span data-ttu-id="1d7f8-126">На следующей блоковой схеме показан процесс перекодирования.</span><span class="sxs-lookup"><span data-stu-id="1d7f8-126">The following block diagram shows the transcoding process.</span></span>

![Схема, показывающая процесс перекодирования](images/encoding05.png)

<span data-ttu-id="1d7f8-128">На следующей блоковой схеме показан процесс ремуксинг.</span><span class="sxs-lookup"><span data-stu-id="1d7f8-128">The following block diagram shows the remuxing process.</span></span>

![Схема, показывающая процесс ремуксинг](images/encoding06.png)

<span data-ttu-id="1d7f8-130">В этой документации иногда используется термин *кодирование* для включения как перекодирования, так и ремуксинг.</span><span class="sxs-lookup"><span data-stu-id="1d7f8-130">This documentation sometimes uses the term *encoding* to include both transcoding and remuxing.</span></span> <span data-ttu-id="1d7f8-131">Если важно различать их, в документации будет заметка разницы.</span><span class="sxs-lookup"><span data-stu-id="1d7f8-131">When it is important to distinguish between them, the documentation will note the difference.</span></span>

<span data-ttu-id="1d7f8-132">См. также: [Media Foundation: основные понятия](media-foundation-programming--essential-concepts.md).</span><span class="sxs-lookup"><span data-stu-id="1d7f8-132">See also: [Media Foundation: Essential Concepts](media-foundation-programming--essential-concepts.md).</span></span>

## <a name="media-foundation-encoding-architecture"></a><span data-ttu-id="1d7f8-133">Архитектура кодировки Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1d7f8-133">Media Foundation Encoding Architecture</span></span>

<span data-ttu-id="1d7f8-134">На самом низком уровне архитектуры Media Foundation для кодирования используются следующие типы компонентов:</span><span class="sxs-lookup"><span data-stu-id="1d7f8-134">At the lowest layer of the Media Foundation architecture, the following types of component are used for encoding:</span></span>

-   <span data-ttu-id="1d7f8-135">Для перекодировки [источники мультимедиа](media-sources.md) используются для демультиплексирования исходного файла.</span><span class="sxs-lookup"><span data-stu-id="1d7f8-135">For transcoding, [Media Sources](media-sources.md) are used to demultiplex the source file.</span></span>
-   <span data-ttu-id="1d7f8-136">Для процесса кодирования [Media Foundation преобразования](media-foundation-transforms.md) используются для декодирования и кодирования потоков.</span><span class="sxs-lookup"><span data-stu-id="1d7f8-136">For the encoding process, [Media Foundation Transforms](media-foundation-transforms.md) are used to decode and encode streams.</span></span>
-   <span data-ttu-id="1d7f8-137">Для процесса мультиплексирования [приемники мультимедиа](media-sinks.md) используются для мультиплексирования потоков и записи мультиплексированного потока в файл или в сеть.</span><span class="sxs-lookup"><span data-stu-id="1d7f8-137">For the multiplexing process, [Media Sinks](media-sinks.md) are used to multiplex the streams and write the multiplexed stream to a file or network.</span></span>

<span data-ttu-id="1d7f8-138">На следующей схеме показан поток данных между этими компонентами в сценарии перекодирования:</span><span class="sxs-lookup"><span data-stu-id="1d7f8-138">The following diagram shows the data flow between these components in a transcoding scenario:</span></span>

![Диаграмма, на которой показаны компоненты, используемые при перекодировании](images/encoding04.png)

<span data-ttu-id="1d7f8-140">Большинство приложений не будут использовать эти компоненты напрямую.</span><span class="sxs-lookup"><span data-stu-id="1d7f8-140">Most applications will not use these components directly.</span></span> <span data-ttu-id="1d7f8-141">Вместо этого приложение будет использовать API более высокого уровня для управления этими компонентами нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="1d7f8-141">Instead, an application will use higher-level APIs that manage these lower-level components.</span></span> <span data-ttu-id="1d7f8-142">Media Foundation предоставляет два интерфейса API более высокого уровня для кодирования:</span><span class="sxs-lookup"><span data-stu-id="1d7f8-142">Media Foundation provides two higher-level APIs for encoding:</span></span>

<dl> <dt>

<span data-ttu-id="1d7f8-143"><span id="Media_Session"></span><span id="media_session"></span><span id="MEDIA_SESSION"></span>[Сеанс мультимедиа](media-session.md)</span><span class="sxs-lookup"><span data-stu-id="1d7f8-143"><span id="Media_Session"></span><span id="media_session"></span><span id="MEDIA_SESSION"></span>[Media Session](media-session.md)</span></span>
</dt> <dd>

<span data-ttu-id="1d7f8-144">Сеанс мультимедиа предоставляет сквозной конвейер, который перемещает данные из источника мультимедиа через кодеки, а затем в приемник мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="1d7f8-144">The Media Session provides an end-to-end pipeline that moves data from the media source, through the codecs, and finally to the media sink.</span></span> <span data-ttu-id="1d7f8-145">Приложение управляет сеансом мультимедиа и получает события состояния от сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="1d7f8-145">The application controls the Media Session and receives status events from the Media Session.</span></span>

</dd> <dt>

<span data-ttu-id="1d7f8-146"><span id="Source_Reader_plus_Sink_Writer"></span><span id="source_reader_plus_sink_writer"></span><span id="SOURCE_READER_PLUS_SINK_WRITER"></span>Модуль [чтения исходного кода](source-reader.md) и [модуль записи приемников](sink-writer.md)</span><span class="sxs-lookup"><span data-stu-id="1d7f8-146"><span id="Source_Reader_plus_Sink_Writer"></span><span id="source_reader_plus_sink_writer"></span><span id="SOURCE_READER_PLUS_SINK_WRITER"></span>[Source Reader](source-reader.md) plus [Sink Writer](sink-writer.md)</span></span>
</dt> <dd>

<span data-ttu-id="1d7f8-147">Модуль чтения исходного кода создает оболочку для источника мультимедиа и, при необходимости, декодеров.</span><span class="sxs-lookup"><span data-stu-id="1d7f8-147">The Source Reader wraps the media source and optionally the decoders.</span></span> <span data-ttu-id="1d7f8-148">Он предоставляет приложению закодированные или декодированные образцы.</span><span class="sxs-lookup"><span data-stu-id="1d7f8-148">It delivers either encoded or decoded samples the application.</span></span> <span data-ttu-id="1d7f8-149">Модуль записи приемника инкапсулирует приемник мультимедиа и, при необходимости, кодировщики.</span><span class="sxs-lookup"><span data-stu-id="1d7f8-149">The Sink Writer wraps the media sink and optionally the encoders.</span></span> <span data-ttu-id="1d7f8-150">Приложение передает примеры в модуль записи приемника.</span><span class="sxs-lookup"><span data-stu-id="1d7f8-150">The application passes samples to the Sink Writer.</span></span>

</dd> </dl>

<span data-ttu-id="1d7f8-151">На следующей схеме показан сеанс мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="1d7f8-151">The following diagram shows the Media Session:</span></span>

![Схема, показывающая, как сеанс мультимедиа выполняет перекодирование](images/encoding01.png)

<span data-ttu-id="1d7f8-153">[API](transcode-api.md) перекодировки (синее затенение) — это набор интерфейсов API, появившихся в Windows 7, которые упрощают настройку сеанса мультимедиа для кодирования.</span><span class="sxs-lookup"><span data-stu-id="1d7f8-153">The [Transcode API](transcode-api.md) (the blue shaded box) is a set of APIs introduced in Windows 7, which make it easier to configure the Media Session for encoding.</span></span>

<span data-ttu-id="1d7f8-154">На следующей схеме показан считыватель исходного кода и модуль записи приемника:</span><span class="sxs-lookup"><span data-stu-id="1d7f8-154">The next diagram shows the Source Reader and Sink Writer:</span></span>

![Схема, демонстрирующая перекодирование с помощью модуля чтения исходного кода и модуля записи приемника](images/encoding02.png)

## <a name="related-topics"></a><span data-ttu-id="1d7f8-156">См. также</span><span class="sxs-lookup"><span data-stu-id="1d7f8-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d7f8-157">Кодировка и разработка файлов</span><span class="sxs-lookup"><span data-stu-id="1d7f8-157">Encoding and File Authoring</span></span>](encoding-and-file-authoring.md)
</dt> <dt>

[<span data-ttu-id="1d7f8-158">Media Foundation программирование: основные понятия</span><span class="sxs-lookup"><span data-stu-id="1d7f8-158">Media Foundation Programming: Essential Concepts</span></span>](media-foundation-programming--essential-concepts.md)
</dt> </dl>

 

 



