---
title: Счедулебивик (Календартригжертипе), элемент
description: Указывает еженедельное расписание.
ms.assetid: d2c33e76-0564-4b3c-ab86-e7bca667fa4f
keywords:
- планировщик задач еженедельного триггера, XML-элемент
- планировщик задач элемента Счедулебивик
topic_type:
- apiref
api_name:
- ScheduleByWeek
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2d5ab62a0c39c4c1d0102edcdb96d310e9315820
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104416057"
---
# <a name="schedulebyweek-calendartriggertype-element"></a><span data-ttu-id="eab92-105">Счедулебивик (Календартригжертипе), элемент</span><span class="sxs-lookup"><span data-stu-id="eab92-105">ScheduleByWeek (calendarTriggerType) Element</span></span>

<span data-ttu-id="eab92-106">Указывает еженедельное расписание.</span><span class="sxs-lookup"><span data-stu-id="eab92-106">Specifies a weekly schedule.</span></span> <span data-ttu-id="eab92-107">Например, задача начинается в 8:00 в конкретный день недели или в конкретный день недели, каждую неделю.</span><span class="sxs-lookup"><span data-stu-id="eab92-107">For example, the task starts at 8:00 AM on a specific day of the week every week or on a specific day of the week every other week.</span></span>

``` syntax
<xs:element name="ScheduleByWeek"
    type="weeklyScheduleType"
 />
```

<span data-ttu-id="eab92-108">Элемент **счедулебивик** определяется сложным типом [**календартригжертипе**](taskschedulerschema-calendartriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="eab92-108">The **ScheduleByWeek** element is defined by the [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="eab92-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="eab92-109">Parent element</span></span>



| <span data-ttu-id="eab92-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="eab92-110">Element</span></span>                                                                             | <span data-ttu-id="eab92-111">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="eab92-111">Derived from</span></span>                                                                       | <span data-ttu-id="eab92-112">Описание</span><span class="sxs-lookup"><span data-stu-id="eab92-112">Description</span></span>                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eab92-113">**календартригжер**</span><span class="sxs-lookup"><span data-stu-id="eab92-113">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md) | [<span data-ttu-id="eab92-114">**календартригжертипе**</span><span class="sxs-lookup"><span data-stu-id="eab92-114">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md) | <span data-ttu-id="eab92-115">Задает ежедневный, еженедельный, ежемесячный или ежемесячный триггер (DOW) в день недели.</span><span class="sxs-lookup"><span data-stu-id="eab92-115">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="eab92-116">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="eab92-116">Child elements</span></span>



| <span data-ttu-id="eab92-117">Элемент</span><span class="sxs-lookup"><span data-stu-id="eab92-117">Element</span></span>                                                                               | <span data-ttu-id="eab92-118">Тип</span><span class="sxs-lookup"><span data-stu-id="eab92-118">Type</span></span>                                                                     | <span data-ttu-id="eab92-119">Описание</span><span class="sxs-lookup"><span data-stu-id="eab92-119">Description</span></span>                                                          |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="eab92-120">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="eab92-120">**DaysOfWeek**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)       | [<span data-ttu-id="eab92-121">**дайсофвиктипе**</span><span class="sxs-lookup"><span data-stu-id="eab92-121">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="eab92-122">Указывает дни недели, в которые выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="eab92-122">Specifies the days of the week in which the task runs.</span></span><br/>    |
| [<span data-ttu-id="eab92-123">**виксинтервал**</span><span class="sxs-lookup"><span data-stu-id="eab92-123">**WeeksInterval**</span></span>](taskschedulerschema-weeksinterval-weeklyscheduletype-element.md) | <span data-ttu-id="eab92-124">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="eab92-124">unsignedByte</span></span>                                                             | <span data-ttu-id="eab92-125">Указывает интервал между неделями в расписании.</span><span class="sxs-lookup"><span data-stu-id="eab92-125">Specifies the interval between the weeks in the schedule.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="eab92-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eab92-126">Remarks</span></span>

<span data-ttu-id="eab92-127">Перечисленные выше дочерние элементы определяются сложными типами элементов [**виклисчедулетипе**](taskschedulerschema-weeklyscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="eab92-127">The child elements listed above are defined by the [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) complex element types.</span></span>

<span data-ttu-id="eab92-128">Время дня, когда начинается задача, задается элементом [**стартбаундари**](taskschedulerschema-startboundary-triggerbasetype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="eab92-128">The time of day that the task is started is set by the [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element.</span></span>

<span data-ttu-id="eab92-129">Для разработки сценариев еженедельный триггер указывается с помощью объекта [**виклитригжер**](weeklytrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="eab92-129">For scripting development, a weekly trigger is specified using the [**WeeklyTrigger**](weeklytrigger.md) object.</span></span>

<span data-ttu-id="eab92-130">Для разработки на C++ еженедельный триггер указывается с помощью интерфейса [**ивиклитригжер**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger) .</span><span class="sxs-lookup"><span data-stu-id="eab92-130">For C++ development, a weekly trigger is specified using the [**IWeeklyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="eab92-131">Примеры</span><span class="sxs-lookup"><span data-stu-id="eab92-131">Examples</span></span>

<span data-ttu-id="eab92-132">Следующий XML-код определяет еженедельный календарный триггер, который запускает задачу с понедельника по пятницу (в 8:00 AM) каждую неделю.</span><span class="sxs-lookup"><span data-stu-id="eab92-132">The following XML defines a weekly calendar trigger that starts a task Monday through Friday (at 8:00 AM) every week.</span></span>


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByWeek>
        <WeeksInterval>1</WeeksInterval>
        <DaysOfWeek>
            <Monday/>
            <Tuesday/>
            <Wednesday/>
            <Thurday/>
            <Friday/>
        </DaysOfWeek>
    </ScheduleByWeek>
</CalendarTrigger>
```



## <a name="requirements"></a><span data-ttu-id="eab92-133">Требования</span><span class="sxs-lookup"><span data-stu-id="eab92-133">Requirements</span></span>



| <span data-ttu-id="eab92-134">Требование</span><span class="sxs-lookup"><span data-stu-id="eab92-134">Requirement</span></span> | <span data-ttu-id="eab92-135">Значение</span><span class="sxs-lookup"><span data-stu-id="eab92-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="eab92-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eab92-136">Minimum supported client</span></span><br/> | <span data-ttu-id="eab92-137">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eab92-137">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="eab92-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eab92-138">Minimum supported server</span></span><br/> | <span data-ttu-id="eab92-139">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="eab92-139">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="eab92-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eab92-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eab92-141">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="eab92-141">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="eab92-142">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="eab92-142">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





