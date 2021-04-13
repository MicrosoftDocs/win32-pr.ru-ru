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
# <a name="enumerating-all-modules-for-a-process"></a>Перечисление всех модулей для процесса

Чтобы определить, какие процессы загрузили определенную библиотеку DLL, необходимо перечислить модули для каждого процесса. В следующем примере кода функция [**енумпроцессмодулес**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) используется для перечисления модулей текущих процессов в системе.


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



Функция Main получает список процессов с помощью функции [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) . Для каждого процесса функция Main вызывает функцию Принтмодулес, передавая ей идентификатор процесса. Принтмодулес, в свою очередь, вызывает функцию [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) для получения маркера процесса. Если **OpenProcess** завершается сбоем, в выходных данных отображается только идентификатор процесса. Например, **OpenProcess** не работает для процессов бездействия и CSRSS, так как их ограничения доступа не позволяют коду на уровне пользователя открывать их. Затем Принтмодулес вызывает функцию [**енумпроцессмодулес**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) для получения функции Handles модуля. Наконец, Принтмодулес вызывает функцию [**жетмодулефиленамикс**](/windows/desktop/api/Psapi/nf-psapi-getmodulefilenameexa) по одному разу для каждого модуля, чтобы получить имена модулей.

 

 