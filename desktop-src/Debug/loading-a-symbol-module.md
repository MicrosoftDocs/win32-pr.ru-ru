---
description: Если приложение не вызывает функцию Симинитиализе с параметром Финвадепроцесс, установленным в значение TRUE, он должен загружать символы для модуля, когда они требуются.
ms.assetid: 01cee812-d1f2-4459-acee-bce8719a85b2
title: Загрузка модуля символов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5182322e62b450333a064069ea5f5de2aa95e912
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104140967"
---
# <a name="loading-a-symbol-module"></a><span data-ttu-id="a6fc2-103">Загрузка модуля символов</span><span class="sxs-lookup"><span data-stu-id="a6fc2-103">Loading a Symbol Module</span></span>

<span data-ttu-id="a6fc2-104">Если приложение не вызывает функцию [**симинитиализе**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) с параметром *финвадепроцесс* , установленным в **значение true**, он должен загружать символы для модуля, когда они требуются.</span><span class="sxs-lookup"><span data-stu-id="a6fc2-104">If an application does not call the [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) function with the *fInvadeProcess* parameter set to **TRUE**, it must load symbols for a module when they are required.</span></span> <span data-ttu-id="a6fc2-105">Чтобы загрузить модуль символов по требованию, приложение может вызвать функцию [**симлоадмодуликс**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) с полным путем к имени модуля.</span><span class="sxs-lookup"><span data-stu-id="a6fc2-105">To load a symbol module on demand, the application can call the [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) function with a full path to a module name.</span></span> <span data-ttu-id="a6fc2-106">При загрузке модуля обработчик символов загружает символы немедленно или откладывает нагрузку, в зависимости от параметров, заданных с помощью функции [**симсетоптионс**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) .</span><span class="sxs-lookup"><span data-stu-id="a6fc2-106">When the module is loaded, the symbol handler will either load the symbols immediately or defer the load, depending on the options set using the [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) function.</span></span>

<span data-ttu-id="a6fc2-107">Следующий код загружает модуль символов.</span><span class="sxs-lookup"><span data-stu-id="a6fc2-107">The following code loads a symbol module.</span></span> <span data-ttu-id="a6fc2-108">Обратите внимание, что предполагается, что обработчик символов инициализирован с помощью кода при [инициализации обработчика символов](initializing-the-symbol-handler.md).</span><span class="sxs-lookup"><span data-stu-id="a6fc2-108">Note that it assumes you have initialized the symbol handler using the code in [Initializing the Symbol Handler](initializing-the-symbol-handler.md).</span></span>


```C++
TCHAR  szImageName[MAX_PATH] = TEXT("foo.dll");
DWORD64 dwBaseAddr = 0;

if (SymLoadModuleEx(hProcess,    // target process 
                    NULL,        // handle to image - not used
                    szImageName, // name of image file
                    NULL,        // name of module - not required
                    dwBaseAddr,  // base address - not required
                    0,           // size of image - not required
                    NULL,        // MODLOAD_DATA used for special cases 
                    0))          // flags - not required
{
    // SymLoadModuleEx returned success
}
else
{
    // SymLoadModuleEx failed
    DWORD error = GetLastError();
    printf("SymLoadModuleEx returned error : %d\n", error);
}
```



<span data-ttu-id="a6fc2-109">Обратите внимание, что *сзимаженаме* может быть путем к любому исполняемому модулю, имеющему отладочную информацию (exe, DLL, DRV, sys, SCR,. cpl,. com).</span><span class="sxs-lookup"><span data-stu-id="a6fc2-109">Note that *szImageName* can be a path to any executable module that has debugging information (.exe, .dll, .drv, .sys, .scr, .cpl, .com).</span></span> <span data-ttu-id="a6fc2-110">Кроме того, *двбасеаддр* является базовым адресом модуля символов для загрузки.</span><span class="sxs-lookup"><span data-stu-id="a6fc2-110">Also, *dwBaseAddr* is the base address of the symbol module to be loaded.</span></span> <span data-ttu-id="a6fc2-111">Если это значение равно 0, обработчик символов будет получать базовый адрес из указанного модуля символов.</span><span class="sxs-lookup"><span data-stu-id="a6fc2-111">If this value is 0, the symbol handler will obtain the base address from the specified symbol module.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a6fc2-112">См. также</span><span class="sxs-lookup"><span data-stu-id="a6fc2-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6fc2-113">Выгрузка модуля символов</span><span class="sxs-lookup"><span data-stu-id="a6fc2-113">Unloading a Symbol Module</span></span>](unloading-a-symbol-module.md)
</dt> </dl>

 

 



