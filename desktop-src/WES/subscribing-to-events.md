---
title: Подписка на события
description: Чтобы подписываться на события, вызовите функцию Евтсубскрибе.
ms.assetid: 1e86deeb-fc59-4658-9353-e4ced7ace89a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0889c4ff440a17696fe6d908ff98d632ff7058ca
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691546"
---
# <a name="subscribing-to-events"></a><span data-ttu-id="18fe9-103">Подписка на события</span><span class="sxs-lookup"><span data-stu-id="18fe9-103">Subscribing to Events</span></span>

<span data-ttu-id="18fe9-104">Чтобы подписываться на события, вызовите функцию [**евтсубскрибе**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) .</span><span class="sxs-lookup"><span data-stu-id="18fe9-104">To subscribe to events, call the [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) function.</span></span> <span data-ttu-id="18fe9-105">Вы можете подписываться на события от одного или нескольких административных или рабочих каналов.</span><span class="sxs-lookup"><span data-stu-id="18fe9-105">You can subscribe to events from one or more Admin or Operational channels.</span></span> <span data-ttu-id="18fe9-106">Канал может существовать на локальном или удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="18fe9-106">The channel can exist on the local computer or a remote computer.</span></span> <span data-ttu-id="18fe9-107">Чтобы указать события, на которые необходимо подписываться, можно использовать запрос XPath или XML-запрос структуры.</span><span class="sxs-lookup"><span data-stu-id="18fe9-107">To specify the events that you want to subscribe to, you can use an XPath query or a structure XML query.</span></span> <span data-ttu-id="18fe9-108">Дополнительные сведения о написании запроса см. в разделе [Использование событий](consuming-events.md).</span><span class="sxs-lookup"><span data-stu-id="18fe9-108">For details on writing the query, see [Consuming Events](consuming-events.md).</span></span>

<span data-ttu-id="18fe9-109">Журнал событий Windows содержит две модели для подписки на события:</span><span class="sxs-lookup"><span data-stu-id="18fe9-109">Windows Event Log provides two models for event subscription:</span></span>

-   <span data-ttu-id="18fe9-110">Модель Push отправляет события асинхронно в обратный вызов, который вы реализуете.</span><span class="sxs-lookup"><span data-stu-id="18fe9-110">The push model pushes events asynchronously to a callback that you implement.</span></span>
-   <span data-ttu-id="18fe9-111">Модель извлечения использует дескриптор события, созданный для оповещения при наличии доступных событий, соответствующих условиям запроса.</span><span class="sxs-lookup"><span data-stu-id="18fe9-111">The pull model uses an event handle that you create to signal you when there are events available that match your query criteria.</span></span> <span data-ttu-id="18fe9-112">Затем вы перечислите события в результирующем наборе.</span><span class="sxs-lookup"><span data-stu-id="18fe9-112">You then enumerate the events in the result set.</span></span>

<span data-ttu-id="18fe9-113">Можно подписываться на прошлые и будущие события, только будущие события, предыдущие и будущие события, начиная с помеченного события.</span><span class="sxs-lookup"><span data-stu-id="18fe9-113">You can subscribe to past and future events, future events only, or past and future events beginning after the bookmarked event.</span></span>

<span data-ttu-id="18fe9-114">Дополнительные сведения о подписке на события см. в разделе [принудительные подписки](#push-subscriptions) или [подписки по запросу](#pull-subscriptions).</span><span class="sxs-lookup"><span data-stu-id="18fe9-114">For details on subscribing to events, see [Push Subscriptions](#push-subscriptions) or [Pull Subscriptions](#pull-subscriptions).</span></span>

<span data-ttu-id="18fe9-115">Дополнительные сведения о отрисовке событий см. в разделе [Подготовка событий к просмотру](rendering-events.md).</span><span class="sxs-lookup"><span data-stu-id="18fe9-115">For details on rendering the events, see [Rendering Events](rendering-events.md).</span></span>

<span data-ttu-id="18fe9-116">Если вы хотите подписаться на события с того места, где вы остановились, Создайте закладку перед завершением подписки и используйте ее при следующей подписке на события.</span><span class="sxs-lookup"><span data-stu-id="18fe9-116">If you want to subscribe to events from where you left off, create a bookmark before ending your subscription and use it the next time you subscribe to events.</span></span> <span data-ttu-id="18fe9-117">Дополнительные сведения см. в разделе [события закладок](bookmarking-events.md).</span><span class="sxs-lookup"><span data-stu-id="18fe9-117">For details, see [Bookmarking Events](bookmarking-events.md).</span></span>

## <a name="push-subscriptions"></a><span data-ttu-id="18fe9-118">Принудительные подписки</span><span class="sxs-lookup"><span data-stu-id="18fe9-118">Push Subscriptions</span></span>

<span data-ttu-id="18fe9-119">В следующем примере показано, как подписаться на события, реализовать обратный вызов подписки и визуализировать события.</span><span class="sxs-lookup"><span data-stu-id="18fe9-119">The following example shows how to subscribe to events, implement the subscription callback, and render the events.</span></span>


```C++
#include <windows.h>
#include <conio.h>
#include <stdio.h>
#include <winevt.h>

#pragma comment(lib, "wevtapi.lib")

DWORD WINAPI SubscriptionCallback(EVT_SUBSCRIBE_NOTIFY_ACTION action, PVOID pContext, EVT_HANDLE hEvent);
DWORD PrintEvent(EVT_HANDLE hEvent);


void main(void)
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hSubscription = NULL;
    LPWSTR pwsPath = L"<channel name goes here>";
    LPWSTR pwsQuery = L"<xpath query goes here>";

    // Subscribe to events beginning with the oldest event in the channel. The subscription
    // will return all current events in the channel and any future events that are raised
    // while the application is active.
    hSubscription = EvtSubscribe(NULL, NULL, pwsPath, pwsQuery, NULL, NULL, 
                                 (EVT_SUBSCRIBE_CALLBACK)SubscriptionCallback, EvtSubscribeStartAtOldestRecord);
    if (NULL == hSubscription)
    {
        status = GetLastError();

        if (ERROR_EVT_CHANNEL_NOT_FOUND == status)
            wprintf(L"Channel %s was not found.\n", pwsPath);
        else if (ERROR_EVT_INVALID_QUERY == status)
            // You can call EvtGetExtendedStatus to get information as to why the query is not valid.
            wprintf(L"The query \"%s\" is not valid.\n", pwsQuery);
        else
            wprintf(L"EvtSubscribe failed with %lu.\n", status);

        goto cleanup;
    }

    wprintf(L"Hit any key to quit\n\n");
    while (!_kbhit())
        Sleep(10);

cleanup:

    if (hSubscription)
        EvtClose(hSubscription);
}

// The callback that receives the events that match the query criteria. 
DWORD WINAPI SubscriptionCallback(EVT_SUBSCRIBE_NOTIFY_ACTION action, PVOID pContext, EVT_HANDLE hEvent)
{
    UNREFERENCED_PARAMETER(pContext);
    
    DWORD status = ERROR_SUCCESS;

    switch(action)
    {
        // You should only get the EvtSubscribeActionError action if your subscription flags 
        // includes EvtSubscribeStrict and the channel contains missing event records.
        case EvtSubscribeActionError:
            if (ERROR_EVT_QUERY_RESULT_STALE == (DWORD)hEvent)
            {
                wprintf(L"The subscription callback was notified that event records are missing.\n");
                // Handle if this is an issue for your application.
            }
            else
            {
                wprintf(L"The subscription callback received the following Win32 error: %lu\n", (DWORD)hEvent);
            }
            break;

        case EvtSubscribeActionDeliver:
            if (ERROR_SUCCESS != (status = PrintEvent(hEvent)))
            {
                goto cleanup;
            }
            break;

        default:
            wprintf(L"SubscriptionCallback: Unknown action.\n");
    }

cleanup:

    if (ERROR_SUCCESS != status)
    {
        // End subscription - Use some kind of IPC mechanism to signal
        // your application to close the subscription handle.
    }

    return status; // The service ignores the returned status.
}

// Render the event as an XML string and print it.
DWORD PrintEvent(EVT_HANDLE hEvent)
{
    DWORD status = ERROR_SUCCESS;
    DWORD dwBufferSize = 0;
    DWORD dwBufferUsed = 0;
    DWORD dwPropertyCount = 0;
    LPWSTR pRenderedContent = NULL;

    if (!EvtRender(NULL, hEvent, EvtRenderEventXml, dwBufferSize, pRenderedContent, &dwBufferUsed, &dwPropertyCount))
    {
        if (ERROR_INSUFFICIENT_BUFFER == (status = GetLastError()))
        {
            dwBufferSize = dwBufferUsed;
            pRenderedContent = (LPWSTR)malloc(dwBufferSize);
            if (pRenderedContent)
            {
                EvtRender(NULL, hEvent, EvtRenderEventXml, dwBufferSize, pRenderedContent, &dwBufferUsed, &dwPropertyCount);
            }
            else
            {
                wprintf(L"malloc failed\n");
                status = ERROR_OUTOFMEMORY;
                goto cleanup;
            }
        }

        if (ERROR_SUCCESS != (status = GetLastError()))
        {
            wprintf(L"EvtRender failed with %d\n", status);
            goto cleanup;
        }
    }

    wprintf(L"%s\n\n", pRenderedContent);

cleanup:

    if (pRenderedContent)
        free(pRenderedContent);

    return status;
}
```



## <a name="pull-subscriptions"></a><span data-ttu-id="18fe9-120">Подписки по запросу</span><span class="sxs-lookup"><span data-stu-id="18fe9-120">Pull Subscriptions</span></span>

<span data-ttu-id="18fe9-121">Модель подписки по запросу использует объект события (см. функцию [**креативентекс**](/windows/desktop/api/synchapi/nf-synchapi-createeventexa) ), чтобы сообщить приложению о наличии в результирующем наборе событий, соответствующих критериям запроса.</span><span class="sxs-lookup"><span data-stu-id="18fe9-121">The pull subscription model uses an event object (see the [**CreateEventEx**](/windows/desktop/api/synchapi/nf-synchapi-createeventexa) function) to signal the application that there are events in the result set that match the query criteria.</span></span> <span data-ttu-id="18fe9-122">Создайте циклическую конструкцию, которая ожидает объект события, пока событие не будет сигнальным.</span><span class="sxs-lookup"><span data-stu-id="18fe9-122">Create a loop construct that waits on the event object until the event is signaled.</span></span> <span data-ttu-id="18fe9-123">Затем вызовите функцию [**евтнекст**](/windows/desktop/api/WinEvt/nf-winevt-evtnext) в цикле, чтобы перечислить события в результирующем наборе.</span><span class="sxs-lookup"><span data-stu-id="18fe9-123">Then, call the [**EvtNext**](/windows/desktop/api/WinEvt/nf-winevt-evtnext) function in a loop to enumerate the events in the result set.</span></span> <span data-ttu-id="18fe9-124">Если функция **евтнекст** завершается с ошибкой и задает для последней ошибки \_ больше \_ \_ элементов, сбросьте объект события и дождитесь, пока служба сообщит объект снова при наличии событий в результирующем наборе.</span><span class="sxs-lookup"><span data-stu-id="18fe9-124">When the **EvtNext** function fails and sets the last error to ERROR\_NO\_MORE\_ITEMS, reset the event object and wait for the service to signal the object again when there are events in the result set.</span></span>

<span data-ttu-id="18fe9-125">В следующем примере показано, как использовать модель подписки по запросу.</span><span class="sxs-lookup"><span data-stu-id="18fe9-125">The following example shows how to use the pull subscription model.</span></span>


```C++
#include <windows.h>
#include <conio.h>
#include <stdio.h>
#include <winevt.h>

#pragma comment(lib, "wevtapi.lib")

#define ARRAY_SIZE 10

DWORD EnumerateResults(EVT_HANDLE hResults);
DWORD PrintEvent(EVT_HANDLE hEvent);
BOOL IsKeyEvent(HANDLE hStdIn);

void __cdecl wmain()
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hSubscription = NULL;
    LPWSTR pwsPath = L"<channel name goes here>";
    LPWSTR pwsQuery = L"*";
    HANDLE aWaitHandles[2];
    DWORD dwWait = 0;

    // Get a handle for console input, so you can break out of the loop.
    aWaitHandles[0] = GetStdHandle(STD_INPUT_HANDLE);
    if (INVALID_HANDLE_VALUE == aWaitHandles[0])
    {
        wprintf(L"GetStdHandle failed with %lu.\n", GetLastError());
        goto cleanup;
    }

    // Get a handle to a manual reset event object that the subscription will signal
    // when events become available that match your query criteria.
    aWaitHandles[1] = CreateEvent(NULL, TRUE, TRUE, NULL);
    if (NULL == aWaitHandles[1])
    {
        wprintf(L"CreateEvent failed with %lu.\n", GetLastError());
        goto cleanup;
    }

    // Subscribe to events.
    hSubscription = EvtSubscribe(NULL, aWaitHandles[1], pwsPath, pwsQuery, NULL, NULL, NULL, EvtSubscribeStartAtOldestRecord);
    if (NULL == hSubscription)
    {
        status = GetLastError();

        if (ERROR_EVT_CHANNEL_NOT_FOUND == status)
            wprintf(L"Channel %s was not found.\n", pwsPath);
        else if (ERROR_EVT_INVALID_QUERY == status)
            wprintf(L"The query %s was not found.\n", pwsQuery);
        else
            wprintf(L"EvtSubscribe failed with %lu.\n", status);

        goto cleanup;
    }

    wprintf(L"Press any key to quit.\n");

    // Loop until the user presses a key or there is an error.
    while (true)
    {
        dwWait = WaitForMultipleObjects(sizeof(aWaitHandles)/sizeof(HANDLE), aWaitHandles, FALSE, INFINITE);

        if (0 == dwWait - WAIT_OBJECT_0)  // Console input
        {
            if (IsKeyEvent(aWaitHandles[0]))
                break;
        }
        else if (1 == dwWait - WAIT_OBJECT_0) // Query results
        {
            if (ERROR_NO_MORE_ITEMS != (status = EnumerateResults(hSubscription)))
            {
                break;
            }

            ResetEvent(aWaitHandles[1]);
        }
        else
        {
            if (WAIT_FAILED == dwWait)
            {
                wprintf(L"WaitForSingleObject failed with %lu\n", GetLastError());
            }
            break;
        }
    }

cleanup:

    if (hSubscription)
        EvtClose(hSubscription);

    if (aWaitHandles[0])
        CloseHandle(aWaitHandles[0]);

    if (aWaitHandles[1])
        CloseHandle(aWaitHandles[1]);
}

// Enumerate the events in the result set.
DWORD EnumerateResults(EVT_HANDLE hResults)
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hEvents[ARRAY_SIZE];
    DWORD dwReturned = 0;

    while (true)
    {
        // Get a block of events from the result set.
        if (!EvtNext(hResults, ARRAY_SIZE, hEvents, INFINITE, 0, &dwReturned))
        {
            if (ERROR_NO_MORE_ITEMS != (status = GetLastError()))
            {
                wprintf(L"EvtNext failed with %lu\n", status);
            }

            goto cleanup;
        }

        // For each event, call the PrintEvent function which renders the
        // event for display.
        for (DWORD i = 0; i < dwReturned; i++)
        {
            if (ERROR_SUCCESS == (status = PrintEvent(hEvents[i])))
            {
                EvtClose(hEvents[i]);
                hEvents[i] = NULL;
            }
            else
            {
                goto cleanup;
            }
        }
    }

cleanup:

    // Closes any events in case an error occurred above.
    for (DWORD i = 0; i < dwReturned; i++)
    {
        if (NULL != hEvents[i])
            EvtClose(hEvents[i]);
    }

    return status;
}

// Render the event as an XML string and print it.
DWORD PrintEvent(EVT_HANDLE hEvent)
{
    DWORD status = ERROR_SUCCESS;
    DWORD dwBufferSize = 0;
    DWORD dwBufferUsed = 0;
    DWORD dwPropertyCount = 0;
    LPWSTR pRenderedContent = NULL;

    // The EvtRenderEventXml flag tells EvtRender to render the event as an XML string.
    if (!EvtRender(NULL, hEvent, EvtRenderEventXml, dwBufferSize, pRenderedContent, &dwBufferUsed, &dwPropertyCount))
    {
        if (ERROR_INSUFFICIENT_BUFFER == (status = GetLastError()))
        {
            dwBufferSize = dwBufferUsed;
            pRenderedContent = (LPWSTR)malloc(dwBufferSize);
            if (pRenderedContent)
            {
                EvtRender(NULL, hEvent, EvtRenderEventXml, dwBufferSize, pRenderedContent, &dwBufferUsed, &dwPropertyCount);
            }
            else
            {
                wprintf(L"malloc failed\n");
                status = ERROR_OUTOFMEMORY;
                goto cleanup;
            }
        }

        if (ERROR_SUCCESS != (status = GetLastError()))
        {
            wprintf(L"EvtRender failed with %d\n", GetLastError());
            goto cleanup;
        }
    }

    wprintf(L"\n\n%s", pRenderedContent);

cleanup:

    if (pRenderedContent)
        free(pRenderedContent);

    return status;
}

// Determines whether the console input was a key event.
BOOL IsKeyEvent(HANDLE hStdIn)
{
    INPUT_RECORD Record[128];
    DWORD dwRecordsRead = 0;
    BOOL fKeyPress = FALSE;

    if (ReadConsoleInput(hStdIn, Record, 128, &dwRecordsRead))
    {
        for (DWORD i = 0; i < dwRecordsRead; i++)
        {
            if (KEY_EVENT == Record[i].EventType)
            {
                fKeyPress = TRUE;
                break;
            }
        }
    }

    return fKeyPress;
}
```



 

 