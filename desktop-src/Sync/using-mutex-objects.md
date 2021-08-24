---
description: Объект Mutex можно использовать для защиты общего ресурса от одновременного доступа несколькими потоками или процессами.
ms.assetid: 0f69ba50-69ce-467a-b068-8fd8f07c6c78
title: Использование объектов Mutex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c629d90e1cd811c62f62e1151cee4c3e2af77b84133e142fcfe7f93a35b2e5bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739264"
---
# <a name="using-mutex-objects"></a>Использование объектов Mutex

[Объект Mutex](mutex-objects.md) можно использовать для защиты общего ресурса от одновременного доступа несколькими потоками или процессами. Каждый поток должен ожидать владения мьютексом, прежде чем он сможет выполнить код, обращающийся к общему ресурсу. Например, если несколько потоков совместно используют доступ к базе данных, потоки могут использовать объект Mutex, чтобы позволить только одному потоку одновременно выполнять запись в базу данных.

В следующем примере функция [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) используется для создания объекта мьютекса и функции [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) для создания рабочих потоков.

Когда поток этого процесса записывает в базу данных, он сначала запрашивает владение мьютексом с помощью функции [**WaitForSingleObject**](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) . Если поток получает владение мьютексом, он записывает данные в базу данных, а затем освобождает владение мьютексом с помощью функции [**ReleaseMutex**](/windows/win32/api/synchapi/nf-synchapi-releasemutex) .

В этом примере используется структурированная обработка исключений, чтобы убедиться, что поток правильно освобождает объект Mutex. Блок кода **\_ \_ finally** выполняется независимо от того, как завершается блок **\_ \_ try** (если блок **\_ \_ try** не включает вызов функции [**TerminateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminatethread) ). Это предотвращает непреднамеренное прекращение объекта мьютекса.

Если мьютекс отброшен, поток, владеющий мьютексом, не освободил его должным образом перед завершением. В этом случае состояние общего ресурса является неопределенным, и продолжение использования мьютекса может скрыть потенциально серьезную ошибку. Некоторые приложения могут попытаться восстановить состояние ресурса до стабильного состояния. в этом примере просто возвращается ошибка и прекращается использование мьютекса. Дополнительные сведения см. в разделе [объекты мьютекса](mutex-objects.md).


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



 

 
