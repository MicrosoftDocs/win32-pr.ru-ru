---
description: В этом разделе приводится шаг 7 из руководства воспроизведение мультимедийных файлов с помощью Media Foundation.
ms.assetid: c31444df-8717-4ca8-a9ec-72cbb0ee4125
title: Шаг 7. Завершение сеанса мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae9fd11cde51b06d932b212f4effabf315deecb7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104157034"
---
# <a name="step-7-shut-down-the-media-session"></a><span data-ttu-id="ff4ca-103">Шаг 7. Завершение сеанса мультимедиа</span><span class="sxs-lookup"><span data-stu-id="ff4ca-103">Step 7: Shut Down the Media Session</span></span>

<span data-ttu-id="ff4ca-104">В этом разделе приводится шаг 7 из руководства [Воспроизведение мультимедийных файлов с помощью Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="ff4ca-104">This topic is step 7 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="ff4ca-105">Полный код показан в разделе [Пример воспроизведения сеанса мультимедиа](media-session-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="ff4ca-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="ff4ca-106">Чтобы завершить [сеанс мультимедиа](media-session.md), выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="ff4ca-106">To shut down the [Media Session](media-session.md), perform the following steps:</span></span>

1.  <span data-ttu-id="ff4ca-107">Вызовите метод [**имфмедиасессион:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) , чтобы закрыть текущую презентацию.</span><span class="sxs-lookup"><span data-stu-id="ff4ca-107">Call [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) to close the current presentation.</span></span>
2.  <span data-ttu-id="ff4ca-108">Дождитесь события [месессионклосед](mesessionclosed.md) .</span><span class="sxs-lookup"><span data-stu-id="ff4ca-108">Wait for the [MESessionClosed](mesessionclosed.md) event.</span></span> <span data-ttu-id="ff4ca-109">Это событие гарантированно является последним событием из сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ff4ca-109">This event is guaranteed to be the last event from the Media Session.</span></span>
3.  <span data-ttu-id="ff4ca-110">Вызов [**имфмедиасессион:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span><span class="sxs-lookup"><span data-stu-id="ff4ca-110">Call [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span></span> <span data-ttu-id="ff4ca-111">Этот метод заставляет сеансы мультимедиа освобождать ресурсы.</span><span class="sxs-lookup"><span data-stu-id="ff4ca-111">This method causes the Media Sessions to release resources.</span></span>
4.  <span data-ttu-id="ff4ca-112">Вызовите [**имфмедиасаурце:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) в текущем источнике мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ff4ca-112">Call [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) on the current media source.</span></span>

<span data-ttu-id="ff4ca-113">Следующий метод завершает сеанс мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ff4ca-113">The following method shuts down the Media Session.</span></span> <span data-ttu-id="ff4ca-114">Для ожидания события [месессионклосед](mesessionclosed.md) используется обработчик событий (*m \_ хклосивент*).</span><span class="sxs-lookup"><span data-stu-id="ff4ca-114">It uses an event handle (*m\_hCloseEvent*) to wait for the [MESessionClosed](mesessionclosed.md) event.</span></span> <span data-ttu-id="ff4ca-115">См. [Шаг 5. Работа с событиями сеанса мультимедиа](step-5--handle-media-session-events.md).</span><span class="sxs-lookup"><span data-stu-id="ff4ca-115">See [Step 5: Handle Media Session Events](step-5--handle-media-session-events.md).</span></span>


```C++
//  Close the media session. 
HRESULT CPlayer::CloseSession()
{
    //  The IMFMediaSession::Close method is asynchronous, but the 
    //  CPlayer::CloseSession method waits on the MESessionClosed event.
    //  
    //  MESessionClosed is guaranteed to be the last event that the 
    //  media session fires.

    HRESULT hr = S_OK;

    SafeRelease(&m_pVideoDisplay);

    // First close the media session.
    if (m_pSession)
    {
        DWORD dwWaitResult = 0;

        m_state = Closing;
           
        hr = m_pSession->Close();
        // Wait for the close operation to complete
        if (SUCCEEDED(hr))
        {
            dwWaitResult = WaitForSingleObject(m_hCloseEvent, 5000);
            if (dwWaitResult == WAIT_TIMEOUT)
            {
                assert(FALSE);
            }
            // Now there will be no more events from this session.
        }
    }

    // Complete shutdown operations.
    if (SUCCEEDED(hr))
    {
        // Shut down the media source. (Synchronous operation, no events.)
        if (m_pSource)
        {
            (void)m_pSource->Shutdown();
        }
        // Shut down the media session. (Synchronous operation, no events.)
        if (m_pSession)
        {
            (void)m_pSession->Shutdown();
        }
    }

    SafeRelease(&m_pSource);
    SafeRelease(&m_pSession);
    m_state = Closed;
    return hr;
}
```



<span data-ttu-id="ff4ca-116">Перед завершением работы приложения завершите сеанс мультимедиа, а затем вызовите [**мфшутдовн**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) , чтобы завершить работу платформы Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="ff4ca-116">Before the application exits, shut down the Media Session, and then call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) to shut down the Microsoft Media Foundation platform.</span></span>


```C++
//  Release all resources held by this object.
HRESULT CPlayer::Shutdown()
{
    // Close the session
    HRESULT hr = CloseSession();

    // Shutdown the Media Foundation platform
    MFShutdown();

    if (m_hCloseEvent)
    {
        CloseHandle(m_hCloseEvent);
        m_hCloseEvent = NULL;
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="ff4ca-117">См. также</span><span class="sxs-lookup"><span data-stu-id="ff4ca-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff4ca-118">Воспроизведение звука/видео</span><span class="sxs-lookup"><span data-stu-id="ff4ca-118">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="ff4ca-119">Воспроизведение мультимедийных файлов с помощью Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ff4ca-119">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



