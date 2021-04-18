---
description: Реализация панели поиска
ms.assetid: 384f0732-e0c5-4b1f-b590-195e0acf90e1
title: Реализация панели поиска
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd3f2440c011267c792c79c8bc3550926c5767f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537811"
---
# <a name="implementing-a-seek-bar"></a>Реализация панели поиска

В этом разделе описывается, как реализовать панель поиска для приложения мультимедиа-проигрывателя. Панель поиска реализуется как элемент управления TrackBar. Общие сведения о поиске в DirectShow см. в разделе [Поиск графа фильтра](seeking-the-filter-graph.md).

При запуске приложения инициализируйте значение TrackBar:


```C++
void InitSlider(HWND hwnd) 
{
    // Initialize the trackbar range, but disable the 
    // control until the user opens a file.
    hScroll = GetDlgItem(hwnd, IDC_SLIDER1);
    EnableWindow(hScroll, FALSE);
    SendMessage(hScroll, TBM_SETRANGE, TRUE, MAKELONG(0, 100));
}
```



Значение TrackBar отключается, пока пользователь не откроет файл мультимедиа. Диапазон TrackBar имеет значение от 0 до 100. Во время воспроизведения файла приложение вычисляет расположение воспроизведения в процентах от длительности файла и соответствующим образом обновляет TrackBar. Например, значение TrackBar "50" всегда соответствует середине файла.

Когда пользователь открывает файл, создайте граф воспроизведения файлов с помощью функции **RenderFile**. Код для этого показан в [процедуре воспроизведения файла](how-to-play-a-file.md). Затем выполните запрос к диспетчеру графа фильтров для интерфейса **имедиасикинг** и сохраните указатель интерфейса:


```C++
IMediaSeeking *g_pSeek = 0;
hr = pGraph->QueryInterface(IID_IMediaSeeking, (void**)&g_pSeek);
```



Чтобы определить, можно ли найти файл, вызовите метод [**имедиасикинг:: чекккапабилитиес**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) или метод [**Имедиасикинг:: Capabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) . Эти методы выполняются почти одинаково, но их семантика немного отличается. В следующем примере используется **чекккапабилитес**:


```C++
// Determine if the source is seekable.
BOOL  bCanSeek = FALSE;
DWORD caps = AM_SEEKING_CanSeekAbsolute | AM_SEEKING_CanGetDuration; 
bCanSeek = (S_OK == pSeek->CheckCapabilities(&caps));
if (bCanSeek)
{
    // Enable the trackbar.
    EnableWindow(hScroll, TRUE);

    // Find the file duration.
    pSeek->GetDuration(&g_rtTotalTime);
}
```



\_ \_ Флаг кансикабсолуте для поиска проверяет, доступен ли исходный файл, а флаг AM- \_ \_ канжетдуратион проверяет, можно ли заранее определить длительность файла. Если поддерживаются обе возможности, приложение включает параметр TrackBar и получает длительность файла.

Если граф доступен для поиска, приложение будет использовать таймер для обновления расположения TrackBar во время воспроизведения. При запуске графа фильтра для воспроизведения файла запустите событие таймера, вызвав одну из функций таймера Windows, например **сеттимер**. Дополнительные сведения о таймерах см. в разделе "таймеры" раздела Platform SDK.


```C++
void StartPlayback(HWND hwnd) 
{
    pControl->Run();
    if (bCanSeek)
    {
        StopTimer(); // Make sure an old timer is not still active.
        nTimerID = SetTimer(hwnd, IDT_TIMER1, TICK_FREQ, (TIMERPROC)NULL);
        if (nTimerID == 0)
        {
            /* Handle Error */
        }
    }
}

void StopTimer() 
{
    if (wTimerID != 0)
    {
        KillTimer(g_hwnd, wTimerID);
        wTimerID = 0;
    }
}
```



Используйте событие Timer для обновления расположения TrackBar. Вызовите [**имедиасикинг:: жеткуррентпоситион**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) , чтобы получить расположение воспроизведения куррант, а затем Вычислите значение в процентах от длительности файла:


```C++
case WM_TIMER:
    if (wParam == IDT_TIMER1)
    {
        // Timer should not be running unless we really can seek.
        ASSERT(bCanSeek == TRUE);

        REFERENCE_TIME timeNow;
        if (SUCCEEDED(pSeek->GetCurrentPosition(&timeNow)))
        {
            long sliderTick = (long)((timeNow * 100) / g_rtTotalTime);
            SendMessage( hScroll, TBM_SETPOS, TRUE, sliderTick );
        }
    }
    break;
```



Пользователь также может перемещать ползунок для поиска файла. Когда пользователь перетаскивает или щелкает элемент управления TrackBar, приложение получает \_ событие WM HSCROLL. Младшее слово параметра *wParam* — это сообщение уведомления TrackBar. Например, ТБ \_ ендтракк отправляется в конце действия TrackBar, а ТБ \_ сумбтракк постоянно отправляется, пока пользователь перетаскивает TrackBar. В следующем коде показан один из способов управления \_ сообщением WM HSCROLL:


```C++
static OAFilterState state;
static BOOL bStartOfScroll = TRUE;

case WM_HSCROLL:
    short int userReq = LOWORD(wParam);
    if (userReq == TB_ENDTRACK || userReq == TB_THUMBTRACK)
    {
        DWORD dwPosition  = SendMessage(hTrackbar, TBM_GETPOS, 0, 0);
        // Pause when the scroll action begins.
        if (bStartOfScroll) 
        {
            pControl->GetState(10, &state);
            bStartOfScroll = FALSE;
            pControl->Pause();
        }
        // Update the position continuously.
        REFERENCE_TIME newTime = (g_rtTotalTime/100) * dwPosition;
        pSeek->SetPositions(&newTime, AM_SEEKING_AbsolutePositioning,
            NULL, AM_SEEKING_NoPositioning);

        // Restore the state at the end.
        if (userReq == TB_ENDTRACK)
        {
            if (state == State_Stopped)
                pControl->Stop();
            else if (state == State_Running) 
                pControl->Run();
            bStartOfScroll = TRUE;
        }
    }
}
```



Если пользователь перетаскивает ползунок, приложение выдает ряд команд Seek, по одному для каждого \_ полученного сообщения сумбтракк. Чтобы сделать операции поиска максимально гладкими, приложение приостанавливает граф. Приостановка графа останавливает воспроизведение, но гарантирует обновление окна видео. Когда приложение получает \_ сообщение ЕНДТРАКК ТБ, оно восстанавливает исходное состояние графа.

 

 



