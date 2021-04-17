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
# <a name="step-5-handle-media-session-events"></a>Шаг 5. Работа с событиями сеанса мультимедиа

В этом разделе приводится шаг 5 руководства по [воспроизведению мультимедийных файлов с помощью Media Foundation](how-to-play-unprotected-media-files.md). Полный код показан в разделе [Пример воспроизведения сеанса мультимедиа](media-session-playback-example.md).

Дополнительные сведения по этой теме см. в статье [генераторы событий мультимедиа](media-event-generators.md). В этом разделе содержатся следующие подразделы.

-   [Получение событий сеанса](#getting-session-events)
-   [месессионтопологистатус](#mesessiontopologystatus)
-   [миндофпресентатион](#meendofpresentation)
-   [меневпресентатион](#menewpresentation)
-   [См. также](#related-topics)

## <a name="getting-session-events"></a>Получение событий сеанса

Чтобы получить события из сеанса мультимедиа, объект Кплайер вызывает метод [**имфмедиаевентженератор:: бегинжетевент**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) , как показано на [шаге 4. Создание сеанса мультимедиа](step-4--create-the-media-session.md). Этот метод является асинхронным, то есть он немедленно возвращается вызывающему. Когда происходит событие следующего сеанса, сеанс мультимедиа вызывает метод [**имфасинккаллбакк:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) объекта кплайер.

Важно помнить, что [**вызов**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) вызывается из рабочего потока, а не из потока приложения. Поэтому реализация **вызова** должна быть потокобезопасной. Одним из подходов является защита данных элемента с помощью критической секции. Однако `CPlayer` класс демонстрирует альтернативный подход:

1.  В методе [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) объект кплайер отправляет в приложение сообщение **о \_ \_ \_ событии проигрывателя приложения WM** . Параметр Message является указателем [**имфмедиаевент**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) .
2.  Приложение получает сообщение о **\_ \_ \_ событии проигрывателя приложения WM** .
3.  Приложение вызывает `CPlayer::HandleEvent` метод, передавая указатель [**имфмедиаевент**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) .
4.  `HandleEvent`Метод отвечает на событие.

В следующем коде показан метод [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) :


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



Метод [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) выполняет следующие действия:

1.  Вызовите метод [**имфмедиаевентженератор:: енджетевент**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) , чтобы получить событие. Этот метод возвращает указатель на интерфейс [**имфмедиаевент**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) .
2.  Вызовите метод [**имфмедиаевент:: GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype) , чтобы получить код события.
3.  Если код события — [месессионклосед](mesessionclosed.md), вызовите выполнить SetEvent, чтобы задать событие *m \_ хклосивент* . Причина этого шага описана в [шаге 7: завершение сеанса мультимедиа](step-7--shut-down-the-media-session.md), а также в комментариях к коду.
4.  Для всех других кодов событий вызовите метод [**имфмедиаевентженератор:: бегинжетевент**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) , чтобы запросить следующее событие.
5.  Опубликуйте в окне сообщение о **\_ \_ \_ событии проигрывателя приложения WM** .

В следующем коде показан метод Хандливент, который вызывается, когда приложение получает сообщение о **\_ \_ \_ событии проигрывателя приложения WM** :


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



Этот метод вызывает [**имфмедиаевент:: GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype) , чтобы получить тип события и [**Имфмедиаевент:: Status**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) , чтобы получить успешный код ошибки, связанный с событием. Следующее выполняемое действие зависит от кода события.

## <a name="mesessiontopologystatus"></a>месессионтопологистатус

Событие [месессионтопологистатус](mesessiontopologystatus.md) сигнализирует об изменении состояния топологии. Атрибут [**\_ \_ \_ состояния топологии событий MF**](mf-event-topology-status-attribute.md) объекта события содержит состояние. В этом примере единственное интересующее вас значение — **MF \_ топостатус \_ Ready**, что означает, что воспроизведение готово к запуску.


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



`CPlayer::StartPlayback`Метод показан на [шаге 6. Управление воспроизведением](step-6--control-playback.md).

В этом примере также вызывается [**мфжетсервице**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) для получения интерфейса [**имфвидеодисплайконтрол**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) из [расширенного модуля подготовки видео](enhanced-video-renderer.md) (Евр). Этот интерфейс необходим для выполнения перерисовки и изменения размера окна видео, также показанного в [шаге 6: Управление воспроизведением](step-6--control-playback.md).

## <a name="meendofpresentation"></a>миндофпресентатион

Событие [миндофпресентатион](meendofpresentation.md) сигнализирует, что воспроизведение достигло конца файла. Сеанс мультимедиа автоматически переключается обратно в остановленное состояние.


```C++
//  Handler for MEEndOfPresentation event.
HRESULT CPlayer::OnPresentationEnded(IMFMediaEvent *pEvent)
{
    // The session puts itself into the stopped state automatically.
    m_state = Stopped;
    return S_OK;
}
```



## <a name="menewpresentation"></a>меневпресентатион

Событие [меневпресентатион](menewpresentation.md) сигнализирует о начале новой презентации. Данные события являются [**имфпресентатиондескриптор**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) указателем для новой презентации.

Во многих случаях это событие не будет появляться вообще. В этом случае используйте указатель [**имфпресентатиондескриптор**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) для создания новой топологии воспроизведения, как показано на [шаге 3. Открытие файла мультимедиа](step-3--open-a-media-file.md). Затем помещает новую топологию в очередь в сеансе мультимедиа.


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



Далее: [Шаг 6. Управление воспроизведением](step-6--control-playback.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Воспроизведение звука/видео](audio-video-playback.md)
</dt> <dt>

[Воспроизведение мультимедийных файлов с помощью Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



