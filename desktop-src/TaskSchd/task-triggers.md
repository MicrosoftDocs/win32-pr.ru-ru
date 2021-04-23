---
title: Триггеры задач
description: Триггер — это набор критериев, при достижении которого начинается выполнение задачи.
ms.assetid: 8b4dff8b-9dc3-4856-aed6-648588a089be
keywords:
- Создание триггеров планировщик задач
- триггеры планировщик задач
- триггеры планировщик задач, описание
- планировщик задач триггеров, с учетом времени
- триггеры планировщик задач, на основе событий
- триггеры на основе событий планировщик задач
- триггеры, основанные на времени планировщик задач
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d465dfa015be19ff220a77d3c85f0cbb223c4899
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104252917"
---
# <a name="task-triggers"></a><span data-ttu-id="356cd-110">Триггеры задач</span><span class="sxs-lookup"><span data-stu-id="356cd-110">Task Triggers</span></span>

<span data-ttu-id="356cd-111">Триггер — это набор критериев, при достижении которого начинается выполнение задачи.</span><span class="sxs-lookup"><span data-stu-id="356cd-111">A trigger is a set of criteria that, when met, starts the execution of a task.</span></span> <span data-ttu-id="356cd-112">Планировщик задач предоставляет триггеры на основе времени и событий, которые могут запускать задачу несколькими разными способами.</span><span class="sxs-lookup"><span data-stu-id="356cd-112">Task Scheduler provides both time-based and event-based triggers that can start a task in several different ways.</span></span> <span data-ttu-id="356cd-113">Заданную задачу можно запустить с помощью одного или нескольких триггеров.</span><span class="sxs-lookup"><span data-stu-id="356cd-113">A given task can be started by one or more triggers.</span></span> <span data-ttu-id="356cd-114">У задачи может быть не более 48 триггеров.</span><span class="sxs-lookup"><span data-stu-id="356cd-114">A task can have a maximum of 48 triggers.</span></span>

## <a name="time-based-triggers"></a><span data-ttu-id="356cd-115">Триггеры на основе времени</span><span class="sxs-lookup"><span data-stu-id="356cd-115">Time-based Triggers</span></span>

<span data-ttu-id="356cd-116">Триггеры, основанные на времени, запускают задачи в указанное время.</span><span class="sxs-lookup"><span data-stu-id="356cd-116">Time-based triggers start tasks at specified times.</span></span> <span data-ttu-id="356cd-117">Сюда входит запуск задачи один раз в определенное время или запуск задачи несколько раз для ежедневного, еженедельного, ежемесячного или ежемесячного расписания недели.</span><span class="sxs-lookup"><span data-stu-id="356cd-117">This includes starting the task once at a specific time or starting the task multiple times on a daily, weekly, monthly, or monthly day-of-week schedule.</span></span>

## <a name="event-based-triggers"></a><span data-ttu-id="356cd-118">Триггеры на основе событий</span><span class="sxs-lookup"><span data-stu-id="356cd-118">Event-based Triggers</span></span>

<span data-ttu-id="356cd-119">Триггеры на основе событий запускают задачу в ответ на определенные системные события.</span><span class="sxs-lookup"><span data-stu-id="356cd-119">Event-based triggers start a task in response to certain system events.</span></span> <span data-ttu-id="356cd-120">Например, триггеры на основе событий можно задать для запуска задачи при запуске системы, когда пользователь входит в систему на локальном компьютере или когда система переходит в состояние простоя.</span><span class="sxs-lookup"><span data-stu-id="356cd-120">For example, event-based triggers can be set to start a task when the system starts up, when a user logs on to the local computer, or when the system becomes idle.</span></span>

## <a name="multiple-triggers"></a><span data-ttu-id="356cd-121">Несколько триггеров</span><span class="sxs-lookup"><span data-stu-id="356cd-121">Multiple Triggers</span></span>

<span data-ttu-id="356cd-122">Каждая задача может запускаться одним или несколькими триггерами, что позволяет запускать задачу несколькими способами.</span><span class="sxs-lookup"><span data-stu-id="356cd-122">Each task can be started by one or more triggers, allowing the task to be started in any number of ways.</span></span> <span data-ttu-id="356cd-123">Однако несколько триггеров реализуются по-разному в планировщик задач 1,0 и планировщик задач 2,0.</span><span class="sxs-lookup"><span data-stu-id="356cd-123">However, multiple triggers are implemented differently in Task Scheduler 1.0 and Task Scheduler 2.0.</span></span>

<span data-ttu-id="356cd-124">В планировщик задач 2,0 каждый триггер определяется отдельным API триггера, который связан с задачей через коллекцию триггеров.</span><span class="sxs-lookup"><span data-stu-id="356cd-124">In Task Scheduler 2.0, each trigger is defined by a separate trigger API that is associated with the task through the trigger collection.</span></span>

<span data-ttu-id="356cd-125">В планировщик задач 1,0 несколько триггеров можно рассматривать как расписание, набор времени, когда начинается задача.</span><span class="sxs-lookup"><span data-stu-id="356cd-125">In Task Scheduler 1.0, multiple triggers can be thought of as a schedule, a set of times at which the task starts.</span></span> <span data-ttu-id="356cd-126">В этом случае расписанием является набор раз (заданный объединением всех триггеров, связанных с рабочим элементом), в которых будет выполняться рабочий элемент.</span><span class="sxs-lookup"><span data-stu-id="356cd-126">In this case, the schedule is the set of times (specified by the union of all of the triggers associated with the work item) at which a work item will execute.</span></span>

## <a name="related-topics"></a><span data-ttu-id="356cd-127">См. также</span><span class="sxs-lookup"><span data-stu-id="356cd-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="356cd-128">Повторение задачи</span><span class="sxs-lookup"><span data-stu-id="356cd-128">Repeating A Task</span></span>](repeating-a-task.md)
</dt> <dt>

[<span data-ttu-id="356cd-129">Типы триггеров</span><span class="sxs-lookup"><span data-stu-id="356cd-129">Trigger Types</span></span>](trigger-types.md)
</dt> <dt>

[<span data-ttu-id="356cd-130">Интерфейсы триггера</span><span class="sxs-lookup"><span data-stu-id="356cd-130">Trigger Interfaces</span></span>](trigger-interfaces.md)
</dt> <dt>

[<span data-ttu-id="356cd-131">Сведения о планировщик задач</span><span class="sxs-lookup"><span data-stu-id="356cd-131">About The Task Scheduler</span></span>](about-the-task-scheduler.md)
</dt> </dl>

 

 




