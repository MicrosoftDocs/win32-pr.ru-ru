---
description: Обучение при возникновении события
ms.assetid: 4e44089b-676b-4220-9721-54ddf56bf760
title: Обучение при возникновении события
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19ed537430fd66818687b142f059399292c923e1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537703"
---
# <a name="learning-when-an-event-occurs"></a><span data-ttu-id="7ee5f-103">Обучение при возникновении события</span><span class="sxs-lookup"><span data-stu-id="7ee5f-103">Learning When an Event Occurs</span></span>

<span data-ttu-id="7ee5f-104">Для обработки событий DirectShow приложению требуется способ выяснить, когда события ожидают в очереди.</span><span class="sxs-lookup"><span data-stu-id="7ee5f-104">To process DirectShow events, an application needs a way to find out when events are waiting in the queue.</span></span> <span data-ttu-id="7ee5f-105">Диспетчер графов фильтров предоставляет два способа:</span><span class="sxs-lookup"><span data-stu-id="7ee5f-105">The Filter Graph Manager provides two ways to do this:</span></span>

-   <span data-ttu-id="7ee5f-106">**Уведомление окна:** Диспетчер графов фильтров отправляет определяемое пользователем сообщение Windows в окно приложения при наличии нового события.</span><span class="sxs-lookup"><span data-stu-id="7ee5f-106">**Window notification:** The Filter Graph Manager sends a user-defined Windows message to an application window whenever there is a new event.</span></span>
-   <span data-ttu-id="7ee5f-107">**Сигнализация события:** Диспетчер графов фильтров сигнализирует о событии Windows, если в очереди есть события DirectShow, и сбросить событие, если очередь пуста.</span><span class="sxs-lookup"><span data-stu-id="7ee5f-107">**Event signaling:** The Filter Graph Manager signals a Windows event if there are DirectShow events in the queue, and reset the event if the queue is empty.</span></span>

<span data-ttu-id="7ee5f-108">Приложение может использовать любой из этих методов.</span><span class="sxs-lookup"><span data-stu-id="7ee5f-108">An application can use either technique.</span></span> <span data-ttu-id="7ee5f-109">Уведомление окна обычно проще.</span><span class="sxs-lookup"><span data-stu-id="7ee5f-109">Window notification is usually simpler.</span></span>

<span data-ttu-id="7ee5f-110">**Уведомление окна**</span><span class="sxs-lookup"><span data-stu-id="7ee5f-110">**Window Notification**</span></span>

<span data-ttu-id="7ee5f-111">Чтобы настроить уведомление окна, вызовите метод [**имедиаевентекс:: сетнотифивиндов**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) и укажите частное сообщение.</span><span class="sxs-lookup"><span data-stu-id="7ee5f-111">To set up window notification, call the [**IMediaEventEx::SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) method and specify a private message.</span></span> <span data-ttu-id="7ee5f-112">Приложения могут использовать номера сообщений в диапазоне от приложения WM \_ через 0xBFFF как частные сообщения.</span><span class="sxs-lookup"><span data-stu-id="7ee5f-112">Applications can use message numbers in the range from WM\_APP through 0xBFFF as private messages.</span></span> <span data-ttu-id="7ee5f-113">Каждый раз, когда диспетчер графа фильтра помещает новое уведомление о событии в очередь, оно отправляет это сообщение в указанное окно.</span><span class="sxs-lookup"><span data-stu-id="7ee5f-113">Whenever the Filter Graph Manager places a new event notification in the queue, it posts this message to the designated window.</span></span> <span data-ttu-id="7ee5f-114">Приложение реагирует на сообщение в цикле обработки сообщений окна.</span><span class="sxs-lookup"><span data-stu-id="7ee5f-114">The application responds to the message from within the window's message loop.</span></span>

<span data-ttu-id="7ee5f-115">В следующем примере кода показано, как задать окно уведомления.</span><span class="sxs-lookup"><span data-stu-id="7ee5f-115">The following code example shows how to set the notification window.</span></span>


```C++
#define WM_GRAPHNOTIFY WM_APP + 1   // Private message.
pEvent->SetNotifyWindow((OAHWND)g_hwnd, WM_GRAPHNOTIFY, 0);
```



<span data-ttu-id="7ee5f-116">Сообщение является обычным сообщением Windows и публикуется отдельно от очереди уведомлений о событиях DirectShow.</span><span class="sxs-lookup"><span data-stu-id="7ee5f-116">The message is an ordinary Windows message, and is posted separately from the DirectShow event notification queue.</span></span> <span data-ttu-id="7ee5f-117">Преимуществом этого подхода является то, что большинство приложений уже реализуют цикл обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="7ee5f-117">The advantage of this approach is that most applications already implement a message loop.</span></span> <span data-ttu-id="7ee5f-118">Таким образом, можно включить обработку событий DirectShow без значительной дополнительной работы.</span><span class="sxs-lookup"><span data-stu-id="7ee5f-118">Therefore, you can incorporate DirectShow event handling without much additional work.</span></span>

<span data-ttu-id="7ee5f-119">В следующем примере кода показано, как реагировать на сообщение уведомления.</span><span class="sxs-lookup"><span data-stu-id="7ee5f-119">The following code example shows an outline of how to respond to the notification message.</span></span> <span data-ttu-id="7ee5f-120">Полный пример см. в разделе [реагирование на события](responding-to-events.md).</span><span class="sxs-lookup"><span data-stu-id="7ee5f-120">For a complete example, see [Responding to Events](responding-to-events.md).</span></span>


```C++
LRESULT CALLBACK WindowProc( HWND hwnd, UINT msg, UINT wParam, LONG lParam)
{
    switch (msg)
    {
        case WM_GRAPHNOTIFY:
            HandleEvent();  // Application-defined function.
            break;
        // Handle other Windows messages here too.
    }
    return (DefWindowProc(hwnd, msg, wParam, lParam));
}
```



<span data-ttu-id="7ee5f-121">Так как уведомления о событиях и цикл сообщений являются асинхронными, очередь может содержать более одного события на время ответа приложения на сообщение.</span><span class="sxs-lookup"><span data-stu-id="7ee5f-121">Because event notification and the message loop are both asynchronous, the queue might contain more than one event by the time your application responds to the message.</span></span> <span data-ttu-id="7ee5f-122">Кроме того, события иногда могут быть удалены из очереди, если они становятся недействительными.</span><span class="sxs-lookup"><span data-stu-id="7ee5f-122">Also, events can sometimes be cleared from the queue if they become invalid.</span></span> <span data-ttu-id="7ee5f-123">Поэтому в коде обработки событий вызовите [**иаммедиаевент::-четный**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) , пока не вернется код сбоя, указывающий, что очередь пуста.</span><span class="sxs-lookup"><span data-stu-id="7ee5f-123">Therefore, in your event handling code, call [**IAMMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) until it returns a failure code, indicating that the queue is empty.</span></span>

<span data-ttu-id="7ee5f-124">Перед освобождением указателя [**имедиаевентекс**](/windows/desktop/api/Control/nn-control-imediaeventex) отмените уведомление о событии, вызвав [**сетнотифивиндов**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) с **пустым** указателем.</span><span class="sxs-lookup"><span data-stu-id="7ee5f-124">Before you release the [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) pointer, cancel event notification by calling [**SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow) with a **NULL** pointer.</span></span> <span data-ttu-id="7ee5f-125">В коде обработки событий проверьте, является ли указатель **имедиаевентекс** допустимым, прежде чем [**вызывать метод**](/windows/desktop/api/Control/nf-control-imediaevent-getevent).</span><span class="sxs-lookup"><span data-stu-id="7ee5f-125">In your event processing code, check whether your **IMediaEventEx** pointer is valid before calling [**GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent).</span></span> <span data-ttu-id="7ee5f-126">Эти действия препятствуют возможной ошибке, при которой приложение получает уведомление о событии после того, как оно выпустило указатель **имедиаевентекс** .</span><span class="sxs-lookup"><span data-stu-id="7ee5f-126">These steps prevent a possible error, in which the application receives the event notification after it has released the **IMediaEventEx** pointer.</span></span>

<span data-ttu-id="7ee5f-127">**Сигнализация о событиях**</span><span class="sxs-lookup"><span data-stu-id="7ee5f-127">**Event Signaling**</span></span>

<span data-ttu-id="7ee5f-128">Диспетчер графов фильтров сохраняет событие ручного сброса, которое отражает состояние очереди событий.</span><span class="sxs-lookup"><span data-stu-id="7ee5f-128">The Filter Graph Manager keeps a manual-reset event that reflects the state of the event queue.</span></span> <span data-ttu-id="7ee5f-129">Если очередь содержит уведомления о событиях, ожидающих выполнения, диспетчер графа фильтров сигнализирует о событии ручного сброса.</span><span class="sxs-lookup"><span data-stu-id="7ee5f-129">If the queue contains pending event notifications, the Filter Graph Manager signals the manual-reset event.</span></span> <span data-ttu-id="7ee5f-130">Если очередь пуста, вызов метода [**имедиаевент::-четный**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) сбрасывает событие.</span><span class="sxs-lookup"><span data-stu-id="7ee5f-130">If the queue is empty, a call to the [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) method resets the event.</span></span> <span data-ttu-id="7ee5f-131">Приложение может использовать это событие для определения состояния очереди.</span><span class="sxs-lookup"><span data-stu-id="7ee5f-131">An application can use this event to determine the state of the queue.</span></span>

> [!Note]  
> <span data-ttu-id="7ee5f-132">Эта терминология может быть запутанной.</span><span class="sxs-lookup"><span data-stu-id="7ee5f-132">The terminology can be confusing here.</span></span> <span data-ttu-id="7ee5f-133">Событие ручного сброса — это тип события, созданного функцией [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) для Windows; Он не имеет никаких действий с событиями, определенными в DirectShow.</span><span class="sxs-lookup"><span data-stu-id="7ee5f-133">The manual-reset event is the type of event created by the Windows [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) function; it has nothing to do with the events defined by DirectShow.</span></span>

 

<span data-ttu-id="7ee5f-134">Вызовите метод [**имедиаевент:: жетевенсандле**](/windows/desktop/api/Control/nf-control-imediaevent-geteventhandle) , чтобы получить маркер события ручного сброса.</span><span class="sxs-lookup"><span data-stu-id="7ee5f-134">Call the [**IMediaEvent::GetEventHandle**](/windows/desktop/api/Control/nf-control-imediaevent-geteventhandle) method to get a handle to the manual-reset event.</span></span> <span data-ttu-id="7ee5f-135">Дождитесь получения сигнала о событии, вызвав функцию, например [**WaitForMultipleObjects**](/windows/win32/api/winuser/nf-winuser-msgwaitformultipleobjects).</span><span class="sxs-lookup"><span data-stu-id="7ee5f-135">Wait for the event to be signaled by calling a function such as [**WaitForMultipleObjects**](/windows/win32/api/winuser/nf-winuser-msgwaitformultipleobjects).</span></span> <span data-ttu-id="7ee5f-136">После получения сигнала о событии вызовите [**имедиаевент::-четный**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) , чтобы получить событие DirectShow.</span><span class="sxs-lookup"><span data-stu-id="7ee5f-136">Once the event is signaled, call [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) to get the DirectShow event.</span></span>

<span data-ttu-id="7ee5f-137">Этот подход показан в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="7ee5f-137">The following code example illustrates this approach.</span></span> <span data-ttu-id="7ee5f-138">Он получает дескриптор события, а затем ожидает в 100-миллисекундах интервала для события.</span><span class="sxs-lookup"><span data-stu-id="7ee5f-138">It gets the event handle, then waits in 100-millisecond intervals for the event to be signaled.</span></span> <span data-ttu-id="7ee5f-139">Если событие является сигнальным, оно вызывает метод in и выводит код **события и параметры** события в окно консоли.</span><span class="sxs-lookup"><span data-stu-id="7ee5f-139">If the event is signaled, it calls **GetEvent** and prints the event code and event parameters to the console window.</span></span> <span data-ttu-id="7ee5f-140">Цикл завершается, когда происходит событие [**EC \_ Complete**](ec-complete.md) , что означает, что воспроизведение завершено.</span><span class="sxs-lookup"><span data-stu-id="7ee5f-140">The loop terminates when the [**EC\_COMPLETE**](ec-complete.md) event occurs, indicating that playback has completed.</span></span>


```C++
HANDLE  hEvent; 
long    evCode, param1, param2;
BOOLEAN bDone = FALSE;
HRESULT hr = S_OK;
hr = pEvent->GetEventHandle((OAEVENT*)&hEvent);
if (FAILED(hr))
{
    /* Insert failure-handling code here. */
}

while(!bDone) 
{
    if (WAIT_OBJECT_0 == WaitForSingleObject(hEvent, 100))
    { 
        while (S_OK == pEvent->GetEvent(&evCode, &param1, &param2, 0)) 
        {
            printf("Event code: %#04x\n Params: %d, %d\n", evCode, param1, param2);
            pEvent->FreeEventParams(evCode, param1, param2);
            bDone = (EC_COMPLETE == evCode);
        }
    }
} 
```



<span data-ttu-id="7ee5f-141">Так как граф фильтра автоматически задает или сбрасывает событие, если это уместно, приложение не должно этого делать.</span><span class="sxs-lookup"><span data-stu-id="7ee5f-141">Because the filter graph automatically sets or resets the event when appropriate, your application should not do so.</span></span> <span data-ttu-id="7ee5f-142">Кроме того, при освобождении графа фильтра граф фильтра закрывает обработчик события, поэтому не следует использовать этот обработчик после этой точки.</span><span class="sxs-lookup"><span data-stu-id="7ee5f-142">Also, when you release the filter graph, the filter graph closes the event handle, so do not use the event handle after that point.</span></span>

 

 
