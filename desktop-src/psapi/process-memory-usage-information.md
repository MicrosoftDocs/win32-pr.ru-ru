---
title: Сведения об использовании памяти процесса
description: Функция Жетпроцессмеморинфо принимает в качестве входных данных обработку и заполняет \_ \_ структуру счетчиков памяти процесса данными о статистике памяти для процесса.
ms.assetid: 683c899e-a7e8-4440-8f13-2a713c1618bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 133032b8cfb8a9af4ccea5661c9e0e0181ab4d93
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888843"
---
# <a name="process-memory-usage-information"></a><span data-ttu-id="86563-103">Сведения об использовании памяти процесса</span><span class="sxs-lookup"><span data-stu-id="86563-103">Process Memory Usage Information</span></span>

<span data-ttu-id="86563-104">Функция [**жетпроцессмеморинфо**](/windows/desktop/api/Psapi/nf-psapi-getprocessmemoryinfo) принимает в качестве входных данных обработку и заполняет структуру [**\_ \_ счетчиков памяти процесса**](/windows/desktop/api/Psapi/ns-psapi-process_memory_counters) данными о статистике памяти для процесса.</span><span class="sxs-lookup"><span data-stu-id="86563-104">The [**GetProcessMemoryInfo**](/windows/desktop/api/Psapi/nf-psapi-getprocessmemoryinfo) function takes a process handle as input and fills a [**PROCESS\_MEMORY\_COUNTERS**](/windows/desktop/api/Psapi/ns-psapi-process_memory_counters) structure with information about the memory statistics for the process.</span></span> <span data-ttu-id="86563-105">Член **CB** получает размер структуры.</span><span class="sxs-lookup"><span data-stu-id="86563-105">The **cb** member receives the size of the structure.</span></span> <span data-ttu-id="86563-106">Элемент **пажефаулткаунт** получает количество ошибок страниц.</span><span class="sxs-lookup"><span data-stu-id="86563-106">The **PageFaultCount** member receives the number of page faults.</span></span> <span data-ttu-id="86563-107">Остальные члены получают текущее и пиковое использование памяти в следующих категориях:</span><span class="sxs-lookup"><span data-stu-id="86563-107">The remaining members receive the current and peak memory usage in the following categories:</span></span>

-   <span data-ttu-id="86563-108">Рабочий набор</span><span class="sxs-lookup"><span data-stu-id="86563-108">working set</span></span>
-   <span data-ttu-id="86563-109">выгружаемого пула</span><span class="sxs-lookup"><span data-stu-id="86563-109">paged pool</span></span>
-   <span data-ttu-id="86563-110">невыгружаемого пула</span><span class="sxs-lookup"><span data-stu-id="86563-110">nonpaged pool</span></span>
-   <span data-ttu-id="86563-111">Размер</span><span class="sxs-lookup"><span data-stu-id="86563-111">pagefile</span></span>

<span data-ttu-id="86563-112">*Рабочий набор* — это объем памяти, физически сопоставленный с контекстом процесса в определенный момент времени.</span><span class="sxs-lookup"><span data-stu-id="86563-112">The *working set* is the amount of memory physically mapped to the process context at a given time.</span></span> <span data-ttu-id="86563-113">Память в *выгружаемого пула* — это системная память, которую можно передать в файл подкачки на диске (с разбивкой на страницы), если он не используется.</span><span class="sxs-lookup"><span data-stu-id="86563-113">Memory in the *paged pool* is system memory that can be transferred to the paging file on disk (paged) when it is not being used.</span></span> <span data-ttu-id="86563-114">В *невыгружаемом пуле* памяти находится системная память, которая не может быть помещена на диск, пока выделены соответствующие объекты.</span><span class="sxs-lookup"><span data-stu-id="86563-114">Memory in the *nonpaged pool* is system memory that cannot be paged to disk as long as the corresponding objects are allocated.</span></span> <span data-ttu-id="86563-115">Использование файла *подкачки* представляет объем памяти, заданный для процесса в файле подкачки системы.</span><span class="sxs-lookup"><span data-stu-id="86563-115">The *pagefile* usage represents how much memory is set aside for the process in the system paging file.</span></span> <span data-ttu-id="86563-116">При слишком высоком потреблении памяти Диспетчер виртуальной памяти выбирает память на диске.</span><span class="sxs-lookup"><span data-stu-id="86563-116">When memory usage is too high, the virtual memory manager pages selected memory to disk.</span></span> <span data-ttu-id="86563-117">Когда потоку требуется страница, которая не находится в памяти, диспетчер памяти перегружает его из файла подкачки.</span><span class="sxs-lookup"><span data-stu-id="86563-117">When a thread needs a page that is not in memory, the memory manager reloads it from the paging file.</span></span>

 

 




