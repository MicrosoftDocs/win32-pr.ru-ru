---
description: Следующий код выгружает модуль символов, на который ссылается адрес модуля Басеофдлл, с помощью SymUnloadModule64.
ms.assetid: f185ae64-1de9-4139-acd5-7c3a108e1eba
title: Выгрузка модуля символов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d84b6fad0177fce36865e90dadf04bd563130789
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895906"
---
# <a name="unloading-a-symbol-module"></a><span data-ttu-id="49ad6-103">Выгрузка модуля символов</span><span class="sxs-lookup"><span data-stu-id="49ad6-103">Unloading a Symbol Module</span></span>

<span data-ttu-id="49ad6-104">Следующий код выгружает модуль символов, на который ссылается адрес модуля Басеофдлл, с помощью [**SymUnloadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symunloadmodule).</span><span class="sxs-lookup"><span data-stu-id="49ad6-104">The following code unloads a symbol module referred to by the BaseOfDll module address using [**SymUnloadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symunloadmodule).</span></span>


```C++
if (SymUnloadModule64(hProcess, BaseOfDll))
{
    // SymUnloadModule64 returned success
}
else
{
    // SymUnloadModule64 failed
    DWORD error = GetLastError();
    printf("SymUnloadModule64 returned error : %d\n", error);
}
```



## <a name="related-topics"></a><span data-ttu-id="49ad6-105">См. также</span><span class="sxs-lookup"><span data-stu-id="49ad6-105">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49ad6-106">Загрузка модуля символов</span><span class="sxs-lookup"><span data-stu-id="49ad6-106">Loading a Symbol Module</span></span>](loading-a-symbol-module.md)
</dt> </dl>

 

 



