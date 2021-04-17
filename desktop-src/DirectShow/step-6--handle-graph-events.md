---
description: В этом разделе описывается шаг 6 руководства воспроизведение аудио-и видеороликов в DirectShow.
ms.assetid: febfe7fa-e5f1-4b37-942a-ed9f8c7c60c1
title: Шаг 6. Работа с событиями графа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3660e270a542a060ed5e5eee79d5c78c107fea4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674173"
---
# <a name="step-6-handle-graph-events"></a>Шаг 6. Работа с событиями графа

В этом разделе описывается шаг 6 руководства [Воспроизведение аудио-и видеороликов в DirectShow](audio-video-playback-in-directshow.md). Полный код приведен в разделе [Пример воспроизведения DirectShow](directshow-playback-example.md).

Когда приложение создает новый экземпляр диспетчера графа фильтров, приложение вызывает [**имедиаевентекс:: сетнотифивиндов**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow). Этот метод регистрирует окно приложения для получения событий из графа фильтра.


```C++
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
```



Значение `WM_GRAPH_EVENT` является сообщением частного окна. Каждый раз, когда приложение получает это сообщение, оно вызывает `DShowPlayer::HandleGraphEvent` метод.


```C++
    case WM_GRAPH_EVENT:
       g_pPlayer->HandleGraphEvent(OnGraphEvent);
       return 0;
```



Метод `DShowPlayer::HandleGraphEvent` выполняет следующие действия:

1.  Вызывает [**имедиаевент::-четный**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) в цикле для получения всех событий в очереди.
2.  Вызывает функцию обратного вызова (*пфнонграфевент*).
3.  Вызывает [**имедиаевент:: фриевентпарамс**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) , чтобы освободить данные, связанные с каждым событием.


```C++
// Respond to a graph event.
//
// The owning window should call this method when it receives the window
// message that the application specified when it called SetEventWindow.
//
// Caution: Do not tear down the graph from inside the callback.

HRESULT DShowPlayer::HandleGraphEvent(GraphEventFN pfnOnGraphEvent)
{
    if (!m_pEvent)
    {
        return E_UNEXPECTED;
    }

    long evCode = 0;
    LONG_PTR param1 = 0, param2 = 0;

    HRESULT hr = S_OK;

    // Get the events from the queue.
    while (SUCCEEDED(m_pEvent->GetEvent(&evCode, &param1, &param2, 0)))
    {
        // Invoke the callback.
        pfnOnGraphEvent(m_hwnd, evCode, param1, param2);

        // Free the event data.
        hr = m_pEvent->FreeEventParams(evCode, param1, param2);
        if (FAILED(hr))
        {
            break;
        }
    }
    return hr;
}
```



В следующем коде показана функция обратного вызова, которая передается в `DShowPlayer::HandleGraphEvent` . Функция обрабатывает минимальное количество событий графа ([**EC \_ Complete**](ec-complete.md), [**EC \_ еррораборт**](ec-errorabort.md)и [**EC \_ усераборт**](ec-userabort.md)); функцию можно расширить для обработки дополнительных событий.


```C++
void CALLBACK OnGraphEvent(HWND hwnd, long evCode, LONG_PTR param1, LONG_PTR param2)
{
    switch (evCode)
    {
    case EC_COMPLETE:
    case EC_USERABORT:
        g_pPlayer->Stop();
        break;

    case EC_ERRORABORT:
        NotifyError(hwnd, L"Playback error.");
        g_pPlayer->Stop();
        break;
    }
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Воспроизведение звука и видео в DirectShow](audio-video-playback-in-directshow.md)
</dt> <dt>

[Пример воспроизведения DirectShow](directshow-playback-example.md)
</dt> <dt>

[Уведомление о событии в DirectShow](event-notification-in-directshow.md)
</dt> <dt>

[Реагирование на события](responding-to-events.md)
</dt> </dl>

 

 



