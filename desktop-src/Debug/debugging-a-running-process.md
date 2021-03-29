---
description: Чтобы выполнить отладку уже запущенного процесса, отладчик должен использовать Дебугактивепроцесс с идентификатором процесса. Чтобы получить список идентификаторов процессов, используйте функцию EnumProcesses или Process32First.
ms.assetid: 2662411f-a69a-442b-a177-a27ea025bb01
title: Отладка выполняющегося процесса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f93d184907bb66a651f04a5e144e40bf5955a672
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104140810"
---
# <a name="debugging-a-running-process"></a><span data-ttu-id="20bf1-104">Отладка выполняющегося процесса</span><span class="sxs-lookup"><span data-stu-id="20bf1-104">Debugging a Running Process</span></span>

<span data-ttu-id="20bf1-105">Чтобы выполнить отладку уже запущенного процесса, отладчик должен использовать [**дебугактивепроцесс**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) с идентификатором процесса.</span><span class="sxs-lookup"><span data-stu-id="20bf1-105">To debug a process that is already running, the debugger should use [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) with the process identifier.</span></span> <span data-ttu-id="20bf1-106">Чтобы получить список идентификаторов процессов, используйте функцию [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses) или [**Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first) .</span><span class="sxs-lookup"><span data-stu-id="20bf1-106">To retrieve a list of process identifiers, use either the [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses) or [**Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first) function.</span></span>

<span data-ttu-id="20bf1-107">[**Дебугактивепроцесс**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) подключает отладчик к активному процессу.</span><span class="sxs-lookup"><span data-stu-id="20bf1-107">[**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) attaches the debugger to the active process.</span></span> <span data-ttu-id="20bf1-108">В этом случае можно отлаживать только активный процесс. его дочерние процессы не могут.</span><span class="sxs-lookup"><span data-stu-id="20bf1-108">In this case, only the active process can be debugged; its child processes cannot.</span></span> <span data-ttu-id="20bf1-109">Отладчик должен иметь соответствующий доступ к выполняющемуся процессу для использования **дебугактивепроцесс**.</span><span class="sxs-lookup"><span data-stu-id="20bf1-109">The debugger must have appropriate access to the executing process to use **DebugActiveProcess**.</span></span> <span data-ttu-id="20bf1-110">Дополнительные сведения о правах доступа см. в разделе [Управление доступом](../secauthz/access-control.md).</span><span class="sxs-lookup"><span data-stu-id="20bf1-110">For more information about access rights, see [Access Control](../secauthz/access-control.md).</span></span>

<span data-ttu-id="20bf1-111">После создания или присоединения отладчика к процессу, который он намеревается выполнить отладку, система уведомляет отладчик обо всех событиях отладки, происходящих в процессе, и, если это указано, в любых дочерних процессах.</span><span class="sxs-lookup"><span data-stu-id="20bf1-111">After the debugger has either created or attached itself to the process it intends to debug, the system notifies the debugger of all debugging events that occur in the process, and, if specified, in any child processes.</span></span> <span data-ttu-id="20bf1-112">Дополнительные сведения об отладке событий см. в разделе [Отладка событий](debugging-events.md).</span><span class="sxs-lookup"><span data-stu-id="20bf1-112">For more information about debugging events, see [Debugging Events](debugging-events.md).</span></span>

<span data-ttu-id="20bf1-113">Чтобы отсоединиться от отлаживаемого процесса, отладчик должен использовать функцию [**дебугактивепроцессстоп**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocessstop) .</span><span class="sxs-lookup"><span data-stu-id="20bf1-113">To detach from the process being debugged, the debugger should use the [**DebugActiveProcessStop**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocessstop) function.</span></span>

 

 
