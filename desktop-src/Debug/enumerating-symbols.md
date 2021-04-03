---
description: В следующем коде отображается имя, адрес и размер каждого загруженного символа в указанном модуле.
ms.assetid: 6ecdbd1e-406a-453e-9037-707ceb72074a
title: Перечисление символов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33f9a98f37ca5ef2249f68ffa9b8ef73198de242
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990322"
---
# <a name="enumerating-symbols"></a><span data-ttu-id="70b33-103">Перечисление символов</span><span class="sxs-lookup"><span data-stu-id="70b33-103">Enumerating Symbols</span></span>

<span data-ttu-id="70b33-104">В следующем коде отображается имя, адрес и размер каждого загруженного символа в указанном модуле.</span><span class="sxs-lookup"><span data-stu-id="70b33-104">The following code displays the name, address, and size of each loaded symbol in the specified module.</span></span> <span data-ttu-id="70b33-105">Функция [**сименумсимболс**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols) требует функцию обратного вызова, которая вызывается по одному разу для каждого загруженного модуля.</span><span class="sxs-lookup"><span data-stu-id="70b33-105">The [**SymEnumSymbols**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumsymbols) function requires a callback function, which is called once for each module loaded.</span></span> <span data-ttu-id="70b33-106">В этом примере Енумсимпрок является реализацией функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="70b33-106">In this example, EnumSymProc is an implementation of the callback function.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <dbghelp.h>

BOOL CALLBACK EnumSymProc( 
    PSYMBOL_INFO pSymInfo,   
    ULONG SymbolSize,      
    PVOID UserContext)
{
    UNREFERENCED_PARAMETER(UserContext);
    
    printf("%08X %4u %s\n", 
           pSymInfo->Address, SymbolSize, pSymInfo->Name);
    return TRUE;
}

void main()
{
    HANDLE hProcess = GetCurrentProcess();
    DWORD64 BaseOfDll;
    char *Mask = "*";
    BOOL status;

    status = SymInitialize(hProcess, NULL, FALSE);
    if (status == FALSE)
    {
        return;
    }
    
    BaseOfDll = SymLoadModuleEx(hProcess,
                                NULL,
                                "foo.dll",
                                NULL,
                                0,
                                0,
                                NULL,
                                0);
                                
    if (BaseOfDll == 0)
    {
        SymCleanup(hProcess);
        return;
    }                                
        
    if (SymEnumSymbols(hProcess,     // Process handle from SymInitialize.
                        BaseOfDll,   // Base address of module.
                        Mask,        // Name of symbols to match.
                        EnumSymProc, // Symbol handler procedure.
                        NULL))       // User context.
    {
        // SymEnumSymbols succeeded
    }
    else
    {
        // SymEnumSymbols failed
        printf("SymEnumSymbols failed: %d\n", GetLastError());
    }
    
    SymCleanup(hProcess);
}
```



 

 



