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
# <a name="enumerating-all-processes"></a>Перечисление всех процессов

В следующем примере кода функция [**EnumProcesses**](/windows/win32/api/Psapi/nf-psapi-enumprocesses) используется для получения идентификатора процесса для каждого объекта процесса в системе. Затем вызывается [енумпроцессмодулес](/windows/win32/api/psapi/nf-psapi-enumprocessmodules) для получения имени каждого процесса и его печати.

>[!NOTE]
> Для 64 разрядных процессов используйте функцию [енумпроцессмодулесекс](/windows/win32/api/psapi/nf-psapi-enumprocessmodulesex) .

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



Функция Main получает список процессов с помощью функции [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) . Для каждого процесса Main вызывает функцию **принтпроцесснамеандид** , передавая ей идентификатор процесса. **Принтпроцесснамеандид** , в свою очередь, вызывает функцию [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) для получения маркера процесса. Если **OpenProcess** завершается сбоем, в выходных данных отображается имя процесса в виде <unknown> . Например, **OpenProcess** не работает для процессов бездействия и CSRSS, так как их ограничения доступа не позволяют коду на уровне пользователя открывать их. Затем **принтпроцесснамеандид** вызывает функцию [**енумпроцессмодулес**](/windows/desktop/api/Psapi/nf-psapi-enumprocessmodules) для получения дескрипторов модуля. Наконец, **принтпроцесснамеандид** вызывает функцию [**жетмодулебасенаме**](/windows/desktop/api/Psapi/nf-psapi-getmodulebasenamea) для получения имени исполняемого файла и отображает имя вместе с идентификатором процесса.

 

 
