---
description: Пример Вавсаурце
ms.assetid: 905fbba5-0a04-4048-80bd-f8707c4879da
title: Пример Вавсаурце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 050edb9df75032384f93c6e1f37c52e89f14a748
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898690"
---
# <a name="wavsource-sample"></a><span data-ttu-id="76d1c-103">Пример Вавсаурце</span><span class="sxs-lookup"><span data-stu-id="76d1c-103">WavSource Sample</span></span>

<span data-ttu-id="76d1c-104">Показывает, как создать пользовательский источник мультимедиа в Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="76d1c-104">Shows how to create a custom media source in Microsoft Media Foundation.</span></span> <span data-ttu-id="76d1c-105">В примере реализуется источник мультимедиа, который анализирует звуковые файлы WAV.</span><span class="sxs-lookup"><span data-stu-id="76d1c-105">The sample implements a media source that parses .wav audio files.</span></span>

<span data-ttu-id="76d1c-106">Этот пример является относительно простым примером источника мультимедиа:</span><span class="sxs-lookup"><span data-stu-id="76d1c-106">This sample is a relatively simple example of a media source:</span></span>

-   <span data-ttu-id="76d1c-107">Существует только один поток, поэтому нет кода для реализации выбора потоков.</span><span class="sxs-lookup"><span data-stu-id="76d1c-107">There is only one stream, so there is no code to implement stream selection.</span></span>
-   <span data-ttu-id="76d1c-108">Источник мультимедиа не реализует управление скоростью (т. е. Перемотка вперед или обратная воспроизведение).</span><span class="sxs-lookup"><span data-stu-id="76d1c-108">The media source does not implement rate control (that is, fast forward or reverse playback).</span></span>
-   <span data-ttu-id="76d1c-109">Все методы источника и потока реализуются как синхронные методы.</span><span class="sxs-lookup"><span data-stu-id="76d1c-109">All source and stream methods are implemented as synchronous methods.</span></span>
-   <span data-ttu-id="76d1c-110">Так как часть данных WAV-файла является одним блоком несжатого звука PCM, источнику мультимедиа не нужно считывать заголовки пакетов или иным образом анализировать поток во время воспроизведения, кроме считывания начального заголовка [**вавеформат**](/windows/win32/api/mmreg/ns-mmreg-waveformat) .</span><span class="sxs-lookup"><span data-stu-id="76d1c-110">Because the data portion of a .wav file is a single block of uncompressed PCM audio, the media source does not need to read packet headers or otherwise parse the stream during playback, other than reading the initial [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) header.</span></span>

<span data-ttu-id="76d1c-111">Более сложный пример источника мультимедиа см. в [примере MPEG1Source](mpeg1source-sample.md).</span><span class="sxs-lookup"><span data-stu-id="76d1c-111">For a more advanced example of a media source, see the [MPEG1Source Sample](mpeg1source-sample.md).</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="76d1c-112">Продемонстрированные API</span><span class="sxs-lookup"><span data-stu-id="76d1c-112">APIs Demonstrated</span></span>

<span data-ttu-id="76d1c-113">В этом образце демонстрируются следующие интерфейсы Media Foundation:</span><span class="sxs-lookup"><span data-stu-id="76d1c-113">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="76d1c-114">**имфбитестреамхандлер**</span><span class="sxs-lookup"><span data-stu-id="76d1c-114">**IMFByteStreamHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)
-   [<span data-ttu-id="76d1c-115">**имфмедиасаурце**</span><span class="sxs-lookup"><span data-stu-id="76d1c-115">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
-   [<span data-ttu-id="76d1c-116">**имфмедиастреам**</span><span class="sxs-lookup"><span data-stu-id="76d1c-116">**IMFMediaStream**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)

## <a name="usage"></a><span data-ttu-id="76d1c-117">Использование</span><span class="sxs-lookup"><span data-stu-id="76d1c-117">Usage</span></span>

<span data-ttu-id="76d1c-118">В примере Вавсаурце создается библиотека DLL, которая является COM-сервером как для источника мультимедиа, так и для обработчика потока байтов источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="76d1c-118">The WavSource sample builds a DLL that is a COM server for both the media source and media source's byte-stream handler.</span></span> <span data-ttu-id="76d1c-119">Прежде чем использовать источник мультимедиа, необходимо зарегистрировать библиотеку DLL.</span><span class="sxs-lookup"><span data-stu-id="76d1c-119">Before using the media source, you must register the DLL.</span></span>

<span data-ttu-id="76d1c-120">Чтобы использовать источник мультимедиа, можно запустить [басикплайбакк](/previous-versions//bb970475(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="76d1c-120">To use the media source, you can run the [BasicPlayback](/previous-versions//bb970475(v=vs.85)).</span></span> <span data-ttu-id="76d1c-121">Сопоставитель источника автоматически загрузит источник мультимедиа, если выбрать WAV-файл для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="76d1c-121">The source resolver will automatically load the media source if you select a .wav file for playback.</span></span> <span data-ttu-id="76d1c-122">(При возникновении ошибки убедитесь, что библиотека DLL Вавсаурце успешно зарегистрирована.)</span><span class="sxs-lookup"><span data-stu-id="76d1c-122">(If an error occurs, make sure that you successfully registered the WavSource DLL.)</span></span>

<span data-ttu-id="76d1c-123">Можно также использовать средство Топоедит для создания топологии воспроизведения, содержащей источник мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="76d1c-123">You can also use the TopoEdit tool to build a playback topology that contains the media source.</span></span> <span data-ttu-id="76d1c-124">Дополнительные сведения о Топоедит см. в разделе [топоедит](topoedit.md).</span><span class="sxs-lookup"><span data-stu-id="76d1c-124">For more information about TopoEdit, see [TopoEdit](topoedit.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="76d1c-125">Требования</span><span class="sxs-lookup"><span data-stu-id="76d1c-125">Requirements</span></span>



| <span data-ttu-id="76d1c-126">Продукт</span><span class="sxs-lookup"><span data-stu-id="76d1c-126">Product</span></span>                                                        | <span data-ttu-id="76d1c-127">Version</span><span class="sxs-lookup"><span data-stu-id="76d1c-127">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="76d1c-128">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="76d1c-128">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="76d1c-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="76d1c-129">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="76d1c-130">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="76d1c-130">Downloading the Sample</span></span>

<span data-ttu-id="76d1c-131">Этот пример доступен в [репозитории GitHub с классическими примерами Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsource).</span><span class="sxs-lookup"><span data-stu-id="76d1c-131">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsource).</span></span>

## <a name="related-topics"></a><span data-ttu-id="76d1c-132">См. также</span><span class="sxs-lookup"><span data-stu-id="76d1c-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76d1c-133">Примеры пакетов SDK Media Foundation</span><span class="sxs-lookup"><span data-stu-id="76d1c-133">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="76d1c-134">Источники мультимедиа</span><span class="sxs-lookup"><span data-stu-id="76d1c-134">Media Sources</span></span>](media-sources.md)
</dt> <dt>

[<span data-ttu-id="76d1c-135">Пример MPEG1Source</span><span class="sxs-lookup"><span data-stu-id="76d1c-135">MPEG1Source Sample</span></span>](mpeg1source-sample.md)
</dt> <dt>

[<span data-ttu-id="76d1c-136">Обработчики схем и обработчики Byte-Stream</span><span class="sxs-lookup"><span data-stu-id="76d1c-136">Scheme Handlers and Byte-Stream Handlers</span></span>](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[<span data-ttu-id="76d1c-137">Запись пользовательского источника мультимедиа</span><span class="sxs-lookup"><span data-stu-id="76d1c-137">Writing a Custom Media Source</span></span>](writing-a-custom-media-source.md)
</dt> </dl>

 

 
