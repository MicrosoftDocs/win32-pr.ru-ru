---
description: Потоковая передача потоков и диспетчер графа фильтров
ms.assetid: b490b72a-ab34-46e6-8dc6-a7bb07cfc7b1
title: Потоковая передача потоков и диспетчер графа фильтров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a8c5b8fa972a8118563ae8f9e73d480ac15e80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674057"
---
# <a name="streaming-threads-and-the-filter-graph-manager"></a><span data-ttu-id="3b1eb-103">Потоковая передача потоков и диспетчер графа фильтров</span><span class="sxs-lookup"><span data-stu-id="3b1eb-103">Streaming Threads and the Filter Graph Manager</span></span>

<span data-ttu-id="3b1eb-104">Когда диспетчер графа фильтров останавливает граф, он ожидает завершения работы всех потоков потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="3b1eb-104">When the Filter Graph Manager stops the graph, it waits for all streaming threads to shut down.</span></span> <span data-ttu-id="3b1eb-105">Это имеет следующие последствия для фильтров:</span><span class="sxs-lookup"><span data-stu-id="3b1eb-105">This has the following implications for filters:</span></span>

-   <span data-ttu-id="3b1eb-106">Фильтр не должен вызывать методы в диспетчере графов фильтров из потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="3b1eb-106">A filter must never call methods on the Filter Graph Manager from a streaming thread.</span></span>

    <span data-ttu-id="3b1eb-107">Диспетчер графов фильтров использует критическую секцию для синхронизации собственных операций.</span><span class="sxs-lookup"><span data-stu-id="3b1eb-107">The Filter Graph Manager uses a critical section to synchronize its own operations.</span></span> <span data-ttu-id="3b1eb-108">Если поток потоковой передачи пытается сохранить этот критический раздел, это может привести к взаимоблокировке.</span><span class="sxs-lookup"><span data-stu-id="3b1eb-108">If a streaming thread tries to hold this critical section, it can cause a deadlock.</span></span> <span data-ttu-id="3b1eb-109">Например: Предположим, что другой поток останавливает граф.</span><span class="sxs-lookup"><span data-stu-id="3b1eb-109">For example: Suppose that another thread stops the graph.</span></span> <span data-ttu-id="3b1eb-110">Этот поток принимает блокировку графа фильтра и ожидает, пока фильтр не завершит доставку данных.</span><span class="sxs-lookup"><span data-stu-id="3b1eb-110">That thread takes the filter graph lock and waits for your filter to stop delivering data.</span></span> <span data-ttu-id="3b1eb-111">Если фильтр ожидает блокировки, он никогда не будет останавливаться, что приведет к взаимоблокировке.</span><span class="sxs-lookup"><span data-stu-id="3b1eb-111">If your filter is waiting for the lock, it will never stop, causing a deadlock.</span></span>

-   <span data-ttu-id="3b1eb-112">Фильтр не должен ни выполнять **AddRef** , ни **QueryInterface** диспетчер графов фильтра из потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="3b1eb-112">A filter must never **AddRef** or **QueryInterface** the Filter Graph Manager from a streaming thread.</span></span>

    <span data-ttu-id="3b1eb-113">Если фильтр содержит счетчик ссылок в диспетчере графов фильтров (через **AddRef** или **QueryInterface**), он может стать последним объектом для хранения счетчика ссылок.</span><span class="sxs-lookup"><span data-stu-id="3b1eb-113">If the filter holds a reference count on the Filter Graph Manager (through **AddRef** or **QueryInterface**), it might become the last object to hold a reference count.</span></span> <span data-ttu-id="3b1eb-114">Когда фильтр вызывает **выпуск**, диспетчер графа фильтров уничтожает себя.</span><span class="sxs-lookup"><span data-stu-id="3b1eb-114">When the filter calls **Release**, the Filter Graph Manager destroys itself.</span></span> <span data-ttu-id="3b1eb-115">Внутри своей подпрограммы очистки диспетчер графа фильтров пытается прекратить граф, что приведет к ожиданию завершения потока потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="3b1eb-115">Inside its cleanup routine, the Filter Graph Manager attempts to stop the graph, causing it to wait for the streaming thread to exit.</span></span> <span data-ttu-id="3b1eb-116">Однако он ожидает в потоке потоковой передачи, поэтому поток потоковой передачи не может завершиться.</span><span class="sxs-lookup"><span data-stu-id="3b1eb-116">However, it is waiting inside the streaming thread, so the streaming thread cannot exit.</span></span> <span data-ttu-id="3b1eb-117">Результатом является взаимоблокировка.</span><span class="sxs-lookup"><span data-stu-id="3b1eb-117">The result is a deadlock.</span></span>

 

 



