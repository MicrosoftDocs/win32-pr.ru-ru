---
description: Существует множество функций для получения сведений о процессах.
ms.assetid: f9ec6aa5-15ad-47e6-b5f8-8ac4daaf178f
title: Получение дополнительных сведений о процессе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b90f7c68a89e2989c33c5f57a4e4fb5cead86a74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545479"
---
# <a name="obtaining-additional-process-information"></a><span data-ttu-id="cdca0-103">Получение дополнительных сведений о процессе</span><span class="sxs-lookup"><span data-stu-id="cdca0-103">Obtaining Additional Process Information</span></span>

<span data-ttu-id="cdca0-104">Существует множество функций для получения сведений о процессах.</span><span class="sxs-lookup"><span data-stu-id="cdca0-104">There are a variety of functions for obtaining information about processes.</span></span> <span data-ttu-id="cdca0-105">Некоторые из этих функций можно использовать только для вызывающего процесса, так как они не принимают в качестве параметра обработку обработки.</span><span class="sxs-lookup"><span data-stu-id="cdca0-105">Some of these functions can be used only for the calling process, because they do not take a process handle as a parameter.</span></span> <span data-ttu-id="cdca0-106">Для получения сведений о других процессах можно использовать функции, которые используют обработчик процесса.</span><span class="sxs-lookup"><span data-stu-id="cdca0-106">You can use functions that take a process handle to obtain information about other processes.</span></span>

-   <span data-ttu-id="cdca0-107">Чтобы получить строку командной строки для текущего процесса, используйте функцию [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea) .</span><span class="sxs-lookup"><span data-stu-id="cdca0-107">To obtain the command-line string for the current process, use the [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea) function.</span></span>
-   <span data-ttu-id="cdca0-108">Чтобы получить структуру [**стартупинфо**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) , указанную при создании текущего процесса, используйте функцию [**жетстартупинфо**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getstartupinfow) .</span><span class="sxs-lookup"><span data-stu-id="cdca0-108">To retrieve the [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) structure specified when the current process was created, use the [**GetStartupInfo**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getstartupinfow) function.</span></span>
-   <span data-ttu-id="cdca0-109">Чтобы получить сведения о версии из заголовка исполняемого файла, используйте функцию [**жетпроцессверсион**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessversion) .</span><span class="sxs-lookup"><span data-stu-id="cdca0-109">To obtain the version information from the executable header, use the [**GetProcessVersion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessversion) function.</span></span>
-   <span data-ttu-id="cdca0-110">Чтобы получить полный путь и имя файла для исполняемого файла, содержащего код процесса, используйте функцию [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) .</span><span class="sxs-lookup"><span data-stu-id="cdca0-110">To obtain the full path and file name for the executable file containing the process code, use the [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) function.</span></span>
-   <span data-ttu-id="cdca0-111">Чтобы получить количество дескрипторов для используемых объектов графического интерфейса пользователя, используйте функцию [**жетгуиресаурцес**](/windows/desktop/api/Winuser/nf-winuser-getguiresources) .</span><span class="sxs-lookup"><span data-stu-id="cdca0-111">To obtain the count of handles to graphical user interface (GUI) objects in use, use the [**GetGuiResources**](/windows/desktop/api/Winuser/nf-winuser-getguiresources) function.</span></span>
-   <span data-ttu-id="cdca0-112">Чтобы определить, выполняется ли отладка процесса, используйте функцию [**исдебугжерпресент**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent) .</span><span class="sxs-lookup"><span data-stu-id="cdca0-112">To determine whether a process is being debugged, use the [**IsDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent) function.</span></span>
-   <span data-ttu-id="cdca0-113">Чтобы получить сведения об учетных данных для всех операций ввода-вывода, выполняемых процессом, используйте функцию [**жетпроцессиокаунтерс**](/windows/desktop/api/WinBase/nf-winbase-getprocessiocounters) .</span><span class="sxs-lookup"><span data-stu-id="cdca0-113">To retrieve accounting information for all I/O operations performed by the process, use the [**GetProcessIoCounters**](/windows/desktop/api/WinBase/nf-winbase-getprocessiocounters) function.</span></span>

 

 
