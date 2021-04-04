---
description: Функция CreateProcess создает новый процесс, который выполняется независимо от процесса создания. Однако для простоты связь называется связью типа «родители-потомки».
ms.assetid: 4c3f76a3-e9f5-4d73-b5ef-eabfa9d6e4d4
title: Создание процессов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75606a3006bf63359b3e52cf2172b8bc2d77ed56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998490"
---
# <a name="creating-processes"></a><span data-ttu-id="ac810-104">Создание процессов</span><span class="sxs-lookup"><span data-stu-id="ac810-104">Creating Processes</span></span>

<span data-ttu-id="ac810-105">Функция [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) создает новый процесс, который выполняется независимо от процесса создания.</span><span class="sxs-lookup"><span data-stu-id="ac810-105">The [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) function creates a new process, which runs independently of the creating process.</span></span> <span data-ttu-id="ac810-106">Однако для простоты связь называется связью типа «родители-потомки».</span><span class="sxs-lookup"><span data-stu-id="ac810-106">However, for simplicity, the relationship is referred to as a parent-child relationship.</span></span>

<span data-ttu-id="ac810-107">В следующем коде показано, как создать процесс.</span><span class="sxs-lookup"><span data-stu-id="ac810-107">The following code demonstrates how to create a process.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <tchar.h>

void _tmain( int argc, TCHAR *argv[] )
{
    STARTUPINFO si;
    PROCESS_INFORMATION pi;

    ZeroMemory( &si, sizeof(si) );
    si.cb = sizeof(si);
    ZeroMemory( &pi, sizeof(pi) );

    if( argc != 2 )
    {
        printf("Usage: %s [cmdline]\n", argv[0]);
        return;
    }

    // Start the child process. 
    if( !CreateProcess( NULL,   // No module name (use command line)
        argv[1],        // Command line
        NULL,           // Process handle not inheritable
        NULL,           // Thread handle not inheritable
        FALSE,          // Set handle inheritance to FALSE
        0,              // No creation flags
        NULL,           // Use parent's environment block
        NULL,           // Use parent's starting directory 
        &si,            // Pointer to STARTUPINFO structure
        &pi )           // Pointer to PROCESS_INFORMATION structure
    ) 
    {
        printf( "CreateProcess failed (%d).\n", GetLastError() );
        return;
    }

    // Wait until child process exits.
    WaitForSingleObject( pi.hProcess, INFINITE );

    // Close process and thread handles. 
    CloseHandle( pi.hProcess );
    CloseHandle( pi.hThread );
}
```



<span data-ttu-id="ac810-108">Если функция [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) завершается, возвращается структура [**\_ сведений о процессе**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information) , содержащая дескрипторы и идентификаторы для нового процесса и его основного потока.</span><span class="sxs-lookup"><span data-stu-id="ac810-108">If [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) succeeds, it returns a [**PROCESS\_INFORMATION**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information) structure containing handles and identifiers for the new process and its primary thread.</span></span> <span data-ttu-id="ac810-109">Дескрипторы потоков и процессов создаются с правами полного доступа, хотя доступ можно ограничить, если указать дескрипторы безопасности.</span><span class="sxs-lookup"><span data-stu-id="ac810-109">The thread and process handles are created with full access rights, although access can be restricted if you specify security descriptors.</span></span> <span data-ttu-id="ac810-110">Если эти дескрипторы больше не нужны, закройте их с помощью функции [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="ac810-110">When you no longer need these handles, close them by using the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function.</span></span>

<span data-ttu-id="ac810-111">Процесс также можно создать с помощью функции [**параметр CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) или [**креатепроцессвислогонв**](/windows/desktop/api/WinBase/nf-winbase-createprocesswithlogonw) .</span><span class="sxs-lookup"><span data-stu-id="ac810-111">You can also create a process using the [**CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) or [**CreateProcessWithLogonW**](/windows/desktop/api/WinBase/nf-winbase-createprocesswithlogonw) function.</span></span> <span data-ttu-id="ac810-112">Это позволяет указать контекст безопасности учетной записи пользователя, в которой будет выполняться процесс.</span><span class="sxs-lookup"><span data-stu-id="ac810-112">This allows you to specify the security context of the user account in which the process will execute.</span></span>

 

 
