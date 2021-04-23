---
description: В этой статье описывается, как реагировать на события, происходящие в графе фильтров.
ms.assetid: 1c09149b-7f34-4296-bd32-dbbae5e1d62b
title: Реагирование на события
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a51481371501c05733e5f637885a71001c1f996
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537202"
---
# <a name="responding-to-events"></a><span data-ttu-id="3c3d5-103">Реагирование на события</span><span class="sxs-lookup"><span data-stu-id="3c3d5-103">Responding to Events</span></span>

<span data-ttu-id="3c3d5-104">В этой статье описывается, как реагировать на события, происходящие в графе фильтров.</span><span class="sxs-lookup"><span data-stu-id="3c3d5-104">This article describes how to respond to events that occur in a filter graph.</span></span>

## <a name="how-event-notification-works"></a><span data-ttu-id="3c3d5-105">Как работает уведомление о событии</span><span class="sxs-lookup"><span data-stu-id="3c3d5-105">How Event Notification Works</span></span>

<span data-ttu-id="3c3d5-106">Пока выполняется приложение DirectShow, в графе фильтра могут возникать события.</span><span class="sxs-lookup"><span data-stu-id="3c3d5-106">While a DirectShow application is running, events can occur within the filter graph.</span></span> <span data-ttu-id="3c3d5-107">Например, фильтр может столкнуться с ошибкой потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="3c3d5-107">For example, a filter might encounter a streaming error.</span></span> <span data-ttu-id="3c3d5-108">Фильтры предупреждают диспетчер диаграмм фильтров, отправляя события, состоящие из кода события и двух параметров событий.</span><span class="sxs-lookup"><span data-stu-id="3c3d5-108">Filters alert the Filter Graph Manager by sending events, which consist of an event code and two event parameters.</span></span> <span data-ttu-id="3c3d5-109">Код события указывает тип события, а параметры события предоставляют дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="3c3d5-109">The event code indicates the type of event, and the event parameters supply additional information.</span></span> <span data-ttu-id="3c3d5-110">Значение параметров зависит от кода события.</span><span class="sxs-lookup"><span data-stu-id="3c3d5-110">The meaning of the parameters depends on the event code.</span></span> <span data-ttu-id="3c3d5-111">Полный список кодов событий см. в разделе [коды уведомлений о событиях](event-notification-codes.md).</span><span class="sxs-lookup"><span data-stu-id="3c3d5-111">For a complete list of event codes, see [Event Notification Codes](event-notification-codes.md).</span></span>

<span data-ttu-id="3c3d5-112">Некоторые события автоматически обрабатываются диспетчером графа фильтров без уведомления приложения.</span><span class="sxs-lookup"><span data-stu-id="3c3d5-112">Some events are handled silently by the Filter Graph Manager, without the application being notified.</span></span> <span data-ttu-id="3c3d5-113">Другие события помещаются в очередь для приложения.</span><span class="sxs-lookup"><span data-stu-id="3c3d5-113">Other events are placed on a queue for the application.</span></span> <span data-ttu-id="3c3d5-114">В зависимости от приложения существуют различные события, которые могут потребоваться для обработки.</span><span class="sxs-lookup"><span data-stu-id="3c3d5-114">Depending on the application, there are various events that you might need to handle.</span></span> <span data-ttu-id="3c3d5-115">Эта статья посвящена трем событиям, которые очень распространены:</span><span class="sxs-lookup"><span data-stu-id="3c3d5-115">This article focuses on three events that are very common:</span></span>

-   <span data-ttu-id="3c3d5-116">Событие [**EC \_ Complete**](ec-complete.md) указывает, что воспроизведение выполнено нормально.</span><span class="sxs-lookup"><span data-stu-id="3c3d5-116">The [**EC\_COMPLETE**](ec-complete.md) event indicates that playback has completed normally.</span></span>
-   <span data-ttu-id="3c3d5-117">Событие [**EC \_ усераборт**](ec-userabort.md) указывает, что пользователь прервал воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="3c3d5-117">The [**EC\_USERABORT**](ec-userabort.md) event indicates that the user has interrupted playback.</span></span> <span data-ttu-id="3c3d5-118">Модули обработки видео отправляют это событие, если пользователь закрывает окно видео.</span><span class="sxs-lookup"><span data-stu-id="3c3d5-118">Video renderers send this event if the user closes the video window.</span></span>
-   <span data-ttu-id="3c3d5-119">Событие [**EC \_ еррораборт**](ec-errorabort.md) указывает, что ошибка привела к остановке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="3c3d5-119">The [**EC\_ERRORABORT**](ec-errorabort.md) event indicates that an error has caused playback to halt.</span></span>

## <a name="using-event-notification"></a><span data-ttu-id="3c3d5-120">Использование уведомления о событии</span><span class="sxs-lookup"><span data-stu-id="3c3d5-120">Using Event Notification</span></span>

<span data-ttu-id="3c3d5-121">Приложение может указать диспетчеру графа фильтров отправить сообщение Windows в указанное окно при возникновении нового события.</span><span class="sxs-lookup"><span data-stu-id="3c3d5-121">An application can instruct the Filter Graph Manager to send a Windows message to a designated window whenever a new event occurs.</span></span> <span data-ttu-id="3c3d5-122">Это позволяет приложению реагировать внутри цикла обработки сообщений окна.</span><span class="sxs-lookup"><span data-stu-id="3c3d5-122">This enables the application to respond inside the window's message loop.</span></span> <span data-ttu-id="3c3d5-123">Сначала определите сообщение, которое будет отправлено в окно приложения.</span><span class="sxs-lookup"><span data-stu-id="3c3d5-123">First, define the message that will be sent to the application window.</span></span> <span data-ttu-id="3c3d5-124">Приложения могут использовать номера сообщений в диапазоне от приложения WM \_ через 0xBFFF как частные сообщения:</span><span class="sxs-lookup"><span data-stu-id="3c3d5-124">Applications can use message numbers in the range from WM\_APP through 0xBFFF as private messages:</span></span>


```C++
#define WM_GRAPHNOTIFY  WM_APP + 1
```



<span data-ttu-id="3c3d5-125">Затем запросите диспетчер графа фильтров для интерфейса [**имедиаевентекс**](/windows/desktop/api/Control/nn-control-imediaeventex) и вызовите метод [**Имедиаевентекс:: сетнотифивиндов**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) :</span><span class="sxs-lookup"><span data-stu-id="3c3d5-125">Next, query the Filter Graph Manager for the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) interface and call the [**IMediaEventEx::SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) method:</span></span>


```C++
IMediaEventEx *g_pEvent = NULL;
g_pGraph->QueryInterface(IID_IMediaEventEx, (void **)&g_pEvent);
g_pEvent->SetNotifyWindow((OAHWND)g_hwnd, WM_GRAPHNOTIFY, 0);
```



<span data-ttu-id="3c3d5-126">Этот метод обозначает указанное окно (g \_ HWND) в качестве получателя сообщения.</span><span class="sxs-lookup"><span data-stu-id="3c3d5-126">This method designates the specified window (g\_hwnd) as the recipient of the message.</span></span> <span data-ttu-id="3c3d5-127">Вызовите метод после создания графа фильтра, но перед запуском графа.</span><span class="sxs-lookup"><span data-stu-id="3c3d5-127">Call the method after you create the filter graph, but before running the graph.</span></span>

<span data-ttu-id="3c3d5-128">WM \_ графнотифи — это обычное сообщение Windows.</span><span class="sxs-lookup"><span data-stu-id="3c3d5-128">WM\_GRAPHNOTIFY is an ordinary Windows message.</span></span> <span data-ttu-id="3c3d5-129">Каждый раз, когда диспетчер графа фильтров помещает новое событие в очередь событий, оно отправляет \_ сообщение ГРАФНОТИФИ WM в указанное окно приложения.</span><span class="sxs-lookup"><span data-stu-id="3c3d5-129">Whenever the Filter Graph Manager puts a new event on the event queue, it posts a WM\_GRAPHNOTIFY message to the designated application window.</span></span> <span data-ttu-id="3c3d5-130">Параметр *lParam* сообщения равен третьему параметру в [**сетнотифивиндов**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow).</span><span class="sxs-lookup"><span data-stu-id="3c3d5-130">The message's *lParam* parameter is equal to the third parameter in [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow).</span></span> <span data-ttu-id="3c3d5-131">Этот параметр позволяет отправить данные экземпляра вместе с сообщением.</span><span class="sxs-lookup"><span data-stu-id="3c3d5-131">This parameter enables you to send instance data with the message.</span></span> <span data-ttu-id="3c3d5-132">Параметр *wParam* сообщения окна всегда равен нулю.</span><span class="sxs-lookup"><span data-stu-id="3c3d5-132">The window message's *wParam* parameter is always zero.</span></span>

<span data-ttu-id="3c3d5-133">В функции **WindowProc** приложения добавьте инструкцию CASE для \_ сообщения WM графнотифи:</span><span class="sxs-lookup"><span data-stu-id="3c3d5-133">In your application's **WindowProc** function, add a case statement for the WM\_GRAPHNOTIFY message:</span></span>


```C++
case WM_GRAPHNOTIFY:
    HandleGraphEvent();
    break;
```



<span data-ttu-id="3c3d5-134">В функции обработчика событий вызовите метод [**имедиаевент:: четный**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) для получения событий из очереди:</span><span class="sxs-lookup"><span data-stu-id="3c3d5-134">In the event handler function, call the [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) method to retrieve events from the queue:</span></span>


```C++
void HandleGraphEvent()
{
    // Disregard if we don't have an IMediaEventEx pointer.
    if (g_pEvent == NULL)
    {
        return;
    }
    // Get all the events
    long evCode;
    LONG_PTR param1, param2;
    HRESULT hr;
    while (SUCCEEDED(g_pEvent->GetEvent(&evCode, &param1, &param2, 0)))
    {
        g_pEvent->FreeEventParams(evCode, param1, param2);
        switch (evCode)
        {
        case EC_COMPLETE:  // Fall through.
        case EC_USERABORT: // Fall through.
        case EC_ERRORABORT:
            CleanUp();
            PostQuitMessage(0);
            return;
        }
    } 
}
```



<span data-ttu-id="3c3d5-135">Метод [**четный**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) извлекает код события и два параметра события.</span><span class="sxs-lookup"><span data-stu-id="3c3d5-135">The [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) method retrieves the event code and the two event parameters.</span></span> <span data-ttu-id="3c3d5-136">Четвертый параметр **четный** указывает продолжительность времени ожидания события в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="3c3d5-136">The fourth **GetEvent** parameter specifies the length of time to wait for an event, in milliseconds.</span></span> <span data-ttu-id="3c3d5-137">Так как приложение вызывает этот метод в ответ на \_ сообщение ГРАФНОТИФИ WM, событие уже поставлено в очередь.</span><span class="sxs-lookup"><span data-stu-id="3c3d5-137">Because the application calls this method in response to a WM\_GRAPHNOTIFY message, the event is already queued.</span></span> <span data-ttu-id="3c3d5-138">Поэтому мы устанавливаем значение времени ожидания равным нулю.</span><span class="sxs-lookup"><span data-stu-id="3c3d5-138">Therefore, we set the time-out value to zero.</span></span>

<span data-ttu-id="3c3d5-139">Уведомление о событии и цикл сообщений являются асинхронными, поэтому очередь может содержать более одного события на время ответа приложения на сообщение.</span><span class="sxs-lookup"><span data-stu-id="3c3d5-139">Event notification and the message loop are both asynchronous, so the queue might hold more than one event by the time your application responds to the message.</span></span> <span data-ttu-id="3c3d5-140">Кроме того, диспетчер графов фильтров может удалить определенные события из очереди, если они станут недействительными.</span><span class="sxs-lookup"><span data-stu-id="3c3d5-140">Also, the Filter Graph Manager can remove certain events from the queue, if they become invalid.</span></span> <span data-ttu-id="3c3d5-141">Таким образом, следует вызывать метод with, [**пока не будет**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) возвращен код сбоя, указывающий, что очередь пуста.</span><span class="sxs-lookup"><span data-stu-id="3c3d5-141">Therefore, you should call [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) until it returns a failure code, indicating the queue is empty.</span></span>

<span data-ttu-id="3c3d5-142">В этом примере приложение реагирует на [**EC \_ Complete**](ec-complete.md), [**EC \_ усераборт**](ec-userabort.md)и [**EC \_ еррораборт**](ec-errorabort.md) , вызывая функцию очистки, определяемую приложением, что приводит к корректному завершению работы приложения.</span><span class="sxs-lookup"><span data-stu-id="3c3d5-142">In this example, the application responds to [**EC\_COMPLETE**](ec-complete.md), [**EC\_USERABORT**](ec-userabort.md), and [**EC\_ERRORABORT**](ec-errorabort.md) by invoking the application-defined CleanUp function, which causes the application to quit gracefully.</span></span> <span data-ttu-id="3c3d5-143">В примере игнорируются два параметра события.</span><span class="sxs-lookup"><span data-stu-id="3c3d5-143">The example ignores the two event parameters.</span></span> <span data-ttu-id="3c3d5-144">После получения события вызовите [**имедиаевент:: фриевентпарамс**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) для любых свободных ресурсов, связанных с параметрами события.</span><span class="sxs-lookup"><span data-stu-id="3c3d5-144">After you retrieve an event, call [**IMediaEvent::FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) to any free resources associated with the event parameters.</span></span>

<span data-ttu-id="3c3d5-145">Обратите внимание, что событие [**EC \_ Complete**](ec-complete.md) не приводит к сбою графа фильтра.</span><span class="sxs-lookup"><span data-stu-id="3c3d5-145">Note that an [**EC\_COMPLETE**](ec-complete.md) event does not cause the filter graph to stop.</span></span> <span data-ttu-id="3c3d5-146">Приложение может либо остановить, либо приостановить граф.</span><span class="sxs-lookup"><span data-stu-id="3c3d5-146">The application can either stop or pause the graph.</span></span> <span data-ttu-id="3c3d5-147">Если вы останавливаете граф, Фильтры освобождают все удерживаемые ими ресурсы.</span><span class="sxs-lookup"><span data-stu-id="3c3d5-147">If you stop the graph, filters release any resources they are holding.</span></span> <span data-ttu-id="3c3d5-148">При приостановке графа фильтры продолжают хранить ресурсы.</span><span class="sxs-lookup"><span data-stu-id="3c3d5-148">If you pause the graph, filters continue to hold resources.</span></span> <span data-ttu-id="3c3d5-149">Кроме того, когда модуль подготовки видео приостанавливает работу, он отображает статическое изображение самого последнего кадра.</span><span class="sxs-lookup"><span data-stu-id="3c3d5-149">Also, when a video renderer pauses, it displays a static image of the most recent frame.</span></span>

<span data-ttu-id="3c3d5-150">Перед освобождением указателя [**имедиаевентекс**](/windows/desktop/api/Control/nn-control-imediaeventex) отмените уведомление о событии, вызвав [**сетнотифивиндов**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) с **нулевым** маркером окна:</span><span class="sxs-lookup"><span data-stu-id="3c3d5-150">Before you release the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) pointer, cancel event notification by calling [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) with a **NULL** window handle:</span></span>


```C++
// Disable event notification before releasing the graph.
g_pEvent->SetNotifyWindow(NULL, 0, 0);
g_pEvent->Release();
g_pEvent = NULL;
```



<span data-ttu-id="3c3d5-151">В \_ обработчике сообщений WM графнотифи проверьте указатель [**имедиаевентекс**](/windows/desktop/api/Control/nn-control-imediaeventex) перед вызовом метода [](/windows/desktop/api/Control/nf-control-imediaevent-getevent):</span><span class="sxs-lookup"><span data-stu-id="3c3d5-151">In the WM\_GRAPHNOTIFY message handler, check the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) pointer before calling [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent):</span></span>


```C++
if (g_pEvent == NULL) return;
```



<span data-ttu-id="3c3d5-152">Это предотвращает возможную ошибку, которая может возникнуть, если приложение получает уведомление о событии после освобождения указателя.</span><span class="sxs-lookup"><span data-stu-id="3c3d5-152">This prevents a possible error that can occur if the application receives the event notification after releasing the pointer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c3d5-153">См. также</span><span class="sxs-lookup"><span data-stu-id="3c3d5-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c3d5-154">Основные задачи DirectShow</span><span class="sxs-lookup"><span data-stu-id="3c3d5-154">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> <dt>

[<span data-ttu-id="3c3d5-155">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="3c3d5-155">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 



