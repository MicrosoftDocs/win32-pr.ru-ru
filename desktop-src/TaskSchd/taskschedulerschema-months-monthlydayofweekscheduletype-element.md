---
title: Months (Монслидайофвиксчедулетипе), элемент
description: Указывает месяцы года, в течение которых задача выполняется для ежемесячного расписания недели.
ms.assetid: 420fa7f4-7106-483e-9b3b-d1ba51f25222
keywords:
- Элемент months планировщик задач
topic_type:
- apiref
api_name:
- Months
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 76f13a5823e0154519dbdb093dd03ea36bbe77b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415097"
---
# <a name="months-monthlydayofweekscheduletype-element"></a><span data-ttu-id="f18b5-104">Months (Монслидайофвиксчедулетипе), элемент</span><span class="sxs-lookup"><span data-stu-id="f18b5-104">Months (monthlyDayOfWeekScheduleType) Element</span></span>

<span data-ttu-id="f18b5-105">Указывает месяцы года, в течение которых задача выполняется для ежемесячного расписания недели.</span><span class="sxs-lookup"><span data-stu-id="f18b5-105">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span>

``` syntax
<xs:element name="Months"
    type="monthsType"
 />
```

<span data-ttu-id="f18b5-106">Элемент **months** определяется сложным типом [**монслидайофвиксчедулетипе**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f18b5-106">The **Months** element is defined by the [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f18b5-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="f18b5-107">Parent element</span></span>



| <span data-ttu-id="f18b5-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="f18b5-108">Element</span></span>                                                                                                                            | <span data-ttu-id="f18b5-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="f18b5-109">Derived from</span></span>                                                                                         | <span data-ttu-id="f18b5-110">Описание</span><span class="sxs-lookup"><span data-stu-id="f18b5-110">Description</span></span>                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="f18b5-111">**Счедулебимонсдайофвик (Календартригжертипе)**</span><span class="sxs-lookup"><span data-stu-id="f18b5-111">**ScheduleByMonthDayOfWeek (calendarTriggerType)**</span></span>](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [<span data-ttu-id="f18b5-112">**монслидайофвиксчедулетипе**</span><span class="sxs-lookup"><span data-stu-id="f18b5-112">**monthlyDayOfWeekScheduleType**</span></span>](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | <span data-ttu-id="f18b5-113">Указывает триггер, который запускает задание для ежемесячного расписания недели.</span><span class="sxs-lookup"><span data-stu-id="f18b5-113">Specifies a trigger that starts a job for a monthly day-of-week schedule.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="f18b5-114">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="f18b5-114">Child elements</span></span>



| <span data-ttu-id="f18b5-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="f18b5-115">Element</span></span>                                                               | <span data-ttu-id="f18b5-116">Тип</span><span class="sxs-lookup"><span data-stu-id="f18b5-116">Type</span></span> | <span data-ttu-id="f18b5-117">Описание</span><span class="sxs-lookup"><span data-stu-id="f18b5-117">Description</span></span>                                           |
|-----------------------------------------------------------------------|------|-------------------------------------------------------|
| [<span data-ttu-id="f18b5-118">**Апрель**</span><span class="sxs-lookup"><span data-stu-id="f18b5-118">**April**</span></span>](taskschedulerschema-april-monthstype-element.md)         |      | <span data-ttu-id="f18b5-119">Указывает, что задача выполняется в апреле.</span><span class="sxs-lookup"><span data-stu-id="f18b5-119">Specifies that the task runs in April.</span></span><br/>     |
| [<span data-ttu-id="f18b5-120">**Августа**</span><span class="sxs-lookup"><span data-stu-id="f18b5-120">**August**</span></span>](taskschedulerschema-august-monthstype-element.md)       |      | <span data-ttu-id="f18b5-121">Указывает, что задача выполняется в августе.</span><span class="sxs-lookup"><span data-stu-id="f18b5-121">Specifies that the task runs in August.</span></span><br/>    |
| [<span data-ttu-id="f18b5-122">**Декабрь**</span><span class="sxs-lookup"><span data-stu-id="f18b5-122">**December**</span></span>](taskschedulerschema-december-monthstype-element.md)   |      | <span data-ttu-id="f18b5-123">Указывает, что задача выполняется в декабре.</span><span class="sxs-lookup"><span data-stu-id="f18b5-123">Specifies that the task runs in December.</span></span><br/>  |
| [<span data-ttu-id="f18b5-124">**Февраль**</span><span class="sxs-lookup"><span data-stu-id="f18b5-124">**February**</span></span>](taskschedulerschema-february-monthstype-element.md)   |      | <span data-ttu-id="f18b5-125">Указывает, что задача выполняется в феврале.</span><span class="sxs-lookup"><span data-stu-id="f18b5-125">Specifies that the task runs in February.</span></span><br/>  |
| [<span data-ttu-id="f18b5-126">**Января**</span><span class="sxs-lookup"><span data-stu-id="f18b5-126">**January**</span></span>](taskschedulerschema-january-monthstype-element.md)     |      | <span data-ttu-id="f18b5-127">Указывает, что задача выполняется в январе.</span><span class="sxs-lookup"><span data-stu-id="f18b5-127">Specifies that the task runs in January.</span></span><br/>   |
| [<span data-ttu-id="f18b5-128">**Июле**</span><span class="sxs-lookup"><span data-stu-id="f18b5-128">**July**</span></span>](taskschedulerschema-july-monthstype-element.md)           |      | <span data-ttu-id="f18b5-129">Указывает, что задача выполняется в июле.</span><span class="sxs-lookup"><span data-stu-id="f18b5-129">Specifies that the task runs in July.</span></span><br/>      |
| [<span data-ttu-id="f18b5-130">**Июнь**</span><span class="sxs-lookup"><span data-stu-id="f18b5-130">**June**</span></span>](taskschedulerschema-june-monthstype-element.md)           |      | <span data-ttu-id="f18b5-131">Указывает, что задача выполняется в июне.</span><span class="sxs-lookup"><span data-stu-id="f18b5-131">Specifies that the task runs in June.</span></span><br/>      |
| [<span data-ttu-id="f18b5-132">**Март**</span><span class="sxs-lookup"><span data-stu-id="f18b5-132">**March**</span></span>](taskschedulerschema-march-monthstype-element.md)         |      | <span data-ttu-id="f18b5-133">Указывает, что задача выполняется в марте.</span><span class="sxs-lookup"><span data-stu-id="f18b5-133">Specifies that the task runs in March.</span></span><br/>     |
| [<span data-ttu-id="f18b5-134">**Мая**</span><span class="sxs-lookup"><span data-stu-id="f18b5-134">**May**</span></span>](taskschedulerschema-may-monthstype-element.md)             |      | <span data-ttu-id="f18b5-135">Указывает, что задача выполняется в Май.</span><span class="sxs-lookup"><span data-stu-id="f18b5-135">Specifies that the task runs in May.</span></span><br/>       |
| [<span data-ttu-id="f18b5-136">**Ноября**</span><span class="sxs-lookup"><span data-stu-id="f18b5-136">**November**</span></span>](taskschedulerschema-november-monthstype-element.md)   |      | <span data-ttu-id="f18b5-137">Указывает, что задача выполняется в ноябре.</span><span class="sxs-lookup"><span data-stu-id="f18b5-137">Specifies that the task runs in November.</span></span><br/>  |
| [<span data-ttu-id="f18b5-138">**Октябре**</span><span class="sxs-lookup"><span data-stu-id="f18b5-138">**October**</span></span>](taskschedulerschema-october-monthstype-element.md)     |      | <span data-ttu-id="f18b5-139">Указывает, что задача выполняется в октябре.</span><span class="sxs-lookup"><span data-stu-id="f18b5-139">Specifies that the task runs in October.</span></span><br/>   |
| [<span data-ttu-id="f18b5-140">**Сентябрь**</span><span class="sxs-lookup"><span data-stu-id="f18b5-140">**September**</span></span>](taskschedulerschema-september-monthstype-element.md) |      | <span data-ttu-id="f18b5-141">Указывает, что задача выполняется в сентябре.</span><span class="sxs-lookup"><span data-stu-id="f18b5-141">Specifies that the task runs in September.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f18b5-142">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f18b5-142">Remarks</span></span>

<span data-ttu-id="f18b5-143">Для разработки со сценариями месяцы года для расписания месячного дня недели задаются с помощью свойства [**монслидовтригжер. монссофеар**](monthlydowtrigger-monthsofyear.md) .</span><span class="sxs-lookup"><span data-stu-id="f18b5-143">For scripting development, the months of a year for a monthly day-of-week schedule are specified using the [**MonthlyDOWTrigger.MonthsOfYear**](monthlydowtrigger-monthsofyear.md) property.</span></span>

<span data-ttu-id="f18b5-144">Для разработки на C++ месяцы месяца года для расписания ежемесячного дня задаются с помощью свойства [**имонслидовтригжер:: монссофеар**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_monthsofyear) .</span><span class="sxs-lookup"><span data-stu-id="f18b5-144">For C++ development, the months of a year for a monthly day-of-week schedule are specified using the [**IMonthlyDOWTrigger::MonthsOfYear**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_monthsofyear) property.</span></span>

<span data-ttu-id="f18b5-145">Приведенные выше дочерние элементы определяются сложным типом [**монсстипе**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f18b5-145">The child elements above are defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="examples"></a><span data-ttu-id="f18b5-146">Примеры</span><span class="sxs-lookup"><span data-stu-id="f18b5-146">Examples</span></span>

<span data-ttu-id="f18b5-147">Следующий XML-код определяет месячный календарь дня недели, который запускает задачу в понедельник первой недели для каждого месяца года.</span><span class="sxs-lookup"><span data-stu-id="f18b5-147">The following XML defines a monthly day-of-week calendar that starts the task on Monday of the first week for each month of the year.</span></span>


```XML
<ScheduleByMonthDayOfWeek>
        <Weeks>
            <Week>1</Week>
        </Weeks>
        <DaysOfWeek>
            <Monday/>
        </DaysOfWeek>
        <Months>
            <January/>
            <February/>
            <March/>
            <April/>
            <May/>
            <June/>
            <July/>
            <August/>
            <September/>
            <October/>
            <November/>
            <December/>
        <Months>
    </ScheduleByMonthDayOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="f18b5-148">Требования</span><span class="sxs-lookup"><span data-stu-id="f18b5-148">Requirements</span></span>



| <span data-ttu-id="f18b5-149">Требование</span><span class="sxs-lookup"><span data-stu-id="f18b5-149">Requirement</span></span> | <span data-ttu-id="f18b5-150">Значение</span><span class="sxs-lookup"><span data-stu-id="f18b5-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f18b5-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f18b5-151">Minimum supported client</span></span><br/> | <span data-ttu-id="f18b5-152">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f18b5-152">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f18b5-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f18b5-153">Minimum supported server</span></span><br/> | <span data-ttu-id="f18b5-154">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f18b5-154">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f18b5-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f18b5-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f18b5-156">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="f18b5-156">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="f18b5-157">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="f18b5-157">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





