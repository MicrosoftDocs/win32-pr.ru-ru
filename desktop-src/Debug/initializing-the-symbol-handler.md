---
description: В следующем коде показано, как инициализировать обработчик символов.
ms.assetid: e8c8f648-c3b0-4595-ac07-f508dd576d9f
title: Инициализация обработчика символов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d5a7ba79a71a389f185a5e18065af818223d4cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990380"
---
# <a name="initializing-the-symbol-handler"></a><span data-ttu-id="b2c02-103">Инициализация обработчика символов</span><span class="sxs-lookup"><span data-stu-id="b2c02-103">Initializing the Symbol Handler</span></span>

<span data-ttu-id="b2c02-104">В следующем коде показано, как инициализировать обработчик символов.</span><span class="sxs-lookup"><span data-stu-id="b2c02-104">The following code demonstrates how to initialize the symbol handler.</span></span> <span data-ttu-id="b2c02-105">Функция [**симсетоптионс**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) откладывает загрузку символов до запроса символьной информации.</span><span class="sxs-lookup"><span data-stu-id="b2c02-105">The [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) function defers symbol loading until symbol information is requested.</span></span> <span data-ttu-id="b2c02-106">Код загружает символы для каждого модуля в указанном процессе, передавая значение **true** для параметра *бинваде* функции [**симинитиализе**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) .</span><span class="sxs-lookup"><span data-stu-id="b2c02-106">The code loads the symbols for each module in the specified process by passing a value of **TRUE** for the *bInvade* parameter of the [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) function.</span></span> <span data-ttu-id="b2c02-107">(Эта функция вызывает функцию [**SymLoadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule) для каждого модуля, который процесс сопоставляет с адресным пространством.)</span><span class="sxs-lookup"><span data-stu-id="b2c02-107">(This function calls the [**SymLoadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmodule) function for each module the process has mapped into its address space.)</span></span>

<span data-ttu-id="b2c02-108">Если указанный процесс не является процессом, вызвавшим [**симинитиализе**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize), код передает идентификатор процесса в качестве первого параметра **симинитиализе**.</span><span class="sxs-lookup"><span data-stu-id="b2c02-108">If the specified process is not the process that called [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize), the code passes a process identifier as the first parameter of **SymInitialize**.</span></span>

<span data-ttu-id="b2c02-109">Указание **значения NULL** в качестве второго параметра [**симинитиализе**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) указывает, что обработчик символов должен использовать путь поиска по умолчанию для поиска файлов символов.</span><span class="sxs-lookup"><span data-stu-id="b2c02-109">Specifying **NULL** as the second parameter of [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) indicates that the symbol handler should use the default search path to locate symbol files.</span></span> <span data-ttu-id="b2c02-110">Подробные сведения о том, как обработчик символов находит файлы символов или как приложение может указать путь поиска символов, см. в разделе [пути к символам](symbol-paths.md).</span><span class="sxs-lookup"><span data-stu-id="b2c02-110">For detailed information on how the symbol handler locates symbol files or how an application can specify a symbol search path, see [Symbol Paths](symbol-paths.md).</span></span>


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



 

 



