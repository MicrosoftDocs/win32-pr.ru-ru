---
title: Интерфейсы триггера
description: API-интерфейсы, используемые для управления триггерами, зависят от версии планировщик задач. Однако в обоих случаях эти API позволяют создавать новые триггеры, получать и обновлять существующие триггеры, а также удалять триггеры, которые больше не требуются.
ms.assetid: 94c11f11-72e2-404f-b396-ab7b1be71942
keywords:
- триггеры планировщик задач, интерфейсы
- триггеры планировщик задач, интерфейсы, описание
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5357bb745b43c51707d9571c7582a44c9225a7fe
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104339712"
---
# <a name="trigger-interfaces"></a><span data-ttu-id="5aede-106">Интерфейсы триггера</span><span class="sxs-lookup"><span data-stu-id="5aede-106">Trigger Interfaces</span></span>

<span data-ttu-id="5aede-107">API-интерфейсы, используемые для управления триггерами, зависят от версии планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="5aede-107">The APIs that are used to manage triggers vary depending on the version of the Task Scheduler.</span></span> <span data-ttu-id="5aede-108">Однако в обоих случаях эти API позволяют создавать новые триггеры, получать и обновлять существующие триггеры, а также удалять триггеры, которые больше не требуются.</span><span class="sxs-lookup"><span data-stu-id="5aede-108">However, in both cases these APIs enable you to create new triggers, retrieve and update existing triggers, and delete triggers that are no longer required.</span></span>


<span data-ttu-id="5aede-109">Приложения, разработанные с помощью планировщик задач 2,0, могут использовать объекты и интерфейсы для создания, извлечения, изменения и удаления триггеров для задачи.</span><span class="sxs-lookup"><span data-stu-id="5aede-109">Applications that are developed using Task Scheduler 2.0 can use objects and interfaces to create, retrieve, modify, and delete the triggers for a task.</span></span>

<span data-ttu-id="5aede-110">На следующем рисунке задача указывает коллекцию триггеров с помощью свойства Triggers.</span><span class="sxs-lookup"><span data-stu-id="5aede-110">In the following illustration, a task specifies a collection of triggers using its Triggers property.</span></span> <span data-ttu-id="5aede-111">Эта коллекция содержит один или несколько отдельных API-интерфейсов триггеров с каждым API, указывающим конкретный тип триггера.</span><span class="sxs-lookup"><span data-stu-id="5aede-111">This collection contains one or more individual trigger APIs with each API specifying a specific trigger type.</span></span> <span data-ttu-id="5aede-112">Например, на рисунке ниже в коллекции триггеров содержится триггер загрузки, триггер входа и ежедневный триггер.</span><span class="sxs-lookup"><span data-stu-id="5aede-112">For example, in the illustration below the trigger collection contains a boot trigger, logon trigger, and a daily trigger.</span></span>

![интерфейсы триггера планировщика заданий 2,0](images/tsktri4.png)

### <a name="object-apis-for-scripting-development"></a><span data-ttu-id="5aede-114">API объектов для разработки сценариев</span><span class="sxs-lookup"><span data-stu-id="5aede-114">Object APIs for Scripting Development</span></span>

<span data-ttu-id="5aede-115">Дополнительные сведения о методах и свойствах объектов, используемых для указания триггеров, см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="5aede-115">For more information about the methods and properties of the objects that are used to specify triggers, see:</span></span>

-   [<span data-ttu-id="5aede-116">**таскдефинитион**</span><span class="sxs-lookup"><span data-stu-id="5aede-116">**TaskDefinition**</span></span>](taskdefinition.md)
-   [<span data-ttu-id="5aede-117">**тригжерколлектион**</span><span class="sxs-lookup"><span data-stu-id="5aede-117">**TriggerCollection**</span></span>](triggercollection.md)
-   [<span data-ttu-id="5aede-118">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="5aede-118">**Trigger**</span></span>](trigger.md)
-   [<span data-ttu-id="5aede-119">**буттригжер**</span><span class="sxs-lookup"><span data-stu-id="5aede-119">**BootTrigger**</span></span>](boottrigger.md)
-   [<span data-ttu-id="5aede-120">**даилитригжер**</span><span class="sxs-lookup"><span data-stu-id="5aede-120">**DailyTrigger**</span></span>](dailytrigger.md)
-   [<span data-ttu-id="5aede-121">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="5aede-121">**EventTrigger**</span></span>](eventtrigger.md)
-   [<span data-ttu-id="5aede-122">**идлетригжер**</span><span class="sxs-lookup"><span data-stu-id="5aede-122">**IdleTrigger**</span></span>](idletrigger.md)
-   [<span data-ttu-id="5aede-123">**логонтригжер**</span><span class="sxs-lookup"><span data-stu-id="5aede-123">**LogonTrigger**</span></span>](logontrigger.md)
-   [<span data-ttu-id="5aede-124">**монслидовтригжер**</span><span class="sxs-lookup"><span data-stu-id="5aede-124">**MonthlyDOWTrigger**</span></span>](monthlydowtrigger.md)
-   [<span data-ttu-id="5aede-125">**монслитригжер**</span><span class="sxs-lookup"><span data-stu-id="5aede-125">**MonthlyTrigger**</span></span>](monthlytrigger.md)
-   [<span data-ttu-id="5aede-126">**регистратионтригжер**</span><span class="sxs-lookup"><span data-stu-id="5aede-126">**RegistrationTrigger**</span></span>](registrationtrigger.md)
-   [<span data-ttu-id="5aede-127">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="5aede-127">**TimeTrigger**</span></span>](timetrigger.md)
-   [<span data-ttu-id="5aede-128">**виклитригжер**</span><span class="sxs-lookup"><span data-stu-id="5aede-128">**WeeklyTrigger**</span></span>](weeklytrigger.md)

### <a name="interfaces-apis-for-c-development"></a><span data-ttu-id="5aede-129">API интерфейсов для разработки на C++</span><span class="sxs-lookup"><span data-stu-id="5aede-129">Interfaces APIs for C++ Development</span></span>

<span data-ttu-id="5aede-130">Дополнительные сведения о методах и свойствах интерфейсов, используемых для указания триггеров, см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="5aede-130">For more information about the methods and properties of the interfaces that are used to specify triggers, see:</span></span>

-   [<span data-ttu-id="5aede-131">**итаскдефинитион**</span><span class="sxs-lookup"><span data-stu-id="5aede-131">**ITaskDefinition**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition)
-   [<span data-ttu-id="5aede-132">**ITriggerCollection**</span><span class="sxs-lookup"><span data-stu-id="5aede-132">**ITriggerCollection**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itriggercollection)
-   [<span data-ttu-id="5aede-133">**итригжер**</span><span class="sxs-lookup"><span data-stu-id="5aede-133">**ITrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itrigger)
-   [<span data-ttu-id="5aede-134">**ибуттригжер**</span><span class="sxs-lookup"><span data-stu-id="5aede-134">**IBootTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger)
-   [<span data-ttu-id="5aede-135">**идаилитригжер**</span><span class="sxs-lookup"><span data-stu-id="5aede-135">**IDailyTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger)
-   [<span data-ttu-id="5aede-136">**иевенттригжер**</span><span class="sxs-lookup"><span data-stu-id="5aede-136">**IEventTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger)
-   [<span data-ttu-id="5aede-137">**иидлетригжер**</span><span class="sxs-lookup"><span data-stu-id="5aede-137">**IIdleTrigger**</span></span>](/windows/win32/api/taskschd/nn-taskschd-iidletrigger)
-   [<span data-ttu-id="5aede-138">**илогонтригжер**</span><span class="sxs-lookup"><span data-stu-id="5aede-138">**ILogonTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger)
-   [<span data-ttu-id="5aede-139">**имонслидовтригжер**</span><span class="sxs-lookup"><span data-stu-id="5aede-139">**IMonthlyDOWTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger)
-   [<span data-ttu-id="5aede-140">**имонслитригжер**</span><span class="sxs-lookup"><span data-stu-id="5aede-140">**IMonthlyTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger)
-   [<span data-ttu-id="5aede-141">**ирегистратионтригжер**</span><span class="sxs-lookup"><span data-stu-id="5aede-141">**IRegistrationTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger)
-   [<span data-ttu-id="5aede-142">**итиметригжер**</span><span class="sxs-lookup"><span data-stu-id="5aede-142">**ITimeTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger)
-   [<span data-ttu-id="5aede-143">**ивиклитригжер**</span><span class="sxs-lookup"><span data-stu-id="5aede-143">**IWeeklyTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger)

## <a name="task-scheduler-10-trigger-interfaces"></a><span data-ttu-id="5aede-144">Интерфейсы триггеров планировщик задач 1,0</span><span class="sxs-lookup"><span data-stu-id="5aede-144">Task Scheduler 1.0 Trigger Interfaces</span></span>

<span data-ttu-id="5aede-145">Существующие приложения, разработанные с помощью планировщик задач 1,0, могут использовать методы, доступные в интерфейсах планировщик задач 1,0 для создания, извлечения, изменения и удаления триггеров для [*рабочего элемента*](w.md).</span><span class="sxs-lookup"><span data-stu-id="5aede-145">Existing applications that are developed using Task Scheduler 1.0 can use the methods that are available from the Task Scheduler 1.0 interfaces to create, retrieve, modify, and delete the triggers for a [*work item*](w.md).</span></span> <span data-ttu-id="5aede-146">Однако обратите внимание, что все интерфейсы планировщик задач 1,0, перечисления и структуры устарели и не должны использоваться для разработки новых приложений.</span><span class="sxs-lookup"><span data-stu-id="5aede-146">However, note that all Task Scheduler 1.0 interfaces, enumerations, and structures are obsolete and should not be used for the development of new applications.</span></span>

<span data-ttu-id="5aede-147">На следующем рисунке показаны два интерфейса, которые используются для этого.</span><span class="sxs-lookup"><span data-stu-id="5aede-147">The two interfaces that are used to do this are shown in the following illustration.</span></span> <span data-ttu-id="5aede-148">Интерфейс [**исчедуледворкитем**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) используется для управления всеми триггерами, связанными с рабочим элементом (такое управление включает создание нового триггера для рабочего элемента).</span><span class="sxs-lookup"><span data-stu-id="5aede-148">The [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface is used to manage all the triggers that are associated with a work item (such management includes creating a new trigger for the work item).</span></span> <span data-ttu-id="5aede-149">Интерфейс [**итасктригжер**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) используется для управления конкретным триггером.</span><span class="sxs-lookup"><span data-stu-id="5aede-149">The [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) interface is used to manage a specific trigger.</span></span>

![интерфейсы триггера планировщика заданий 1,0](images/tsktri2.png)

<span data-ttu-id="5aede-151">Интерфейс [**исчедуледворкитем**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) предоставляет методы для создания нового триггера для рабочего элемента, получения числа триггеров, связанных с рабочим элементом, получения [*структур триггеров*](t.md) , связанных с рабочим элементом, получения [*строк триггера*](t.md) , связанных с рабочим элементом, и для удаления триггеров.</span><span class="sxs-lookup"><span data-stu-id="5aede-151">The [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) interface provides methods for creating a new trigger for a work item, retrieving the number of triggers that are associated with a work item, retrieving the [*trigger structures*](t.md) that are associated with the work item, retrieving [*trigger strings*](t.md) that are associated with the work item, and for deleting triggers.</span></span>

<span data-ttu-id="5aede-152">После того как объект триггера будет доступен, можно использовать интерфейс [**итасктригжер**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) для получения структуры триггера и строки триггера, а также для установки критериев срабатывания триггера.</span><span class="sxs-lookup"><span data-stu-id="5aede-152">Once the trigger object is available, you can use the [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) interface to retrieve the trigger structure and the string of the trigger and to set the criteria that is used to fire the trigger.</span></span> <span data-ttu-id="5aede-153">Этот интерфейс используется только при работе с [*объектом триггера задачи*](t.md).</span><span class="sxs-lookup"><span data-stu-id="5aede-153">This interface is used only when you are working with a [*task trigger object*](t.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5aede-154">См. также</span><span class="sxs-lookup"><span data-stu-id="5aede-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5aede-155">Триггеры задач</span><span class="sxs-lookup"><span data-stu-id="5aede-155">Task Triggers</span></span>](task-triggers.md)
</dt> <dt>

[<span data-ttu-id="5aede-156">Типы триггеров</span><span class="sxs-lookup"><span data-stu-id="5aede-156">Trigger Types</span></span>](trigger-types.md)
</dt> <dt>

[<span data-ttu-id="5aede-157">Структуры триггеров</span><span class="sxs-lookup"><span data-stu-id="5aede-157">Trigger Structures</span></span>](trigger-structures.md)
</dt> </dl>

 

 