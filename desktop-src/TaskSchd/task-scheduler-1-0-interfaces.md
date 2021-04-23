---
title: Интерфейсы планировщик задач 1,0
description: Интерфейсы, описанные в следующих разделах, предоставляют программный доступ к функциональным возможностям, доступным в планировщик задач, используемом в операционных системах Windows 2000, Windows XP и Windows Server 2003.
ms.assetid: 25f9c1ad-1859-4788-a876-6f4faa6e556e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bab12b59d4b4561ecbe46c09a76c69209574c9d
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104261561"
---
# <a name="task-scheduler-10-interfaces"></a><span data-ttu-id="bd03c-103">Интерфейсы планировщик задач 1,0</span><span class="sxs-lookup"><span data-stu-id="bd03c-103">Task Scheduler 1.0 Interfaces</span></span>

<span data-ttu-id="bd03c-104">\[\[Этот API может быть изменен или недоступен в последующих версиях операционной системы или продукта.</span><span class="sxs-lookup"><span data-stu-id="bd03c-104">\[\[This API may be altered or unavailable in subsequent versions of the operating system or product.</span></span> <span data-ttu-id="bd03c-105">Вместо них используйте [планировщик задач интерфейсы 2,0](task-scheduler-2-0-interfaces.md) или [перечислимые типы планировщик задач 2,0](task-scheduler-2-0-enumerated-types.md) . \]\]</span><span class="sxs-lookup"><span data-stu-id="bd03c-105">Please use the [Task Scheduler 2.0 Interfaces](task-scheduler-2-0-interfaces.md) or [Task Scheduler 2.0 Enumerated Types](task-scheduler-2-0-enumerated-types.md) instead.\] \]</span></span>

<span data-ttu-id="bd03c-106">Интерфейсы, описанные в следующих разделах, предоставляют программный доступ к функциональным возможностям, доступным в планировщик задач, используемом в операционных системах Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="bd03c-106">The interfaces that are described in the following topics provide programmatic access to the functionality that is available within the Task Scheduler that is used in the Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span>

<span data-ttu-id="bd03c-107">В этих разделах содержится описание интерфейса, список свойств и методов, определенных интерфейсом, и примечания о специальных обстоятельствах, которые следует отметить при использовании интерфейса.</span><span class="sxs-lookup"><span data-stu-id="bd03c-107">These topics contain a description of the interface, a list of the properties and methods defined by the interface, and remarks about any special circumstances that should be noted when using the interface.</span></span>


<span data-ttu-id="bd03c-108">Следующие интерфейсы представлены планировщик задач 1,0.</span><span class="sxs-lookup"><span data-stu-id="bd03c-108">The following interfaces are introduced by Task Scheduler 1.0.</span></span>



| <span data-ttu-id="bd03c-109">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="bd03c-109">Interface</span></span>                                        | <span data-ttu-id="bd03c-110">Описание</span><span class="sxs-lookup"><span data-stu-id="bd03c-110">Description</span></span>                                                                                                                                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bd03c-111">**иенумворкитемс**</span><span class="sxs-lookup"><span data-stu-id="bd03c-111">**IEnumWorkItems**</span></span>](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems)         | <span data-ttu-id="bd03c-112">Предоставляет методы для перечисления задач в [*папке «Назначенные задания*](s.md)».</span><span class="sxs-lookup"><span data-stu-id="bd03c-112">Provides the methods for enumerating the tasks in the [*Scheduled Tasks folder*](s.md).</span></span>                                                                                                              |
| [<span data-ttu-id="bd03c-113">**ипровидетаскпаже**</span><span class="sxs-lookup"><span data-stu-id="bd03c-113">**IProvideTaskPage**</span></span>](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage)     | <span data-ttu-id="bd03c-114">Предоставляет методы для доступа к параметрам страницы свойств задачи.</span><span class="sxs-lookup"><span data-stu-id="bd03c-114">Provides the methods to access the property sheet settings of a task.</span></span>                                                                                                                                                                 |
| [<span data-ttu-id="bd03c-115">**исчедуледворкитем**</span><span class="sxs-lookup"><span data-stu-id="bd03c-115">**IScheduledWorkItem**</span></span>](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) | <span data-ttu-id="bd03c-116">Предоставляет методы для управления конкретными [*рабочими элементами*](w.md).</span><span class="sxs-lookup"><span data-stu-id="bd03c-116">Provides the methods for managing specific [*work items*](w.md).</span></span>                                                                                                                                                 |
| [<span data-ttu-id="bd03c-117">**ITask**</span><span class="sxs-lookup"><span data-stu-id="bd03c-117">**ITask**</span></span>](/windows/desktop/api/Mstask/nn-mstask-itask)                           | <span data-ttu-id="bd03c-118">Предоставляет методы для выполнения задач, получения или задания сведений о задачах, а также для завершения задач.</span><span class="sxs-lookup"><span data-stu-id="bd03c-118">Provides the methods for running tasks, getting or setting task information, and terminating tasks.</span></span> <span data-ttu-id="bd03c-119">Он является производным от интерфейса [**исчедуледворкитем**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) и наследует все методы этого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="bd03c-119">It is derived from the [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface and inherits all the methods of that interface.</span></span> |
| [<span data-ttu-id="bd03c-120">**итасксчедулер**</span><span class="sxs-lookup"><span data-stu-id="bd03c-120">**ITaskScheduler**</span></span>](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler)         | <span data-ttu-id="bd03c-121">Предоставляет методы для планирования задач.</span><span class="sxs-lookup"><span data-stu-id="bd03c-121">Provides the methods for scheduling tasks.</span></span>                                                                                                                                                                                            |
| [<span data-ttu-id="bd03c-122">**итасктригжер**</span><span class="sxs-lookup"><span data-stu-id="bd03c-122">**ITaskTrigger**</span></span>](/windows/desktop/api/Mstask/nn-mstask-itasktrigger)             | <span data-ttu-id="bd03c-123">Предоставляет методы для доступа и настройки триггеров для задачи.</span><span class="sxs-lookup"><span data-stu-id="bd03c-123">Provides the methods for accessing and setting triggers for a task.</span></span> <span data-ttu-id="bd03c-124">Триггеры указывают время начала задачи, критерии повторения и другие параметры, управляющие запуском задачи.</span><span class="sxs-lookup"><span data-stu-id="bd03c-124">Triggers specify task start times, repetition criteria, and other parameters that control when a task is run.</span></span>                                                     |



 

 

 




