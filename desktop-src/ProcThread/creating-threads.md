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
# <a name="creating-threads"></a><span data-ttu-id="c22af-104">Создание потоков</span><span class="sxs-lookup"><span data-stu-id="c22af-104">Creating Threads</span></span>

<span data-ttu-id="c22af-105">Функция [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) создает новый поток для процесса.</span><span class="sxs-lookup"><span data-stu-id="c22af-105">The [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) function creates a new thread for a process.</span></span> <span data-ttu-id="c22af-106">В создаваемом потоке должен быть указан начальный адрес кода, который будет выполняться новым потоком.</span><span class="sxs-lookup"><span data-stu-id="c22af-106">The creating thread must specify the starting address of the code that the new thread is to execute.</span></span> <span data-ttu-id="c22af-107">Как правило, начальный адрес — это имя функции, определенной в программном коде (Дополнительные сведения см. в разделе [*среадпрок*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85))).</span><span class="sxs-lookup"><span data-stu-id="c22af-107">Typically, the starting address is the name of a function defined in the program code (for more information, see [*ThreadProc*](/previous-versions/windows/desktop/legacy/ms686736(v=vs.85))).</span></span> <span data-ttu-id="c22af-108">Эта функция принимает один параметр и возвращает значение **типа DWORD** .</span><span class="sxs-lookup"><span data-stu-id="c22af-108">This function takes a single parameter and returns a **DWORD** value.</span></span> <span data-ttu-id="c22af-109">Процесс может иметь несколько потоков, одновременно выполняющих одну и ту же функцию.</span><span class="sxs-lookup"><span data-stu-id="c22af-109">A process can have multiple threads simultaneously executing the same function.</span></span>

<span data-ttu-id="c22af-110">Ниже приведен простой пример, демонстрирующий создание нового потока, выполняющего локально определенную функцию `MyThreadFunction` .</span><span class="sxs-lookup"><span data-stu-id="c22af-110">The following is a simple example that demonstrates how to create a new thread that executes the locally defined function, `MyThreadFunction`.</span></span>

<span data-ttu-id="c22af-111">Вызывающий поток использует функцию [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) для сохранения до завершения всех рабочих потоков.</span><span class="sxs-lookup"><span data-stu-id="c22af-111">The calling thread uses the [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) function to persist until all worker threads have terminated.</span></span> <span data-ttu-id="c22af-112">Вызывающий поток блокируется в ожидании; чтобы продолжить обработку, вызывающий поток будет использовать [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) и ждет, пока каждый рабочий поток сообщит свой объект ожидания.</span><span class="sxs-lookup"><span data-stu-id="c22af-112">The calling thread blocks while it is waiting; to continue processing, a calling thread would use [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) and wait for each worker thread to signal its wait object.</span></span> <span data-ttu-id="c22af-113">Обратите внимание, что если бы вы закрыли обработчик до конца рабочего потока, это не завершит рабочий поток.</span><span class="sxs-lookup"><span data-stu-id="c22af-113">Note that if you were to close the handle to a worker thread before it terminated, this does not terminate the worker thread.</span></span> <span data-ttu-id="c22af-114">Однако этот маркер будет недоступен для использования в последующих вызовах функций.</span><span class="sxs-lookup"><span data-stu-id="c22af-114">However, the handle will be unavailable for use in subsequent function calls.</span></span>


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



<span data-ttu-id="c22af-115">`MyThreadFunction`Функция позволяет избежать использования библиотеки времени выполнения C (CRT), так как многие ее функции не являются потокобезопасными, особенно если не используется многопоточный CRT.</span><span class="sxs-lookup"><span data-stu-id="c22af-115">The `MyThreadFunction` function avoids the use of the C run-time library (CRT), as many of its functions are not thread-safe, particularly if you are not using the multithreaded CRT.</span></span> <span data-ttu-id="c22af-116">Если вы хотите использовать CRT в `ThreadProc` функции, используйте вместо этого функцию **\_ бегинсреадекс** .</span><span class="sxs-lookup"><span data-stu-id="c22af-116">If you would like to use the CRT in a `ThreadProc` function, use the **\_beginthreadex** function instead.</span></span>

<span data-ttu-id="c22af-117">При завершении создания потока до нового потока рискованно передавать адрес локальной переменной, так как указатель становится недопустимым.</span><span class="sxs-lookup"><span data-stu-id="c22af-117">It is risky to pass the address of a local variable if the creating thread exits before the new thread, because the pointer becomes invalid.</span></span> <span data-ttu-id="c22af-118">Вместо этого либо передайте указатель на динамически выделяемую память, либо создайте поток, ожидающий завершения нового потока.</span><span class="sxs-lookup"><span data-stu-id="c22af-118">Instead, either pass a pointer to dynamically allocated memory or make the creating thread wait for the new thread to terminate.</span></span> <span data-ttu-id="c22af-119">Данные также могут передаваться из создания потока в новый поток с помощью глобальных переменных.</span><span class="sxs-lookup"><span data-stu-id="c22af-119">Data can also be passed from the creating thread to the new thread using global variables.</span></span> <span data-ttu-id="c22af-120">При использовании глобальных переменных обычно требуется синхронизация доступа по нескольким потокам.</span><span class="sxs-lookup"><span data-stu-id="c22af-120">With global variables, it is usually necessary to synchronize access by multiple threads.</span></span> <span data-ttu-id="c22af-121">Дополнительные сведения о синхронизации см. в разделе [Синхронизация выполнения нескольких потоков](synchronizing-execution-of-multiple-threads.md).</span><span class="sxs-lookup"><span data-stu-id="c22af-121">For more information about synchronization, see [Synchronizing Execution of Multiple Threads](synchronizing-execution-of-multiple-threads.md).</span></span>

<span data-ttu-id="c22af-122">Создание потока может использовать аргументы для [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) , чтобы указать следующее:</span><span class="sxs-lookup"><span data-stu-id="c22af-122">The creating thread can use the arguments to [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) to specify the following:</span></span>

-   <span data-ttu-id="c22af-123">Атрибуты безопасности для этого маркера для нового потока.</span><span class="sxs-lookup"><span data-stu-id="c22af-123">The security attributes for the handle to the new thread.</span></span> <span data-ttu-id="c22af-124">Эти атрибуты безопасности включают флаг наследования, определяющий, может ли этот маркер наследоваться дочерними процессами.</span><span class="sxs-lookup"><span data-stu-id="c22af-124">These security attributes include an inheritance flag that determines whether the handle can be inherited by child processes.</span></span> <span data-ttu-id="c22af-125">Атрибуты безопасности также включают в себя дескриптор безопасности, который система использует для выполнения проверок доступа во всех последующих применениях дескриптора потока до предоставления доступа.</span><span class="sxs-lookup"><span data-stu-id="c22af-125">The security attributes also include a security descriptor, which the system uses to perform access checks on all subsequent uses of the thread's handle before access is granted.</span></span>
-   <span data-ttu-id="c22af-126">Начальный размер стека нового потока.</span><span class="sxs-lookup"><span data-stu-id="c22af-126">The initial stack size of the new thread.</span></span> <span data-ttu-id="c22af-127">Стек потока выделяется автоматически в области памяти процесса; система увеличивает стек по мере необходимости и освобождает ее после завершения потока.</span><span class="sxs-lookup"><span data-stu-id="c22af-127">The thread's stack is allocated automatically in the memory space of the process; the system increases the stack as needed and frees it when the thread terminates.</span></span> <span data-ttu-id="c22af-128">Дополнительные сведения см. в разделе [размер стека потока](thread-stack-size.md).</span><span class="sxs-lookup"><span data-stu-id="c22af-128">For more information, see [Thread Stack Size](thread-stack-size.md).</span></span>
-   <span data-ttu-id="c22af-129">Флаг создания, позволяющий создать поток в приостановленном состоянии.</span><span class="sxs-lookup"><span data-stu-id="c22af-129">A creation flag that enables you to create the thread in a suspended state.</span></span> <span data-ttu-id="c22af-130">При приостановке поток не выполняется до тех пор, пока не будет вызвана функция [**ресумесреад**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) .</span><span class="sxs-lookup"><span data-stu-id="c22af-130">When suspended, the thread does not run until the [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) function is called.</span></span>

<span data-ttu-id="c22af-131">Вы также можете создать поток, вызвав функцию [**креатеремотесреад**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) .</span><span class="sxs-lookup"><span data-stu-id="c22af-131">You can also create a thread by calling the [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) function.</span></span> <span data-ttu-id="c22af-132">Эта функция используется процессами отладчика для создания потока, выполняемого в адресном пространстве отлаживаемого процесса.</span><span class="sxs-lookup"><span data-stu-id="c22af-132">This function is used by debugger processes to create a thread that runs in the address space of the process being debugged.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c22af-133">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="c22af-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c22af-134">Завершение потока</span><span class="sxs-lookup"><span data-stu-id="c22af-134">Terminating a Thread</span></span>](terminating-a-thread.md)
</dt> </dl>

 

 
