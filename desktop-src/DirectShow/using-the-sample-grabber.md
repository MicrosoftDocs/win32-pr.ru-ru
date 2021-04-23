---
description: Образец фильтра захвата — это фильтр преобразования, который можно использовать для извлечения примеров мультимедиа из потока по мере их прохождения через граф фильтра.
ms.assetid: ec0e367e-9ef9-4de6-9132-b462c233bc98
title: Использование образца захвата
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4886c796691e83e02b58ddea129d60d5004c9f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673986"
---
# <a name="using-the-sample-grabber"></a><span data-ttu-id="6b69b-103">Использование образца захвата</span><span class="sxs-lookup"><span data-stu-id="6b69b-103">Using the Sample Grabber</span></span>

<span data-ttu-id="6b69b-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="6b69b-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="6b69b-105">[**Образец фильтра захвата**](sample-grabber-filter.md) — это фильтр преобразования, который можно использовать для извлечения примеров мультимедиа из потока по мере их прохождения через граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="6b69b-105">The [**Sample Grabber**](sample-grabber-filter.md) filter is a transform filter that can be used to grab media samples from a stream as they pass through the filter graph.</span></span>

<span data-ttu-id="6b69b-106">Если нужно просто извлечь точечный рисунок из видеофайла, проще использовать объект [детектора мультимедиа (медиадет)](media-detector--mediadet.md) .</span><span class="sxs-lookup"><span data-stu-id="6b69b-106">If you simply want to grab a bitmap from a video file, it is easier to use the [Media Detector (MediaDet)](media-detector--mediadet.md) object.</span></span> <span data-ttu-id="6b69b-107">Дополнительные сведения см. в разделе Получение [кадра афиши](grabbing-a-poster-frame.md) .</span><span class="sxs-lookup"><span data-stu-id="6b69b-107">See [Grabbing a Poster Frame](grabbing-a-poster-frame.md) for details.</span></span> <span data-ttu-id="6b69b-108">Тем не менее, образец захвата является более гибким, так как он работает практически с любым типом мультимедиа (см. раздел [**исамплеграббер:: сетмедиатипе**](isamplegrabber-setmediatype.md) для некоторых исключений) и обеспечивает больший контроль над приложением.</span><span class="sxs-lookup"><span data-stu-id="6b69b-108">The Sample Grabber is more flexible, however, because it works with nearly any media type (see [**ISampleGrabber::SetMediaType**](isamplegrabber-setmediatype.md) for the few exceptions), and offers more control to the application.</span></span>

-   [<span data-ttu-id="6b69b-109">Создание диспетчера графа фильтров</span><span class="sxs-lookup"><span data-stu-id="6b69b-109">Create the Filter Graph Manager</span></span>](#create-the-filter-graph-manager)
-   [<span data-ttu-id="6b69b-110">Добавление образца захвата к графу фильтра</span><span class="sxs-lookup"><span data-stu-id="6b69b-110">Add the Sample Grabber to the Filter Graph</span></span>](#add-the-sample-grabber-to-the-filter-graph)
-   [<span data-ttu-id="6b69b-111">Задание типа носителя</span><span class="sxs-lookup"><span data-stu-id="6b69b-111">Set the Media Type</span></span>](#set-the-media-type)
-   [<span data-ttu-id="6b69b-112">Создание графа фильтра</span><span class="sxs-lookup"><span data-stu-id="6b69b-112">Build the Filter Graph</span></span>](#build-the-filter-graph)
-   [<span data-ttu-id="6b69b-113">Запуск графа</span><span class="sxs-lookup"><span data-stu-id="6b69b-113">Run the Graph</span></span>](#run-the-graph)
-   [<span data-ttu-id="6b69b-114">Взять пример</span><span class="sxs-lookup"><span data-stu-id="6b69b-114">Grab the Sample</span></span>](#grab-the-sample)
-   [<span data-ttu-id="6b69b-115">Пример кода</span><span class="sxs-lookup"><span data-stu-id="6b69b-115">Example Code</span></span>](#example-code)
-   [<span data-ttu-id="6b69b-116">См. также</span><span class="sxs-lookup"><span data-stu-id="6b69b-116">Related topics</span></span>](#related-topics)

## <a name="create-the-filter-graph-manager"></a><span data-ttu-id="6b69b-117">Создание диспетчера графа фильтров</span><span class="sxs-lookup"><span data-stu-id="6b69b-117">Create the Filter Graph Manager</span></span>

<span data-ttu-id="6b69b-118">Для начала создайте [Диспетчер графа фильтров](filter-graph-manager.md) и запросите интерфейсы [**имедиаконтрол**](/windows/desktop/api/Control/nn-control-imediacontrol) и [**имедиаевентекс**](/windows/desktop/api/Control/nn-control-imediaeventex) .</span><span class="sxs-lookup"><span data-stu-id="6b69b-118">To start, create the [Filter Graph Manager](filter-graph-manager.md) and query for the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) and [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) interfaces.</span></span>


```C++
    IGraphBuilder *pGraph = NULL;
    IMediaControl *pControl = NULL;
    IMediaEventEx *pEvent = NULL;


    HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
        CLSCTX_INPROC_SERVER,IID_PPV_ARGS(&pGraph));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pControl));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pEvent));
    if (FAILED(hr))
    {
        goto done;
    }
```





## <a name="add-the-sample-grabber-to-the-filter-graph"></a><span data-ttu-id="6b69b-119">Добавление образца захвата к графу фильтра</span><span class="sxs-lookup"><span data-stu-id="6b69b-119">Add the Sample Grabber to the Filter Graph</span></span>

<span data-ttu-id="6b69b-120">Создайте экземпляр фильтра захвата образца и аддит на графе фильтра.</span><span class="sxs-lookup"><span data-stu-id="6b69b-120">Create an instance of the Sample Grabber filter and addit to the filter graph.</span></span> <span data-ttu-id="6b69b-121">Запросите образец фильтра захвата для интерфейса [**исамплеграббер**](isamplegrabber.md) .</span><span class="sxs-lookup"><span data-stu-id="6b69b-121">Query the Sample Grabber filter for the [**ISampleGrabber**](isamplegrabber.md) interface.</span></span>


```C++
    IBaseFilter *pGrabberF = NULL;
    ISampleGrabber *pGrabber = NULL;


    // Create the Sample Grabber filter.
    hr = CoCreateInstance(CLSID_SampleGrabber, NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&pGrabberF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pGrabberF, L&quot;Sample Grabber&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabberF->QueryInterface(IID_PPV_ARGS(&pGrabber));
    if (FAILED(hr))
    {
        goto done;
    }
```





## <a name="set-the-media-type"></a><span data-ttu-id="6b69b-122">Задание типа носителя</span><span class="sxs-lookup"><span data-stu-id="6b69b-122">Set the Media Type</span></span>

<span data-ttu-id="6b69b-123">При первом создании образца захвата не имеет предпочтительного типа носителя.</span><span class="sxs-lookup"><span data-stu-id="6b69b-123">When you first create the Sample Grabber, it has no preferred media type.</span></span> <span data-ttu-id="6b69b-124">Это означает, что вы можете подключиться почти к любому фильтру в графе, но вы не сможете контролировать тип полученных данных.</span><span class="sxs-lookup"><span data-stu-id="6b69b-124">This means you can connect to almost any filter in the graph, but you would have no control over the type of data that it received.</span></span> <span data-ttu-id="6b69b-125">Перед построением остальной части графа необходимо задать тип мультимедиа для образца захвата, вызвав метод [**исамплеграббер:: сетмедиатипе**](isamplegrabber-setmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="6b69b-125">Before building the rest of the graph, therefore, you must set a media type for the Sample Grabber, by calling the [**ISampleGrabber::SetMediaType**](isamplegrabber-setmediatype.md) method.</span></span>

<span data-ttu-id="6b69b-126">При подключении образца захвата будет сравнивать этот тип носителя с типом мультимедиа, предлагаемым другим фильтром.</span><span class="sxs-lookup"><span data-stu-id="6b69b-126">When the Sample Grabber connects, it will compare this media type against the media type offered by the other filter.</span></span> <span data-ttu-id="6b69b-127">Единственные поля, которые он проверяет, — основной тип, подтип и тип формата.</span><span class="sxs-lookup"><span data-stu-id="6b69b-127">The only fields that it checks are the major type, subtype, and format type.</span></span> <span data-ttu-id="6b69b-128">Для любого из этих значений GUID значения \_ null означает "принимать любое значение".</span><span class="sxs-lookup"><span data-stu-id="6b69b-128">For any of these, the value GUID\_NULL means "accept any value."</span></span> <span data-ttu-id="6b69b-129">В большинстве случаев потребуется задать основной тип и подтип.</span><span class="sxs-lookup"><span data-stu-id="6b69b-129">Most of the time, you will want to set the major type and subtype.</span></span> <span data-ttu-id="6b69b-130">Например, в следующем коде указано несжатое 24-разрядное видео RGB:</span><span class="sxs-lookup"><span data-stu-id="6b69b-130">For example, the following code specifies uncompressed 24-bit RGB video:</span></span>


```C++
    AM_MEDIA_TYPE mt;
    ZeroMemory(&mt, sizeof(mt));
    mt.majortype = MEDIATYPE_Video;
    mt.subtype = MEDIASUBTYPE_RGB24;

    hr = pGrabber->SetMediaType(&mt);
    if (FAILED(hr))
    {
        goto done;
    }
```



## <a name="build-the-filter-graph"></a><span data-ttu-id="6b69b-131">Создание графа фильтра</span><span class="sxs-lookup"><span data-stu-id="6b69b-131">Build the Filter Graph</span></span>

<span data-ttu-id="6b69b-132">Теперь можно построить оставшуюся часть графа фильтра.</span><span class="sxs-lookup"><span data-stu-id="6b69b-132">Now you can build the rest of the filter graph.</span></span> <span data-ttu-id="6b69b-133">Так как образец захвата будет подключаться только с помощью указанного типа носителя, это позволяет использовать преимущества [интеллектуальных механизмов соединения](intelligent-connect.md) диспетчера графа фильтров при построении графа.</span><span class="sxs-lookup"><span data-stu-id="6b69b-133">Because the Sample Grabber will only connect using the media type you have specified, this lets you take advantage of the Filter Graph Manager's [Intelligent Connect](intelligent-connect.md) mechanisms when you build the graph.</span></span>

<span data-ttu-id="6b69b-134">Например, если указано несжатое видео, можно подключить фильтр источника к образцу области захвата, а диспетчер графа фильтров автоматически добавит средство синтаксического анализа файлов и декодера.</span><span class="sxs-lookup"><span data-stu-id="6b69b-134">For example, if you specified uncompressed video, you can connect a source filter to the Sample Grabber, and the Filter Graph Manager will automatically add the file parser and the decoder.</span></span> <span data-ttu-id="6b69b-135">В следующем примере используется вспомогательная функция Коннектфилтерс, которая указана в [подсоединении двух фильтров](connect-two-filters.md):</span><span class="sxs-lookup"><span data-stu-id="6b69b-135">The following example uses the ConnectFilters helper function, which is listed in [Connect Two Filters](connect-two-filters.md):</span></span>


```C++
    IBaseFilter *pSourceF = NULL;
    IEnumPins *pEnum = NULL;
    IPin *pPin = NULL;


    hr = pGraph->AddSourceFilter(pszVideoFile, L&quot;Source&quot;, &pSourceF);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSourceF->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        goto done;
    }

    while (S_OK == pEnum->Next(1, &pPin, NULL))
    {
        hr = ConnectFilters(pGraph, pPin, pGrabberF);
        SafeRelease(&pPin);
        if (SUCCEEDED(hr))
        {
            break;
        }
    }

    if (FAILED(hr))
    {
        goto done;
    }
```





<span data-ttu-id="6b69b-136">Образец захвата представляет собой фильтр преобразования, поэтому выходной ПИН-код должен быть подключен к другому фильтру.</span><span class="sxs-lookup"><span data-stu-id="6b69b-136">The Sample Grabber is a transform filter, so the output pin must be connected to another filter.</span></span> <span data-ttu-id="6b69b-137">Часто вы можете просто отбросить образцы после завершения их выполнения.</span><span class="sxs-lookup"><span data-stu-id="6b69b-137">Often, you may simply want to discard the samples after you are done with them.</span></span> <span data-ttu-id="6b69b-138">В этом случае подключите образец захвата к [**фильтру визуализации NULL**](null-renderer-filter.md), который отклоняет полученные данные.</span><span class="sxs-lookup"><span data-stu-id="6b69b-138">In that case, connect the Sample Grabber to the [**Null Renderer Filter**](null-renderer-filter.md), which discards the data that it receives.</span></span>

<span data-ttu-id="6b69b-139">В следующем примере показана связь образца захвата с фильтром визуализации NULL:</span><span class="sxs-lookup"><span data-stu-id="6b69b-139">The following example connects the Sample Grabber to the Null Renderer filter:</span></span>


```C++
    IBaseFilter *pNullF = NULL;


    hr = CoCreateInstance(CLSID_NullRenderer, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pNullF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pNullF, L&quot;Null Filter&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = ConnectFilters(pGraph, pGrabberF, pNullF);
    if (FAILED(hr))
    {
        goto done;
    }
```





<span data-ttu-id="6b69b-140">Имейте в виду, что размещение образца захвата между видеодекодером и модулем визуализации видео может значительно повредить производительность визуализации.</span><span class="sxs-lookup"><span data-stu-id="6b69b-140">Be aware that placing the Sample Grabber between a video decoder and the video renderer can significantly hurt rendering performance.</span></span> <span data-ttu-id="6b69b-141">Образец захвата — это фильтр переноса на месте, который означает, что выходной буфер совпадает с входным буфером.</span><span class="sxs-lookup"><span data-stu-id="6b69b-141">The Sample Grabber is a trans-in-place filter, which means the output buffer is the same as the input buffer.</span></span> <span data-ttu-id="6b69b-142">Для отрисовки видео выходной буфер, скорее всего, находится на графической карте, где операции чтения выполняются намного медленнее, по сравнению с операциями чтения в основной памяти.</span><span class="sxs-lookup"><span data-stu-id="6b69b-142">For video rendering, the output buffer is likely to be located on the graphics card, where read operations are much slower, compared with read operations in main memory.</span></span>

## <a name="run-the-graph"></a><span data-ttu-id="6b69b-143">Запуск графа</span><span class="sxs-lookup"><span data-stu-id="6b69b-143">Run the Graph</span></span>

<span data-ttu-id="6b69b-144">Образец захвата работает в одном из двух режимов:</span><span class="sxs-lookup"><span data-stu-id="6b69b-144">The Sample Grabber operates in one of two modes:</span></span>

-   <span data-ttu-id="6b69b-145">Режим буферизации создает копию каждого примера, прежде чем доставлять пример нисходящий.</span><span class="sxs-lookup"><span data-stu-id="6b69b-145">Buffering mode makes a copy of each sample before delivering the sample downstream.</span></span>
-   <span data-ttu-id="6b69b-146">Режим обратного вызова вызывает определяемую приложением функцию обратного вызова для каждого примера.</span><span class="sxs-lookup"><span data-stu-id="6b69b-146">Callback mode invokes an application-defined callback function on each sample.</span></span>

<span data-ttu-id="6b69b-147">В этой статье описывается режим буферизации.</span><span class="sxs-lookup"><span data-stu-id="6b69b-147">This article describes buffering mode.</span></span> <span data-ttu-id="6b69b-148">(Перед использованием режима обратного вызова имейте в виду, что функция обратного вызова должна быть достаточно ограниченной.</span><span class="sxs-lookup"><span data-stu-id="6b69b-148">(Before using callback mode, be aware that the callback function must be quite limited.</span></span> <span data-ttu-id="6b69b-149">В противном случае это может радикально снизить производительность или даже привести к взаимоблокировкам.</span><span class="sxs-lookup"><span data-stu-id="6b69b-149">Otherwise, it can drastically reduce performance or even cause deadlocks.</span></span> <span data-ttu-id="6b69b-150">Дополнительные сведения см. в разделе [**исамплеграббер:: сеткаллбакк**](isamplegrabber-setcallback.md). Чтобы активировать режим буферизации, вызовите метод [**исамплеграббер:: сетбуфферсамплес**](isamplegrabber-setbuffersamples.md) со значением **true**.</span><span class="sxs-lookup"><span data-stu-id="6b69b-150">For more information, see [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md).) To activate buffering mode, call the [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md) method with the value **TRUE**.</span></span>

<span data-ttu-id="6b69b-151">При необходимости вызовите метод [**исамплеграббер:: сетонешот**](isamplegrabber-setoneshot.md) со значением **true**.</span><span class="sxs-lookup"><span data-stu-id="6b69b-151">Optionally, call the [**ISampleGrabber::SetOneShot**](isamplegrabber-setoneshot.md) method with the value **TRUE**.</span></span> <span data-ttu-id="6b69b-152">Это приводит к остановке образца захвата после получения первого примера носителя, что бывает полезно, если требуется взять один кадр из потока.</span><span class="sxs-lookup"><span data-stu-id="6b69b-152">This causes the Sample Grabber to halt after it receives the first media sample, which is useful if you want to grab a single frame from the stream.</span></span> <span data-ttu-id="6b69b-153">Выполните поиск в нужное время, запустите граф и дождитесь события [**EC \_ Complete**](ec-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="6b69b-153">Seek to the desired time, run the graph, and wait for the [**EC\_COMPLETE**](ec-complete.md) event.</span></span> <span data-ttu-id="6b69b-154">Обратите внимание, что уровень точности кадров зависит от источника.</span><span class="sxs-lookup"><span data-stu-id="6b69b-154">Note that the level of frame accuracy depends on the source.</span></span> <span data-ttu-id="6b69b-155">Например, поиск файла MPEG часто не является точным.</span><span class="sxs-lookup"><span data-stu-id="6b69b-155">For example, seeking an MPEG file is often not frame accurate.</span></span>

<span data-ttu-id="6b69b-156">Чтобы максимально ускорить выполнение графа, включите график часов, как описано в разделе [Настройка часов графа](setting-the-graph-clock.md).</span><span class="sxs-lookup"><span data-stu-id="6b69b-156">To run the graph as fast as possible, turn of the graph clock as described in [Setting the Graph Clock](setting-the-graph-clock.md).</span></span>

<span data-ttu-id="6b69b-157">В следующем примере включается Однофакторный режим и режим буферизации, запускается граф фильтра и происходит ожидание завершения.</span><span class="sxs-lookup"><span data-stu-id="6b69b-157">The following example enables one-shot mode and buffering mode, runs the filter graph, and waits for completion.</span></span>


```C++
    hr = pGrabber->SetOneShot(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->SetBufferSamples(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pControl->Run();
    if (FAILED(hr))
    {
        goto done;
    }

    long evCode;
    hr = pEvent->WaitForCompletion(INFINITE, &evCode);
```



## <a name="grab-the-sample"></a><span data-ttu-id="6b69b-158">Взять пример</span><span class="sxs-lookup"><span data-stu-id="6b69b-158">Grab the Sample</span></span>

<span data-ttu-id="6b69b-159">В режиме буферизации образец захвата сохраняет копию каждого образца.</span><span class="sxs-lookup"><span data-stu-id="6b69b-159">In buffering mode, the Sample Grabber stores a copy of every sample.</span></span> <span data-ttu-id="6b69b-160">Метод [**исамплеграббер:: жеткуррентбуффер**](isamplegrabber-getcurrentbuffer.md) копирует буфер в выделенный вызывающим объектом массив.</span><span class="sxs-lookup"><span data-stu-id="6b69b-160">The [**ISampleGrabber::GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md) method copies the buffer into a caller-allocated array.</span></span> <span data-ttu-id="6b69b-161">Чтобы определить необходимый размер массива, сначала вызовите **жеткуррентбуффер** с **пустым** указателем для адреса массива.</span><span class="sxs-lookup"><span data-stu-id="6b69b-161">To determine the size of the array that is needed, first call **GetCurrentBuffer** with a **NULL** pointer for the array address.</span></span> <span data-ttu-id="6b69b-162">Затем выделите массив и вызовите метод еще раз, чтобы скопировать буфер.</span><span class="sxs-lookup"><span data-stu-id="6b69b-162">Then allocate the array and call the method a second time to copy the buffer.</span></span> <span data-ttu-id="6b69b-163">Следующий пример показывает эти шаги.</span><span class="sxs-lookup"><span data-stu-id="6b69b-163">The following example shows these steps.</span></span>


```C++
    // Find the required buffer size.
    long cbBuffer;
    hr = pGrabber->GetCurrentBuffer(&cbBuffer, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    pBuffer = (BYTE*)CoTaskMemAlloc(cbBuffer);
    if (!pBuffer) 
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    hr = pGrabber->GetCurrentBuffer(&cbBuffer, (long*)pBuffer);
    if (FAILED(hr))
    {
        goto done;
    }
```



<span data-ttu-id="6b69b-164">Необходимо знать точный формат данных в буфере.</span><span class="sxs-lookup"><span data-stu-id="6b69b-164">You will need to know the exact format of the data in the buffer.</span></span> <span data-ttu-id="6b69b-165">Чтобы получить эти сведения, вызовите метод [**исамплеграббер:: жетконнектедмедиатипе**](isamplegrabber-getconnectedmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="6b69b-165">To get this information, call the [**ISampleGrabber::GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md) method.</span></span> <span data-ttu-id="6b69b-166">Этот метод заполняет структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) форматом.</span><span class="sxs-lookup"><span data-stu-id="6b69b-166">This method fills in an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure with the format.</span></span>

<span data-ttu-id="6b69b-167">Для несжатого видеопотока сведения о форматировании содержатся в структуре [**видеоинфохеадер**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="6b69b-167">For an uncompressed video stream, the format information is contained in a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span> <span data-ttu-id="6b69b-168">В следующем примере показано, как получить сведения о форматировании для несжатого видеопотока.</span><span class="sxs-lookup"><span data-stu-id="6b69b-168">The following example shows how to get the format information for an uncompressed video stream.</span></span>


```C++
    // Examine the format block.
    if ((mt.formattype == FORMAT_VideoInfo) && 
        (mt.cbFormat >= sizeof(VIDEOINFOHEADER)) &&
        (mt.pbFormat != NULL)) 
    {
        VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)mt.pbFormat;

        hr = WriteBitmap(pszBitmapFile, &pVih->bmiHeader, 
            mt.cbFormat - SIZE_PREHEADER, pBuffer, cbBuffer);
    }
    else 
    {
        // Invalid format.
        hr = VFW_E_INVALIDMEDIATYPE; 
    }
```



> [!Note]  
> <span data-ttu-id="6b69b-169">Образец захвата не поддерживает [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).</span><span class="sxs-lookup"><span data-stu-id="6b69b-169">The Sample Grabber does not support [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).</span></span>

 

## <a name="example-code"></a><span data-ttu-id="6b69b-170">Пример кода</span><span class="sxs-lookup"><span data-stu-id="6b69b-170">Example Code</span></span>

<span data-ttu-id="6b69b-171">Ниже приведен полный код для предыдущих примеров.</span><span class="sxs-lookup"><span data-stu-id="6b69b-171">Here is the complete code for the previous examples.</span></span>

> [!Note]  
> <span data-ttu-id="6b69b-172">В этом примере функция [саферелеасе](../medfound/saferelease.md) используется для высвобождения указателей интерфейса.</span><span class="sxs-lookup"><span data-stu-id="6b69b-172">This example uses the [SafeRelease](../medfound/saferelease.md) function to release interface pointers.</span></span>

 


```C++
#include <windows.h>
#include <dshow.h>
#include "qedit.h"

template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}



HRESULT WriteBitmap(PCWSTR, BITMAPINFOHEADER*, size_t, BYTE*, size_t);

HRESULT GrabVideoBitmap(PCWSTR pszVideoFile, PCWSTR pszBitmapFile)
{
    IGraphBuilder *pGraph = NULL;
    IMediaControl *pControl = NULL;
    IMediaEventEx *pEvent = NULL;
    IBaseFilter *pGrabberF = NULL;
    ISampleGrabber *pGrabber = NULL;
    IBaseFilter *pSourceF = NULL;
    IEnumPins *pEnum = NULL;
    IPin *pPin = NULL;
    IBaseFilter *pNullF = NULL;

    BYTE *pBuffer = NULL;

    HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
        CLSCTX_INPROC_SERVER,IID_PPV_ARGS(&pGraph));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pControl));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->QueryInterface(IID_PPV_ARGS(&pEvent));
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the Sample Grabber filter.
    hr = CoCreateInstance(CLSID_SampleGrabber, NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&pGrabberF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pGrabberF, L&quot;Sample Grabber&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabberF->QueryInterface(IID_PPV_ARGS(&pGrabber));
    if (FAILED(hr))
    {
        goto done;
    }

    AM_MEDIA_TYPE mt;
    ZeroMemory(&mt, sizeof(mt));
    mt.majortype = MEDIATYPE_Video;
    mt.subtype = MEDIASUBTYPE_RGB24;

    hr = pGrabber->SetMediaType(&mt);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddSourceFilter(pszVideoFile, L&quot;Source&quot;, &pSourceF);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSourceF->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        goto done;
    }

    while (S_OK == pEnum->Next(1, &pPin, NULL))
    {
        hr = ConnectFilters(pGraph, pPin, pGrabberF);
        SafeRelease(&pPin);
        if (SUCCEEDED(hr))
        {
            break;
        }
    }

    if (FAILED(hr))
    {
        goto done;
    }

    hr = CoCreateInstance(CLSID_NullRenderer, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pNullF));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pNullF, L&quot;Null Filter&quot;);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = ConnectFilters(pGraph, pGrabberF, pNullF);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->SetOneShot(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->SetBufferSamples(TRUE);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pControl->Run();
    if (FAILED(hr))
    {
        goto done;
    }

    long evCode;
    hr = pEvent->WaitForCompletion(INFINITE, &evCode);

    // Find the required buffer size.
    long cbBuffer;
    hr = pGrabber->GetCurrentBuffer(&cbBuffer, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    pBuffer = (BYTE*)CoTaskMemAlloc(cbBuffer);
    if (!pBuffer) 
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    hr = pGrabber->GetCurrentBuffer(&cbBuffer, (long*)pBuffer);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGrabber->GetConnectedMediaType(&mt);
    if (FAILED(hr))
    {
        goto done;
    }

    // Examine the format block.
    if ((mt.formattype == FORMAT_VideoInfo) && 
        (mt.cbFormat >= sizeof(VIDEOINFOHEADER)) &&
        (mt.pbFormat != NULL)) 
    {
        VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)mt.pbFormat;

        hr = WriteBitmap(pszBitmapFile, &pVih->bmiHeader, 
            mt.cbFormat - SIZE_PREHEADER, pBuffer, cbBuffer);
    }
    else 
    {
        // Invalid format.
        hr = VFW_E_INVALIDMEDIATYPE; 
    }

    FreeMediaType(mt);

done:
    CoTaskMemFree(pBuffer);
    SafeRelease(&pPin);
    SafeRelease(&pEnum);
    SafeRelease(&pNullF);
    SafeRelease(&pSourceF);
    SafeRelease(&pGrabber);
    SafeRelease(&pGrabberF);
    SafeRelease(&pControl);
    SafeRelease(&pEvent);
    SafeRelease(&pGraph);
    return hr;
};

// Writes a bitmap file
//  pszFileName:  Output file name.
//  pBMI:         Bitmap format information (including pallete).
//  cbBMI:        Size of the BITMAPINFOHEADER, including palette, if present.
//  pData:        Pointer to the bitmap bits.
//  cbData        Size of the bitmap, in bytes.

HRESULT WriteBitmap(PCWSTR pszFileName, BITMAPINFOHEADER *pBMI, size_t cbBMI,
    BYTE *pData, size_t cbData)
{
    HANDLE hFile = CreateFile(pszFileName, GENERIC_WRITE, 0, NULL, 
        CREATE_ALWAYS, 0, NULL);
    if (hFile == NULL)
    {
        return HRESULT_FROM_WIN32(GetLastError());
    }

    BITMAPFILEHEADER bmf = { };

    bmf.bfType = &#39;MB&#39;;
    bmf.bfSize = cbBMI+ cbData + sizeof(bmf); 
    bmf.bfOffBits = sizeof(bmf) + cbBMI; 

    DWORD cbWritten = 0;
    BOOL result = WriteFile(hFile, &bmf, sizeof(bmf), &cbWritten, NULL);
    if (result)
    {
        result = WriteFile(hFile, pBMI, cbBMI, &cbWritten, NULL);
    }
    if (result)
    {
        result = WriteFile(hFile, pData, cbData, &cbWritten, NULL);
    }

    HRESULT hr = result ? S_OK : HRESULT_FROM_WIN32(GetLastError());

    CloseHandle(hFile);

    return hr;
}
```





## <a name="related-topics"></a><span data-ttu-id="6b69b-173">См. также</span><span class="sxs-lookup"><span data-stu-id="6b69b-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b69b-174">Использование служб редактирования DirectShow</span><span class="sxs-lookup"><span data-stu-id="6b69b-174">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 
