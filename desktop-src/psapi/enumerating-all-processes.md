---
title: Перечисление всех процессов
description: В следующем примере кода функция EnumProcesses используется для перечисления текущих процессов в системе.
ms.assetid: 0ed81548-4936-40e9-bfc8-baa71492310e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf03fd9ad06bfb15924f3f5ec92d8f8858fbff60
ms.sourcegitcommit: 07ba02719c9779e082b108ae74f9699fb0236c34
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/06/2021
ms.locfileid: "108644116"
---
# <a name="enumerating-all-processes"></a><span data-ttu-id="92d13-103">Перечисление всех процессов</span><span class="sxs-lookup"><span data-stu-id="92d13-103">Enumerating All Processes</span></span>

<span data-ttu-id="92d13-104">В следующем примере кода функция [**EnumProcesses**](/windows/win32/api/Psapi/nf-psapi-enumprocesses) используется для получения идентификатора процесса для каждого объекта процесса в системе.</span><span class="sxs-lookup"><span data-stu-id="92d13-104">The following sample code uses the [**EnumProcesses**](/windows/win32/api/Psapi/nf-psapi-enumprocesses) function to retrieve the process identifier for each process object in the system.</span></span> <span data-ttu-id="92d13-105">Затем вызывается [енумпроцессмодулес](/windows/win32/api/psapi/nf-psapi-enumprocessmodules) для получения имени каждого процесса и его печати.</span><span class="sxs-lookup"><span data-stu-id="92d13-105">[EnumProcessModules](/windows/win32/api/psapi/nf-psapi-enumprocessmodules) is then called to get each process name and print it.</span></span>

>[!NOTE]
> <span data-ttu-id="92d13-106">Для 64 разрядных процессов используйте функцию [енумпроцессмодулесекс](/windows/win32/api/psapi/nf-psapi-enumprocessmodulesex) .</span><span class="sxs-lookup"><span data-stu-id="92d13-106">For 64 bit processes, use the [EnumProcessModulesEx](/windows/win32/api/psapi/nf-psapi-enumprocessmodulesex) function.</span></span>

```C++
#include <windows.h>
#include <stdio.h>
#include <tchar.h>
#include <psapi.h>

// To ensure correct resolution of symbols, add Psapi.lib to TARGETLIBS
// and compile with -DPSAPI_VERSION=1

void PrintProcessNameAndID( DWORD processID )
{
    TCHAR szProcessName[MAX_PATH] = TEXT("<unknown>");

    // Get a handle to the process.

    HANDLE hProcess = OpenProcess( PROCESS_QUERY_INFORMATION |
                                   PROCESS_VM_READ,
                                   FALSE, processID );

    // Get the process name.

    if (NULL != hProcess )
    {
        HMODULE hMod;
        DWORD cbNeeded;

        if ( EnumProcessModules( hProcess, &hMod, sizeof(hMod), 
             &cbNeeded) )
        {
            GetModuleBaseName( hProcess, hMod, szProcessName, 
                               sizeof(szProcessName)/sizeof(TCHAR) );
        }
    }

    // Print the process name and identifier.

    _tprintf( TEXT("%s  (PID: %u)\n"), szProcessName, processID );

    // Release the handle to the process.

    CloseHandle( hProcess );
}

int main( void )
{
    // Get the list of process identifiers.

    DWORD aProcesses[1024], cbNeeded, cProcesses;
    unsigned int i;

    if ( !EnumProcesses( aProcesses, sizeof(aProcesses), &cbNeeded ) )
    {
        return 1;
    }


    // Calculate how many process identifiers were returned.

    cProcesses = cbNeeded / sizeof(DWORD);

    // Print the name and process identifier for each process.

    for ( i = 0; i < cProcesses; i++ )
    {
        if( aProcesses[i] != 0 )
        {
            PrintProcessNameAndID( aProcesses[i] );
        }
    }

    return 0;
}
```



<span data-ttu-id="92d13-107">Функция Main получает список процессов с помощью функции [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) .</span><span class="sxs-lookup"><span data-stu-id="92d13-107">The main function obtains a list of processes by using the [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) function.</span></span> <span data-ttu-id="92d13-108">Для каждого процесса Main вызывает функцию **принтпроцесснамеандид** , передавая ей идентификатор процесса.</span><span class="sxs-lookup"><span data-stu-id="92d13-108">For each process, main calls the **PrintProcessNameAndID** function, passing it the process identifier.</span></span> <span data-ttu-id="92d13-109">**Принтпроцесснамеандид** , в свою очередь, вызывает функцию [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) для получения маркера процесса.</span><span class="sxs-lookup"><span data-stu-id="92d13-109">**PrintProcessNameAndID** in turn calls the [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) function to obtain the process handle.</span></span> <span data-ttu-id="92d13-110">Если **OpenProcess** завершается сбоем, в выходных данных отображается имя процесса в виде <unknown> .</span><span class="sxs-lookup"><span data-stu-id="92d13-110">If **OpenProcess** fails, the output shows the process name as <unknown>.</span></span> <span data-ttu-id="92d13-111">Например, **OpenProcess** не работает для процессов бездействия и CSRSS, так как их ограничения доступа не позволяют коду на уровне пользователя открывать их.</span><span class="sxs-lookup"><span data-stu-id="92d13-111">For example, **OpenProcess** fails for the Idle and CSRSS processes because their access restrictions prevent user-level code from opening them.</span></span> <span data-ttu-id="92d13-112">Затем **принтпроцесснамеандид** вызывает функцию [**енумпроцессмодулес**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) для получения дескрипторов модуля.</span><span class="sxs-lookup"><span data-stu-id="92d13-112">Next, **PrintProcessNameAndID** calls the [**EnumProcessModules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) function to obtain the module handles.</span></span> <span data-ttu-id="92d13-113">Наконец, **принтпроцесснамеандид** вызывает функцию [**жетмодулебасенаме**](/windows/desktop/api/Psapi/nf-psapi-getmodulebasenamea) для получения имени исполняемого файла и отображает имя вместе с идентификатором процесса.</span><span class="sxs-lookup"><span data-stu-id="92d13-113">Finally, **PrintProcessNameAndID** calls the [**GetModuleBaseName**](/windows/desktop/api/Psapi/nf-psapi-getmodulebasenamea) function to obtain the name of the executable file and displays the name along with the process identifier.</span></span>

 

 
