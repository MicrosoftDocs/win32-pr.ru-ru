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
# <a name="step-6-handle-graph-events"></a><span data-ttu-id="30516-103">Шаг 6. Работа с событиями графа</span><span class="sxs-lookup"><span data-stu-id="30516-103">Step 6: Handle Graph Events</span></span>

<span data-ttu-id="30516-104">В этом разделе описывается шаг 6 руководства [Воспроизведение аудио-и видеороликов в DirectShow](audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="30516-104">This topic is step 6 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="30516-105">Полный код приведен в разделе [Пример воспроизведения DirectShow](directshow-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="30516-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="30516-106">Когда приложение создает новый экземпляр диспетчера графа фильтров, приложение вызывает [**имедиаевентекс:: сетнотифивиндов**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow).</span><span class="sxs-lookup"><span data-stu-id="30516-106">When the application creates a new instance of the Filter Graph Manager, the application calls [**IMediaEventEx::SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow).</span></span> <span data-ttu-id="30516-107">Этот метод регистрирует окно приложения для получения событий из графа фильтра.</span><span class="sxs-lookup"><span data-stu-id="30516-107">This method registers the application window to receive events from the filter graph.</span></span>


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



<span data-ttu-id="30516-108">Значение `WM_GRAPH_EVENT` является сообщением частного окна.</span><span class="sxs-lookup"><span data-stu-id="30516-108">The value `WM_GRAPH_EVENT` is a private window message.</span></span> <span data-ttu-id="30516-109">Каждый раз, когда приложение получает это сообщение, оно вызывает `DShowPlayer::HandleGraphEvent` метод.</span><span class="sxs-lookup"><span data-stu-id="30516-109">Whenever the application receives this message, it calls the `DShowPlayer::HandleGraphEvent` method.</span></span>


```C++
    case WM_GRAPH_EVENT:
       g_pPlayer->HandleGraphEvent(OnGraphEvent);
       return 0;
```



<span data-ttu-id="30516-110">Метод `DShowPlayer::HandleGraphEvent` выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="30516-110">The `DShowPlayer::HandleGraphEvent` method does the following:</span></span>

1.  <span data-ttu-id="30516-111">Вызывает [**имедиаевент::-четный**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) в цикле для получения всех событий в очереди.</span><span class="sxs-lookup"><span data-stu-id="30516-111">Calls [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) in a loop to get all of the queued events.</span></span>
2.  <span data-ttu-id="30516-112">Вызывает функцию обратного вызова (*пфнонграфевент*).</span><span class="sxs-lookup"><span data-stu-id="30516-112">Invokes a callback function (*pfnOnGraphEvent*).</span></span>
3.  <span data-ttu-id="30516-113">Вызывает [**имедиаевент:: фриевентпарамс**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) , чтобы освободить данные, связанные с каждым событием.</span><span class="sxs-lookup"><span data-stu-id="30516-113">Calls [**IMediaEvent::FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) to free the data associated with each event.</span></span>


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



<span data-ttu-id="30516-114">В следующем коде показана функция обратного вызова, которая передается в `DShowPlayer::HandleGraphEvent` .</span><span class="sxs-lookup"><span data-stu-id="30516-114">The following code shows the callback function that is passed to `DShowPlayer::HandleGraphEvent`.</span></span> <span data-ttu-id="30516-115">Функция обрабатывает минимальное количество событий графа ([**EC \_ Complete**](ec-complete.md), [**EC \_ еррораборт**](ec-errorabort.md)и [**EC \_ усераборт**](ec-userabort.md)); функцию можно расширить для обработки дополнительных событий.</span><span class="sxs-lookup"><span data-stu-id="30516-115">The function handles the minimum number of graph events ([**EC\_COMPLETE**](ec-complete.md), [**EC\_ERRORABORT**](ec-errorabort.md), and [**EC\_USERABORT**](ec-userabort.md)); you could expand the function to handle additional events.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="30516-116">См. также</span><span class="sxs-lookup"><span data-stu-id="30516-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30516-117">Воспроизведение звука и видео в DirectShow</span><span class="sxs-lookup"><span data-stu-id="30516-117">Audio/Video Playback in DirectShow</span></span>](audio-video-playback-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="30516-118">Пример воспроизведения DirectShow</span><span class="sxs-lookup"><span data-stu-id="30516-118">DirectShow Playback Example</span></span>](directshow-playback-example.md)
</dt> <dt>

[<span data-ttu-id="30516-119">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="30516-119">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="30516-120">Реагирование на события</span><span class="sxs-lookup"><span data-stu-id="30516-120">Responding to Events</span></span>](responding-to-events.md)
</dt> </dl>

 

 



