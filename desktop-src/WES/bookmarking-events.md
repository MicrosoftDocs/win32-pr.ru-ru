---
title: События закладок
description: Закладка определяет событие в канале или файле журнала.
ms.assetid: e7eeafc3-deb9-4cdc-9763-f784db7333be
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64d7fb4aef883a51084420c5a2d78e4f0ff25dac
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691547"
---
# <a name="bookmarking-events"></a><span data-ttu-id="9c719-103">События закладок</span><span class="sxs-lookup"><span data-stu-id="9c719-103">Bookmarking Events</span></span>

<span data-ttu-id="9c719-104">Закладка определяет событие в канале или файле журнала.</span><span class="sxs-lookup"><span data-stu-id="9c719-104">A bookmark identifies an event in a channel or log file.</span></span> <span data-ttu-id="9c719-105">Можно использовать закладку при запросе или подписываться на события, чтобы начать чтение событий из этого события с закладкой.</span><span class="sxs-lookup"><span data-stu-id="9c719-105">You can use a bookmark when you query for or subscribe to events to begin reading events from that bookmarked event.</span></span> <span data-ttu-id="9c719-106">Обычно создается закладка последнего события в результирующем наборе (при условии, что все события перечислены в результирующем наборе).</span><span class="sxs-lookup"><span data-stu-id="9c719-106">Typically you create a bookmark of the last event in the result set (assuming that you have enumerated all events in the result set).</span></span>

<span data-ttu-id="9c719-107">Следующая процедура описывает создание закладки на основе события.</span><span class="sxs-lookup"><span data-stu-id="9c719-107">The following procedure describes how to create a bookmark from an event.</span></span>

<span data-ttu-id="9c719-108">**Создание закладки на основе события**</span><span class="sxs-lookup"><span data-stu-id="9c719-108">**To create a bookmark from an event**</span></span>

1.  <span data-ttu-id="9c719-109">Чтобы создать закладку, вызовите функцию [**евткреатебукмарк**](/windows/desktop/api/WinEvt/nf-winevt-evtcreatebookmark) .</span><span class="sxs-lookup"><span data-stu-id="9c719-109">Call the [**EvtCreateBookmark**](/windows/desktop/api/WinEvt/nf-winevt-evtcreatebookmark) function to create a bookmark.</span></span> <span data-ttu-id="9c719-110">Передайте **значение NULL** для аргумента.</span><span class="sxs-lookup"><span data-stu-id="9c719-110">Pass **NULL** for the argument.</span></span>
2.  <span data-ttu-id="9c719-111">Вызовите функцию [**евтупдатебукмарк**](/windows/desktop/api/WinEvt/nf-winevt-evtupdatebookmark) , чтобы обновить закладку с помощью события.</span><span class="sxs-lookup"><span data-stu-id="9c719-111">Call the [**EvtUpdateBookmark**](/windows/desktop/api/WinEvt/nf-winevt-evtupdatebookmark) function to update the bookmark with the event.</span></span> <span data-ttu-id="9c719-112">Передайте в событие этот обработчик в качестве аргумента.</span><span class="sxs-lookup"><span data-stu-id="9c719-112">Pass the handle to the event as the argument.</span></span>
3.  <span data-ttu-id="9c719-113">Вызовите функцию [**евтрендер**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) , чтобы создать XML-строку, представляющую закладку.</span><span class="sxs-lookup"><span data-stu-id="9c719-113">Call the [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) function to create an XML string that represents the bookmark.</span></span> <span data-ttu-id="9c719-114">Передайте Евтрендербукмарк в качестве флага отрисовки.</span><span class="sxs-lookup"><span data-stu-id="9c719-114">Pass EvtRenderBookmark as the rendering flag.</span></span>
4.  <span data-ttu-id="9c719-115">Сохранить XML-строку для дальнейшего использования (например, можно сохранить XML-строку в файле или реестре).</span><span class="sxs-lookup"><span data-stu-id="9c719-115">Persist the XML string for use later (for example, you can persist the XML string in a file or the registry).</span></span>

<span data-ttu-id="9c719-116">Следующая процедура описывает создание закладки с помощью строки XML-закладки, которая была сохранена в предыдущей процедуре.</span><span class="sxs-lookup"><span data-stu-id="9c719-116">The following procedure describes how to create a bookmark using an XML bookmark string that was persisted in the previous procedure.</span></span>

<span data-ttu-id="9c719-117">**Создание закладки с помощью строки закладки XML**</span><span class="sxs-lookup"><span data-stu-id="9c719-117">**To create a bookmark using an XML bookmark string**</span></span>

1.  <span data-ttu-id="9c719-118">Получите XML-строку, которая представляет ранее сохраненную закладку.</span><span class="sxs-lookup"><span data-stu-id="9c719-118">Get the XML string that represents the bookmark that you previously persisted.</span></span>
2.  <span data-ttu-id="9c719-119">Чтобы создать закладку, вызовите функцию [**евткреатебукмарк**](/windows/desktop/api/WinEvt/nf-winevt-evtcreatebookmark) .</span><span class="sxs-lookup"><span data-stu-id="9c719-119">Call the [**EvtCreateBookmark**](/windows/desktop/api/WinEvt/nf-winevt-evtcreatebookmark) function to create a bookmark.</span></span> <span data-ttu-id="9c719-120">Передайте XML-строку для аргумента.</span><span class="sxs-lookup"><span data-stu-id="9c719-120">Pass the XML string for the argument.</span></span>

<span data-ttu-id="9c719-121">Следующая процедура описывает использование закладки в запросе.</span><span class="sxs-lookup"><span data-stu-id="9c719-121">The following procedure describes how to use a bookmark in a query.</span></span>

<span data-ttu-id="9c719-122">**Использование закладки в запросе**</span><span class="sxs-lookup"><span data-stu-id="9c719-122">**To use a bookmark in a query**</span></span>

1.  <span data-ttu-id="9c719-123">Вызовите функцию [**евткуери**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) для получения событий, соответствующих запросу.</span><span class="sxs-lookup"><span data-stu-id="9c719-123">Call the [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) function to get events that match your query.</span></span>
2.  <span data-ttu-id="9c719-124">Вызовите функцию [**евтсик**](/windows/desktop/api/WinEvt/nf-winevt-evtseek) , чтобы перейти к событию с закладкой.</span><span class="sxs-lookup"><span data-stu-id="9c719-124">Call the [**EvtSeek**](/windows/desktop/api/WinEvt/nf-winevt-evtseek) function to seek to the bookmarked event.</span></span> <span data-ttu-id="9c719-125">Передайте маркер в закладку и флаг Евтсикрелативетобукмарк.</span><span class="sxs-lookup"><span data-stu-id="9c719-125">Pass the handle to the bookmark and the EvtSeekRelativeToBookmark flag.</span></span>
3.  <span data-ttu-id="9c719-126">Вызовите функцию [**евтнекст**](/windows/desktop/api/WinEvt/nf-winevt-evtnext) в цикле, чтобы перечислить события, которые начинаются после события с закладкой (в зависимости от смещения, указанного в [**евтсик**](/windows/desktop/api/WinEvt/nf-winevt-evtseek)).</span><span class="sxs-lookup"><span data-stu-id="9c719-126">Call the [**EvtNext**](/windows/desktop/api/WinEvt/nf-winevt-evtnext) function in a loop to enumerate the events that begin after the bookmarked event (depending on the offset you specified in [**EvtSeek**](/windows/desktop/api/WinEvt/nf-winevt-evtseek)).</span></span>

<span data-ttu-id="9c719-127">Пример см. в разделе [Использование закладки в запросе](#using-a-bookmark-in-a-query).</span><span class="sxs-lookup"><span data-stu-id="9c719-127">For an example, see [Using a bookmark in a query](#using-a-bookmark-in-a-query).</span></span>

<span data-ttu-id="9c719-128">В следующей процедуре описывается использование закладки в подписке.</span><span class="sxs-lookup"><span data-stu-id="9c719-128">The following procedure describes how to use a bookmark in a subscription.</span></span>

<span data-ttu-id="9c719-129">**Использование закладки в подписке**</span><span class="sxs-lookup"><span data-stu-id="9c719-129">**To use a bookmark in a subscription**</span></span>

1.  <span data-ttu-id="9c719-130">Вызовите функцию [**евтсубскрибе**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) , чтобы подписываться на события, соответствующие запросу.</span><span class="sxs-lookup"><span data-stu-id="9c719-130">Call the [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) function to subscribe to events that match your query.</span></span> <span data-ttu-id="9c719-131">Передайте маркер в закладку и флаг Евтсубскрибестартафтербукмарк.</span><span class="sxs-lookup"><span data-stu-id="9c719-131">Pass the handle to the bookmark and the EvtSubscribeStartAfterBookmark flag.</span></span>
2.  <span data-ttu-id="9c719-132">Если вы реализовали [**функцию \_ \_ обратного вызова evt Subscribe**](/windows/win32/api/winevt/nc-winevt-evt_subscribe_callback) , ваш обратный вызов будет принимать события, которые начинаются после события с закладкой.</span><span class="sxs-lookup"><span data-stu-id="9c719-132">If you implemented the [**EVT\_SUBSCRIBE\_CALLBACK**](/windows/win32/api/winevt/nc-winevt-evt_subscribe_callback) function, your callback will receive events that begin after the bookmarked event.</span></span>
3.  <span data-ttu-id="9c719-133">Если вы не реализовали обратный вызов, вызовите функцию [**евтнекст**](/windows/desktop/api/WinEvt/nf-winevt-evtnext) в цикле, чтобы перечислить события, которые начинаются после события с закладкой.</span><span class="sxs-lookup"><span data-stu-id="9c719-133">If you did not implement the callback, call the [**EvtNext**](/windows/desktop/api/WinEvt/nf-winevt-evtnext) function in a loop to enumerate the events that begin after the bookmarked event.</span></span>

<span data-ttu-id="9c719-134">Пример см. в разделе [Использование закладки в подписке](#using-a-bookmark-in-a-subscription).</span><span class="sxs-lookup"><span data-stu-id="9c719-134">For an example, see [Using a bookmark in a subscription](#using-a-bookmark-in-a-subscription).</span></span>

## <a name="using-a-bookmark-in-a-query"></a><span data-ttu-id="9c719-135">Использование закладки в запросе</span><span class="sxs-lookup"><span data-stu-id="9c719-135">Using a bookmark in a query</span></span>

<span data-ttu-id="9c719-136">В следующем примере показано, как использовать закладку в запросе.</span><span class="sxs-lookup"><span data-stu-id="9c719-136">The following example shows how to use a bookmark in a query.</span></span> <span data-ttu-id="9c719-137">Пример разворачивается в примере [запроса событий](querying-for-events.md).</span><span class="sxs-lookup"><span data-stu-id="9c719-137">The example expands on the example in [Querying for Events](querying-for-events.md).</span></span>


```C++
// Enumerate all the events in the result set beginning with the bookmarked event. 
DWORD PrintResults(EVT_HANDLE hResults)
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hEvents[ARRAY_SIZE];
    DWORD dwReturned = 0;
    LPWSTR pwsBookmarkXml = NULL;
    EVT_HANDLE hBookmark = NULL;

    // Get the persisted bookmark XML string.
    pwsBookmarkXml = GetBookmarkedString();

    // If the bookmark string was persisted, create a bookmark and
    // seek to the bookmarked event in the result set.
    if (pwsBookmarkXml)
    {
        hBookmark = EvtCreateBookmark(pwsBookmarkXml);
        if (NULL == hBookmark)
        {
            wprintf(L"EvtCreateBookmark failed with %lu\n", GetLastError());
            goto cleanup;
        }

        if (!EvtSeek(hResults, 1, hBookmark, 0, EvtSeekRelativeToBookmark))
        {
            wprintf(L"EvtSeek failed with %lu\n", GetLastError());
            goto cleanup;
        }
    }

    // Enumerate the events in the result set after the bookmarked event.
    while (true)
    {
        if (!EvtNext(hResults, ARRAY_SIZE, hEvents, INFINITE, 0, &dwReturned))
        {
            if (ERROR_NO_MORE_ITEMS != (status = GetLastError()))
            {
                wprintf(L"EvtNext failed with %lu\n", status);
            }

            goto cleanup;
        }

        for (DWORD i = 0; i < dwReturned; i++)
        {
            if (status = PrintEvent(hEvents[i]))
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

    if (ERROR_NO_MORE_ITEMS == status)
    {
        // Get the last event in the result set, use it to create a
        // bookmark, render the bookmark as an XML string, and persist the string.
        if (ERROR_SUCCESS != (status = SaveBookmark(hResults)))
            wprintf(L"\nFailed to save bookmark\n");
    }
    else
    {
        for (DWORD i = 0; i < dwReturned; i++)
        {
            if (NULL != hEvents[i])
                EvtClose(hEvents[i]);
        }
    }

    if (pwsBookmarkXml)
        free(pwsBookmarkXml);

    return status;
}

// Get the bookmark XML string from wherever you persisted it.
LPWSTR GetBookmarkedString(void)
{
    LPWSTR pwsBookmarkXML = NULL;

    // TODO: Add the code to get the bookmark XML string from storage.

    return pwsBookmarkXML;
}


// Persist the bookmark XML string. This example assumes that we've read through
// the result set and are persisting the last event as the bookmark.
DWORD SaveBookmark(EVT_HANDLE hResults)
{
    DWORD status = ERROR_SUCCESS;
    DWORD dwBufferSize = 0;
    DWORD dwBufferUsed = 0;
    DWORD dwPropertyCount = 0;
    DWORD dwReturned = 0;
    LPWSTR pBookmarkXml = NULL;
    EVT_HANDLE hBookmark = NULL;
    EVT_HANDLE hEvent = NULL;

    // Seek to the last event in the result set and get the event.
    if (!EvtSeek(hResults, 0, NULL, 0, EvtSeekRelativeToLast))
    {
        wprintf(L"EvtSeek failed with %lu\n", status = GetLastError());
        goto cleanup;
    }

    if (!EvtNext(hResults, 1, &hEvent, INFINITE, 0, &dwReturned))
    {
        wprintf(L"EvtNext failed with %lu\n", status = GetLastError());
        goto cleanup;
    }

    // Create a bookmark and update it with the last event in the result set.
    hBookmark = EvtCreateBookmark(NULL);
    if (NULL == hBookmark)
    {
        wprintf(L"EvtCreateBookmark failed with %lu\n", GetLastError());
        goto cleanup;
    }

    if (!EvtUpdateBookmark(hBookmark, hEvent))
    {
        wprintf(L"EvtUpdateBookmark failed with %lu\n", GetLastError());
        goto cleanup;
    }

    // Render the bookmark as an XML string that you can then persist.
    if (!EvtRender(NULL, hBookmark, EvtRenderBookmark, dwBufferSize, pBookmarkXml, &dwBufferUsed, &dwPropertyCount))
    {
        if (ERROR_INSUFFICIENT_BUFFER == (status = GetLastError()))
        {
            dwBufferSize = dwBufferUsed;
            pBookmarkXml = (LPWSTR)malloc(dwBufferSize);
            if (pBookmarkXml)
            {
                EvtRender(NULL, hBookmark, EvtRenderBookmark, dwBufferSize, pBookmarkXml, &dwBufferUsed, &dwPropertyCount);
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

    // TODO: Add code to persist bookmark XML string.

cleanup:

    if (pBookmarkXml)
        free(pBookmarkXml);

    if (hBookmark)
        EvtClose(hBookmark);

    if (hEvent)
        EvtClose(hEvent);

    return status;
}
```



## <a name="using-a-bookmark-in-a-subscription"></a><span data-ttu-id="9c719-138">Использование закладки в подписке</span><span class="sxs-lookup"><span data-stu-id="9c719-138">Using a bookmark in a subscription</span></span>

<span data-ttu-id="9c719-139">В следующем примере показано, как использовать закладку в принудительной подписке.</span><span class="sxs-lookup"><span data-stu-id="9c719-139">The following example shows how to use a bookmark in a push subscription.</span></span>


```C++
#include <windows.h>
#include <conio.h>
#include <stdio.h>
#include <winevt.h>

#pragma comment(lib, "wevtapi.lib")

DWORD WINAPI SubscriptionCallback(EVT_SUBSCRIBE_NOTIFY_ACTION action, PVOID pContext, EVT_HANDLE hEvent);
DWORD PrintEvent(EVT_HANDLE hEvent);
EVT_HANDLE GetBookmark();
DWORD SaveBookmark(EVT_HANDLE hBookmark);


void main(void)
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hSubscription = NULL;
    EVT_HANDLE hBookmark = NULL;
    LPWSTR pwsPath = L"<channel name goes here>";
    LPWSTR pwsQuery = L"<xpath query goes here>";

    // Get the saved bookmark.
    hBookmark = GetBookmark();

    // Subscribe to existing and furture events beginning with the bookmarked event.
    // If the bookmark has not been persisted, pass an empty bookmark and the subscription
    // will begin with the second event that matches the query criteria.
    hSubscription = EvtSubscribe(NULL, NULL, pwsPath, pwsQuery, hBookmark, (PVOID)hBookmark, 
                                 (EVT_SUBSCRIBE_CALLBACK)SubscriptionCallback, EvtSubscribeStartAfterBookmark);
    if (NULL == hSubscription)
    {
        wprintf(L"EvtSubscribe failed with %lu.\n", GetLastError());
        goto cleanup;
    }

    wprintf(L"Hit any key to quit\n\n");
    while (!_kbhit())
        Sleep(10);

    status = SaveBookmark(hBookmark);

cleanup:

    if (hSubscription)
        EvtClose(hSubscription);

    if (hBookmark)
        EvtClose(hBookmark);
 }


// The callback that receives the events that match the query criteria. Use the 
// context parameter to pass the handle to the bookmark, so you can update the bookmark
// with each event that you receive.
DWORD WINAPI SubscriptionCallback(EVT_SUBSCRIBE_NOTIFY_ACTION action, PVOID pContext, EVT_HANDLE hEvent)
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hBookmark = (EVT_HANDLE)pContext;

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

            if (!EvtUpdateBookmark(hBookmark, hEvent))
            {
                wprintf(L"EvtUpdateBookmark failed with %lu\n", status = GetLastError());
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


EVT_HANDLE GetBookmark(void)
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hBookmark = NULL;
    LPWSTR pBookmarkXml = NULL;

    // Set pBookmarkXml to the XML string that you persisted in SaveBookmark.

    hBookmark = EvtCreateBookmark(pBookmarkXml);
    if (NULL == hBookmark)
    {
        wprintf(L"EvtCreateBookmark failed with %lu\n", GetLastError());
        goto cleanup;
    }

cleanup:

    if (pBookmarkXml)
        free(pBookmarkXml);

    return hBookmark;
}


DWORD SaveBookmark(EVT_HANDLE hBookmark)
{
    DWORD status = ERROR_SUCCESS;
    DWORD dwBufferSize = 0;
    DWORD dwBufferUsed = 0;
    DWORD dwPropertyCount = 0;
    LPWSTR pBookmarkXml = NULL;

    if (!EvtRender(NULL, hBookmark, EvtRenderBookmark, dwBufferSize, pBookmarkXml, &dwBufferUsed, &dwPropertyCount))
    {
        if (ERROR_INSUFFICIENT_BUFFER == (status = GetLastError()))
        {
            dwBufferSize = dwBufferUsed;
            pBookmarkXml = (LPWSTR)malloc(dwBufferSize);
            if (pBookmarkXml)
            {
                EvtRender(NULL, hBookmark, EvtRenderBookmark, dwBufferSize, pBookmarkXml, &dwBufferUsed, &dwPropertyCount);
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

    // Persist bookmark to a file or the registry.

cleanup:

    if (pBookmarkXml)
        free(pBookmarkXml);

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



 

 