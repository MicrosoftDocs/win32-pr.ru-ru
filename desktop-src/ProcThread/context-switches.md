---
description: Планировщик поддерживает очередь исполняемых потоков для каждого уровня приоритета.
ms.assetid: 82463d71-9cef-4608-b997-25dc9c1e1c0a
title: Переключения контекста
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7628ee9e659cdbc2369b5f69d25847e8864dbd62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264498"
---
# <a name="context-switches"></a><span data-ttu-id="9b4ca-103">Переключения контекста</span><span class="sxs-lookup"><span data-stu-id="9b4ca-103">Context Switches</span></span>

<span data-ttu-id="9b4ca-104">Планировщик поддерживает очередь исполняемых потоков для каждого уровня приоритета.</span><span class="sxs-lookup"><span data-stu-id="9b4ca-104">The scheduler maintains a queue of executable threads for each priority level.</span></span> <span data-ttu-id="9b4ca-105">Они известны как *Готовые потоки*.</span><span class="sxs-lookup"><span data-stu-id="9b4ca-105">These are known as *ready threads*.</span></span> <span data-ttu-id="9b4ca-106">Когда процессор станет доступным, система выполняет *Переключение контекста*.</span><span class="sxs-lookup"><span data-stu-id="9b4ca-106">When a processor becomes available, the system performs a *context switch*.</span></span> <span data-ttu-id="9b4ca-107">В контекстном переключении выполняются следующие действия.</span><span class="sxs-lookup"><span data-stu-id="9b4ca-107">The steps in a context switch are:</span></span>

1.  <span data-ttu-id="9b4ca-108">Сохраните контекст потока, который только что завершил исполнение.</span><span class="sxs-lookup"><span data-stu-id="9b4ca-108">Save the context of the thread that just finished executing.</span></span>
2.  <span data-ttu-id="9b4ca-109">Поместите поток, который только что завершил исполнение в конце очереди, в качестве его приоритета.</span><span class="sxs-lookup"><span data-stu-id="9b4ca-109">Place the thread that just finished executing at the end of the queue for its priority.</span></span>
3.  <span data-ttu-id="9b4ca-110">Поиск очереди с наивысшим приоритетом, которая содержит готовые потоки.</span><span class="sxs-lookup"><span data-stu-id="9b4ca-110">Find the highest priority queue that contains ready threads.</span></span>
4.  <span data-ttu-id="9b4ca-111">Удалите поток в заголовке очереди, загрузите его контекст и выполните его.</span><span class="sxs-lookup"><span data-stu-id="9b4ca-111">Remove the thread at the head of the queue, load its context, and execute it.</span></span>

<span data-ttu-id="9b4ca-112">Следующие классы потоков не являются готовыми потоками.</span><span class="sxs-lookup"><span data-stu-id="9b4ca-112">The following classes of threads are not ready threads.</span></span>

-   <span data-ttu-id="9b4ca-113">Потоки, созданные с \_ флагом "создать приостановку"</span><span class="sxs-lookup"><span data-stu-id="9b4ca-113">Threads created with the CREATE\_SUSPENDED flag</span></span>
-   <span data-ttu-id="9b4ca-114">Потоки, остановленные во время выполнения с помощью функции [**суспендсреад**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) или [**свитчтосреад**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread)</span><span class="sxs-lookup"><span data-stu-id="9b4ca-114">Threads halted during execution with the [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) or [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) function</span></span>
-   <span data-ttu-id="9b4ca-115">Потоки, ожидающие объект синхронизации или входные данные.</span><span class="sxs-lookup"><span data-stu-id="9b4ca-115">Threads waiting for a synchronization object or input.</span></span>

<span data-ttu-id="9b4ca-116">Пока приостановленные или заблокированные потоки становятся готовы к выполнению, планировщик не выделяет для них какое – либо процессорное время, независимо от их приоритета.</span><span class="sxs-lookup"><span data-stu-id="9b4ca-116">Until threads that are suspended or blocked become ready to run, the scheduler does not allocate any processor time to them, regardless of their priority.</span></span>

<span data-ttu-id="9b4ca-117">Ниже перечислены наиболее распространенные причины переключения контекста.</span><span class="sxs-lookup"><span data-stu-id="9b4ca-117">The most common reasons for a context switch are:</span></span>

-   <span data-ttu-id="9b4ca-118">Временной срез истек.</span><span class="sxs-lookup"><span data-stu-id="9b4ca-118">The time slice has elapsed.</span></span>
-   <span data-ttu-id="9b4ca-119">Поток с более высоким приоритетом стал готов к выполнению.</span><span class="sxs-lookup"><span data-stu-id="9b4ca-119">A thread with a higher priority has become ready to run.</span></span>
-   <span data-ttu-id="9b4ca-120">Выполняемый поток должен ждать.</span><span class="sxs-lookup"><span data-stu-id="9b4ca-120">A running thread needs to wait.</span></span>

<span data-ttu-id="9b4ca-121">Когда выполняющийся поток должен ждать, он освобождает оставшуюся часть его временного среза.</span><span class="sxs-lookup"><span data-stu-id="9b4ca-121">When a running thread needs to wait, it relinquishes the remainder of its time slice.</span></span>

 

 
