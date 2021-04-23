---
title: DaysOfMonth (Монслисчедулетипе), элемент
description: Указывает дни месяца, в которые выполняется задача.
ms.assetid: 62f28f44-b3d8-414e-80d4-f4d8bd3c4527
keywords:
- планировщик задач элемента DaysOfMonth
topic_type:
- apiref
api_name:
- DaysOfMonth
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 38c2106f8d612ee27dc1297023a59b531fa9548d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682140"
---
# <a name="daysofmonth-monthlyscheduletype-element"></a><span data-ttu-id="539db-104">DaysOfMonth (Монслисчедулетипе), элемент</span><span class="sxs-lookup"><span data-stu-id="539db-104">DaysOfMonth (monthlyScheduleType) Element</span></span>

<span data-ttu-id="539db-105">Указывает дни месяца, в которые выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="539db-105">Specifies the days of the month during which the task runs.</span></span>

``` syntax
<xs:element name="DaysOfMonth"
    type="daysOfMonthType"
 />
```

<span data-ttu-id="539db-106">Элемент **DaysOfMonth** определяется сложным типом [**монслисчедулетипе**](taskschedulerschema-monthlyscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="539db-106">The **DaysOfMonth** element is defined by the [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="539db-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="539db-107">Parent element</span></span>



| <span data-ttu-id="539db-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="539db-108">Element</span></span>                                                                                    | <span data-ttu-id="539db-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="539db-109">Derived from</span></span>                                                                                         | <span data-ttu-id="539db-110">Описание</span><span class="sxs-lookup"><span data-stu-id="539db-110">Description</span></span>                                                                          |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="539db-111">**счедулебимонс**</span><span class="sxs-lookup"><span data-stu-id="539db-111">**ScheduleByMonth**</span></span>](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) | [<span data-ttu-id="539db-112">**монслидайофвиксчедулетипе**</span><span class="sxs-lookup"><span data-stu-id="539db-112">**monthlyDayOfWeekScheduleType**</span></span>](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | <span data-ttu-id="539db-113">Указывает триггер, который запускает задание для ежемесячного расписания недели.</span><span class="sxs-lookup"><span data-stu-id="539db-113">Specifies a trigger that starts a job for a monthly day-of-week schedule.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="539db-114">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="539db-114">Child elements</span></span>



| <span data-ttu-id="539db-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="539db-115">Element</span></span>                                                        | <span data-ttu-id="539db-116">Тип</span><span class="sxs-lookup"><span data-stu-id="539db-116">Type</span></span>                                                                    | <span data-ttu-id="539db-117">Описание</span><span class="sxs-lookup"><span data-stu-id="539db-117">Description</span></span>                                                         |
|----------------------------------------------------------------|-------------------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="539db-118">**День**</span><span class="sxs-lookup"><span data-stu-id="539db-118">**Day**</span></span>](taskschedulerschema-day-daysofmonthtype-element.md) | [<span data-ttu-id="539db-119">**дайофмонстипе**</span><span class="sxs-lookup"><span data-stu-id="539db-119">**dayOfMonthType**</span></span>](taskschedulerschema-dayofmonthtype-simpletype.md) | <span data-ttu-id="539db-120">Указывает день месяца, в который выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="539db-120">Specifies a day of the month during which the task runs.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="539db-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="539db-121">Remarks</span></span>

<span data-ttu-id="539db-122">Для разработки скриптов дни месяца для расписания задаются с помощью свойства [**монслитригжер. DaysOfMonth**](monthlytrigger-daysofmonth.md) .</span><span class="sxs-lookup"><span data-stu-id="539db-122">For script development, the days of the month for the schedule are specified using the [**MonthlyTrigger.DaysOfMonth**](monthlytrigger-daysofmonth.md) property.</span></span>

<span data-ttu-id="539db-123">Для разработки на C++ дни месяца для расписания задаются с помощью свойства [**имонслитригжер::D айсофмонс**](/windows/desktop/api/taskschd/nf-taskschd-imonthlytrigger-get_daysofmonth) .</span><span class="sxs-lookup"><span data-stu-id="539db-123">For C++ development, the days of the month for the schedule are specified using the [**IMonthlyTrigger::DaysOfMonth**](/windows/desktop/api/taskschd/nf-taskschd-imonthlytrigger-get_daysofmonth) property.</span></span>

<span data-ttu-id="539db-124">Дочерний элемент должен повторяться для каждого дня месяца, который будет выполняться задачей.</span><span class="sxs-lookup"><span data-stu-id="539db-124">The child element must be repeated for each day of the month the task is to run.</span></span>

## <a name="examples"></a><span data-ttu-id="539db-125">Примеры</span><span class="sxs-lookup"><span data-stu-id="539db-125">Examples</span></span>

<span data-ttu-id="539db-126">Следующий XML-код определяет месячный триггер календаря, который запускает задачу (в 8:30 AM) в 1-й день каждого месяца.</span><span class="sxs-lookup"><span data-stu-id="539db-126">The following XML defines a monthly calendar trigger that starts a task (at 8:30 AM) on the 1st day of every month.</span></span>


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByMonth>
        <DaysOfMonth>
            <Day>1</Day>  
        </DaysOfMonth>
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
    </ScheduleByMonth>
</CalendarTrigger>
```



## <a name="requirements"></a><span data-ttu-id="539db-127">Требования</span><span class="sxs-lookup"><span data-stu-id="539db-127">Requirements</span></span>



| <span data-ttu-id="539db-128">Требование</span><span class="sxs-lookup"><span data-stu-id="539db-128">Requirement</span></span> | <span data-ttu-id="539db-129">Значение</span><span class="sxs-lookup"><span data-stu-id="539db-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="539db-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="539db-130">Minimum supported client</span></span><br/> | <span data-ttu-id="539db-131">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="539db-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="539db-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="539db-132">Minimum supported server</span></span><br/> | <span data-ttu-id="539db-133">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="539db-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="539db-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="539db-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="539db-135">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="539db-135">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="539db-136">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="539db-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





