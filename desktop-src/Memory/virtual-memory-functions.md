---
description: Функции виртуальной памяти позволяют процессу управлять состоянием страниц в его виртуальном адресном пространстве.
ms.assetid: 9488a854-1ef0-488f-b3d1-57c1acb82a88
title: Функции виртуальной памяти
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c76866fd10dac01315622e8a4faef7bea436a61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673377"
---
# <a name="virtual-memory-functions"></a><span data-ttu-id="c597b-103">Функции виртуальной памяти</span><span class="sxs-lookup"><span data-stu-id="c597b-103">Virtual Memory Functions</span></span>

<span data-ttu-id="c597b-104">Функции виртуальной памяти позволяют процессу управлять состоянием страниц в его виртуальном адресном пространстве.</span><span class="sxs-lookup"><span data-stu-id="c597b-104">The virtual memory functions enable a process to manipulate or determine the status of pages in its virtual address space.</span></span> <span data-ttu-id="c597b-105">Они могут выполнять следующие операции:</span><span class="sxs-lookup"><span data-stu-id="c597b-105">They can perform the following operations:</span></span>

-   <span data-ttu-id="c597b-106">Зарезервируйте диапазон виртуального адресного пространства процесса.</span><span class="sxs-lookup"><span data-stu-id="c597b-106">Reserve a range of a process's virtual address space.</span></span> <span data-ttu-id="c597b-107">Резервирование адресного пространства не выделяет физическое хранилище, но не позволяет другим операциям выделения использовать указанный диапазон.</span><span class="sxs-lookup"><span data-stu-id="c597b-107">Reserving address space does not allocate any physical storage, but it prevents other allocation operations from using the specified range.</span></span> <span data-ttu-id="c597b-108">Он не влияет на виртуальные адресные пространства других процессов.</span><span class="sxs-lookup"><span data-stu-id="c597b-108">It does not affect the virtual address spaces of other processes.</span></span> <span data-ttu-id="c597b-109">Резервирование страниц предотвращает необязательное использование физического хранилища, одновременно позволяя процессу резервировать диапазон адресного пространства, в котором может расти структура динамических данных.</span><span class="sxs-lookup"><span data-stu-id="c597b-109">Reserving pages prevents needless consumption of physical storage, while enabling a process to reserve a range of its address space into which a dynamic data structure can grow.</span></span> <span data-ttu-id="c597b-110">При необходимости процесс может выделить физическое хранилище для этого пространства.</span><span class="sxs-lookup"><span data-stu-id="c597b-110">The process can allocate physical storage for this space, as needed.</span></span>
-   <span data-ttu-id="c597b-111">Зафиксируйте диапазон зарезервированных страниц в виртуальном адресном пространстве процесса, чтобы физическое хранилище (в ОЗУ или на диске) было доступно только для процесса выделения.</span><span class="sxs-lookup"><span data-stu-id="c597b-111">Commit a range of reserved pages in a process's virtual address space so that physical storage (either in RAM or on disk) is accessible only to the allocating process.</span></span>
-   <span data-ttu-id="c597b-112">Укажите доступ для чтения и записи, только для чтения или без доступа для диапазона зафиксированных страниц.</span><span class="sxs-lookup"><span data-stu-id="c597b-112">Specify read/write, read-only, or no access for a range of committed pages.</span></span> <span data-ttu-id="c597b-113">Это отличается от стандартных функций выделения, которые всегда выделяют страницы с доступом на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="c597b-113">This differs from the standard allocation functions that always allocate pages with read/write access.</span></span>
-   <span data-ttu-id="c597b-114">Освободите диапазон зарезервированных страниц, сделав диапазон виртуальных адресов для последующих операций выделения вызывающим процессом.</span><span class="sxs-lookup"><span data-stu-id="c597b-114">Free a range of reserved pages, making the range of virtual addresses available for subsequent allocation operations by the calling process.</span></span>
-   <span data-ttu-id="c597b-115">Отменяет выделение диапазона зафиксированных страниц, освобождая их физическое хранилище и делая их доступными для последующего выделения любым процессом.</span><span class="sxs-lookup"><span data-stu-id="c597b-115">Decommit a range of committed pages, releasing their physical storage and making it available for subsequent allocation by any process.</span></span>
-   <span data-ttu-id="c597b-116">Блокировка одной или нескольких страниц выделенной памяти в физическую память (ОЗУ), чтобы система не могла переключать страницы в файл подкачки.</span><span class="sxs-lookup"><span data-stu-id="c597b-116">Lock one or more pages of committed memory into physical memory (RAM) so that the system cannot swap the pages out to the paging file.</span></span>
-   <span data-ttu-id="c597b-117">Получение сведений о диапазоне страниц в виртуальном адресном пространстве вызывающего процесса или указанного процесса.</span><span class="sxs-lookup"><span data-stu-id="c597b-117">Obtain information about a range of pages in the virtual address space of the calling process or a specified process.</span></span>
-   <span data-ttu-id="c597b-118">Изменение защиты доступа для указанного диапазона зафиксированных страниц в виртуальном адресном пространстве вызывающего процесса или указанного процесса.</span><span class="sxs-lookup"><span data-stu-id="c597b-118">Change the access protection for a specified range of committed pages in the virtual address space of the calling process or a specified process.</span></span>

<span data-ttu-id="c597b-119">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="c597b-119">For more information, see the following topics.</span></span>

-   [<span data-ttu-id="c597b-120">Выделение виртуальной памяти</span><span class="sxs-lookup"><span data-stu-id="c597b-120">Allocating Virtual Memory</span></span>](allocating-virtual-memory.md)
-   [<span data-ttu-id="c597b-121">Сравнение методов выделения памяти</span><span class="sxs-lookup"><span data-stu-id="c597b-121">Comparing Memory Allocation Methods</span></span>](comparing-memory-allocation-methods.md)
-   [<span data-ttu-id="c597b-122">Освобождение виртуальной памяти</span><span class="sxs-lookup"><span data-stu-id="c597b-122">Freeing Virtual Memory</span></span>](freeing-virtual-memory.md)
-   [<span data-ttu-id="c597b-123">Работа со страницами</span><span class="sxs-lookup"><span data-stu-id="c597b-123">Working With Pages</span></span>](working-with-pages.md)
-   [<span data-ttu-id="c597b-124">Функции управления памятью</span><span class="sxs-lookup"><span data-stu-id="c597b-124">Memory Management Functions</span></span>](memory-management-functions.md)

 

 



