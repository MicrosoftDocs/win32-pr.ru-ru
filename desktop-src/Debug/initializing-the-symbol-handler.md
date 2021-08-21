---
description: В следующем коде показано, как инициализировать обработчик символов.
ms.assetid: e8c8f648-c3b0-4595-ac07-f508dd576d9f
title: Инициализация обработчика символов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24f1da864c4550232d278b6bfb9b2006a6d56956e363dcf4fbd72ed0e6b9685d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956983"
---
# <a name="initializing-the-symbol-handler"></a>Инициализация обработчика символов

В следующем коде показано, как инициализировать обработчик символов. Функция [**симсетоптионс**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) откладывает загрузку символов до запроса символьной информации. Код загружает символы для каждого модуля в указанном процессе, передавая значение **true** для параметра *бинваде* функции [**симинитиализе**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) . (Эта функция вызывает функцию [**SymLoadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule) для каждого модуля, который процесс сопоставляет с адресным пространством.)

Если указанный процесс не является процессом, вызвавшим [**симинитиализе**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize), код передает идентификатор процесса в качестве первого параметра **симинитиализе**.

Указание **значения NULL** в качестве второго параметра [**симинитиализе**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) указывает, что обработчик символов должен использовать путь поиска по умолчанию для поиска файлов символов. Подробные сведения о том, как обработчик символов находит файлы символов или как приложение может указать путь поиска символов, см. в разделе [пути к символам](symbol-paths.md).


```C++
DWORD  error;
HANDLE hProcess;

SymSetOptions(SYMOPT_UNDNAME | SYMOPT_DEFERRED_LOADS);

hProcess = GetCurrentProcess();

if (!SymInitialize(hProcess, NULL, TRUE))
{
    // SymInitialize failed
    error = GetLastError();
    printf("SymInitialize returned error : %d\n", error);
    return FALSE;
}
```



 

 



