---
description: В следующем коде показано, как получить недекорированное имя символа из имени символа с помощью Ундекоратесимболнаме.
ms.assetid: fcb0591a-dac3-45eb-b4c0-4a35c42450e5
title: Получение недекорированных имен символов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f18a1cbdf51c64134489850343b466e49d9867fab483699a719997c3be9b5798
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076348"
---
# <a name="retrieving-undecorated-symbol-names"></a>Получение недекорированных имен символов

В следующем коде показано, как получить недекорированное имя символа из имени символа с помощью [**ундекоратесимболнаме**](/windows/desktop/api/Dbghelp/nf-dbghelp-undecoratesymbolname). Декорированное имя хранится в `szName` . В примере предполагается, что обработчик символов инициализирован с помощью кода при [инициализации обработчика символов](initializing-the-symbol-handler.md).


```C++
if (UnDecorateSymbolName(szName, szUndName, sizeof(szUndName), UNDNAME_COMPLETE))
{
    // UnDecorateSymbolName returned success
    printf ("Symbol : %s\n", szUndName);
}
else
{
    // UnDecorateSymbolName failed
    DWORD error = GetLastError();
    printf("UnDecorateSymbolName returned error %d\n", error);
}
```



 

 



