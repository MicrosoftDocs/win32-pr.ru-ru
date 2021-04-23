---
description: В этом разделе описывается шаг 3 руководства воспроизведение аудио-и видеороликов в DirectShow.
ms.assetid: 45679c14-2671-420d-9766-61f2b2bb713a
title: Шаг 3. Создание графа фильтра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a770ad823a2578fab88a09cc44a3c7f2be4a4ca8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674178"
---
# <a name="step-3-build-the-filter-graph"></a><span data-ttu-id="8f490-103">Шаг 3. Создание графа фильтра</span><span class="sxs-lookup"><span data-stu-id="8f490-103">Step 3: Build the Filter Graph</span></span>

<span data-ttu-id="8f490-104">В этом разделе описывается шаг 3 руководства [Воспроизведение аудио-и видеороликов в DirectShow](audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="8f490-104">This topic is step 3 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="8f490-105">Полный код приведен в разделе [Пример воспроизведения DirectShow](directshow-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="8f490-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="8f490-106">Следующим шагом является создание графа фильтра для воспроизведения файла мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="8f490-106">The next step is to build a filter graph to play the media file.</span></span>

### <a name="opening-a-media-file"></a><span data-ttu-id="8f490-107">Открытие файла мультимедиа</span><span class="sxs-lookup"><span data-stu-id="8f490-107">Opening a Media File</span></span>

<span data-ttu-id="8f490-108">`DShowPlayer::OpenFile`Метод открывает файл мультимедиа для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="8f490-108">The `DShowPlayer::OpenFile` method opens a media file for playback.</span></span> <span data-ttu-id="8f490-109">Этот метод выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="8f490-109">This method does the following:</span></span>

1.  <span data-ttu-id="8f490-110">Создает новый граф фильтра (пустой).</span><span class="sxs-lookup"><span data-stu-id="8f490-110">Creates a new (empty) filter graph.</span></span>
2.  <span data-ttu-id="8f490-111">Вызывает [**играфбуилдер:: аддсаурцефилтер**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) , чтобы добавить фильтр источника для указанного файла.</span><span class="sxs-lookup"><span data-stu-id="8f490-111">Calls [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) to add a source filter for the specified file.</span></span>
3.  <span data-ttu-id="8f490-112">Отображает потоки в фильтре источника.</span><span class="sxs-lookup"><span data-stu-id="8f490-112">Renders the streams on the source filter.</span></span>


```C++
HRESULT DShowPlayer::OpenFile(PCWSTR pszFileName)
{
    IBaseFilter *pSource = NULL;

    // Create a new filter graph. (This also closes the old one, if any.)
    HRESULT hr = InitializeGraph();
    if (FAILED(hr))
    {
        goto done;
    }
    
    // Add the source filter to the graph.
    hr = m_pGraph->AddSourceFilter(pszFileName, NULL, &pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    // Try to render the streams.
    hr = RenderStreams(pSource);

done:
    if (FAILED(hr))
    {
        TearDownGraph();
    }
    SafeRelease(&pSource);
    return hr;
}
```



### <a name="creating-the-filter-graph-manager"></a><span data-ttu-id="8f490-113">Создание диспетчера графа фильтров</span><span class="sxs-lookup"><span data-stu-id="8f490-113">Creating the Filter Graph Manager</span></span>

<span data-ttu-id="8f490-114">`DShowPlayer::InitializeGraph`Метод создает новый граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="8f490-114">The `DShowPlayer::InitializeGraph` method creates a new filter graph.</span></span> <span data-ttu-id="8f490-115">Этот метод выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="8f490-115">This method does the following:</span></span>

1.  <span data-ttu-id="8f490-116">Вызывает метод [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) для создания нового экземпляра [диспетчера графа фильтров](filter-graph-manager.md).</span><span class="sxs-lookup"><span data-stu-id="8f490-116">Calls [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a new instance of the [Filter Graph Manager](filter-graph-manager.md).</span></span>
2.  <span data-ttu-id="8f490-117">Запрашивает диспетчер графа фильтров для интерфейсов [**имедиаконтрол**](/windows/desktop/api/Control/nn-control-imediacontrol) и [**имедиаевентекс**](/windows/desktop/api/Control/nn-control-imediaeventex) .</span><span class="sxs-lookup"><span data-stu-id="8f490-117">Queries the Filter Graph Manager for the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) and [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) interfaces.</span></span>
3.  <span data-ttu-id="8f490-118">Вызывает [**имедиаевентекс:: сетнотифивиндов**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) для настройки уведомления о событии.</span><span class="sxs-lookup"><span data-stu-id="8f490-118">Calls [**IMediaEventEx::SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) to set up event notification.</span></span> <span data-ttu-id="8f490-119">Дополнительные сведения см. [в разделе уведомление о событии в DirectShow](event-notification-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="8f490-119">For more information, see [Event Notification in DirectShow](event-notification-in-directshow.md).</span></span>


```C++
HRESULT DShowPlayer::InitializeGraph()
{
    TearDownGraph();

    // Create the Filter Graph Manager.
    HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
        CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&m_pGraph));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = m_pGraph->QueryInterface(IID_PPV_ARGS(&m_pControl));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = m_pGraph->QueryInterface(IID_PPV_ARGS(&m_pEvent));
    if (FAILED(hr))
    {
        goto done;
    }

    // Set up event notification.
    hr = m_pEvent->SetNotifyWindow((OAHWND)m_hwnd, WM_GRAPH_EVENT, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    m_state = STATE_STOPPED;

done:
    return hr;
}
```



### <a name="rendering-the-streams"></a><span data-ttu-id="8f490-120">Подготовка потоков</span><span class="sxs-lookup"><span data-stu-id="8f490-120">Rendering the Streams</span></span>

<span data-ttu-id="8f490-121">Следующим шагом является подключение фильтра источника к одному или нескольким фильтрам визуализации.</span><span class="sxs-lookup"><span data-stu-id="8f490-121">The next step is to connect the source filter to one or more renderer filters.</span></span>

<span data-ttu-id="8f490-122">`DShowPlayer::RenderStreams`Метод выполняет следующие действия.</span><span class="sxs-lookup"><span data-stu-id="8f490-122">The `DShowPlayer::RenderStreams` method performs the following steps.</span></span>

1.  <span data-ttu-id="8f490-123">Запрашивает диспетчер графа фильтров для интерфейса [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2) .</span><span class="sxs-lookup"><span data-stu-id="8f490-123">Queries the Filter Graph Manager for the [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2) interface.</span></span>
2.  <span data-ttu-id="8f490-124">Добавляет фильтр модуля обработки видео в граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="8f490-124">Adds a video renderer filter to the filter graph.</span></span>
3.  <span data-ttu-id="8f490-125">Добавляет [Фильтр модуля подготовки отчетов DirectSound](directsound-renderer-filter.md) к графу фильтра для воспроизведения звука.</span><span class="sxs-lookup"><span data-stu-id="8f490-125">Adds the [DirectSound Renderer Filter](directsound-renderer-filter.md) to the filter graph, to support audio playback.</span></span> <span data-ttu-id="8f490-126">Дополнительные сведения о добавлении фильтров к графу фильтра см. в разделе [Добавление фильтра по CLSID](add-a-filter-by-clsid.md).</span><span class="sxs-lookup"><span data-stu-id="8f490-126">For more information about adding filters to the filter graph, see [Add a Filter by CLSID](add-a-filter-by-clsid.md).</span></span>
4.  <span data-ttu-id="8f490-127">Перечисляет выходные контакты в фильтре источника.</span><span class="sxs-lookup"><span data-stu-id="8f490-127">Enumerates the output pins on the source filter.</span></span> <span data-ttu-id="8f490-128">Дополнительные сведения о перечислении ПИН-кодов см. в разделе [перечисление ПИН](enumerating-pins.md)-кодов.</span><span class="sxs-lookup"><span data-stu-id="8f490-128">For more information about enumerating pins, see [Enumerating Pins](enumerating-pins.md).</span></span>
5.  <span data-ttu-id="8f490-129">Для каждого ПИН-кода вызывается метод [**IFilterGraph2:: рендерекс**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-renderex) .</span><span class="sxs-lookup"><span data-stu-id="8f490-129">For each pin, calls the [**IFilterGraph2::RenderEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-renderex) method.</span></span> <span data-ttu-id="8f490-130">Этот метод подключает выходный закрепление к фильтру модуля подготовки отчетов, добавляя промежуточные фильтры (например, декодеры).</span><span class="sxs-lookup"><span data-stu-id="8f490-130">This method connects the output pin to a renderer filter, adding intermediate filters if needed (such as decoders).</span></span>
6.  <span data-ttu-id="8f490-131">Вызывает метод `CVideoRenderer::FinalizeGraph` для завершения инициализации модуля подготовки видео.</span><span class="sxs-lookup"><span data-stu-id="8f490-131">Calls `CVideoRenderer::FinalizeGraph` to finish initializing the video renderer.</span></span>
7.  <span data-ttu-id="8f490-132">Удаляет фильтр модуля [подготовки отчетов DirectSound](directsound-renderer-filter.md) , если этот фильтр не подключен к другому фильтру.</span><span class="sxs-lookup"><span data-stu-id="8f490-132">Removes the [DirectSound Renderer](directsound-renderer-filter.md) filter if that filter is not connected to another filter.</span></span> <span data-ttu-id="8f490-133">Это может произойти, если исходный файл не содержит аудиопоток.</span><span class="sxs-lookup"><span data-stu-id="8f490-133">This can occur if the source file does not contain an audio stream.</span></span>


```C++
// Render the streams from a source filter. 

HRESULT DShowPlayer::RenderStreams(IBaseFilter *pSource)
{
    BOOL bRenderedAnyPin = FALSE;

    IFilterGraph2 *pGraph2 = NULL;
    IEnumPins *pEnum = NULL;
    IBaseFilter *pAudioRenderer = NULL;
    HRESULT hr = m_pGraph->QueryInterface(IID_PPV_ARGS(&pGraph2));
    if (FAILED(hr))
    {
        goto done;
    }

    // Add the video renderer to the graph
    hr = CreateVideoRenderer();
    if (FAILED(hr))
    {
        goto done;
    }

    // Add the DSound Renderer to the graph.
    hr = AddFilterByCLSID(m_pGraph, CLSID_DSoundRender, 
        &pAudioRenderer, L"Audio Renderer");
    if (FAILED(hr))
    {
        goto done;
    }

    // Enumerate the pins on the source filter.
    hr = pSource->EnumPins(&pEnum);
    if (FAILED(hr))
    {
        goto done;
    }

    // Loop through all the pins
    IPin *pPin;
    while (S_OK == pEnum->Next(1, &pPin, NULL))
    {           
        // Try to render this pin. 
        // It's OK if we fail some pins, if at least one pin renders.
        HRESULT hr2 = pGraph2->RenderEx(pPin, AM_RENDEREX_RENDERTOEXISTINGRENDERERS, NULL);

        pPin->Release();
        if (SUCCEEDED(hr2))
        {
            bRenderedAnyPin = TRUE;
        }
    }

    hr = m_pVideo->FinalizeGraph(m_pGraph);
    if (FAILED(hr))
    {
        goto done;
    }

    // Remove the audio renderer, if not used.
    BOOL bRemoved;
    hr = RemoveUnconnectedRenderer(m_pGraph, pAudioRenderer, &bRemoved);

done:
    SafeRelease(&pEnum);
    SafeRelease(&pAudioRenderer);
    SafeRelease(&pGraph2);

    // If we succeeded to this point, make sure we rendered at least one 
    // stream.
    if (SUCCEEDED(hr))
    {
        if (!bRenderedAnyPin)
        {
            hr = VFW_E_CANNOT_RENDER;
        }
    }
    return hr;
}
```



<span data-ttu-id="8f490-134">Ниже приведен код для `RemoveUnconnectedRenderer` функции, который используется в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="8f490-134">Here is the code for the `RemoveUnconnectedRenderer` function, which is used in the previous example.</span></span>


```C++
HRESULT RemoveUnconnectedRenderer(IGraphBuilder *pGraph, IBaseFilter *pRenderer, BOOL *pbRemoved)
{
    IPin *pPin = NULL;

    *pbRemoved = FALSE;

    // Look for a connected input pin on the renderer.

    HRESULT hr = FindConnectedPin(pRenderer, PINDIR_INPUT, &pPin);
    SafeRelease(&pPin);

    // If this function succeeds, the renderer is connected, so we don't remove it.
    // If it fails, it means the renderer is not connected to anything, so
    // we remove it.

    if (FAILED(hr))
    {
        hr = pGraph->RemoveFilter(pRenderer);
        *pbRemoved = TRUE;
    }

    return hr;
}
```



### <a name="releasing-the-filter-graph"></a><span data-ttu-id="8f490-135">Освобождение графа фильтра</span><span class="sxs-lookup"><span data-stu-id="8f490-135">Releasing the Filter Graph</span></span>

<span data-ttu-id="8f490-136">Когда приложение завершает работу, оно должно освободить граф фильтра, как показано в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="8f490-136">When the application exits, it must release the filter graph, as shown in the following code.</span></span>


```C++
void DShowPlayer::TearDownGraph()
{
    // Stop sending event messages
    if (m_pEvent)
    {
        m_pEvent->SetNotifyWindow((OAHWND)NULL, NULL, NULL);
    }

    SafeRelease(&m_pGraph);
    SafeRelease(&m_pControl);
    SafeRelease(&m_pEvent);

    delete m_pVideo;
    m_pVideo = NULL;

    m_state = STATE_NO_GRAPH;
}
```



<span data-ttu-id="8f490-137">Далее. [Шаг 4. Добавление модуля подготовки видео](step-4--add-the-video-renderer.md).</span><span class="sxs-lookup"><span data-stu-id="8f490-137">Next: [Step 4: Add the Video Renderer](step-4--add-the-video-renderer.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8f490-138">См. также</span><span class="sxs-lookup"><span data-stu-id="8f490-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f490-139">Воспроизведение звука и видео в DirectShow</span><span class="sxs-lookup"><span data-stu-id="8f490-139">Audio/Video Playback in DirectShow</span></span>](audio-video-playback-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="8f490-140">Пример воспроизведения DirectShow</span><span class="sxs-lookup"><span data-stu-id="8f490-140">DirectShow Playback Example</span></span>](directshow-playback-example.md)
</dt> <dt>

[<span data-ttu-id="8f490-141">Построение графа фильтра</span><span class="sxs-lookup"><span data-stu-id="8f490-141">Building the Filter Graph</span></span>](building-the-filter-graph.md)
</dt> <dt>

[<span data-ttu-id="8f490-142">Общие методы Graph-Building</span><span class="sxs-lookup"><span data-stu-id="8f490-142">General Graph-Building Techniques</span></span>](general-graph-building-techniques.md)
</dt> </dl>

 

 
