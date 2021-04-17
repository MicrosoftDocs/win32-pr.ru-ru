---
description: В этом разделе приведен шаг 4 руководства по воспроизведению аудио-и видеороликов в DirectShow.
ms.assetid: 34f35a95-1981-4467-a581-46db96c05224
title: Шаг 4. Добавление модуля подготовки видео
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea17a0622909525f69cf64fd374c8512a8fa9bb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684712"
---
# <a name="step-4-add-the-video-renderer"></a><span data-ttu-id="cbe85-103">Шаг 4. Добавление модуля подготовки видео</span><span class="sxs-lookup"><span data-stu-id="cbe85-103">Step 4: Add the Video Renderer</span></span>

<span data-ttu-id="cbe85-104">В этом разделе приведен шаг 4 руководства по [воспроизведению аудио-и видеороликов в DirectShow](audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="cbe85-104">This topic is step 4 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="cbe85-105">Полный код приведен в разделе [Пример воспроизведения DirectShow](directshow-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="cbe85-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="cbe85-106">DirectShow предоставляет несколько различных фильтров, которые визуализируют видео:</span><span class="sxs-lookup"><span data-stu-id="cbe85-106">DirectShow provides several different filters that render video:</span></span>

-   <span data-ttu-id="cbe85-107">[**Расширенный фильтр модуля подготовки**](enhanced-video-renderer-filter.md) отчетов (Евр)</span><span class="sxs-lookup"><span data-stu-id="cbe85-107">[**Enhanced Video Renderer Filter**](enhanced-video-renderer-filter.md) (EVR)</span></span>
-   <span data-ttu-id="cbe85-108">[Фильтр прорисовки видео 9](video-mixing-renderer-filter-9.md) (VMR-9)</span><span class="sxs-lookup"><span data-stu-id="cbe85-108">[Video Mixing Renderer Filter 9](video-mixing-renderer-filter-9.md) (VMR-9)</span></span>
-   <span data-ttu-id="cbe85-109">[Фильтр визуализации 7 для микширования видео](video-mixing-renderer-filter-7.md) (VMR-7)</span><span class="sxs-lookup"><span data-stu-id="cbe85-109">[Video Mixing Renderer Filter 7](video-mixing-renderer-filter-7.md) (VMR-7)</span></span>

<span data-ttu-id="cbe85-110">Дополнительные сведения о различиях между этими фильтрами см. [в разделе Выбор правильного модуля подготовки видео](choosing-the-right-renderer.md).</span><span class="sxs-lookup"><span data-stu-id="cbe85-110">For more information about the differences between these filters, see [Choosing the Right Video Renderer](choosing-the-right-renderer.md).</span></span>

<span data-ttu-id="cbe85-111">В этом руководстве каждый фильтр модуля подготовки видео упаковывается классом, который абстрагирует некоторые различия между ними.</span><span class="sxs-lookup"><span data-stu-id="cbe85-111">In this tutorial, each video renderer filter is wrapped by a class that abstracts some of the differences between them.</span></span> <span data-ttu-id="cbe85-112">Все эти классы являются производными от абстрактного базового класса с именем `CVideoRenderer` .</span><span class="sxs-lookup"><span data-stu-id="cbe85-112">These classes all derive from an abstract base class named `CVideoRenderer`.</span></span> <span data-ttu-id="cbe85-113">Объявление `CVideoRenderer` показано на [шаге 2: Declare Квидеорендерер и Derived Classes](step-2--declare-cvideorenderer-and-derived-classes.md).</span><span class="sxs-lookup"><span data-stu-id="cbe85-113">The declaration of `CVideoRenderer` is shown in [Step 2: Declare CVideoRenderer and Derived Classes](step-2--declare-cvideorenderer-and-derived-classes.md).</span></span>

<span data-ttu-id="cbe85-114">Следующий метод пытается создать каждый модуль подготовки видео, в свою очередь, начиная с евр, затем VMR-9 и, наконец, VMR-7.</span><span class="sxs-lookup"><span data-stu-id="cbe85-114">The following method tries to create each video renderer in turn, starting with the EVR, then the VMR-9, and finally the VMR-7.</span></span>


```C++
HRESULT DShowPlayer::CreateVideoRenderer()
{
    HRESULT hr = E_FAIL;

    enum { Try_EVR, Try_VMR9, Try_VMR7 };

    for (DWORD i = Try_EVR; i <= Try_VMR7; i++)
    {
        switch (i)
        {
        case Try_EVR:
            m_pVideo = new (std::nothrow) CEVR();
            break;

        case Try_VMR9:
            m_pVideo = new (std::nothrow) CVMR9();
            break;

        case Try_VMR7:
            m_pVideo = new (std::nothrow) CVMR7();
            break;
        }

        if (m_pVideo == NULL)
        {
            hr = E_OUTOFMEMORY;
            break;
        }

        hr = m_pVideo->AddToGraph(m_pGraph, m_hwnd);
        if (SUCCEEDED(hr))
        {
            break;
        }

        delete m_pVideo;
        m_pVideo = NULL;
    }
    return hr;
}

```



### <a name="evr-filter"></a><span data-ttu-id="cbe85-115">Фильтр Евр</span><span class="sxs-lookup"><span data-stu-id="cbe85-115">EVR Filter</span></span>

<span data-ttu-id="cbe85-116">Следующий код создает фильтр Евр и добавляет его в граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="cbe85-116">The following code creates the EVR filter and adds it to the filter graph.</span></span> <span data-ttu-id="cbe85-117">Функция, `AddFilterByCLSID` используемая в этом примере, показана в разделе [Добавление фильтра по CLSID](add-a-filter-by-clsid.md).</span><span class="sxs-lookup"><span data-stu-id="cbe85-117">The function `AddFilterByCLSID` used in this example is shown in the topic [Add a Filter by CLSID](add-a-filter-by-clsid.md).</span></span>


```C++
HRESULT CEVR::AddToGraph(IGraphBuilder *pGraph, HWND hwnd)
{
    IBaseFilter *pEVR = NULL;

    HRESULT hr = AddFilterByCLSID(pGraph, CLSID_EnhancedVideoRenderer, 
        &pEVR, L"EVR");

    if (FAILED(hr))
    {
        goto done;
    }

    hr = InitializeEVR(pEVR, hwnd, &m_pVideoDisplay);
    if (FAILED(hr))
    {
        goto done;
    }

    // Note: Because IMFVideoDisplayControl is a service interface,
    // you cannot QI the pointer to get back the IBaseFilter pointer.
    // Therefore, we need to cache the IBaseFilter pointer.

    m_pEVR = pEVR;
    m_pEVR->AddRef();

done:
    SafeRelease(&pEVR);
    return hr;
}
```



<span data-ttu-id="cbe85-118">`InitializeEVR`Функция инициализирует фильтр Евр.</span><span class="sxs-lookup"><span data-stu-id="cbe85-118">The `InitializeEVR` function initializes the EVR filter.</span></span> <span data-ttu-id="cbe85-119">Эта функция выполняет следующие действия.</span><span class="sxs-lookup"><span data-stu-id="cbe85-119">This function performs the following steps.</span></span>

1.  <span data-ttu-id="cbe85-120">Запрашивает фильтр для интерфейса [**имфжетсервице**](/windows/win32/api/mfidl/nn-mfidl-imfgetservice) .</span><span class="sxs-lookup"><span data-stu-id="cbe85-120">Queries the filter for the [**IMFGetService**](/windows/win32/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span>
2.  <span data-ttu-id="cbe85-121">Вызывает [**имфжетсервице::-Service**](/windows/win32/api/mfidl/nf-mfidl-imfgetservice-getservice) , чтобы получить указатель на интерфейс [**имфвидеодисплайконтрол**](/windows/win32/api/evr/nn-evr-imfvideodisplaycontrol) .</span><span class="sxs-lookup"><span data-stu-id="cbe85-121">Calls [**IMFGetService::GetService**](/windows/win32/api/mfidl/nf-mfidl-imfgetservice-getservice) to get a pointer to the [**IMFVideoDisplayControl**](/windows/win32/api/evr/nn-evr-imfvideodisplaycontrol) interface.</span></span>
3.  <span data-ttu-id="cbe85-122">Вызывает [**имфвидеодисплайконтрол:: сетвидеовиндов**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) для установки окна видео.</span><span class="sxs-lookup"><span data-stu-id="cbe85-122">Calls [**IMFVideoDisplayControl::SetVideoWindow**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) to set the video window.</span></span>
4.  <span data-ttu-id="cbe85-123">Вызывает [**имфвидеодисплайконтрол:: сетаспектратиомоде**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setaspectratiomode) , чтобы настроить Евр для сохранения пропорций видео.</span><span class="sxs-lookup"><span data-stu-id="cbe85-123">Calls [**IMFVideoDisplayControl::SetAspectRatioMode**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setaspectratiomode) to configure the EVR to preserve the video aspect ratio.</span></span>

<span data-ttu-id="cbe85-124">В следующем коде показана `InitializeEVR` функция.</span><span class="sxs-lookup"><span data-stu-id="cbe85-124">The following code shows the `InitializeEVR` function.</span></span>


```C++
HRESULT InitializeEVR( 
    IBaseFilter *pEVR,              // Pointer to the EVR
    HWND hwnd,                      // Clipping window
    IMFVideoDisplayControl** ppDisplayControl
    ) 
{ 
    IMFGetService *pGS = NULL;
    IMFVideoDisplayControl *pDisplay = NULL;

    HRESULT hr = pEVR->QueryInterface(IID_PPV_ARGS(&pGS)); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGS->GetService(MR_VIDEO_RENDER_SERVICE, IID_PPV_ARGS(&pDisplay));
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the clipping window.
    hr = pDisplay->SetVideoWindow(hwnd);
    if (FAILED(hr))
    {
        goto done;
    }

    // Preserve aspect ratio by letter-boxing
    hr = pDisplay->SetAspectRatioMode(MFVideoARMode_PreservePicture);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the IMFVideoDisplayControl pointer to the caller.
    *ppDisplayControl = pDisplay;
    (*ppDisplayControl)->AddRef();

done:
    SafeRelease(&pGS);
    SafeRelease(&pDisplay);
    return hr; 
} 
```



<span data-ttu-id="cbe85-125">После построения графа `DShowPlayer::RenderStreams` вызывает `CVideoRenderer::FinalizeGraph` .</span><span class="sxs-lookup"><span data-stu-id="cbe85-125">After the graph is built, the `DShowPlayer::RenderStreams` calls `CVideoRenderer::FinalizeGraph`.</span></span> <span data-ttu-id="cbe85-126">Этот метод выполняет конечную инициализацию или очистку.</span><span class="sxs-lookup"><span data-stu-id="cbe85-126">This method performs any final initialization or cleanup.</span></span> <span data-ttu-id="cbe85-127">В следующем коде показана `CEVR` Реализация этого метода.</span><span class="sxs-lookup"><span data-stu-id="cbe85-127">The following code shows the `CEVR` implementation of this method.</span></span>


```C++
HRESULT CEVR::FinalizeGraph(IGraphBuilder *pGraph)
{
    if (m_pEVR == NULL)
    {
        return S_OK;
    }

    BOOL bRemoved;
    HRESULT hr = RemoveUnconnectedRenderer(pGraph, m_pEVR, &bRemoved);
    if (bRemoved)
    {
        SafeRelease(&m_pEVR);
        SafeRelease(&m_pVideoDisplay);
    }
    return hr;
}
```



<span data-ttu-id="cbe85-128">Если Евр не соединен ни с каким другим фильтром, этот метод удаляет Евр из графа.</span><span class="sxs-lookup"><span data-stu-id="cbe85-128">If the EVR is not connected to any other filter, this method removes the EVR from the graph.</span></span> <span data-ttu-id="cbe85-129">Это может произойти, если файл мультимедиа не содержит поток видео.</span><span class="sxs-lookup"><span data-stu-id="cbe85-129">This can occur if the media file does not contain a video stream.</span></span>

### <a name="vmr-9-filter"></a><span data-ttu-id="cbe85-130">Фильтр VMR-9</span><span class="sxs-lookup"><span data-stu-id="cbe85-130">VMR-9 Filter</span></span>

<span data-ttu-id="cbe85-131">Следующий код создает фильтр VMR-9 и добавляет его в граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="cbe85-131">The following code creates the VMR-9 filter and adds it to the filter graph.</span></span>


```C++
HRESULT CVMR9::AddToGraph(IGraphBuilder *pGraph, HWND hwnd)
{
    IBaseFilter *pVMR = NULL;

    HRESULT hr = AddFilterByCLSID(pGraph, CLSID_VideoMixingRenderer9, 
        &pVMR, L"VMR-9");
    if (SUCCEEDED(hr))
    {
        // Set windowless mode on the VMR. This must be done before the VMR 
        // is connected.
        hr = InitWindowlessVMR9(pVMR, hwnd, &m_pWindowless);
    }
    SafeRelease(&pVMR);
    return hr;
}
```



<span data-ttu-id="cbe85-132">`InitWindowlessVMR9`Функция инициализирует VMR-9 для режима без окон.</span><span class="sxs-lookup"><span data-stu-id="cbe85-132">The `InitWindowlessVMR9` function initializes the VMR-9 for windowless mode.</span></span> <span data-ttu-id="cbe85-133">(Дополнительные сведения о режиме без окон см. в разделе [режим без окон VMR](vmr-windowless-mode.md).) Эта функция выполняет следующие действия.</span><span class="sxs-lookup"><span data-stu-id="cbe85-133">(For more information about windowless mode, see [VMR Windowless Mode](vmr-windowless-mode.md).) This function performs the following steps.</span></span>

1.  <span data-ttu-id="cbe85-134">Запрашивает фильтр VMR-9 для интерфейса [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) .</span><span class="sxs-lookup"><span data-stu-id="cbe85-134">Queries the VMR-9 filter for the [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) interface.</span></span>
2.  <span data-ttu-id="cbe85-135">Вызывает метод [**IVMRFilterConfig9:: сетрендерингмоде**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) для установки режима без окон.</span><span class="sxs-lookup"><span data-stu-id="cbe85-135">Calls the [**IVMRFilterConfig9::SetRenderingMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) method to set windowless mode.</span></span>
3.  <span data-ttu-id="cbe85-136">Запрашивает фильтр VMR-9 для интерфейса [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) .</span><span class="sxs-lookup"><span data-stu-id="cbe85-136">Queries the VMR-9 filter for the [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) interface.</span></span>
4.  <span data-ttu-id="cbe85-137">Вызывает метод [**IVMRWindowlessControl9:: сетвидеоклиппингвиндов**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow) для установки окна видео.</span><span class="sxs-lookup"><span data-stu-id="cbe85-137">Calls the [**IVMRWindowlessControl9::SetVideoClippingWindow**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow) method to set the video window.</span></span>
5.  <span data-ttu-id="cbe85-138">Вызывает метод [**IVMRWindowlessControl9:: сетаспектратиомоде**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setaspectratiomode) , чтобы сохранить пропорции видео.</span><span class="sxs-lookup"><span data-stu-id="cbe85-138">Calls the [**IVMRWindowlessControl9::SetAspectRatioMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setaspectratiomode) method to preserve the video aspect ratio.</span></span>

<span data-ttu-id="cbe85-139">В следующем коде показана `InitWindowlessVMR9` функция.</span><span class="sxs-lookup"><span data-stu-id="cbe85-139">The following code shows the `InitWindowlessVMR9` function.</span></span>


```C++
HRESULT InitWindowlessVMR9( 
    IBaseFilter *pVMR,              // Pointer to the VMR
    HWND hwnd,                      // Clipping window
    IVMRWindowlessControl9** ppWC   // Receives a pointer to the VMR.
    ) 
{ 

    IVMRFilterConfig9 * pConfig = NULL; 
    IVMRWindowlessControl9 *pWC = NULL;

    // Set the rendering mode.  
    HRESULT hr = pVMR->QueryInterface(IID_PPV_ARGS(&pConfig)); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pConfig->SetRenderingMode(VMR9Mode_Windowless); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Query for the windowless control interface.
    hr = pVMR->QueryInterface(IID_PPV_ARGS(&pWC));
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the clipping window.
    hr = pWC->SetVideoClippingWindow(hwnd);
    if (FAILED(hr))
    {
        goto done;
    }

    // Preserve aspect ratio by letter-boxing
    hr = pWC->SetAspectRatioMode(VMR9ARMode_LetterBox);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the IVMRWindowlessControl pointer to the caller.
    *ppWC = pWC;
    (*ppWC)->AddRef();

done:
    SafeRelease(&pConfig);
    SafeRelease(&pWC);
    return hr; 
} 
```



<span data-ttu-id="cbe85-140">`CVMR9::FinalizeGraph`Метод проверяет, подключен ли фильтр VMR-9, и, если нет, удаляет его из графа фильтра.</span><span class="sxs-lookup"><span data-stu-id="cbe85-140">The `CVMR9::FinalizeGraph` method checks if the VMR-9 filter is connected, and if not, removes it from the filter graph.</span></span>


```C++
HRESULT CVMR9::FinalizeGraph(IGraphBuilder *pGraph)
{
    if (m_pWindowless == NULL)
    {
        return S_OK;
    }

    IBaseFilter *pFilter = NULL;

    HRESULT hr = m_pWindowless->QueryInterface(IID_PPV_ARGS(&pFilter));
    if (FAILED(hr))
    {
        goto done;
    }

    BOOL bRemoved;
    hr = RemoveUnconnectedRenderer(pGraph, pFilter, &bRemoved);

    // If we removed the VMR, then we also need to release our 
    // pointer to the VMR's windowless control interface.
    if (bRemoved)
    {
        SafeRelease(&m_pWindowless);
    }

done:
    SafeRelease(&pFilter);
    return hr;
}
```



### <a name="vmr-7-filter"></a><span data-ttu-id="cbe85-141">Фильтр VMR-7</span><span class="sxs-lookup"><span data-stu-id="cbe85-141">VMR-7 Filter</span></span>

<span data-ttu-id="cbe85-142">Действия фильтра VMR-7 практически идентичны параметрам для VMR-9, за исключением того, что вместо них используются интерфейсы VMR-7.</span><span class="sxs-lookup"><span data-stu-id="cbe85-142">The steps for the VMR-7 filter are nearly identical to those for the VMR-9, except the VMR-7 interfaces are used instead.</span></span> <span data-ttu-id="cbe85-143">Следующий код создает фильтр VMR-7 и добавляет его в граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="cbe85-143">The following code creates the VMR-7 filter and adds it to the filter graph.</span></span>


```C++
HRESULT CVMR7::AddToGraph(IGraphBuilder *pGraph, HWND hwnd)
{
    IBaseFilter *pVMR = NULL;

    HRESULT hr = AddFilterByCLSID(pGraph, CLSID_VideoMixingRenderer, 
        &pVMR, L"VMR-7");

    if (SUCCEEDED(hr))
    {
        // Set windowless mode on the VMR. This must be done before the VMR
        // is connected.
        hr = InitWindowlessVMR(pVMR, hwnd, &m_pWindowless);
    }
    SafeRelease(&pVMR);
    return hr;
}
```



<span data-ttu-id="cbe85-144">`InitWindowlessVMR`Функция инициализирует VMR-7 для режима без окон.</span><span class="sxs-lookup"><span data-stu-id="cbe85-144">The `InitWindowlessVMR` function initializes the VMR-7 for windowless mode.</span></span> <span data-ttu-id="cbe85-145">Эта функция выполняет следующие действия.</span><span class="sxs-lookup"><span data-stu-id="cbe85-145">This function performs the following steps.</span></span>

1.  <span data-ttu-id="cbe85-146">Запрашивает фильтр VMR-7 для интерфейса [**ивмрфилтерконфиг**](/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig) .</span><span class="sxs-lookup"><span data-stu-id="cbe85-146">Queries the VMR-7 filter for the [**IVMRFilterConfig**](/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig) interface.</span></span>
2.  <span data-ttu-id="cbe85-147">Вызывает метод [**ивмрфилтерконфиг:: сетрендерингмоде**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) для установки режима без окон.</span><span class="sxs-lookup"><span data-stu-id="cbe85-147">Calls the [**IVMRFilterConfig::SetRenderingMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) method to set windowless mode.</span></span>
3.  <span data-ttu-id="cbe85-148">Запрашивает фильтр VMR-7 для интерфейса [**ивмрвиндовлессконтрол**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) .</span><span class="sxs-lookup"><span data-stu-id="cbe85-148">Queries the VMR-7 filter for the [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) interface.</span></span>
4.  <span data-ttu-id="cbe85-149">Вызывает метод [**ивмрвиндовлессконтрол:: сетвидеоклиппингвиндов**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) для установки окна видео.</span><span class="sxs-lookup"><span data-stu-id="cbe85-149">Calls the [**IVMRWindowlessControl::SetVideoClippingWindow**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) method to set the video window.</span></span>
5.  <span data-ttu-id="cbe85-150">Вызывает метод [**ивмрвиндовлессконтрол:: сетаспектратиомоде**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setaspectratiomode) , чтобы сохранить пропорции видео.</span><span class="sxs-lookup"><span data-stu-id="cbe85-150">Calls the [**IVMRWindowlessControl::SetAspectRatioMode**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setaspectratiomode) method to preserve the video aspect ratio.</span></span>

<span data-ttu-id="cbe85-151">В следующем коде показана `InitWindowlessVMR` функция.</span><span class="sxs-lookup"><span data-stu-id="cbe85-151">The following code shows the `InitWindowlessVMR` function.</span></span>


```C++
HRESULT InitWindowlessVMR( 
    IBaseFilter *pVMR,              // Pointer to the VMR
    HWND hwnd,                      // Clipping window
    IVMRWindowlessControl** ppWC    // Receives a pointer to the VMR.
    ) 
{ 

    IVMRFilterConfig* pConfig = NULL; 
    IVMRWindowlessControl *pWC = NULL;

    // Set the rendering mode.  
    HRESULT hr = pVMR->QueryInterface(IID_PPV_ARGS(&pConfig)); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pConfig->SetRenderingMode(VMRMode_Windowless); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Query for the windowless control interface.
    hr = pVMR->QueryInterface(IID_PPV_ARGS(&pWC));
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the clipping window.
    hr = pWC->SetVideoClippingWindow(hwnd);
    if (FAILED(hr))
    {
        goto done;
    }

    // Preserve aspect ratio by letter-boxing
    hr = pWC->SetAspectRatioMode(VMR_ARMODE_LETTER_BOX);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the IVMRWindowlessControl pointer to the caller.
    *ppWC = pWC;
    (*ppWC)->AddRef();

done:
    SafeRelease(&pConfig);
    SafeRelease(&pWC);
    return hr; 
} 
```



<span data-ttu-id="cbe85-152">`CVMR7::FinalizeGraph`Метод проверяет, подключен ли фильтр VMR-7, и, если нет, удаляет его из графа фильтра.</span><span class="sxs-lookup"><span data-stu-id="cbe85-152">The `CVMR7::FinalizeGraph` method checks if the VMR-7 filter is connected, and if not, removes it from the filter graph.</span></span>


```C++
HRESULT CVMR7::FinalizeGraph(IGraphBuilder *pGraph)
{
    if (m_pWindowless == NULL)
    {
        return S_OK;
    }

    IBaseFilter *pFilter = NULL;

    HRESULT hr = m_pWindowless->QueryInterface(IID_PPV_ARGS(&pFilter));
    if (FAILED(hr))
    {
        goto done;
    }

    BOOL bRemoved;
    hr = RemoveUnconnectedRenderer(pGraph, pFilter, &bRemoved);

    // If we removed the VMR, then we also need to release our 
    // pointer to the VMR's windowless control interface.
    if (bRemoved)
    {
        SafeRelease(&m_pWindowless);
    }

done:
    SafeRelease(&pFilter);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="cbe85-153">См. также</span><span class="sxs-lookup"><span data-stu-id="cbe85-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbe85-154">Пример воспроизведения DirectShow</span><span class="sxs-lookup"><span data-stu-id="cbe85-154">DirectShow Playback Example</span></span>](directshow-playback-example.md)
</dt> <dt>

[<span data-ttu-id="cbe85-155">Использование фильтра Евр DirectShow</span><span class="sxs-lookup"><span data-stu-id="cbe85-155">Using the DirectShow EVR Filter</span></span>](../medfound/using-the-directshow-evr-filter.md)
</dt> <dt>

[<span data-ttu-id="cbe85-156">Использование модуля подготовки видео для микширования</span><span class="sxs-lookup"><span data-stu-id="cbe85-156">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 
