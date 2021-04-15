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
# <a name="using-thread-local-storage-in-a-dynamic-link-library"></a>Использование локального хранилища потока в библиотеке Dynamic-Link

В этом разделе показано использование функции точки входа библиотеки DLL для настройки индекса локального хранилища потока (TLS) для предоставления закрытого хранилища для каждого потока многопоточного процесса.

Индекс TLS хранится в глобальной переменной и становится доступным для всех функций DLL. В этом примере предполагается, что глобальные данные библиотеки DLL не являются общими, так как индекс TLS не обязательно одинаков для каждого процесса, который загружает библиотеку DLL.

Функция точки входа использует функцию [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) для выделения индекса TLS каждый раз, когда процесс ЗАГРУЖАЕТ библиотеку DLL. Затем каждый поток может использовать этот индекс для хранения указателя на собственный блок памяти.

Когда функция точки входа вызывается с использованием \_ значения attach для процесса DLL \_ , код выполняет следующие действия:

1.  Использует функцию [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) для выделения индекса TLS.
2.  Выделяет блок памяти, используемый исключительно исходным потоком процесса.
3.  Использует индекс TLS в вызове функции [**тлссетвалуе**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlssetvalue) для хранения адреса блока памяти в СЛОТе TLS, связанном с индексом.

Каждый раз, когда процесс создает новый поток, функция точки входа вызывается со \_ \_ значением присоединения потока DLL. Затем функция точки входа выделяет блок памяти для нового потока и сохраняет указатель на него с помощью индекса TLS.

Если функции требуется доступ к данным, связанным с индексом TLS, укажите индекс в вызове функции [**тлсжетвалуе**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) . При этом извлекается содержимое слота TLS для вызывающего потока, который в данном случае является указателем на блок памяти для данных. Если процесс использует связывание во время загрузки с этой библиотекой DLL, функция точки входа достаточна для управления локальным хранилищем потока. Проблемы могут возникать в процессе, который использует связывание во время выполнения, так как функция точки входа не вызывается для потоков, которые существуют до вызова функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) , поэтому для этих потоков не выделяется память TLS. Этот пример решает эту проблему, проверяя значение, возвращаемое функцией [**тлсжетвалуе**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue) , и выделяя память, если значение указывает, что слот TLS для этого потока не задан.

Когда каждому потоку больше не требуется использовать TLS-индекс, он должен освободить память, указатель которой хранится в слоте TLS. Когда все потоки завершили работу с индексом TLS, используйте функцию [**TlsFree**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsfree) для освобождения индекса.

Когда поток завершается, функция точки входа вызывается с использованием \_ \_ значения отсоединения потока DLL, а память для этого потока освобождается. Когда процесс завершается, функция точки входа вызывается вместе со \_ \_ значением отсоединения процесса DLL и память, на которую ссылается указатель в TLS-индексе, освобождается.


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



В следующем коде показано использование функций DLL, определенных в предыдущем примере.


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Данные библиотеки динамической компоновки](dynamic-link-library-data.md)
</dt> <dt>

[Использование локального хранилища потоков](/windows/desktop/ProcThread/using-thread-local-storage)
</dt> </dl>

 

 
