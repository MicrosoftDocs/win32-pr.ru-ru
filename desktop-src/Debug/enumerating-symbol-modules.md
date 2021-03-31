---
description: В следующем коде перечислены модули, загруженные функцией SymLoadModule64 или Симинитиализе.
ms.assetid: 8c7fdfaa-d4d3-42d6-ad19-23e8ffda7bf4
title: Перечисление модулей символов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43623a7409116450fccc822bbc0bef1a309fbd2a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104495798"
---
# <a name="enumerating-symbol-modules"></a><span data-ttu-id="04d00-103">Перечисление модулей символов</span><span class="sxs-lookup"><span data-stu-id="04d00-103">Enumerating Symbol Modules</span></span>

<span data-ttu-id="04d00-104">В следующем коде перечислены модули, загруженные функцией [**SymLoadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule) или [**симинитиализе**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) .</span><span class="sxs-lookup"><span data-stu-id="04d00-104">The following code lists the modules that have been loaded by the [**SymLoadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule) or [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) function.</span></span> <span data-ttu-id="04d00-105">Функция [**SymEnumerateModules64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules) требует функцию обратного вызова, которая будет вызываться один раз для каждого загруженного модуля.</span><span class="sxs-lookup"><span data-stu-id="04d00-105">The [**SymEnumerateModules64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symenumeratemodules) function requires a callback function, which will be called once for each module loaded.</span></span> <span data-ttu-id="04d00-106">В этом примере EnumModules является реализацией функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="04d00-106">In this example, EnumModules is an implementation of the callback function.</span></span> <span data-ttu-id="04d00-107">В примере предполагается, что обработчик символов инициализирован с помощью кода при [инициализации обработчика символов](initializing-the-symbol-handler.md).</span><span class="sxs-lookup"><span data-stu-id="04d00-107">The example assumes you have initialized the symbol handler using the code in [Initializing the Symbol Handler](initializing-the-symbol-handler.md).</span></span>


```C++
BOOL CALLBACK EnumModules(
    PCTSTR  ModuleName, 
    DWORD64 BaseOfDll,  
    PVOID   UserContext )
{
    UNREFERENCED_PARAMETER(UserContext);
    
    _tprintf(TEXT("%08X %s\n"), BaseOfDll, ModuleName);
    return TRUE;
}


if (SymEnumerateModules64(hProcess, EnumModules, NULL))
{
    // SymEnumerateModules64 returned success
}
else
{
    // SymEnumerateModules64 failed
    error = GetLastError();
    _tprintf(TEXT("SymEnumerateModules64 returned error : %d\n"), error);
}
```



 

 



