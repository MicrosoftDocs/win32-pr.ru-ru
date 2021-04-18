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
# <a name="implementing-a-seek-bar"></a><span data-ttu-id="67acd-103">Реализация панели поиска</span><span class="sxs-lookup"><span data-stu-id="67acd-103">Implementing a Seek Bar</span></span>

<span data-ttu-id="67acd-104">В этом разделе описывается, как реализовать панель поиска для приложения мультимедиа-проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="67acd-104">This section describes how to implement a seek bar for a media-player application.</span></span> <span data-ttu-id="67acd-105">Панель поиска реализуется как элемент управления TrackBar.</span><span class="sxs-lookup"><span data-stu-id="67acd-105">The seek bar is implemented as a trackbar control.</span></span> <span data-ttu-id="67acd-106">Общие сведения о поиске в DirectShow см. в разделе [Поиск графа фильтра](seeking-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="67acd-106">For an overview of seeking in DirectShow, see [Seeking the Filter Graph](seeking-the-filter-graph.md).</span></span>

<span data-ttu-id="67acd-107">При запуске приложения инициализируйте значение TrackBar:</span><span class="sxs-lookup"><span data-stu-id="67acd-107">When the application starts, initialize the trackbar:</span></span>


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



<span data-ttu-id="67acd-108">Значение TrackBar отключается, пока пользователь не откроет файл мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="67acd-108">The trackbar is disabled until the user opens a media file.</span></span> <span data-ttu-id="67acd-109">Диапазон TrackBar имеет значение от 0 до 100.</span><span class="sxs-lookup"><span data-stu-id="67acd-109">The trackbar range is set from 0 to 100.</span></span> <span data-ttu-id="67acd-110">Во время воспроизведения файла приложение вычисляет расположение воспроизведения в процентах от длительности файла и соответствующим образом обновляет TrackBar.</span><span class="sxs-lookup"><span data-stu-id="67acd-110">During file playback, the application will calculate the playback position as a percentage of the file duration, and update the trackbar accordingly.</span></span> <span data-ttu-id="67acd-111">Например, значение TrackBar "50" всегда соответствует середине файла.</span><span class="sxs-lookup"><span data-stu-id="67acd-111">For example, trackbar position "50" always corresponds to the middle of the file.</span></span>

<span data-ttu-id="67acd-112">Когда пользователь открывает файл, создайте граф воспроизведения файлов с помощью функции **RenderFile**.</span><span class="sxs-lookup"><span data-stu-id="67acd-112">When the user opens a file, build a file-playback graph using **RenderFile**.</span></span> <span data-ttu-id="67acd-113">Код для этого показан в [процедуре воспроизведения файла](how-to-play-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="67acd-113">The code for this is shown in [How To Play a File](how-to-play-a-file.md).</span></span> <span data-ttu-id="67acd-114">Затем выполните запрос к диспетчеру графа фильтров для интерфейса **имедиасикинг** и сохраните указатель интерфейса:</span><span class="sxs-lookup"><span data-stu-id="67acd-114">Then query the Filter Graph Manager for the **IMediaSeeking** interface and store the interface pointer:</span></span>


```C++
IMediaSeeking *g_pSeek = 0;
hr = pGraph->QueryInterface(IID_IMediaSeeking, (void**)&g_pSeek);
```



<span data-ttu-id="67acd-115">Чтобы определить, можно ли найти файл, вызовите метод [**имедиасикинг:: чекккапабилитиес**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) или метод [**Имедиасикинг:: Capabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="67acd-115">To determine whether the file is seekable, call either the [**IMediaSeeking::CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) method or the [**IMediaSeeking::GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) method.</span></span> <span data-ttu-id="67acd-116">Эти методы выполняются почти одинаково, но их семантика немного отличается.</span><span class="sxs-lookup"><span data-stu-id="67acd-116">These methods do almost the same thing, but their semantics are slightly different.</span></span> <span data-ttu-id="67acd-117">В следующем примере используется **чекккапабилитес**:</span><span class="sxs-lookup"><span data-stu-id="67acd-117">The following example uses **CheckCapabilites**:</span></span>


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



<span data-ttu-id="67acd-118">\_ \_ Флаг кансикабсолуте для поиска проверяет, доступен ли исходный файл, а флаг AM- \_ \_ канжетдуратион проверяет, можно ли заранее определить длительность файла.</span><span class="sxs-lookup"><span data-stu-id="67acd-118">The AM\_SEEKING\_CanSeekAbsolute flag checks whether the source file is seekable, and the AM\_SEEKING\_CanGetDuration flag checks whether the duration of the file can be determined in advance.</span></span> <span data-ttu-id="67acd-119">Если поддерживаются обе возможности, приложение включает параметр TrackBar и получает длительность файла.</span><span class="sxs-lookup"><span data-stu-id="67acd-119">If both of the capabilities are supported, the application enables the trackbar and retrieves the file duration.</span></span>

<span data-ttu-id="67acd-120">Если граф доступен для поиска, приложение будет использовать таймер для обновления расположения TrackBar во время воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="67acd-120">If the graph is seekable, the application will use a timer to update the trackbar position during playback.</span></span> <span data-ttu-id="67acd-121">При запуске графа фильтра для воспроизведения файла запустите событие таймера, вызвав одну из функций таймера Windows, например **сеттимер**.</span><span class="sxs-lookup"><span data-stu-id="67acd-121">When you run the filter graph to play the file, start the timer event by calling one of the Windows timer functions, such as **SetTimer**.</span></span> <span data-ttu-id="67acd-122">Дополнительные сведения о таймерах см. в разделе "таймеры" раздела Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="67acd-122">For more information about timers, see the topic "Timers" in the Platform SDK.</span></span>


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



<span data-ttu-id="67acd-123">Используйте событие Timer для обновления расположения TrackBar.</span><span class="sxs-lookup"><span data-stu-id="67acd-123">Use the timer event to update the position of the trackbar.</span></span> <span data-ttu-id="67acd-124">Вызовите [**имедиасикинг:: жеткуррентпоситион**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) , чтобы получить расположение воспроизведения куррант, а затем Вычислите значение в процентах от длительности файла:</span><span class="sxs-lookup"><span data-stu-id="67acd-124">Call [**IMediaSeeking::GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) to retrieve the currant playback position, and then calculate the position as a percentage of the file duration:</span></span>


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



<span data-ttu-id="67acd-125">Пользователь также может перемещать ползунок для поиска файла.</span><span class="sxs-lookup"><span data-stu-id="67acd-125">The user can also move the trackbar to seek the file.</span></span> <span data-ttu-id="67acd-126">Когда пользователь перетаскивает или щелкает элемент управления TrackBar, приложение получает \_ событие WM HSCROLL.</span><span class="sxs-lookup"><span data-stu-id="67acd-126">When the user drags or clicks the trackbar control, the application receives a WM\_HSCROLL event.</span></span> <span data-ttu-id="67acd-127">Младшее слово параметра *wParam* — это сообщение уведомления TrackBar.</span><span class="sxs-lookup"><span data-stu-id="67acd-127">The low word of the *wParam* parameter is the trackbar notification message.</span></span> <span data-ttu-id="67acd-128">Например, ТБ \_ ендтракк отправляется в конце действия TrackBar, а ТБ \_ сумбтракк постоянно отправляется, пока пользователь перетаскивает TrackBar.</span><span class="sxs-lookup"><span data-stu-id="67acd-128">For example, TB\_ENDTRACK is sent at the end of the trackbar action, and TB\_THUMBTRACK is sent continuously while the user drags the trackbar.</span></span> <span data-ttu-id="67acd-129">В следующем коде показан один из способов управления \_ сообщением WM HSCROLL:</span><span class="sxs-lookup"><span data-stu-id="67acd-129">The following code shows one way to handle the WM\_HSCROLL message:</span></span>


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



<span data-ttu-id="67acd-130">Если пользователь перетаскивает ползунок, приложение выдает ряд команд Seek, по одному для каждого \_ полученного сообщения сумбтракк.</span><span class="sxs-lookup"><span data-stu-id="67acd-130">If the user drags the trackbar, the application issues a series of seek commands, one for each TB\_THUMBTRACK message that it receives.</span></span> <span data-ttu-id="67acd-131">Чтобы сделать операции поиска максимально гладкими, приложение приостанавливает граф.</span><span class="sxs-lookup"><span data-stu-id="67acd-131">To make the seek operations as smooth as possible, the application pauses the graph.</span></span> <span data-ttu-id="67acd-132">Приостановка графа останавливает воспроизведение, но гарантирует обновление окна видео.</span><span class="sxs-lookup"><span data-stu-id="67acd-132">Pausing the graph halts playback but ensures that the video window is updated.</span></span> <span data-ttu-id="67acd-133">Когда приложение получает \_ сообщение ЕНДТРАКК ТБ, оно восстанавливает исходное состояние графа.</span><span class="sxs-lookup"><span data-stu-id="67acd-133">When the application receives the TB\_ENDTRACK message, it restores the graph to its original state.</span></span>

 

 



