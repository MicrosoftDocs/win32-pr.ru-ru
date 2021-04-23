---
title: Счедулебидай (Календартригжертипе), элемент
description: Указывает ежедневное расписание.
ms.assetid: 5a6097ce-a855-4b08-84c5-71f06343805e
keywords:
- планировщик задач ежедневного триггера, XML-элемент
- планировщик задач элемента Счедулебидай
topic_type:
- apiref
api_name:
- ScheduleByDay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 614777ede63605dc7ed6936bda952c6071bda371
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989145"
---
# <a name="schedulebyday-calendartriggertype-element"></a><span data-ttu-id="74b67-105">Счедулебидай (Календартригжертипе), элемент</span><span class="sxs-lookup"><span data-stu-id="74b67-105">ScheduleByDay (calendarTriggerType) Element</span></span>

<span data-ttu-id="74b67-106">Указывает ежедневное расписание.</span><span class="sxs-lookup"><span data-stu-id="74b67-106">Specifies a daily schedule.</span></span> <span data-ttu-id="74b67-107">Например, задача начинается в 8:00 раз в день, каждые-каждый день, каждый третий день и т. д.</span><span class="sxs-lookup"><span data-stu-id="74b67-107">For example, the task starts at 8:00 AM every day, every-other day, every third day, and so on.</span></span>

``` syntax
<xs:element name="ScheduleByDay"
    type="dailyScheduleType"
 />
```

<span data-ttu-id="74b67-108">Элемент **счедулебидай** определяется сложным типом [**календартригжертипе**](taskschedulerschema-calendartriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="74b67-108">The **ScheduleByDay** element is defined by the [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="74b67-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="74b67-109">Parent element</span></span>



| <span data-ttu-id="74b67-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="74b67-110">Element</span></span>                                                                             | <span data-ttu-id="74b67-111">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="74b67-111">Derived from</span></span>                                                                       | <span data-ttu-id="74b67-112">Описание</span><span class="sxs-lookup"><span data-stu-id="74b67-112">Description</span></span>                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="74b67-113">**календартригжер**</span><span class="sxs-lookup"><span data-stu-id="74b67-113">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md) | [<span data-ttu-id="74b67-114">**календартригжертипе**</span><span class="sxs-lookup"><span data-stu-id="74b67-114">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md) | <span data-ttu-id="74b67-115">Задает ежедневный, еженедельный, ежемесячный или ежемесячный триггер (DOW) в день недели.</span><span class="sxs-lookup"><span data-stu-id="74b67-115">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="74b67-116">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="74b67-116">Child elements</span></span>



| <span data-ttu-id="74b67-117">Элемент</span><span class="sxs-lookup"><span data-stu-id="74b67-117">Element</span></span>                                                                            | <span data-ttu-id="74b67-118">Тип</span><span class="sxs-lookup"><span data-stu-id="74b67-118">Type</span></span>             | <span data-ttu-id="74b67-119">Описание</span><span class="sxs-lookup"><span data-stu-id="74b67-119">Description</span></span>                                                         |
|------------------------------------------------------------------------------------|------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="74b67-120">**дайсинтервал**</span><span class="sxs-lookup"><span data-stu-id="74b67-120">**DaysInterval**</span></span>](taskschedulerschema-daysinterval-dailyscheduletype-element.md) | <span data-ttu-id="74b67-121">**unsignedByte**</span><span class="sxs-lookup"><span data-stu-id="74b67-121">**unsignedByte**</span></span> | <span data-ttu-id="74b67-122">Указывает интервал между днями в расписании.</span><span class="sxs-lookup"><span data-stu-id="74b67-122">Specifies the interval between the days in the schedule.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="74b67-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="74b67-123">Remarks</span></span>

<span data-ttu-id="74b67-124">Перечисленный выше дочерний элемент определяется сложными типами элементов [**даилисчедулетипе**](taskschedulerschema-dailyscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="74b67-124">The child element listed previously is defined by the [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md) complex element types.</span></span>

<span data-ttu-id="74b67-125">Время дня, когда начинается задача, задается элементом [**стартбаундари**](taskschedulerschema-startboundary-triggerbasetype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="74b67-125">The time of day that the task is started is set by the [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element.</span></span>

<span data-ttu-id="74b67-126">Для разработки сценариев ежедневный триггер указывается с помощью объекта [**даилитригжер**](weeklytrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="74b67-126">For scripting development, a daily trigger is specified using the [**DailyTrigger**](weeklytrigger.md) object.</span></span>

<span data-ttu-id="74b67-127">Для разработки на C++ ежедневный триггер указывается с помощью интерфейса [**идаилитригжер**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger) .</span><span class="sxs-lookup"><span data-stu-id="74b67-127">For C++ development, a daily trigger is specified using the [**IDailyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="74b67-128">Примеры</span><span class="sxs-lookup"><span data-stu-id="74b67-128">Examples</span></span>

<span data-ttu-id="74b67-129">Следующий XML-код определяет ежедневный триггер календаря, который запускает задачу каждый день.</span><span class="sxs-lookup"><span data-stu-id="74b67-129">The following XML defines a daily calendar trigger that starts the task every day.</span></span>


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T00:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByDay>
        <DaysInterval>1</DaysInterval>
    </ScheduleByDay>
</CalendarTrigger>
```



<span data-ttu-id="74b67-130">Полный пример кода XML для задачи, в котором указано ежедневное расписание, см. в разделе [Пример ежедневного триггера (XML)](daily-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="74b67-130">For a complete example of the XML for a task that specifies a daily schedule, see [Daily Trigger Example (XML)](daily-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="74b67-131">Требования</span><span class="sxs-lookup"><span data-stu-id="74b67-131">Requirements</span></span>



| <span data-ttu-id="74b67-132">Требование</span><span class="sxs-lookup"><span data-stu-id="74b67-132">Requirement</span></span> | <span data-ttu-id="74b67-133">Значение</span><span class="sxs-lookup"><span data-stu-id="74b67-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="74b67-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="74b67-134">Minimum supported client</span></span><br/> | <span data-ttu-id="74b67-135">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="74b67-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="74b67-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="74b67-136">Minimum supported server</span></span><br/> | <span data-ttu-id="74b67-137">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="74b67-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="74b67-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="74b67-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74b67-139">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="74b67-139">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="74b67-140">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="74b67-140">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





