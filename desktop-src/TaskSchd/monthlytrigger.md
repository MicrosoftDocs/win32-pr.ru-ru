---
title: Объект Монслитригжер
description: Объект скрипта, представляющий триггер, который запускает задачу на основе ежемесячного расписания.
ms.assetid: d73715cb-a52e-4daf-930f-e94fbe28881e
keywords:
- месячный триггер планировщик задач, объект
- планировщик задач объекта Монслитригжер
- Планировщик задач объекта Монслитригжер, описание
topic_type:
- apiref
api_name:
- MonthlyTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce433f626fbe45e209f881c00787495cc6343bc1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802561"
---
# <a name="monthlytrigger-object"></a><span data-ttu-id="41b29-106">Объект Монслитригжер</span><span class="sxs-lookup"><span data-stu-id="41b29-106">MonthlyTrigger object</span></span>

<span data-ttu-id="41b29-107">Объект скрипта, представляющий триггер, который запускает задачу на основе ежемесячного расписания.</span><span class="sxs-lookup"><span data-stu-id="41b29-107">Scripting object that represents a trigger that starts a task based on a monthly schedule.</span></span> <span data-ttu-id="41b29-108">Например, задача запускается в определенные дни конкретного месяца.</span><span class="sxs-lookup"><span data-stu-id="41b29-108">For example, the task starts on specific days of specific months.</span></span>

## <a name="members"></a><span data-ttu-id="41b29-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="41b29-109">Members</span></span>

<span data-ttu-id="41b29-110">Объект **монслитригжер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="41b29-110">The **MonthlyTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="41b29-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="41b29-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="41b29-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="41b29-112">Properties</span></span>

<span data-ttu-id="41b29-113">Объект **монслитригжер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="41b29-113">The **MonthlyTrigger** object has these properties.</span></span>



| <span data-ttu-id="41b29-114">Свойство</span><span class="sxs-lookup"><span data-stu-id="41b29-114">Property</span></span>                                                                     | <span data-ttu-id="41b29-115">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="41b29-115">Access type</span></span>           | <span data-ttu-id="41b29-116">Описание</span><span class="sxs-lookup"><span data-stu-id="41b29-116">Description</span></span>                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="41b29-117">**DaysOfMonth**</span><span class="sxs-lookup"><span data-stu-id="41b29-117">**DaysOfMonth**</span></span>](monthlytrigger-daysofmonth.md)<br/>                 | <span data-ttu-id="41b29-118">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="41b29-118">Read/write</span></span><br/> | <span data-ttu-id="41b29-119">Возвращает или задает дни месяца, в которые выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="41b29-119">Gets or sets the days of the month during which the task runs.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="41b29-120">**Активировано**</span><span class="sxs-lookup"><span data-stu-id="41b29-120">**Enabled**</span></span>](trigger-enabled.md)<br/>                                | <span data-ttu-id="41b29-121">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="41b29-121">Read/write</span></span><br/> | <span data-ttu-id="41b29-122">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="41b29-122">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="41b29-123">Возвращает или задает логическое значение, указывающее, включен ли триггер.</span><span class="sxs-lookup"><span data-stu-id="41b29-123">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="41b29-124">ендбаундари</span><span class="sxs-lookup"><span data-stu-id="41b29-124">EndBoundary</span></span>](trigger-endboundary.md)<br/>                            | <span data-ttu-id="41b29-125">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="41b29-125">Read/write</span></span><br/> | <span data-ttu-id="41b29-126">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="41b29-126">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="41b29-127">Возвращает или задает дату и время деактивации триггера.</span><span class="sxs-lookup"><span data-stu-id="41b29-127">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="41b29-128">Триггер не может запустить задачу после ее деактивации.</span><span class="sxs-lookup"><span data-stu-id="41b29-128">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="41b29-129">**ексекутионтимелимит**</span><span class="sxs-lookup"><span data-stu-id="41b29-129">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/>          | <span data-ttu-id="41b29-130">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="41b29-130">Read/write</span></span><br/> | <span data-ttu-id="41b29-131">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="41b29-131">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="41b29-132">Возвращает или задает максимальное время, в течение которого разрешено выполнение задачи, запущенной триггером.</span><span class="sxs-lookup"><span data-stu-id="41b29-132">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                           |
| [<span data-ttu-id="41b29-133">**Удостоверения**</span><span class="sxs-lookup"><span data-stu-id="41b29-133">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                         | <span data-ttu-id="41b29-134">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="41b29-134">Read/write</span></span><br/> | <span data-ttu-id="41b29-135">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="41b29-135">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="41b29-136">Возвращает или задает идентификатор триггера.</span><span class="sxs-lookup"><span data-stu-id="41b29-136">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="41b29-137">**монссофеар**</span><span class="sxs-lookup"><span data-stu-id="41b29-137">**MonthsOfYear**</span></span>](monthlytrigger-monthsofyear.md)<br/>               | <span data-ttu-id="41b29-138">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="41b29-138">Read/write</span></span><br/> | <span data-ttu-id="41b29-139">Возвращает или задает месяцы года, в течение которых выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="41b29-139">Gets or sets the months of the year during which the task runs.</span></span><br/>                                                                                                                  |
| [<span data-ttu-id="41b29-140">**рандомделай**</span><span class="sxs-lookup"><span data-stu-id="41b29-140">**RandomDelay**</span></span>](monthlytrigger-randomdelay.md)<br/>                 | <span data-ttu-id="41b29-141">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="41b29-141">Read/write</span></span><br/> | <span data-ttu-id="41b29-142">Возвращает или задает время задержки, которое добавляется случайным образом к времени начала триггера.</span><span class="sxs-lookup"><span data-stu-id="41b29-142">Gets or sets a delay time that is randomly added to the start time of the trigger.</span></span><br/>                                                                                               |
| [<span data-ttu-id="41b29-143">**Повторение**</span><span class="sxs-lookup"><span data-stu-id="41b29-143">**Repetition**</span></span>](trigger-repetition.md)<br/>                          | <span data-ttu-id="41b29-144">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="41b29-144">Read/write</span></span><br/> | <span data-ttu-id="41b29-145">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="41b29-145">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="41b29-146">Возвращает или задает частоту выполнения задачи и период повторения шаблона повторения после запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="41b29-146">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="41b29-147">**рунонластдайофмонс**</span><span class="sxs-lookup"><span data-stu-id="41b29-147">**RunOnLastDayOfMonth**</span></span>](monthlytrigger-runonlastdayofmonth.md)<br/> | <span data-ttu-id="41b29-148">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="41b29-148">Read/write</span></span><br/> | <span data-ttu-id="41b29-149">Возвращает или задает логическое значение, указывающее, что задача выполняется в последний день месяца.</span><span class="sxs-lookup"><span data-stu-id="41b29-149">Gets or sets a Boolean value that indicates that the task runs on the last day of the month.</span></span><br/>                                                                                     |
| [<span data-ttu-id="41b29-150">**стартбаундари**</span><span class="sxs-lookup"><span data-stu-id="41b29-150">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>                    | <span data-ttu-id="41b29-151">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="41b29-151">Read/write</span></span><br/> | <span data-ttu-id="41b29-152">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="41b29-152">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="41b29-153">Возвращает или задает дату и время активации триггера.</span><span class="sxs-lookup"><span data-stu-id="41b29-153">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="41b29-154">**Тип**</span><span class="sxs-lookup"><span data-stu-id="41b29-154">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                                     | <span data-ttu-id="41b29-155">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="41b29-155">Read-only</span></span><br/>  | <span data-ttu-id="41b29-156">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="41b29-156">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="41b29-157">Возвращает тип триггера.</span><span class="sxs-lookup"><span data-stu-id="41b29-157">Gets the type of the trigger.</span></span><br/>                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="41b29-158">Комментарии</span><span class="sxs-lookup"><span data-stu-id="41b29-158">Remarks</span></span>

<span data-ttu-id="41b29-159">Время дня запуска задачи задается свойством [**стартбаундари**](trigger-startboundary.md) .</span><span class="sxs-lookup"><span data-stu-id="41b29-159">The time of day that the task is started is set by the [**StartBoundary**](trigger-startboundary.md) property.</span></span>

<span data-ttu-id="41b29-160">При чтении или записи собственного XML-кода для задачи ежемесячный триггер указывается с помощью элемента [**счедулебимонс**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="41b29-160">When reading or writing your own XML for a task, a monthly trigger is specified using the [**ScheduleByMonth**](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="41b29-161">Требования</span><span class="sxs-lookup"><span data-stu-id="41b29-161">Requirements</span></span>



| <span data-ttu-id="41b29-162">Требование</span><span class="sxs-lookup"><span data-stu-id="41b29-162">Requirement</span></span> | <span data-ttu-id="41b29-163">Значение</span><span class="sxs-lookup"><span data-stu-id="41b29-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41b29-164">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="41b29-164">Minimum supported client</span></span><br/> | <span data-ttu-id="41b29-165">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="41b29-165">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="41b29-166">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="41b29-166">Minimum supported server</span></span><br/> | <span data-ttu-id="41b29-167">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="41b29-167">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="41b29-168">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="41b29-168">Type library</span></span><br/>             | <dl> <span data-ttu-id="41b29-169"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="41b29-169"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="41b29-170">DLL</span><span class="sxs-lookup"><span data-stu-id="41b29-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41b29-171"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41b29-171"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41b29-172">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="41b29-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41b29-173">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="41b29-173">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="41b29-174">планировщик задач объекты</span><span class="sxs-lookup"><span data-stu-id="41b29-174">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="41b29-175">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="41b29-175">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="41b29-176">**тригжерколлектион**</span><span class="sxs-lookup"><span data-stu-id="41b29-176">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="41b29-177">**Тригжерколлектион. Create**</span><span class="sxs-lookup"><span data-stu-id="41b29-177">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





