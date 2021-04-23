---
title: Перечислимые типы планировщик задач 2,0
description: Описывает перечислимые типы, которые определяют константы, используемые API-интерфейсами планировщик задач 2,0.
ms.assetid: d59f017e-df32-4826-954d-9ba338282d0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db410564ab97f0477ecac8aeda2b54b8fd655d62
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104339760"
---
# <a name="task-scheduler-20-enumerated-types"></a><span data-ttu-id="e2c1a-103">Перечислимые типы планировщик задач 2,0</span><span class="sxs-lookup"><span data-stu-id="e2c1a-103">Task Scheduler 2.0 Enumerated Types</span></span>

<span data-ttu-id="e2c1a-104">Описывает перечислимые типы, которые определяют константы, используемые API-интерфейсами планировщик задач 2,0.</span><span class="sxs-lookup"><span data-stu-id="e2c1a-104">Describes the enumerated types that define the constants that are used by the Task Scheduler 2.0 APIs.</span></span>


<span data-ttu-id="e2c1a-105">Следующие перечислимые типы введены в планировщик задач 2,0.</span><span class="sxs-lookup"><span data-stu-id="e2c1a-105">The following enumerated types are introduced in Task Scheduler 2.0.</span></span>



| <span data-ttu-id="e2c1a-106">Перечисление</span><span class="sxs-lookup"><span data-stu-id="e2c1a-106">Enumeration</span></span>                                                                  | <span data-ttu-id="e2c1a-107">Описание</span><span class="sxs-lookup"><span data-stu-id="e2c1a-107">Description</span></span>                                                                                                      |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e2c1a-108">**\_тип действия \_ задачи**</span><span class="sxs-lookup"><span data-stu-id="e2c1a-108">**TASK\_ACTION\_TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)                               | <span data-ttu-id="e2c1a-109">Определяет тип действий, которые может выполнять задача.</span><span class="sxs-lookup"><span data-stu-id="e2c1a-109">Defines the type of actions that a task can perform.</span></span>                                                             |
| [<span data-ttu-id="e2c1a-110">**\_совместимость задач**</span><span class="sxs-lookup"><span data-stu-id="e2c1a-110">**TASK\_COMPATIBILITY**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_compatibility)                            | <span data-ttu-id="e2c1a-111">Определяет версии планировщик задач или команды AT, с которыми совместима задача.</span><span class="sxs-lookup"><span data-stu-id="e2c1a-111">Defines what versions of Task Scheduler or the AT command that the task is compatible with.</span></span>                      |
| [<span data-ttu-id="e2c1a-112">**\_Создание задачи**</span><span class="sxs-lookup"><span data-stu-id="e2c1a-112">**TASK\_CREATION**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_creation)                                       | <span data-ttu-id="e2c1a-113">Определяет, как служба планировщик задач создает, обновляет или отключает задачу.</span><span class="sxs-lookup"><span data-stu-id="e2c1a-113">Defines how the Task Scheduler service creates, updates, or disables the task.</span></span>                                   |
| [<span data-ttu-id="e2c1a-114">**\_ \_ флаги перечисления задач**</span><span class="sxs-lookup"><span data-stu-id="e2c1a-114">**TASK\_ENUM\_FLAGS**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_enum_flags)                                 | <span data-ttu-id="e2c1a-115">Определяет, как планировщик задач перечисляется с помощью зарегистрированных задач.</span><span class="sxs-lookup"><span data-stu-id="e2c1a-115">Defines how the Task Scheduler enumerates through registered tasks.</span></span>                                              |
| [<span data-ttu-id="e2c1a-116">**\_политика экземпляров \_ задач**</span><span class="sxs-lookup"><span data-stu-id="e2c1a-116">**TASK\_INSTANCES\_POLICY**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy)                     | <span data-ttu-id="e2c1a-117">Определяет, как планировщик задач обрабатывает существующие экземпляры задачи при запуске нового экземпляра задачи.</span><span class="sxs-lookup"><span data-stu-id="e2c1a-117">Defines how the Task Scheduler handles existing instances of the task when it starts a new instance of the task.</span></span> |
| [<span data-ttu-id="e2c1a-118">**\_тип входа задачи**</span><span class="sxs-lookup"><span data-stu-id="e2c1a-118">**TASK\_LOGON TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type)                                  | <span data-ttu-id="e2c1a-119">Определяет, какой метод входа необходим для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="e2c1a-119">Defines what logon technique is required to run a task.</span></span>                                                          |
| [<span data-ttu-id="e2c1a-120">**\_тип ПРОЦЕССТОКЕНСИД \_ задачи**</span><span class="sxs-lookup"><span data-stu-id="e2c1a-120">**TASK\_PROCESSTOKENSID\_TYPE**</span></span>](/windows/win32/api/taskschd/ne-taskschd-task_processtokensid_type)             | <span data-ttu-id="e2c1a-121">Определяет типы идентификаторов безопасности процесса, которые могут использоваться задачами.</span><span class="sxs-lookup"><span data-stu-id="e2c1a-121">Defines the types of process SID that can be used by tasks.</span></span>                                                      |
| [<span data-ttu-id="e2c1a-122">**\_ \_ Флаги запуска задач**</span><span class="sxs-lookup"><span data-stu-id="e2c1a-122">**TASK\_RUN\_FLAGS**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_run_flags)                                   | <span data-ttu-id="e2c1a-123">Определяет, как выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="e2c1a-123">Defines how a task is run.</span></span>                                                                                       |
| [<span data-ttu-id="e2c1a-124">**\_тип RUNLEVEL \_ задачи**</span><span class="sxs-lookup"><span data-stu-id="e2c1a-124">**TASK\_RUNLEVEL\_TYPE**</span></span>](/windows/win32/api/taskschd/ne-taskschd-task_runlevel_type)                           | <span data-ttu-id="e2c1a-125">Определяет флаги повышения прав LUA, указывающие, какой уровень привилегий будет выполняться задачей.</span><span class="sxs-lookup"><span data-stu-id="e2c1a-125">Defines LUA elevation flags that specify with what privilege level the task will be run.</span></span>                         |
| [<span data-ttu-id="e2c1a-126">**\_ \_ \_ тип изменения состояния сеанса \_ задачи**</span><span class="sxs-lookup"><span data-stu-id="e2c1a-126">**TASK\_SESSION\_STATE\_CHANGE\_TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_session_state_change_type) | <span data-ttu-id="e2c1a-127">Определяет, какие виды изменений состояния сеанса сервера терминалов можно использовать для запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="e2c1a-127">Defines what kinds of Terminal Server session state change you can use to trigger a task to start.</span></span>               |
| [<span data-ttu-id="e2c1a-128">**\_состояние задачи**</span><span class="sxs-lookup"><span data-stu-id="e2c1a-128">**TASK\_STATE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_state)                                            | <span data-ttu-id="e2c1a-129">Определяет различные состояния, в которых может находиться зарегистрированная задача.</span><span class="sxs-lookup"><span data-stu-id="e2c1a-129">Defines the different states that a registered task can be in.</span></span>                                                   |
| [<span data-ttu-id="e2c1a-130">**\_Тип 2 триггера задачи \_**</span><span class="sxs-lookup"><span data-stu-id="e2c1a-130">**TASK\_TRIGGER\_TYPE2**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2)                                  | <span data-ttu-id="e2c1a-131">Определяет тип триггеров, которые могут использоваться задачами.</span><span class="sxs-lookup"><span data-stu-id="e2c1a-131">Defines the type of triggers that can be used by tasks.</span></span>                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="e2c1a-132">См. также</span><span class="sxs-lookup"><span data-stu-id="e2c1a-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2c1a-133">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="e2c1a-133">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="e2c1a-134">Справочник по планировщик задач</span><span class="sxs-lookup"><span data-stu-id="e2c1a-134">Task Scheduler Reference</span></span>](task-scheduler-reference.md)
</dt> </dl>

 

 




