---
description: Чтобы освободить всю память, используемую обработчиком символов для процесса, используйте функцию Симклеануп.
ms.assetid: d442b2f2-9225-43fd-bd25-274322857834
title: Очистка обработчика символов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0daea96e780f7e3a685b408c7c774e91b2795b84
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895693"
---
# <a name="symbol-handler-cleanup"></a><span data-ttu-id="26679-103">Очистка обработчика символов</span><span class="sxs-lookup"><span data-stu-id="26679-103">Symbol Handler Cleanup</span></span>

<span data-ttu-id="26679-104">Чтобы освободить всю память, используемую обработчиком символов для процесса, используйте функцию [**симклеануп**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup) .</span><span class="sxs-lookup"><span data-stu-id="26679-104">To free all the memory used by the symbol handler for a process, use the [**SymCleanup**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup) function.</span></span> <span data-ttu-id="26679-105">Эта функция перечисляет все загруженные модули, освобождает каждый модуль и освобождает память, выделенную для списка модулей.</span><span class="sxs-lookup"><span data-stu-id="26679-105">This function enumerates all loaded modules, frees each module, and frees the memory allocated for the list of modules.</span></span> <span data-ttu-id="26679-106">После вызова **симклеануп** нельзя использовать обработчик процесса в функциях обработки символов, пока не будет вызвана функция [**симинитиализе**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) .</span><span class="sxs-lookup"><span data-stu-id="26679-106">After you call **SymCleanup**, you cannot use the process handle in the symbol handling functions until you call the [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) function.</span></span>

 

 



