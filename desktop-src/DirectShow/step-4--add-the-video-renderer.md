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
# <a name="step-4-add-the-video-renderer"></a>Шаг 4. Добавление модуля подготовки видео

В этом разделе приведен шаг 4 руководства по [воспроизведению аудио-и видеороликов в DirectShow](audio-video-playback-in-directshow.md). Полный код приведен в разделе [Пример воспроизведения DirectShow](directshow-playback-example.md).

DirectShow предоставляет несколько различных фильтров, которые визуализируют видео:

-   [**Расширенный фильтр модуля подготовки**](enhanced-video-renderer-filter.md) отчетов (Евр)
-   [Фильтр прорисовки видео 9](video-mixing-renderer-filter-9.md) (VMR-9)
-   [Фильтр визуализации 7 для микширования видео](video-mixing-renderer-filter-7.md) (VMR-7)

Дополнительные сведения о различиях между этими фильтрами см. [в разделе Выбор правильного модуля подготовки видео](choosing-the-right-renderer.md).

В этом руководстве каждый фильтр модуля подготовки видео упаковывается классом, который абстрагирует некоторые различия между ними. Все эти классы являются производными от абстрактного базового класса с именем `CVideoRenderer` . Объявление `CVideoRenderer` показано на [шаге 2: Declare Квидеорендерер и Derived Classes](step-2--declare-cvideorenderer-and-derived-classes.md).

Следующий метод пытается создать каждый модуль подготовки видео, в свою очередь, начиная с евр, затем VMR-9 и, наконец, VMR-7.


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



### <a name="evr-filter"></a>Фильтр Евр

Следующий код создает фильтр Евр и добавляет его в граф фильтра. Функция, `AddFilterByCLSID` используемая в этом примере, показана в разделе [Добавление фильтра по CLSID](add-a-filter-by-clsid.md).


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



`InitializeEVR`Функция инициализирует фильтр Евр. Эта функция выполняет следующие действия.

1.  Запрашивает фильтр для интерфейса [**имфжетсервице**](/windows/win32/api/mfidl/nn-mfidl-imfgetservice) .
2.  Вызывает [**имфжетсервице::-Service**](/windows/win32/api/mfidl/nf-mfidl-imfgetservice-getservice) , чтобы получить указатель на интерфейс [**имфвидеодисплайконтрол**](/windows/win32/api/evr/nn-evr-imfvideodisplaycontrol) .
3.  Вызывает [**имфвидеодисплайконтрол:: сетвидеовиндов**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) для установки окна видео.
4.  Вызывает [**имфвидеодисплайконтрол:: сетаспектратиомоде**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setaspectratiomode) , чтобы настроить Евр для сохранения пропорций видео.

В следующем коде показана `InitializeEVR` функция.


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



После построения графа `DShowPlayer::RenderStreams` вызывает `CVideoRenderer::FinalizeGraph` . Этот метод выполняет конечную инициализацию или очистку. В следующем коде показана `CEVR` Реализация этого метода.


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



Если Евр не соединен ни с каким другим фильтром, этот метод удаляет Евр из графа. Это может произойти, если файл мультимедиа не содержит поток видео.

### <a name="vmr-9-filter"></a>Фильтр VMR-9

Следующий код создает фильтр VMR-9 и добавляет его в граф фильтра.


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



`InitWindowlessVMR9`Функция инициализирует VMR-9 для режима без окон. (Дополнительные сведения о режиме без окон см. в разделе [режим без окон VMR](vmr-windowless-mode.md).) Эта функция выполняет следующие действия.

1.  Запрашивает фильтр VMR-9 для интерфейса [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) .
2.  Вызывает метод [**IVMRFilterConfig9:: сетрендерингмоде**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) для установки режима без окон.
3.  Запрашивает фильтр VMR-9 для интерфейса [**IVMRWindowlessControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrwindowlesscontrol9) .
4.  Вызывает метод [**IVMRWindowlessControl9:: сетвидеоклиппингвиндов**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoclippingwindow) для установки окна видео.
5.  Вызывает метод [**IVMRWindowlessControl9:: сетаспектратиомоде**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setaspectratiomode) , чтобы сохранить пропорции видео.

В следующем коде показана `InitWindowlessVMR9` функция.


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



`CVMR9::FinalizeGraph`Метод проверяет, подключен ли фильтр VMR-9, и, если нет, удаляет его из графа фильтра.


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



### <a name="vmr-7-filter"></a>Фильтр VMR-7

Действия фильтра VMR-7 практически идентичны параметрам для VMR-9, за исключением того, что вместо них используются интерфейсы VMR-7. Следующий код создает фильтр VMR-7 и добавляет его в граф фильтра.


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



`InitWindowlessVMR`Функция инициализирует VMR-7 для режима без окон. Эта функция выполняет следующие действия.

1.  Запрашивает фильтр VMR-7 для интерфейса [**ивмрфилтерконфиг**](/windows/desktop/api/Strmif/nn-strmif-ivmrfilterconfig) .
2.  Вызывает метод [**ивмрфилтерконфиг:: сетрендерингмоде**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingmode) для установки режима без окон.
3.  Запрашивает фильтр VMR-7 для интерфейса [**ивмрвиндовлессконтрол**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) .
4.  Вызывает метод [**ивмрвиндовлессконтрол:: сетвидеоклиппингвиндов**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoclippingwindow) для установки окна видео.
5.  Вызывает метод [**ивмрвиндовлессконтрол:: сетаспектратиомоде**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setaspectratiomode) , чтобы сохранить пропорции видео.

В следующем коде показана `InitWindowlessVMR` функция.


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



`CVMR7::FinalizeGraph`Метод проверяет, подключен ли фильтр VMR-7, и, если нет, удаляет его из графа фильтра.


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Пример воспроизведения DirectShow](directshow-playback-example.md)
</dt> <dt>

[Использование фильтра Евр DirectShow](../medfound/using-the-directshow-evr-filter.md)
</dt> <dt>

[Использование модуля подготовки видео для микширования](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 
