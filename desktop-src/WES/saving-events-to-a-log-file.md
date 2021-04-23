---
title: Сохранение событий в файл журнала
description: Чтобы сохранить события из канала в файл журнала, вызовите функцию Евтклеарлог или Евтекспортлог.
ms.assetid: 6d71ed15-97e3-4888-b161-c7e31bf3fc6d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3295d8a7a235fbb5fd5857d1b7283e9ca1fbb773
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258863"
---
# <a name="saving-events-to-a-log-file"></a><span data-ttu-id="70a45-103">Сохранение событий в файл журнала</span><span class="sxs-lookup"><span data-stu-id="70a45-103">Saving Events to a Log File</span></span>

<span data-ttu-id="70a45-104">Чтобы сохранить события из канала в файл журнала, вызовите функцию [**евтклеарлог**](/windows/desktop/api/WinEvt/nf-winevt-evtclearlog) или [**евтекспортлог**](/windows/desktop/api/WinEvt/nf-winevt-evtexportlog) .</span><span class="sxs-lookup"><span data-stu-id="70a45-104">To save events from a channel to a log file, call the [**EvtClearLog**](/windows/desktop/api/WinEvt/nf-winevt-evtclearlog) or [**EvtExportLog**](/windows/desktop/api/WinEvt/nf-winevt-evtexportlog) function.</span></span> <span data-ttu-id="70a45-105">Функция [**евтклеарлог**](/windows/desktop/api/WinEvt/nf-winevt-evtclearlog) копирует события в файл журнала и удаляет их из канала.</span><span class="sxs-lookup"><span data-stu-id="70a45-105">The [**EvtClearLog**](/windows/desktop/api/WinEvt/nf-winevt-evtclearlog) function copies the events to the log file and deletes them from the channel.</span></span> <span data-ttu-id="70a45-106">Функция [**евтекспортлог**](/windows/desktop/api/WinEvt/nf-winevt-evtexportlog) также копирует события в файл журнала, но не удаляет их из канала.</span><span class="sxs-lookup"><span data-stu-id="70a45-106">The [**EvtExportLog**](/windows/desktop/api/WinEvt/nf-winevt-evtexportlog) function also copies the events to the log file but does not delete them from the channel.</span></span> <span data-ttu-id="70a45-107">Чтобы очистить канал, пользователь должен иметь разрешения на чтение и очистку.</span><span class="sxs-lookup"><span data-stu-id="70a45-107">To clear a channel, the user must have Read and Clear permissions.</span></span>

<span data-ttu-id="70a45-108">Вы можете запрашивать события из созданного файла журнала. Однако для отображения событий поставщик должен быть зарегистрирован на компьютере.</span><span class="sxs-lookup"><span data-stu-id="70a45-108">You can query events from the log file that you created; however, to render the events, the provider must be registered on the computer.</span></span> <span data-ttu-id="70a45-109">Чтобы отобразить события из файла журнала, если поставщик не зарегистрирован на компьютере, необходимо вызвать [**евтарчивикспортедлог**](/windows/desktop/api/WinEvt/nf-winevt-evtarchiveexportedlog), который копирует ресурсы из поставщика и добавляет их в файл журнала.</span><span class="sxs-lookup"><span data-stu-id="70a45-109">To render events from a log file when the provider is not registered on the computer, you must call the [**EvtArchiveExportedLog**](/windows/desktop/api/WinEvt/nf-winevt-evtarchiveexportedlog), which copies the resources from the provider and adds them to the log file.</span></span> <span data-ttu-id="70a45-110">Затем можно скопировать файл журнала на любой компьютер и успешно запрашивать и подготавливать события.</span><span class="sxs-lookup"><span data-stu-id="70a45-110">You can then copy the log file to any computer and successfully query and render its events.</span></span>

<span data-ttu-id="70a45-111">Кроме использования [**евтекспортлог**](/windows/desktop/api/WinEvt/nf-winevt-evtexportlog) для копирования событий из канала, его также можно использовать для регистрации событий из одного файла журнала в другой.</span><span class="sxs-lookup"><span data-stu-id="70a45-111">In addition to using [**EvtExportLog**](/windows/desktop/api/WinEvt/nf-winevt-evtexportlog) to copy events from a channel, you can also use it to relog events from one log file to another log file.</span></span> <span data-ttu-id="70a45-112">Его также можно использовать для слияния событий из нескольких каналов, если используется структурированный XML-запрос, но его нельзя использовать для слияния событий из нескольких файлов журнала.</span><span class="sxs-lookup"><span data-stu-id="70a45-112">You can also use it to merge events from multiple channels if you use a structured XML query but you cannot use it to merge events from multiple log files.</span></span>

<span data-ttu-id="70a45-113">В следующем примере показано, как копировать события из канала в файл журнала.</span><span class="sxs-lookup"><span data-stu-id="70a45-113">The following example shows how to copy events from a channel to a log file.</span></span> <span data-ttu-id="70a45-114">Затем в примере повторно записываются определенные события из вновь созданного файла журнала в новый файл журнала.</span><span class="sxs-lookup"><span data-stu-id="70a45-114">The example then relogs specific events from the newly created log file to a new log file.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <winevt.h>

#pragma comment(lib, "wevtapi.lib")

#define ARRAY_SIZE 10

DWORD DumpEvents(LPCWSTR pwsLogFile);
DWORD PrintResults(EVT_HANDLE hResults);
DWORD PrintEvent(EVT_HANDLE hEvent);

void main(void)
{
    DWORD status = ERROR_SUCCESS;
    LPWSTR pPath = L"<path to channel goes here>";
    LPWSTR pQuery = NULL;
    LPWSTR pTargetLogFile = L".\\log.evtx";

    // Export all the events in the specified channel to the target log file.
    if (!EvtExportLog(NULL, pPath, pQuery, pTargetLogFile, EvtExportLogChannelPath))
    {
        wprintf(L"EvtExportLog failed for initial export with %lu.\n", GetLastError());
        goto cleanup;
    }

    // Dump the events from the log file.
    wprintf(L"Events from %s log file\n\n", pTargetLogFile);
    DumpEvents(pTargetLogFile);

    // Create a new log file that will contain all events from the specified 
    // log file where the event ID is 2.
    pPath =  L".\\log.evtx";
    pQuery = L"Event/System[EventID=2]";
    pTargetLogFile = L".\\log2.evtx";

    // Export all events from the specified log file that have an ID of 2 and
    // write them to a new log file.
    if (!EvtExportLog(NULL, pPath, pQuery, pTargetLogFile, EvtExportLogFilePath))
    {
        wprintf(L"EvtExportLog failed for relog with %lu.\n", GetLastError());
        goto cleanup;
    }

    // Dump the events from the log file.
    wprintf(L"\n\n\nEvents from %s log file\n\n", pTargetLogFile);
    DumpEvents(pTargetLogFile);

cleanup:

    return;
}


// Dump all the events in the from the log file.
DWORD DumpEvents(LPCWSTR pwsPath)
{
    EVT_HANDLE hResults = NULL;
    DWORD status = ERROR_SUCCESS;

    hResults = EvtQuery(NULL, pwsPath, NULL, EvtQueryFilePath);
    if (NULL == hResults)
    {
        wprintf(L"EvtQuery failed with %lu.\n", status = GetLastError());
        goto cleanup;
    }

    status = PrintResults(hResults);

cleanup:

    if (hResults)
        EvtClose(hResults);

    return status;
}


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

    // Executed only if there was an error.
    for (DWORD i = 0; i < dwReturned; i++)
    {
        if (NULL != hEvents[i])
            EvtClose(hEvents[i]);
    }

    return status;
}


// Print the event as an XML string.
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
```



<span data-ttu-id="70a45-115">В следующем примере показано, как выполнить слияние события из нескольких каналов с помощью структурированного XML-запроса.</span><span class="sxs-lookup"><span data-stu-id="70a45-115">The following example shows how to merge event from multiple channels using a structured XML query.</span></span> <span data-ttu-id="70a45-116">Пример заменяет основную процедуру из предыдущего примера.</span><span class="sxs-lookup"><span data-stu-id="70a45-116">The example replaces the main procedure from the previous example.</span></span>


```C++
void main(void)
{
    DWORD status = ERROR_SUCCESS;
    LPWSTR pTargetLogFile = L".\\log.evtx";
    LPWSTR pQuery = L"<QueryList>"
                    L"  <Query Id='0'>"
                    L"    <Select Path='<path to channel goes here>'>*</Select>"
                    L"  </Query>"
                    L"  <Query Id='1'>"
                    L"    <Select Path='<path to channel goes here>'>*</Select>"
                    L"  </Query>"
                    L"</QueryList>";

    if (!EvtExportLog(NULL, NULL, pQuery, pTargetLogFile, EvtExportLogChannelPath)) 
    {
        wprintf(L"EvtExportLog failed with %lu.\n", GetLastError());
        goto cleanup;
    }

    wprintf(L"Events from %s log file\n\n", pTargetLogFile);
    DumpEvents(pTargetLogFile);

cleanup:

    return;
}
```



 

 




