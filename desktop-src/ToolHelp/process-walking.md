---
title: Процесс прохода
description: Моментальный снимок, включающий список процессов, содержит сведения о каждом выполняющемся процессе.
ms.assetid: 4fb55763-2206-48ad-8b1f-ed2c33b6f56b
keywords:
- перечисление
- Перечисление, процессы
- процессы
- процессы, перечисление процессов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc95f0de4021ce3c355286376decbdecef2c883
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487937"
---
# <a name="process-walking"></a><span data-ttu-id="40a96-107">Процесс прохода</span><span class="sxs-lookup"><span data-stu-id="40a96-107">Process Walking</span></span>

<span data-ttu-id="40a96-108">Моментальный снимок, включающий список процессов, содержит сведения о каждом выполняющемся процессе.</span><span class="sxs-lookup"><span data-stu-id="40a96-108">A snapshot that includes the process list contains information about each currently executing process.</span></span> <span data-ttu-id="40a96-109">Сведения для первого процесса в списке можно получить с помощью функции [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) .</span><span class="sxs-lookup"><span data-stu-id="40a96-109">You can retrieve information for the first process in the list by using the [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) function.</span></span> <span data-ttu-id="40a96-110">После получения первого процесса в списке можно просмотреть список процессов для последующих записей с помощью функции [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next) .</span><span class="sxs-lookup"><span data-stu-id="40a96-110">After retrieving the first process in the list, you can traverse the process list for subsequent entries by using the [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next) function.</span></span> <span data-ttu-id="40a96-111">**Process32First** и **Process32Next** заполняют структуру [**PROCESSENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-processentry32) информацией о процессе в моментальном снимке.</span><span class="sxs-lookup"><span data-stu-id="40a96-111">**Process32First** and **Process32Next** fill a [**PROCESSENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-processentry32) structure with information about a process in the snapshot.</span></span> <span data-ttu-id="40a96-112">Пример см. в разделе [Создание моментального снимка и Просмотр процессов](taking-a-snapshot-and-viewing-processes.md).</span><span class="sxs-lookup"><span data-stu-id="40a96-112">For an example, see [Taking a Snapshot and Viewing Processes](taking-a-snapshot-and-viewing-processes.md).</span></span>

<span data-ttu-id="40a96-113">Код расширенного состояния ошибки для [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) и [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next) можно получить с помощью функции [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="40a96-113">You can retrieve an extended error status code for [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) and [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next) by using the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

<span data-ttu-id="40a96-114">Можно прочитать память в определенном процессе в буфер с помощью функции [**Toolhelp32ReadProcessMemory**](/windows/desktop/api/TlHelp32/nf-tlhelp32-toolhelp32readprocessmemory) (или функции [**виртуалкуерекс**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualqueryex) ).</span><span class="sxs-lookup"><span data-stu-id="40a96-114">You can read the memory in a specific process into a buffer by using the [**Toolhelp32ReadProcessMemory**](/windows/desktop/api/TlHelp32/nf-tlhelp32-toolhelp32readprocessmemory) function (or the [**VirtualQueryEx**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualqueryex) function).</span></span>

> [!Note]  
> <span data-ttu-id="40a96-115">Содержимое элементов **th32ProcessID** и **th32ParentProcessID** в [**PROCESSENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-processentry32) являются идентификаторами процессов и могут использоваться любыми функциями, которым требуется идентификатор процесса.</span><span class="sxs-lookup"><span data-stu-id="40a96-115">The contents of the **th32ProcessID** and **th32ParentProcessID** members of [**PROCESSENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-processentry32) are process identifiers and can be used by any functions that require a process identifier.</span></span>

 

 

 