---
title: T (планировщик задач)
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d4c6d7ba-7bca-420d-a4dc-4daea816f99c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2730cdbe3a13456aed0e613a614d43a0e56e6673
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104533668"
---
# <a name="t-task-scheduler"></a><span data-ttu-id="06df8-103">T (планировщик задач)</span><span class="sxs-lookup"><span data-stu-id="06df8-103">T (Task Scheduler)</span></span>

<span data-ttu-id="06df8-104">A B C D [E](e.md) F G р [. J K](i.md) L M N O [P](p.md) Q R [S](s.md) T U V [W](w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="06df8-104">A B C D [E](e.md) F G H [I](i.md) J K L M N O [P](p.md) Q R [S](s.md) T U V [W](w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="06df8-105"><span id="_msb_task_objects_gly"></span><span id="_MSB_TASK_OBJECTS_GLY"></span>**объекты Task**</span><span class="sxs-lookup"><span data-stu-id="06df8-105"><span id="_msb_task_objects_gly"></span><span id="_MSB_TASK_OBJECTS_GLY"></span>**task objects**</span></span>
</dt> <dd>

<span data-ttu-id="06df8-106">Экземпляры объекта, предоставляющие методы для управления задачами.</span><span class="sxs-lookup"><span data-stu-id="06df8-106">Instances of an object that provides methods for managing tasks.</span></span> <span data-ttu-id="06df8-107">Сюда входят методы установки и извлечения свойств. выполнение, остановка и удаление задач; и создание новых триггеров и получение старых триггеров.</span><span class="sxs-lookup"><span data-stu-id="06df8-107">This includes methods for setting and retrieving properties; running, terminating, and deleting tasks; and creating new triggers and retrieving old triggers.</span></span>

<span data-ttu-id="06df8-108">Объект Task создается вызовами методов [**исчедуледворкитем:: CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) и [**исчедуледворкитем::**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettrigger)GetObject.</span><span class="sxs-lookup"><span data-stu-id="06df8-108">The task object is created by calls to [**IScheduledWorkItem::CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) and [**IScheduledWorkItem::GetTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettrigger).</span></span>

</dd> <dt>

<span data-ttu-id="06df8-109"><span id="_msb_task_scheduler_objects_gly"></span><span id="_MSB_TASK_SCHEDULER_OBJECTS_GLY"></span>**объекты планировщика заданий**</span><span class="sxs-lookup"><span data-stu-id="06df8-109"><span id="_msb_task_scheduler_objects_gly"></span><span id="_MSB_TASK_SCHEDULER_OBJECTS_GLY"></span>**task scheduler objects**</span></span>
</dt> <dd>

<span data-ttu-id="06df8-110">Экземпляры объекта, представляющие службу планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="06df8-110">Instances of an object the represents the Task Scheduler service.</span></span> <span data-ttu-id="06df8-111">Этот объект поддерживает два интерфейса: **IUnknown** и [**итасксчедулер**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) (в настоящее время это только рабочие элементы, поддерживаемые службой планировщик задач).</span><span class="sxs-lookup"><span data-stu-id="06df8-111">This object supports two interfaces: **IUnknown** and [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) (currently tasks are the only type of work items supported by the Task Scheduler service).</span></span>

<span data-ttu-id="06df8-112">Объекты планировщика задач создаются вызовами метода **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="06df8-112">Task scheduler objects are created by calls to **CoCreateInstance**.</span></span>

</dd> <dt>

<span data-ttu-id="06df8-113"><span id="_msb_task_trigger_objects_gly"></span><span id="_MSB_TASK_TRIGGER_OBJECTS_GLY"></span>**объекты триггеров задач**</span><span class="sxs-lookup"><span data-stu-id="06df8-113"><span id="_msb_task_trigger_objects_gly"></span><span id="_MSB_TASK_TRIGGER_OBJECTS_GLY"></span>**task trigger objects**</span></span>
</dt> <dd>

<span data-ttu-id="06df8-114">Экземпляры объекта предоставляет методы для установки и извлечения триггеров задач.</span><span class="sxs-lookup"><span data-stu-id="06df8-114">Instances of an object the provides methods for setting and retrieving task triggers.</span></span> <span data-ttu-id="06df8-115">Этот объект поддерживает два интерфейса: **IUnknown** и [**итасктригжер**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger).</span><span class="sxs-lookup"><span data-stu-id="06df8-115">This object supports two interfaces: **IUnknown** and [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger).</span></span>

<span data-ttu-id="06df8-116">Объекты триггеров задач создаются вызовами методов [**исчедуледворкитем:: CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) и [**Исчедуледворкитем:: Trigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettrigger).</span><span class="sxs-lookup"><span data-stu-id="06df8-116">Task trigger objects are created by calls to [**IScheduledWorkItem::CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) and [**IScheduledWorkItem::GetTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettrigger).</span></span>

<span data-ttu-id="06df8-117">См. также: *триггеры*.</span><span class="sxs-lookup"><span data-stu-id="06df8-117">See also: *triggers*.</span></span>

</dd> <dt>

<span data-ttu-id="06df8-118"><span id="_msb_tasks_gly"></span><span id="_MSB_TASKS_GLY"></span>**операции**</span><span class="sxs-lookup"><span data-stu-id="06df8-118"><span id="_msb_tasks_gly"></span><span id="_MSB_TASKS_GLY"></span>**tasks**</span></span>
</dt> <dd>

<span data-ttu-id="06df8-119">Любой элемент, который может выполняться планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="06df8-119">Any item that the Task Scheduler can execute.</span></span> <span data-ttu-id="06df8-120">Эти элементы могут включать любое из следующих элементов (как поддерживается операционной системой, в которой будет выполняться задача): Win32® приложениями, приложениями Win16, приложениями OS/2, приложениями MS-DOS®, пакетными файлами ( \* bat), командными файлами ( \* cmd) или любым надлежащим образом зарегистрированным типом файлов.</span><span class="sxs-lookup"><span data-stu-id="06df8-120">These items may include any of the following (as supported by the operating system on which the task will execute): Win32® applications, Win16 applications, OS/2 applications, MS-DOS® applications, batch files (\*.bat), command files (\*.cmd), or any properly registered file type.</span></span>

</dd> <dt>

<span data-ttu-id="06df8-121"><span id="_msb_tasks_folder_gly"></span><span id="_MSB_TASKS_FOLDER_GLY"></span>**Папка Tasks**</span><span class="sxs-lookup"><span data-stu-id="06df8-121"><span id="_msb_tasks_folder_gly"></span><span id="_MSB_TASKS_FOLDER_GLY"></span>**Tasks folder**</span></span>
</dt> <dd>

<span data-ttu-id="06df8-122">Папка, в которой перечислены все файлы задач (в настоящее время задачи являются единственными доступными рабочими элементами).</span><span class="sxs-lookup"><span data-stu-id="06df8-122">The folder that lists all task files (currently, tasks are the only work items available).</span></span> <span data-ttu-id="06df8-123">Эти файлы содержат сведения о задаче.</span><span class="sxs-lookup"><span data-stu-id="06df8-123">These files contain the information about the task.</span></span> <span data-ttu-id="06df8-124">Имена этих файлов отражают имя задачи.</span><span class="sxs-lookup"><span data-stu-id="06df8-124">The name of these files reflects the name of the task.</span></span>

<span data-ttu-id="06df8-125">Расположение папки Tasks можно извлечь из реестра, получая данные следующего значения:</span><span class="sxs-lookup"><span data-stu-id="06df8-125">You can retrieve the location of the Tasks folder from the registry by getting data for the following value:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         SchedulingAgent
            TasksFolder
```

</dd> <dt>

<span data-ttu-id="06df8-126"><span id="_msb_triggers_gly"></span><span id="_MSB_TRIGGERS_GLY"></span>**план**</span><span class="sxs-lookup"><span data-stu-id="06df8-126"><span id="_msb_triggers_gly"></span><span id="_MSB_TRIGGERS_GLY"></span>**triggers**</span></span>
</dt> <dd>

<span data-ttu-id="06df8-127">Набор критериев, которые при выполнении приведут к выполнению задачи.</span><span class="sxs-lookup"><span data-stu-id="06df8-127">A set of criteria that, when met, will cause a task to be executed.</span></span> <span data-ttu-id="06df8-128">Планировщик задач предоставляет триггеры на основе времени и событий, которые могут указывать время запуска задачи, критерии повторения и другие параметры.</span><span class="sxs-lookup"><span data-stu-id="06df8-128">Task Scheduler provides time-based and event-based triggers that can specify task start times, repetition criteria, and other parameters.</span></span>

</dd> <dt>

<span data-ttu-id="06df8-129"><span id="_msb_trigger_strings_gly"></span><span id="_MSB_TRIGGER_STRINGS_GLY"></span>**строки триггера**</span><span class="sxs-lookup"><span data-stu-id="06df8-129"><span id="_msb_trigger_strings_gly"></span><span id="_MSB_TRIGGER_STRINGS_GLY"></span>**trigger strings**</span></span>
</dt> <dd>

<span data-ttu-id="06df8-130">Строка, описывающая триггер.</span><span class="sxs-lookup"><span data-stu-id="06df8-130">A string that describes the trigger.</span></span> <span data-ttu-id="06df8-131">Эта строка создается службой планировщик задач и отображается в пользовательском интерфейсе планировщик задач в форме, подобной "at 2PM каждый день, начиная с 5/11/97".</span><span class="sxs-lookup"><span data-stu-id="06df8-131">This string is created by the Task Scheduler service, and appears in the Task Scheduler user interface in a form similar to "At 2PM every day, starting 5/11/97."</span></span>

</dd> <dt>

<span data-ttu-id="06df8-132"><span id="_msb_trigger_structures_gly"></span><span id="_MSB_TRIGGER_STRUCTURES_GLY"></span>**структуры триггеров**</span><span class="sxs-lookup"><span data-stu-id="06df8-132"><span id="_msb_trigger_structures_gly"></span><span id="_MSB_TRIGGER_STRUCTURES_GLY"></span>**trigger structures**</span></span>
</dt> <dd>

<span data-ttu-id="06df8-133">Структура [**\_ триггера задачи**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) , используемая при задании или извлечении критериев, определяющих триггер.</span><span class="sxs-lookup"><span data-stu-id="06df8-133">The [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure used when setting or retrieving the criteria that defines the trigger.</span></span> <span data-ttu-id="06df8-134">Критерий включает срабатывание триггера и тип триггера.</span><span class="sxs-lookup"><span data-stu-id="06df8-134">The criteria includes when the trigger will fire, and the type of the trigger.</span></span>

</dd> </dl>

 

 




