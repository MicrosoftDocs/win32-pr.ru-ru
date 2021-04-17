---
description: Реализация многозадачности, планирование приоритетов и работа с процессами, потоками, пулами потоков, объектами заданий и волокнами. Планирование потоков с помощью планирования пользовательского режима.
ms.assetid: 6bff848c-0c55-41e7-aff1-84c6b21a1b8d
title: Процессы и потоки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f469806a5f803910a773c78c9847d0f7b0ecc7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673745"
---
# <a name="processes-and-threads"></a><span data-ttu-id="d2f5e-104">Процессы и потоки</span><span class="sxs-lookup"><span data-stu-id="d2f5e-104">Processes and Threads</span></span>

<span data-ttu-id="d2f5e-105">Приложение состоит из одного или нескольких процессов.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-105">An application consists of one or more processes.</span></span> <span data-ttu-id="d2f5e-106">*Процесс*, в простейшем смысле, является исполняемой программой.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-106">A *process*, in the simplest terms, is an executing program.</span></span> <span data-ttu-id="d2f5e-107">Один или несколько потоков выполняются в контексте процесса.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-107">One or more threads run in the context of the process.</span></span> <span data-ttu-id="d2f5e-108">*Поток* — это базовая единица, в которой операционная система выделяет процессорное время.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-108">A *thread* is the basic unit to which the operating system allocates processor time.</span></span> <span data-ttu-id="d2f5e-109">Поток может выполнять любую часть кода процесса, включая части, которые в данный момент выполняются другим потоком.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-109">A thread can execute any part of the process code, including parts currently being executed by another thread.</span></span>

<span data-ttu-id="d2f5e-110">*Объект задания* позволяет управлять группами процессов как единым целым.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-110">A *job object* allows groups of processes to be managed as a unit.</span></span> <span data-ttu-id="d2f5e-111">Объекты заданий являются намаблеными, защищаемыми объектами, совместно используемые объекты, которые управляют атрибутами связанных с ними процессов.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-111">Job objects are namable, securable, sharable objects that control attributes of the processes associated with them.</span></span> <span data-ttu-id="d2f5e-112">Операции, выполняемые над объектом задания, влияют на все процессы, связанные с объектом Job.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-112">Operations performed on the job object affect all processes associated with the job object.</span></span>

<span data-ttu-id="d2f5e-113">*Пул потоков* — это коллекция рабочих потоков, которые эффективно выполняют асинхронные обратные вызовы от имени приложения.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-113">A *thread pool* is a collection of worker threads that efficiently execute asynchronous callbacks on behalf of the application.</span></span> <span data-ttu-id="d2f5e-114">Пул потоков в основном используется для сокращения числа потоков приложения и обеспечения управления рабочими потоками.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-114">The thread pool is primarily used to reduce the number of application threads and provide management of the worker threads.</span></span>

<span data-ttu-id="d2f5e-115">*Волокно* — это единица выполнения, которая должна быть запланирована приложением вручную.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-115">A *fiber* is a unit of execution that must be manually scheduled by the application.</span></span> <span data-ttu-id="d2f5e-116">Волокна выполняются в контексте потоков, планирующих их.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-116">Fibers run in the context of the threads that schedule them.</span></span>

<span data-ttu-id="d2f5e-117">*Планирование пользовательского режима* (UMS) — это упрощенный механизм, с помощью которого приложения могут планировать собственные потоки.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-117">*User-mode scheduling* (UMS) is a lightweight mechanism that applications can use to schedule their own threads.</span></span> <span data-ttu-id="d2f5e-118">UMS-потоки отличаются от [волокон](fibers.md) тем, что каждый поток UMS имеет собственный контекст потока вместо того, чтобы совместно использовать контекст потока одного потока.</span><span class="sxs-lookup"><span data-stu-id="d2f5e-118">UMS threads differ from [fibers](fibers.md) in that each UMS thread has its own thread context instead of sharing the thread context of a single thread.</span></span>

-   [<span data-ttu-id="d2f5e-119">Новые возможности в процессах и потоках</span><span class="sxs-lookup"><span data-stu-id="d2f5e-119">What's New in Processes and Threads</span></span>](what-s-new-in-processes-and-threads.md)
-   [<span data-ttu-id="d2f5e-120">Процессы и потоки</span><span class="sxs-lookup"><span data-stu-id="d2f5e-120">About Processes and Threads</span></span>](about-processes-and-threads.md)
-   [<span data-ttu-id="d2f5e-121">Использование процессов и потоков</span><span class="sxs-lookup"><span data-stu-id="d2f5e-121">Using Processes and Threads</span></span>](using-processes-and-threads.md)
-   [<span data-ttu-id="d2f5e-122">Справочник по процессам и потокам</span><span class="sxs-lookup"><span data-stu-id="d2f5e-122">Process and Thread Reference</span></span>](process-and-thread-reference.md)

 

 



