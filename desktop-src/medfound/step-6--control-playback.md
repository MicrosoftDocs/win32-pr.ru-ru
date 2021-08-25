---
description: В этом разделе приведен шаг 6 руководства по воспроизведению мультимедийных файлов с помощью Media Foundation.
ms.assetid: e2e3e95b-41b2-45fb-b495-0e700220e5f5
title: Шаг 6. Управление воспроизведением
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eef0aa18f671c994837ba195cddba38976c3ffba990eb95748d2bede09141317
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887264"
---
# <a name="step-6-control-playback"></a>Шаг 6. Управление воспроизведением

В этом разделе приведен шаг 6 руководства по [воспроизведению мультимедийных файлов с помощью Media Foundation](how-to-play-unprotected-media-files.md). Полный код показан в разделе [Пример воспроизведения сеанса мультимедиа](media-session-playback-example.md).

Этот раздел состоит из следующих подразделов.

-   [Запуск воспроизведения](#starting-playback)
-   [Приостановка воспроизведения](#pausing-playback)
-   [Остановка воспроизведения](#stopping-playback)
-   [Перерисовка окна видео](#repainting-the-video-window)
-   [Изменение размера окна видео](#resizing-the-video-window)
-   [Связанные темы](#related-topics)

## <a name="starting-playback"></a>Запуск воспроизведения

Чтобы запустить воспроизведение, вызовите [**имфмедиасессион:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start). В следующем коде показано, как начать с текущей позицией воспроизведения.


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



Метод [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) также может указывать начальную точку относительно начала файла; Дополнительные сведения см. в разделе Справочник по API.

## <a name="pausing-playback"></a>Приостановка воспроизведения

Чтобы приостановить воспроизведение, вызовите [**имфмедиасессион::P Аусе**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause).


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



## <a name="stopping-playback"></a>Остановка воспроизведения

Чтобы прерывать воспроизведение, вызовите [**имфмедиасессион:: останавливаться**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop). Когда воспроизведение останавливается, видеоизображение удаляется, а видеоокно закрашивается цветом фона (по умолчанию черный).


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



## <a name="repainting-the-video-window"></a>Перерисовка окна видео

[Расширенный обработчик видео](enhanced-video-renderer.md) (Евр) рисует видео в окне, заданном приложением. Это происходит в отдельном потоке, и в большинстве случаев приложению не требуется управлять этим процессом. Однако если воспроизведение приостановлено или остановлено, ЕВР должно получать уведомления всякий раз, когда видеоокно получает сообщение [**WM \_ Paint**](../gdi/wm-paint.md) . Это позволяет Евр перерисовывать окно. Чтобы уведомить евр, вызовите метод [**имфвидеодисплайконтрол:: репаинтвидео**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo) :


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



В следующем коде показан обработчик для сообщения [**WM \_ Paint**](../gdi/wm-paint.md) . Эта функция должна вызываться из цикла сообщений приложения.


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



`HasVideo`Метод возвращает **значение true** , если у `CPlayer` объекта есть допустимый указатель [**имфвидеодисплайконтрол**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) . (См. [Шаг 1. объявление класса кплайер](step-1--declare-the-cplayer-class.md).)


```C++
    BOOL          HasVideo() const { return (m_pVideoDisplay != NULL);  }
```



## <a name="resizing-the-video-window"></a>Изменение размера окна видео

При изменении размера окна видео обновите прямоугольник назначения в евр, вызвав метод [**имфвидеодисплайконтрол:: сетвидеопоситион**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) :


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



Далее: [Шаг 7. Завершение сеанса мультимедиа](step-7--shut-down-the-media-session.md)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Воспроизведение звука/видео](audio-video-playback.md)
</dt> <dt>

[Воспроизведение мультимедийных файлов с помощью Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 
