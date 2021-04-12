---
description: Многозадачная операционная система делит доступное время процессора между процессами или потоками, которым он необходим.
ms.assetid: ac45bef6-f078-40ac-95f4-06bd61ff46c4
title: Многозадачность
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d06c1d8d44f397f06923c793971bcb20f35b2b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345465"
---
# <a name="multitasking"></a><span data-ttu-id="61dc7-103">Многозадачность</span><span class="sxs-lookup"><span data-stu-id="61dc7-103">Multitasking</span></span>

<span data-ttu-id="61dc7-104">Многозадачная операционная система делит доступное время процессора между процессами или потоками, которым он необходим.</span><span class="sxs-lookup"><span data-stu-id="61dc7-104">A multitasking operating system divides the available processor time among the processes or threads that need it.</span></span> <span data-ttu-id="61dc7-105">Система разработана для многозадачного с вытеснением. Он выделяет *срез времени* процессора для каждого выполняемого потока.</span><span class="sxs-lookup"><span data-stu-id="61dc7-105">The system is designed for preemptive multitasking; it allocates a processor *time slice* to each thread it executes.</span></span> <span data-ttu-id="61dc7-106">Выполняющийся в данный момент поток приостанавливается по истечении его временного среза, что позволяет запустить другой поток.</span><span class="sxs-lookup"><span data-stu-id="61dc7-106">The currently executing thread is suspended when its time slice elapses, allowing another thread to run.</span></span> <span data-ttu-id="61dc7-107">Когда система переключается с одного потока на другой, он сохраняет контекст вытесненного потока и восстанавливает сохраненный контекст следующего потока в очереди.</span><span class="sxs-lookup"><span data-stu-id="61dc7-107">When the system switches from one thread to another, it saves the context of the preempted thread and restores the saved context of the next thread in the queue.</span></span>

<span data-ttu-id="61dc7-108">Длительность среза времени зависит от конкретной операционной системы и процессора.</span><span class="sxs-lookup"><span data-stu-id="61dc7-108">The length of the time slice depends on the operating system and the processor.</span></span> <span data-ttu-id="61dc7-109">Так как каждый временный срез является небольшим (приблизительно 20 миллисекунд), несколько потоков выполняются одновременно.</span><span class="sxs-lookup"><span data-stu-id="61dc7-109">Because each time slice is small (approximately 20 milliseconds), multiple threads appear to be executing at the same time.</span></span> <span data-ttu-id="61dc7-110">А на многопроцессорных системах выполняемые потоки действительно одновременно распределяются между доступными процессорами.</span><span class="sxs-lookup"><span data-stu-id="61dc7-110">This is actually the case on multiprocessor systems, where the executable threads are distributed among the available processors.</span></span> <span data-ttu-id="61dc7-111">Однако при использовании нескольких потоков в приложении необходимо соблюдать осторожность, так как производительность системы может снизиться, если слишком много потоков.</span><span class="sxs-lookup"><span data-stu-id="61dc7-111">However, you must use caution when using multiple threads in an application, because system performance can decrease if there are too many threads.</span></span>

<span data-ttu-id="61dc7-112">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="61dc7-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="61dc7-113">Преимущества многозадачности</span><span class="sxs-lookup"><span data-stu-id="61dc7-113">Advantages of Multitasking</span></span>](advantages-of-multitasking.md)
-   [<span data-ttu-id="61dc7-114">Когда следует использовать многозадачность</span><span class="sxs-lookup"><span data-stu-id="61dc7-114">When to Use Multitasking</span></span>](when-to-use-multitasking.md)
-   [<span data-ttu-id="61dc7-115">Рекомендации по многозадачности</span><span class="sxs-lookup"><span data-stu-id="61dc7-115">Multitasking Considerations</span></span>](multitasking-considerations.md)

 

 



