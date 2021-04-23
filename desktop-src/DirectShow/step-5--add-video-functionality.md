---
description: В этом разделе описывается шаг 5 руководства воспроизведение аудио-и видеороликов в DirectShow.
ms.assetid: 9d7a40e0-4327-4ca3-b430-2be02f80c16f
title: Шаг 5. Добавление функции видео
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f5ccf1ae3ca24a705506bc41620ac53a13d7e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265961"
---
# <a name="step-5-add-video-functionality"></a><span data-ttu-id="9b542-103">Шаг 5. Добавление функции видео</span><span class="sxs-lookup"><span data-stu-id="9b542-103">Step 5: Add Video Functionality</span></span>

<span data-ttu-id="9b542-104">В этом разделе описывается шаг 5 руководства [Воспроизведение аудио-и видеороликов в DirectShow](audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="9b542-104">This topic is step 5 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="9b542-105">Полный код приведен в разделе [Пример воспроизведения DirectShow](directshow-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="9b542-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="9b542-106">Чтобы убедиться, что видео отображается правильно, приложение должно реагировать на сообщения [**WM \_ Paint**](../gdi/wm-paint.md), [**WM \_ size**](../winmsg/wm-size.md)и [**WM \_ дисплайчанже**](../gdi/wm-displaychange.md) следующим образом.</span><span class="sxs-lookup"><span data-stu-id="9b542-106">To ensure that video displays correctly, the application must respond to [**WM\_PAINT**](../gdi/wm-paint.md), [**WM\_SIZE**](../winmsg/wm-size.md), and [**WM\_DISPLAYCHANGE**](../gdi/wm-displaychange.md) messages as follows.</span></span>

### <a name="handle-wm_paint-messages"></a><span data-ttu-id="9b542-107">Обрабатывать \_ сообщения WM Paint</span><span class="sxs-lookup"><span data-stu-id="9b542-107">Handle WM\_PAINT Messages</span></span>

<span data-ttu-id="9b542-108">Когда приложение получает сообщение [**WM \_ Paint**](../gdi/wm-paint.md) , модулю обработки видео может потребоваться перерисовать последний кадр видео.</span><span class="sxs-lookup"><span data-stu-id="9b542-108">When the application receives a [**WM\_PAINT**](../gdi/wm-paint.md) message, the video renderer might need to redraw the last video frame.</span></span> <span data-ttu-id="9b542-109">Для фильтра [**расширенного обработчика видео**](enhanced-video-renderer-filter.md) (Евр) вызовите [**Имфвидеодисплайконтрол:: репаинтвидео**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).</span><span class="sxs-lookup"><span data-stu-id="9b542-109">For the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) filter, call [**IMFVideoDisplayControl::RepaintVideo**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).</span></span>


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



<span data-ttu-id="9b542-110">Для модуля [подготовки видео с фильтром 9](video-mixing-renderer-filter-9.md) (VMR-9) вызовите [**IVMRWindowlessControl9:: репаинтвидео**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo).</span><span class="sxs-lookup"><span data-stu-id="9b542-110">For the [Video Mixing Renderer Filter 9](video-mixing-renderer-filter-9.md) (VMR-9), call [**IVMRWindowlessControl9::RepaintVideo**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-repaintvideo).</span></span>


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



<span data-ttu-id="9b542-111">Для [фильтра модуля подготовки видео "Микширование 7](video-mixing-renderer-filter-7.md) " (VMR-7) вызовите [**Ивмрвиндовлессконтрол:: репаинтвидео**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo).</span><span class="sxs-lookup"><span data-stu-id="9b542-111">For the [Video Mixing Renderer Filter 7](video-mixing-renderer-filter-7.md) (VMR-7), call [**IVMRWindowlessControl::RepaintVideo**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-repaintvideo).</span></span>


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



### <a name="handle-wm_size-messages"></a><span data-ttu-id="9b542-112">Обрабатывает \_ сообщения размером WM</span><span class="sxs-lookup"><span data-stu-id="9b542-112">Handle WM\_SIZE Messages</span></span>

<span data-ttu-id="9b542-113">Если размер окна видео меняется, уведомляет модуль подготовки видео о необходимости изменения размера видео.</span><span class="sxs-lookup"><span data-stu-id="9b542-113">If the size of the video window changes, notify the video renderer to resize the video.</span></span> <span data-ttu-id="9b542-114">Для Евр вызовите [**имфвидеодисплайконтрол:: сетвидеопоситион**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span><span class="sxs-lookup"><span data-stu-id="9b542-114">For the EVR, call [**IMFVideoDisplayControl::SetVideoPosition**](/windows/win32/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span></span>


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



<span data-ttu-id="9b542-115">Для VMR-9 вызовите [**IVMRWindowlessControl9:: сетвидеопоситион**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition).</span><span class="sxs-lookup"><span data-stu-id="9b542-115">For the VMR-9, call [**IVMRWindowlessControl9::SetVideoPosition**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-setvideoposition).</span></span>


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



<span data-ttu-id="9b542-116">Для VMR-7 вызовите [**ивмрвиндовлессконтрол:: сетвидеопоситион**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition).</span><span class="sxs-lookup"><span data-stu-id="9b542-116">For the VMR-7, call [**IVMRWindowlessControl::SetVideoPosition**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-setvideoposition).</span></span>


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



### <a name="handle-wm_displaychange-messages"></a><span data-ttu-id="9b542-117">Работа с \_ сообщениями WM дисплайчанже</span><span class="sxs-lookup"><span data-stu-id="9b542-117">Handle WM\_DISPLAYCHANGE Messages</span></span>

<span data-ttu-id="9b542-118">При изменении режима просмотра необходимо уведомить фильтр VMR-9 или VMR-7.</span><span class="sxs-lookup"><span data-stu-id="9b542-118">If the display mode changes, you must notify the VMR-9 or VMR-7 filter.</span></span> <span data-ttu-id="9b542-119">Для VMR-9 вызовите [**IVMRWindowlessControl9::D исплаймодечанжед**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged).</span><span class="sxs-lookup"><span data-stu-id="9b542-119">For the VMR-9, call [**IVMRWindowlessControl9::DisplayModeChanged**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrwindowlesscontrol9-displaymodechanged).</span></span>


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



<span data-ttu-id="9b542-120">Для VMR-7 вызовите [**ивмрвиндовлессконтрол::D исплаймодечанжед**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).</span><span class="sxs-lookup"><span data-stu-id="9b542-120">For the VMR-7, call [**IVMRWindowlessControl::DisplayModeChanged**](/windows/desktop/api/Strmif/nf-strmif-ivmrwindowlesscontrol-displaymodechanged).</span></span>


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



<span data-ttu-id="9b542-121">Евр не требует уведомления при изменении режима экрана.</span><span class="sxs-lookup"><span data-stu-id="9b542-121">The EVR does not need to be notified when the display mode changes.</span></span>

<span data-ttu-id="9b542-122">Далее: [Шаг 6. Работа с событиями графа](step-6--handle-graph-events.md).</span><span class="sxs-lookup"><span data-stu-id="9b542-122">Next: [Step 6: Handle Graph Events](step-6--handle-graph-events.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b542-123">См. также</span><span class="sxs-lookup"><span data-stu-id="9b542-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b542-124">Воспроизведение звука и видео в DirectShow</span><span class="sxs-lookup"><span data-stu-id="9b542-124">Audio/Video Playback in DirectShow</span></span>](audio-video-playback-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="9b542-125">Пример воспроизведения DirectShow</span><span class="sxs-lookup"><span data-stu-id="9b542-125">DirectShow Playback Example</span></span>](directshow-playback-example.md)
</dt> <dt>

[<span data-ttu-id="9b542-126">Использование фильтра Евр DirectShow</span><span class="sxs-lookup"><span data-stu-id="9b542-126">Using the DirectShow EVR Filter</span></span>](../medfound/using-the-directshow-evr-filter.md)
</dt> <dt>

[<span data-ttu-id="9b542-127">Использование модуля подготовки видео для микширования</span><span class="sxs-lookup"><span data-stu-id="9b542-127">Using the Video Mixing Renderer</span></span>](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 
