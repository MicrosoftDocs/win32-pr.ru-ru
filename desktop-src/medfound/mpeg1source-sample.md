---
description: Пример MPEG1Source
ms.assetid: c9f131ff-0b79-487c-9a46-a9b1350553a1
title: Пример MPEG1Source
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c71bd541a7bd01621ca7359eb9e229a08e91a04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650628"
---
# <a name="mpeg1source-sample"></a><span data-ttu-id="f76ba-103">Пример MPEG1Source</span><span class="sxs-lookup"><span data-stu-id="f76ba-103">MPEG1Source Sample</span></span>

<span data-ttu-id="f76ba-104">Описание процесса записи пользовательского источника мультимедиа в Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="f76ba-104">Shows how to write a custom media source in Microsoft Media Foundation.</span></span> <span data-ttu-id="f76ba-105">В примере реализуется источник мультимедиа, который анализирует потоки на уровне системы MPEG-1 и создает образцы, содержащие полезные данные MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="f76ba-105">The sample implements a media source that parses MPEG-1 systems-layer streams and generates samples that contain MPEG-1 payloads.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="f76ba-106">Продемонстрированные API</span><span class="sxs-lookup"><span data-stu-id="f76ba-106">APIs Demonstrated</span></span>

<span data-ttu-id="f76ba-107">В этом образце демонстрируются следующие интерфейсы Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="f76ba-107">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="f76ba-108">**имфбитестреамхандлер**</span><span class="sxs-lookup"><span data-stu-id="f76ba-108">**IMFByteStreamHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)
-   [<span data-ttu-id="f76ba-109">**имфмедиасаурце**</span><span class="sxs-lookup"><span data-stu-id="f76ba-109">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
-   [<span data-ttu-id="f76ba-110">**имфмедиастреам**</span><span class="sxs-lookup"><span data-stu-id="f76ba-110">**IMFMediaStream**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)

<span data-ttu-id="f76ba-111">Перед изучением этого примера может потребоваться ознакомиться с [примером вавсаурце](wavsource-sample.md), который предоставляет более простую реализацию источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f76ba-111">Before examining this sample, you might want to review the [WavSource Sample](wavsource-sample.md), which provides a simpler implementation of a media source.</span></span> <span data-ttu-id="f76ba-112">В примере MPEG1Source добавляются некоторые функции, которые можно найти в большинстве реальных реализаций источника мультимедиа:</span><span class="sxs-lookup"><span data-stu-id="f76ba-112">The MPEG1Source sample adds some features that would be found in most real-world implementations of a media source:</span></span>

-   <span data-ttu-id="f76ba-113">Несколько потоков</span><span class="sxs-lookup"><span data-stu-id="f76ba-113">Multiple streams</span></span>
-   <span data-ttu-id="f76ba-114">Асинхронные методы</span><span class="sxs-lookup"><span data-stu-id="f76ba-114">Asynchronous methods</span></span>
-   <span data-ttu-id="f76ba-115">Асинхронный ввод-вывод</span><span class="sxs-lookup"><span data-stu-id="f76ba-115">Asynchronous I/O</span></span>

<span data-ttu-id="f76ba-116">В Windows SDK для Windows Server 2008 этот пример также включает пример видеодекодера MPEG-1, который отображает код времени для каждого кадра видео.</span><span class="sxs-lookup"><span data-stu-id="f76ba-116">In the Windows SDK for Windows Server 2008, this sample also includes a sample MPEG-1 video decoder that displays the time code for each video frame.</span></span> <span data-ttu-id="f76ba-117">(В действительности он не расшифровывает битовый поток MPEG-1.)</span><span class="sxs-lookup"><span data-stu-id="f76ba-117">(It does not actually decode the MPEG-1 bitstream.)</span></span>

<span data-ttu-id="f76ba-118">Начиная с Windows SDK для Windows 7 декодер был перемещен в отдельный пример.</span><span class="sxs-lookup"><span data-stu-id="f76ba-118">Starting in the Windows SDK for Windows 7, the decoder has been moved to a separate sample.</span></span> <span data-ttu-id="f76ba-119">См. [Пример декодера](decoder-sample.md).</span><span class="sxs-lookup"><span data-stu-id="f76ba-119">See [Decoder Sample](decoder-sample.md).</span></span>

## <a name="usage"></a><span data-ttu-id="f76ba-120">Использование</span><span class="sxs-lookup"><span data-stu-id="f76ba-120">Usage</span></span>

<span data-ttu-id="f76ba-121">В примере MPEG1Source создается библиотека DLL, которая является сервером COM для источника мультимедиа, обработчиком потока байтов источника мультимедиа и файлом MFT декодера.</span><span class="sxs-lookup"><span data-stu-id="f76ba-121">The MPEG1Source sample builds a DLL that is a COM server for the media source, media source's byte-stream handler, and the decoder MFT.</span></span> <span data-ttu-id="f76ba-122">Прежде чем использовать источник мультимедиа, необходимо зарегистрировать библиотеку DLL.</span><span class="sxs-lookup"><span data-stu-id="f76ba-122">Before using the media source, you must register the DLL.</span></span>

<span data-ttu-id="f76ba-123">Чтобы использовать источник мультимедиа, можно запустить [Пример басикплайбакк](/previous-versions//bb970475(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f76ba-123">To use the media source, you can run the [BasicPlayback Sample](/previous-versions//bb970475(v=vs.85)).</span></span> <span data-ttu-id="f76ba-124">Сопоставитель источника автоматически загрузит источник мультимедиа, если для воспроизведения выбран файл MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="f76ba-124">The source resolver will automatically load the media source if you select an MPEG-1 file for playback.</span></span> <span data-ttu-id="f76ba-125">(При возникновении ошибки убедитесь, что библиотека DLL MPEG1Source успешно зарегистрирована.)</span><span class="sxs-lookup"><span data-stu-id="f76ba-125">(If an error occurs, make sure that you successfully registered the MPEG1Source DLL.)</span></span>

<span data-ttu-id="f76ba-126">Можно также использовать средство Топоедит для создания топологии воспроизведения, содержащей источник мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f76ba-126">You can also use the TopoEdit tool to build a playback topology that contains the media source.</span></span> <span data-ttu-id="f76ba-127">Дополнительные сведения о Топоедит см. в разделе [топоедит](topoedit.md).</span><span class="sxs-lookup"><span data-stu-id="f76ba-127">For more information about TopoEdit, see [TopoEdit](topoedit.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f76ba-128">Требования</span><span class="sxs-lookup"><span data-stu-id="f76ba-128">Requirements</span></span>



| <span data-ttu-id="f76ba-129">Продукт</span><span class="sxs-lookup"><span data-stu-id="f76ba-129">Product</span></span>                                                        | <span data-ttu-id="f76ba-130">Version</span><span class="sxs-lookup"><span data-stu-id="f76ba-130">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="f76ba-131">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="f76ba-131">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="f76ba-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f76ba-132">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="f76ba-133">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="f76ba-133">Downloading the Sample</span></span>

<span data-ttu-id="f76ba-134">Этот пример доступен в [репозитории GitHub с классическими примерами Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mpeg1source).</span><span class="sxs-lookup"><span data-stu-id="f76ba-134">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mpeg1source).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f76ba-135">См. также</span><span class="sxs-lookup"><span data-stu-id="f76ba-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f76ba-136">Примеры пакетов SDK Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f76ba-136">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="f76ba-137">Источники мультимедиа</span><span class="sxs-lookup"><span data-stu-id="f76ba-137">Media Sources</span></span>](media-sources.md)
</dt> <dt>

[<span data-ttu-id="f76ba-138">Обработчики схем и обработчики Byte-Stream</span><span class="sxs-lookup"><span data-stu-id="f76ba-138">Scheme Handlers and Byte-Stream Handlers</span></span>](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[<span data-ttu-id="f76ba-139">Учебник. запись пользовательского источника мультимедиа</span><span class="sxs-lookup"><span data-stu-id="f76ba-139">Tutorial: Writing a Custom Media Source</span></span>](tutorial--writing-a-custom-media-source.md)
</dt> <dt>

[<span data-ttu-id="f76ba-140">Пример Вавсаурце</span><span class="sxs-lookup"><span data-stu-id="f76ba-140">WavSource Sample</span></span>](wavsource-sample.md)
</dt> </dl>

 

 
