---
description: Функция CreateProcess позволяет отладчику запустить процесс и выполнить его отладку.
ms.assetid: 7056e181-9bc5-4530-a7b8-d5ff1e345eef
title: Обработка функций для отладки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d31378a4115acfdd5a4a1836199b7387adeb6e3f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990487"
---
# <a name="process-functions-for-debugging"></a><span data-ttu-id="0257b-103">Обработка функций для отладки</span><span class="sxs-lookup"><span data-stu-id="0257b-103">Process Functions for Debugging</span></span>

<span data-ttu-id="0257b-104">Функция [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) позволяет отладчику запустить процесс и выполнить его отладку.</span><span class="sxs-lookup"><span data-stu-id="0257b-104">The [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) function enables a debugger to start a process and debug it.</span></span> <span data-ttu-id="0257b-105">Параметр *фдвкреате* в **CreateProcess** используется для указания типа операции отладки.</span><span class="sxs-lookup"><span data-stu-id="0257b-105">The *fdwCreate* parameter of **CreateProcess** is used to specify the type of debugging operation.</span></span> <span data-ttu-id="0257b-106">Если \_ для параметра указан флаг отладки Process, отладчик выдает новый процесс и все потомки процесса, при условии, что потомки создаются без \_ флага процесса отладки.</span><span class="sxs-lookup"><span data-stu-id="0257b-106">If the DEBUG\_PROCESS flag is specified for the parameter, a debugger debugs the new process and all of the process's descendants, provided that the descendants are created without the DEBUG\_PROCESS flag.</span></span>

<span data-ttu-id="0257b-107">Если \_ для фдвкреате заданы отладочный и отладочный \_ только \_ этот \_ флаг процесса, отладчик выдает новый процесс, но не имеет ни одного потомка.</span><span class="sxs-lookup"><span data-stu-id="0257b-107">If the DEBUG\_PROCESS and DEBUG\_ONLY\_THIS\_PROCESS flags are specified for *fdwCreate*, a debugger debugs the new process but none of its descendants.</span></span>

<span data-ttu-id="0257b-108">Один отладчик может выполнить отладку другого, создав процесс с \_ флагом процесса отладки.</span><span class="sxs-lookup"><span data-stu-id="0257b-108">One debugger can debug another by creating a process with the DEBUG\_PROCESS flag.</span></span> <span data-ttu-id="0257b-109">Новый процесс (отлаживаемый отладчик) должен создать процесс с \_ флагом процесса отладки.</span><span class="sxs-lookup"><span data-stu-id="0257b-109">The new process (the debugger being debugged) must then create a process with the DEBUG\_PROCESS flag.</span></span>

<span data-ttu-id="0257b-110">Функция [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess) позволяет отладчику получить идентификатор существующего процесса.</span><span class="sxs-lookup"><span data-stu-id="0257b-110">The [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess) function enables a debugger to obtain the identifier of an existing process.</span></span> <span data-ttu-id="0257b-111">(Функция [**дебугактивепроцесс**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) использует этот идентификатор для подключения отладчика к процессу.) Как правило, отладчики открывают процесс с \_ \_ \_ флагами записи виртуальной машины для чтения и обработки \_ .</span><span class="sxs-lookup"><span data-stu-id="0257b-111">(The [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) function uses this identifier to attach the debugger to the process.) Typically, debuggers open a process with the PROCESS\_VM\_READ and PROCESS\_VM\_WRITE flags.</span></span> <span data-ttu-id="0257b-112">Использование этих флагов позволяет отладчику считывать данные из виртуальной памяти процесса и записывать их в виртуальную память, используя функции [**реадпроцессмемори**](/windows/win32/api/memoryapi/nf-memoryapi-readprocessmemory) и [**вритепроцессмемори**](/windows/win32/api/memoryapi/nf-memoryapi-writeprocessmemory) .</span><span class="sxs-lookup"><span data-stu-id="0257b-112">Using these flags enables the debugger to read from and write to the virtual memory of the process by using the [**ReadProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-readprocessmemory) and [**WriteProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-writeprocessmemory) functions.</span></span> <span data-ttu-id="0257b-113">Дополнительные сведения см. в разделе [**процессы и потоки**](../procthread/processes-and-threads.md).</span><span class="sxs-lookup"><span data-stu-id="0257b-113">For more information, see [**Processes and Threads**](../procthread/processes-and-threads.md).</span></span>

 

 
