---
description: Инверсия приоритетов возникает, когда для запланированных конфликтов между двумя или более потоками с разными приоритетами.
ms.assetid: 1cb2f3c9-4641-40d8-892c-768abaf6affb
title: Инверсия приоритета
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79a0f4c9d57000e9e81429ee882e70dc14f63ae4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345455"
---
# <a name="priority-inversion"></a><span data-ttu-id="6f9ee-103">Инверсия приоритета</span><span class="sxs-lookup"><span data-stu-id="6f9ee-103">Priority Inversion</span></span>

<span data-ttu-id="6f9ee-104">Инверсия приоритетов возникает, когда для запланированных конфликтов между двумя или более потоками с разными приоритетами.</span><span class="sxs-lookup"><span data-stu-id="6f9ee-104">Priority inversion occurs when two or more threads with different priorities are in contention to be scheduled.</span></span> <span data-ttu-id="6f9ee-105">Рассмотрим простой случай с тремя потоками: поток 1, поток 2 и поток 3.</span><span class="sxs-lookup"><span data-stu-id="6f9ee-105">Consider a simple case with three threads: thread 1, thread 2, and thread 3.</span></span> <span data-ttu-id="6f9ee-106">Поток 1 имеет высокий приоритет и становится готовым к планированию.</span><span class="sxs-lookup"><span data-stu-id="6f9ee-106">Thread 1 is high priority and becomes ready to be scheduled.</span></span> <span data-ttu-id="6f9ee-107">Поток 2, поток с низким приоритетом, исполняет код в критической секции.</span><span class="sxs-lookup"><span data-stu-id="6f9ee-107">Thread 2, a low-priority thread, is executing code in a critical section.</span></span> <span data-ttu-id="6f9ee-108">Поток 1, поток с высоким приоритетом, начинает ожидание общего ресурса из потока 2.</span><span class="sxs-lookup"><span data-stu-id="6f9ee-108">Thread 1, the high-priority thread, begins waiting for a shared resource from thread 2.</span></span> <span data-ttu-id="6f9ee-109">Поток 3 имеет средний приоритет.</span><span class="sxs-lookup"><span data-stu-id="6f9ee-109">Thread 3 has medium priority.</span></span> <span data-ttu-id="6f9ee-110">Поток 3 получает все процессорное время, так как поток с высоким приоритетом (поток 1) ожидает общие ресурсы от потока с низким приоритетом (поток 2).</span><span class="sxs-lookup"><span data-stu-id="6f9ee-110">Thread 3 receives all the processor time, because the high-priority thread (thread 1) is waiting for shared resources from the low-priority thread (thread 2).</span></span> <span data-ttu-id="6f9ee-111">Поток 2 не оставляет критический раздел, так как он не имеет наивысшего приоритета и не будет планироваться.</span><span class="sxs-lookup"><span data-stu-id="6f9ee-111">Thread 2 will not leave the critical section, because it does not have the highest priority and will not be scheduled.</span></span>

<span data-ttu-id="6f9ee-112">Планировщик решает эту проблему путем случайного увеличения приоритета готовых потоков (в данном случае блокировки с низким приоритетом).</span><span class="sxs-lookup"><span data-stu-id="6f9ee-112">The scheduler solves this problem by randomly boosting the priority of the ready threads (in this case, the low priority lock-holders).</span></span> <span data-ttu-id="6f9ee-113">Потоки с низким приоритетом выполняются достаточно долго для выхода из критической секции, и поток с высоким приоритетом может войти в критическую секцию.</span><span class="sxs-lookup"><span data-stu-id="6f9ee-113">The low priority threads run long enough to exit the critical section, and the high-priority thread can enter the critical section.</span></span> <span data-ttu-id="6f9ee-114">Если поток с низким приоритетом не получит достаточно времени ЦП для выхода из критического раздела, он получит еще одну шанс в ходе следующего цикла планирования.</span><span class="sxs-lookup"><span data-stu-id="6f9ee-114">If the low-priority thread does not get enough CPU time to exit the critical section the first time, it will get another chance during the next round of scheduling.</span></span>

 

 



