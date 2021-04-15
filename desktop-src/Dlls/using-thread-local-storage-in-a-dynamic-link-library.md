---
description: В этом разделе показано использование функции точки входа библиотеки DLL для настройки индекса локального хранилища потока (TLS) для предоставления закрытого хранилища для каждого потока многопоточного процесса.
ms.assetid: a300f223-b513-4a22-a7a4-5d98cf74d77d
title: Использование локального хранилища потока в библиотеке Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 261ef7482520b4cb6e6c7b630f10ebb456231283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683048"
---
# <a name="using-thread-local-storage-in-a-dynamic-link-library"></a><span data-ttu-id="4a59a-103">Использование локального хранилища потока в библиотеке Dynamic-Link</span><span class="sxs-lookup"><span data-stu-id="4a59a-103">Using Thread Local Storage in a Dynamic-Link Library</span></span>

<span data-ttu-id="4a59a-104">В этом разделе показано использование функции точки входа библиотеки DLL для настройки индекса локального хранилища потока (TLS) для предоставления закрытого хранилища для каждого потока многопоточного процесса.</span><span class="sxs-lookup"><span data-stu-id="4a59a-104">This section shows the use of a DLL entry-point function to set up a thread local storage (TLS) index to provide private storage for each thread of a multithreaded process.</span></span>

<span data-ttu-id="4a59a-105">Индекс TLS хранится в глобальной переменной и становится доступным для всех функций DLL.</span><span class="sxs-lookup"><span data-stu-id="4a59a-105">The TLS index is stored in a global variable, making it available to all of the DLL functions.</span></span> <span data-ttu-id="4a59a-106">В этом примере предполагается, что глобальные данные библиотеки DLL не являются общими, так как индекс TLS не обязательно одинаков для каждого процесса, который загружает библиотеку DLL.</span><span class="sxs-lookup"><span data-stu-id="4a59a-106">This example assumes that the DLL's global data is not shared, because the TLS index is not necessarily the same for each process that loads the DLL.</span></span>

<span data-ttu-id="4a59a-107">Функция точки входа использует функцию [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) для выделения индекса TLS каждый раз, когда процесс ЗАГРУЖАЕТ библиотеку DLL.</span><span class="sxs-lookup"><span data-stu-id="4a59a-107">The entry-point function uses the [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) function to allocate a TLS index whenever a process loads the DLL.</span></span> <span data-ttu-id="4a59a-108">Затем каждый поток может использовать этот индекс для хранения указателя на собственный блок памяти.</span><span class="sxs-lookup"><span data-stu-id="4a59a-108">Each thread can then use this index to store a pointer to its own block of memory.</span></span>

<span data-ttu-id="4a59a-109">Когда функция точки входа вызывается с использованием \_ значения attach для процесса DLL \_ , код выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="4a59a-109">When the entry-point function is called with the DLL\_PROCESS\_ATTACH value, the code performs the following actions:</span></span>

1.  <span data-ttu-id="4a59a-110">Использует функцию [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) для выделения индекса TLS.</span><span class="sxs-lookup"><span data-stu-id="4a59a-110">Uses the [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) function to allocate a TLS index.</span></span>
2.  <span data-ttu-id="4a59a-111">Выделяет блок памяти, используемый исключительно исходным потоком процесса.</span><span class="sxs-lookup"><span data-stu-id="4a59a-111">Allocates a block of memory to be used exclusively by the initial thread of the process.</span></span>
3.  <span data-ttu-id="4a59a-112">Использует индекс TLS в вызове функции [**тлссетвалуе**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlssetvalue) для хранения адреса блока памяти в СЛОТе TLS, связанном с индексом.</span><span class="sxs-lookup"><span data-stu-id="4a59a-112">Uses the TLS index in a call to the [**TlsSetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlssetvalue) function to store the address of the memory block in the TLS slot associated with the index.</span></span>

<span data-ttu-id="4a59a-113">Каждый раз, когда процесс создает новый поток, функция точки входа вызывается со \_ \_ значением присоединения потока DLL.</span><span class="sxs-lookup"><span data-stu-id="4a59a-113">Each time the process creates a new thread, the entry-point function is called with the DLL\_THREAD\_ATTACH value.</span></span> <span data-ttu-id="4a59a-114">Затем функция точки входа выделяет блок памяти для нового потока и сохраняет указатель на него с помощью индекса TLS.</span><span class="sxs-lookup"><span data-stu-id="4a59a-114">The entry-point function then allocates a block of memory for the new thread and stores a pointer to it by using the TLS index.</span></span>

<span data-ttu-id="4a59a-115">Если функции требуется доступ к данным, связанным с индексом TLS, укажите индекс в вызове функции [**тлсжетвалуе**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) .</span><span class="sxs-lookup"><span data-stu-id="4a59a-115">When a function requires access to the data associated with a TLS index, specify the index in a call to the [**TlsGetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) function.</span></span> <span data-ttu-id="4a59a-116">При этом извлекается содержимое слота TLS для вызывающего потока, который в данном случае является указателем на блок памяти для данных.</span><span class="sxs-lookup"><span data-stu-id="4a59a-116">This retrieves the contents of the TLS slot for the calling thread, which in this case is a pointer to the memory block for the data.</span></span> <span data-ttu-id="4a59a-117">Если процесс использует связывание во время загрузки с этой библиотекой DLL, функция точки входа достаточна для управления локальным хранилищем потока.</span><span class="sxs-lookup"><span data-stu-id="4a59a-117">When a process uses load-time linking with this DLL, the entry-point function is sufficient to manage the thread local storage.</span></span> <span data-ttu-id="4a59a-118">Проблемы могут возникать в процессе, который использует связывание во время выполнения, так как функция точки входа не вызывается для потоков, которые существуют до вызова функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) , поэтому для этих потоков не выделяется память TLS.</span><span class="sxs-lookup"><span data-stu-id="4a59a-118">Problems can occur with a process that uses run-time linking because the entry-point function is not called for threads that exist before the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) function is called, so TLS memory is not allocated for these threads.</span></span> <span data-ttu-id="4a59a-119">Этот пример решает эту проблему, проверяя значение, возвращаемое функцией [**тлсжетвалуе**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) , и выделяя память, если значение указывает, что слот TLS для этого потока не задан.</span><span class="sxs-lookup"><span data-stu-id="4a59a-119">This example solves this problem by checking the value returned by the [**TlsGetValue**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) function and allocating memory if the value indicates that the TLS slot for this thread is not set.</span></span>

<span data-ttu-id="4a59a-120">Когда каждому потоку больше не требуется использовать TLS-индекс, он должен освободить память, указатель которой хранится в слоте TLS.</span><span class="sxs-lookup"><span data-stu-id="4a59a-120">When each thread no longer needs to use a TLS index, it must free the memory whose pointer is stored in the TLS slot.</span></span> <span data-ttu-id="4a59a-121">Когда все потоки завершили работу с индексом TLS, используйте функцию [**TlsFree**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsfree) для освобождения индекса.</span><span class="sxs-lookup"><span data-stu-id="4a59a-121">When all threads have finished using a TLS index, use the [**TlsFree**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsfree) function to release the index.</span></span>

<span data-ttu-id="4a59a-122">Когда поток завершается, функция точки входа вызывается с использованием \_ \_ значения отсоединения потока DLL, а память для этого потока освобождается.</span><span class="sxs-lookup"><span data-stu-id="4a59a-122">When a thread terminates, the entry-point function is called with the DLL\_THREAD\_DETACH value and the memory for that thread is freed.</span></span> <span data-ttu-id="4a59a-123">Когда процесс завершается, функция точки входа вызывается вместе со \_ \_ значением отсоединения процесса DLL и память, на которую ссылается указатель в TLS-индексе, освобождается.</span><span class="sxs-lookup"><span data-stu-id="4a59a-123">When a process terminates, the entry-point function is called with the DLL\_PROCESS\_DETACH value and the memory referenced by the pointer in the TLS index is freed.</span></span>


```C++
// The DLL code

#include <windows.h>

static DWORD dwTlsIndex; // address of shared memory
 
// DllMain() is the entry-point function for this DLL. 
 
BOOL WINAPI DllMain(HINSTANCE hinstDLL, // DLL module handle
    DWORD fdwReason,                    // reason called
    LPVOID lpvReserved)                 // reserved
{ 
    LPVOID lpvData; 
    BOOL fIgnore; 
 
    switch (fdwReason) 
    { 
        // The DLL is loading due to process 
        // initialization or a call to LoadLibrary. 
 
        case DLL_PROCESS_ATTACH: 
 
            // Allocate a TLS index.
 
            if ((dwTlsIndex = TlsAlloc()) == TLS_OUT_OF_INDEXES) 
                return FALSE; 
 
            // No break: Initialize the index for first thread.
 
        // The attached process creates a new thread. 
 
        case DLL_THREAD_ATTACH: 
 
            // Initialize the TLS index for this thread.
 
            lpvData = (LPVOID) LocalAlloc(LPTR, 256); 
            if (lpvData != NULL) 
                fIgnore = TlsSetValue(dwTlsIndex, lpvData); 
 
            break; 
 
        // The thread of the attached process terminates.
 
        case DLL_THREAD_DETACH: 
 
            // Release the allocated memory for this thread.
 
            lpvData = TlsGetValue(dwTlsIndex); 
            if (lpvData != NULL) 
                LocalFree((HLOCAL) lpvData); 
 
            break; 
 
        // DLL unload due to process termination or FreeLibrary. 
 
        case DLL_PROCESS_DETACH: 
 
            // Release the allocated memory for this thread.
 
            lpvData = TlsGetValue(dwTlsIndex); 
            if (lpvData != NULL) 
                LocalFree((HLOCAL) lpvData); 
 
            // Release the TLS index.
 
            TlsFree(dwTlsIndex); 
            break; 
 
        default: 
            break; 
    } 
 
    return TRUE; 
    UNREFERENCED_PARAMETER(hinstDLL); 
    UNREFERENCED_PARAMETER(lpvReserved); 
}

// The export mechanism used here is the __declspec(export)
// method supported by Microsoft Visual Studio, but any
// other export method supported by your development
// environment may be substituted.

#ifdef __cplusplus    // If used by C++ code, 
extern "C" {          // we need to export the C interface
#endif

__declspec(dllexport)
BOOL WINAPI StoreData(DWORD dw)
{
   LPVOID lpvData; 
   DWORD * pData;  // The stored memory pointer 

   lpvData = TlsGetValue(dwTlsIndex); 
   if (lpvData == NULL)
   {
      lpvData = (LPVOID) LocalAlloc(LPTR, 256); 
      if (lpvData == NULL) 
         return FALSE;
      if (!TlsSetValue(dwTlsIndex, lpvData))
         return FALSE;
   }

   pData = (DWORD *) lpvData; // Cast to my data type.
   // In this example, it is only a pointer to a DWORD
   // but it can be a structure pointer to contain more complicated data.

   (*pData) = dw;
   return TRUE;
}

__declspec(dllexport)
BOOL WINAPI GetData(DWORD *pdw)
{
   LPVOID lpvData; 
   DWORD * pData;  // The stored memory pointer 

   lpvData = TlsGetValue(dwTlsIndex); 
   if (lpvData == NULL)
      return FALSE;

   pData = (DWORD *) lpvData;
   (*pdw) = (*pData);
   return TRUE;
}
#ifdef __cplusplus
}
#endif
```



<span data-ttu-id="4a59a-124">В следующем коде показано использование функций DLL, определенных в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="4a59a-124">The following code demonstrates the use of the DLL functions defined in the previous example.</span></span>


```C++
#include <windows.h> 
#include <stdio.h> 
 
#define THREADCOUNT 4 
#define DLL_NAME TEXT("testdll")

VOID ErrorExit(LPSTR); 

extern "C" BOOL WINAPI StoreData(DWORD dw);
extern "C" BOOL WINAPI GetData(DWORD *pdw);
 
DWORD WINAPI ThreadFunc(VOID) 
{   
   int i;

   if(!StoreData(GetCurrentThreadId()))
      ErrorExit("StoreData error");

   for(i=0; i<THREADCOUNT; i++)
   {
      DWORD dwOut;
      if(!GetData(&dwOut))
         ErrorExit("GetData error");
      if( dwOut != GetCurrentThreadId())
         printf("thread %d: data is incorrect (%d)\n", GetCurrentThreadId(), dwOut);
      else printf("thread %d: data is correct\n", GetCurrentThreadId());
      Sleep(0);
   }
   return 0; 
} 
 
int main(VOID) 
{ 
   DWORD IDThread; 
   HANDLE hThread[THREADCOUNT]; 
   int i; 
   HMODULE hm;
 
// Load the DLL

   hm = LoadLibrary(DLL_NAME);
   if(!hm)
   {
      ErrorExit("DLL failed to load");
   }

// Create multiple threads. 
 
   for (i = 0; i < THREADCOUNT; i++) 
   { 
      hThread[i] = CreateThread(NULL, // default security attributes 
         0,                           // use default stack size 
         (LPTHREAD_START_ROUTINE) ThreadFunc, // thread function 
         NULL,                    // no thread function argument 
         0,                       // use default creation flags 
         &IDThread);              // returns thread identifier 
 
   // Check the return value for success. 
      if (hThread[i] == NULL) 
         ErrorExit("CreateThread error\n"); 
   } 
 
   WaitForMultipleObjects(THREADCOUNT, hThread, TRUE, INFINITE); 

   FreeLibrary(hm);
 
   return 0; 
} 
 
VOID ErrorExit (LPSTR lpszMessage) 
{ 
   fprintf(stderr, "%s\n", lpszMessage); 
   ExitProcess(0); 
}
```



## <a name="related-topics"></a><span data-ttu-id="4a59a-125">См. также</span><span class="sxs-lookup"><span data-stu-id="4a59a-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a59a-126">Данные библиотеки динамической компоновки</span><span class="sxs-lookup"><span data-stu-id="4a59a-126">Dynamic-Link Library Data</span></span>](dynamic-link-library-data.md)
</dt> <dt>

[<span data-ttu-id="4a59a-127">Использование локального хранилища потоков</span><span class="sxs-lookup"><span data-stu-id="4a59a-127">Using Thread Local Storage</span></span>](/windows/desktop/ProcThread/using-thread-local-storage)
</dt> </dl>

 

 
