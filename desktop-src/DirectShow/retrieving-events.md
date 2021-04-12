---
description: Получение событий
ms.assetid: 18c5892d-7e33-497c-ab7d-d17fea5df17e
title: Получение событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78d23cf4f8060c15db564e718ba3a2fa4a660022
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104416380"
---
# <a name="retrieving-events"></a><span data-ttu-id="239bc-103">Получение событий</span><span class="sxs-lookup"><span data-stu-id="239bc-103">Retrieving Events</span></span>

<span data-ttu-id="239bc-104">Диспетчер графов фильтров предоставляет три интерфейса, поддерживающих уведомления о событиях.</span><span class="sxs-lookup"><span data-stu-id="239bc-104">The Filter Graph Manager exposes three interfaces that support event notification.</span></span>

-   <span data-ttu-id="239bc-105">[**Имедиаевентсинк**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) содержит метод для фильтров для публикации событий.</span><span class="sxs-lookup"><span data-stu-id="239bc-105">[**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) contains the method for filters to post events.</span></span>
-   <span data-ttu-id="239bc-106">[**Имедиаевент**](/windows/desktop/api/Control/nn-control-imediaevent) содержит методы для получения событий приложениями.</span><span class="sxs-lookup"><span data-stu-id="239bc-106">[**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) contains methods for applications to retrieve events.</span></span>
-   <span data-ttu-id="239bc-107">[**Имедиаевентекс**](/windows/desktop/api/Control/nn-control-imediaeventex) наследует от и расширяет интерфейс [**имедиаевент**](/windows/desktop/api/Control/nn-control-imediaevent) .</span><span class="sxs-lookup"><span data-stu-id="239bc-107">[**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) inherits from and extends the [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) interface.</span></span>

<span data-ttu-id="239bc-108">Фильтр отправляет уведомления о событиях, вызывая метод [**имедиаевентсинк:: notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) в диспетчере графов фильтров.</span><span class="sxs-lookup"><span data-stu-id="239bc-108">Filters post event notifications by calling the [**IMediaEventSink::Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) method on the Filter Graph Manager.</span></span> <span data-ttu-id="239bc-109">Уведомление о событии состоит из кода события, определяющего тип события, и двух параметров, которые предоставляют дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="239bc-109">An event notification consists of an event code, which defines the type of event, and two parameters that give additional information.</span></span> <span data-ttu-id="239bc-110">В зависимости от кода события параметры могут содержать указатели, коды возврата, время ссылки или другие сведения.</span><span class="sxs-lookup"><span data-stu-id="239bc-110">Depending on the event code, the parameters might contain pointers, return codes, reference times, or other information.</span></span> <span data-ttu-id="239bc-111">Полный список кодов событий и параметров см. в разделе [коды уведомлений о событиях](event-notification-codes.md).</span><span class="sxs-lookup"><span data-stu-id="239bc-111">For a complete list of event codes and parameters, see [Event Notification Codes](event-notification-codes.md).</span></span>

<span data-ttu-id="239bc-112">Чтобы получить событие из очереди, приложение вызывает метод [**имедиаевент:: четный**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) в диспетчере графов фильтров.</span><span class="sxs-lookup"><span data-stu-id="239bc-112">To retrieve an event from the queue, the application calls the [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) method on the Filter Graph Manager.</span></span> <span data-ttu-id="239bc-113">Этот метод блокируется до тех пор, пока не будет возвращено событие, которое будет возвращаться или пока не истечет указанное время.</span><span class="sxs-lookup"><span data-stu-id="239bc-113">This method blocks until there is an event to return or until a specified time elapses.</span></span> <span data-ttu-id="239bc-114">Если имеется событие в очереди, метод возвращает код события и два параметра события.</span><span class="sxs-lookup"><span data-stu-id="239bc-114">Assuming there is a queued event, the method returns with the event code and the two event parameters.</span></span> <span data-ttu-id="239bc-115">После вызова **метода** Event приложение всегда должно вызывать метод [**Имедиаевент:: фриевентпарамс**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) , чтобы освободить все ресурсы, связанные с параметрами события.</span><span class="sxs-lookup"><span data-stu-id="239bc-115">After calling **GetEvent**, an application should always call the [**IMediaEvent::FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) method to release any resources associated with the event parameters.</span></span> <span data-ttu-id="239bc-116">Например, параметр может быть значением **BSTR** , выделенным графом фильтра.</span><span class="sxs-lookup"><span data-stu-id="239bc-116">For example, a parameter might be a **BSTR** value that was allocated by the filter graph.</span></span>

<span data-ttu-id="239bc-117">В следующем примере кода показана структура извлечения событий из очереди.</span><span class="sxs-lookup"><span data-stu-id="239bc-117">The following code example provides an outline of how to retrieve events from the queue.</span></span>


```C++
long evCode;
LONG_PTR param1, param2;
HRESULT hr;
while (hr = pEvent->GetEvent(&evCode, &param1, &param2, 0), SUCCEEDED(hr))
{
    switch(evCode) 
    { 
        // Call application-defined functions for each 
        // type of event that you want to handle.
    } 
    hr = pEvent->FreeEventParams(evCode, param1, param2);
}
```



<span data-ttu-id="239bc-118">Чтобы переопределить обработку события по умолчанию диспетчером графа фильтра, вызовите метод [**имедиаевент:: канцелдефаулсандлинг**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) с кодом события в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="239bc-118">To override the Filter Graph Manager's default handling for an event, call the [**IMediaEvent::CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) method with the event code as a parameter.</span></span> <span data-ttu-id="239bc-119">Можно восстановить обработку по умолчанию, вызвав метод [**имедиаевент:: ресторедефаулсандлинг**](/windows/desktop/api/Control/nf-control-imediaevent-restoredefaulthandling) .</span><span class="sxs-lookup"><span data-stu-id="239bc-119">You can reinstate the default handling by calling the [**IMediaEvent::RestoreDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-restoredefaulthandling) method.</span></span> <span data-ttu-id="239bc-120">Если граф фильтра не выполняет обработку по умолчанию для указанного кода события, вызов этих методов не оказывает никакого влияния.</span><span class="sxs-lookup"><span data-stu-id="239bc-120">If the filter graph performs no default handling for the specified event code, calling these methods has no effect.</span></span>

## <a name="related-topics"></a><span data-ttu-id="239bc-121">См. также</span><span class="sxs-lookup"><span data-stu-id="239bc-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="239bc-122">Уведомление о событии в DirectShow</span><span class="sxs-lookup"><span data-stu-id="239bc-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 



