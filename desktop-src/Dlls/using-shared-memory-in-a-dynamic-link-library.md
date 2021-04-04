---
description: В следующем примере показано, как функция точки входа библиотеки DLL может использовать объект сопоставления файлов для настройки памяти, которая может совместно использоваться процессами, которые загружают библиотеку DLL.
ms.assetid: ab751ab1-3b40-4111-b724-9f8676b722a3
title: Использование общей памяти в библиотеке Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 978a6fa77964c6404b3f85e9c9bcec6c3644f2ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898141"
---
# <a name="using-shared-memory-in-a-dynamic-link-library"></a>Использование общей памяти в библиотеке Dynamic-Link

В следующем примере показано, как функция точки входа библиотеки DLL может использовать объект сопоставления файлов для настройки памяти, которая может совместно использоваться процессами, которые загружают библиотеку DLL. Общая память DLL сохраняется только при загрузке библиотеки DLL. Приложения могут использовать функции Сетшаредмем и Жетшаредмем для доступа к общей памяти.

## <a name="dll-that-implements-the-shared-memory"></a>Библиотека DLL, реализующая общую память

В примере используется сопоставление файлов для сопоставления блока именованной общей памяти с виртуальным адресным пространством каждого процесса, который загружает библиотеку DLL. Для этого функция точки входа должна:

1.  Вызовите функцию [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga) , чтобы получить маркер для объекта сопоставления файлов. Первый процесс, загружающий библиотеку DLL, создает объект сопоставления файлов. Последующие процессы открывают обработчик для существующего объекта. Дополнительные сведения см. [в разделе Создание объекта File-Mapping](/windows/desktop/Memory/creating-a-file-mapping-object).
2.  Вызовите функцию [**MapViewOfFile**](/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile) , чтобы связать представление с виртуальным адресным пространством. Это позволяет процессу получить доступ к общей памяти. Дополнительные сведения см. [в разделе Создание представления файлов](/windows/desktop/Memory/creating-a-file-view).

Обратите внимание, что хотя можно указать атрибуты безопасности по умолчанию, передав значение NULL для параметра *лпаттрибутес* в [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga), вы можете использовать структуру [**\_ атрибутов безопасности**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) для обеспечения дополнительной безопасности.


```C++
// The DLL code

#include <windows.h> 
#include <memory.h> 
 
#define SHMEMSIZE 4096 
 
static LPVOID lpvMem = NULL;      // pointer to shared memory
static HANDLE hMapObject = NULL;  // handle to file mapping

// The DLL entry-point function sets up shared memory using a 
// named file-mapping object. 
 
BOOL WINAPI DllMain(HINSTANCE hinstDLL,  // DLL module handle
    DWORD fdwReason,              // reason called 
    LPVOID lpvReserved)           // reserved 
{ 
    BOOL fInit, fIgnore; 
 
    switch (fdwReason) 
    { 
        // DLL load due to process initialization or LoadLibrary
 
          case DLL_PROCESS_ATTACH: 
 
            // Create a named file mapping object
 
            hMapObject = CreateFileMapping( 
                INVALID_HANDLE_VALUE,   // use paging file
                NULL,                   // default security attributes
                PAGE_READWRITE,         // read/write access
                0,                      // size: high 32-bits
                SHMEMSIZE,              // size: low 32-bits
                TEXT("dllmemfilemap")); // name of map object
            if (hMapObject == NULL) 
                return FALSE; 
 
            // The first process to attach initializes memory
 
            fInit = (GetLastError() != ERROR_ALREADY_EXISTS); 
 
            // Get a pointer to the file-mapped shared memory
 
            lpvMem = MapViewOfFile( 
                hMapObject,     // object to map view of
                FILE_MAP_WRITE, // read/write access
                0,              // high offset:  map from
                0,              // low offset:   beginning
                0);             // default: map entire file
            if (lpvMem == NULL) 
                return FALSE; 
 
            // Initialize memory if this is the first process
 
            if (fInit) 
                memset(lpvMem, '\0', SHMEMSIZE); 
 
            break; 
 
        // The attached process creates a new thread
 
        case DLL_THREAD_ATTACH: 
            break; 
 
        // The thread of the attached process terminates
 
        case DLL_THREAD_DETACH: 
            break; 
 
        // DLL unload due to process termination or FreeLibrary
 
        case DLL_PROCESS_DETACH: 
 
            // Unmap shared memory from the process's address space
 
            fIgnore = UnmapViewOfFile(lpvMem); 
 
            // Close the process's handle to the file-mapping object
 
            fIgnore = CloseHandle(hMapObject); 
 
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
 
// SetSharedMem sets the contents of the shared memory 
 
__declspec(dllexport) VOID __cdecl SetSharedMem(LPWSTR lpszBuf) 
{ 
    LPWSTR lpszTmp; 
    DWORD dwCount=1;
 
    // Get the address of the shared memory block
 
    lpszTmp = (LPWSTR) lpvMem; 
 
    // Copy the null-terminated string into shared memory
 
    while (*lpszBuf && dwCount<SHMEMSIZE) 
    {
        *lpszTmp++ = *lpszBuf++; 
        dwCount++;
    }
    *lpszTmp = '\0'; 
} 
 
// GetSharedMem gets the contents of the shared memory
 
__declspec(dllexport) VOID __cdecl GetSharedMem(LPWSTR lpszBuf, DWORD cchSize) 
{ 
    LPWSTR lpszTmp; 
 
    // Get the address of the shared memory block
 
    lpszTmp = (LPWSTR) lpvMem; 
 
    // Copy from shared memory into the caller's buffer
 
    while (*lpszTmp && --cchSize) 
        *lpszBuf++ = *lpszTmp++; 
    *lpszBuf = '\0'; 
}
#ifdef __cplusplus
}
#endif
```



Общая память может быть сопоставлена с другим адресом в каждом процессе. По этой причине каждый процесс имеет собственный экземпляр Лпвмем, который объявляется как глобальная переменная, чтобы она была доступна для всех функций DLL. В этом примере предполагается, что глобальные данные библиотеки DLL не являются общими, поэтому каждый процесс, загружающий библиотеку DLL, имеет собственный экземпляр Лпвмем.

Обратите внимание, что общая память освобождается при закрытии последнего маркера объекта сопоставления файлов. Чтобы создать постоянную общую память, необходимо убедиться, что некоторый процесс всегда имеет открытый маркер для объекта сопоставления файлов.

## <a name="processes-that-use-the-shared-memory"></a>Процессы, использующие общую память

Следующие процессы используют общую память, предоставляемую библиотекой DLL, определенной выше. Первый процесс вызывает Сетшаредмем для записи строки, а второй процесс вызывает Жетшаредмем для получения этой строки.

В этом процессе используется функция Сетшаредмем, реализованная библиотекой DLL для записи строки "This является тестовой строкой" в общую память. Он также запускает дочерний процесс, который будет считывать строку из общей памяти.


```C++
// Parent process

#include <windows.h>
#include <tchar.h>
#include <stdio.h>

extern "C" VOID __cdecl SetSharedMem(LPWSTR lpszBuf);

HANDLE CreateChildProcess(LPTSTR szCmdline) 
{ 
   PROCESS_INFORMATION piProcInfo; 
   STARTUPINFO siStartInfo;
   BOOL bFuncRetn = FALSE; 
 
// Set up members of the PROCESS_INFORMATION structure. 
 
   ZeroMemory( &piProcInfo, sizeof(PROCESS_INFORMATION) );
 
// Set up members of the STARTUPINFO structure. 
 
   ZeroMemory( &siStartInfo, sizeof(STARTUPINFO) );
   siStartInfo.cb = sizeof(STARTUPINFO); 
 
// Create the child process. 
    
   bFuncRetn = CreateProcess(NULL, 
      szCmdline,     // command line 
      NULL,          // process security attributes 
      NULL,          // primary thread security attributes 
      TRUE,          // handles are inherited 
      0,             // creation flags 
      NULL,          // use parent's environment 
      NULL,          // use parent's current directory 
      &siStartInfo,  // STARTUPINFO pointer 
      &piProcInfo);  // receives PROCESS_INFORMATION 
   
   if (bFuncRetn == 0) 
   {
      printf("CreateProcess failed (%)\n", GetLastError());
      return INVALID_HANDLE_VALUE;
   }
   else 
   {
      CloseHandle(piProcInfo.hThread);
      return piProcInfo.hProcess;
   }
}

int _tmain(int argc, TCHAR *argv[])
{
   HANDLE hProcess;

   if (argc == 1) 
   {
      printf("Please specify an input file");
      ExitProcess(0);
   }

   // Call the DLL function
   printf("\nProcess is writing to shared memory...\n\n");
   SetSharedMem(L"This is a test string");

   // Start the child process that will read the memory
   hProcess = CreateChildProcess(argv[1]);

   // Ensure this process is around until the child process terminates
   if (INVALID_HANDLE_VALUE != hProcess) 
   {
      WaitForSingleObject(hProcess, INFINITE);
      CloseHandle(hProcess);
   }
   return 0;
}

```



В этом процессе используется функция Жетшаредмем, реализованная библиотекой DLL, для чтения строки из общей памяти. Он запускается родительским процессом выше.


```C++
// Child process

#include <windows.h>
#include <tchar.h>
#include <stdio.h>

extern "C" VOID __cdecl GetSharedMem(LPWSTR lpszBuf, DWORD cchSize);

int _tmain( void )
{
    WCHAR cBuf[MAX_PATH];

    GetSharedMem(cBuf, MAX_PATH);
 
    printf("Child process read from shared memory: %S\n", cBuf);
    
    return 0;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Данные библиотеки динамической компоновки](dynamic-link-library-data.md)
</dt> </dl>

 

 
