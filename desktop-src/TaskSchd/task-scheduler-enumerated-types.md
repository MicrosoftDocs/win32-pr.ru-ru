---
title: планировщик задач перечислимых типов
description: Перечисляет перечисления, используемые интерфейсами API планировщик задач.
ms.assetid: 9779d32b-0142-41bb-88e2-df79a3b0c1b2
keywords:
- Планировщик задач планировщик задач, ссылки, перечислимые типы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a70c4a939d176516d47f6af8bc0825b414bf1de
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104533614"
---
# <a name="task-scheduler-enumerated-types"></a><span data-ttu-id="62afb-104">планировщик задач перечислимых типов</span><span class="sxs-lookup"><span data-stu-id="62afb-104">Task Scheduler Enumerated Types</span></span>

<span data-ttu-id="62afb-105">Описывает перечислимые типы, которые определяют константы, используемые интерфейсами API планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="62afb-105">Describes the enumerated types that define the constants that are used by the Task Scheduler APIs.</span></span>


<span data-ttu-id="62afb-106">Следующие перечислимые типы введены в планировщик задач 2,0.</span><span class="sxs-lookup"><span data-stu-id="62afb-106">The following enumerated types are introduced in Task Scheduler 2.0.</span></span>



| <span data-ttu-id="62afb-107">Перечисление</span><span class="sxs-lookup"><span data-stu-id="62afb-107">Enumeration</span></span>                                                                  | <span data-ttu-id="62afb-108">Описание</span><span class="sxs-lookup"><span data-stu-id="62afb-108">Description</span></span>                                                                                                      |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="62afb-109">**\_тип действия \_ задачи**</span><span class="sxs-lookup"><span data-stu-id="62afb-109">**TASK\_ACTION\_TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)                               | <span data-ttu-id="62afb-110">Определяет тип действий, которые может выполнять задача.</span><span class="sxs-lookup"><span data-stu-id="62afb-110">Defines the type of actions that a task can perform.</span></span>                                                             |
| [<span data-ttu-id="62afb-111">**\_совместимость задач**</span><span class="sxs-lookup"><span data-stu-id="62afb-111">**TASK\_COMPATIBILITY**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_compatibility)                            | <span data-ttu-id="62afb-112">Определяет версии планировщик задач или команды AT, с которыми совместима задача.</span><span class="sxs-lookup"><span data-stu-id="62afb-112">Defines what versions of Task Scheduler or the AT command that the task is compatible with.</span></span>                      |
| [<span data-ttu-id="62afb-113">**\_Создание задачи**</span><span class="sxs-lookup"><span data-stu-id="62afb-113">**TASK\_CREATION**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_creation)                                       | <span data-ttu-id="62afb-114">Определяет, как служба планировщик задач создает, обновляет или отключает задачу.</span><span class="sxs-lookup"><span data-stu-id="62afb-114">Defines how the Task Scheduler service creates, updates, or disables the task.</span></span>                                   |
| [<span data-ttu-id="62afb-115">**\_ \_ флаги перечисления задач**</span><span class="sxs-lookup"><span data-stu-id="62afb-115">**TASK\_ENUM\_FLAGS**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_enum_flags)                                 | <span data-ttu-id="62afb-116">Определяет, как планировщик задач перечисляется с помощью зарегистрированных задач.</span><span class="sxs-lookup"><span data-stu-id="62afb-116">Defines how the Task Scheduler enumerates through registered tasks.</span></span>                                              |
| [<span data-ttu-id="62afb-117">**\_политика экземпляров \_ задач**</span><span class="sxs-lookup"><span data-stu-id="62afb-117">**TASK\_INSTANCES\_POLICY**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy)                     | <span data-ttu-id="62afb-118">Определяет, как планировщик задач обрабатывает существующие экземпляры задачи при запуске нового экземпляра задачи.</span><span class="sxs-lookup"><span data-stu-id="62afb-118">Defines how the Task Scheduler handles existing instances of the task when it starts a new instance of the task.</span></span> |
| [<span data-ttu-id="62afb-119">**\_тип входа задачи**</span><span class="sxs-lookup"><span data-stu-id="62afb-119">**TASK\_LOGON TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type)                                  | <span data-ttu-id="62afb-120">Определяет, какой метод входа необходим для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="62afb-120">Defines what logon technique is required to run a task.</span></span>                                                          |
| [<span data-ttu-id="62afb-121">**\_тип ПРОЦЕССТОКЕНСИД задачи**</span><span class="sxs-lookup"><span data-stu-id="62afb-121">**TASK\_PROCESSTOKENSID TYPE**</span></span>](/windows/win32/api/taskschd/ne-taskschd-task_processtokensid_type)              | <span data-ttu-id="62afb-122">Определяет типы идентификаторов безопасности процесса, которые могут использоваться задачами.</span><span class="sxs-lookup"><span data-stu-id="62afb-122">Defines the types of process SID that can used by tasks.</span></span>                                                         |
| [<span data-ttu-id="62afb-123">**\_ \_ Флаги запуска задач**</span><span class="sxs-lookup"><span data-stu-id="62afb-123">**TASK\_RUN\_FLAGS**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_run_flags)                                   | <span data-ttu-id="62afb-124">Определяет, как выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="62afb-124">Defines how a task is run.</span></span>                                                                                       |
| [<span data-ttu-id="62afb-125">**\_тип RUNLEVEL \_ задачи**</span><span class="sxs-lookup"><span data-stu-id="62afb-125">**TASK\_RUNLEVEL\_TYPE**</span></span>](/windows/win32/api/taskschd/ne-taskschd-task_runlevel_type)                           | <span data-ttu-id="62afb-126">Определяет флаги повышения прав LUA, указывающие, какой уровень привилегий будет выполняться задачей.</span><span class="sxs-lookup"><span data-stu-id="62afb-126">Defines LUA elevation flags that specify with what privilege level the task will be run.</span></span>                         |
| [<span data-ttu-id="62afb-127">**\_ \_ \_ тип изменения состояния сеанса \_ задачи**</span><span class="sxs-lookup"><span data-stu-id="62afb-127">**TASK\_SESSION\_STATE\_CHANGE\_TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_session_state_change_type) | <span data-ttu-id="62afb-128">Определяет, какие виды изменений состояния сеанса сервера терминалов можно использовать для запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="62afb-128">Defines what kinds of Terminal Server session state change you can use to trigger a task to start.</span></span>               |
| [<span data-ttu-id="62afb-129">**\_состояние задачи**</span><span class="sxs-lookup"><span data-stu-id="62afb-129">**TASK\_STATE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_state)                                            | <span data-ttu-id="62afb-130">Определяет различные состояния, в которых может находиться зарегистрированная задача.</span><span class="sxs-lookup"><span data-stu-id="62afb-130">Defines the different states that a registered task can be in.</span></span>                                                   |
| [<span data-ttu-id="62afb-131">**\_Тип 2 триггера задачи \_**</span><span class="sxs-lookup"><span data-stu-id="62afb-131">**TASK\_TRIGGER\_TYPE2**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2)                                  | <span data-ttu-id="62afb-132">Определяет тип триггеров, которые могут использоваться задачами.</span><span class="sxs-lookup"><span data-stu-id="62afb-132">Defines the type of triggers that can be used by tasks.</span></span>                                                          |



 


> [!WARNING]
> <span data-ttu-id="62afb-133">Перечисления планировщик задач 1,0 доступны только в операционных системах Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="62afb-133">The Task Scheduler 1.0 enumerations are available only in Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="62afb-134">Они являются устаревшими в Windows Vista и могут быть полностью удалены в будущем.</span><span class="sxs-lookup"><span data-stu-id="62afb-134">They are deprecated as of Windows Vista and may be removed completely in the future.</span></span> <span data-ttu-id="62afb-135">Используйте перечисленные выше перечисления планировщик задач 2,0.</span><span class="sxs-lookup"><span data-stu-id="62afb-135">Please use the Task Scheduler 2.0 enumerations listed above instead.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="62afb-136">См. также</span><span class="sxs-lookup"><span data-stu-id="62afb-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62afb-137">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="62afb-137">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="62afb-138">Справочник по планировщик задач</span><span class="sxs-lookup"><span data-stu-id="62afb-138">Task Scheduler Reference</span></span>](task-scheduler-reference.md)
</dt> </dl>

 

 




