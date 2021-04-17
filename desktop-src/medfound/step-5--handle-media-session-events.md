---
description: В этом разделе приводится шаг 5 руководства по воспроизведению мультимедийных файлов с помощью Media Foundation.
ms.assetid: db9b896f-6f56-47b1-b129-331c984e0b16
title: Шаг 5. Работа с событиями сеанса мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2ea3092189644f800a5cb27d2e8b07744f5d90c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105713305"
---
# <a name="step-5-handle-media-session-events"></a><span data-ttu-id="1de4a-103">Шаг 5. Работа с событиями сеанса мультимедиа</span><span class="sxs-lookup"><span data-stu-id="1de4a-103">Step 5: Handle Media Session Events</span></span>

<span data-ttu-id="1de4a-104">В этом разделе приводится шаг 5 руководства по [воспроизведению мультимедийных файлов с помощью Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="1de4a-104">This topic is step 5 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="1de4a-105">Полный код показан в разделе [Пример воспроизведения сеанса мультимедиа](media-session-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="1de4a-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="1de4a-106">Дополнительные сведения по этой теме см. в статье [генераторы событий мультимедиа](media-event-generators.md).</span><span class="sxs-lookup"><span data-stu-id="1de4a-106">For background on this topic, read [Media Event Generators](media-event-generators.md).</span></span> <span data-ttu-id="1de4a-107">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="1de4a-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="1de4a-108">Получение событий сеанса</span><span class="sxs-lookup"><span data-stu-id="1de4a-108">Getting Session Events</span></span>](#getting-session-events)
-   [<span data-ttu-id="1de4a-109">месессионтопологистатус</span><span class="sxs-lookup"><span data-stu-id="1de4a-109">MESessionTopologyStatus</span></span>](#mesessiontopologystatus)
-   [<span data-ttu-id="1de4a-110">миндофпресентатион</span><span class="sxs-lookup"><span data-stu-id="1de4a-110">MEEndOfPresentation</span></span>](#meendofpresentation)
-   [<span data-ttu-id="1de4a-111">меневпресентатион</span><span class="sxs-lookup"><span data-stu-id="1de4a-111">MENewPresentation</span></span>](#menewpresentation)
-   [<span data-ttu-id="1de4a-112">См. также</span><span class="sxs-lookup"><span data-stu-id="1de4a-112">Related topics</span></span>](#related-topics)

## <a name="getting-session-events"></a><span data-ttu-id="1de4a-113">Получение событий сеанса</span><span class="sxs-lookup"><span data-stu-id="1de4a-113">Getting Session Events</span></span>

<span data-ttu-id="1de4a-114">Чтобы получить события из сеанса мультимедиа, объект Кплайер вызывает метод [**имфмедиаевентженератор:: бегинжетевент**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) , как показано на [шаге 4. Создание сеанса мультимедиа](step-4--create-the-media-session.md).</span><span class="sxs-lookup"><span data-stu-id="1de4a-114">To get events from the Media Session, the CPlayer object calls the [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) method, as shown in [Step 4: Create the Media Session](step-4--create-the-media-session.md).</span></span> <span data-ttu-id="1de4a-115">Этот метод является асинхронным, то есть он немедленно возвращается вызывающему.</span><span class="sxs-lookup"><span data-stu-id="1de4a-115">This method is asynchronous, meaning it returns to the caller immediately.</span></span> <span data-ttu-id="1de4a-116">Когда происходит событие следующего сеанса, сеанс мультимедиа вызывает метод [**имфасинккаллбакк:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) объекта кплайер.</span><span class="sxs-lookup"><span data-stu-id="1de4a-116">When the next session event occurs, the Media Session calls the [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method of the CPlayer object.</span></span>

<span data-ttu-id="1de4a-117">Важно помнить, что [**вызов**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) вызывается из рабочего потока, а не из потока приложения.</span><span class="sxs-lookup"><span data-stu-id="1de4a-117">It is important to remember that [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) gets called from a worker thread, not from the application thread.</span></span> <span data-ttu-id="1de4a-118">Поэтому реализация **вызова** должна быть потокобезопасной.</span><span class="sxs-lookup"><span data-stu-id="1de4a-118">Therefore, the implementation of **Invoke** must be multithread-safe.</span></span> <span data-ttu-id="1de4a-119">Одним из подходов является защита данных элемента с помощью критической секции.</span><span class="sxs-lookup"><span data-stu-id="1de4a-119">One approach would be to protect the member data with a critical section.</span></span> <span data-ttu-id="1de4a-120">Однако `CPlayer` класс демонстрирует альтернативный подход:</span><span class="sxs-lookup"><span data-stu-id="1de4a-120">However, the `CPlayer` class shows an alternative approach:</span></span>

1.  <span data-ttu-id="1de4a-121">В методе [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) объект кплайер отправляет в приложение сообщение **о \_ \_ \_ событии проигрывателя приложения WM** .</span><span class="sxs-lookup"><span data-stu-id="1de4a-121">In the [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method, the CPlayer object posts a **WM\_APP\_PLAYER\_EVENT** message to the application.</span></span> <span data-ttu-id="1de4a-122">Параметр Message является указателем [**имфмедиаевент**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) .</span><span class="sxs-lookup"><span data-stu-id="1de4a-122">The message parameter is an [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) pointer.</span></span>
2.  <span data-ttu-id="1de4a-123">Приложение получает сообщение о **\_ \_ \_ событии проигрывателя приложения WM** .</span><span class="sxs-lookup"><span data-stu-id="1de4a-123">The application receives the **WM\_APP\_PLAYER\_EVENT** message.</span></span>
3.  <span data-ttu-id="1de4a-124">Приложение вызывает `CPlayer::HandleEvent` метод, передавая указатель [**имфмедиаевент**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) .</span><span class="sxs-lookup"><span data-stu-id="1de4a-124">The application calls the `CPlayer::HandleEvent` method, passing in the [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) pointer.</span></span>
4.  <span data-ttu-id="1de4a-125">`HandleEvent`Метод отвечает на событие.</span><span class="sxs-lookup"><span data-stu-id="1de4a-125">The `HandleEvent` method responds to the event.</span></span>

<span data-ttu-id="1de4a-126">В следующем коде показан метод [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) :</span><span class="sxs-lookup"><span data-stu-id="1de4a-126">The following code shows the [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method:</span></span>


```C++
//  Callback for the asynchronous BeginGetEvent method.

HRESULT CPlayer::Invoke(IMFAsyncResult *pResult)
{
    MediaEventType meType = MEUnknown;  // Event type

    IMFMediaEvent *pEvent = NULL;

    // Get the event from the event queue.
    HRESULT hr = m_pSession->EndGetEvent(pResult, &pEvent);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the event type. 
    hr = pEvent->GetType(&meType);
    if (FAILED(hr))
    {
        goto done;
    }

    if (meType == MESessionClosed)
    {
        // The session was closed. 
        // The application is waiting on the m_hCloseEvent event handle. 
        SetEvent(m_hCloseEvent);
    }
    else
    {
        // For all other events, get the next event in the queue.
        hr = m_pSession->BeginGetEvent(this, NULL);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    // Check the application state. 
        
    // If a call to IMFMediaSession::Close is pending, it means the 
    // application is waiting on the m_hCloseEvent event and
    // the application's message loop is blocked. 

    // Otherwise, post a private window message to the application. 

    if (m_state != Closing)
    {
        // Leave a reference count on the event.
        pEvent->AddRef();

        PostMessage(m_hwndEvent, WM_APP_PLAYER_EVENT, 
            (WPARAM)pEvent, (LPARAM)meType);
    }

done:
    SafeRelease(&pEvent);
    return S_OK;
}
```



<span data-ttu-id="1de4a-127">Метод [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="1de4a-127">The [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method performs the following steps:</span></span>

1.  <span data-ttu-id="1de4a-128">Вызовите метод [**имфмедиаевентженератор:: енджетевент**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) , чтобы получить событие.</span><span class="sxs-lookup"><span data-stu-id="1de4a-128">Call [**IMFMediaEventGenerator::EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) to get the event.</span></span> <span data-ttu-id="1de4a-129">Этот метод возвращает указатель на интерфейс [**имфмедиаевент**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) .</span><span class="sxs-lookup"><span data-stu-id="1de4a-129">This method returns a pointer to the [**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) interface.</span></span>
2.  <span data-ttu-id="1de4a-130">Вызовите метод [**имфмедиаевент:: GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype) , чтобы получить код события.</span><span class="sxs-lookup"><span data-stu-id="1de4a-130">Call [**IMFMediaEvent::GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype) to get the event code.</span></span>
3.  <span data-ttu-id="1de4a-131">Если код события — [месессионклосед](mesessionclosed.md), вызовите выполнить SetEvent, чтобы задать событие *m \_ хклосивент* .</span><span class="sxs-lookup"><span data-stu-id="1de4a-131">If the event code is [MESessionClosed](mesessionclosed.md), call SetEvent to set the *m\_hCloseEvent* event.</span></span> <span data-ttu-id="1de4a-132">Причина этого шага описана в [шаге 7: завершение сеанса мультимедиа](step-7--shut-down-the-media-session.md), а также в комментариях к коду.</span><span class="sxs-lookup"><span data-stu-id="1de4a-132">The reason for this step is explained in [Step 7: Shut Down the Media Session](step-7--shut-down-the-media-session.md), and also in the code comments.</span></span>
4.  <span data-ttu-id="1de4a-133">Для всех других кодов событий вызовите метод [**имфмедиаевентженератор:: бегинжетевент**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) , чтобы запросить следующее событие.</span><span class="sxs-lookup"><span data-stu-id="1de4a-133">For all other event codes, call [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) to request the next event.</span></span>
5.  <span data-ttu-id="1de4a-134">Опубликуйте в окне сообщение о **\_ \_ \_ событии проигрывателя приложения WM** .</span><span class="sxs-lookup"><span data-stu-id="1de4a-134">Post a **WM\_APP\_PLAYER\_EVENT** message to the window.</span></span>

<span data-ttu-id="1de4a-135">В следующем коде показан метод Хандливент, который вызывается, когда приложение получает сообщение о **\_ \_ \_ событии проигрывателя приложения WM** :</span><span class="sxs-lookup"><span data-stu-id="1de4a-135">The following code shows the HandleEvent method, which is called when the application receives the **WM\_APP\_PLAYER\_EVENT** message:</span></span>


```C++
HRESULT CPlayer::HandleEvent(UINT_PTR pEventPtr)
{
    HRESULT hrStatus = S_OK;            
    MediaEventType meType = MEUnknown;  

    IMFMediaEvent *pEvent = (IMFMediaEvent*)pEventPtr;

    if (pEvent == NULL)
    {
        return E_POINTER;
    }

    // Get the event type.
    HRESULT hr = pEvent->GetType(&meType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the event status. If the operation that triggered the event 
    // did not succeed, the status is a failure code.
    hr = pEvent->GetStatus(&hrStatus);

    // Check if the async operation succeeded.
    if (SUCCEEDED(hr) && FAILED(hrStatus)) 
    {
        hr = hrStatus;
    }
    if (FAILED(hr))
    {
        goto done;
    }

    switch(meType)
    {
    case MESessionTopologyStatus:
        hr = OnTopologyStatus(pEvent);
        break;

    case MEEndOfPresentation:
        hr = OnPresentationEnded(pEvent);
        break;

    case MENewPresentation:
        hr = OnNewPresentation(pEvent);
        break;

    default:
        hr = OnSessionEvent(pEvent, meType);
        break;
    }

done:
    SafeRelease(&pEvent);
    return hr;
}
```



<span data-ttu-id="1de4a-136">Этот метод вызывает [**имфмедиаевент:: GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype) , чтобы получить тип события и [**Имфмедиаевент:: Status**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) , чтобы получить успешный код ошибки, связанный с событием.</span><span class="sxs-lookup"><span data-stu-id="1de4a-136">This method calls [**IMFMediaEvent::GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype) to get the event type and [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) to get the success of failure code associated with the event.</span></span> <span data-ttu-id="1de4a-137">Следующее выполняемое действие зависит от кода события.</span><span class="sxs-lookup"><span data-stu-id="1de4a-137">The next action taken depends on the event code.</span></span>

## <a name="mesessiontopologystatus"></a><span data-ttu-id="1de4a-138">месессионтопологистатус</span><span class="sxs-lookup"><span data-stu-id="1de4a-138">MESessionTopologyStatus</span></span>

<span data-ttu-id="1de4a-139">Событие [месессионтопологистатус](mesessiontopologystatus.md) сигнализирует об изменении состояния топологии.</span><span class="sxs-lookup"><span data-stu-id="1de4a-139">The [MESessionTopologyStatus](mesessiontopologystatus.md) event signals a change in the status of the topology.</span></span> <span data-ttu-id="1de4a-140">Атрибут [**\_ \_ \_ состояния топологии событий MF**](mf-event-topology-status-attribute.md) объекта события содержит состояние.</span><span class="sxs-lookup"><span data-stu-id="1de4a-140">The [**MF\_EVENT\_TOPOLOGY\_STATUS**](mf-event-topology-status-attribute.md) attribute of the event object contains the status.</span></span> <span data-ttu-id="1de4a-141">В этом примере единственное интересующее вас значение — **MF \_ топостатус \_ Ready**, что означает, что воспроизведение готово к запуску.</span><span class="sxs-lookup"><span data-stu-id="1de4a-141">For this example, the only value of interest is **MF\_TOPOSTATUS\_READY**, which indicates that playback is ready to start.</span></span>


```C++
HRESULT CPlayer::OnTopologyStatus(IMFMediaEvent *pEvent)
{
    UINT32 status; 

    HRESULT hr = pEvent->GetUINT32(MF_EVENT_TOPOLOGY_STATUS, &status);
    if (SUCCEEDED(hr) && (status == MF_TOPOSTATUS_READY))
    {
        SafeRelease(&m_pVideoDisplay);

        // Get the IMFVideoDisplayControl interface from EVR. This call is
        // expected to fail if the media file does not have a video stream.

        (void)MFGetService(m_pSession, MR_VIDEO_RENDER_SERVICE, 
            IID_PPV_ARGS(&m_pVideoDisplay));

        hr = StartPlayback();
    }
    return hr;
}
```



<span data-ttu-id="1de4a-142">`CPlayer::StartPlayback`Метод показан на [шаге 6. Управление воспроизведением](step-6--control-playback.md).</span><span class="sxs-lookup"><span data-stu-id="1de4a-142">The `CPlayer::StartPlayback` method is shown in [Step 6: Control Playback](step-6--control-playback.md).</span></span>

<span data-ttu-id="1de4a-143">В этом примере также вызывается [**мфжетсервице**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) для получения интерфейса [**имфвидеодисплайконтрол**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) из [расширенного модуля подготовки видео](enhanced-video-renderer.md) (Евр).</span><span class="sxs-lookup"><span data-stu-id="1de4a-143">This example also calls [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) to get the [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface from the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR).</span></span> <span data-ttu-id="1de4a-144">Этот интерфейс необходим для выполнения перерисовки и изменения размера окна видео, также показанного в [шаге 6: Управление воспроизведением](step-6--control-playback.md).</span><span class="sxs-lookup"><span data-stu-id="1de4a-144">This interface is needed to handle repainting and resizing the video window, also shown in [Step 6: Control Playback](step-6--control-playback.md).</span></span>

## <a name="meendofpresentation"></a><span data-ttu-id="1de4a-145">миндофпресентатион</span><span class="sxs-lookup"><span data-stu-id="1de4a-145">MEEndOfPresentation</span></span>

<span data-ttu-id="1de4a-146">Событие [миндофпресентатион](meendofpresentation.md) сигнализирует, что воспроизведение достигло конца файла.</span><span class="sxs-lookup"><span data-stu-id="1de4a-146">The [MEEndOfPresentation](meendofpresentation.md) event signals that playback has reached the end of the file.</span></span> <span data-ttu-id="1de4a-147">Сеанс мультимедиа автоматически переключается обратно в остановленное состояние.</span><span class="sxs-lookup"><span data-stu-id="1de4a-147">The Media Session automatically switches back to the stopped state.</span></span>


```C++
//  Handler for MEEndOfPresentation event.
HRESULT CPlayer::OnPresentationEnded(IMFMediaEvent *pEvent)
{
    // The session puts itself into the stopped state automatically.
    m_state = Stopped;
    return S_OK;
}
```



## <a name="menewpresentation"></a><span data-ttu-id="1de4a-148">меневпресентатион</span><span class="sxs-lookup"><span data-stu-id="1de4a-148">MENewPresentation</span></span>

<span data-ttu-id="1de4a-149">Событие [меневпресентатион](menewpresentation.md) сигнализирует о начале новой презентации.</span><span class="sxs-lookup"><span data-stu-id="1de4a-149">The [MENewPresentation](menewpresentation.md) event signals the start of a new presentation.</span></span> <span data-ttu-id="1de4a-150">Данные события являются [**имфпресентатиондескриптор**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) указателем для новой презентации.</span><span class="sxs-lookup"><span data-stu-id="1de4a-150">The event data is an [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) pointer for the new presentation.</span></span>

<span data-ttu-id="1de4a-151">Во многих случаях это событие не будет появляться вообще.</span><span class="sxs-lookup"><span data-stu-id="1de4a-151">In many cases, you will not receive this event at all.</span></span> <span data-ttu-id="1de4a-152">В этом случае используйте указатель [**имфпресентатиондескриптор**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) для создания новой топологии воспроизведения, как показано на [шаге 3. Открытие файла мультимедиа](step-3--open-a-media-file.md).</span><span class="sxs-lookup"><span data-stu-id="1de4a-152">If you do, use the [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) pointer to create a new playback topology, as shown in [Step 3: Open a Media File](step-3--open-a-media-file.md).</span></span> <span data-ttu-id="1de4a-153">Затем помещает новую топологию в очередь в сеансе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="1de4a-153">Then queue the new topology on the Media Session.</span></span>


```C++
//  Handler for MENewPresentation event.
//
//  This event is sent if the media source has a new presentation, which 
//  requires a new topology. 

HRESULT CPlayer::OnNewPresentation(IMFMediaEvent *pEvent)
{
    IMFPresentationDescriptor *pPD = NULL;
    IMFTopology *pTopology = NULL;

    // Get the presentation descriptor from the event.
    HRESULT hr = GetEventObject(pEvent, &pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create a partial topology.
    hr = CreatePlaybackTopology(m_pSource, pPD,  m_hwndVideo,&pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the topology on the media session.
    hr = m_pSession->SetTopology(0, pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    m_state = OpenPending;

done:
    SafeRelease(&pTopology);
    SafeRelease(&pPD);
    return S_OK;
}
```



<span data-ttu-id="1de4a-154">Далее: [Шаг 6. Управление воспроизведением](step-6--control-playback.md)</span><span class="sxs-lookup"><span data-stu-id="1de4a-154">Next: [Step 6: Control Playback](step-6--control-playback.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="1de4a-155">См. также</span><span class="sxs-lookup"><span data-stu-id="1de4a-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1de4a-156">Воспроизведение звука/видео</span><span class="sxs-lookup"><span data-stu-id="1de4a-156">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="1de4a-157">Воспроизведение мультимедийных файлов с помощью Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1de4a-157">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



