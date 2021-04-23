---
title: Объект Монслидовтригжер
description: Объект скрипта, представляющий триггер, который запускает задачу в расписании ежемесячного дня недели.
ms.assetid: 18607189-295f-4f7d-bf72-f0ac8d5067cf
keywords:
- месячный планировщик задач триггера DOW, объект
- планировщик задач объекта Монслидовтригжер
- Планировщик задач объекта Монслидовтригжер, описание
topic_type:
- apiref
api_name:
- MonthlyDOWTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b7e43925c6ebe27933a39fe5e25f37ffe6cf72e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071414"
---
# <a name="monthlydowtrigger-object"></a><span data-ttu-id="e8b4d-106">Объект Монслидовтригжер</span><span class="sxs-lookup"><span data-stu-id="e8b4d-106">MonthlyDOWTrigger object</span></span>

<span data-ttu-id="e8b4d-107">Объект скрипта, представляющий триггер, который запускает задачу в расписании ежемесячного дня недели.</span><span class="sxs-lookup"><span data-stu-id="e8b4d-107">Scripting object that represents a trigger that starts a task on a monthly day-of-week schedule.</span></span> <span data-ttu-id="e8b4d-108">Например, задача начинается каждый первый четверг, с мая по октября.</span><span class="sxs-lookup"><span data-stu-id="e8b4d-108">For example, the task starts on every first Thursday, May through October.</span></span>

## <a name="members"></a><span data-ttu-id="e8b4d-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="e8b4d-109">Members</span></span>

<span data-ttu-id="e8b4d-110">Объект **монслидовтригжер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e8b4d-110">The **MonthlyDOWTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="e8b4d-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="e8b4d-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e8b4d-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="e8b4d-112">Properties</span></span>

<span data-ttu-id="e8b4d-113">Объект **монслидовтригжер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e8b4d-113">The **MonthlyDOWTrigger** object has these properties.</span></span>



| <span data-ttu-id="e8b4d-114">Свойство</span><span class="sxs-lookup"><span data-stu-id="e8b4d-114">Property</span></span>                                                                          | <span data-ttu-id="e8b4d-115">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="e8b4d-115">Access type</span></span>           | <span data-ttu-id="e8b4d-116">Описание</span><span class="sxs-lookup"><span data-stu-id="e8b4d-116">Description</span></span>                                                                                                                                                                                 |
|:----------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e8b4d-117">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="e8b4d-117">**DaysOfWeek**</span></span>](monthlydowtrigger-daysofweek.md)<br/>                     | <span data-ttu-id="e8b4d-118">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="e8b4d-118">Read/write</span></span><br/> | <span data-ttu-id="e8b4d-119">Возвращает или задает дни недели, в которые выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="e8b4d-119">Gets or sets the days of the week during which the task runs.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="e8b4d-120">**Активировано**</span><span class="sxs-lookup"><span data-stu-id="e8b4d-120">**Enabled**</span></span>](trigger-enabled.md)<br/>                                     | <span data-ttu-id="e8b4d-121">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="e8b4d-121">Read/write</span></span><br/> | <span data-ttu-id="e8b4d-122">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="e8b4d-122">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="e8b4d-123">Возвращает или задает логическое значение, указывающее, включен ли триггер.</span><span class="sxs-lookup"><span data-stu-id="e8b4d-123">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="e8b4d-124">ендбаундари</span><span class="sxs-lookup"><span data-stu-id="e8b4d-124">EndBoundary</span></span>](trigger-endboundary.md)<br/>                                 | <span data-ttu-id="e8b4d-125">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="e8b4d-125">Read/write</span></span><br/> | <span data-ttu-id="e8b4d-126">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="e8b4d-126">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="e8b4d-127">Возвращает или задает дату и время деактивации триггера.</span><span class="sxs-lookup"><span data-stu-id="e8b4d-127">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="e8b4d-128">Триггер не может запустить задачу после ее деактивации.</span><span class="sxs-lookup"><span data-stu-id="e8b4d-128">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="e8b4d-129">**ексекутионтимелимит**</span><span class="sxs-lookup"><span data-stu-id="e8b4d-129">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/>               | <span data-ttu-id="e8b4d-130">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="e8b4d-130">Read/write</span></span><br/> | <span data-ttu-id="e8b4d-131">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="e8b4d-131">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="e8b4d-132">Возвращает или задает максимальное время, в течение которого разрешено выполнение задачи, запущенной этим триггером.</span><span class="sxs-lookup"><span data-stu-id="e8b4d-132">Gets or sets the maximum amount of time that the task launched by this trigger is allowed to run.</span></span><br/>                          |
| [<span data-ttu-id="e8b4d-133">**Удостоверения**</span><span class="sxs-lookup"><span data-stu-id="e8b4d-133">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                              | <span data-ttu-id="e8b4d-134">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="e8b4d-134">Read/write</span></span><br/> | <span data-ttu-id="e8b4d-135">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="e8b4d-135">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="e8b4d-136">Возвращает или задает идентификатор триггера.</span><span class="sxs-lookup"><span data-stu-id="e8b4d-136">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="e8b4d-137">**монссофеар**</span><span class="sxs-lookup"><span data-stu-id="e8b4d-137">**MonthsOfYear**</span></span>](monthlydowtrigger-monthsofyear.md)<br/>                 | <span data-ttu-id="e8b4d-138">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="e8b4d-138">Read/write</span></span><br/> | <span data-ttu-id="e8b4d-139">Возвращает или задает месяцы года, в течение которых выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="e8b4d-139">Gets or sets the months of the year during which the task runs.</span></span><br/>                                                                                                                  |
| [<span data-ttu-id="e8b4d-140">**рандомделай**</span><span class="sxs-lookup"><span data-stu-id="e8b4d-140">**RandomDelay**</span></span>](monthlydowtrigger-randomdelay.md)<br/>                   | <span data-ttu-id="e8b4d-141">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="e8b4d-141">Read/write</span></span><br/> | <span data-ttu-id="e8b4d-142">Возвращает или задает время задержки, которое добавляется случайным образом к времени начала триггера.</span><span class="sxs-lookup"><span data-stu-id="e8b4d-142">Gets or sets a delay time that is randomly added to the start time of the trigger.</span></span><br/>                                                                                               |
| [<span data-ttu-id="e8b4d-143">**Повторение**</span><span class="sxs-lookup"><span data-stu-id="e8b4d-143">**Repetition**</span></span>](trigger-repetition.md)<br/>                               | <span data-ttu-id="e8b4d-144">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="e8b4d-144">Read/write</span></span><br/> | <span data-ttu-id="e8b4d-145">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="e8b4d-145">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="e8b4d-146">Возвращает или задает частоту выполнения задачи и период повторения шаблона повторения после запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="e8b4d-146">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="e8b4d-147">**рунонластвикофмонс**</span><span class="sxs-lookup"><span data-stu-id="e8b4d-147">**RunOnLastWeekOfMonth**</span></span>](monthlydowtrigger-runonlastweekofmonth.md)<br/> | <span data-ttu-id="e8b4d-148">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="e8b4d-148">Read/write</span></span><br/> | <span data-ttu-id="e8b4d-149">Возвращает или задает логическое значение, указывающее, что задача выполняется в последнюю неделю месяца.</span><span class="sxs-lookup"><span data-stu-id="e8b4d-149">Gets or sets a Boolean value that indicates that the task runs on the last week of the month.</span></span><br/>                                                                                    |
| [<span data-ttu-id="e8b4d-150">**стартбаундари**</span><span class="sxs-lookup"><span data-stu-id="e8b4d-150">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>                         | <span data-ttu-id="e8b4d-151">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="e8b4d-151">Read/write</span></span><br/> | <span data-ttu-id="e8b4d-152">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="e8b4d-152">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="e8b4d-153">Возвращает или задает дату и время активации триггера.</span><span class="sxs-lookup"><span data-stu-id="e8b4d-153">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="e8b4d-154">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e8b4d-154">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                                          | <span data-ttu-id="e8b4d-155">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="e8b4d-155">Read-only</span></span><br/>  | <span data-ttu-id="e8b4d-156">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="e8b4d-156">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="e8b4d-157">Возвращает тип триггера.</span><span class="sxs-lookup"><span data-stu-id="e8b4d-157">Gets the type of the trigger.</span></span><br/>                                                                                              |
| [<span data-ttu-id="e8b4d-158">**виксофмонс**</span><span class="sxs-lookup"><span data-stu-id="e8b4d-158">**WeeksOfMonth**</span></span>](monthlydowtrigger-weeksofmonth.md)<br/>                 | <span data-ttu-id="e8b4d-159">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="e8b4d-159">Read/write</span></span><br/> | <span data-ttu-id="e8b4d-160">Возвращает или задает недели месяца, в течение которых выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="e8b4d-160">Gets or sets the weeks of the month during which the task runs.</span></span><br/>                                                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="e8b4d-161">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e8b4d-161">Remarks</span></span>

<span data-ttu-id="e8b4d-162">Время дня запуска задачи задается свойством [**стартбаундари**](trigger-startboundary.md) .</span><span class="sxs-lookup"><span data-stu-id="e8b4d-162">The time of day that the task is started is set by the [**StartBoundary**](trigger-startboundary.md) property.</span></span>

<span data-ttu-id="e8b4d-163">При чтении или записи XML для задачи триггер месячного дня недели указывается с помощью элемента [**счедулебимонсдайофвик**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="e8b4d-163">When reading or writing XML for a task, a monthly day-of-week trigger is specified using the [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8b4d-164">Требования</span><span class="sxs-lookup"><span data-stu-id="e8b4d-164">Requirements</span></span>



| <span data-ttu-id="e8b4d-165">Требование</span><span class="sxs-lookup"><span data-stu-id="e8b4d-165">Requirement</span></span> | <span data-ttu-id="e8b4d-166">Значение</span><span class="sxs-lookup"><span data-stu-id="e8b4d-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8b4d-167">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e8b4d-167">Minimum supported client</span></span><br/> | <span data-ttu-id="e8b4d-168">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e8b4d-168">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e8b4d-169">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e8b4d-169">Minimum supported server</span></span><br/> | <span data-ttu-id="e8b4d-170">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e8b4d-170">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e8b4d-171">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="e8b4d-171">Type library</span></span><br/>             | <dl> <span data-ttu-id="e8b4d-172"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e8b4d-172"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e8b4d-173">DLL</span><span class="sxs-lookup"><span data-stu-id="e8b4d-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8b4d-174"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8b4d-174"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8b4d-175">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e8b4d-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8b4d-176">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="e8b4d-176">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="e8b4d-177">планировщик задач объекты</span><span class="sxs-lookup"><span data-stu-id="e8b4d-177">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="e8b4d-178">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="e8b4d-178">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="e8b4d-179">**тригжерколлектион**</span><span class="sxs-lookup"><span data-stu-id="e8b4d-179">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="e8b4d-180">**Тригжерколлектион. Create**</span><span class="sxs-lookup"><span data-stu-id="e8b4d-180">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





