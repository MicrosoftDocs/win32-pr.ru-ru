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
# <a name="writing-the-file"></a>Запись файла

Чтобы записать файл, просто запустите граф фильтра, вызвав метод [**имедиаконтрол:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) . Дождитесь завершения воспроизведения и явно прервите граф, вызвав [**имедиаконтрол:: останавливаться**](/windows/desktop/api/Control/nf-control-imediacontrol-stop); в противном случае файл будет записан неправильно.

Чтобы отобразить ход выполнения операции записи в файл, запросите фильтр мультиплексора для интерфейса [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) . Вызовите метод [**имедиасикинг::ической длительности**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) , чтобы получить длительность файла. Периодически во время выполнения графа вызовите метод [**имедиасикинг:: жеткуррентпоситион**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) для получения текущей позицией графа в потоке. Текущее расположение, деленное на Duration, дает процент завершения.

> [!Note]  
> Приложение обычно запрашивает диспетчер графа фильтров для **имедиасикинг**, но запись файла является исключением из этого правила. Диспетчер графов фильтров вычисляет текущую точку начиная с начальной и как долго работает граф, что является точным для воспроизведения файла, но не для записи файлов. Поэтому, чтобы получить точный результат, необходимо извлечь расположение из фильтра МУЛЬТИПЛЕКСОРа.

 

Следующий код возвращает длительность файла, запускает таймер для обновления пользовательского интерфейса приложения и запускает граф фильтра. (Для ясности пропущена проверка ошибок.)


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



Когда приложение получает событие таймера, оно может обновить пользовательский интерфейс с текущей позицией:


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



Когда приложение получает событие завершения DirectShow, оно должно прерывать граф, как показано в следующем коде:


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



 

 



