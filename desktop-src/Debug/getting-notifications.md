---
description: В следующем коде показано, как получить подробные сведения о состоянии из обработчика символов о поиске и загрузке модулей и соответствующих файлов символов.
ms.assetid: 1dd8af0e-280b-4fc4-bf75-45c5c7517365
title: Получение уведомлений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bebaed2683f329fa267bdc926063d0b763190400
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262767"
---
# <a name="getting-notifications"></a>Получение уведомлений

В следующем коде показано, как получить подробные сведения о состоянии из обработчика символов о поиске и загрузке модулей и соответствующих файлов символов.

Многие знакомые с отладчиком WinDbg могут запомнить команду "! SYM шумный". Эта команда используется пользователем для определения того, почему WinDbg не может загружать файлы символов. В нем показан подробный список всех попыток обработчика символов.

Этот же список также доступен всем, кто разрабатывает клиент для обработчика символов DbgHelp.

Сначала вызовите [**симсетоптионс**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) с помощью **симопт \_ Debug**. Это приводит к тому, что DbgHelp включает отладочные уведомления.

После вызова [**симинитиализе**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize)используйте [**SymRegisterCallback64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symregistercallback) для регистрации функции обратного вызова, которую DBGHELP будет вызывать каждый раз при возникновении интересного события. В этом примере функция обратного вызова называется [*SymRegisterCallbackProc64*](/windows/desktop/api/DbgHelp/nc-dbghelp-psymbol_registered_callback). Функциям обратного вызова символов передаются различные коды действий, которые они могут обрабатывались в соответствии с типом. В этом примере мы обрабатываем только код действия **\_ события CBA** . Эта функция передает строку, содержащую подробные сведения о событии, которое произошло в процессе загрузки символа. Это событие может быть любым из попытки прочитать данные в исполняемом образе до успешного расположения файла символов. **SymRegisterCallbackProc64** отображает эту строку и возвращает **значение true**.

> [!IMPORTANT]
> Убедитесь, что вы возвращаете **значение false** для каждого кода действия, который не обрабатывается, в противном случае может возникнуть неопределенное поведение. Список всех кодов действий и их последствия см. в разделе [*SymRegisterCallbackProc64*](/windows/desktop/api/DbgHelp/nc-dbghelp-psymbol_registered_callback) .

 

Теперь, когда обратный вызов зарегистрирован, можно загрузить модуль, указанный в командной строке, вызвав [**симлоадмодуликс**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex).

Наконец, вызовите [**симклеануп**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup) перед выходом.


```C++
#include <windows.h>
#include <stdio.h>
#include <tchar.h>

#ifdef UNICODE
 #define DBGHELP_TRANSLATE_TCHAR
#endif
#include <dbghelp.h>

// Here is an implementation of a Symbol Callback function.

BOOL 
CALLBACK 
SymRegisterCallbackProc64(
    __in HANDLE hProcess,
    __in ULONG ActionCode,
    __in_opt ULONG64 CallbackData,
    __in_opt ULONG64 UserContext
    )
{
    UNREFERENCED_PARAMETER(hProcess);
    UNREFERENCED_PARAMETER(UserContext);
    
    PIMAGEHLP_CBA_EVENT evt;

    // If SYMOPT_DEBUG is set, then the symbol handler will pass
    // verbose information on its attempt to load symbols.
    // This information be delivered as text strings.
    
    switch (ActionCode)
    {
    case CBA_EVENT:
        evt = (PIMAGEHLP_CBA_EVENT)CallbackData;
        _tprintf(_T("%s"), (PTSTR)evt->desc);
        break;

    // CBA_DEBUG_INFO is the old ActionCode for symbol spew.
    // It still works, but we use CBA_EVENT in this example.
#if 0
    case CBA_DEBUG_INFO:
        _tprintf(_T("%s"), (PTSTR)CallbackData);
        break;
#endif

    default:
        // Return false to any ActionCode we don't handle
        // or we could generate some undesirable behavior.
        return FALSE;
    }

    return TRUE;
}

// Main code.

int __cdecl
#ifdef UNICODE
_tmain(
#else
main(
#endif
    __in int argc,
    __in_ecount(argc) PCTSTR argv[]
    )
{
    BOOL status;
    int rc = -1;
    HANDLE hProcess;
    DWORD64 module;
    
    if (argc < 2)
    {
        _tprintf(_T("You must specify an executable image to load.\n"));
        return rc;
    }

    // If we want to se debug spew, we need to set this option.
        
    SymSetOptions(SYMOPT_DEBUG);
    
    // We are not debugging an actual process, so lets use a placeholder
    // value of 1 for hProcess just to ID these calls from any other
    // series we may want to load.  For this simple case, anything will do.
    
    hProcess = (HANDLE)1;
    
    // Initialize the symbol handler.  No symbol path.  
    // Just let dbghelp use _NT_SYMBOL_PATH
    
    status = SymInitialize(hProcess, NULL, false);
    if (!status)
    {
        _tprintf(_T("Error 0x%x calling SymInitialize.\n"), GetLastError());
        return rc;
    }
     
    // Now register our callback.
    
    status = SymRegisterCallback64(hProcess, SymRegisterCallbackProc64, NULL);
    if (!status)
    {
        _tprintf(_T("Error 0x%x calling SymRegisterCallback64.\n"), GetLastError());
        goto cleanup;
    }
    
    // Go ahead and load a module for testing.
    
    module = SymLoadModuleEx(hProcess,  // our unique id
                             NULL,      // no open file handle to image
                             argv[1],   // name of image to load
                             NULL,      // no module name - dbghelp will get it
                             0,         // no base address - dbghelp will get it
                             0,         // no module size - dbghelp will get it
                             NULL,      // no special MODLOAD_DATA structure
                             0);        // flags
    if (!module)
    {
        _tprintf(_T("Error 0x%x calling SymLoadModuleEx.\n"), GetLastError());
        goto cleanup;
    }
    rc = 0;
    
cleanup:
    SymCleanup(hProcess);
    
    return rc;    
}
```



Указание **значения NULL** в качестве второго параметра [**симинитиализе**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) указывает, что обработчик символов должен использовать путь поиска по умолчанию для поиска файлов символов. Подробные сведения о том, как обработчик символов находит файлы символов или как приложение может указать путь поиска символов, см. в разделе [пути к символам](symbol-paths.md).

Выполнение этой программы показывает, как обрабатывается путь к символам. Так как DbgHelp просматривает путь к символам, чтобы найти файл символов, он многократно вызывает [*SymRegisterCallbackProc64*](/windows/desktop/api/DbgHelp/nc-dbghelp-psymbol_registered_callback) , который, в свою очередь, отображает следующие строки, передаваемые dbghelp.

``` syntax
d:\load.exe c:\home\dbghelp.dll
DBGHELP: No header for c:\home\dbghelp.dll.  Searching for image on disk
DBGHELP: c:\home\dbghelp.dll - OK
DBGHELP: .\dbghelp.pdb - file not found
DBGHELP: .\dll\dbghelp.pdb - file not found
DBGHELP: .\symbols\dll\dbghelp.pdb - file not found
DBGHELP: .\symbols\dll\dbghelp.pdb - file not found
DBGHELP: cache*c:\symbols\dbghelp.pdb - file not found
DBGHELP: cache*c:\symbols\dll\dbghelp.pdb - file not found
DBGHELP: cache*c:\symbols\symbols\dll\dbghelp.pdb - file not found
DBGHELP: d:\nt.binaries.amd64chk\symbols.pri\dbg\dbghelp.pdb - file not found
DBGHELP: dbghelp - private symbols & lines
         dbghelp.pdb
```

 

 



