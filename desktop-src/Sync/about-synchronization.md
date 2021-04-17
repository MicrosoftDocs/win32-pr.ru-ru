---
description: Чтобы синхронизировать доступ к ресурсу, используйте один из объектов синхронизации в одной из функций ожидания.
ms.assetid: 0930bf12-6d5f-4f2c-914d-53e6e862d3bd
title: Сведения о синхронизации
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ad53dc8c309d8ec55f37cef5f78839348071477
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663894"
---
# <a name="about-synchronization"></a><span data-ttu-id="897d2-103">Сведения о синхронизации</span><span class="sxs-lookup"><span data-stu-id="897d2-103">About Synchronization</span></span>

<span data-ttu-id="897d2-104">Чтобы синхронизировать доступ к ресурсу, используйте один из [объектов синхронизации](synchronization-objects.md) в одной из [функций ожидания](wait-functions.md).</span><span class="sxs-lookup"><span data-stu-id="897d2-104">To synchronize access to a resource, use one of the [synchronization objects](synchronization-objects.md) in one of the [wait functions](wait-functions.md).</span></span> <span data-ttu-id="897d2-105">Состояние объекта синхронизации — « *сигнальный* » или « *несигнальный*».</span><span class="sxs-lookup"><span data-stu-id="897d2-105">The state of a synchronization object is either *signaled* or *nonsignaled*.</span></span> <span data-ttu-id="897d2-106">Функции Wait позволяют потоку блокировать свое выполнение, пока для заданного несигнального объекта не будет установлено сигнальное состояние.</span><span class="sxs-lookup"><span data-stu-id="897d2-106">The wait functions allow a thread to block its own execution until a specified nonsignaled object is set to the signaled state.</span></span> <span data-ttu-id="897d2-107">Дополнительные сведения см. в разделе [межпроцессная синхронизация](interprocess-synchronization.md).</span><span class="sxs-lookup"><span data-stu-id="897d2-107">For more information, see [Interprocess Synchronization](interprocess-synchronization.md).</span></span>

<span data-ttu-id="897d2-108">Ниже приведены другие механизмы синхронизации.</span><span class="sxs-lookup"><span data-stu-id="897d2-108">The following are other synchronization mechanisms:</span></span>

-   [<span data-ttu-id="897d2-109">перекрывающиеся входные и выходные данные</span><span class="sxs-lookup"><span data-stu-id="897d2-109">overlapped input and output</span></span>](synchronization-and-overlapped-input-and-output.md)
-   [<span data-ttu-id="897d2-110">асинхронные вызовы процедур</span><span class="sxs-lookup"><span data-stu-id="897d2-110">asynchronous procedure calls</span></span>](asynchronous-procedure-calls.md)
-   [<span data-ttu-id="897d2-111">объекты критических секций</span><span class="sxs-lookup"><span data-stu-id="897d2-111">critical section objects</span></span>](critical-section-objects.md)
-   [<span data-ttu-id="897d2-112">переменные условий</span><span class="sxs-lookup"><span data-stu-id="897d2-112">condition variables</span></span>](condition-variables.md)
-   [<span data-ttu-id="897d2-113">Упрощенные блокировки потоков чтения/записи</span><span class="sxs-lookup"><span data-stu-id="897d2-113">slim reader/writer locks</span></span>](slim-reader-writer--srw--locks.md)
-   [<span data-ttu-id="897d2-114">однократная инициализация</span><span class="sxs-lookup"><span data-stu-id="897d2-114">one-time initialization</span></span>](one-time-initialization.md)
-   [<span data-ttu-id="897d2-115">доступ к блокируемым переменным</span><span class="sxs-lookup"><span data-stu-id="897d2-115">interlocked variable access</span></span>](interlocked-variable-access.md)
-   [<span data-ttu-id="897d2-116">взаимозаблокированные однонаправленные списки</span><span class="sxs-lookup"><span data-stu-id="897d2-116">interlocked singly linked lists</span></span>](interlocked-singly-linked-lists.md)
-   [<span data-ttu-id="897d2-117">очереди таймера</span><span class="sxs-lookup"><span data-stu-id="897d2-117">timer queues</span></span>](timer-queues.md)
-   <span data-ttu-id="897d2-118">макрос [**меморибарриер**](/windows/win32/api/winnt/nf-winnt-memorybarrier)</span><span class="sxs-lookup"><span data-stu-id="897d2-118">the [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier) macro</span></span>

<span data-ttu-id="897d2-119">Дополнительные сведения о синхронизации см. в разделе [проблемы синхронизации и многопроцессорной обработки](synchronization-and-multiprocessor-issues.md).</span><span class="sxs-lookup"><span data-stu-id="897d2-119">For additional information on synchronization, see [Synchronization and Multiprocessor Issues](synchronization-and-multiprocessor-issues.md).</span></span>

 

 
