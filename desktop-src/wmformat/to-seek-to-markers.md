---
title: Поиск маркеров
description: Поиск маркеров
ms.assetid: 2d5efebf-dcbd-4fb8-933e-cc6d3a99adf8
keywords:
- Расширенный системный формат (ASF), Поиск маркеров
- ASF (Расширенный системный формат), Поиск маркеров
- Расширенный системный формат (ASF), асинхронный читатель
- ASF (Расширенный системный формат), асинхронный читатель
- Расширенный формат систем (ASF), маркеры
- ASF (Расширенный системный формат), маркеры
- асинхронные читатели, Поиск маркеров
- асинхронные читатели, маркеры
- маркеры, Поиск
- маркеры, асинхронные читатели
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16cb4fef99a5c735a12f03f8d2e962d6caf9c2a
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/25/2020
ms.locfileid: "105700829"
---
# <a name="to-seek-to-markers"></a><span data-ttu-id="1bd1e-113">Поиск маркеров</span><span class="sxs-lookup"><span data-stu-id="1bd1e-113">To Seek to Markers</span></span>

<span data-ttu-id="1bd1e-114">Маркер — это именованное расположение в файле ASF.</span><span class="sxs-lookup"><span data-stu-id="1bd1e-114">A marker is a named location in an ASF file.</span></span> <span data-ttu-id="1bd1e-115">Воспроизведение можно запустить только из расположения маркера с помощью асинхронного модуля чтения.</span><span class="sxs-lookup"><span data-stu-id="1bd1e-115">You can only start playback from the location of a marker by using the asynchronous reader.</span></span> <span data-ttu-id="1bd1e-116">Чтобы начать воспроизведение на маркере, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1bd1e-116">You can begin playback at a marker by following these steps.</span></span>

1.  <span data-ttu-id="1bd1e-117">Вызовите метод **ивмреадер:: QueryInterface** , чтобы получить указатель на интерфейс [**ивмхеадеринфо**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) .</span><span class="sxs-lookup"><span data-stu-id="1bd1e-117">Call **IWMReader::QueryInterface** to obtain a pointer to the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface.</span></span>
2.  <span data-ttu-id="1bd1e-118">Получите общее число маркеров в файле, вызвав [**ивмхеадеринфо:: жетмаркеркаунт**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount).</span><span class="sxs-lookup"><span data-stu-id="1bd1e-118">Retrieve the total number of markers in the file by calling [**IWMHeaderInfo::GetMarkerCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount).</span></span>
3.  <span data-ttu-id="1bd1e-119">Пройдите по маркерам, используя счетчик маркеров, полученный на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="1bd1e-119">Loop through the markers, using the marker count retrieved in step 2.</span></span> <span data-ttu-id="1bd1e-120">Извлеките имя и время каждого маркера, вызвав [**ивмхеадеринфо:: Mark**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker) для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="1bd1e-120">Retrieve the name and time of each marker by calling [**IWMHeaderInfo::GetMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker) for each.</span></span> <span data-ttu-id="1bd1e-121">Сохраните индекс нужного маркера.</span><span class="sxs-lookup"><span data-stu-id="1bd1e-121">Save the index of the desired marker.</span></span>
4.  <span data-ttu-id="1bd1e-122">Вызовите метод **ивмреадер:: QueryInterface** , чтобы получить указатель на интерфейс [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) .</span><span class="sxs-lookup"><span data-stu-id="1bd1e-122">Call **IWMReader::QueryInterface** to obtain a pointer to the [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) interface.</span></span>
5.  <span data-ttu-id="1bd1e-123">Укажите маркер, с которого следует начать воспроизведение, вызвав [**IWMReaderAdvanced2:: стартатмаркер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker).</span><span class="sxs-lookup"><span data-stu-id="1bd1e-123">Specify the marker at which to start playback by calling [**IWMReaderAdvanced2::StartAtMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker).</span></span> <span data-ttu-id="1bd1e-124">Необходимо передать индекс нужного маркера, который был сохранен на шаге 3.</span><span class="sxs-lookup"><span data-stu-id="1bd1e-124">You must pass the index of the desired marker, which you saved in step 3.</span></span>
6.  <span data-ttu-id="1bd1e-125">Обработайте примеры, как обычно в реализации метода [**ивмреадеркаллбакк:: OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) .</span><span class="sxs-lookup"><span data-stu-id="1bd1e-125">Handle the samples as you normally would in your implementation of the [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1bd1e-126">См. также</span><span class="sxs-lookup"><span data-stu-id="1bd1e-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1bd1e-127">**Метки**</span><span class="sxs-lookup"><span data-stu-id="1bd1e-127">**Markers**</span></span>](markers.md)
</dt> <dt>

[<span data-ttu-id="1bd1e-128">**Чтение файлов с помощью асинхронного модуля чтения**</span><span class="sxs-lookup"><span data-stu-id="1bd1e-128">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="1bd1e-129">**Работа с индексами**</span><span class="sxs-lookup"><span data-stu-id="1bd1e-129">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




