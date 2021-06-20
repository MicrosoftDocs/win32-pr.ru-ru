---
description: Узнайте, как использовать функцию CreateThread для создания нового потока для процесса. Изучите пример кода, демонстрирующий его использование.
ms.assetid: eb0cc3c0-14f2-4913-a592-4ba3eaf67002
title: Создание потоков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: befd6c00cadb6758d076ad6c4d0fe940cf855f89
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406737"
---
# <a name="creating-threads"></a>Создание потоков

Функция [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) создает новый поток для процесса. В создаваемом потоке должен быть указан начальный адрес кода, который будет выполняться новым потоком. Как правило, начальный адрес — это имя функции, определенной в программном коде (Дополнительные сведения см. в разделе [*среадпрок*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85))). Эта функция принимает один параметр и возвращает значение **типа DWORD** . Процесс может иметь несколько потоков, одновременно выполняющих одну и ту же функцию.

Ниже приведен простой пример, демонстрирующий создание нового потока, выполняющего локально определенную функцию `MyThreadFunction` .

Вызывающий поток использует функцию [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) для сохранения до завершения всех рабочих потоков. Вызывающий поток блокируется в ожидании; чтобы продолжить обработку, вызывающий поток будет использовать [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) и ждет, пока каждый рабочий поток сообщит свой объект ожидания. Обратите внимание, что если бы вы закрыли обработчик до конца рабочего потока, это не завершит рабочий поток. Однако этот маркер будет недоступен для использования в последующих вызовах функций.


```C++
#include <windows.h>
#include <tchar.h>
#include <strsafe.h>

#define MAX_THREADS 3
#define BUF_SIZE 255

DWORD WINAPI MyThreadFunction( LPVOID lpParam );
void ErrorHandler(LPTSTR lpszFunction);

// Sample custom data structure for threads to use.
// This is passed by void pointer so it can be any data type
// that can be passed using a single void pointer (LPVOID).
typedef struct MyData {
    int val1;
    int val2;
} MYDATA, *PMYDATA;


int _tmain()
{
    PMYDATA pDataArray[MAX_THREADS];
    DWORD   dwThreadIdArray[MAX_THREADS];
    HANDLE  hThreadArray[MAX_THREADS]; 

    // Create MAX_THREADS worker threads.

    for( int i=0; i<MAX_THREADS; i++ )
    {
        // Allocate memory for thread data.

        pDataArray[i] = (PMYDATA) HeapAlloc(GetProcessHeap(), HEAP_ZERO_MEMORY,
                sizeof(MYDATA));

        if( pDataArray[i] == NULL )
        {
           // If the array allocation fails, the system is out of memory
           // so there is no point in trying to print an error message.
           // Just terminate execution.
            ExitProcess(2);
        }

        // Generate unique data for each thread to work with.

        pDataArray[i]->val1 = i;
        pDataArray[i]->val2 = i+100;

        // Create the thread to begin execution on its own.

        hThreadArray[i] = CreateThread( 
            NULL,                   // default security attributes
            0,                      // use default stack size  
            MyThreadFunction,       // thread function name
            pDataArray[i],          // argument to thread function 
            0,                      // use default creation flags 
            &dwThreadIdArray[i]);   // returns the thread identifier 


        // Check the return value for success.
        // If CreateThread fails, terminate execution. 
        // This will automatically clean up threads and memory. 

        if (hThreadArray[i] == NULL) 
        {
           ErrorHandler(TEXT("CreateThread"));
           ExitProcess(3);
        }
    } // End of main thread creation loop.

    // Wait until all threads have terminated.

    WaitForMultipleObjects(MAX_THREADS, hThreadArray, TRUE, INFINITE);

    // Close all thread handles and free memory allocations.

    for(int i=0; i<MAX_THREADS; i++)
    {
        CloseHandle(hThreadArray[i]);
        if(pDataArray[i] != NULL)
        {
            HeapFree(GetProcessHeap(), 0, pDataArray[i]);
            pDataArray[i] = NULL;    // Ensure address is not reused.
        }
    }

    return 0;
}


DWORD WINAPI MyThreadFunction( LPVOID lpParam ) 
{ 
    HANDLE hStdout;
    PMYDATA pDataArray;

    TCHAR msgBuf[BUF_SIZE];
    size_t cchStringSize;
    DWORD dwChars;

    // Make sure there is a console to receive output results. 

    hStdout = GetStdHandle(STD_OUTPUT_HANDLE);
    if( hStdout == INVALID_HANDLE_VALUE )
        return 1;

    // Cast the parameter to the correct data type.
    // The pointer is known to be valid because 
    // it was checked for NULL before the thread was created.
 
    pDataArray = (PMYDATA)lpParam;

    // Print the parameter values using thread-safe functions.

    StringCchPrintf(msgBuf, BUF_SIZE, TEXT("Parameters = %d, %d\n"), 
        pDataArray->val1, pDataArray->val2); 
    StringCchLength(msgBuf, BUF_SIZE, &cchStringSize);
    WriteConsole(hStdout, msgBuf, (DWORD)cchStringSize, &dwChars, NULL);

    return 0; 
} 



void ErrorHandler(LPTSTR lpszFunction) 
{ 
    // Retrieve the system error message for the last-error code.

    LPVOID lpMsgBuf;
    LPVOID lpDisplayBuf;
    DWORD dw = GetLastError(); 

    FormatMessage(
        FORMAT_MESSAGE_ALLOCATE_BUFFER | 
        FORMAT_MESSAGE_FROM_SYSTEM |
        FORMAT_MESSAGE_IGNORE_INSERTS,
        NULL,
        dw,
        MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT),
        (LPTSTR) &lpMsgBuf,
        0, NULL );

    // Display the error message.

    lpDisplayBuf = (LPVOID)LocalAlloc(LMEM_ZEROINIT, 
        (lstrlen((LPCTSTR) lpMsgBuf) + lstrlen((LPCTSTR) lpszFunction) + 40) * sizeof(TCHAR)); 
    StringCchPrintf((LPTSTR)lpDisplayBuf, 
        LocalSize(lpDisplayBuf) / sizeof(TCHAR),
        TEXT("%s failed with error %d: %s"), 
        lpszFunction, dw, lpMsgBuf); 
    MessageBox(NULL, (LPCTSTR) lpDisplayBuf, TEXT("Error"), MB_OK); 

    // Free error-handling buffer allocations.

    LocalFree(lpMsgBuf);
    LocalFree(lpDisplayBuf);
}
```



`MyThreadFunction`Функция позволяет избежать использования библиотеки времени выполнения C (CRT), так как многие ее функции не являются потокобезопасными, особенно если не используется многопоточный CRT. Если вы хотите использовать CRT в `ThreadProc` функции, используйте вместо этого функцию **\_ бегинсреадекс** .

При завершении создания потока до нового потока рискованно передавать адрес локальной переменной, так как указатель становится недопустимым. Вместо этого либо передайте указатель на динамически выделяемую память, либо создайте поток, ожидающий завершения нового потока. Данные также могут передаваться из создания потока в новый поток с помощью глобальных переменных. При использовании глобальных переменных обычно требуется синхронизация доступа по нескольким потокам. Дополнительные сведения о синхронизации см. в разделе [Синхронизация выполнения нескольких потоков](synchronizing-execution-of-multiple-threads.md).

Создание потока может использовать аргументы для [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) , чтобы указать следующее:

-   Атрибуты безопасности для этого маркера для нового потока. Эти атрибуты безопасности включают флаг наследования, определяющий, может ли этот маркер наследоваться дочерними процессами. Атрибуты безопасности также включают в себя дескриптор безопасности, который система использует для выполнения проверок доступа во всех последующих применениях дескриптора потока до предоставления доступа.
-   Начальный размер стека нового потока. Стек потока выделяется автоматически в области памяти процесса; система увеличивает стек по мере необходимости и освобождает ее после завершения потока. Дополнительные сведения см. в разделе [размер стека потока](thread-stack-size.md).
-   Флаг создания, позволяющий создать поток в приостановленном состоянии. При приостановке поток не выполняется до тех пор, пока не будет вызвана функция [**ресумесреад**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) .

Вы также можете создать поток, вызвав функцию [**креатеремотесреад**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) . Эта функция используется процессами отладчика для создания потока, выполняемого в адресном пространстве отлаживаемого процесса.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Завершение потока](terminating-a-thread.md)
</dt> </dl>

 

 
