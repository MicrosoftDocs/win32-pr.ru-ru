---
description: В следующем примере показано использование функций VirtualAlloc и VirtualFree при резервировании и фиксации памяти в случае необходимости для динамического массива.
ms.assetid: f46bd57d-7684-4a08-8ac7-de204aecb207
title: Резервирование и фиксация памяти
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66ff5853d01561454265e1ee2102fbf6ebd9bb04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684588"
---
# <a name="reserving-and-committing-memory"></a><span data-ttu-id="ca027-103">Резервирование и фиксация памяти</span><span class="sxs-lookup"><span data-stu-id="ca027-103">Reserving and Committing Memory</span></span>

<span data-ttu-id="ca027-104">В следующем примере показано использование функций [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) и [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) при резервировании и фиксации памяти в случае необходимости для динамического массива.</span><span class="sxs-lookup"><span data-stu-id="ca027-104">The following example illustrates the use of the [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) and [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) functions in reserving and committing memory as needed for a dynamic array.</span></span> <span data-ttu-id="ca027-105">Во-первых, вызывается **VirtualAlloc** для резервирования блока страниц со **значением NULL** , указанным в качестве параметра базового адреса, что позволяет системе определить расположение блока.</span><span class="sxs-lookup"><span data-stu-id="ca027-105">First, **VirtualAlloc** is called to reserve a block of pages with **NULL** specified as the base address parameter, forcing the system to determine the location of the block.</span></span> <span data-ttu-id="ca027-106">В дальнейшем **VirtualAlloc** вызывается каждый раз, когда необходимо зафиксировать страницу из этого зарезервированного региона, и указан базовый адрес следующей зафиксированной страницы.</span><span class="sxs-lookup"><span data-stu-id="ca027-106">Later, **VirtualAlloc** is called whenever it is necessary to commit a page from this reserved region, and the base address of the next page to be committed is specified.</span></span>

<span data-ttu-id="ca027-107">В примере используется структурированный синтаксис обработки исключений для фиксации страниц из зарезервированного региона.</span><span class="sxs-lookup"><span data-stu-id="ca027-107">The example uses structured exception-handling syntax to commit pages from the reserved region.</span></span> <span data-ttu-id="ca027-108">Всякий раз, когда возникает исключение страницы во время выполнения блока **\_ \_ try** , выполняется функция Filter в выражении перед блоком **\_ \_ except** .</span><span class="sxs-lookup"><span data-stu-id="ca027-108">Whenever a page fault exception occurs during the execution of the **\_\_try** block, the filter function in the expression preceding the **\_\_except** block is executed.</span></span> <span data-ttu-id="ca027-109">Если функция фильтра может выделить другую страницу, выполнение продолжится в блоке **\_ \_ try** в той точке, где возникло исключение.</span><span class="sxs-lookup"><span data-stu-id="ca027-109">If the filter function can allocate another page, execution continues in the **\_\_try** block at the point where the exception occurred.</span></span> <span data-ttu-id="ca027-110">В противном случае выполняется обработчик исключений в блоке **\_ \_ except** .</span><span class="sxs-lookup"><span data-stu-id="ca027-110">Otherwise, the exception handler in the **\_\_except** block is executed.</span></span> <span data-ttu-id="ca027-111">Дополнительные сведения см. в разделе [структурированная обработка исключений](../debug/structured-exception-handling.md).</span><span class="sxs-lookup"><span data-stu-id="ca027-111">For more information, see [Structured Exception Handling](../debug/structured-exception-handling.md).</span></span>

<span data-ttu-id="ca027-112">В качестве альтернативы динамическому выделению процесс может просто зафиксировать весь регион, а не только его резервирование.</span><span class="sxs-lookup"><span data-stu-id="ca027-112">As an alternative to dynamic allocation, the process can simply commit the entire region instead of only reserving it.</span></span> <span data-ttu-id="ca027-113">Оба метода приводят к одинаковому использованию физической памяти, так как зафиксированные страницы не используют физическое хранилище до первого обращения к ним.</span><span class="sxs-lookup"><span data-stu-id="ca027-113">Both methods result in the same physical memory usage because committed pages do not consume any physical storage until they are first accessed.</span></span> <span data-ttu-id="ca027-114">Преимуществом динамического выделения является сокращение общего количества зафиксированных страниц в системе.</span><span class="sxs-lookup"><span data-stu-id="ca027-114">The advantage of dynamic allocation is that it minimizes the total number of committed pages on the system.</span></span> <span data-ttu-id="ca027-115">Для очень больших выделений предварительное выделение всего выделения может привести к тому, что система закончит работу с фиксируемых страниц, что приведет к сбоям при выделении виртуальной памяти.</span><span class="sxs-lookup"><span data-stu-id="ca027-115">For very large allocations, pre-committing an entire allocation can cause the system to run out of committable pages, resulting in virtual memory allocation failures.</span></span>

<span data-ttu-id="ca027-116">Функция [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) в блоке **\_ \_ except** автоматически освобождает выделение виртуальной памяти, поэтому нет необходимости явно освобождать страницы, когда программа завершается через этот путь выполнения.</span><span class="sxs-lookup"><span data-stu-id="ca027-116">The [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) function in the **\_\_except** block automatically releases virtual memory allocations, so it is not necessary to explicitly free the pages when the program terminates through this execution path.</span></span> <span data-ttu-id="ca027-117">Функция [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) освобождает зарезервированные и зафиксированные страницы, если программа построена с отключенной обработкой исключений.</span><span class="sxs-lookup"><span data-stu-id="ca027-117">The [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) function frees the reserved and committed pages if the program is built with exception handling disabled.</span></span> <span data-ttu-id="ca027-118">Эта функция использует **\_ выпуск MEM** для отмены фиксации и освобождения всего региона зарезервированных и зафиксированных страниц.</span><span class="sxs-lookup"><span data-stu-id="ca027-118">This function uses **MEM\_RELEASE** to decommit and release the entire region of reserved and committed pages.</span></span>

<span data-ttu-id="ca027-119">В следующем примере C++ демонстрируется динамическое выделение памяти с помощью структурированного обработчика исключений.</span><span class="sxs-lookup"><span data-stu-id="ca027-119">The following C++ example demonstrates dynamic memory allocation using a structured exception handler.</span></span>


```C++
// A short program to demonstrate dynamic memory allocation
// using a structured exception handler.

#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <stdlib.h>             // For exit

#define PAGELIMIT 80            // Number of pages to ask for

LPTSTR lpNxtPage;               // Address of the next page to ask for
DWORD dwPages = 0;              // Count of pages gotten so far
DWORD dwPageSize;               // Page size on this computer

INT PageFaultExceptionFilter(DWORD dwCode)
{
    LPVOID lpvResult;

    // If the exception is not a page fault, exit.

    if (dwCode != EXCEPTION_ACCESS_VIOLATION)
    {
        _tprintf(TEXT("Exception code = %d.\n"), dwCode);
        return EXCEPTION_EXECUTE_HANDLER;
    }

    _tprintf(TEXT("Exception is a page fault.\n"));

    // If the reserved pages are used up, exit.

    if (dwPages >= PAGELIMIT)
    {
        _tprintf(TEXT("Exception: out of pages.\n"));
        return EXCEPTION_EXECUTE_HANDLER;
    }

    // Otherwise, commit another page.

    lpvResult = VirtualAlloc(
                     (LPVOID) lpNxtPage, // Next page to commit
                     dwPageSize,         // Page size, in bytes
                     MEM_COMMIT,         // Allocate a committed page
                     PAGE_READWRITE);    // Read/write access
    if (lpvResult == NULL )
    {
        _tprintf(TEXT("VirtualAlloc failed.\n"));
        return EXCEPTION_EXECUTE_HANDLER;
    }
    else
    {
        _tprintf(TEXT("Allocating another page.\n"));
    }

    // Increment the page count, and advance lpNxtPage to the next page.

    dwPages++;
    lpNxtPage = (LPTSTR) ((PCHAR) lpNxtPage + dwPageSize);

    // Continue execution where the page fault occurred.

    return EXCEPTION_CONTINUE_EXECUTION;
}

VOID ErrorExit(LPTSTR lpMsg)
{
    _tprintf(TEXT("Error! %s with error code of %ld.\n"),
             lpMsg, GetLastError ());
    exit (0);
}

VOID _tmain(VOID)
{
    LPVOID lpvBase;               // Base address of the test memory
    LPTSTR lpPtr;                 // Generic character pointer
    BOOL bSuccess;                // Flag
    DWORD i;                      // Generic counter
    SYSTEM_INFO sSysInfo;         // Useful information about the system

    GetSystemInfo(&sSysInfo);     // Initialize the structure.

    _tprintf (TEXT("This computer has page size %d.\n"), sSysInfo.dwPageSize);

    dwPageSize = sSysInfo.dwPageSize;

    // Reserve pages in the virtual address space of the process.

    lpvBase = VirtualAlloc(
                     NULL,                 // System selects address
                     PAGELIMIT*dwPageSize, // Size of allocation
                     MEM_RESERVE,          // Allocate reserved pages
                     PAGE_NOACCESS);       // Protection = no access
    if (lpvBase == NULL )
        ErrorExit(TEXT("VirtualAlloc reserve failed."));

    lpPtr = lpNxtPage = (LPTSTR) lpvBase;

    // Use structured exception handling when accessing the pages.
    // If a page fault occurs, the exception filter is executed to
    // commit another page from the reserved block of pages.

    for (i=0; i < PAGELIMIT*dwPageSize; i++)
    {
        __try
        {
            // Write to memory.

            lpPtr[i] = 'a';
        }

        // If there's a page fault, commit another page and try again.

        __except ( PageFaultExceptionFilter( GetExceptionCode() ) )
        {

            // This code is executed only if the filter function
            // is unsuccessful in committing the next page.

            _tprintf (TEXT("Exiting process.\n"));

            ExitProcess( GetLastError() );

        }

    }

    // Release the block of pages when you are finished using them.

    bSuccess = VirtualFree(
                       lpvBase,       // Base address of block
                       0,             // Bytes of committed pages
                       MEM_RELEASE);  // Decommit the pages

    _tprintf (TEXT("Release %s.\n"), bSuccess ? TEXT("succeeded") : TEXT("failed") );

}
```



 

 
