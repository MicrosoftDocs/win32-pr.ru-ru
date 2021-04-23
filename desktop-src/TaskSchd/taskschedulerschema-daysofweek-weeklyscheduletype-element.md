---
title: DaysOfWeek (Виклисчедулетипе), элемент
description: Указывает дни недели, в которые выполняется задача. | DaysOfWeek (Виклисчедулетипе), элемент
ms.assetid: 86555681-2324-4095-9eab-fdef40e0acba
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
ms.openlocfilehash: 3a2b310feb49f3141d1f7f08c4552305f9ffc3ea
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105684946"
---
# <a name="daysofweek-weeklyscheduletype-element"></a><span data-ttu-id="1e4ce-105">DaysOfWeek (Виклисчедулетипе), элемент</span><span class="sxs-lookup"><span data-stu-id="1e4ce-105">DaysOfWeek (weeklyScheduleType) Element</span></span>

<span data-ttu-id="1e4ce-106">Указывает дни недели, в которые выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="1e4ce-106">Specifies the days of the week in which the task runs.</span></span>

``` syntax
<xs:element name="DaysOfWeek"
    type="daysOfWeekType"
 />
```

<span data-ttu-id="1e4ce-107">Элемент **DaysOfWeek** определяется сложным типом [**виклисчедулетипе**](taskschedulerschema-weeklyscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="1e4ce-107">The **DaysOfWeek** element is defined by the [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="1e4ce-108">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="1e4ce-108">Parent element</span></span>



| <span data-ttu-id="1e4ce-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="1e4ce-109">Element</span></span>                                                                                  | <span data-ttu-id="1e4ce-110">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="1e4ce-110">Derived from</span></span>                                                                     | <span data-ttu-id="1e4ce-111">Описание</span><span class="sxs-lookup"><span data-stu-id="1e4ce-111">Description</span></span>                             |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="1e4ce-112">**счедулебивик**</span><span class="sxs-lookup"><span data-stu-id="1e4ce-112">**ScheduleByWeek**</span></span>](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) | [<span data-ttu-id="1e4ce-113">**виклисчедулетипе**</span><span class="sxs-lookup"><span data-stu-id="1e4ce-113">**weeklyScheduleType**</span></span>](taskschedulerschema-weeklyscheduletype-complextype.md) | <span data-ttu-id="1e4ce-114">Указывает еженедельное расписание.</span><span class="sxs-lookup"><span data-stu-id="1e4ce-114">Specifies a weekly schedule.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="1e4ce-115">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="1e4ce-115">Child elements</span></span>



| <span data-ttu-id="1e4ce-116">Элемент</span><span class="sxs-lookup"><span data-stu-id="1e4ce-116">Element</span></span>                                                                   | <span data-ttu-id="1e4ce-117">Тип</span><span class="sxs-lookup"><span data-stu-id="1e4ce-117">Type</span></span> | <span data-ttu-id="1e4ce-118">Описание</span><span class="sxs-lookup"><span data-stu-id="1e4ce-118">Description</span></span>                                           |
|---------------------------------------------------------------------------|------|-------------------------------------------------------|
| [<span data-ttu-id="1e4ce-119">**Пятница**</span><span class="sxs-lookup"><span data-stu-id="1e4ce-119">**Friday**</span></span>](taskschedulerschema-friday-daysofweektype-element.md)       |      | <span data-ttu-id="1e4ce-120">Указывает, что задача выполняется в пятницу.</span><span class="sxs-lookup"><span data-stu-id="1e4ce-120">Specifies that the task runs on Friday.</span></span><br/>    |
| [<span data-ttu-id="1e4ce-121">**Понедельник**</span><span class="sxs-lookup"><span data-stu-id="1e4ce-121">**Monday**</span></span>](taskschedulerschema-monday-daysofweektype-element.md)       |      | <span data-ttu-id="1e4ce-122">Указывает, что задача выполняется в понедельник.</span><span class="sxs-lookup"><span data-stu-id="1e4ce-122">Specifies that the task runs on Monday.</span></span><br/>    |
| [<span data-ttu-id="1e4ce-123">**Суббота**</span><span class="sxs-lookup"><span data-stu-id="1e4ce-123">**Saturday**</span></span>](taskschedulerschema-saturday-daysofweektype-element.md)   |      | <span data-ttu-id="1e4ce-124">Указывает, что задача выполняется в субботу.</span><span class="sxs-lookup"><span data-stu-id="1e4ce-124">Specifies that the task runs on Saturday.</span></span><br/>  |
| [<span data-ttu-id="1e4ce-125">**Воскресенье**</span><span class="sxs-lookup"><span data-stu-id="1e4ce-125">**Sunday**</span></span>](taskschedulerschema-sunday-daysofweektype-element.md)       |      | <span data-ttu-id="1e4ce-126">Указывает, что задача выполняется в воскресенье.</span><span class="sxs-lookup"><span data-stu-id="1e4ce-126">Specifies that the task runs on Sunday.</span></span><br/>    |
| [<span data-ttu-id="1e4ce-127">**Четверг**</span><span class="sxs-lookup"><span data-stu-id="1e4ce-127">**Thursday**</span></span>](taskschedulerschema-thursday-daysofweektype-element.md)   |      | <span data-ttu-id="1e4ce-128">Указывает, что задача выполняется в четверг.</span><span class="sxs-lookup"><span data-stu-id="1e4ce-128">Specifies that the task runs on Thursday.</span></span><br/>  |
| [<span data-ttu-id="1e4ce-129">**Вторник**</span><span class="sxs-lookup"><span data-stu-id="1e4ce-129">**Tuesday**</span></span>](taskschedulerschema-tuesday-daysofweektype-element.md)     |      | <span data-ttu-id="1e4ce-130">Указывает, что задача выполняется во вторник.</span><span class="sxs-lookup"><span data-stu-id="1e4ce-130">Specifies that the task runs on Tuesday.</span></span><br/>   |
| [<span data-ttu-id="1e4ce-131">**Среда**</span><span class="sxs-lookup"><span data-stu-id="1e4ce-131">**Wednesday**</span></span>](taskschedulerschema-wednesday-daysofweektype-element.md) |      | <span data-ttu-id="1e4ce-132">Указывает, что задача выполняется в среду.</span><span class="sxs-lookup"><span data-stu-id="1e4ce-132">Specifies that the task runs on Wednesday.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1e4ce-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1e4ce-133">Remarks</span></span>

<span data-ttu-id="1e4ce-134">Предыдущие дочерние элементы определяются сложным типом [**дайсофвиктипе**](taskschedulerschema-daysofweektype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="1e4ce-134">The previous child elements are defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

<span data-ttu-id="1e4ce-135">Для разработки сценариев еженедельный интервал указывается с помощью свойства [**виклитригжер. виксинтервал**](weeklytrigger-weeksinterval.md) .</span><span class="sxs-lookup"><span data-stu-id="1e4ce-135">For scripting development, the weekly interval is specified using the [**WeeklyTrigger.WeeksInterval**](weeklytrigger-weeksinterval.md) property.</span></span>

<span data-ttu-id="1e4ce-136">Для разработки на C++ еженедельный интервал задается с помощью свойства [**ивиклитригжер:: виксинтервал**](/windows/desktop/api/taskschd/nf-taskschd-iweeklytrigger-get_weeksinterval) .</span><span class="sxs-lookup"><span data-stu-id="1e4ce-136">For C++ development, the weekly interval is specified using the [**IWeeklyTrigger::WeeksInterval**](/windows/desktop/api/taskschd/nf-taskschd-iweeklytrigger-get_weeksinterval) property.</span></span>

## <a name="examples"></a><span data-ttu-id="1e4ce-137">Примеры</span><span class="sxs-lookup"><span data-stu-id="1e4ce-137">Examples</span></span>

<span data-ttu-id="1e4ce-138">Следующий XML-код определяет ежедневный триггер календаря, который запускает задачу с понедельника по пятницу (в 8:00 AM) каждую неделю.</span><span class="sxs-lookup"><span data-stu-id="1e4ce-138">The following XML defines a daily calendar trigger that starts a task Monday through Friday ( at 8:00 AM) every week.</span></span>


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



<span data-ttu-id="1e4ce-139">Полный пример XML-кода для задачи, использующей еженедельный триггер, см. в разделе [Пример еженедельного триггера (XML)](weekly-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="1e4ce-139">For a complete example of the XML for a task that uses a weekly trigger, see [Weekly Trigger Example (XML)](weekly-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1e4ce-140">Требования</span><span class="sxs-lookup"><span data-stu-id="1e4ce-140">Requirements</span></span>



| <span data-ttu-id="1e4ce-141">Требование</span><span class="sxs-lookup"><span data-stu-id="1e4ce-141">Requirement</span></span> | <span data-ttu-id="1e4ce-142">Значение</span><span class="sxs-lookup"><span data-stu-id="1e4ce-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1e4ce-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1e4ce-143">Minimum supported client</span></span><br/> | <span data-ttu-id="1e4ce-144">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1e4ce-144">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1e4ce-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1e4ce-145">Minimum supported server</span></span><br/> | <span data-ttu-id="1e4ce-146">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1e4ce-146">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1e4ce-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1e4ce-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e4ce-148">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="1e4ce-148">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="1e4ce-149">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="1e4ce-149">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





