---
title: Функции справки средства
description: Содержит список функций библиотеки справки по средствам.
ms.assetid: 83732bd6-f4cf-409d-ad17-86503d408dc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54f9d95598f9b48343ea9731e1a826fb147a73a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068479"
---
# <a name="tool-help-functions"></a><span data-ttu-id="00d0f-103">Функции справки средства</span><span class="sxs-lookup"><span data-stu-id="00d0f-103">Tool Help Functions</span></span>

<span data-ttu-id="00d0f-104">Следующие функции являются частью библиотеки справки по средствам.</span><span class="sxs-lookup"><span data-stu-id="00d0f-104">The following functions are part of the tool help library.</span></span>



| <span data-ttu-id="00d0f-105">Функция</span><span class="sxs-lookup"><span data-stu-id="00d0f-105">Function</span></span>                                                           | <span data-ttu-id="00d0f-106">Описание</span><span class="sxs-lookup"><span data-stu-id="00d0f-106">Description</span></span>                                                                                                      |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="00d0f-107">**CreateToolhelp32Snapshot**</span><span class="sxs-lookup"><span data-stu-id="00d0f-107">**CreateToolhelp32Snapshot**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot)       | <span data-ttu-id="00d0f-108">Создает моментальный снимок указанных процессов, а также кучи, модули и потоки, используемые этими процессами.</span><span class="sxs-lookup"><span data-stu-id="00d0f-108">Takes a snapshot of the specified processes, as well as the heaps, modules, and threads used by these processes.</span></span> |
| [<span data-ttu-id="00d0f-109">**Heap32First**</span><span class="sxs-lookup"><span data-stu-id="00d0f-109">**Heap32First**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first)                                 | <span data-ttu-id="00d0f-110">Извлекает сведения о первом блоке кучи, выделенной процессом.</span><span class="sxs-lookup"><span data-stu-id="00d0f-110">Retrieves information about the first block of a heap that has been allocated by a process.</span></span>                      |
| [<span data-ttu-id="00d0f-111">**Heap32ListFirst**</span><span class="sxs-lookup"><span data-stu-id="00d0f-111">**Heap32ListFirst**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst)                         | <span data-ttu-id="00d0f-112">Извлекает сведения о первой куче, выделенной указанным процессом.</span><span class="sxs-lookup"><span data-stu-id="00d0f-112">Retrieves information about the first heap that has been allocated by a specified process.</span></span>                       |
| [<span data-ttu-id="00d0f-113">**Heap32ListNext**</span><span class="sxs-lookup"><span data-stu-id="00d0f-113">**Heap32ListNext**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext)                           | <span data-ttu-id="00d0f-114">Извлекает сведения о следующей куче, выделенной процессом.</span><span class="sxs-lookup"><span data-stu-id="00d0f-114">Retrieves information about the next heap that has been allocated by a process.</span></span>                                  |
| [<span data-ttu-id="00d0f-115">**Heap32Next**</span><span class="sxs-lookup"><span data-stu-id="00d0f-115">**Heap32Next**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next)                                   | <span data-ttu-id="00d0f-116">Извлекает сведения о следующем блоке кучи, выделенной процессом.</span><span class="sxs-lookup"><span data-stu-id="00d0f-116">Retrieves information about the next block of a heap that has been allocated by a process.</span></span>                       |
| [<span data-ttu-id="00d0f-117">**Module32First**</span><span class="sxs-lookup"><span data-stu-id="00d0f-117">**Module32First**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first)                             | <span data-ttu-id="00d0f-118">Извлекает сведения о первом модуле, связанном с процессом.</span><span class="sxs-lookup"><span data-stu-id="00d0f-118">Retrieves information about the first module associated with a process.</span></span>                                          |
| [<span data-ttu-id="00d0f-119">**Module32Next**</span><span class="sxs-lookup"><span data-stu-id="00d0f-119">**Module32Next**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next)                               | <span data-ttu-id="00d0f-120">Извлекает сведения о следующем модуле, связанном с процессом или потоком.</span><span class="sxs-lookup"><span data-stu-id="00d0f-120">Retrieves information about the next module associated with a process or thread.</span></span>                                 |
| [<span data-ttu-id="00d0f-121">**Process32First**</span><span class="sxs-lookup"><span data-stu-id="00d0f-121">**Process32First**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first)                           | <span data-ttu-id="00d0f-122">Извлекает сведения о первом процессе, обнаруженном в системном снимке.</span><span class="sxs-lookup"><span data-stu-id="00d0f-122">Retrieves information about the first process encountered in a system snapshot.</span></span>                                  |
| [<span data-ttu-id="00d0f-123">**Process32Next**</span><span class="sxs-lookup"><span data-stu-id="00d0f-123">**Process32Next**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next)                             | <span data-ttu-id="00d0f-124">Извлекает сведения о следующем процессе, записанном в системном снимке.</span><span class="sxs-lookup"><span data-stu-id="00d0f-124">Retrieves information about the next process recorded in a system snapshot.</span></span>                                      |
| [<span data-ttu-id="00d0f-125">**Thread32First**</span><span class="sxs-lookup"><span data-stu-id="00d0f-125">**Thread32First**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first)                             | <span data-ttu-id="00d0f-126">Извлекает сведения о первом потоке любого процесса, обнаруженного в системном снимке.</span><span class="sxs-lookup"><span data-stu-id="00d0f-126">Retrieves information about the first thread of any process encountered in a system snapshot.</span></span>                    |
| [<span data-ttu-id="00d0f-127">**Thread32Next**</span><span class="sxs-lookup"><span data-stu-id="00d0f-127">**Thread32Next**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next)                               | <span data-ttu-id="00d0f-128">Извлекает сведения о следующем потоке любого процесса, обнаруженного в снимке системной памяти.</span><span class="sxs-lookup"><span data-stu-id="00d0f-128">Retrieves information about the next thread of any process encountered in the system memory snapshot.</span></span>            |
| [<span data-ttu-id="00d0f-129">**Toolhelp32ReadProcessMemory**</span><span class="sxs-lookup"><span data-stu-id="00d0f-129">**Toolhelp32ReadProcessMemory**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-toolhelp32readprocessmemory) | <span data-ttu-id="00d0f-130">Копирует память, выделенную для другого процесса, в буфер, предоставленный приложением.</span><span class="sxs-lookup"><span data-stu-id="00d0f-130">Copies memory allocated to another process into an application-supplied buffer.</span></span>                                  |



 

 

 




