---
title: Структуры триггеров для планировщик задач 1,0
description: Планировщик задач 1,0 использует несколько структур для определения критериев триггера.
ms.assetid: dd2ae4f6-fb2d-41f8-9400-7426b7ca4546
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a03f28f85782d87ee3349582929babe6f907e8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068106"
---
# <a name="trigger-structures-for-task-scheduler-10"></a><span data-ttu-id="50c51-103">Структуры триггеров для планировщик задач 1,0</span><span class="sxs-lookup"><span data-stu-id="50c51-103">Trigger Structures for Task Scheduler 1.0</span></span>

<span data-ttu-id="50c51-104">Планировщик задач 1,0 использует несколько структур для определения критериев триггера.</span><span class="sxs-lookup"><span data-stu-id="50c51-104">Task Scheduler 1.0 uses several structures to define the criteria of a trigger.</span></span>

> [!Note]  
> <span data-ttu-id="50c51-105">Дополнительные сведения о триггерах планировщик задач 2,0 см. в разделе [Trigger interfaces](trigger-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="50c51-105">For more information about Task Scheduler 2.0 triggers, see [Trigger Interfaces](trigger-interfaces.md).</span></span>

 

## <a name="task-scheduler-10-structures"></a><span data-ttu-id="50c51-106">Планировщик задач структуры 1,0</span><span class="sxs-lookup"><span data-stu-id="50c51-106">Task Scheduler 1.0 Structures</span></span>

<span data-ttu-id="50c51-107">На следующем рисунке показана [**Структура \_ триггера задачи**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) .</span><span class="sxs-lookup"><span data-stu-id="50c51-107">The following illustration shows the [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure.</span></span> <span data-ttu-id="50c51-108">Он имеет три обязательных элемента (**вбегинеар**, **вбегинмонс** и **вбегиндай**), которые должны быть заданы при создании нового триггера.</span><span class="sxs-lookup"><span data-stu-id="50c51-108">It has three required members (**wBeginYear**, **wBeginMonth**, and **wBeginDay**) that must be set when creating a new trigger.</span></span> <span data-ttu-id="50c51-109">(Чтобы перейти на страницу ссылки для этой структуры, щелкните имя структуры на рисунке.)</span><span class="sxs-lookup"><span data-stu-id="50c51-109">(To jump to the reference page for this structure, click the structure name in the illustration.)</span></span>

![Структура триггера задачи](images/tsktri1.png)

<span data-ttu-id="50c51-111">Имейте в виду, что элемент **triggerType может принимать** использует перечисление [**\_ \_ типа триггера задачи**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) , а член **типа** использует структуру **\_ \_ объединения триггера задачи** .</span><span class="sxs-lookup"><span data-stu-id="50c51-111">Be aware that the **TriggerType** member uses the [**TASK\_TRIGGER\_TYPE**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) enumeration and the **Type** member uses a **TASK\_TRIGGER\_UNION** structure.</span></span> <span data-ttu-id="50c51-112">Перечисление **\_ \_ типов триггеров задач** используется для указания типа триггера (типы триггеров на основе событий и времени).</span><span class="sxs-lookup"><span data-stu-id="50c51-112">The **TASK\_TRIGGER\_TYPE** enumeration is used to specify the type of trigger (event and time-based trigger types).</span></span> <span data-ttu-id="50c51-113">Структура [**\_ \_ объединения типов триггеров**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) используется для объединения монслидатеных [**,**](/windows/desktop/api/Mstask/ns-mstask-daily) [**еженедельных**](/windows/desktop/api/Mstask/ns-mstask-weekly), [](/windows/desktop/api/Mstask/ns-mstask-monthlydate) (дней месяца) и [**монслидов**](/windows/desktop/api/Mstask/ns-mstask-monthlydow) (день недели) структур, которые используются для указания времени срабатывания триггера на основе часов.</span><span class="sxs-lookup"><span data-stu-id="50c51-113">The [**TRIGGER\_TYPE\_UNION**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) structure is used to combine the [**DAILY**](/windows/desktop/api/Mstask/ns-mstask-daily), [**WEEKLY**](/windows/desktop/api/Mstask/ns-mstask-weekly), [**MONTHLYDATE**](/windows/desktop/api/Mstask/ns-mstask-monthlydate) (day of month), and [**MONTHLYDOW**](/windows/desktop/api/Mstask/ns-mstask-monthlydow) (day of week) structures that are used to specify when a time-based trigger will fire.</span></span>

<span data-ttu-id="50c51-114">Если **triggerType может принимать** указывает одноразовый триггер на основе времени или триггер на основе события, член **типа** игнорируется.</span><span class="sxs-lookup"><span data-stu-id="50c51-114">If **TriggerType** specifies a one-time time-based trigger or an event-based trigger, the **Type** member is ignored.</span></span> <span data-ttu-id="50c51-115">Структура [**\_ \_ объединения типа триггера**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) используется только в том случае, если элемент **triggerType может принимать** задает ежедневный, еженедельный, день месяца или ежемесячный триггер на основе времени недели.</span><span class="sxs-lookup"><span data-stu-id="50c51-115">The [**TRIGGER\_TYPE\_UNION**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) structure is used only if the **TriggerType** member specifies a daily, weekly, day-of-month, or monthly day-of-week time-based trigger.</span></span>

<span data-ttu-id="50c51-116">Кроме того, параметр члена **типа** указывает, какой элемент структуры [**\_ \_ объединения типа триггера**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) используется.</span><span class="sxs-lookup"><span data-stu-id="50c51-116">In addition, the setting of the **Type** member indicates which member of the [**TRIGGER\_TYPE\_UNION**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) structure is used.</span></span> <span data-ttu-id="50c51-117">На следующем рисунке показана связь между значениями перечисления [**\_ \_ типов триггеров задач**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) и элементами структуры **\_ \_ типа триггера** .</span><span class="sxs-lookup"><span data-stu-id="50c51-117">The following illustration shows the relationship between the values of the [**TASK\_TRIGGER\_TYPE**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) enumeration and the members of the **TRIGGER\_TYPE\_STRUCTURE** structure.</span></span> <span data-ttu-id="50c51-118">(Чтобы перейти на страницы ссылок для этих структур, щелкните имя структуры на рисунке.)</span><span class="sxs-lookup"><span data-stu-id="50c51-118">(To jump to the reference pages for these structures click the structure name in the illustration.)</span></span>

![отношение между значениями перечисления типа триггера задачи и элементами структуры типа триггера](images/tsktri3.png)

## <a name="related-topics"></a><span data-ttu-id="50c51-120">См. также</span><span class="sxs-lookup"><span data-stu-id="50c51-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50c51-121">Триггеры задач</span><span class="sxs-lookup"><span data-stu-id="50c51-121">Task Triggers</span></span>](task-triggers.md)
</dt> <dt>

[<span data-ttu-id="50c51-122">Типы триггеров</span><span class="sxs-lookup"><span data-stu-id="50c51-122">Trigger Types</span></span>](trigger-types.md)
</dt> <dt>

[<span data-ttu-id="50c51-123">Интерфейсы триггера</span><span class="sxs-lookup"><span data-stu-id="50c51-123">Trigger Interfaces</span></span>](trigger-interfaces.md)
</dt> </dl>

 

 




