---
description: В этом разделе описывается шаг 3 руководства воспроизведение аудио-и видеофайлов в DirectShow.
ms.assetid: 45679c14-2671-420d-9766-61f2b2bb713a
title: Шаг 3. Создание фильтра Graph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad4903e08b19e15721c8b62f130261bb4d05fcd94d544380b2e501f56d60704d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072508"
---
# <a name="step-3-build-the-filter-graph"></a>Шаг 3. Создание фильтра Graph

В этом разделе описывается шаг 3 руководства [Воспроизведение аудио-и видеофайлов в DirectShow](audio-video-playback-in-directshow.md). полный код приведен в разделе [пример воспроизведения DirectShow](directshow-playback-example.md).

Следующим шагом является создание графа фильтра для воспроизведения файла мультимедиа.

### <a name="opening-a-media-file"></a>Открытие файла мультимедиа

`DShowPlayer::OpenFile`Метод открывает файл мультимедиа для воспроизведения. Этот метод выполняет следующие действия:

1.  Создает новый граф фильтра (пустой).
2.  Вызывает [**играфбуилдер:: аддсаурцефилтер**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) , чтобы добавить фильтр источника для указанного файла.
3.  Отображает потоки в фильтре источника.


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



### <a name="creating-the-filter-graph-manager"></a>создание фильтра Graph Manager

`DShowPlayer::InitializeGraph`Метод создает новый граф фильтра. Этот метод выполняет следующие действия:

1.  вызывает метод [**cocreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) для создания нового экземпляра [фильтра Graph Manager](filter-graph-manager.md).
2.  запрашивает у фильтра Graph Manager интерфейсы [**имедиаконтрол**](/windows/desktop/api/Control/nn-control-imediacontrol) и [**имедиаевентекс**](/windows/desktop/api/Control/nn-control-imediaeventex) .
3.  Вызывает [**имедиаевентекс:: сетнотифивиндов**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) для настройки уведомления о событии. Дополнительные сведения см. [в разделе уведомление о событии в DirectShow](event-notification-in-directshow.md).


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



### <a name="rendering-the-streams"></a>подготовка к просмотру Потоки

Следующим шагом является подключение фильтра источника к одному или нескольким фильтрам визуализации.

`DShowPlayer::RenderStreams`Метод выполняет следующие действия.

1.  запрашивает Graph диспетчера фильтров для интерфейса [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2) .
2.  Добавляет фильтр модуля обработки видео в граф фильтра.
3.  Добавляет [Фильтр модуля подготовки отчетов DirectSound](directsound-renderer-filter.md) к графу фильтра для воспроизведения звука. Дополнительные сведения о добавлении фильтров к графу фильтра см. в разделе [Добавление фильтра по CLSID](add-a-filter-by-clsid.md).
4.  Перечисляет выходные контакты в фильтре источника. Дополнительные сведения о перечислении ПИН-кодов см. в разделе [перечисление ПИН](enumerating-pins.md)-кодов.
5.  Для каждого ПИН-кода вызывается метод [**IFilterGraph2:: рендерекс**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-renderex) . Этот метод подключает выходный закрепление к фильтру модуля подготовки отчетов, добавляя промежуточные фильтры (например, декодеры).
6.  Вызывает метод `CVideoRenderer::FinalizeGraph` для завершения инициализации модуля подготовки видео.
7.  Удаляет фильтр модуля [подготовки отчетов DirectSound](directsound-renderer-filter.md) , если этот фильтр не подключен к другому фильтру. Это может произойти, если исходный файл не содержит аудиопоток.


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



Ниже приведен код для `RemoveUnconnectedRenderer` функции, который используется в предыдущем примере.


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



### <a name="releasing-the-filter-graph"></a>Освобождение Graph фильтра

Когда приложение завершает работу, оно должно освободить граф фильтра, как показано в следующем коде.


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



Далее. [Шаг 4. Добавление модуля подготовки видео](step-4--add-the-video-renderer.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Воспроизведение звука и видео в DirectShow](audio-video-playback-in-directshow.md)
</dt> <dt>

[DirectShow Пример воспроизведения](directshow-playback-example.md)
</dt> <dt>

[Создание фильтра Graph](building-the-filter-graph.md)
</dt> <dt>

[Общие методы Graph-Building](general-graph-building-techniques.md)
</dt> </dl>

 

 
