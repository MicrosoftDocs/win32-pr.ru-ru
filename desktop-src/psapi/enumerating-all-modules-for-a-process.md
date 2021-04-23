---
title: Перечисление всех модулей для процесса
description: Чтобы определить, какие процессы загрузили определенную библиотеку DLL, необходимо перечислить модули для каждого процесса. В следующем примере кода функция Енумпроцессмодулес используется для перечисления модулей текущих процессов в системе.
ms.assetid: 2e411eba-ba60-4678-bf6f-bc15b6e8b478
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bf09d02d4ae9dc7e55177653e05e3d19df4ab7b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337500"
---
# <a name="enumerating-all-modules-for-a-process"></a><span data-ttu-id="d9dca-104">Перечисление всех модулей для процесса</span><span class="sxs-lookup"><span data-stu-id="d9dca-104">Enumerating All Modules For a Process</span></span>

<span data-ttu-id="d9dca-105">Чтобы определить, какие процессы загрузили определенную библиотеку DLL, необходимо перечислить модули для каждого процесса.</span><span class="sxs-lookup"><span data-stu-id="d9dca-105">To determine which processes have loaded a particular DLL, you must enumerate the modules for each process.</span></span> <span data-ttu-id="d9dca-106">В следующем примере кода функция [**енумпроцессмодулес**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) используется для перечисления модулей текущих процессов в системе.</span><span class="sxs-lookup"><span data-stu-id="d9dca-106">The following sample code uses the [**EnumProcessModules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) function to enumerate the modules of current processes in the system.</span></span>


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>
#include <psapi.h>

// To ensure correct resolution of symbols, add Psapi.lib to TARGETLIBS
// and compile with -DPSAPI_VERSION=1

int PrintModules( DWORD processID )
{
    HMODULE hMods[1024];
    HANDLE hProcess;
    DWORD cbNeeded;
    unsigned int i;

    // Print the process identifier.

    printf( "\nProcess ID: %u\n", processID );

    // Get a handle to the process.

    hProcess = OpenProcess( PROCESS_QUERY_INFORMATION |
                            PROCESS_VM_READ,
                            FALSE, processID );
    if (NULL == hProcess)
        return 1;

   // Get a list of all the modules in this process.

    if( EnumProcessModules(hProcess, hMods, sizeof(hMods), &cbNeeded))
    {
        for ( i = 0; i < (cbNeeded / sizeof(HMODULE)); i++ )
        {
            TCHAR szModName[MAX_PATH];

            // Get the full path to the module's file.

            if ( GetModuleFileNameEx( hProcess, hMods[i], szModName,
                                      sizeof(szModName) / sizeof(TCHAR)))
            {
                // Print the module name and handle value.

                _tprintf( TEXT("\t%s (0x%08X)\n"), szModName, hMods[i] );
            }
        }
    }
    
    // Release the handle to the process.

    CloseHandle( hProcess );

    return 0;
}

int main( void )
{

    DWORD aProcesses[1024]; 
    DWORD cbNeeded; 
    DWORD cProcesses;
    unsigned int i;

    // Get the list of process identifiers.

    if ( !EnumProcesses( aProcesses, sizeof(aProcesses), &cbNeeded ) )
        return 1;

    // Calculate how many process identifiers were returned.

    cProcesses = cbNeeded / sizeof(DWORD);

    // Print the names of the modules for each process.

    for ( i = 0; i < cProcesses; i++ )
    {
        PrintModules( aProcesses[i] );
    }

    return 0;
}
```



<span data-ttu-id="d9dca-107">Функция Main получает список процессов с помощью функции [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) .</span><span class="sxs-lookup"><span data-stu-id="d9dca-107">The main function obtains a list of processes by using the [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) function.</span></span> <span data-ttu-id="d9dca-108">Для каждого процесса функция Main вызывает функцию Принтмодулес, передавая ей идентификатор процесса.</span><span class="sxs-lookup"><span data-stu-id="d9dca-108">For each process, the main function calls the PrintModules function, passing it the process identifier.</span></span> <span data-ttu-id="d9dca-109">Принтмодулес, в свою очередь, вызывает функцию [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) для получения маркера процесса.</span><span class="sxs-lookup"><span data-stu-id="d9dca-109">PrintModules in turn calls the [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) function to obtain the process handle.</span></span> <span data-ttu-id="d9dca-110">Если **OpenProcess** завершается сбоем, в выходных данных отображается только идентификатор процесса.</span><span class="sxs-lookup"><span data-stu-id="d9dca-110">If **OpenProcess** fails, the output shows only the process identifier.</span></span> <span data-ttu-id="d9dca-111">Например, **OpenProcess** не работает для процессов бездействия и CSRSS, так как их ограничения доступа не позволяют коду на уровне пользователя открывать их.</span><span class="sxs-lookup"><span data-stu-id="d9dca-111">For example, **OpenProcess** fails for the Idle and CSRSS processes because their access restrictions prevent user-level code from opening them.</span></span> <span data-ttu-id="d9dca-112">Затем Принтмодулес вызывает функцию [**енумпроцессмодулес**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) для получения функции Handles модуля.</span><span class="sxs-lookup"><span data-stu-id="d9dca-112">Next, PrintModules calls the [**EnumProcessModules**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) function to obtain the module handles function.</span></span> <span data-ttu-id="d9dca-113">Наконец, Принтмодулес вызывает функцию [**жетмодулефиленамикс**](/windows/desktop/api/Psapi/nf-psapi-getmodulefilenameexa) по одному разу для каждого модуля, чтобы получить имена модулей.</span><span class="sxs-lookup"><span data-stu-id="d9dca-113">Finally, PrintModules calls the [**GetModuleFileNameEx**](/windows/desktop/api/Psapi/nf-psapi-getmodulefilenameexa) function, once for each module, to obtain the module names.</span></span>

 

 