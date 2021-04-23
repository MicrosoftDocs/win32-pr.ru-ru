---
description: После создания библиотеки DLL можно использовать функции, которые она определяет в приложении. Ниже приведено простое консольное приложение, использующее функцию Мипутс, экспортированную из Myputs.dll (см. раздел Создание простой библиотеки Dynamic-Link).
ms.assetid: d67000c2-21ca-49c2-86f1-708f33003d1e
title: Использование Load-Time динамической компоновки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e31e5d14ba2190528c44d892b957d22b273fd4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662751"
---
# <a name="using-load-time-dynamic-linking"></a><span data-ttu-id="95d5f-104">Использование Load-Time динамической компоновки</span><span class="sxs-lookup"><span data-stu-id="95d5f-104">Using Load-Time Dynamic Linking</span></span>

<span data-ttu-id="95d5f-105">После создания библиотеки DLL можно использовать функции, которые она определяет в приложении.</span><span class="sxs-lookup"><span data-stu-id="95d5f-105">After you have created a DLL, you can use the functions it defines in an application.</span></span> <span data-ttu-id="95d5f-106">Ниже приведено простое консольное приложение, использующее функцию Мипутс, экспортированную из Myputs.dll (см. раздел [Создание простой библиотеки Dynamic-Link](creating-a-simple-dynamic-link-library.md)).</span><span class="sxs-lookup"><span data-stu-id="95d5f-106">The following is a simple console application that uses the myPuts function exported from Myputs.dll (see [Creating a Simple Dynamic-Link Library](creating-a-simple-dynamic-link-library.md)).</span></span>

<span data-ttu-id="95d5f-107">Так как в этом примере функция DLL вызывается явным образом, модуль для приложения должен быть связан с библиотекой импорта Мипутс. lib.</span><span class="sxs-lookup"><span data-stu-id="95d5f-107">Because this example calls the DLL function explicitly, the module for the application must be linked with the import library Myputs.lib.</span></span> <span data-ttu-id="95d5f-108">Дополнительные сведения о создании библиотек DLL см. в документации, входящей в состав средств разработки.</span><span class="sxs-lookup"><span data-stu-id="95d5f-108">For more information about building DLLs, see the documentation included with your development tools.</span></span>


```C++
#include <windows.h> 

extern "C" int __cdecl myPuts(LPWSTR);   // a function from a DLL

int main(VOID) 
{ 
    int Ret = 1;

    Ret = myPuts(L"Message sent to the DLL function\n"); 
    return Ret;
}
```



## <a name="related-topics"></a><span data-ttu-id="95d5f-109">См. также</span><span class="sxs-lookup"><span data-stu-id="95d5f-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95d5f-110">Динамическая компоновка во время загрузки</span><span class="sxs-lookup"><span data-stu-id="95d5f-110">Load-Time Dynamic Linking</span></span>](load-time-dynamic-linking.md)
</dt> </dl>

 

 



