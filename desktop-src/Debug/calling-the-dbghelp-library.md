---
description: несмотря на то, что DbgHelp.dll поставляется со всеми версиями Windows, вызывающие объекты должны использовать одну из более новых версий библиотеки DLL, которая находится в пакете средств отладки для Windows. Дополнительные сведения о распространении DbgHelp см. в разделе версии DbgHelp.
ms.assetid: 4e615e75-5ab8-4155-a3d3-b96313b37e9b
title: Вызов библиотеки DbgHelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4d6a111da8b0874a0c66fa08840e1ea4edeabf539afab2e9decf0eb19372db3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957163"
---
# <a name="calling-the-dbghelp-library"></a>Вызов библиотеки DbgHelp

несмотря на то, что DbgHelp.dll поставляется со всеми версиями Windows, вызывающие объекты должны использовать одну из более новых версий библиотеки DLL, которая находится в пакете [средств отладки для Windows](https://www.microsoft.com/?ref=go) . Дополнительные сведения о распространении DbgHelp см. в разделе [версии dbghelp](dbghelp-versions.md).

при использовании DbgHelp оптимальной стратегией является установка копии библиотеки из пакета [средств отладки для Windows](https://www.microsoft.com/?ref=go) в каталоге приложения логически рядом с программным обеспечением, которое его вызывает. Если также требуются сервер символов и исходный сервер, то оба SymSrv.dll и SrcSrv.dll должны быть установлены в одном каталоге с DbgHelp.dll, так как DbgHelp будет вызывать эти библиотеки только в том случае, если они совместно используют один и тот же каталог. (Обратите внимание, что DbgHelp не будет вызывать эти две библиотеки DLL из стандартного пути поиска.) Это помогает предотвратить использование несоответствующих библиотек DLL. Аналогично, он также повышает безопасность в целом.

Следующий код извлекается из источника DbgHelp. В нем показано, как DbgHelp загружает только версии SymSrv.dll и SrcSrv.dll из того же каталога, в котором находится DbgHelp.dll.


```C++
HINSTANCE ghinst;

// For calculating the size of arrays for safe string functions.

#ifndef cch
 #define ccht(Array, EltType) (sizeof(Array) / sizeof(EltType))
 #define cch(Array) ccht(Array, (Array)[0])
#endif

//
// LoadLibrary() a DLL, using the same directory as dbghelp.dll.
//

HMODULE 
LoadDLL(
    __in PCWSTR filename
    )
{
    WCHAR drive[10] = L"";
    WCHAR dir[MAX_PATH + 1] = L"";
    WCHAR file[MAX_PATH + 1] = L"";
    WCHAR ext[MAX_PATH + 1] = L"";
    WCHAR path[MAX_PATH + 1] = L"";
    HMODULE hm;
    
    // Chop up 'filename' into its elements.
    
    _wsplitpath_s(filename, drive, cch(drive), dir, cch(dir), file, cch(file), ext, cch(ext));

    // If 'filename' contains no path information, then get the path to our module and 
    // use it to create a fully qualified path to the module we are loading.  Then load it.
    
    if (!*drive && !*dir) 
    {
        // ghinst is the HINSTANCE of this module, initialized in DllMain or WinMain
         
        if (GetModuleFileNameW(ghinst, path, MAX_PATH)) 
        {
            _wsplitpath_s(path, drive, cch(drive), dir, cch(dir), NULL, 0, NULL, 0);
            if (*drive || *dir) 
            {
                swprintf_s(path, cch(path), L"%s%s%s%s", drive, dir, file, ext);
                hm = LoadLibrary(path);
                if (hm)
                    return hm;
            }
        }
    }
    else
    {
        // If we wanted to, we could have LoadDLL also support directories being specified
        // in 'filename'.  We could pass the path here.  The result is if no path is specified,
        // the module path is used as above, otherwise the path in 'filename' is specified.
        // But the standard search logic of LoadLibrary is still avoided.
        
        /*
        hm = LoadLibrary(path);
        if (hm)
            return hm;
        */
    }
    
    return 0;
}
```



После загрузки этих двух библиотек DLL DbgHelp вызывает [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) для получения необходимых ей функций.

Как правило, код, вызывающий DbgHelp.dll, обеспечивает загрузку необходимой версии путем установки DbgHelp.dll в том же каталоге, что и приложение, которое инициировало текущий процесс. Если вызывающий код находится в библиотеке DLL и не имеет доступа или знаний о расположении начального процесса, то DbgHelp.dll должны быть установлены вместе с вызывающей библиотекой DLL, а также должен использоваться код, аналогичный DbgHelp Лоаддлл.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Версии DbgHelp](dbghelp-versions.md)
</dt> <dt>

[**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)
</dt> </dl>

 

 
