---
description: В следующем коде показано, как получить недекорированное имя символа из имени символа с помощью Ундекоратесимболнаме.
ms.assetid: fcb0591a-dac3-45eb-b4c0-4a35c42450e5
title: Получение недекорированных имен символов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99b0f21c884a0a58f0546ef275f2f3096abe2c50
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647149"
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



 

 



