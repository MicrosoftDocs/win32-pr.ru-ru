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
# <a name="media-event-generators"></a>Генераторы событий мультимедиа

Media Foundation обеспечивает единообразный способ отправки событий объектами. Объект может использовать события для сигнализации о завершении асинхронного метода или для уведомления приложения об изменении состояния объекта.

Если объект отправляет события, он предоставляет интерфейс [**имфмедиаевентженератор**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) . Каждый раз, когда объект отправляет новое событие, событие помещается в очередь. Приложение может запросить следующее событие из очереди, вызвав один из следующих методов:

-   [**Имфмедиаевентженератор:: четный**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent)

-   [**Имфмедиаевентженератор:: Бегинжетевент**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent)

Метод [**четный**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent) является синхронным. Если событие уже находится в очереди, метод немедленно возвращает значение. Если в очереди нет события, метод либо завершается неудачно, либо блокируется, пока следующее событие не помещается в очередь в зависимости от флага, который передается в метод **GetNext.**

Метод [**бегинжетевент**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) является асинхронным, поэтому он никогда не блокируется. Этот метод принимает указатель на интерфейс [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) , который должен быть реализован приложением. При вызове обратного вызова приложение вызывает [**имфмедиаевентженератор:: енджетевент**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) , чтобы получить событие из очереди. Дополнительные сведения о **имфасинккаллбакк** см. в разделе [асинхронные методы обратного вызова](asynchronous-callback-methods.md).

События представлены интерфейсом [**имфмедиаевент**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) . Этот интерфейс имеет следующие методы:

-   [**GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype): получает тип события. Тип события указывает, что произошло для активации события.

-   Параметр [**Status**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus): получает значение **HRESULT** , указывающее, успешно ли выполнена операция, вызвавшая событие. Если операция завершается со сбоем асинхронно, функция **OnStatus** возвращает код ошибки.

-   [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue): извлекает **пропвариант** , содержащий данные события. Данные события зависят от типа события. Некоторые события не содержат данных.

-   [**Жетекстендедтипе**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype): получает **идентификатор GUID**. Этот метод применяется к [событию микстендедтипе](meextendedtype.md)и предоставляет способ определения пользовательских событий.

Интерфейс [**имфмедиаевент**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) также наследует интерфейс [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) . Некоторые события содержат дополнительные сведения в качестве атрибутов.

Список типов событий и связанных с ними данных и атрибутов см. в разделе [Media Foundation Events](media-foundation-events.md).

## <a name="implementing-imfmediaeventgenerator"></a>Реализация Имфмедиаевентженератор

При написании подключаемого компонента для Media Foundation, например пользовательского источника мультимедиа или приемника мультимедиа, может потребоваться реализовать [**имфмедиаевентженератор**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator). Чтобы упростить эту задачу, Media Foundation предоставляет вспомогательный объект, реализующий очередь событий. Создайте очередь событий, вызвав функцию [**мфкреативенткуеуе**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateeventqueue) . Очередь событий предоставляет интерфейс [**имфмедиаевенткуеуе**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventqueue) . В реализации методов **имфмедиаевентженератор** в объекте вызовите соответствующий метод в очереди событий.

Объект очереди событий является потокобезопасным. Никогда не держите тот же самый важный объект раздела [**при вызове**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-getevent) метода GetObject и [**куеуивент**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-queueevent), так как **четный** может блокировать ожидание [**куеуивент**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueevent). Если вы удерживаете одинаковую критическую секцию для обоих методов, это вызовет взаимоблокировку.

Перед освобождением очереди событий вызовите [**имфмедиаевенткуеуе:: Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown) , чтобы освободить ресурсы, удерживаемые объектом.

Когда объекту необходимо вызвать событие, вызовите один из следующих методов в очереди событий:

-   [**Имфмедиаевенткуеуе:: Куеуивент**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueevent)

-   [**Имфмедиаевенткуеуе:: Куеуивентпарамвар**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueeventparamvar)

-   [**Имфмедиаевенткуеуе:: Куеуивентпарамунк**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-queueeventparamunk)

Эти методы помещают новое событие в очередь и передают вызывающий объект, ожидающий следующего события.

В следующем коде показан класс, реализующий [**имфмедиаевентженератор**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) с помощью этого вспомогательного объекта. Этот класс определяет открытый метод **завершения работы** , который завершает работу очереди событий и освобождает указатель очереди событий. Такое поведение характерно для источников мультимедиа и приемников мультимедиа, которые всегда имеют метод **завершения работы** .


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Media Foundation API платформы](media-foundation-platform-apis.md)
</dt> </dl>

 

 



