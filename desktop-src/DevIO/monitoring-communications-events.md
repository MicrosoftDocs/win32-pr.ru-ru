---
description: В следующем примере кода открывается последовательный порт для перекрывающихся операций ввода-вывода, создается маска событий для мониторинга сигналов CTS и DSR, а затем ожидается возникновение события.
ms.assetid: 23ebcb04-1571-4e93-a549-46ad6b9d4272
title: Мониторинг событий связи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5eac453b7f864f4f0b5fc756b1ffc6a730e2769
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655855"
---
# <a name="monitoring-communications-events"></a><span data-ttu-id="14de9-103">Мониторинг событий связи</span><span class="sxs-lookup"><span data-stu-id="14de9-103">Monitoring Communications Events</span></span>

<span data-ttu-id="14de9-104">В следующем примере кода открывается последовательный порт для перекрывающихся операций ввода-вывода, создается маска событий для мониторинга сигналов CTS и DSR, а затем ожидается возникновение события.</span><span class="sxs-lookup"><span data-stu-id="14de9-104">The following example code opens the serial port for overlapped I/O, creates an event mask to monitor CTS and DSR signals, and then waits for an event to occur.</span></span> <span data-ttu-id="14de9-105">Функция [**ваиткоммевент**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) должна выполняться как перекрывающаяся операция, чтобы другие потоки процесса могли выполнять операции ввода-вывода в течение ожидания.</span><span class="sxs-lookup"><span data-stu-id="14de9-105">The [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) function should be executed as an overlapped operation so the other threads of the process can perform I/O operations during the wait.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <assert.h>
#include <stdio.h>

void _tmain(
            int argc, 
            TCHAR *argv[]
           )
{
    HANDLE hCom;
    OVERLAPPED o;
    BOOL fSuccess;
    DWORD dwEvtMask;

    hCom = CreateFile( TEXT("\\\\.\\COM1"),
        GENERIC_READ | GENERIC_WRITE,
        0,    // exclusive access 
        NULL, // default security attributes 
        OPEN_EXISTING,
        FILE_FLAG_OVERLAPPED,
        NULL 
        );

    if (hCom == INVALID_HANDLE_VALUE) 
    {
        // Handle the error. 
        printf("CreateFile failed with error %d.\n", GetLastError());
        return;
    }

    // Set the event mask. 

    fSuccess = SetCommMask(hCom, EV_CTS | EV_DSR);

    if (!fSuccess) 
    {
        // Handle the error. 
        printf("SetCommMask failed with error %d.\n", GetLastError());
        return;
    }

    // Create an event object for use by WaitCommEvent. 

    o.hEvent = CreateEvent(
        NULL,   // default security attributes 
        TRUE,   // manual-reset event 
        FALSE,  // not signaled 
        NULL    // no name
         );
    

    // Initialize the rest of the OVERLAPPED structure to zero.
    o.Internal = 0;
    o.InternalHigh = 0;
    o.Offset = 0;
    o.OffsetHigh = 0;

    assert(o.hEvent);

    if (WaitCommEvent(hCom, &dwEvtMask, &o)) 
    {
        if (dwEvtMask & EV_DSR) 
        {
             // To do.
        }

        if (dwEvtMask & EV_CTS) 
        {
            // To do. 
        }
    }
    else
    {
        DWORD dwRet = GetLastError();
        if( ERROR_IO_PENDING == dwRet)
        {
            printf("I/O is pending...\n");

            // To do.
        }
        else 
            printf("Wait failed with error %d.\n", GetLastError());
    }
}
```



 

 



