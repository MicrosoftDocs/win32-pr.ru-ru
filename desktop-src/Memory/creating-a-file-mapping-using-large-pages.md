---
description: В следующем примере используется функция CreateFileMapping с \_ \_ флагом больших страниц sec для использования больших страниц. Для этого требуется Windows Server 2003 с пакетом обновления 1 (SP1) или более поздней версии.
ms.assetid: be2cdcbc-03e8-407d-8ae2-569f8fd8cba8
title: Создание сопоставления файлов с помощью больших страниц
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49a852de187f6798904ef1795dca5955663283f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682612"
---
# <a name="creating-a-file-mapping-using-large-pages"></a><span data-ttu-id="63430-104">Создание сопоставления файлов с помощью больших страниц</span><span class="sxs-lookup"><span data-stu-id="63430-104">Creating a File Mapping Using Large Pages</span></span>

<span data-ttu-id="63430-105">В следующем примере используется функция [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) с флагом **\_ больших \_ страниц sec** для использования больших страниц.</span><span class="sxs-lookup"><span data-stu-id="63430-105">The following example uses the [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) function with the **SEC\_LARGE\_PAGES** flag to use large pages.</span></span> <span data-ttu-id="63430-106">Буфер должен быть достаточно большим, чтобы вместить минимальный размер большой страницы.</span><span class="sxs-lookup"><span data-stu-id="63430-106">The buffer must be large enough to contain the minimum size of a large page.</span></span> <span data-ttu-id="63430-107">Это значение получается с помощью функции [**жетларжепажеминимум**](/windows/win32/api/memoryapi/nf-memoryapi-getlargepageminimum) .</span><span class="sxs-lookup"><span data-stu-id="63430-107">This value is obtained using the [**GetLargePageMinimum**](/windows/win32/api/memoryapi/nf-memoryapi-getlargepageminimum) function.</span></span> <span data-ttu-id="63430-108">Для этой функции также требуется привилегия "SeLockMemoryPrivilege".</span><span class="sxs-lookup"><span data-stu-id="63430-108">This feature also requires the "SeLockMemoryPrivilege" privilege.</span></span>

> [!NOTE]
> <span data-ttu-id="63430-109">Начиная с Windows 10 версии 1703 функция [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) сопоставляет представление с помощью мелких страниц по умолчанию, даже для объектов сопоставления файлов, созданных с помощью флага **\_ больших \_ страниц sec** .</span><span class="sxs-lookup"><span data-stu-id="63430-109">Starting in Windows 10, version 1703, the [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) function maps a view using small pages by default, even for file mapping objects created with the **SEC\_LARGE\_PAGES** flag.</span></span> <span data-ttu-id="63430-110">В этой и более поздних версиях ОС необходимо указать флаг **File \_ Map \_ Large \_ pages** с функцией [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) для отображения больших страниц.</span><span class="sxs-lookup"><span data-stu-id="63430-110">In this and later OS versions, you must specify the **FILE\_MAP\_LARGE\_PAGES** flag with the [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) function to map large pages.</span></span> <span data-ttu-id="63430-111">Этот флаг не учитывается в версиях ОС до Windows 10, версия 1703.</span><span class="sxs-lookup"><span data-stu-id="63430-111">This flag is ignored on OS versions before Windows 10, version 1703.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

#define BUF_SIZE 65536

TCHAR szName[]=TEXT("LARGEPAGE");
typedef int (*GETLARGEPAGEMINIMUM)(void);

void DisplayError(const wchar_t* pszAPI, DWORD dwError)
{
    LPVOID lpvMessageBuffer;

    FormatMessage(FORMAT_MESSAGE_ALLOCATE_BUFFER |
                  FORMAT_MESSAGE_FROM_SYSTEM |
                  FORMAT_MESSAGE_IGNORE_INSERTS,
                  NULL, dwError,
                  MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT),
                  (LPTSTR)&lpvMessageBuffer, 0, NULL);

    //... now display this string
    _tprintf(TEXT("ERROR: API        = %s\n"), pszAPI);
    _tprintf(TEXT("       error code = %d\n"), dwError);
    _tprintf(TEXT("       message    = %s\n"), lpvMessageBuffer);

    // Free the buffer allocated by the system
    LocalFree(lpvMessageBuffer);

    ExitProcess(GetLastError());
}

void Privilege(const wchar_t* pszPrivilege, BOOL bEnable)
{
    HANDLE           hToken;
    TOKEN_PRIVILEGES tp;
    BOOL             status;
    DWORD            error;

    // open process token
    if (!OpenProcessToken(GetCurrentProcess(), TOKEN_ADJUST_PRIVILEGES | TOKEN_QUERY, &hToken))
        DisplayError(TEXT("OpenProcessToken"), GetLastError());

    // get the luid
    if (!LookupPrivilegeValue(NULL, pszPrivilege, &tp.Privileges[0].Luid))
        DisplayError(TEXT("LookupPrivilegeValue"), GetLastError());

    tp.PrivilegeCount = 1;

    // enable or disable privilege
    if (bEnable)
        tp.Privileges[0].Attributes = SE_PRIVILEGE_ENABLED;
    else
        tp.Privileges[0].Attributes = 0;

    // enable or disable privilege
    status = AdjustTokenPrivileges(hToken, FALSE, &tp, 0, (PTOKEN_PRIVILEGES)NULL, 0);

    // It is possible for AdjustTokenPrivileges to return TRUE and still not succeed.
    // So always check for the last error value.
    error = GetLastError();
    if (!status || (error != ERROR_SUCCESS))
        DisplayError(TEXT("AdjustTokenPrivileges"), GetLastError());

    // close the handle
    if (!CloseHandle(hToken))
        DisplayError(TEXT("CloseHandle"), GetLastError());
}

int _tmain(void)
{
    HANDLE hMapFile;
    LPCTSTR pBuf;
    DWORD size;
    GETLARGEPAGEMINIMUM pGetLargePageMinimum;
    HINSTANCE  hDll;

    // call succeeds only on Windows Server 2003 SP1 or later
    hDll = LoadLibrary(TEXT("kernel32.dll"));
    if (hDll == NULL)
        DisplayError(TEXT("LoadLibrary"), GetLastError());

    pGetLargePageMinimum = (GETLARGEPAGEMINIMUM)GetProcAddress(hDll,
        "GetLargePageMinimum");
    if (pGetLargePageMinimum == NULL)
        DisplayError(TEXT("GetProcAddress"), GetLastError());

    size = (*pGetLargePageMinimum)();

    FreeLibrary(hDll);

    _tprintf(TEXT("Page Size: %u\n"), size);

    Privilege(TEXT("SeLockMemoryPrivilege"), TRUE);

    hMapFile = CreateFileMapping(
         INVALID_HANDLE_VALUE,    // use paging file
         NULL,                    // default security
         PAGE_READWRITE | SEC_COMMIT | SEC_LARGE_PAGES,
         0,                       // max. object size
         size,                    // buffer size
         szName);                 // name of mapping object

    if (hMapFile == NULL)
        DisplayError(TEXT("CreateFileMapping"), GetLastError());
    else
        _tprintf(TEXT("File mapping object successfully created.\n"));

    Privilege(TEXT("SeLockMemoryPrivilege"), FALSE);

    pBuf = (LPTSTR) MapViewOfFile(hMapFile,          // handle to map object
         FILE_MAP_ALL_ACCESS | FILE_MAP_LARGE_PAGES, // read/write permission
         0,
         0,
         BUF_SIZE);

    if (pBuf == NULL)
        DisplayError(TEXT("MapViewOfFile"), GetLastError());
    else
        _tprintf(TEXT("View of file successfully mapped.\n"));

    // do nothing, clean up an exit
    UnmapViewOfFile(pBuf);
    CloseHandle(hMapFile);
}
```



## <a name="related-topics"></a><span data-ttu-id="63430-112">См. также</span><span class="sxs-lookup"><span data-stu-id="63430-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63430-113">Создание объекта сопоставления файлов</span><span class="sxs-lookup"><span data-stu-id="63430-113">Creating a File Mapping Object</span></span>](creating-a-file-mapping-object.md)
</dt> <dt>

[<span data-ttu-id="63430-114">Поддержка больших страниц</span><span class="sxs-lookup"><span data-stu-id="63430-114">Large Page Support</span></span>](large-page-support.md)
</dt> </dl>

 

 
