---
title: DaysOfWeek (Монслидайофвиксчедулетипе), элемент
description: Указывает дни недели, в которые выполняется задача. | DaysOfWeek (Монслидайофвиксчедулетипе), элемент
ms.assetid: d84f0019-1369-465f-9054-0fb5a83cad6d
keywords:
- планировщик задач элемента DaysOfWeek
topic_type:
- apiref
api_name:
- DaysOfWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3867e08dd001a035a3ab25da056f75c1e73eeeef
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684947"
---
# <a name="daysofweek-monthlydayofweekscheduletype-element"></a><span data-ttu-id="249f6-105">DaysOfWeek (Монслидайофвиксчедулетипе), элемент</span><span class="sxs-lookup"><span data-stu-id="249f6-105">DaysOfWeek (monthlyDayOfWeekScheduleType) Element</span></span>

<span data-ttu-id="249f6-106">Указывает дни недели, в которые выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="249f6-106">Specifies the days of the week in which the task runs.</span></span>

``` syntax
<xs:element name="DaysOfWeek"
    type="daysOfWeekType"
 />
```

<span data-ttu-id="249f6-107">Элемент **DaysOfWeek** определяется сложным типом [**монслидайофвиксчедулетипе**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="249f6-107">The **DaysOfWeek** element is defined by the [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="249f6-108">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="249f6-108">Parent element</span></span>



| <span data-ttu-id="249f6-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="249f6-109">Element</span></span>                                                                                                      | <span data-ttu-id="249f6-110">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="249f6-110">Derived from</span></span>                                                                                         | <span data-ttu-id="249f6-111">Описание</span><span class="sxs-lookup"><span data-stu-id="249f6-111">Description</span></span>                                                                          |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="249f6-112">**счедулебимонсдайофвик**</span><span class="sxs-lookup"><span data-stu-id="249f6-112">**ScheduleByMonthDayOfWeek**</span></span>](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [<span data-ttu-id="249f6-113">**монслидайофвиксчедулетипе**</span><span class="sxs-lookup"><span data-stu-id="249f6-113">**monthlyDayOfWeekScheduleType**</span></span>](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | <span data-ttu-id="249f6-114">Указывает триггер, который запускает задание для ежемесячного расписания недели.</span><span class="sxs-lookup"><span data-stu-id="249f6-114">Specifies a trigger that starts a job for a monthly day-of-week schedule.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="249f6-115">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="249f6-115">Child elements</span></span>



| <span data-ttu-id="249f6-116">Элемент</span><span class="sxs-lookup"><span data-stu-id="249f6-116">Element</span></span>                                                                   | <span data-ttu-id="249f6-117">Тип</span><span class="sxs-lookup"><span data-stu-id="249f6-117">Type</span></span> | <span data-ttu-id="249f6-118">Описание</span><span class="sxs-lookup"><span data-stu-id="249f6-118">Description</span></span>                                           |
|---------------------------------------------------------------------------|------|-------------------------------------------------------|
| [<span data-ttu-id="249f6-119">**Пятница**</span><span class="sxs-lookup"><span data-stu-id="249f6-119">**Friday**</span></span>](taskschedulerschema-friday-daysofweektype-element.md)       |      | <span data-ttu-id="249f6-120">Указывает, что задача выполняется в пятницу.</span><span class="sxs-lookup"><span data-stu-id="249f6-120">Specifies that the task runs on Friday.</span></span><br/>    |
| [<span data-ttu-id="249f6-121">**Понедельник**</span><span class="sxs-lookup"><span data-stu-id="249f6-121">**Monday**</span></span>](taskschedulerschema-monday-daysofweektype-element.md)       |      | <span data-ttu-id="249f6-122">Указывает, что задача выполняется в понедельник.</span><span class="sxs-lookup"><span data-stu-id="249f6-122">Specifies that the task runs on Monday.</span></span><br/>    |
| [<span data-ttu-id="249f6-123">**Суббота**</span><span class="sxs-lookup"><span data-stu-id="249f6-123">**Saturday**</span></span>](taskschedulerschema-saturday-daysofweektype-element.md)   |      | <span data-ttu-id="249f6-124">Указывает, что задача выполняется в субботу.</span><span class="sxs-lookup"><span data-stu-id="249f6-124">Specifies that the task runs on Saturday.</span></span><br/>  |
| [<span data-ttu-id="249f6-125">**Воскресенье**</span><span class="sxs-lookup"><span data-stu-id="249f6-125">**Sunday**</span></span>](taskschedulerschema-sunday-daysofweektype-element.md)       |      | <span data-ttu-id="249f6-126">Указывает, что задача выполняется в воскресенье.</span><span class="sxs-lookup"><span data-stu-id="249f6-126">Specifies that the task runs on Sunday.</span></span><br/>    |
| [<span data-ttu-id="249f6-127">**Четверг**</span><span class="sxs-lookup"><span data-stu-id="249f6-127">**Thursday**</span></span>](taskschedulerschema-thursday-daysofweektype-element.md)   |      | <span data-ttu-id="249f6-128">Указывает, что задача выполняется в четверг.</span><span class="sxs-lookup"><span data-stu-id="249f6-128">Specifies that the task runs on Thursday.</span></span><br/>  |
| [<span data-ttu-id="249f6-129">**Вторник**</span><span class="sxs-lookup"><span data-stu-id="249f6-129">**Tuesday**</span></span>](taskschedulerschema-tuesday-daysofweektype-element.md)     |      | <span data-ttu-id="249f6-130">Указывает, что задача выполняется во вторник.</span><span class="sxs-lookup"><span data-stu-id="249f6-130">Specifies that the task runs on Tuesday.</span></span><br/>   |
| [<span data-ttu-id="249f6-131">**Среда**</span><span class="sxs-lookup"><span data-stu-id="249f6-131">**Wednesday**</span></span>](taskschedulerschema-wednesday-daysofweektype-element.md) |      | <span data-ttu-id="249f6-132">Указывает, что задача выполняется в среду.</span><span class="sxs-lookup"><span data-stu-id="249f6-132">Specifies that the task runs on Wednesday.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="249f6-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="249f6-133">Remarks</span></span>

<span data-ttu-id="249f6-134">Для разработки сценариев дни недели для месячного дня недели задаются с помощью свойства [**монслидовтригжер. DaysOfWeek**](monthlydowtrigger-daysofweek.md) .</span><span class="sxs-lookup"><span data-stu-id="249f6-134">For scripting development, the days of the week for a monthly day-of-week calendar are specified using the [**MonthlyDOWTrigger.DaysOfWeek**](monthlydowtrigger-daysofweek.md) property.</span></span>

<span data-ttu-id="249f6-135">Для разработки на C++ дни недели для месячного дня недели задаются с помощью свойства [**имонслидовтригжер::D айсофвик**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_daysofweek) .</span><span class="sxs-lookup"><span data-stu-id="249f6-135">For C++ development, the days of the week for a monthly day-of-week calendar are specified using the [**IMonthlyDOWTrigger::DaysOfWeek**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_daysofweek) property.</span></span>

<span data-ttu-id="249f6-136">Приведенные выше дочерние элементы определяются сложным типом [**дайсофвиктипе**](taskschedulerschema-daysofweektype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="249f6-136">The child elements above are defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

## <a name="examples"></a><span data-ttu-id="249f6-137">Примеры</span><span class="sxs-lookup"><span data-stu-id="249f6-137">Examples</span></span>

<span data-ttu-id="249f6-138">Следующий XML-код определяет месячный календарь дня недели, который запускает задачу в понедельник первой недели для каждого месяца года.</span><span class="sxs-lookup"><span data-stu-id="249f6-138">The following XML defines a monthly day-of-week calendar that starts the task on Monday of the first week for each month of the year.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="249f6-139">Требования</span><span class="sxs-lookup"><span data-stu-id="249f6-139">Requirements</span></span>



| <span data-ttu-id="249f6-140">Требование</span><span class="sxs-lookup"><span data-stu-id="249f6-140">Requirement</span></span> | <span data-ttu-id="249f6-141">Значение</span><span class="sxs-lookup"><span data-stu-id="249f6-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="249f6-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="249f6-142">Minimum supported client</span></span><br/> | <span data-ttu-id="249f6-143">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="249f6-143">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="249f6-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="249f6-144">Minimum supported server</span></span><br/> | <span data-ttu-id="249f6-145">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="249f6-145">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="249f6-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="249f6-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="249f6-147">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="249f6-147">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="249f6-148">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="249f6-148">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





