---
title: Запрос событий
description: Можно запросить события из канала или файла журнала.
ms.assetid: 929bedbf-6dce-428e-b2c0-de9dcfe4531b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6fa69f9b1308cd7ebbc4e4510692bb25ab031ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691644"
---
# <a name="querying-for-events"></a><span data-ttu-id="f2496-103">Запрос событий</span><span class="sxs-lookup"><span data-stu-id="f2496-103">Querying for Events</span></span>

<span data-ttu-id="f2496-104">Можно запросить события из канала или файла журнала.</span><span class="sxs-lookup"><span data-stu-id="f2496-104">You can query for events from a channel or a log file.</span></span> <span data-ttu-id="f2496-105">Канал или файл журнала может находиться на локальном или удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="f2496-105">The channel or log file can exist on the local computer or a remote computer.</span></span> <span data-ttu-id="f2496-106">Чтобы указать события, которые необходимо получить из канала или файла журнала, используйте запрос XPath или XML-запрос структуры.</span><span class="sxs-lookup"><span data-stu-id="f2496-106">To specify the events that you want to get from the channel or log file, you use an XPath query or a structure XML query.</span></span> <span data-ttu-id="f2496-107">Дополнительные сведения о написании запроса см. в разделе [Использование событий](consuming-events.md).</span><span class="sxs-lookup"><span data-stu-id="f2496-107">For details on writing the query, see [Consuming Events](consuming-events.md).</span></span>

<span data-ttu-id="f2496-108">Чтобы запросить события, вызовите функцию [**евткуери**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) .</span><span class="sxs-lookup"><span data-stu-id="f2496-108">To query events, call the [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) function.</span></span> <span data-ttu-id="f2496-109">Можно указать порядок, в котором будут возвращаться события (от старых к новым (по умолчанию) или от новых к старым), а также следует ли допускать некорректные выражения XPath в запросе (Дополнительные сведения о том, как функция пропускает неверно сформированные выражения, см. в разделе флаг [**евткуеритолератекуереррорс**](/windows/desktop/api/WinEvt/ne-winevt-evt_query_flags) ).</span><span class="sxs-lookup"><span data-stu-id="f2496-109">You can specify the order in which the events are returned (oldest to newest (the default) or newest to oldest) and whether to tolerate malformed XPath expressions in the query (for details on how the function ignores the malformed expressions, see the [**EvtQueryTolerateQueryErrors**](/windows/desktop/api/WinEvt/ne-winevt-evt_query_flags) flag).</span></span>

<span data-ttu-id="f2496-110">В следующем примере показано, как запрашивать события из канала с помощью выражения XPath.</span><span class="sxs-lookup"><span data-stu-id="f2496-110">The following example shows how to query events from a channel using an XPath expression.</span></span>


```C++
#include <windows.h>
#include <sddl.h>
#include <stdio.h>
#include <winevt.h>

#pragma comment(lib, "wevtapi.lib")

#define ARRAY_SIZE 10
#define TIMEOUT 1000  // 1 second; Set and use in place of INFINITE in EvtNext call

DWORD PrintResults(EVT_HANDLE hResults);
DWORD PrintEvent(EVT_HANDLE hEvent); // Shown in the Rendering Events topic

void main(void)
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hResults = NULL;
    LPWSTR pwsPath = L"<Name of the channel goes here>";
    LPWSTR pwsQuery = L"Event/System[EventID=4]";

    hResults = EvtQuery(NULL, pwsPath, pwsQuery, EvtQueryChannelPath | EvtQueryReverseDirection);
    if (NULL == hResults)
    {
        status = GetLastError();

        if (ERROR_EVT_CHANNEL_NOT_FOUND == status)
            wprintf(L"The channel was not found.\n");
        else if (ERROR_EVT_INVALID_QUERY == status)
            // You can call the EvtGetExtendedStatus function to try to get 
            // additional information as to what is wrong with the query.
            wprintf(L"The query is not valid.\n");
        else
            wprintf(L"EvtQuery failed with %lu.\n", status);

        goto cleanup;
    }

    PrintResults(hResults);

cleanup:

    if (hResults)
        EvtClose(hResults);

}
```



<span data-ttu-id="f2496-111">В следующем примере показано, как запрашивать события из канала с помощью структурированного XML-запроса.</span><span class="sxs-lookup"><span data-stu-id="f2496-111">The following example shows how to query events from a channel using a structured XML query.</span></span> <span data-ttu-id="f2496-112">События возвращаются в порядке от новых к старым.</span><span class="sxs-lookup"><span data-stu-id="f2496-112">The events are returned in order from newest to oldest.</span></span>


```C++
#include <windows.h>
#include <sddl.h>
#include <stdio.h>
#include <winevt.h>

#pragma comment(lib, "wevtapi.lib")

#define ARRAY_SIZE 10
#define TIMEOUT 1000  // 1 second; Set and use in place of INFINITE in EvtNext call

// The structured XML query.
#define QUERY \
    L"<QueryList>" \
    L"  <Query Path='Name of the channel goes here'>" \
    L"    <Select>Event/System[EventID=4]</Select>" \
    L"  </Query>" \
    L"</QueryList>"

DWORD PrintQueryStatuses(EVT_HANDLE hResults);
DWORD GetQueryStatusProperty(EVT_QUERY_PROPERTY_ID Id, EVT_HANDLE hResults, PEVT_VARIANT& pProperty);
DWORD PrintResults(EVT_HANDLE hResults);
DWORD PrintEvent(EVT_HANDLE hEvent);  // Shown in the Rendering Events topic

void main(void)
{
    DWORD status = ERROR_SUCCESS;
    EVT_HANDLE hResults = NULL;

    hResults = EvtQuery(NULL, NULL, QUERY, EvtQueryChannelPath | EvtQueryTolerateQueryErrors);
    if (NULL == hResults)
    {
        // Handle error.
        goto cleanup;
    }

    // Print the status of each query. If all the queries succeeded,
    // print the events in the result set. The status can be
    // ERROR_EVT_CHANNEL_NOT_FOUND or ERROR_EVT_INVALID_QUERY among others.
    if (ERROR_SUCCESS == PrintQueryStatuses(hResults))
        PrintResults(hResults);

cleanup:

    if (hResults)
        EvtClose(hResults);

}
```



<span data-ttu-id="f2496-113">Если вы используете структурированный XML-запрос и передаете флаг Евткуеритолератекуереррорс в [**евткуери**](/windows/desktop/api/WinEvt/nf-winevt-evtquery), функция выполняется успешно, даже если один или несколько запросов в структурированном запросе могут быть действительно неудачными.</span><span class="sxs-lookup"><span data-stu-id="f2496-113">If you are using a structured XML query and pass the EvtQueryTolerateQueryErrors flag to [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery), the function succeeds even though one or more of the queries in the structured query may have actually failed.</span></span> <span data-ttu-id="f2496-114">Чтобы определить, какие запросы в структурированном запросе завершились успешно или с ошибкой, вызовите функцию [**евтжеткуеринфо**](/windows/desktop/api/WinEvt/nf-winevt-evtgetqueryinfo) .</span><span class="sxs-lookup"><span data-stu-id="f2496-114">To determine which queries in the structured query succeeded or failed, call the [**EvtGetQueryInfo**](/windows/desktop/api/WinEvt/nf-winevt-evtgetqueryinfo) function.</span></span> <span data-ttu-id="f2496-115">Если не передать флаг Евткуеритолератекуереррорс, функция **евткуери** завершится с первой ошибкой, найденной в запросе.</span><span class="sxs-lookup"><span data-stu-id="f2496-115">If you do not pass the EvtQueryTolerateQueryErrors flag, the **EvtQuery** function will fail with the first error that it finds in the query.</span></span> <span data-ttu-id="f2496-116">Если запрос завершается с ошибкой \_ " \_ Недопустимый \_ запрос", вызовите функцию [**евтжетекстендедстатус**](/windows/desktop/api/WinEvt/nf-winevt-evtgetextendedstatus) , чтобы получить строку сообщения, описывающую ошибку XPath.</span><span class="sxs-lookup"><span data-stu-id="f2496-116">If the query fails with ERROR\_EVT\_INVALID\_QUERY, call the [**EvtGetExtendedStatus**](/windows/desktop/api/WinEvt/nf-winevt-evtgetextendedstatus) function to get a message string that describes the XPath error.</span></span>

<span data-ttu-id="f2496-117">В следующем примере показано, как определить успешность или сбой каждого запроса в структурированном запросе при передаче флага Евткуеритолератекуереррорс в [**евткуери**](/windows/desktop/api/WinEvt/nf-winevt-evtquery).</span><span class="sxs-lookup"><span data-stu-id="f2496-117">The following example shows how to determine the success or failure of each query in a structured query when passing the EvtQueryTolerateQueryErrors flag to [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery).</span></span>


```C++
// Get the list of paths in the query and the status for each path. Return
// the sum of the statuses, so the caller can decide whether to enumerate 
// the results.
DWORD PrintQueryStatuses(EVT_HANDLE hResults)
{
    DWORD status = ERROR_SUCCESS;
    PEVT_VARIANT pPaths = NULL;
    PEVT_VARIANT pStatuses = NULL;

    wprintf(L"List of channels/logs that were queried and their status\n\n");

    if (status = GetQueryStatusProperty(EvtQueryNames, hResults, pPaths))
        goto cleanup;

    if (status = GetQueryStatusProperty(EvtQueryStatuses, hResults, pStatuses))
        goto cleanup;

    for (DWORD i = 0; i < pPaths->Count; i++)
    {
        wprintf(L"%s (%lu)\n", pPaths->StringArr[i], pStatuses->UInt32Arr[i]);
        status += pStatuses->UInt32Arr[i];
    }

cleanup:

    if (pPaths)
        free(pPaths);

    if (pStatuses)
        free(pStatuses);

    return status;
}


// Get the list of paths specified in the query or the list of status values 
// for each path.
DWORD GetQueryStatusProperty(EVT_QUERY_PROPERTY_ID Id, EVT_HANDLE hResults, PEVT_VARIANT& pProperty)
{
    DWORD status = ERROR_SUCCESS;
    DWORD dwBufferSize = 0;
    DWORD dwBufferUsed = 0;

    if  (!EvtGetQueryInfo(hResults, Id, dwBufferSize, pProperty, &dwBufferUsed))
    {
        status = GetLastError();
        if (ERROR_INSUFFICIENT_BUFFER == status)
        {
            dwBufferSize = dwBufferUsed;
            pProperty = (PEVT_VARIANT)malloc(dwBufferSize);
            if (pProperty)
            {
                EvtGetQueryInfo(hResults, Id, dwBufferSize, pProperty, &dwBufferUsed);
            }
            else
            {
                wprintf(L"realloc failed\n");
                status = ERROR_OUTOFMEMORY;
                goto cleanup;
            }
        }

        if (ERROR_SUCCESS != (status = GetLastError()))
        {
            wprintf(L"EvtGetQueryInfo failed with %d\n", GetLastError());
            goto cleanup;
        }
    }

cleanup:

    return status;
}
```



## <a name="reading-events-from-the-result-set"></a><span data-ttu-id="f2496-118">Считывание событий из результирующего набора</span><span class="sxs-lookup"><span data-stu-id="f2496-118">Reading events from the result set</span></span>

<span data-ttu-id="f2496-119">Чтобы перечислить события в результирующем наборе, вызовите функцию [**евтнекст**](/windows/desktop/api/WinEvt/nf-winevt-evtnext) в цикле до тех пор, пока функция не вернет **значение false** , а функция [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) вернет ошибку, что больше \_ нет \_ \_ элементов.</span><span class="sxs-lookup"><span data-stu-id="f2496-119">To enumerate the events in the result set, call the [**EvtNext**](/windows/desktop/api/WinEvt/nf-winevt-evtnext) function in a loop until the function returns **FALSE** and the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns ERROR\_NO\_MORE\_ITEMS.</span></span> <span data-ttu-id="f2496-120">События в результирующем наборе не являются статическими; новые события, записанные в канал, будут включены в результирующий набор до тех пор, пока не \_ \_ \_ будет задано значение ошибка.</span><span class="sxs-lookup"><span data-stu-id="f2496-120">The events in the result set are not static; new events that are written to the channel will be included in the result set until ERROR\_NO\_MORE\_ITEMS is set.</span></span> <span data-ttu-id="f2496-121">Чтобы повысить производительность, выберете события из результирующего набора в пакетах (принимая во внимание размер каждого события при определении количества событий для получения).</span><span class="sxs-lookup"><span data-stu-id="f2496-121">To improve performance, fetch events from the result set in batches (taking into account the size of each event when determining the number of events to fetch).</span></span>

<span data-ttu-id="f2496-122">В следующем примере показано, как перечислить события в результирующем наборе.</span><span class="sxs-lookup"><span data-stu-id="f2496-122">The following example shows how to enumerate the events in a result set.</span></span>


```C++
// Enumerate all the events in the result set. 
DWORD PrintResults(EVT_HANDLE hResults)
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
        // event for display. PrintEvent is shown in RenderingEvents.
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

    for (DWORD i = 0; i < dwReturned; i++)
    {
        if (NULL != hEvents[i])
            EvtClose(hEvents[i]);
    }

    return status;
}
```



<span data-ttu-id="f2496-123">Дополнительные сведения о визуализации событий, получаемых из результирующего набора, см. в разделе [Подготовка событий к просмотру](rendering-events.md).</span><span class="sxs-lookup"><span data-stu-id="f2496-123">For details on rendering the events that you get from the result set, see [Rendering Events](rendering-events.md).</span></span>

<span data-ttu-id="f2496-124">Если вы хотите запросить события с того места, где вы остановились, Создайте закладку последнего прочитанного события и используйте его при следующем выполнении запроса.</span><span class="sxs-lookup"><span data-stu-id="f2496-124">If you want to query for events from where you left off, create a bookmark of the last event that you read and use it the next time you run your query.</span></span> <span data-ttu-id="f2496-125">Дополнительные сведения см. в разделе [события закладок](bookmarking-events.md).</span><span class="sxs-lookup"><span data-stu-id="f2496-125">For details, see [Bookmarking Events](bookmarking-events.md).</span></span>

 

 