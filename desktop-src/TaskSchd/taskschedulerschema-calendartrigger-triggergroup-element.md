---
title: Календартригжер (Тригжерграуп), элемент
description: Задает ежедневный, еженедельный, ежемесячный или ежемесячный триггер (DOW) в день недели.
ms.assetid: 9b9218bf-222c-4ece-8b37-5c5d8b765015
keywords:
- планировщик задач триггера календаря, XML-элемент
- планировщик задач элемента Календартригжер
topic_type:
- apiref
api_name:
- CalendarTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 02c061d8821dffa82eca8756ab26acadc6bb9281
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681986"
---
# <a name="calendartrigger-triggergroup-element"></a><span data-ttu-id="eb602-105">Календартригжер (Тригжерграуп), элемент</span><span class="sxs-lookup"><span data-stu-id="eb602-105">CalendarTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="eb602-106">Задает ежедневный, еженедельный, ежемесячный или ежемесячный триггер (DOW) в день недели.</span><span class="sxs-lookup"><span data-stu-id="eb602-106">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span>

``` syntax
<xs:element name="CalendarTrigger"
    type="calendarTriggerType"
 />
```

<span data-ttu-id="eb602-107">Элемент **календартригжер** определяется сложным типом [**календартригжертипе**](taskschedulerschema-calendartriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="eb602-107">The **CalendarTrigger** element is defined by the [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="eb602-108">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="eb602-108">Parent element</span></span>



| <span data-ttu-id="eb602-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="eb602-109">Element</span></span>                                                           | <span data-ttu-id="eb602-110">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="eb602-110">Derived from</span></span>                                                         | <span data-ttu-id="eb602-111">Описание</span><span class="sxs-lookup"><span data-stu-id="eb602-111">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="eb602-112">**Триггеры**</span><span class="sxs-lookup"><span data-stu-id="eb602-112">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="eb602-113">**тригжерстипе**</span><span class="sxs-lookup"><span data-stu-id="eb602-113">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="eb602-114">Задает триггеры, которые запускают задачу.</span><span class="sxs-lookup"><span data-stu-id="eb602-114">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="eb602-115">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="eb602-115">Child elements</span></span>



| <span data-ttu-id="eb602-116">Элемент</span><span class="sxs-lookup"><span data-stu-id="eb602-116">Element</span></span>                                                                                                                            | <span data-ttu-id="eb602-117">Тип</span><span class="sxs-lookup"><span data-stu-id="eb602-117">Type</span></span>                                                                                                 | <span data-ttu-id="eb602-118">Описание</span><span class="sxs-lookup"><span data-stu-id="eb602-118">Description</span></span>                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eb602-119">**Включено (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="eb602-119">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                                           | <span data-ttu-id="eb602-120">Логическое</span><span class="sxs-lookup"><span data-stu-id="eb602-120">boolean</span></span>                                                                                              | <span data-ttu-id="eb602-121">Указывает, что триггер включен.</span><span class="sxs-lookup"><span data-stu-id="eb602-121">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="eb602-122">**Ендбаундари (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="eb602-122">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)                                   | <span data-ttu-id="eb602-123">dateTime</span><span class="sxs-lookup"><span data-stu-id="eb602-123">dateTime</span></span>                                                                                             | <span data-ttu-id="eb602-124">Указывает дату и время деактивации триггера.</span><span class="sxs-lookup"><span data-stu-id="eb602-124">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="eb602-125">Триггер не может запустить задачу после ее деактивации.</span><span class="sxs-lookup"><span data-stu-id="eb602-125">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="eb602-126">**Ексекутионтимелимит (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="eb602-126">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)                     | <span data-ttu-id="eb602-127">длительность</span><span class="sxs-lookup"><span data-stu-id="eb602-127">duration</span></span>                                                                                             | <span data-ttu-id="eb602-128">Указывает максимальное время, в течение которого задача может запускаться триггером.</span><span class="sxs-lookup"><span data-stu-id="eb602-128">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                   |
| [<span data-ttu-id="eb602-129">**Повторение (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="eb602-129">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                                     | [<span data-ttu-id="eb602-130">**репетитионтипе**</span><span class="sxs-lookup"><span data-stu-id="eb602-130">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md)                             | <span data-ttu-id="eb602-131">Указывает, как часто выполняется задача и как долго шаблон повторения повторяется после запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="eb602-131">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="eb602-132">**Счедулебидай (Календартригжертипе)**</span><span class="sxs-lookup"><span data-stu-id="eb602-132">**ScheduleByDay (calendarTriggerType)**</span></span>](taskschedulerschema-schedulebyday-calendartriggertype-element.md)                       | [<span data-ttu-id="eb602-133">**даилисчедулетипе**</span><span class="sxs-lookup"><span data-stu-id="eb602-133">**dailyScheduleType**</span></span>](taskschedulerschema-dailyscheduletype-complextype.md)                       | <span data-ttu-id="eb602-134">Указывает ежедневное расписание.</span><span class="sxs-lookup"><span data-stu-id="eb602-134">Specifies a daily schedule.</span></span><br/>                                                                                             |
| [<span data-ttu-id="eb602-135">**Счедулебимонс (Календартригжертипе)**</span><span class="sxs-lookup"><span data-stu-id="eb602-135">**ScheduleByMonth (calendarTriggerType)**</span></span>](taskschedulerschema-schedulebymonth-calendartriggertype-element.md)                   | [<span data-ttu-id="eb602-136">**монслисчедулетипе**</span><span class="sxs-lookup"><span data-stu-id="eb602-136">**monthlyScheduleType**</span></span>](taskschedulerschema-monthlyscheduletype-complextype.md)                   | <span data-ttu-id="eb602-137">Указывает ежемесячное расписание.</span><span class="sxs-lookup"><span data-stu-id="eb602-137">Specifies a monthly schedule.</span></span><br/>                                                                                           |
| [<span data-ttu-id="eb602-138">**Счедулебимонсдайофвик (Календартригжертипе)**</span><span class="sxs-lookup"><span data-stu-id="eb602-138">**ScheduleByMonthDayOfWeek (calendarTriggerType)**</span></span>](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [<span data-ttu-id="eb602-139">**монслидайофвиксчедулетипе**</span><span class="sxs-lookup"><span data-stu-id="eb602-139">**monthlyDayOfWeekScheduleType**</span></span>](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | <span data-ttu-id="eb602-140">Указывает триггер, который запускает задание в месячном расписании недели.</span><span class="sxs-lookup"><span data-stu-id="eb602-140">Specifies a trigger that starts a job on a monthly day-of-week schedule.</span></span><br/>                                                |
| [<span data-ttu-id="eb602-141">**Счедулебивик (Календартригжертипе)**</span><span class="sxs-lookup"><span data-stu-id="eb602-141">**ScheduleByWeek (calendarTriggerType)**</span></span>](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)                     | [<span data-ttu-id="eb602-142">**виклисчедулетипе**</span><span class="sxs-lookup"><span data-stu-id="eb602-142">**weeklyScheduleType**</span></span>](taskschedulerschema-weeklyscheduletype-complextype.md)                     | <span data-ttu-id="eb602-143">Указывает еженедельное расписание.</span><span class="sxs-lookup"><span data-stu-id="eb602-143">Specifies a weekly schedule.</span></span><br/>                                                                                            |
| [<span data-ttu-id="eb602-144">**Стартбаундари (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="eb602-144">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)                               | <span data-ttu-id="eb602-145">dateTime</span><span class="sxs-lookup"><span data-stu-id="eb602-145">dateTime</span></span>                                                                                             | <span data-ttu-id="eb602-146">Указывает дату и время активации триггера.</span><span class="sxs-lookup"><span data-stu-id="eb602-146">Specifies the date and time when the trigger is activated.</span></span> <span data-ttu-id="eb602-147">Этот элемент является обязательным.</span><span class="sxs-lookup"><span data-stu-id="eb602-147">This element is required.</span></span><br/>                                    |



## <a name="attributes"></a><span data-ttu-id="eb602-148">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="eb602-148">Attributes</span></span>



| <span data-ttu-id="eb602-149">Имя</span><span class="sxs-lookup"><span data-stu-id="eb602-149">Name</span></span> | <span data-ttu-id="eb602-150">Тип</span><span class="sxs-lookup"><span data-stu-id="eb602-150">Type</span></span> | <span data-ttu-id="eb602-151">Описание</span><span class="sxs-lookup"><span data-stu-id="eb602-151">Description</span></span>                               |
|------|------|-------------------------------------------|
| <span data-ttu-id="eb602-152">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="eb602-152">Id</span></span>   | <span data-ttu-id="eb602-153">ID</span><span class="sxs-lookup"><span data-stu-id="eb602-153">ID</span></span>   | <span data-ttu-id="eb602-154">Идентификатор триггера.</span><span class="sxs-lookup"><span data-stu-id="eb602-154">The identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="eb602-155">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eb602-155">Remarks</span></span>

<span data-ttu-id="eb602-156">Элемент [**стартбаундари**](taskschedulerschema-startboundary-triggerbasetype-element.md) является обязательным элементом для триггеров времени и календаря ([**тиметригжер**](taskschedulerschema-timetrigger-triggergroup-element.md) и **календартригжер**).</span><span class="sxs-lookup"><span data-stu-id="eb602-156">The [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element is a required element for time and calendar triggers ([**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) and **CalendarTrigger**).</span></span>

<span data-ttu-id="eb602-157">Перечисленные выше дочерние элементы определяются сложными типами элементов [**тригжербасетипе**](taskschedulerschema-triggerbasetype-complextype.md) и [**календартригжертипе**](taskschedulerschema-calendartriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="eb602-157">The child elements listed above are defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) and [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) complex element types.</span></span>

<span data-ttu-id="eb602-158">Для разработки скриптов триггеры календаря указываются с помощью одного из следующих объектов.</span><span class="sxs-lookup"><span data-stu-id="eb602-158">For script development, calendar triggers are specified using one of the following objects.</span></span>

-   [<span data-ttu-id="eb602-159">**даилитригжер**</span><span class="sxs-lookup"><span data-stu-id="eb602-159">**DailyTrigger**</span></span>](dailytrigger.md)
-   [<span data-ttu-id="eb602-160">**виклитригжер**</span><span class="sxs-lookup"><span data-stu-id="eb602-160">**WeeklyTrigger**</span></span>](weeklytrigger.md)
-   [<span data-ttu-id="eb602-161">**монслитригжер**</span><span class="sxs-lookup"><span data-stu-id="eb602-161">**MonthlyTrigger**</span></span>](monthlytrigger.md)
-   [<span data-ttu-id="eb602-162">**монслидовтригжер**</span><span class="sxs-lookup"><span data-stu-id="eb602-162">**MonthlyDOWTrigger**</span></span>](monthlydowtrigger.md)

<span data-ttu-id="eb602-163">Для разработки на C++ триггеры календаря указываются с помощью одного из следующих интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="eb602-163">For C++ development, calendar triggers are specified using one of the following interfaces.</span></span>

-   [<span data-ttu-id="eb602-164">**идаилитригжер**</span><span class="sxs-lookup"><span data-stu-id="eb602-164">**IDailyTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger)
-   [<span data-ttu-id="eb602-165">**ивиклитригжер**</span><span class="sxs-lookup"><span data-stu-id="eb602-165">**IWeeklyTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger)
-   [<span data-ttu-id="eb602-166">**имонслитригжер**</span><span class="sxs-lookup"><span data-stu-id="eb602-166">**IMonthlyTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger)
-   [<span data-ttu-id="eb602-167">**имонслидовтригжер**</span><span class="sxs-lookup"><span data-stu-id="eb602-167">**IMonthlyDOWTrigger**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger)

## <a name="examples"></a><span data-ttu-id="eb602-168">Примеры</span><span class="sxs-lookup"><span data-stu-id="eb602-168">Examples</span></span>

<span data-ttu-id="eb602-169">Полный пример XML-кода для задачи, указывающей триггер календаря, см. в разделе [Пример ежедневного триггера (XML)](daily-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="eb602-169">For a complete example of the XML for a task that specifies a calendar trigger, see [Daily Trigger Example (XML)](daily-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eb602-170">Требования</span><span class="sxs-lookup"><span data-stu-id="eb602-170">Requirements</span></span>



| <span data-ttu-id="eb602-171">Требование</span><span class="sxs-lookup"><span data-stu-id="eb602-171">Requirement</span></span> | <span data-ttu-id="eb602-172">Значение</span><span class="sxs-lookup"><span data-stu-id="eb602-172">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="eb602-173">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eb602-173">Minimum supported client</span></span><br/> | <span data-ttu-id="eb602-174">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eb602-174">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="eb602-175">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eb602-175">Minimum supported server</span></span><br/> | <span data-ttu-id="eb602-176">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="eb602-176">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="eb602-177">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eb602-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb602-178">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="eb602-178">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="eb602-179">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="eb602-179">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





