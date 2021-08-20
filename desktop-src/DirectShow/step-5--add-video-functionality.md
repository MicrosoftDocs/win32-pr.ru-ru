---
description: В этом разделе приводится шаг 5 руководства воспроизведение аудио-и видеороликов в DirectShow.
ms.assetid: 9d7a40e0-4327-4ca3-b430-2be02f80c16f
title: Шаг 5. Добавление функции видео
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 968c35916f90f226305eb987058d14cc7891d250961e2b8a41a1756ec3794b1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951783"
---
# <a name="step-5-add-video-functionality"></a>Шаг 5. Добавление функции видео

В этом разделе приводится шаг 5 руководства [Воспроизведение аудио-и видеороликов в DirectShow](audio-video-playback-in-directshow.md). полный код приведен в разделе [пример воспроизведения DirectShow](directshow-playback-example.md).

Чтобы убедиться, что видео отображается правильно, приложение должно реагировать на сообщения [**WM \_ Paint**](../gdi/wm-paint.md), [**WM \_ size**](../winmsg/wm-size.md)и [**WM \_ дисплайчанже**](../gdi/wm-displaychange.md) следующим образом.

### <a name="handle-wm_paint-messages"></a>Обрабатывать \_ сообщения WM Paint

Когда приложение получает сообщение [**WM \_ Paint**](../gdi/wm-paint.md) , модулю обработки видео может потребоваться перерисовать последний кадр видео. Для фильтра [**расширенного обработчика видео**](enhanced-video-renderer-filter.md) (Евр) вызовите [**Имфвидеодисплайконтрол:: репаинтвидео**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).


```C++
HRESULT CEVR::Repaint(HWND hwnd, HDC hdc)
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



Для модуля [подготовки видео с фильтром 9](video-mixing-renderer-filter-9.md) (VMR-9) вызовите [**IVMRWindowlessControl9:: репаинтвидео**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo).


```C++
HRESULT CVMR9::Repaint(HWND hwnd, HDC hdc)
{
    if (m_pWindowless)
    {
        return m_pWindowless->RepaintVideo(hwnd, hdc);
    }
    else
    {
        return S_OK;
    }
}
```



Для [фильтра модуля подготовки видео "Микширование 7](video-mixing-renderer-filter-7.md) " (VMR-7) вызовите [**Ивмрвиндовлессконтрол:: репаинтвидео**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo).


```C++
HRESULT CVMR7::Repaint(HWND hwnd, HDC hdc)
{
    if (m_pWindowless)
    {
        return m_pWindowless->RepaintVideo(hwnd, hdc);
    }
    else
    {
        return S_OK;
    }
}
```



### <a name="handle-wm_size-messages"></a>Обрабатывает \_ сообщения размером WM

Если размер окна видео меняется, уведомляет модуль подготовки видео о необходимости изменения размера видео. Для Евр вызовите [**имфвидеодисплайконтрол:: сетвидеопоситион**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).


```C++
HRESULT CEVR::UpdateVideoWindow(HWND hwnd, const LPRECT prc)
{
    if (m_pVideoDisplay == NULL)
    {
        return S_OK; // no-op
    }

    if (prc)
    {
        return m_pVideoDisplay->SetVideoPosition(NULL, prc);
    }
    else
    {

        RECT rc;
        GetClientRect(hwnd, &rc);
        return m_pVideoDisplay->SetVideoPosition(NULL, &rc);
    }
}
```



Для VMR-9 вызовите [**IVMRWindowlessControl9:: сетвидеопоситион**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition).


```C++
HRESULT CVMR9::UpdateVideoWindow(HWND hwnd, const LPRECT prc)
{
    if (m_pWindowless == NULL)
    {
        return S_OK; // no-op
    }

    if (prc)
    {
        return m_pWindowless->SetVideoPosition(NULL, prc);
    }
    else
    {

        RECT rc;
        GetClientRect(hwnd, &rc);
        return m_pWindowless->SetVideoPosition(NULL, &rc);
    }
}
```



Для VMR-7 вызовите [**ивмрвиндовлессконтрол:: сетвидеопоситион**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition).


```C++
HRESULT CVMR7::UpdateVideoWindow(HWND hwnd, const LPRECT prc)
{
    if (m_pWindowless == NULL)
    {
        return S_OK; // no-op
    }

    if (prc)
    {
        return m_pWindowless->SetVideoPosition(NULL, prc);
    }
    else
    {
        RECT rc;
        GetClientRect(hwnd, &rc);
        return m_pWindowless->SetVideoPosition(NULL, &rc);
    }
}
```



### <a name="handle-wm_displaychange-messages"></a>Работа с \_ сообщениями WM дисплайчанже

При изменении режима просмотра необходимо уведомить фильтр VMR-9 или VMR-7. Для VMR-9 вызовите [**IVMRWindowlessControl9::D исплаймодечанжед**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged).


```C++
HRESULT CVMR9::DisplayModeChanged()
{
    if (m_pWindowless)
    {
        return m_pWindowless->DisplayModeChanged();
    }
    else
    {
        return S_OK;
    }
}
```



Для VMR-7 вызовите [**ивмрвиндовлессконтрол::D исплаймодечанжед**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).


```C++
HRESULT CVMR7::DisplayModeChanged()
{
    if (m_pWindowless)
    {
        return m_pWindowless->DisplayModeChanged();
    }
    else
    {
        return S_OK;
    }
}
```



Евр не требует уведомления при изменении режима экрана.

далее: [шаг 6. обработайте события Graph](step-6--handle-graph-events.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Воспроизведение звука и видео в DirectShow](audio-video-playback-in-directshow.md)
</dt> <dt>

[DirectShow Пример воспроизведения](directshow-playback-example.md)
</dt> <dt>

[использование DirectShow фильтра евр](../medfound/using-the-directshow-evr-filter.md)
</dt> <dt>

[Использование модуля подготовки видео для микширования](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 
