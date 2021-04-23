---
title: Объект Даилитригжер
description: Объект скрипта, представляющий триггер, который запускает задачу на основе ежедневного расписания.
ms.assetid: f03f53a0-0060-4793-96c1-b47a96852579
keywords:
- планировщик задач ежедневного триггера, объект
- планировщик задач объекта Даилитригжер
- Планировщик задач объекта Даилитригжер, описание
topic_type:
- apiref
api_name:
- DailyTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22203ecf7a421f07ccb823745e6619e05f84f550
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489873"
---
# <a name="dailytrigger-object"></a><span data-ttu-id="29ef5-106">Объект Даилитригжер</span><span class="sxs-lookup"><span data-stu-id="29ef5-106">DailyTrigger object</span></span>

<span data-ttu-id="29ef5-107">Объект скрипта, представляющий триггер, который запускает задачу на основе ежедневного расписания.</span><span class="sxs-lookup"><span data-stu-id="29ef5-107">Scripting object that represents a trigger that starts a task based on a daily schedule.</span></span>

## <a name="members"></a><span data-ttu-id="29ef5-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="29ef5-108">Members</span></span>

<span data-ttu-id="29ef5-109">Объект **даилитригжер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="29ef5-109">The **DailyTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="29ef5-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="29ef5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="29ef5-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="29ef5-111">Properties</span></span>

<span data-ttu-id="29ef5-112">Объект **даилитригжер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="29ef5-112">The **DailyTrigger** object has these properties.</span></span>



| <span data-ttu-id="29ef5-113">Свойство</span><span class="sxs-lookup"><span data-stu-id="29ef5-113">Property</span></span>                                                            | <span data-ttu-id="29ef5-114">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="29ef5-114">Access type</span></span>           | <span data-ttu-id="29ef5-115">Описание</span><span class="sxs-lookup"><span data-stu-id="29ef5-115">Description</span></span>                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="29ef5-116">**дайсинтервал**</span><span class="sxs-lookup"><span data-stu-id="29ef5-116">**DaysInterval**</span></span>](dailytrigger-daysinterval.md)<br/>        | <span data-ttu-id="29ef5-117">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="29ef5-117">Read/write</span></span><br/> | <span data-ttu-id="29ef5-118">Возвращает или задает интервал между днями в расписании.</span><span class="sxs-lookup"><span data-stu-id="29ef5-118">Gets or sets the interval between the days in the schedule.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="29ef5-119">**Активировано**</span><span class="sxs-lookup"><span data-stu-id="29ef5-119">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="29ef5-120">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="29ef5-120">Read/write</span></span><br/> | <span data-ttu-id="29ef5-121">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="29ef5-121">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="29ef5-122">Возвращает или задает логическое значение, указывающее, включен ли триггер.</span><span class="sxs-lookup"><span data-stu-id="29ef5-122">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="29ef5-123">**ендбаундари**</span><span class="sxs-lookup"><span data-stu-id="29ef5-123">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="29ef5-124">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="29ef5-124">Read/write</span></span><br/> | <span data-ttu-id="29ef5-125">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="29ef5-125">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="29ef5-126">Возвращает или задает дату и время деактивации триггера.</span><span class="sxs-lookup"><span data-stu-id="29ef5-126">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="29ef5-127">Триггер не может запустить задачу после ее деактивации.</span><span class="sxs-lookup"><span data-stu-id="29ef5-127">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="29ef5-128">**ексекутионтимелимит**</span><span class="sxs-lookup"><span data-stu-id="29ef5-128">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="29ef5-129">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="29ef5-129">Read/write</span></span><br/> | <span data-ttu-id="29ef5-130">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="29ef5-130">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="29ef5-131">Возвращает или задает максимальное время, в течение которого разрешено выполнение задачи, запущенной триггером.</span><span class="sxs-lookup"><span data-stu-id="29ef5-131">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                           |
| [<span data-ttu-id="29ef5-132">**Удостоверения**</span><span class="sxs-lookup"><span data-stu-id="29ef5-132">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="29ef5-133">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="29ef5-133">Read/write</span></span><br/> | <span data-ttu-id="29ef5-134">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="29ef5-134">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="29ef5-135">Возвращает или задает идентификатор триггера.</span><span class="sxs-lookup"><span data-stu-id="29ef5-135">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="29ef5-136">**рандомделай**</span><span class="sxs-lookup"><span data-stu-id="29ef5-136">**RandomDelay**</span></span>](dailytrigger-randomdelay.md)<br/>          | <span data-ttu-id="29ef5-137">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="29ef5-137">Read/write</span></span><br/> | <span data-ttu-id="29ef5-138">Возвращает или задает время задержки, которое добавляется случайным образом к времени начала триггера.</span><span class="sxs-lookup"><span data-stu-id="29ef5-138">Gets or sets a delay time that is randomly added to the start time of the trigger.</span></span><br/>                                                                                               |
| [<span data-ttu-id="29ef5-139">**Повторение**</span><span class="sxs-lookup"><span data-stu-id="29ef5-139">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="29ef5-140">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="29ef5-140">Read/write</span></span><br/> | <span data-ttu-id="29ef5-141">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="29ef5-141">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="29ef5-142">Возвращает или задает частоту выполнения задачи и период повторения шаблона повторения после запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="29ef5-142">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="29ef5-143">**стартбаундари**</span><span class="sxs-lookup"><span data-stu-id="29ef5-143">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="29ef5-144">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="29ef5-144">Read/write</span></span><br/> | <span data-ttu-id="29ef5-145">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="29ef5-145">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="29ef5-146">Возвращает или задает дату и время активации триггера.</span><span class="sxs-lookup"><span data-stu-id="29ef5-146">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="29ef5-147">**Тип**</span><span class="sxs-lookup"><span data-stu-id="29ef5-147">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="29ef5-148">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="29ef5-148">Read-only</span></span><br/>  | <span data-ttu-id="29ef5-149">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="29ef5-149">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="29ef5-150">Возвращает тип триггера.</span><span class="sxs-lookup"><span data-stu-id="29ef5-150">Gets the type of the trigger.</span></span><br/>                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="29ef5-151">Комментарии</span><span class="sxs-lookup"><span data-stu-id="29ef5-151">Remarks</span></span>

<span data-ttu-id="29ef5-152">Время дня запуска задачи задается свойством [**стартбаундари**](trigger-startboundary.md) .</span><span class="sxs-lookup"><span data-stu-id="29ef5-152">The time of day that the task is started is set by the [**StartBoundary**](trigger-startboundary.md) property.</span></span>

<span data-ttu-id="29ef5-153">Интервал 1 создает ежедневное расписание.</span><span class="sxs-lookup"><span data-stu-id="29ef5-153">An interval of 1 produces a daily schedule.</span></span> <span data-ttu-id="29ef5-154">Интервал 2 создает все остальные календарные расписания и т. д.</span><span class="sxs-lookup"><span data-stu-id="29ef5-154">An interval of 2 produces an every other day schedule and so on.</span></span>

<span data-ttu-id="29ef5-155">При чтении или записи собственного XML-кода для задачи ежедневный триггер указывается с помощью элемента [**счедулебидай**](taskschedulerschema-schedulebyday-calendartriggertype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="29ef5-155">When reading or writing your own XML for a task, a daily trigger is specified using the [**ScheduleByDay**](taskschedulerschema-schedulebyday-calendartriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="29ef5-156">Примеры</span><span class="sxs-lookup"><span data-stu-id="29ef5-156">Examples</span></span>

<span data-ttu-id="29ef5-157">Дополнительные сведения и пример кода для этого объекта скрипта см. в разделе [Пример ежедневного триггера (сценарии)](daily-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="29ef5-157">For more information and a code example for this scripting object, see [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="29ef5-158">Требования</span><span class="sxs-lookup"><span data-stu-id="29ef5-158">Requirements</span></span>



| <span data-ttu-id="29ef5-159">Требование</span><span class="sxs-lookup"><span data-stu-id="29ef5-159">Requirement</span></span> | <span data-ttu-id="29ef5-160">Значение</span><span class="sxs-lookup"><span data-stu-id="29ef5-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="29ef5-161">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="29ef5-161">Minimum supported client</span></span><br/> | <span data-ttu-id="29ef5-162">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="29ef5-162">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="29ef5-163">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="29ef5-163">Minimum supported server</span></span><br/> | <span data-ttu-id="29ef5-164">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="29ef5-164">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="29ef5-165">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="29ef5-165">Type library</span></span><br/>             | <dl> <span data-ttu-id="29ef5-166"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="29ef5-166"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="29ef5-167">DLL</span><span class="sxs-lookup"><span data-stu-id="29ef5-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29ef5-168"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29ef5-168"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29ef5-169">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="29ef5-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29ef5-170">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="29ef5-170">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="29ef5-171">**тригжерколлектион**</span><span class="sxs-lookup"><span data-stu-id="29ef5-171">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="29ef5-172">**Тригжерколлектион. Create**</span><span class="sxs-lookup"><span data-stu-id="29ef5-172">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





