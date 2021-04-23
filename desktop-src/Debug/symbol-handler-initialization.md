---
description: Обработчик символов предназначен для наблюдения за различными наборами файлов символов.
ms.assetid: 1bd7ac25-e46d-442b-b365-52edcd8bf922
title: Инициализация обработчика символов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 146af0e1118e85a3478ca45be7a86c4b1d8dfe83
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141019"
---
# <a name="symbol-handler-initialization"></a><span data-ttu-id="6d3c4-103">Инициализация обработчика символов</span><span class="sxs-lookup"><span data-stu-id="6d3c4-103">Symbol Handler Initialization</span></span>

<span data-ttu-id="6d3c4-104">Обработчик символов предназначен для наблюдения за различными наборами файлов символов.</span><span class="sxs-lookup"><span data-stu-id="6d3c4-104">The symbol handler is designed to track various sets of symbol files.</span></span>

<span data-ttu-id="6d3c4-105">Чтобы инициализировать обработчик символов, вызовите функцию [**симинитиализе**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) .</span><span class="sxs-lookup"><span data-stu-id="6d3c4-105">To initialize the symbol handler, call the [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) function.</span></span> <span data-ttu-id="6d3c4-106">Параметр *хпроцесс* может быть уникальным произвольным числом, значением, возвращаемым функцией [**жеткуррентпроцесс**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) , или идентификатором любого выполняющегося процесса.</span><span class="sxs-lookup"><span data-stu-id="6d3c4-106">The *hProcess* parameter can be a unique arbitrary number, a value returned from the [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) function, or the identifier of any running process.</span></span> <span data-ttu-id="6d3c4-107">Параметр *финвадепроцесс* указывает, должен ли обработчик символов перечислять модули, загруженные процессом, и загружать символы для каждого из его модулей.</span><span class="sxs-lookup"><span data-stu-id="6d3c4-107">The *fInvadeProcess* parameter indicates whether the symbol handler should enumerate the modules loaded by the process and load symbols for each of its modules.</span></span> <span data-ttu-id="6d3c4-108">Если *финвадепроцесс* имеет **значение true**, параметр *хпроцесс* должен быть значением, возвращенным из **жеткуррентпроцесс** , или идентификатором существующего процесса.</span><span class="sxs-lookup"><span data-stu-id="6d3c4-108">If *fInvadeProcess* is **TRUE**, the *hProcess* parameter must be the value returned from **GetCurrentProcess** or the identifier of an existing process.</span></span> <span data-ttu-id="6d3c4-109">Чтобы обновить этот список, используйте функцию [**симрефрешмодулелист**](/windows/desktop/api/Dbghelp/nf-dbghelp-symrefreshmodulelist) .</span><span class="sxs-lookup"><span data-stu-id="6d3c4-109">To refresh this list, use the [**SymRefreshModuleList**](/windows/desktop/api/Dbghelp/nf-dbghelp-symrefreshmodulelist) function.</span></span>

<span data-ttu-id="6d3c4-110">Использование *финвадепроцесс* — это простой способ загрузки всех файлов символов для процесса.</span><span class="sxs-lookup"><span data-stu-id="6d3c4-110">Using *fInvadeProcess* is a simple way to load all symbol files for a process.</span></span> <span data-ttu-id="6d3c4-111">Однако обработчик символов не будет пытаться загрузить символы для модулей, которые затем загружаются функцией [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) .</span><span class="sxs-lookup"><span data-stu-id="6d3c4-111">However, the symbol handler will not attempt to load symbols for modules subsequently loaded by the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) function.</span></span> <span data-ttu-id="6d3c4-112">В этом случае необходимо использовать функцию [**симлоадмодуликс**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) .</span><span class="sxs-lookup"><span data-stu-id="6d3c4-112">You must use the [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) function in this case.</span></span>

 

 
