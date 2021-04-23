---
description: Генераторы событий мультимедиа
ms.assetid: 2e003ad4-9fcb-4834-a335-e4969ffd3a00
title: Генераторы событий мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 125bf165740b0260f9131e0df8af420c8a669d97
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105720045"
---
# <a name="media-event-generators"></a><span data-ttu-id="d5cc8-103">Генераторы событий мультимедиа</span><span class="sxs-lookup"><span data-stu-id="d5cc8-103">Media Event Generators</span></span>

<span data-ttu-id="d5cc8-104">Media Foundation обеспечивает единообразный способ отправки событий объектами.</span><span class="sxs-lookup"><span data-stu-id="d5cc8-104">Media Foundation provides a consistent way for objects to send events.</span></span> <span data-ttu-id="d5cc8-105">Объект может использовать события для сигнализации о завершении асинхронного метода или для уведомления приложения об изменении состояния объекта.</span><span class="sxs-lookup"><span data-stu-id="d5cc8-105">An object can use events to signal the completion of an asynchronous method, or to notify the application about a change in the object's state.</span></span>

<span data-ttu-id="d5cc8-106">Если объект отправляет события, он предоставляет интерфейс [**имфмедиаевентженератор**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="d5cc8-106">If an object sends events, it exposes the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="d5cc8-107">Каждый раз, когда объект отправляет новое событие, событие помещается в очередь.</span><span class="sxs-lookup"><span data-stu-id="d5cc8-107">Whenever the object sends a new event, the event is placed in a queue.</span></span> <span data-ttu-id="d5cc8-108">Приложение может запросить следующее событие из очереди, вызвав один из следующих методов:</span><span class="sxs-lookup"><span data-stu-id="d5cc8-108">The application can request the next event from the queue by calling one of the following methods:</span></span>

-   [<span data-ttu-id="d5cc8-109">**Имфмедиаевентженератор:: четный**</span><span class="sxs-lookup"><span data-stu-id="d5cc8-109">**IMFMediaEventGenerator::GetEvent**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent)

-   [<span data-ttu-id="d5cc8-110">**Имфмедиаевентженератор:: Бегинжетевент**</span><span class="sxs-lookup"><span data-stu-id="d5cc8-110">**IMFMediaEventGenerator::BeginGetEvent**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent)

<span data-ttu-id="d5cc8-111">Метод [**четный**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent) является синхронным.</span><span class="sxs-lookup"><span data-stu-id="d5cc8-111">The [**GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent) method is synchronous.</span></span> <span data-ttu-id="d5cc8-112">Если событие уже находится в очереди, метод немедленно возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d5cc8-112">If an event is already in the queue, the method returns immediately.</span></span> <span data-ttu-id="d5cc8-113">Если в очереди нет события, метод либо завершается неудачно, либо блокируется, пока следующее событие не помещается в очередь в зависимости от флага, который передается в метод **GetNext.**</span><span class="sxs-lookup"><span data-stu-id="d5cc8-113">If there is no event in the queue, the method either fails immediately, or blocks until the next event is queued, depending on which flag you pass into **GetEvent**.</span></span>

<span data-ttu-id="d5cc8-114">Метод [**бегинжетевент**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) является асинхронным, поэтому он никогда не блокируется.</span><span class="sxs-lookup"><span data-stu-id="d5cc8-114">The [**BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) method is asynchronous, so it never blocks.</span></span> <span data-ttu-id="d5cc8-115">Этот метод принимает указатель на интерфейс [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) , который должен быть реализован приложением.</span><span class="sxs-lookup"><span data-stu-id="d5cc8-115">This method takes a pointer to the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface, which the application must implement.</span></span> <span data-ttu-id="d5cc8-116">При вызове обратного вызова приложение вызывает [**имфмедиаевентженератор:: енджетевент**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) , чтобы получить событие из очереди.</span><span class="sxs-lookup"><span data-stu-id="d5cc8-116">When the callback is invoked, the application calls [**IMFMediaEventGenerator::EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) to get the event from the queue.</span></span> <span data-ttu-id="d5cc8-117">Дополнительные сведения о **имфасинккаллбакк** см. в разделе [асинхронные методы обратного вызова](asynchronous-callback-methods.md).</span><span class="sxs-lookup"><span data-stu-id="d5cc8-117">For more information about **IMFAsyncCallback**, see [Asynchronous Callback Methods](asynchronous-callback-methods.md).</span></span>

<span data-ttu-id="d5cc8-118">События представлены интерфейсом [**имфмедиаевент**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) .</span><span class="sxs-lookup"><span data-stu-id="d5cc8-118">Events are represented by the [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) interface.</span></span> <span data-ttu-id="d5cc8-119">Этот интерфейс имеет следующие методы:</span><span class="sxs-lookup"><span data-stu-id="d5cc8-119">This interface has the following methods:</span></span>

-   <span data-ttu-id="d5cc8-120">[**GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype): получает тип события.</span><span class="sxs-lookup"><span data-stu-id="d5cc8-120">[**GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype): Retrieves the event type.</span></span> <span data-ttu-id="d5cc8-121">Тип события указывает, что произошло для активации события.</span><span class="sxs-lookup"><span data-stu-id="d5cc8-121">The event type indicates what happened to trigger the event.</span></span>

-   <span data-ttu-id="d5cc8-122">Параметр [**Status**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus): получает значение **HRESULT** , указывающее, успешно ли выполнена операция, вызвавшая событие.</span><span class="sxs-lookup"><span data-stu-id="d5cc8-122">[**GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus): Retrieves an **HRESULT** value, indicating whether the operation that triggered the event was successful.</span></span> <span data-ttu-id="d5cc8-123">Если операция завершается со сбоем асинхронно, функция **OnStatus** возвращает код ошибки.</span><span class="sxs-lookup"><span data-stu-id="d5cc8-123">If an operation fails asynchronously, **GetStatus** returns a failure code.</span></span>

-   <span data-ttu-id="d5cc8-124">[**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue): извлекает **пропвариант** , содержащий данные события.</span><span class="sxs-lookup"><span data-stu-id="d5cc8-124">[**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue): Retrieves a **PROPVARIANT** that contains event data.</span></span> <span data-ttu-id="d5cc8-125">Данные события зависят от типа события.</span><span class="sxs-lookup"><span data-stu-id="d5cc8-125">The event data depends on the event type.</span></span> <span data-ttu-id="d5cc8-126">Некоторые события не содержат данных.</span><span class="sxs-lookup"><span data-stu-id="d5cc8-126">Some events do not have any data.</span></span>

-   <span data-ttu-id="d5cc8-127">[**Жетекстендедтипе**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype): получает **идентификатор GUID**.</span><span class="sxs-lookup"><span data-stu-id="d5cc8-127">[**GetExtendedType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype): Retrieves a **GUID**.</span></span> <span data-ttu-id="d5cc8-128">Этот метод применяется к [событию микстендедтипе](meextendedtype.md)и предоставляет способ определения пользовательских событий.</span><span class="sxs-lookup"><span data-stu-id="d5cc8-128">This method applies to the [MEExtendedType Event](meextendedtype.md), and provides a way to define custom events.</span></span>

<span data-ttu-id="d5cc8-129">Интерфейс [**имфмедиаевент**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) также наследует интерфейс [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="d5cc8-129">The [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) interface also inherits the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="d5cc8-130">Некоторые события содержат дополнительные сведения в качестве атрибутов.</span><span class="sxs-lookup"><span data-stu-id="d5cc8-130">Some events carry additional information as attributes.</span></span>

<span data-ttu-id="d5cc8-131">Список типов событий и связанных с ними данных и атрибутов см. в разделе [Media Foundation Events](media-foundation-events.md).</span><span class="sxs-lookup"><span data-stu-id="d5cc8-131">For a list of event types and their associated data and attributes, see [Media Foundation Events](media-foundation-events.md).</span></span>

## <a name="implementing-imfmediaeventgenerator"></a><span data-ttu-id="d5cc8-132">Реализация Имфмедиаевентженератор</span><span class="sxs-lookup"><span data-stu-id="d5cc8-132">Implementing IMFMediaEventGenerator</span></span>

<span data-ttu-id="d5cc8-133">При написании подключаемого компонента для Media Foundation, например пользовательского источника мультимедиа или приемника мультимедиа, может потребоваться реализовать [**имфмедиаевентженератор**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator).</span><span class="sxs-lookup"><span data-stu-id="d5cc8-133">If you are writing a plug-in component for Media Foundation, such as a custom media source or media sink, you might need to implement [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator).</span></span> <span data-ttu-id="d5cc8-134">Чтобы упростить эту задачу, Media Foundation предоставляет вспомогательный объект, реализующий очередь событий.</span><span class="sxs-lookup"><span data-stu-id="d5cc8-134">To make this easier, Media Foundation provides a helper object that implements an event queue.</span></span> <span data-ttu-id="d5cc8-135">Создайте очередь событий, вызвав функцию [**мфкреативенткуеуе**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateeventqueue) .</span><span class="sxs-lookup"><span data-stu-id="d5cc8-135">Create the event queue by calling the [**MFCreateEventQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateeventqueue) function.</span></span> <span data-ttu-id="d5cc8-136">Очередь событий предоставляет интерфейс [**имфмедиаевенткуеуе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventqueue) .</span><span class="sxs-lookup"><span data-stu-id="d5cc8-136">The event queue exposes the [**IMFMediaEventQueue**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventqueue) interface.</span></span> <span data-ttu-id="d5cc8-137">В реализации методов **имфмедиаевентженератор** в объекте вызовите соответствующий метод в очереди событий.</span><span class="sxs-lookup"><span data-stu-id="d5cc8-137">In your object's implementation of the **IMFMediaEventGenerator** methods, call the corresponding method on the event queue.</span></span>

<span data-ttu-id="d5cc8-138">Объект очереди событий является потокобезопасным.</span><span class="sxs-lookup"><span data-stu-id="d5cc8-138">The event queue object is thread safe.</span></span> <span data-ttu-id="d5cc8-139">Никогда не держите тот же самый важный объект раздела [**при вызове**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-getevent) метода GetObject и [**куеуивент**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-queueevent), так как **четный** может блокировать ожидание [**куеуивент**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueevent).</span><span class="sxs-lookup"><span data-stu-id="d5cc8-139">Never hold the same critical section object when calling [**GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-getevent) and [**QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-queueevent), because **GetEvent** might block indefinitely waiting for [**QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueevent).</span></span> <span data-ttu-id="d5cc8-140">Если вы удерживаете одинаковую критическую секцию для обоих методов, это вызовет взаимоблокировку.</span><span class="sxs-lookup"><span data-stu-id="d5cc8-140">If you hold the same critical section for both methods, it will cause a deadlock.</span></span>

<span data-ttu-id="d5cc8-141">Перед освобождением очереди событий вызовите [**имфмедиаевенткуеуе:: Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown) , чтобы освободить ресурсы, удерживаемые объектом.</span><span class="sxs-lookup"><span data-stu-id="d5cc8-141">Before releasing the event queue, call [**IMFMediaEventQueue::Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown) to release the resources that the object holds.</span></span>

<span data-ttu-id="d5cc8-142">Когда объекту необходимо вызвать событие, вызовите один из следующих методов в очереди событий:</span><span class="sxs-lookup"><span data-stu-id="d5cc8-142">When your object needs to raise an event, call one of the following methods on the event queue:</span></span>

-   [<span data-ttu-id="d5cc8-143">**Имфмедиаевенткуеуе:: Куеуивент**</span><span class="sxs-lookup"><span data-stu-id="d5cc8-143">**IMFMediaEventQueue::QueueEvent**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueevent)

-   [<span data-ttu-id="d5cc8-144">**Имфмедиаевенткуеуе:: Куеуивентпарамвар**</span><span class="sxs-lookup"><span data-stu-id="d5cc8-144">**IMFMediaEventQueue::QueueEventParamVar**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueeventparamvar)

-   [<span data-ttu-id="d5cc8-145">**Имфмедиаевенткуеуе:: Куеуивентпарамунк**</span><span class="sxs-lookup"><span data-stu-id="d5cc8-145">**IMFMediaEventQueue::QueueEventParamUnk**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueeventparamunk)

<span data-ttu-id="d5cc8-146">Эти методы помещают новое событие в очередь и передают вызывающий объект, ожидающий следующего события.</span><span class="sxs-lookup"><span data-stu-id="d5cc8-146">These methods put a new event on the queue and signal any caller that is waiting for the next event.</span></span>

<span data-ttu-id="d5cc8-147">В следующем коде показан класс, реализующий [**имфмедиаевентженератор**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) с помощью этого вспомогательного объекта.</span><span class="sxs-lookup"><span data-stu-id="d5cc8-147">The following code shows a class that implements [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) using this helper object.</span></span> <span data-ttu-id="d5cc8-148">Этот класс определяет открытый метод **завершения работы** , который завершает работу очереди событий и освобождает указатель очереди событий.</span><span class="sxs-lookup"><span data-stu-id="d5cc8-148">This class defines a public **Shutdown** method that shuts down the event queue and releases the event queue pointer.</span></span> <span data-ttu-id="d5cc8-149">Такое поведение характерно для источников мультимедиа и приемников мультимедиа, которые всегда имеют метод **завершения работы** .</span><span class="sxs-lookup"><span data-stu-id="d5cc8-149">This behavior would be typical for media sources and media sinks, which always have a **Shutdown** method.</span></span>


```C++
class MyObject : public IMFMediaEventGenerator
{
private:
    long                m_nRefCount;    // Reference count.
    CRITICAL_SECTION    m_critSec;      // Critical section.
    IMFMediaEventQueue *m_pQueue;       // Event queue.
    BOOL                m_bShutdown;    // Is the object shut down?

    // CheckShutdown: Returns MF_E_SHUTDOWN if the object was shut down.
    HRESULT CheckShutdown() const 
    {
        return (m_bShutdown? MF_E_SHUTDOWN : S_OK);
    }

public:
    MyObject(HRESULT &hr) : m_nRefCount(0), m_pQueue(NULL), m_bShutdown(FALSE)
    {
        InitializeCriticalSection(&m_critSec);
        
        // Create the event queue.
        hr = MFCreateEventQueue(&m_pQueue);
    }

    // Shutdown: Shuts down this object.
    HRESULT Shutdown()
    {
        EnterCriticalSection(&m_critSec);

        HRESULT hr = CheckShutdown();
        if (SUCCEEDED(hr))
        {
            // Shut down the event queue.
            if (m_pQueue)
            {
                hr = m_pQueue->Shutdown();
            }

            // Release the event queue.
            SAFE_RELEASE(m_pQueue);
            // Release any other objects owned by the class (not shown).

            // Set the shutdown flag.
            m_bShutdown = TRUE;
        }

        LeaveCriticalSection(&m_critSec);
        return hr;
    }

    // TODO: Implement IUnknown (not shown).
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv);

    // IMFMediaEventGenerator::BeginGetEvent
    STDMETHODIMP BeginGetEvent(IMFAsyncCallback* pCallback, IUnknown* pState)
    {
        EnterCriticalSection(&m_critSec);

        HRESULT hr = CheckShutdown();
        if (SUCCEEDED(hr))
        {
            hr = m_pQueue->BeginGetEvent(pCallback, pState);
        }

        LeaveCriticalSection(&m_critSec);
        return hr;    
    }

    // IMFMediaEventGenerator::EndGetEvent
    STDMETHODIMP EndGetEvent(IMFAsyncResult* pResult, IMFMediaEvent** ppEvent)
    {
        EnterCriticalSection(&m_critSec);

        HRESULT hr = CheckShutdown();
        if (SUCCEEDED(hr))
        {
            hr = m_pQueue->EndGetEvent(pResult, ppEvent);
        }

        LeaveCriticalSection(&m_critSec);
        return hr;    
    }

    // IMFMediaEventGenerator::GetEvent
    STDMETHODIMP GetEvent(DWORD dwFlags, IMFMediaEvent** ppEvent)
    {
        // Because GetEvent can block indefinitely, it requires
        // a slightly different locking strategy.
        IMFMediaEventQueue *pQueue = NULL;

        // Hold lock.
        EnterCriticalSection(&m_critSec);

        // Check shutdown
        HRESULT hr = CheckShutdown();

        // Store the pointer in a local variable, so that another thread
        // does not release it after we leave the critical section.
        if (SUCCEEDED(hr))
        {
            pQueue = m_pQueue;
            pQueue->AddRef();
        }

        // Release the lock.
        LeaveCriticalSection(&m_critSec);

        if (SUCCEEDED(hr))
        {
            hr = pQueue->GetEvent(dwFlags, ppEvent);
        }

        SAFE_RELEASE(pQueue);
        return hr;
    }

    // IMFMediaEventGenerator::QueueEvent
    STDMETHODIMP QueueEvent(
        MediaEventType met, REFGUID extendedType, 
        HRESULT hrStatus, const PROPVARIANT* pvValue)
    {
        EnterCriticalSection(&m_critSec);

        HRESULT hr = CheckShutdown();
        if (SUCCEEDED(hr))
        {
            hr = m_pQueue->QueueEventParamVar(
                met, extendedType, hrStatus, pvValue);
        }

        LeaveCriticalSection(&m_critSec);
        return hr;
    }

private:

    // The destructor is private. The caller must call Release.
    virtual ~MyObject()
    {
        assert(m_bShutdown);
        assert(m_nRefCount == 0);
    }
};
```



## <a name="related-topics"></a><span data-ttu-id="d5cc8-150">См. также</span><span class="sxs-lookup"><span data-stu-id="d5cc8-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5cc8-151">Media Foundation API платформы</span><span class="sxs-lookup"><span data-stu-id="d5cc8-151">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> </dl>

 

 



