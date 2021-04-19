---
description: Управление внешним устройством
ms.assetid: 5347cd55-a27e-40b9-857c-09e3665a1817
title: Управление внешним устройством
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84cb82de59877f2527c92da9123d8a9d5a59d41e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536695"
---
# <a name="controlling-an-external-device"></a>Управление внешним устройством

Чтобы управлять устройством записи на магнитной ленте (Втр), используйте метод [**иамексттранспорт::p UT \_**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-put_mode) . Укажите новое состояние с помощью одной из констант, перечисленных в [состоянии транспорта устройства](device-transport-state.md). Например, чтобы отключить устройство, используйте следующую команду:


```C++
pTransport->put_Mode(ED_MODE_STOP); 
```



Так как Втр является физическим устройством, обычно возникает задержка между выдачей команды и завершением выполнения команды. Приложение должно создать второй рабочий поток, ожидающий завершения команды. По завершении выполнения команды поток может обновить пользовательский интерфейс. Используйте критическую секцию для сериализации изменения состояния.

Некоторые ВТРС могут уведомлять приложение об изменении состояния транспорта устройства. Если устройство поддерживает эту функцию, Рабочий поток может ожидать уведомления. Тем не менее, в соответствии со спецификацией торговой привязки 1394 "AV/C" (спецификация подединицы проигрывателя), то команда уведомления о состоянии транспорта необязательна, что означает, что устройства не обязаны поддерживать их. Если устройство не поддерживает уведомления, следует запрашивать его через периодические интервалы для его текущего состояния.

В этом разделе сначала описывается механизм уведомлений, а затем описывается опрос устройств.

Использование уведомления о состоянии транспорта

Уведомление о состоянии транспорта работает посредством того, что драйвер сообщает о событии, когда транспорт переключается на новое состояние. В приложении объявите критическую секцию, событие и обработчик потока. Критическая секция используется для синхронизации состояния устройства. Событие используется для остановки рабочего потока при выходе из приложения:


```C++
HANDLE hThread = 0;
HANDLE hThreadEnd = CreateEvent(NULL, TRUE, FALSE, NULL); 
if (hThreadEnd == NULL)
{
    // Handle error.
}
CRITICAL_SECTION csIssueCmd;
InitializeCriticalSection(&cdIssueCmd);
```



После создания экземпляра фильтра записи создайте рабочий поток:


```C++
DWORD ThreadId;
hThread = CreateThread(NULL, 0, ThreadProc, 0, 0, &ThreadId);
```



В рабочем потоке Начните с вызова метода [**иамексттранспорт::**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-getstatus) WebMethod со значением ED \_ уведомлять \_ Хевент \_ Get. Этот вызов возвращает дескриптор события, которое будет сигнальным после завершения операции:


```C++
// Get the handle to the notification event.
HANDLE hEvent = NULL;
hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_GET, (long*)&hNotify);
```



**Затем вызовите команду** GetNext еще раз и передайте значение \_ \_ уведомления об изменении режима ED \_ :


```C++
LONG State;
hr = pTransport->GetStatus(ED_MODE_CHANGE_NOTIFY, &State);
```



Если устройство поддерживает уведомление, метод возвращает значение " \_ в ожидании". (В противном случае необходимо опросить устройство, как описано в следующем разделе.) Предполагая, что устройство поддерживает уведомление, событие будет сигнальным при каждом изменении состояния транспорта Втр. На этом этапе можно обновить пользовательский интерфейс, чтобы отразить новое состояние. Чтобы получить следующее уведомление, сбросьте этот обработчик событий и снова **вызовите метод** GetNext с \_ \_ изменением уведомлений в режиме ED \_ .

Перед выходом из рабочего потока освободите его, **вызвав команду** "getHandler" с флагом \_ \_ Хевент \_ и адресом маркера:


```C++
hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_RELEASE, (long*)&hNotify)
```



В следующем коде показана полная процедура потока. Предполагается, что функция Упдатетранспортстате является функцией приложения, которая обновляет пользовательский интерфейс. Обратите внимание, что поток ожидает два события: событие уведомления (*хнотифи*) и событие завершения потока (*хсреаденд*). Также обратите внимание, где критическая секция используется для защиты переменной состояния устройства.


```C++
DWORD WINAPI ThreadProc(void *pParam)
{
    HRESULT hr;
    HANDLE  EventHandles[2];
    HANDLE  hNotify = NULL;
    DWORD   WaitStatus;
    LONG    State;

    // Get the notification event handle. This event will be signaled when
    // the next state-change operation completes.   
    hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_GET, (long*)&hNotify);

    while (hThread && hNotify && hThreadEnd) 
    {
        EnterCriticalSection(&csIssueCmd);
        // Ask the device to notify us when the state changes.
        hr = pTransport->GetStatus(ED_MODE_CHANGE_NOTIFY, &State);
        LeaveCriticalSection(&csIssueCmd); 

        if(hr == E_PENDING)  // The device supports notification.
        {
            // Wait for the notification.
            EventHandles[0] = hNotify;
            EventHandles[1] = hThreadEnd;
            WaitStatus = WaitForMultipleObjects(2, EventHandles, FALSE, INFINITE);
            if(WAIT_OBJECT_0 == WaitStatus) 
            {
                // We got notified. Query for the new state.
                EnterCriticalSection(&csIssueCmd);  
                hr = m_pTransport->get_Mode(State);
                UpdateTransportState(State);  // Update the UI.
                LeaveCriticalSection(&m_csIssueCmd);
                ResetEvent(hNotify);
            } 
            else {
                break;  // End this thread.
            }
        } 
        else {          
            // The device does not support notification.
            PollDevice();        
        } 
    } // while

    // Cancel notification. 
    hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_RELEASE, (long*)&hNotify);
    return 1; 
}
```



Также используйте критическую секцию при выдаче команд на устройство, как показано ниже.


```C++
// Issue the "stop" command.
EnterCriticalSection(&csIssueCmd); 
if (SUCCEEDED(hr = pTransport->put_Mode(ED_MODE_STOP)))
{
    UpdateTransportState(ED_MODE_STOP);
}
LeaveCriticalSection(&csIssueCmd); 
```



Перед выходом из приложения остановите вторичный поток, задав событие конца потока:


```C++
if (hThread) 
{
    // Signaling this event will cause the thread to end.    
    if (SetEvent(hThreadEnd))
    {
        // Wait for it to end.
        WaitForSingleObjectEx(hThread, INFINITE, FALSE);
    }
}
CloseHandle(hThreadEnd);
CloseHandle(hThread);
```



Опрос состояния транспорта

При вызове **иамексттранспорт::-Status** с \_ \_ \_ флагом уведомления об изменении режима ED, а возвращаемое значение не является E- \_ ожидающим, это означает, что устройство не поддерживает уведомления. В этом случае необходимо опросить устройство, чтобы определить его состояние. *Опрос* просто означает вызов **\_ режима получения** с регулярными интервалами для проверки состояния транспорта. Необходимо по-прежнему использовать вторичный поток и критическую секцию, как описано выше. Поток запрашивает у устройства состояние через обычный интервал. В следующем примере показан один из способов реализации потока:


```C++
DWORD WINAPI ThreadProc(void *pParam)
{
    HRESULT hr;
    LONG State;
    DWORD WaitStatus;

    while (hThread && hThreadEnd) 
    {
        EnterCriticalSection(&csIssueCmd);  
        State = 0;
        hr = pTransport->get_Mode(&State);
        LeaveCriticalSection(&csIssueCmd); 
        UpdateTransportState(State);

        // Wait for a while, or until the thread ends. 
        WaitStatus = WaitForSingleObjectEx(hThreadEnd, 200, FALSE); 
        if (WaitStatus == WAIT_OBJECT_0)
        {
            break; // Exit thread now. 
        }
        // Otherwise, the wait timed out. Time to poll again.
    }
    return 1;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Управление видеокамерой](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



