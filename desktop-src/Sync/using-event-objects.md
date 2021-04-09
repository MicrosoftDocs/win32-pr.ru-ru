---
description: Приложения могут использовать объекты событий в ряде случаев для уведомления ожидающего потока вхождения события.
ms.assetid: f3f455bb-7563-4920-a728-f75fa5854dc9
title: Использование объектов событий (синхронизация)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c0c7ee5f58b8359e989b19ffc9c016dd1a6593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910020"
---
# <a name="using-event-objects-synchronization"></a><span data-ttu-id="6f67e-103">Использование объектов событий (синхронизация)</span><span class="sxs-lookup"><span data-stu-id="6f67e-103">Using Event Objects (Synchronization)</span></span>

<span data-ttu-id="6f67e-104">Приложения могут использовать [объекты событий](event-objects.md) в ряде случаев для уведомления ожидающего потока вхождения события.</span><span class="sxs-lookup"><span data-stu-id="6f67e-104">Applications can use [event objects](event-objects.md) in a number of situations to notify a waiting thread of the occurrence of an event.</span></span> <span data-ttu-id="6f67e-105">Например, перекрывающиеся операции ввода-вывода для файлов, именованных каналов и устройств связи используют объект события для сигнализации их завершения.</span><span class="sxs-lookup"><span data-stu-id="6f67e-105">For example, overlapped I/O operations on files, named pipes, and communications devices use an event object to signal their completion.</span></span> <span data-ttu-id="6f67e-106">Дополнительные сведения об использовании объектов событий в перекрывающихся операциях ввода-вывода см. в разделе [Синхронизация и перекрывающиеся входные и выходные данные](synchronization-and-overlapped-input-and-output.md).</span><span class="sxs-lookup"><span data-stu-id="6f67e-106">For more information about the use of event objects in overlapped I/O operations, see [Synchronization and Overlapped Input and Output](synchronization-and-overlapped-input-and-output.md).</span></span>

<span data-ttu-id="6f67e-107">В следующем примере используются объекты событий, чтобы предотвратить чтение нескольких потоков из буфера общей памяти во время записи главным потоком в этот буфер.</span><span class="sxs-lookup"><span data-stu-id="6f67e-107">The following example uses event objects to prevent several threads from reading from a shared memory buffer while a master thread is writing to that buffer.</span></span> <span data-ttu-id="6f67e-108">Во-первых, главный поток использует функцию [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) для создания объекта события ручного сброса, исходное состояние которого не сигнальное.</span><span class="sxs-lookup"><span data-stu-id="6f67e-108">First, the master thread uses the [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) function to create a manual-reset event object whose initial state is nonsignaled.</span></span> <span data-ttu-id="6f67e-109">Затем создается несколько потоков чтения.</span><span class="sxs-lookup"><span data-stu-id="6f67e-109">Then it creates several reader threads.</span></span> <span data-ttu-id="6f67e-110">Главный поток выполняет операцию записи, а затем устанавливает объект события в сигнальное состояние по завершении записи.</span><span class="sxs-lookup"><span data-stu-id="6f67e-110">The master thread performs a write operation and then sets the event object to the signaled state when it has finished writing.</span></span>

<span data-ttu-id="6f67e-111">Перед началом операции чтения каждый поток чтения использует [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) для ожидания сигнала объекта события ручного сброса.</span><span class="sxs-lookup"><span data-stu-id="6f67e-111">Before starting a read operation, each reader thread uses [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) to wait for the manual-reset event object to be signaled.</span></span> <span data-ttu-id="6f67e-112">Когда функция **WaitForSingleObject** возвращает, это означает, что основной поток готов для начала операции чтения.</span><span class="sxs-lookup"><span data-stu-id="6f67e-112">When **WaitForSingleObject** returns, this indicates that the main thread is ready for it to begin its read operation.</span></span>


```C++
#include <windows.h>
#include <stdio.h>

#define THREADCOUNT 4 

HANDLE ghWriteEvent; 
HANDLE ghThreads[THREADCOUNT];

DWORD WINAPI ThreadProc(LPVOID);

void CreateEventsAndThreads(void) 
{
    int i; 
    DWORD dwThreadID; 

    // Create a manual-reset event object. The write thread sets this
    // object to the signaled state when it finishes writing to a 
    // shared buffer. 

    ghWriteEvent = CreateEvent( 
        NULL,               // default security attributes
        TRUE,               // manual-reset event
        FALSE,              // initial state is nonsignaled
        TEXT("WriteEvent")  // object name
        ); 

    if (ghWriteEvent == NULL) 
    { 
        printf("CreateEvent failed (%d)\n", GetLastError());
        return;
    }

    // Create multiple threads to read from the buffer.

    for(i = 0; i < THREADCOUNT; i++) 
    {
        // TODO: More complex scenarios may require use of a parameter
        //   to the thread procedure, such as an event per thread to  
        //   be used for synchronization.
        ghThreads[i] = CreateThread(
            NULL,              // default security
            0,                 // default stack size
            ThreadProc,        // name of the thread function
            NULL,              // no thread parameters
            0,                 // default startup flags
            &dwThreadID); 

        if (ghThreads[i] == NULL) 
        {
            printf("CreateThread failed (%d)\n", GetLastError());
            return;
        }
    }
}

void WriteToBuffer(VOID) 
{
    // TODO: Write to the shared buffer.
    
    printf("Main thread writing to the shared buffer...\n");

    // Set ghWriteEvent to signaled

    if (! SetEvent(ghWriteEvent) ) 
    {
        printf("SetEvent failed (%d)\n", GetLastError());
        return;
    }
}

void CloseEvents()
{
    // Close all event handles (currently, only one global handle).
    
    CloseHandle(ghWriteEvent);
}

int main( void )
{
    DWORD dwWaitResult;

    // TODO: Create the shared buffer

    // Create events and THREADCOUNT threads to read from the buffer

    CreateEventsAndThreads();

    // At this point, the reader threads have started and are most
    // likely waiting for the global event to be signaled. However, 
    // it is safe to write to the buffer because the event is a 
    // manual-reset event.
    
    WriteToBuffer();

    printf("Main thread waiting for threads to exit...\n");

    // The handle for each thread is signaled when the thread is
    // terminated.
    dwWaitResult = WaitForMultipleObjects(
        THREADCOUNT,   // number of handles in array
        ghThreads,     // array of thread handles
        TRUE,          // wait until all are signaled
        INFINITE);

    switch (dwWaitResult) 
    {
        // All thread objects were signaled
        case WAIT_OBJECT_0: 
            printf("All threads ended, cleaning up for application exit...\n");
            break;

        // An error occurred
        default: 
            printf("WaitForMultipleObjects failed (%d)\n", GetLastError());
            return 1;
    } 
            
    // Close the events to clean up

    CloseEvents();

    return 0;
}

DWORD WINAPI ThreadProc(LPVOID lpParam) 
{
    // lpParam not used in this example.
    UNREFERENCED_PARAMETER(lpParam);

    DWORD dwWaitResult;

    printf("Thread %d waiting for write event...\n", GetCurrentThreadId());
    
    dwWaitResult = WaitForSingleObject( 
        ghWriteEvent, // event handle
        INFINITE);    // indefinite wait

    switch (dwWaitResult) 
    {
        // Event object was signaled
        case WAIT_OBJECT_0: 
            //
            // TODO: Read from the shared buffer
            //
            printf("Thread %d reading from buffer\n", 
                   GetCurrentThreadId());
            break; 

        // An error occurred
        default: 
            printf("Wait error (%d)\n", GetLastError()); 
            return 0; 
    }

    // Now that we are done reading the buffer, we could use another
    // event to signal that this thread is no longer reading. This
    // example simply uses the thread handle for synchronization (the
    // handle is signaled when the thread terminates.)

    printf("Thread %d exiting\n", GetCurrentThreadId());
    return 1;
}

```



 

 
