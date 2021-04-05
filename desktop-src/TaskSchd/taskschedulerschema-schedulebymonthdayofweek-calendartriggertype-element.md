---
title: Счедулебимонсдайофвик (Календартригжертипе), элемент
description: Задает ежемесячное расписание для дня недели.
ms.assetid: 7ff17bea-fa26-40c4-90fa-d94a3690e464
keywords:
- планировщик задач элемента Счедулебимонсдайофвик
topic_type:
- apiref
api_name:
- ScheduleByMonthDayOfWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3e92d6ad530466a2238c8239c9e262f85ae361d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803317"
---
# <a name="schedulebymonthdayofweek-calendartriggertype-element"></a><span data-ttu-id="5438f-104">Счедулебимонсдайофвик (Календартригжертипе), элемент</span><span class="sxs-lookup"><span data-stu-id="5438f-104">ScheduleByMonthDayOfWeek (calendarTriggerType) Element</span></span>

<span data-ttu-id="5438f-105">Задает ежемесячное расписание для дня недели.</span><span class="sxs-lookup"><span data-stu-id="5438f-105">Specifies a monthly day-of-week schedule.</span></span> <span data-ttu-id="5438f-106">Например, задача запускается в определенные дни недели, недели месяца и месяцы года.</span><span class="sxs-lookup"><span data-stu-id="5438f-106">For example, the task starts on specific days of the week, weeks of the month, and months of the year.</span></span>

``` syntax
<xs:element name="ScheduleByMonthDayOfWeek"
    type="monthlyDayOfWeekScheduleType"
 />
```

<span data-ttu-id="5438f-107">Элемент **счедулебимонсдайофвик** определяется сложным типом [**монслидайофвиксчедулетипе**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="5438f-107">The **ScheduleByMonthDayOfWeek** element is defined by the [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="5438f-108">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="5438f-108">Parent element</span></span>



| <span data-ttu-id="5438f-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="5438f-109">Element</span></span>                                                                             | <span data-ttu-id="5438f-110">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="5438f-110">Derived from</span></span>                                                                       | <span data-ttu-id="5438f-111">Описание</span><span class="sxs-lookup"><span data-stu-id="5438f-111">Description</span></span>                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5438f-112">**календартригжер**</span><span class="sxs-lookup"><span data-stu-id="5438f-112">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md) | [<span data-ttu-id="5438f-113">**календартригжертипе**</span><span class="sxs-lookup"><span data-stu-id="5438f-113">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md) | <span data-ttu-id="5438f-114">Задает ежедневный, еженедельный, ежемесячный или ежемесячный триггер (DOW) в день недели.</span><span class="sxs-lookup"><span data-stu-id="5438f-114">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="5438f-115">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="5438f-115">Child elements</span></span>



| <span data-ttu-id="5438f-116">Элемент</span><span class="sxs-lookup"><span data-stu-id="5438f-116">Element</span></span>                                                                                   | <span data-ttu-id="5438f-117">Тип</span><span class="sxs-lookup"><span data-stu-id="5438f-117">Type</span></span>                                                                     | <span data-ttu-id="5438f-118">Описание</span><span class="sxs-lookup"><span data-stu-id="5438f-118">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="5438f-119">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="5438f-119">**DaysOfWeek**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="5438f-120">**дайсофвиктипе**</span><span class="sxs-lookup"><span data-stu-id="5438f-120">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="5438f-121">Указывает дни недели, в которые выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="5438f-121">Specifies the days of the week in which the task runs.</span></span><br/>       |
| [<span data-ttu-id="5438f-122">**Месяц**</span><span class="sxs-lookup"><span data-stu-id="5438f-122">**Months**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md)         | [<span data-ttu-id="5438f-123">**монсстипе**</span><span class="sxs-lookup"><span data-stu-id="5438f-123">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md)         | <span data-ttu-id="5438f-124">Указывает месяцы года, в течение которых выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="5438f-124">Specifies the months of the year during which the task runs.</span></span><br/> |
| [<span data-ttu-id="5438f-125">**Недели**</span><span class="sxs-lookup"><span data-stu-id="5438f-125">**Weeks**</span></span>](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md)           | <span data-ttu-id="5438f-126">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="5438f-126">unsignedByte</span></span>                                                             | <span data-ttu-id="5438f-127">Указывает интервал между неделями в расписании.</span><span class="sxs-lookup"><span data-stu-id="5438f-127">Specifies the interval between the weeks in the schedule.</span></span><br/>    |



## <a name="remarks"></a><span data-ttu-id="5438f-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5438f-128">Remarks</span></span>

<span data-ttu-id="5438f-129">Время дня, когда начинается задача, задается элементом [**стартбаундари**](taskschedulerschema-startboundary-triggerbasetype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="5438f-129">The time of day that the task is started is set by the [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element.</span></span>

<span data-ttu-id="5438f-130">Для разработки сценариев месячный триггер дня недели указывается с помощью объекта [**монслидовтригжер**](monthlydowtrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="5438f-130">For scripting development, a monthly day-of-week trigger is specified using the [**MonthlyDOWTrigger**](monthlydowtrigger.md) object.</span></span>

<span data-ttu-id="5438f-131">Для разработки на C++ триггер месячного дня недели указывается с помощью интерфейса [**имонслидовтригжер**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger) .</span><span class="sxs-lookup"><span data-stu-id="5438f-131">For C++ development, a monthly day-of-week trigger is specified using the [**IMonthlyDOWTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger) interface.</span></span>

<span data-ttu-id="5438f-132">Перечисленные выше дочерние элементы определяются сложными типами элементов [**монслидайофвиксчедулетипе**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="5438f-132">The child elements listed above are defined by the [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) complex element types.</span></span>

## <a name="examples"></a><span data-ttu-id="5438f-133">Примеры</span><span class="sxs-lookup"><span data-stu-id="5438f-133">Examples</span></span>

<span data-ttu-id="5438f-134">Следующий XML-код определяет месячный день недели в календаре, который запускает задачу (в 8:00 AM) в понедельник первой недели для каждого месяца года.</span><span class="sxs-lookup"><span data-stu-id="5438f-134">The following XML defines a monthly day of week calendar trigger that starts a task ( at 8:00 AM) on Monday of the first week for each month of the year.</span></span>


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
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
</CalendarTrigger>
```



## <a name="requirements"></a><span data-ttu-id="5438f-135">Требования</span><span class="sxs-lookup"><span data-stu-id="5438f-135">Requirements</span></span>



| <span data-ttu-id="5438f-136">Требование</span><span class="sxs-lookup"><span data-stu-id="5438f-136">Requirement</span></span> | <span data-ttu-id="5438f-137">Значение</span><span class="sxs-lookup"><span data-stu-id="5438f-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5438f-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5438f-138">Minimum supported client</span></span><br/> | <span data-ttu-id="5438f-139">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5438f-139">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5438f-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5438f-140">Minimum supported server</span></span><br/> | <span data-ttu-id="5438f-141">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5438f-141">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5438f-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5438f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5438f-143">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="5438f-143">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="5438f-144">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="5438f-144">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





