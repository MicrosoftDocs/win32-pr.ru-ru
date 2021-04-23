---
title: Триггеры бездействия для планировщик задач 1,0
description: Триггер простоя — это триггер на основе событий, который запускается определенное число раз после бездействия компьютера. Существует несколько условий, которые определяют, когда компьютер переходит в состояние простоя, например, когда не происходит ввода с клавиатуры или мыши.
ms.assetid: f2e0b120-dadc-470f-8349-42843149bb60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d6a19f3f6d474a9463667316e353a4803ab8fa9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105681416"
---
# <a name="idle-triggers-for-task-scheduler-10"></a><span data-ttu-id="faf4b-104">Триггеры бездействия для планировщик задач 1,0</span><span class="sxs-lookup"><span data-stu-id="faf4b-104">Idle Triggers for Task Scheduler 1.0</span></span>

<span data-ttu-id="faf4b-105">Триггер простоя — это триггер на основе событий, который запускается определенное число раз после бездействия компьютера.</span><span class="sxs-lookup"><span data-stu-id="faf4b-105">An idle trigger is an event-based trigger that is fired a specific number of times after the computer becomes idle.</span></span> <span data-ttu-id="faf4b-106">Существует несколько условий, которые определяют, когда компьютер переходит в состояние простоя, например, когда не происходит ввода с клавиатуры или мыши.</span><span class="sxs-lookup"><span data-stu-id="faf4b-106">There are multiple conditions that define when a computer becomes idle, such as when no keyboard or mouse input occurs.</span></span>

<span data-ttu-id="faf4b-107">Триггеры простоя создаются путем указания \_ \_ триггера события задачи \_ в \_ состоянии простоя в элементе [**\_ \_ типа триггера**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) задачи в структуре [**\_ триггера задачи**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) .</span><span class="sxs-lookup"><span data-stu-id="faf4b-107">Idle triggers are created by specifying TASK\_EVENT\_TRIGGER\_ON\_IDLE in the [**TASK\_TRIGGER\_TYPE**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) member of the [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure.</span></span> <span data-ttu-id="faf4b-108">Триггер Idle срабатывает, когда система переходит в состояние бездействия в течение времени, указанного в параметре время ожидания простоя рабочего элемента.</span><span class="sxs-lookup"><span data-stu-id="faf4b-108">The idle trigger is fired when the system becomes idle for the amount of time that is specified by the idle wait time of the work item.</span></span>

> [!Note]  
> <span data-ttu-id="faf4b-109">Если \_ задан триггер события задачи при \_ \_ \_ неактивном состоянии, члены **встарсаур**, **встартминуте** и **Type** структуры [**\_ триггера задачи**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) игнорируются.</span><span class="sxs-lookup"><span data-stu-id="faf4b-109">When TASK\_EVENT\_TRIGGER\_ON\_IDLE is specified, the **wStartHour**, **wStartMinute**, and **Type** members of the [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure are ignored.</span></span>

 

<span data-ttu-id="faf4b-110">Можно задать время ожидания простоя рабочего элемента, вызвав метод [**исчедуледворкитем:: сетидлеваит**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) .</span><span class="sxs-lookup"><span data-stu-id="faf4b-110">You can set the idle wait time of a work item by calling the [**IScheduledWorkItem::SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) method.</span></span> <span data-ttu-id="faf4b-111">Этот метод задает период времени (в минутах), в течение которого система должна оставаться неактивной до срабатывания триггера и выполнения рабочего элемента.</span><span class="sxs-lookup"><span data-stu-id="faf4b-111">This method sets the amount of time (in minutes) that the system must remain idle before the trigger is fired and the work item is executed.</span></span>

<span data-ttu-id="faf4b-112">Чтобы получить время простоя задачи, вызовите метод [**исчедуледворкитем:: жетидлеваит**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getidlewait) .</span><span class="sxs-lookup"><span data-stu-id="faf4b-112">To retrieve the idle time of a task, call the [**IScheduledWorkItem::GetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getidlewait) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="faf4b-113">См. также</span><span class="sxs-lookup"><span data-stu-id="faf4b-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="faf4b-114">Триггеры задач</span><span class="sxs-lookup"><span data-stu-id="faf4b-114">Task Triggers</span></span>](task-triggers.md)
</dt> </dl>

 

 




