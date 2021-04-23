---
title: Запланированные рабочие элементы
description: В планировщик задач используются два термина для описания того, что может запланировать рабочие элементы и задачи.
ms.assetid: 6ca182c3-eba8-43dd-bf2e-27dd972e3cf8
keywords:
- планировщик задач рабочих элементов
- рабочие элементы планировщик задач, по сравнению с задачами
- задачи планировщик задач
- задачи, планировщик задач, по сравнению с рабочими элементами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586747e4049529dcfe747959aae994360a7b1485
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329328"
---
# <a name="scheduled-work-items"></a><span data-ttu-id="394be-107">Запланированные рабочие элементы</span><span class="sxs-lookup"><span data-stu-id="394be-107">Scheduled Work Items</span></span>

<span data-ttu-id="394be-108">В планировщик задач используются два термина для описания того, что может запланировать: рабочие элементы и задачи.</span><span class="sxs-lookup"><span data-stu-id="394be-108">The Task Scheduler uses two terms to describe what it can schedule: work items and tasks.</span></span> <span data-ttu-id="394be-109">Из этих двух терминов [*Рабочий элемент*](w.md) является более общим термином, описывающим любой тип элемента, который можно запланировать.</span><span class="sxs-lookup"><span data-stu-id="394be-109">Of these two terms, [*work item*](w.md) is a more general term that describes any type of item that can be scheduled.</span></span> <span data-ttu-id="394be-110">*Рабочим элементом* может быть любой элемент, выполняемый службой планировщик задач в момент, определенный триггерами элемента.</span><span class="sxs-lookup"><span data-stu-id="394be-110">A *work item* can be any item that the Task Scheduler service runs at a time that is specified by the item's trigger(s).</span></span>

<span data-ttu-id="394be-111">В отличие от этого, [*задача*](t.md) — это конкретный тип рабочего элемента.</span><span class="sxs-lookup"><span data-stu-id="394be-111">In contrast, a [*task*](t.md) is a specific type of work item.</span></span> <span data-ttu-id="394be-112">В настоящее время только поддерживаемый тип запланированного рабочего элемента — это задача.</span><span class="sxs-lookup"><span data-stu-id="394be-112">Currently, the only type of scheduled work item that is supported is a task.</span></span>

<span data-ttu-id="394be-113">Интерфейс [**исчедуледворкитем**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) содержит методы, поддерживаемые всеми типами запланированных рабочих элементов.</span><span class="sxs-lookup"><span data-stu-id="394be-113">The [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface contains methods that are supported by all types of scheduled work items.</span></span> <span data-ttu-id="394be-114">Например, сведения об учетной записи, времени выполнения и комментарии, определяемые приложением, являются свойствами, которые могут применяться ко всем типам рабочих элементов.</span><span class="sxs-lookup"><span data-stu-id="394be-114">For example, account information, run times, and application-defined comments are properties that may apply to all types of work items.</span></span> <span data-ttu-id="394be-115">Эти свойства можно задать и получить с помощью интерфейса **исчедуледворкитем** .</span><span class="sxs-lookup"><span data-stu-id="394be-115">These properties can be set and retrieved through the **IScheduledWorkItem** interface.</span></span>

<span data-ttu-id="394be-116">Интерфейс [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) содержит методы, поддерживаемые только задачами.</span><span class="sxs-lookup"><span data-stu-id="394be-116">The [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface contains methods that are supported only by tasks.</span></span>

<span data-ttu-id="394be-117">Методы интерфейса [**исчедуледворкитем**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) в настоящее время наследуются интерфейсом [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) , и в будущем они будут унаследованы другими интерфейсами рабочих элементов.</span><span class="sxs-lookup"><span data-stu-id="394be-117">The methods of the [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface are currently inherited by the [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) interface and in the future will be inherited by other work item interfaces.</span></span>

| <span data-ttu-id="394be-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="394be-118">For examples of</span></span>                                              | <span data-ttu-id="394be-119">См.</span><span class="sxs-lookup"><span data-stu-id="394be-119">See</span></span>                                                                                        |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="394be-120">Создание новой задачи.</span><span class="sxs-lookup"><span data-stu-id="394be-120">Creating a new task.</span></span>                                         | [<span data-ttu-id="394be-121">Создание задачи с помощью примера Невворкитем</span><span class="sxs-lookup"><span data-stu-id="394be-121">Creating a Task Using NewWorkItem Example</span></span>](creating-a-task-using-newworkitem-example.md) |
| <span data-ttu-id="394be-122">Выполнение существующей задачи.</span><span class="sxs-lookup"><span data-stu-id="394be-122">Running an existing task.</span></span>                                    | [<span data-ttu-id="394be-123">Пример запуска задачи</span><span class="sxs-lookup"><span data-stu-id="394be-123">Starting a Task Example</span></span>](starting-a-task-example.md)                                     |
| <span data-ttu-id="394be-124">Получение свойств, которые применяются ко всем типам рабочих элементов.</span><span class="sxs-lookup"><span data-stu-id="394be-124">Retrieving properties that apply to all types of work items.</span></span> | [<span data-ttu-id="394be-125">Получение примеров свойств рабочего элемента</span><span class="sxs-lookup"><span data-stu-id="394be-125">Retrieving Work Item Property Examples</span></span>](retrieving-work-item-property-examples.md)       |
| <span data-ttu-id="394be-126">Задание свойств, которые применяются ко всем типам рабочих элементов.</span><span class="sxs-lookup"><span data-stu-id="394be-126">Setting properties that apply to all types of work items.</span></span>    | [<span data-ttu-id="394be-127">Примеры настройки свойств рабочих элементов</span><span class="sxs-lookup"><span data-stu-id="394be-127">Setting Work Item Property Examples</span></span>](setting-work-item-property-examples.md)             |



 

 

 




