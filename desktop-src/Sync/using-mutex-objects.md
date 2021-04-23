---
description: Объект Mutex можно использовать для защиты общего ресурса от одновременного доступа несколькими потоками или процессами.
ms.assetid: 0f69ba50-69ce-467a-b068-8fd8f07c6c78
title: Использование объектов Mutex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbd68f41319125613e8569e7b343c0b1601a7735
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663408"
---
# <a name="using-mutex-objects"></a><span data-ttu-id="1b78e-103">Использование объектов Mutex</span><span class="sxs-lookup"><span data-stu-id="1b78e-103">Using Mutex Objects</span></span>

<span data-ttu-id="1b78e-104">[Объект Mutex](mutex-objects.md) можно использовать для защиты общего ресурса от одновременного доступа несколькими потоками или процессами.</span><span class="sxs-lookup"><span data-stu-id="1b78e-104">You can use a [mutex object](mutex-objects.md) to protect a shared resource from simultaneous access by multiple threads or processes.</span></span> <span data-ttu-id="1b78e-105">Каждый поток должен ожидать владения мьютексом, прежде чем он сможет выполнить код, обращающийся к общему ресурсу.</span><span class="sxs-lookup"><span data-stu-id="1b78e-105">Each thread must wait for ownership of the mutex before it can execute the code that accesses the shared resource.</span></span> <span data-ttu-id="1b78e-106">Например, если несколько потоков совместно используют доступ к базе данных, потоки могут использовать объект Mutex, чтобы позволить только одному потоку одновременно выполнять запись в базу данных.</span><span class="sxs-lookup"><span data-stu-id="1b78e-106">For example, if several threads share access to a database, the threads can use a mutex object to permit only one thread at a time to write to the database.</span></span>

<span data-ttu-id="1b78e-107">В следующем примере функция [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) используется для создания объекта мьютекса и функции [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) для создания рабочих потоков.</span><span class="sxs-lookup"><span data-stu-id="1b78e-107">The following example uses the [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) function to create a mutex object and the [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) function to create worker threads.</span></span>

<span data-ttu-id="1b78e-108">Когда поток этого процесса записывает в базу данных, он сначала запрашивает владение мьютексом с помощью функции [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) .</span><span class="sxs-lookup"><span data-stu-id="1b78e-108">When a thread of this process writes to the database, it first requests ownership of the mutex using the [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) function.</span></span> <span data-ttu-id="1b78e-109">Если поток получает владение мьютексом, он записывает данные в базу данных, а затем освобождает владение мьютексом с помощью функции [**ReleaseMutex**](/windows/win32/api/synchapi/nf-synchapi-releasemutex) .</span><span class="sxs-lookup"><span data-stu-id="1b78e-109">If the thread obtains ownership of the mutex, it writes to the database and then releases its ownership of the mutex using the [**ReleaseMutex**](/windows/win32/api/synchapi/nf-synchapi-releasemutex) function.</span></span>

<span data-ttu-id="1b78e-110">В этом примере используется структурированная обработка исключений, чтобы убедиться, что поток правильно освобождает объект Mutex.</span><span class="sxs-lookup"><span data-stu-id="1b78e-110">This example uses structured exception handling to ensure that the thread properly releases the mutex object.</span></span> <span data-ttu-id="1b78e-111">Блок кода **\_ \_ finally** выполняется независимо от того, как завершается блок **\_ \_ try** (если блок **\_ \_ try** не включает вызов функции [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) ).</span><span class="sxs-lookup"><span data-stu-id="1b78e-111">The **\_\_finally** block of code is executed no matter how the **\_\_try** block terminates (unless the **\_\_try** block includes a call to the [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) function).</span></span> <span data-ttu-id="1b78e-112">Это предотвращает непреднамеренное прекращение объекта мьютекса.</span><span class="sxs-lookup"><span data-stu-id="1b78e-112">This prevents the mutex object from being abandoned inadvertently.</span></span>

<span data-ttu-id="1b78e-113">Если мьютекс отброшен, поток, владеющий мьютексом, не освободил его должным образом перед завершением.</span><span class="sxs-lookup"><span data-stu-id="1b78e-113">If a mutex is abandoned, the thread that owned the mutex did not properly release it before terminating.</span></span> <span data-ttu-id="1b78e-114">В этом случае состояние общего ресурса является неопределенным, и продолжение использования мьютекса может скрыть потенциально серьезную ошибку.</span><span class="sxs-lookup"><span data-stu-id="1b78e-114">In this case, the status of the shared resource is indeterminate, and continuing to use the mutex can obscure a potentially serious error.</span></span> <span data-ttu-id="1b78e-115">Некоторые приложения могут попытаться восстановить состояние ресурса до стабильного состояния. в этом примере просто возвращается ошибка и прекращается использование мьютекса.</span><span class="sxs-lookup"><span data-stu-id="1b78e-115">Some applications might attempt to restore the resource to a consistent state; this example simply returns an error and stops using the mutex.</span></span> <span data-ttu-id="1b78e-116">Дополнительные сведения см. в разделе [объекты мьютекса](mutex-objects.md).</span><span class="sxs-lookup"><span data-stu-id="1b78e-116">For more information, see [Mutex Objects](mutex-objects.md).</span></span>


```C++
#include <windows.h>
#include <stdio.h>

#define THREADCOUNT 2

HANDLE ghMutex; 

DWORD WINAPI WriteToDatabase( LPVOID );

int main( void )
{
    HANDLE aThread[THREADCOUNT];
    DWORD ThreadID;
    int i;

    // Create a mutex with no initial owner

    ghMutex = CreateMutex( 
        NULL,              // default security attributes
        FALSE,             // initially not owned
        NULL);             // unnamed mutex

    if (ghMutex == NULL) 
    {
        printf("CreateMutex error: %d\n", GetLastError());
        return 1;
    }

    // Create worker threads

    for( i=0; i < THREADCOUNT; i++ )
    {
        aThread[i] = CreateThread( 
                     NULL,       // default security attributes
                     0,          // default stack size
                     (LPTHREAD_START_ROUTINE) WriteToDatabase, 
                     NULL,       // no thread function arguments
                     0,          // default creation flags
                     &ThreadID); // receive thread identifier

        if( aThread[i] == NULL )
        {
            printf("CreateThread error: %d\n", GetLastError());
            return 1;
        }
    }

    // Wait for all threads to terminate

    WaitForMultipleObjects(THREADCOUNT, aThread, TRUE, INFINITE);

    // Close thread and mutex handles

    for( i=0; i < THREADCOUNT; i++ )
        CloseHandle(aThread[i]);

    CloseHandle(ghMutex);

    return 0;
}

DWORD WINAPI WriteToDatabase( LPVOID lpParam )
{ 
    // lpParam not used in this example
    UNREFERENCED_PARAMETER(lpParam);

    DWORD dwCount=0, dwWaitResult; 

    // Request ownership of mutex.

    while( dwCount < 20 )
    { 
        dwWaitResult = WaitForSingleObject( 
            ghMutex,    // handle to mutex
            INFINITE);  // no time-out interval
 
        switch (dwWaitResult) 
        {
            // The thread got ownership of the mutex
            case WAIT_OBJECT_0: 
                __try { 
                    // TODO: Write to the database
                    printf("Thread %d writing to database...\n", 
                            GetCurrentThreadId());
                    dwCount++;
                } 

                __finally { 
                    // Release ownership of the mutex object
                    if (! ReleaseMutex(ghMutex)) 
                    { 
                        // Handle error.
                    } 
                } 
                break; 

            // The thread got ownership of an abandoned mutex
            // The database is in an indeterminate state
            case WAIT_ABANDONED: 
                return FALSE; 
        }
    }
    return TRUE; 
}
```



 

 
