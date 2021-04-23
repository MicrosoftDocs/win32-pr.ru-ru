---
description: Несмотря на то, что DbgHelp.dll поставляется со всеми версиями Windows, вызывающим объектам следует использовать одну из более новых версий этой библиотеки DLL, которая находится в пакете средств отладки для Windows. Дополнительные сведения о распространении DbgHelp см. в разделе версии DbgHelp.
ms.assetid: 4e615e75-5ab8-4155-a3d3-b96313b37e9b
title: Вызов библиотеки DbgHelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70cc06f6a0e28f163d80490647ee8f33754c249b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104495816"
---
# <a name="calling-the-dbghelp-library"></a><span data-ttu-id="10790-104">Вызов библиотеки DbgHelp</span><span class="sxs-lookup"><span data-stu-id="10790-104">Calling the DbgHelp Library</span></span>

<span data-ttu-id="10790-105">Несмотря на то, что DbgHelp.dll поставляется со всеми версиями Windows, вызывающим объектам следует использовать одну из более новых версий этой библиотеки DLL, которая находится в пакете [средств отладки для Windows](https://www.microsoft.com/?ref=go) .</span><span class="sxs-lookup"><span data-stu-id="10790-105">Although DbgHelp.dll ships with all versions of Windows, callers should consider using one of the more recent versions of this DLL as found in the [Debugging Tools For Windows](https://www.microsoft.com/?ref=go) package.</span></span> <span data-ttu-id="10790-106">Дополнительные сведения о распространении DbgHelp см. в разделе [версии dbghelp](dbghelp-versions.md).</span><span class="sxs-lookup"><span data-stu-id="10790-106">For details on distribution of DbgHelp, see [DbgHelp Versions](dbghelp-versions.md).</span></span>

<span data-ttu-id="10790-107">При использовании DbgHelp оптимальной стратегией является установка копии библиотеки из пакета [средств отладки для Windows](https://www.microsoft.com/?ref=go) в каталоге приложения логически рядом с программным обеспечением, которое его вызывает.</span><span class="sxs-lookup"><span data-stu-id="10790-107">When using DbgHelp, the best strategy is to install a copy of the library from the [Debugging Tools For Windows](https://www.microsoft.com/?ref=go) package in the application directory logically adjacent to the software that calls it.</span></span> <span data-ttu-id="10790-108">Если также требуются сервер символов и исходный сервер, то оба SymSrv.dll и SrcSrv.dll должны быть установлены в одном каталоге с DbgHelp.dll, так как DbgHelp будет вызывать эти библиотеки только в том случае, если они совместно используют один и тот же каталог.</span><span class="sxs-lookup"><span data-stu-id="10790-108">If Symbol Server and Source Server are also needed, then both SymSrv.dll and SrcSrv.dll must be installed in the same directory as DbgHelp.dll, as DbgHelp will only call these DLLs if they share the same directory with it.</span></span> <span data-ttu-id="10790-109">(Обратите внимание, что DbgHelp не будет вызывать эти две библиотеки DLL из стандартного пути поиска.) Это помогает предотвратить использование несоответствующих библиотек DLL. Аналогично, он также повышает безопасность в целом.</span><span class="sxs-lookup"><span data-stu-id="10790-109">(Note that DbgHelp will not call these two DLLs from the standard search path.) This helps prevent the usage of mismatched DLLs; likewise, it also improves security overall.</span></span>

<span data-ttu-id="10790-110">Следующий код извлекается из источника DbgHelp.</span><span class="sxs-lookup"><span data-stu-id="10790-110">The following code is extracted from the DbgHelp source.</span></span> <span data-ttu-id="10790-111">В нем показано, как DbgHelp загружает только версии SymSrv.dll и SrcSrv.dll из того же каталога, в котором находится DbgHelp.dll.</span><span class="sxs-lookup"><span data-stu-id="10790-111">It shows how DbgHelp only loads versions of SymSrv.dll and SrcSrv.dll from the same directory that DbgHelp.dll resides in.</span></span>


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



<span data-ttu-id="10790-112">После загрузки этих двух библиотек DLL DbgHelp вызывает [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) для получения необходимых ей функций.</span><span class="sxs-lookup"><span data-stu-id="10790-112">After loading these two DLLs, DbgHelp calls [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) to obtain the functions it needs from them.</span></span>

<span data-ttu-id="10790-113">Как правило, код, вызывающий DbgHelp.dll, обеспечивает загрузку необходимой версии путем установки DbgHelp.dll в том же каталоге, что и приложение, которое инициировало текущий процесс.</span><span class="sxs-lookup"><span data-stu-id="10790-113">Normally, code that calls DbgHelp.dll ensures that the correct version is loaded by installing DbgHelp.dll in the same directory as the application that initiated the current process.</span></span> <span data-ttu-id="10790-114">Если вызывающий код находится в библиотеке DLL и не имеет доступа или знаний о расположении начального процесса, то DbgHelp.dll должны быть установлены вместе с вызывающей библиотекой DLL, а также должен использоваться код, аналогичный DbgHelp Лоаддлл.</span><span class="sxs-lookup"><span data-stu-id="10790-114">If the calling code is in a DLL and does not have access to or knowledge of the location of the initial process, then DbgHelp.dll must be installed alongside the calling DLL and code similar to DbgHelp's LoadDLL should be used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="10790-115">См. также</span><span class="sxs-lookup"><span data-stu-id="10790-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10790-116">Версии DbgHelp</span><span class="sxs-lookup"><span data-stu-id="10790-116">DbgHelp Versions</span></span>](dbghelp-versions.md)
</dt> <dt>

[<span data-ttu-id="10790-117">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="10790-117">**LoadLibrary**</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[<span data-ttu-id="10790-118">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="10790-118">**GetProcAddress**</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[<span data-ttu-id="10790-119">**GetModuleFileName**</span><span class="sxs-lookup"><span data-stu-id="10790-119">**GetModuleFileName**</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)
</dt> </dl>

 

 
