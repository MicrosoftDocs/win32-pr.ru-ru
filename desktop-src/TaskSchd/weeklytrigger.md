---
title: Объект Виклитригжер
description: Объект скрипта, представляющий триггер, который запускает задачу на основе еженедельного расписания.
ms.assetid: a000d7a8-0239-440f-b49b-7f0c55b01e8e
keywords:
- Еженедельный триггер планировщик задач, объект
- планировщик задач объекта Виклитригжер
- Планировщик задач объекта Виклитригжер, описание
topic_type:
- apiref
api_name:
- WeeklyTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58dec9172d38b53f779f44a048b39bc709dbd54f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804037"
---
# <a name="weeklytrigger-object"></a><span data-ttu-id="93f07-106">Объект Виклитригжер</span><span class="sxs-lookup"><span data-stu-id="93f07-106">WeeklyTrigger object</span></span>

<span data-ttu-id="93f07-107">Объект скрипта, представляющий триггер, который запускает задачу на основе еженедельного расписания.</span><span class="sxs-lookup"><span data-stu-id="93f07-107">Scripting object that represents a trigger that starts a task based on a weekly schedule.</span></span> <span data-ttu-id="93f07-108">Например, задача начинается в 8:00 утра.</span><span class="sxs-lookup"><span data-stu-id="93f07-108">For example, the task starts at 8:00 A.M.</span></span> <span data-ttu-id="93f07-109">в конкретный день недели каждую неделю или каждую неделю.</span><span class="sxs-lookup"><span data-stu-id="93f07-109">on a specific day of the week every week or every other week.</span></span>

## <a name="members"></a><span data-ttu-id="93f07-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="93f07-110">Members</span></span>

<span data-ttu-id="93f07-111">Объект **виклитригжер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="93f07-111">The **WeeklyTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="93f07-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="93f07-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="93f07-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="93f07-113">Properties</span></span>

<span data-ttu-id="93f07-114">Объект **виклитригжер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="93f07-114">The **WeeklyTrigger** object has these properties.</span></span>



| <span data-ttu-id="93f07-115">Свойство</span><span class="sxs-lookup"><span data-stu-id="93f07-115">Property</span></span>                                                            | <span data-ttu-id="93f07-116">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="93f07-116">Access type</span></span>           | <span data-ttu-id="93f07-117">Описание</span><span class="sxs-lookup"><span data-stu-id="93f07-117">Description</span></span>                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="93f07-118">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="93f07-118">**DaysOfWeek**</span></span>](weeklytrigger-daysofweek.md)<br/>           | <span data-ttu-id="93f07-119">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="93f07-119">Read/write</span></span><br/> | <span data-ttu-id="93f07-120">Возвращает или задает дни недели, в которые выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="93f07-120">Gets or sets the days of the week on which the task runs.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="93f07-121">**Активировано**</span><span class="sxs-lookup"><span data-stu-id="93f07-121">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="93f07-122">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="93f07-122">Read/write</span></span><br/> | <span data-ttu-id="93f07-123">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="93f07-123">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="93f07-124">Возвращает или задает логическое значение, указывающее, включен ли триггер.</span><span class="sxs-lookup"><span data-stu-id="93f07-124">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="93f07-125">**ендбаундари**</span><span class="sxs-lookup"><span data-stu-id="93f07-125">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="93f07-126">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="93f07-126">Read/write</span></span><br/> | <span data-ttu-id="93f07-127">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="93f07-127">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="93f07-128">Возвращает или задает дату и время деактивации триггера.</span><span class="sxs-lookup"><span data-stu-id="93f07-128">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="93f07-129">Триггер не может запустить задачу после ее деактивации.</span><span class="sxs-lookup"><span data-stu-id="93f07-129">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="93f07-130">**ексекутионтимелимит**</span><span class="sxs-lookup"><span data-stu-id="93f07-130">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="93f07-131">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="93f07-131">Read/write</span></span><br/> | <span data-ttu-id="93f07-132">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="93f07-132">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="93f07-133">Возвращает или задает максимальное время, в течение которого разрешено выполнение задачи, запущенной триггером.</span><span class="sxs-lookup"><span data-stu-id="93f07-133">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                           |
| [<span data-ttu-id="93f07-134">**Удостоверения**</span><span class="sxs-lookup"><span data-stu-id="93f07-134">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="93f07-135">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="93f07-135">Read/write</span></span><br/> | <span data-ttu-id="93f07-136">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="93f07-136">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="93f07-137">Возвращает или задает идентификатор триггера.</span><span class="sxs-lookup"><span data-stu-id="93f07-137">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="93f07-138">**рандомделай**</span><span class="sxs-lookup"><span data-stu-id="93f07-138">**RandomDelay**</span></span>](weeklytrigger-randomdelay.md)<br/>         | <span data-ttu-id="93f07-139">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="93f07-139">Read/write</span></span><br/> | <span data-ttu-id="93f07-140">Возвращает или задает время задержки, которое добавляется случайным образом к времени начала триггера.</span><span class="sxs-lookup"><span data-stu-id="93f07-140">Gets or sets a delay time that is randomly added to the start time of the trigger.</span></span><br/>                                                                                               |
| [<span data-ttu-id="93f07-141">**Повторение**</span><span class="sxs-lookup"><span data-stu-id="93f07-141">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="93f07-142">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="93f07-142">Read/write</span></span><br/> | <span data-ttu-id="93f07-143">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="93f07-143">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="93f07-144">Возвращает или задает частоту выполнения задачи и период повторения шаблона повторения после запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="93f07-144">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="93f07-145">**стартбаундари**</span><span class="sxs-lookup"><span data-stu-id="93f07-145">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="93f07-146">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="93f07-146">Read/write</span></span><br/> | <span data-ttu-id="93f07-147">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="93f07-147">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="93f07-148">Возвращает или задает дату и время активации триггера.</span><span class="sxs-lookup"><span data-stu-id="93f07-148">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="93f07-149">**Тип**</span><span class="sxs-lookup"><span data-stu-id="93f07-149">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="93f07-150">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="93f07-150">Read-only</span></span><br/>  | <span data-ttu-id="93f07-151">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="93f07-151">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="93f07-152">Возвращает тип триггера.</span><span class="sxs-lookup"><span data-stu-id="93f07-152">Gets the type of the trigger.</span></span><br/>                                                                                              |
| [<span data-ttu-id="93f07-153">**виксинтервал**</span><span class="sxs-lookup"><span data-stu-id="93f07-153">**WeeksInterval**</span></span>](weeklytrigger-weeksinterval.md)<br/>     | <span data-ttu-id="93f07-154">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="93f07-154">Read/write</span></span><br/> | <span data-ttu-id="93f07-155">Возвращает или задает интервал между неделями в расписании.</span><span class="sxs-lookup"><span data-stu-id="93f07-155">Gets or sets the interval between the weeks in the schedule.</span></span><br/>                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="93f07-156">Комментарии</span><span class="sxs-lookup"><span data-stu-id="93f07-156">Remarks</span></span>

<span data-ttu-id="93f07-157">Время дня запуска задачи задается свойством [**стартбаундари**](trigger-startboundary.md) .</span><span class="sxs-lookup"><span data-stu-id="93f07-157">The time of day that the task is started is set by the [**StartBoundary**](trigger-startboundary.md) property.</span></span>

<span data-ttu-id="93f07-158">При чтении или записи собственного XML-кода для задачи еженедельный триггер указывается с помощью элемента [**счедулебивик**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="93f07-158">When reading or writing your own XML for a task, a weekly trigger is specified using the [**ScheduleByWeek**](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="93f07-159">Примеры</span><span class="sxs-lookup"><span data-stu-id="93f07-159">Examples</span></span>

<span data-ttu-id="93f07-160">Дополнительные сведения и пример кода для этого объекта скрипта см. в разделе [Пример еженедельного триггера (сценарии)](weekly-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="93f07-160">For more information and a code example for this scripting object, see [Weekly Trigger Example (Scripting)](weekly-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="93f07-161">Требования</span><span class="sxs-lookup"><span data-stu-id="93f07-161">Requirements</span></span>



| <span data-ttu-id="93f07-162">Требование</span><span class="sxs-lookup"><span data-stu-id="93f07-162">Requirement</span></span> | <span data-ttu-id="93f07-163">Значение</span><span class="sxs-lookup"><span data-stu-id="93f07-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="93f07-164">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="93f07-164">Minimum supported client</span></span><br/> | <span data-ttu-id="93f07-165">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="93f07-165">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="93f07-166">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="93f07-166">Minimum supported server</span></span><br/> | <span data-ttu-id="93f07-167">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="93f07-167">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="93f07-168">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="93f07-168">Type library</span></span><br/>             | <dl> <span data-ttu-id="93f07-169"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="93f07-169"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="93f07-170">DLL</span><span class="sxs-lookup"><span data-stu-id="93f07-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93f07-171"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93f07-171"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93f07-172">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="93f07-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93f07-173">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="93f07-173">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="93f07-174">**тригжерколлектион**</span><span class="sxs-lookup"><span data-stu-id="93f07-174">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="93f07-175">**Тригжерколлектион. Create**</span><span class="sxs-lookup"><span data-stu-id="93f07-175">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





