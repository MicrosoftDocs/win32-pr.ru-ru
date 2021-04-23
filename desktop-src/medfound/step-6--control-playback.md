---
description: В этом разделе приведен шаг 6 руководства по воспроизведению мультимедийных файлов с помощью Media Foundation.
ms.assetid: e2e3e95b-41b2-45fb-b495-0e700220e5f5
title: Шаг 6. Управление воспроизведением
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfdfecea3484ac6b06cc44e23fd3bd1b3235324e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898178"
---
# <a name="step-6-control-playback"></a><span data-ttu-id="ac520-103">Шаг 6. Управление воспроизведением</span><span class="sxs-lookup"><span data-stu-id="ac520-103">Step 6: Control Playback</span></span>

<span data-ttu-id="ac520-104">В этом разделе приведен шаг 6 руководства по [воспроизведению мультимедийных файлов с помощью Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="ac520-104">This topic is step 6 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="ac520-105">Полный код показан в разделе [Пример воспроизведения сеанса мультимедиа](media-session-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="ac520-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="ac520-106">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="ac520-106">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="ac520-107">Запуск воспроизведения</span><span class="sxs-lookup"><span data-stu-id="ac520-107">Starting Playback</span></span>](#starting-playback)
-   [<span data-ttu-id="ac520-108">Приостановка воспроизведения</span><span class="sxs-lookup"><span data-stu-id="ac520-108">Pausing Playback</span></span>](#pausing-playback)
-   [<span data-ttu-id="ac520-109">Остановка воспроизведения</span><span class="sxs-lookup"><span data-stu-id="ac520-109">Stopping Playback</span></span>](#stopping-playback)
-   [<span data-ttu-id="ac520-110">Перерисовка окна видео</span><span class="sxs-lookup"><span data-stu-id="ac520-110">Repainting the Video Window</span></span>](#repainting-the-video-window)
-   [<span data-ttu-id="ac520-111">Изменение размера окна видео</span><span class="sxs-lookup"><span data-stu-id="ac520-111">Resizing the Video Window</span></span>](#resizing-the-video-window)
-   [<span data-ttu-id="ac520-112">См. также</span><span class="sxs-lookup"><span data-stu-id="ac520-112">Related topics</span></span>](#related-topics)

## <a name="starting-playback"></a><span data-ttu-id="ac520-113">Запуск воспроизведения</span><span class="sxs-lookup"><span data-stu-id="ac520-113">Starting Playback</span></span>

<span data-ttu-id="ac520-114">Чтобы запустить воспроизведение, вызовите [**имфмедиасессион:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span><span class="sxs-lookup"><span data-stu-id="ac520-114">To start playback, call [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span></span> <span data-ttu-id="ac520-115">В следующем коде показано, как начать с текущей позицией воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="ac520-115">The following code shows how to start from the current playback position.</span></span>


```C++
//  Start playback from the current position. 
HRESULT CPlayer::StartPlayback()
{
    assert(m_pSession != NULL);

    PROPVARIANT varStart;
    PropVariantInit(&varStart);

    HRESULT hr = m_pSession->Start(&GUID_NULL, &varStart);
    if (SUCCEEDED(hr))
    {
        // Note: Start is an asynchronous operation. However, we
        // can treat our state as being already started. If Start
        // fails later, we'll get an MESessionStarted event with
        // an error code, and we will update our state then.
        m_state = Started;
    }
    PropVariantClear(&varStart);
    return hr;
}

//  Start playback from paused or stopped.
HRESULT CPlayer::Play()
{
    if (m_state != Paused && m_state != Stopped)
    {
        return MF_E_INVALIDREQUEST;
    }
    if (m_pSession == NULL || m_pSource == NULL)
    {
        return E_UNEXPECTED;
    }
    return StartPlayback();
}

```



<span data-ttu-id="ac520-116">Метод [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) также может указывать начальную точку относительно начала файла; Дополнительные сведения см. в разделе Справочник по API.</span><span class="sxs-lookup"><span data-stu-id="ac520-116">The [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) method can also specify a starting position relative to the start of the file; see the API reference topic for more information.</span></span>

## <a name="pausing-playback"></a><span data-ttu-id="ac520-117">Приостановка воспроизведения</span><span class="sxs-lookup"><span data-stu-id="ac520-117">Pausing Playback</span></span>

<span data-ttu-id="ac520-118">Чтобы приостановить воспроизведение, вызовите [**имфмедиасессион::P Аусе**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause).</span><span class="sxs-lookup"><span data-stu-id="ac520-118">To pause playback, call [**IMFMediaSession::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause).</span></span>


```C++
//  Pause playback.
HRESULT CPlayer::Pause()    
{
    if (m_state != Started)
    {
        return MF_E_INVALIDREQUEST;
    }
    if (m_pSession == NULL || m_pSource == NULL)
    {
        return E_UNEXPECTED;
    }

    HRESULT hr = m_pSession->Pause();
    if (SUCCEEDED(hr))
    {
        m_state = Paused;
    }

    return hr;
}
```



## <a name="stopping-playback"></a><span data-ttu-id="ac520-119">Остановка воспроизведения</span><span class="sxs-lookup"><span data-stu-id="ac520-119">Stopping Playback</span></span>

<span data-ttu-id="ac520-120">Чтобы прерывать воспроизведение, вызовите [**имфмедиасессион:: останавливаться**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).</span><span class="sxs-lookup"><span data-stu-id="ac520-120">To stop playback, call [**IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).</span></span> <span data-ttu-id="ac520-121">Когда воспроизведение останавливается, видеоизображение удаляется, а видеоокно закрашивается цветом фона (по умолчанию черный).</span><span class="sxs-lookup"><span data-stu-id="ac520-121">While playback is stopped, the video image is cleared and the video window is painted with the background color (black by default).</span></span>


```C++
// Stop playback.
HRESULT CPlayer::Stop()
{
    if (m_state != Started && m_state != Paused)
    {
        return MF_E_INVALIDREQUEST;
    }
    if (m_pSession == NULL)
    {
        return E_UNEXPECTED;
    }

    HRESULT hr = m_pSession->Stop();
    if (SUCCEEDED(hr))
    {
        m_state = Stopped;
    }
    return hr;
}
```



## <a name="repainting-the-video-window"></a><span data-ttu-id="ac520-122">Перерисовка окна видео</span><span class="sxs-lookup"><span data-stu-id="ac520-122">Repainting the Video Window</span></span>

<span data-ttu-id="ac520-123">[Расширенный обработчик видео](enhanced-video-renderer.md) (Евр) рисует видео в окне, заданном приложением.</span><span class="sxs-lookup"><span data-stu-id="ac520-123">The [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR) draws the video in the window specified by the application.</span></span> <span data-ttu-id="ac520-124">Это происходит в отдельном потоке, и в большинстве случаев приложению не требуется управлять этим процессом.</span><span class="sxs-lookup"><span data-stu-id="ac520-124">This occurs on a separate thread, and for the most part, your application does not need to manage this process.</span></span> <span data-ttu-id="ac520-125">Однако если воспроизведение приостановлено или остановлено, ЕВР должно получать уведомления всякий раз, когда видеоокно получает сообщение [**WM \_ Paint**](../gdi/wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="ac520-125">If playback is paused or stopped, however, the EVR must be notified whenever the video window receives a [**WM\_PAINT**](../gdi/wm-paint.md) message.</span></span> <span data-ttu-id="ac520-126">Это позволяет Евр перерисовывать окно.</span><span class="sxs-lookup"><span data-stu-id="ac520-126">This allows the EVR to repaint the window.</span></span> <span data-ttu-id="ac520-127">Чтобы уведомить евр, вызовите метод [**имфвидеодисплайконтрол:: репаинтвидео**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo) :</span><span class="sxs-lookup"><span data-stu-id="ac520-127">To notify the EVR, call the [**IMFVideoDisplayControl::RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo) method:</span></span>


```C++
//  Repaint the video window. Call this method on WM_PAINT.

HRESULT CPlayer::Repaint()
{
    if (m_pVideoDisplay)
    {
        return m_pVideoDisplay->RepaintVideo();
    }
    else
    {
        return S_OK;
    }
}
```



<span data-ttu-id="ac520-128">В следующем коде показан обработчик для сообщения [**WM \_ Paint**](../gdi/wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="ac520-128">The following code shows the handler for the [**WM\_PAINT**](../gdi/wm-paint.md) message.</span></span> <span data-ttu-id="ac520-129">Эта функция должна вызываться из цикла сообщений приложения.</span><span class="sxs-lookup"><span data-stu-id="ac520-129">This function should be called from the application's message loop.</span></span>


```C++
//  Handler for WM_PAINT messages.
void OnPaint(HWND hwnd)
{
    PAINTSTRUCT ps;
    HDC hdc = BeginPaint(hwnd, &ps);

    if (g_pPlayer && g_pPlayer->HasVideo())
    {
        // Video is playing. Ask the player to repaint.
        g_pPlayer->Repaint();
    }
    else
    {
        // The video is not playing, so we must paint the application window.
        RECT rc;
        GetClientRect(hwnd, &rc);
        FillRect(hdc, &rc, (HBRUSH) COLOR_WINDOW);
    }
    EndPaint(hwnd, &ps);
}
```



<span data-ttu-id="ac520-130">`HasVideo`Метод возвращает **значение true** , если у `CPlayer` объекта есть допустимый указатель [**имфвидеодисплайконтрол**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) .</span><span class="sxs-lookup"><span data-stu-id="ac520-130">The `HasVideo` method returns **TRUE** if the `CPlayer` object has a valid [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) pointer.</span></span> <span data-ttu-id="ac520-131">(См. [Шаг 1. объявление класса кплайер](step-1--declare-the-cplayer-class.md).)</span><span class="sxs-lookup"><span data-stu-id="ac520-131">(See [Step 1: Declare the CPlayer Class](step-1--declare-the-cplayer-class.md).)</span></span>


```C++
    BOOL          HasVideo() const { return (m_pVideoDisplay != NULL);  }
```



## <a name="resizing-the-video-window"></a><span data-ttu-id="ac520-132">Изменение размера окна видео</span><span class="sxs-lookup"><span data-stu-id="ac520-132">Resizing the Video Window</span></span>

<span data-ttu-id="ac520-133">При изменении размера окна видео обновите прямоугольник назначения в евр, вызвав метод [**имфвидеодисплайконтрол:: сетвидеопоситион**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) :</span><span class="sxs-lookup"><span data-stu-id="ac520-133">If you resize the video window, update the destination rectangle on the EVR by calling the [**IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) method:</span></span>


```C++
//  Resize the video rectangle.
//
//  Call this method if the size of the video window changes.

HRESULT CPlayer::ResizeVideo(WORD width, WORD height)
{
    if (m_pVideoDisplay)
    {
        // Set the destination rectangle.
        // Leave the default source rectangle (0,0,1,1).

        RECT rcDest = { 0, 0, width, height };

        return m_pVideoDisplay->SetVideoPosition(NULL, &rcDest);
    }
    else
    {
        return S_OK;
    }
}
```



<span data-ttu-id="ac520-134">Далее: [Шаг 7. Завершение сеанса мультимедиа](step-7--shut-down-the-media-session.md)</span><span class="sxs-lookup"><span data-stu-id="ac520-134">Next: [Step 7: Shut Down the Media Session](step-7--shut-down-the-media-session.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="ac520-135">См. также</span><span class="sxs-lookup"><span data-stu-id="ac520-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac520-136">Воспроизведение звука/видео</span><span class="sxs-lookup"><span data-stu-id="ac520-136">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="ac520-137">Воспроизведение мультимедийных файлов с помощью Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ac520-137">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 
