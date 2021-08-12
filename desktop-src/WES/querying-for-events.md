---
title: Запрос событий
description: Можно запросить события из канала или файла журнала.
ms.assetid: 929bedbf-6dce-428e-b2c0-de9dcfe4531b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 981e4a8c39daebbce641c79e7d26331b9b36845d3c71fd1902ea667ca85c5dbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118587805"
---
# <a name="querying-for-events"></a>Запрос событий

Можно запросить события из канала или файла журнала. Канал или файл журнала может находиться на локальном или удаленном компьютере. Чтобы указать события, которые необходимо получить из канала или файла журнала, используйте запрос XPath или XML-запрос структуры. Дополнительные сведения о написании запроса см. в разделе [Использование событий](consuming-events.md).

Чтобы запросить события, вызовите функцию [**евткуери**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) . Можно указать порядок, в котором будут возвращаться события (от старых к новым (по умолчанию) или от новых к старым), а также следует ли допускать некорректные выражения XPath в запросе (Дополнительные сведения о том, как функция пропускает неверно сформированные выражения, см. в разделе флаг [**евткуеритолератекуереррорс**](/windows/desktop/api/WinEvt/ne-winevt-evt_query_flags) ).

В следующем примере показано, как запрашивать события из канала с помощью выражения XPath.


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



В следующем примере показано, как запрашивать события из канала с помощью структурированного XML-запроса. События возвращаются в порядке от новых к старым.


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



Если вы используете структурированный XML-запрос и передаете флаг Евткуеритолератекуереррорс в [**евткуери**](/windows/desktop/api/WinEvt/nf-winevt-evtquery), функция выполняется успешно, даже если один или несколько запросов в структурированном запросе могут быть действительно неудачными. Чтобы определить, какие запросы в структурированном запросе завершились успешно или с ошибкой, вызовите функцию [**евтжеткуеринфо**](/windows/desktop/api/WinEvt/nf-winevt-evtgetqueryinfo) . Если не передать флаг Евткуеритолератекуереррорс, функция **евткуери** завершится с первой ошибкой, найденной в запросе. Если запрос завершается с ошибкой \_ " \_ Недопустимый \_ запрос", вызовите функцию [**евтжетекстендедстатус**](/windows/desktop/api/WinEvt/nf-winevt-evtgetextendedstatus) , чтобы получить строку сообщения, описывающую ошибку XPath.

В следующем примере показано, как определить успешность или сбой каждого запроса в структурированном запросе при передаче флага Евткуеритолератекуереррорс в [**евткуери**](/windows/desktop/api/WinEvt/nf-winevt-evtquery).


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



## <a name="reading-events-from-the-result-set"></a>Считывание событий из результирующего набора

Чтобы перечислить события в результирующем наборе, вызовите функцию [**евтнекст**](/windows/desktop/api/WinEvt/nf-winevt-evtnext) в цикле до тех пор, пока функция не вернет **значение false** , а функция [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) вернет ошибку, что больше \_ нет \_ \_ элементов. События в результирующем наборе не являются статическими; новые события, записанные в канал, будут включены в результирующий набор до тех пор, пока не \_ \_ \_ будет задано значение ошибка. Чтобы повысить производительность, выберете события из результирующего набора в пакетах (принимая во внимание размер каждого события при определении количества событий для получения).

В следующем примере показано, как перечислить события в результирующем наборе.


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



Дополнительные сведения о визуализации событий, получаемых из результирующего набора, см. в разделе [Подготовка событий к просмотру](rendering-events.md).

Если вы хотите запросить события с того места, где вы остановились, Создайте закладку последнего прочитанного события и используйте его при следующем выполнении запроса. Дополнительные сведения см. в разделе [события закладок](bookmarking-events.md).

 

 