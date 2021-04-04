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
# <a name="creating-processes"></a>Создание процессов

Функция [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) создает новый процесс, который выполняется независимо от процесса создания. Однако для простоты связь называется связью типа «родители-потомки».

В следующем коде показано, как создать процесс.


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



Если функция [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) завершается, возвращается структура [**\_ сведений о процессе**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information) , содержащая дескрипторы и идентификаторы для нового процесса и его основного потока. Дескрипторы потоков и процессов создаются с правами полного доступа, хотя доступ можно ограничить, если указать дескрипторы безопасности. Если эти дескрипторы больше не нужны, закройте их с помощью функции [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .

Процесс также можно создать с помощью функции [**параметр CreateProcessAsUser**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) или [**креатепроцессвислогонв**](/windows/desktop/api/WinBase/nf-winbase-createprocesswithlogonw) . Это позволяет указать контекст безопасности учетной записи пользователя, в которой будет выполняться процесс.

 

 
