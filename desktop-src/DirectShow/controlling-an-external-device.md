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
# <a name="controlling-an-external-device"></a><span data-ttu-id="7ba80-103">Управление внешним устройством</span><span class="sxs-lookup"><span data-stu-id="7ba80-103">Controlling an External Device</span></span>

<span data-ttu-id="7ba80-104">Чтобы управлять устройством записи на магнитной ленте (Втр), используйте метод [**иамексттранспорт::p UT \_**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-put_mode) .</span><span class="sxs-lookup"><span data-stu-id="7ba80-104">To control a video tape recorder (VTR) device, use the [**IAMExtTransport::put\_Mode**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-put_mode) method.</span></span> <span data-ttu-id="7ba80-105">Укажите новое состояние с помощью одной из констант, перечисленных в [состоянии транспорта устройства](device-transport-state.md).</span><span class="sxs-lookup"><span data-stu-id="7ba80-105">Specify the new state by using one of the constants listed in the [Device Transport State](device-transport-state.md).</span></span> <span data-ttu-id="7ba80-106">Например, чтобы отключить устройство, используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="7ba80-106">For example, to stop the device, use the following:</span></span>


```C++
pTransport->put_Mode(ED_MODE_STOP); 
```



<span data-ttu-id="7ba80-107">Так как Втр является физическим устройством, обычно возникает задержка между выдачей команды и завершением выполнения команды.</span><span class="sxs-lookup"><span data-stu-id="7ba80-107">Because the VTR is a physical device, there is typically a lag between issuing the command and when the command completes.</span></span> <span data-ttu-id="7ba80-108">Приложение должно создать второй рабочий поток, ожидающий завершения команды.</span><span class="sxs-lookup"><span data-stu-id="7ba80-108">Your application should create a second worker thread that waits for the command to finish.</span></span> <span data-ttu-id="7ba80-109">По завершении выполнения команды поток может обновить пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="7ba80-109">When the command finishes, the thread can update the user interface.</span></span> <span data-ttu-id="7ba80-110">Используйте критическую секцию для сериализации изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="7ba80-110">Use a critical section to serialize the state change.</span></span>

<span data-ttu-id="7ba80-111">Некоторые ВТРС могут уведомлять приложение об изменении состояния транспорта устройства.</span><span class="sxs-lookup"><span data-stu-id="7ba80-111">Some VTRs can notify the application when the device's transport state has changed.</span></span> <span data-ttu-id="7ba80-112">Если устройство поддерживает эту функцию, Рабочий поток может ожидать уведомления.</span><span class="sxs-lookup"><span data-stu-id="7ba80-112">If the device supports this feature, the worker thread can wait for the notification.</span></span> <span data-ttu-id="7ba80-113">Тем не менее, в соответствии со спецификацией торговой привязки 1394 "AV/C" (спецификация подединицы проигрывателя), то команда уведомления о состоянии транспорта необязательна, что означает, что устройства не обязаны поддерживать их.</span><span class="sxs-lookup"><span data-stu-id="7ba80-113">According to the 1394 Trade Association's "AV/C Tape Recorder/Player Subunit Specification", however, the transport-state notification command is optional, meaning devices are not required to support it.</span></span> <span data-ttu-id="7ba80-114">Если устройство не поддерживает уведомления, следует запрашивать его через периодические интервалы для его текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="7ba80-114">If a device does not support notification, you should poll the device at periodic intervals for its current state.</span></span>

<span data-ttu-id="7ba80-115">В этом разделе сначала описывается механизм уведомлений, а затем описывается опрос устройств.</span><span class="sxs-lookup"><span data-stu-id="7ba80-115">This section first describes the notification mechanism, and then describes device polling.</span></span>

<span data-ttu-id="7ba80-116">Использование уведомления о состоянии транспорта</span><span class="sxs-lookup"><span data-stu-id="7ba80-116">Using Transport State Notification</span></span>

<span data-ttu-id="7ba80-117">Уведомление о состоянии транспорта работает посредством того, что драйвер сообщает о событии, когда транспорт переключается на новое состояние.</span><span class="sxs-lookup"><span data-stu-id="7ba80-117">Transport state notification works by having the driver signal an event when the transport switches to a new state.</span></span> <span data-ttu-id="7ba80-118">В приложении объявите критическую секцию, событие и обработчик потока.</span><span class="sxs-lookup"><span data-stu-id="7ba80-118">In your application, declare a critical section, an event, and a thread handle.</span></span> <span data-ttu-id="7ba80-119">Критическая секция используется для синхронизации состояния устройства.</span><span class="sxs-lookup"><span data-stu-id="7ba80-119">The critical section is used to synchronize the device state.</span></span> <span data-ttu-id="7ba80-120">Событие используется для остановки рабочего потока при выходе из приложения:</span><span class="sxs-lookup"><span data-stu-id="7ba80-120">The event is used to halt the worker thread when the application exits:</span></span>


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



<span data-ttu-id="7ba80-121">После создания экземпляра фильтра записи создайте рабочий поток:</span><span class="sxs-lookup"><span data-stu-id="7ba80-121">After you create an instance of the capture filter, create the worker thread:</span></span>


```C++
DWORD ThreadId;
hThread = CreateThread(NULL, 0, ThreadProc, 0, 0, &ThreadId);
```



<span data-ttu-id="7ba80-122">В рабочем потоке Начните с вызова метода [**иамексттранспорт::**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-getstatus) WebMethod со значением ED \_ уведомлять \_ Хевент \_ Get.</span><span class="sxs-lookup"><span data-stu-id="7ba80-122">In the worker thread, start by calling the [**IAMExtTransport::GetStatus**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-getstatus) method with the value ED\_NOTIFY\_HEVENT\_GET.</span></span> <span data-ttu-id="7ba80-123">Этот вызов возвращает дескриптор события, которое будет сигнальным после завершения операции:</span><span class="sxs-lookup"><span data-stu-id="7ba80-123">This call returns a handle to an event that will be signaled when an operation completes:</span></span>


```C++
// Get the handle to the notification event.
HANDLE hEvent = NULL;
hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_GET, (long*)&hNotify);
```



<span data-ttu-id="7ba80-124">**Затем вызовите команду** GetNext еще раз и передайте значение \_ \_ уведомления об изменении режима ED \_ :</span><span class="sxs-lookup"><span data-stu-id="7ba80-124">Next, call **GetState** again and pass the value ED\_MODE\_CHANGE\_NOTIFY:</span></span>


```C++
LONG State;
hr = pTransport->GetStatus(ED_MODE_CHANGE_NOTIFY, &State);
```



<span data-ttu-id="7ba80-125">Если устройство поддерживает уведомление, метод возвращает значение " \_ в ожидании".</span><span class="sxs-lookup"><span data-stu-id="7ba80-125">If the device supports notification, the method returns the value E\_PENDING.</span></span> <span data-ttu-id="7ba80-126">(В противном случае необходимо опросить устройство, как описано в следующем разделе.) Предполагая, что устройство поддерживает уведомление, событие будет сигнальным при каждом изменении состояния транспорта Втр.</span><span class="sxs-lookup"><span data-stu-id="7ba80-126">(Otherwise, you must poll device, as described in the next section.) Assuming the device supports notification, the event will be signaled whenever the state of the VTR transport changes.</span></span> <span data-ttu-id="7ba80-127">На этом этапе можно обновить пользовательский интерфейс, чтобы отразить новое состояние.</span><span class="sxs-lookup"><span data-stu-id="7ba80-127">At this point, you can update the user interface to reflect the new state.</span></span> <span data-ttu-id="7ba80-128">Чтобы получить следующее уведомление, сбросьте этот обработчик событий и снова **вызовите метод** GetNext с \_ \_ изменением уведомлений в режиме ED \_ .</span><span class="sxs-lookup"><span data-stu-id="7ba80-128">To get the next notification, reset the event handle and call **GetStatus** with ED\_MODE\_CHANGE\_NOTIFY again.</span></span>

<span data-ttu-id="7ba80-129">Перед выходом из рабочего потока освободите его, **вызвав команду** "getHandler" с флагом \_ \_ Хевент \_ и адресом маркера:</span><span class="sxs-lookup"><span data-stu-id="7ba80-129">Before the worker thread exits, release the event handle by calling **GetStatus** with the flag ED\_NOTIFY\_HEVENT\_RELEASE and the address of the handle:</span></span>


```C++
hr = pTransport->GetStatus(ED_NOTIFY_HEVENT_RELEASE, (long*)&hNotify)
```



<span data-ttu-id="7ba80-130">В следующем коде показана полная процедура потока.</span><span class="sxs-lookup"><span data-stu-id="7ba80-130">The following code shows the complete thread procedure.</span></span> <span data-ttu-id="7ba80-131">Предполагается, что функция Упдатетранспортстате является функцией приложения, которая обновляет пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="7ba80-131">The function UpdateTransportState is assumed to be an application function that updates the user interface.</span></span> <span data-ttu-id="7ba80-132">Обратите внимание, что поток ожидает два события: событие уведомления (*хнотифи*) и событие завершения потока (*хсреаденд*).</span><span class="sxs-lookup"><span data-stu-id="7ba80-132">Note that the thread waits for two events: the notification event (*hNotify*) and the thread-termination event (*hThreadEnd*).</span></span> <span data-ttu-id="7ba80-133">Также обратите внимание, где критическая секция используется для защиты переменной состояния устройства.</span><span class="sxs-lookup"><span data-stu-id="7ba80-133">Also note where the critical section is used to protect the device state variable.</span></span>


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



<span data-ttu-id="7ba80-134">Также используйте критическую секцию при выдаче команд на устройство, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="7ba80-134">Also use the critical section when you issue commands to the device, as follows:</span></span>


```C++
// Issue the "stop" command.
EnterCriticalSection(&csIssueCmd); 
if (SUCCEEDED(hr = pTransport->put_Mode(ED_MODE_STOP)))
{
    UpdateTransportState(ED_MODE_STOP);
}
LeaveCriticalSection(&csIssueCmd); 
```



<span data-ttu-id="7ba80-135">Перед выходом из приложения остановите вторичный поток, задав событие конца потока:</span><span class="sxs-lookup"><span data-stu-id="7ba80-135">Before the application exits, halt the secondary thread by setting the thread-end event:</span></span>


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



<span data-ttu-id="7ba80-136">Опрос состояния транспорта</span><span class="sxs-lookup"><span data-stu-id="7ba80-136">Polling the Transport State</span></span>

<span data-ttu-id="7ba80-137">При вызове **иамексттранспорт::-Status** с \_ \_ \_ флагом уведомления об изменении режима ED, а возвращаемое значение не является E- \_ ожидающим, это означает, что устройство не поддерживает уведомления.</span><span class="sxs-lookup"><span data-stu-id="7ba80-137">If you call **IAMExtTransport::GetStatus** with the ED\_MODE\_CHANGE\_NOTIFY flag and the return value is not E\_PENDING, it means the device does not support notification.</span></span> <span data-ttu-id="7ba80-138">В этом случае необходимо опросить устройство, чтобы определить его состояние.</span><span class="sxs-lookup"><span data-stu-id="7ba80-138">In that case, you must poll the device to determine its state.</span></span> <span data-ttu-id="7ba80-139">*Опрос* просто означает вызов **\_ режима получения** с регулярными интервалами для проверки состояния транспорта.</span><span class="sxs-lookup"><span data-stu-id="7ba80-139">*Polling* simply means calling **get\_Mode** at regular intervals to check the transport state.</span></span> <span data-ttu-id="7ba80-140">Необходимо по-прежнему использовать вторичный поток и критическую секцию, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="7ba80-140">You should still use a secondary thread and a critical section, as described earlier.</span></span> <span data-ttu-id="7ba80-141">Поток запрашивает у устройства состояние через обычный интервал.</span><span class="sxs-lookup"><span data-stu-id="7ba80-141">The thread queries the device for its state at a regular interval.</span></span> <span data-ttu-id="7ba80-142">В следующем примере показан один из способов реализации потока:</span><span class="sxs-lookup"><span data-stu-id="7ba80-142">The following example shows one way to implement the thread:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="7ba80-143">См. также</span><span class="sxs-lookup"><span data-stu-id="7ba80-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ba80-144">Управление видеокамерой</span><span class="sxs-lookup"><span data-stu-id="7ba80-144">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



