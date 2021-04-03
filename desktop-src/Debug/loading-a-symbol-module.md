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
# <a name="loading-a-symbol-module"></a>Загрузка модуля символов

Если приложение не вызывает функцию [**симинитиализе**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) с параметром *финвадепроцесс* , установленным в **значение true**, он должен загружать символы для модуля, когда они требуются. Чтобы загрузить модуль символов по требованию, приложение может вызвать функцию [**симлоадмодуликс**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) с полным путем к имени модуля. При загрузке модуля обработчик символов загружает символы немедленно или откладывает нагрузку, в зависимости от параметров, заданных с помощью функции [**симсетоптионс**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) .

Следующий код загружает модуль символов. Обратите внимание, что предполагается, что обработчик символов инициализирован с помощью кода при [инициализации обработчика символов](initializing-the-symbol-handler.md).


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



Обратите внимание, что *сзимаженаме* может быть путем к любому исполняемому модулю, имеющему отладочную информацию (exe, DLL, DRV, sys, SCR,. cpl,. com). Кроме того, *двбасеаддр* является базовым адресом модуля символов для загрузки. Если это значение равно 0, обработчик символов будет получать базовый адрес из указанного модуля символов.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Выгрузка модуля символов](unloading-a-symbol-module.md)
</dt> </dl>

 

 



