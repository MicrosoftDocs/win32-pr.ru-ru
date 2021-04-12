---
title: планировщик задач структур и объединений
description: Содержит список структур и объединений, используемых API планировщик задач 1,0.
ms.assetid: 37dc7818-7719-4975-b7bd-f8c2d5cc008b
keywords:
- Планировщик задач планировщик задач, ссылки, структур и объединений
- триггеры планировщик задач, структуры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bdb73620ccd92eed3ce8aea9bf5a17c5734d926
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104252886"
---
# <a name="task-scheduler-structures-and-unions"></a><span data-ttu-id="a58e0-105">планировщик задач структур и объединений</span><span class="sxs-lookup"><span data-stu-id="a58e0-105">Task Scheduler Structures and Unions</span></span>

<span data-ttu-id="a58e0-106">В этом разделе описываются структуры и объединения, используемые интерфейсами API планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="a58e0-106">This section describes the structures and unions used by the Task Scheduler APIs.</span></span>

<span data-ttu-id="a58e0-107">Все структуры и объединения, приведенные ниже, используются планировщик задач 1,0.</span><span class="sxs-lookup"><span data-stu-id="a58e0-107">All the structures and unions below are used by Task Scheduler 1.0.</span></span>



| <span data-ttu-id="a58e0-108">Имя</span><span class="sxs-lookup"><span data-stu-id="a58e0-108">Name</span></span>                                               | <span data-ttu-id="a58e0-109">Описание</span><span class="sxs-lookup"><span data-stu-id="a58e0-109">Description</span></span>                                                                                                                     |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a58e0-110">**ОБНОВЛЯЕТСЯ**</span><span class="sxs-lookup"><span data-stu-id="a58e0-110">**DAILY**</span></span>](/windows/desktop/api/Mstask/ns-mstask-daily)                             | <span data-ttu-id="a58e0-111">Определяет интервал в днях, в течение которого выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="a58e0-111">Defines the interval, in days, at which a task is run.</span></span>                                                                          |
| [<span data-ttu-id="a58e0-112">**монслидате**</span><span class="sxs-lookup"><span data-stu-id="a58e0-112">**MONTHLYDATE**</span></span>](/windows/desktop/api/Mstask/ns-mstask-monthlydate)                 | <span data-ttu-id="a58e0-113">Определяет день месяца, в который будет выполняться задача.</span><span class="sxs-lookup"><span data-stu-id="a58e0-113">Defines the day of the month the task will run.</span></span>                                                                                 |
| [<span data-ttu-id="a58e0-114">**монслидов**</span><span class="sxs-lookup"><span data-stu-id="a58e0-114">**MONTHLYDOW**</span></span>](/windows/desktop/api/Mstask/ns-mstask-monthlydow)                   | <span data-ttu-id="a58e0-115">Определяет даты выполнения задачи по месяцам, неделям и дням недели.</span><span class="sxs-lookup"><span data-stu-id="a58e0-115">Defines the date(s) that the task runs by month, week, and day of the week.</span></span>                                                     |
| [<span data-ttu-id="a58e0-116">**\_триггер задачи**</span><span class="sxs-lookup"><span data-stu-id="a58e0-116">**TASK\_TRIGGER**</span></span>](/windows/desktop/api/Mstask/ns-mstask-task_trigger)              | <span data-ttu-id="a58e0-117">Определяет время выполнения запланированного [*рабочего элемента*](w.md).</span><span class="sxs-lookup"><span data-stu-id="a58e0-117">Defines the times to run a scheduled [*work item*](w.md).</span></span>                                                  |
| [<span data-ttu-id="a58e0-118">**\_объединение типов триггеров \_**</span><span class="sxs-lookup"><span data-stu-id="a58e0-118">**TRIGGER\_TYPE\_UNION**</span></span>](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) | <span data-ttu-id="a58e0-119">Определяет расписание вызова триггера в пределах члена **типа** структуры [**\_ триггера задачи**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) .</span><span class="sxs-lookup"><span data-stu-id="a58e0-119">Defines the invocation schedule of the trigger within the **Type** member of a [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure.</span></span> |
| [<span data-ttu-id="a58e0-120">**Запуск**</span><span class="sxs-lookup"><span data-stu-id="a58e0-120">**WEEKLY**</span></span>](/windows/desktop/api/Mstask/ns-mstask-weekly)                           | <span data-ttu-id="a58e0-121">Определяет интервал (в неделях) между вызовами задачи.</span><span class="sxs-lookup"><span data-stu-id="a58e0-121">Defines the interval, in weeks, between invocations of a task.</span></span>                                                                  |



 

 

 




