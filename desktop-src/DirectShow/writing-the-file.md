---
description: Запись файла
ms.assetid: d3dbe6ab-810c-4798-a769-c3f00c52a93a
title: Запись файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bda23b144956ab5afca9dd733b29a6f9d639cddf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683059"
---
# <a name="writing-the-file"></a><span data-ttu-id="5e6df-103">Запись файла</span><span class="sxs-lookup"><span data-stu-id="5e6df-103">Writing the File</span></span>

<span data-ttu-id="5e6df-104">Чтобы записать файл, просто запустите граф фильтра, вызвав метод [**имедиаконтрол:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) .</span><span class="sxs-lookup"><span data-stu-id="5e6df-104">To write the file, simply run the filter graph by calling the [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) method.</span></span> <span data-ttu-id="5e6df-105">Дождитесь завершения воспроизведения и явно прервите граф, вызвав [**имедиаконтрол:: останавливаться**](/windows/desktop/api/Control/nf-control-imediacontrol-stop); в противном случае файл будет записан неправильно.</span><span class="sxs-lookup"><span data-stu-id="5e6df-105">Wait for playback to complete and explicitly stop the graph by calling [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop); otherwise the file is not written correctly.</span></span>

<span data-ttu-id="5e6df-106">Чтобы отобразить ход выполнения операции записи в файл, запросите фильтр мультиплексора для интерфейса [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) .</span><span class="sxs-lookup"><span data-stu-id="5e6df-106">To display the progress of the file-writing operation, query the Mux filter for the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface.</span></span> <span data-ttu-id="5e6df-107">Вызовите метод [**имедиасикинг::ической длительности**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) , чтобы получить длительность файла.</span><span class="sxs-lookup"><span data-stu-id="5e6df-107">Call the [**IMediaSeeking::GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) method to retrieve the duration of the file.</span></span> <span data-ttu-id="5e6df-108">Периодически во время выполнения графа вызовите метод [**имедиасикинг:: жеткуррентпоситион**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) для получения текущей позицией графа в потоке.</span><span class="sxs-lookup"><span data-stu-id="5e6df-108">Periodically while the graph is running, call the [**IMediaSeeking::GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) method to retrieve the graph's current position in the stream.</span></span> <span data-ttu-id="5e6df-109">Текущее расположение, деленное на Duration, дает процент завершения.</span><span class="sxs-lookup"><span data-stu-id="5e6df-109">Current position divided by duration gives the percentage complete.</span></span>

> [!Note]  
> <span data-ttu-id="5e6df-110">Приложение обычно запрашивает диспетчер графа фильтров для **имедиасикинг**, но запись файла является исключением из этого правила.</span><span class="sxs-lookup"><span data-stu-id="5e6df-110">An application usually queries the Filter Graph Manager for **IMediaSeeking**, but file writing is an exception to this rule.</span></span> <span data-ttu-id="5e6df-111">Диспетчер графов фильтров вычисляет текущую точку начиная с начальной и как долго работает граф, что является точным для воспроизведения файла, но не для записи файлов.</span><span class="sxs-lookup"><span data-stu-id="5e6df-111">The Filter Graph Manager calculates the current position from the starting position and how long the graph has been running, which is accurate for file playback but not for file writing.</span></span> <span data-ttu-id="5e6df-112">Поэтому, чтобы получить точный результат, необходимо извлечь расположение из фильтра МУЛЬТИПЛЕКСОРа.</span><span class="sxs-lookup"><span data-stu-id="5e6df-112">Therefore, to get an accurate result, you should retrieve the position from the MUX filter.</span></span>

 

<span data-ttu-id="5e6df-113">Следующий код возвращает длительность файла, запускает таймер для обновления пользовательского интерфейса приложения и запускает граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="5e6df-113">The following code gets the duration of the file, starts a timer to update the application UI, and runs the filter graph.</span></span> <span data-ttu-id="5e6df-114">(Для ясности пропущена проверка ошибок.)</span><span class="sxs-lookup"><span data-stu-id="5e6df-114">(Error checking is omitted for clarity.)</span></span>


```C++
IMediaSeeking *pSeek = NULL;
IMediaEventEx *pEvent = NULL;
IMediaControl *pControl = NULL;
REFERENCE_TIME rtTotal;

// Query for interfaces. Remember to release them later.
hr = pMux->QueryInterface(IID_IMediaSeeking, (void**)&pSeek);
hr = pGraph->QueryInterface(IID_IMediaEventEx, (void**)&pEvent);
hr = pGraph->QueryInterface(IID_IMediaControl, (void**)&pControl);

// Error checking is omitted for clarity.

// Set the DirectShow event notification window.
hr = pEvent->SetNotifyWindow((OAHWND)hwnd, WM_GRAPHNOTIFY, 0);

// Set the range of the progress bar to the file length (in seconds).
hr = pSeek->GetDuration(&rtTotal);
SendDlgItemMessage(hwnd, IDC_PROGRESS1, PBM_SETRANGE, 0, 
   MAKELPARAM(0, rtTotal / 10000000));
// Start the timer.
UINT_PTR res = SetTimer(hwnd, nIDEvent, 100, NULL);
// Run the graph.
pControl->Run();
```



<span data-ttu-id="5e6df-115">Когда приложение получает событие таймера, оно может обновить пользовательский интерфейс с текущей позицией:</span><span class="sxs-lookup"><span data-stu-id="5e6df-115">When the application receives a timer event, it can update the UI with the current position:</span></span>


```C++
void OnTimer(HWND hDlg, IMediaSeeking *pSeek)
{
    REFERENCE_TIME rtNow;
    HRESULT hr = pSeek->GetCurrentPosition(&rtNow);
    if (SUCCEEDED(hr))
    {
        SendDlgItemMessage(hDlg, IDC_PROGRESS1, PBM_SETPOS, rtNow/10000000, 0);
    }
}
```



<span data-ttu-id="5e6df-116">Когда приложение получает событие завершения DirectShow, оно должно прерывать граф, как показано в следующем коде:</span><span class="sxs-lookup"><span data-stu-id="5e6df-116">When the application receives a DirectShow completion event, it should stop the graph, as shown in the following code:</span></span>


```C++
// Application window procedure
LRESULT CALLBACK WndProc(HWND hDlg, UINT msg, WPARAM wParam, LPARAM lParam)
{
    switch (msg)
    {
    /*  ...  */
    case WM_GRAPHNOTIFY:
        DoHandleEvent();
        break;
    /*  ...  */
    }
}

void DoHandleEvent()
{
    long evCode, param1, param2;
    bool bComplete = false;
    if (!pEvent) return;

    // Get all the events, and see we're done.
    while (SUCCEEDED(pEvent->GetEvent(&evCode, &param1, &param2, 0))
    {
        pEvent->FreeEventParams(evCode, param1, param2);
        switch(evCode)
        {
            case EC_USERABORT:
            case EC_ERRORABORT:
            case EC_COMPLETE:
                bComplete = true;
                break;
        }
    }
    if (bComplete)
    {
        pControl->Stop(); // Important! You must stop the graph!

        // Turn off event notification.
        pEvent->SetNotifyWindow(NULL, 0, 0);
        pEvent->Release();
        pEvent = NULL;
        // Reset the progress bar to zero and get rid of the timer.
        SendDlgItemMessage(IDC_PROGRESS1, PBM_SETPOS, 0, 0);
        KillTimer(hwnd, nIDEvent);
    }
}
```



 

 



