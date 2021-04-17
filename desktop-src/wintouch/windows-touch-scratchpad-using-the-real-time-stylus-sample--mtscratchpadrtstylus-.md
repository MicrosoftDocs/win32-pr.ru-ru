---
title: Блокнот для сенсорного ввода Windows с помощью примера пера в режиме реального времени (C++)
description: Пример использования сенсорного ввода Windows (Мтскратчпадртстилус) демонстрирует использование сообщений Windows Touch для рисования трассировок точек касания в окне.
ms.assetid: c72ddc71-48b7-4c26-af2b-10919038eaf8
keywords:
- Windows Touch, примеры кода
- Windows Touch, пример кода
- Касание Windows, образцы для ввода пометок
- Образцы для ввода пометок
- Сенсорный экран Windows, объект пера в режиме реального времени (RTS)
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: 94d425bcb39dd35d3bd71636fb19b6b408af9477
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "105710236"
---
# <a name="windows-touch-scratchpad-using-the-real-time-stylus-sample-c"></a>Блокнот для сенсорного ввода Windows с помощью примера пера в режиме реального времени (C++)

Пример использования сенсорного ввода Windows ([мтскратчпадртстилус](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp)) демонстрирует использование сообщений Windows Touch для рисования трассировок точек касания в окне. Трассировка основного пальца, который был размещен на дигитайзере, сначала рисуется черным цветом. Дополнительные пальцы рисуются шестью цветами: красный, зеленый, синий, голубой, пурпурный и желтый. На следующем снимке экрана показано, как приложение может выглядеть при выполнении.

![снимок экрана с примером сенсорного ввода-вывода Windows с помощью пера в режиме реального времени с зеленым, красным, черным цветом и синей линией на экране](images/mtscratchpadrtstylus.png)

В этом примере создается объект пера в режиме реального времени, а также включается поддержка нескольких точек контакта. Подключаемый модуль DynamicRenderer добавляется в RTS для отображения содержимого. Подключаемый модуль, **ксинцевенсандлерртс**, реализуется для наблюдения за количеством пальцев и изменения цвета, который рисуется динамическим модулем визуализации. При использовании обоих подключаемых модулей в стеке Plug-in RTS приложение Windows Touch помещает основное контактное лицо в черный, а остальные контакты — по различным цветам.

В следующем коде показано, как создается объект RTS с поддержкой нескольких точек контакта.

```C++
IRealTimeStylus* CreateRealTimeStylus(HWND hWnd)
{
    // Check input argument
    if (hWnd == NULL)
    {
        ASSERT(hWnd && L"CreateRealTimeStylus: invalid argument hWnd");
        return NULL;
    }

    // Create RTS object
    IRealTimeStylus* pRealTimeStylus = NULL;
    HRESULT hr = CoCreateInstance(CLSID_RealTimeStylus, NULL, CLSCTX_ALL, IID_PPV_ARGS(&pRealTimeStylus));
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateRealTimeStylus: failed to CoCreateInstance of RealTimeStylus");
        return NULL;
    }

    // Attach RTS object to a window
    hr = pRealTimeStylus->put_HWND((HANDLE_PTR)hWnd);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateRealTimeStylus: failed to set window handle");
        pRealTimeStylus->Release();
        return NULL;
    }

    // Register RTS object for receiving multi-touch input.
    IRealTimeStylus3* pRealTimeStylus3 = NULL;
    hr = pRealTimeStylus->QueryInterface(&pRealTimeStylus3);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateRealTimeStylus: cannot access IRealTimeStylus3");
        pRealTimeStylus->Release();
        return NULL;
    }
    hr = pRealTimeStylus3->put_MultiTouchEnabled(TRUE);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateRealTimeStylus: failed to enable multi-touch");
        pRealTimeStylus->Release();
        pRealTimeStylus3->Release();
        return NULL;
    }
    pRealTimeStylus3->Release();

    return pRealTimeStylus;
}
```

В следующем коде показано, как создается подключаемый модуль динамического рендеринга и добавляется в RTS.

```C++
IDynamicRenderer* CreateDynamicRenderer(IRealTimeStylus* pRealTimeStylus)
{
    // Check input argument
    if (pRealTimeStylus == NULL)
    {
        ASSERT(pRealTimeStylus && L"CreateDynamicRenderer: invalid argument RealTimeStylus");
        return NULL;
    }

    // Get window handle from RTS object
    HWND hWnd = NULL;
    HRESULT hr = pRealTimeStylus->get_HWND((HANDLE_PTR*)&hWnd);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateDynamicRenderer: failed to get window handle");
        return NULL;
    }

    // Create DynamicRenderer object
    IDynamicRenderer* pDynamicRenderer = NULL;
    hr = CoCreateInstance(CLSID_DynamicRenderer, NULL, CLSCTX_ALL, IID_PPV_ARGS(&pDynamicRenderer));
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateDynamicRenderer: failed to CoCreateInstance of DynamicRenderer");
        return NULL;
    }

    // Add DynamicRenderer to the RTS object as a synchronous plugin
    IStylusSyncPlugin* pSyncDynamicRenderer = NULL;
    hr = pDynamicRenderer->QueryInterface(&pSyncDynamicRenderer);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateDynamicRenderer: failed to access IStylusSyncPlugin of DynamicRenderer");
        pDynamicRenderer->Release();
        return NULL;
    }

    hr = pRealTimeStylus->AddStylusSyncPlugin(
        0,                      // insert plugin at position 0 in the sync plugin list
        pSyncDynamicRenderer);  // plugin to be inserted - DynamicRenderer
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateDynamicRenderer: failed to add DynamicRenderer to the RealTimeStylus plugins");
        pDynamicRenderer->Release();
        pSyncDynamicRenderer->Release();
        return NULL;
    }

    // Attach DynamicRenderer to the same window RTS object is attached to
    hr = pDynamicRenderer->put_HWND((HANDLE_PTR)hWnd);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CreateDynamicRenderer: failed to set window handle");
        pDynamicRenderer->Release();
        pSyncDynamicRenderer->Release();
        return NULL;
    }

    pSyncDynamicRenderer->Release();

    return pDynamicRenderer;
}
```

Следующий код изменяет цвет штриха пера для обработчика событий **стилусдовн** в **ксинцевенсандлерртс**, настраиваемый подключаемый модуль RTS.

```C++
HRESULT CSyncEventHandlerRTS::StylusDown(
    IRealTimeStylus* /* piRtsSrc */,
    const StylusInfo* /* pStylusInfo */,
    ULONG /* cPropCountPerPkt */,
    LONG* /* pPacket */,
    LONG** /* ppInOutPkt */)
{
    // Get DrawingAttributes of DynamicRenderer
    IInkDrawingAttributes* pDrawingAttributesDynamicRenderer;
    HRESULT hr = g_pDynamicRenderer->get_DrawingAttributes(&pDrawingAttributesDynamicRenderer);
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CSyncEventHandlerRTS::StylusDown: failed to get RTS's drawing attributes");
        return hr;
    }

    // Set new stroke color to the DrawingAttributes of the DynamicRenderer
    // If there are no fingers down, this is a primary contact
    hr = pDrawingAttributesDynamicRenderer->put_Color(GetTouchColor(m_nContacts == 0));
    if (FAILED(hr))
    {
        ASSERT(SUCCEEDED(hr) && L"CSyncEventHandlerRTS::StylusDown: failed to set color");
        pDrawingAttributesDynamicRenderer->Release();
        return hr;
    }

    pDrawingAttributesDynamicRenderer->Release();

    ++m_nContacts;  // Increment finger-down counter

    return S_OK;
}
```

Когда значение *m_nContacts* увеличивается, цветовой набор в динамическом модуле подготовки отчетов изменится. Штрихи, не являющиеся основными контактами, будут отображаться с разными цветами.

## <a name="related-topics"></a>См. также

[Многосенсорное приложение для ввода пометок (RTS/C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS), [многосенсорный Блокнот (RTS/C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp), [примеры Windows Touch](windows-touch-samples.md)
