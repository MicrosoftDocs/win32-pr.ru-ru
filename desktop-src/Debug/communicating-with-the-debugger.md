---
description: Функция OutputDebugString отправляет строку из процесса, отлаживаемого в отладчик, путем создания события отладки для отладочной \_ строки исходящего \_ \_ события. Процесс может определить, выполняется ли его отладка, вызвав функцию Исдебугжерпресент.
ms.assetid: d9e1d565-fb76-4d91-8aa7-4ff0ff31f71f
title: Взаимодействие с отладчиком
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f982d89ac99a0f0de159579212323e298a773aa2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895301"
---
# <a name="communicating-with-the-debugger"></a><span data-ttu-id="9861c-104">Взаимодействие с отладчиком</span><span class="sxs-lookup"><span data-stu-id="9861c-104">Communicating with the Debugger</span></span>

<span data-ttu-id="9861c-105">Функция [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) отправляет строку из процесса, отлаживаемого в отладчик, путем создания события отладки для отладочной \_ строки исходящего \_ \_ события.</span><span class="sxs-lookup"><span data-stu-id="9861c-105">The [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) function sends a string from the process being debugged to the debugger by generating an OUTPUT\_DEBUG\_STRING\_EVENT debugging event.</span></span> <span data-ttu-id="9861c-106">Процесс может определить, выполняется ли его отладка, вызвав функцию [**исдебугжерпресент**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent) .</span><span class="sxs-lookup"><span data-stu-id="9861c-106">A process can detect whether it is being debugged by calling the [**IsDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent) function.</span></span>

<span data-ttu-id="9861c-107">Функция [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak) вызывает исключение точки останова в текущем процессе.</span><span class="sxs-lookup"><span data-stu-id="9861c-107">The [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak) function causes a breakpoint exception in the current process.</span></span> <span data-ttu-id="9861c-108">Точка останова — это расположение в программе, в которой выполнение останавливается, чтобы позволить разработчику исследовать код программы, переменные и регистр значений, а также при необходимости выполнять изменения, продолжать выполнение или прерывать выполнение.</span><span class="sxs-lookup"><span data-stu-id="9861c-108">A breakpoint is a location in a program where execution is stopped to allow the developer to examine the program's code, variables, and register values and, as necessary, to make changes, continue execution, or terminate execution.</span></span>

<span data-ttu-id="9861c-109">Функция [**фаталексит**](/windows/desktop/api/WinBase/nf-winbase-fatalexit) завершает текущий процесс и предоставляет управление выполнением отладчику, но в отличие от [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak), он не создает исключение.</span><span class="sxs-lookup"><span data-stu-id="9861c-109">The [**FatalExit**](/windows/desktop/api/WinBase/nf-winbase-fatalexit) function terminates the current process and gives execution control to the debugger, but unlike [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak), it does not generate an exception.</span></span> <span data-ttu-id="9861c-110">Эта функция должна использоваться только в качестве крайней функции, поскольку она не всегда освобождает память процесса или не закрывает файлы.</span><span class="sxs-lookup"><span data-stu-id="9861c-110">This function should only be used as a last resort, because it does not always free the process's memory or close its files.</span></span>

 

 
