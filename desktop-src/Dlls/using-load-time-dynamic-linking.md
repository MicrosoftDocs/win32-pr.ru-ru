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
# <a name="using-load-time-dynamic-linking"></a>Использование Load-Time динамической компоновки

После создания библиотеки DLL можно использовать функции, которые она определяет в приложении. Ниже приведено простое консольное приложение, использующее функцию Мипутс, экспортированную из Myputs.dll (см. раздел [Создание простой библиотеки Dynamic-Link](creating-a-simple-dynamic-link-library.md)).

Так как в этом примере функция DLL вызывается явным образом, модуль для приложения должен быть связан с библиотекой импорта Мипутс. lib. Дополнительные сведения о создании библиотек DLL см. в документации, входящей в состав средств разработки.


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Динамическая компоновка во время загрузки](load-time-dynamic-linking.md)
</dt> </dl>

 

 



