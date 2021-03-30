---
title: Weeks (Монслидайофвиксчедулетипе), элемент
description: Указывает недели месяца, в которых выполняется задача.
ms.assetid: c126d1e2-6e60-4067-9fc2-86c9522cce5d
keywords:
- Элемент weeks планировщик задач
topic_type:
- apiref
api_name:
- Weeks
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e032b936353d2c89a84b5da684f681ea3c2b6d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803634"
---
# <a name="weeks-monthlydayofweekscheduletype-element"></a><span data-ttu-id="24439-104">Weeks (Монслидайофвиксчедулетипе), элемент</span><span class="sxs-lookup"><span data-stu-id="24439-104">Weeks (monthlyDayOfWeekScheduleType) Element</span></span>

<span data-ttu-id="24439-105">Указывает недели месяца, в которых выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="24439-105">Specifies the weeks of the month in which the task is run.</span></span>

``` syntax
<xs:element name="Weeks"
    type="weeksType"
 />
```

<span data-ttu-id="24439-106">Элемент **weeks** определяется сложным типом [**монслидайофвиксчедулетипе**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="24439-106">The **Weeks** element is defined by the [**monthlyDayOfWeekScheduleType**](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="24439-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="24439-107">Parent element</span></span>



| <span data-ttu-id="24439-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="24439-108">Element</span></span>                                                                                                      | <span data-ttu-id="24439-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="24439-109">Derived from</span></span>                                                                                         | <span data-ttu-id="24439-110">Описание</span><span class="sxs-lookup"><span data-stu-id="24439-110">Description</span></span>                                                                         |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="24439-111">**счедулебимонсдайофвик**</span><span class="sxs-lookup"><span data-stu-id="24439-111">**ScheduleByMonthDayOfWeek**</span></span>](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [<span data-ttu-id="24439-112">**монслидайофвиксчедулетипе**</span><span class="sxs-lookup"><span data-stu-id="24439-112">**monthlyDayOfWeekScheduleType**</span></span>](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | <span data-ttu-id="24439-113">Указывает триггер, который запускает задание в месячном расписании недели.</span><span class="sxs-lookup"><span data-stu-id="24439-113">Specifies a trigger that starts a job on a monthly day-of-week schedule.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="24439-114">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="24439-114">Child elements</span></span>



| <span data-ttu-id="24439-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="24439-115">Element</span></span>                                                    | <span data-ttu-id="24439-116">Тип</span><span class="sxs-lookup"><span data-stu-id="24439-116">Type</span></span>                                                        | <span data-ttu-id="24439-117">Описание</span><span class="sxs-lookup"><span data-stu-id="24439-117">Description</span></span>                                        |
|------------------------------------------------------------|-------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="24439-118">**Неделя**</span><span class="sxs-lookup"><span data-stu-id="24439-118">**Week**</span></span>](taskschedulerschema-week-weekstype-element.md) | [<span data-ttu-id="24439-119">**виктипе**</span><span class="sxs-lookup"><span data-stu-id="24439-119">**weekType**</span></span>](taskschedulerschema-weektype-simpletype.md) | <span data-ttu-id="24439-120">Указывает конкретную неделю месяца.</span><span class="sxs-lookup"><span data-stu-id="24439-120">Specifies a specific week of the month.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="24439-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="24439-121">Remarks</span></span>

<span data-ttu-id="24439-122">Для разработки сценариев недели месяца указываются с помощью свойства [**монслидовтригжер. виксофмонс**](monthlydowtrigger-weeksofmonth.md) .</span><span class="sxs-lookup"><span data-stu-id="24439-122">For scripting development, the weeks of the month are specified using the [**MonthlyDOWTrigger.WeeksOfMonth**](monthlydowtrigger-weeksofmonth.md) property.</span></span>

<span data-ttu-id="24439-123">Для разработки на C++ недели месяца указываются с помощью свойства [**имонслидовтригжер:: виксофмонс**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_weeksofmonth) .</span><span class="sxs-lookup"><span data-stu-id="24439-123">For C++ development, the weeks of the month are specified using the [**IMonthlyDOWTrigger::WeeksOfMonth**](/windows/desktop/api/taskschd/nf-taskschd-imonthlydowtrigger-get_weeksofmonth) property.</span></span>

<span data-ttu-id="24439-124">При указании недель месяца используйте 1-4, чтобы указать первые четыре недели месяца, или используйте строку "Last", чтобы указать последнюю неделю независимо от недели.</span><span class="sxs-lookup"><span data-stu-id="24439-124">When specifying the weeks of the month, use 1-4 to specify the first four weeks of the month or use the string "Last" to indicate the last week regardless of which week it is.</span></span>

## <a name="examples"></a><span data-ttu-id="24439-125">Примеры</span><span class="sxs-lookup"><span data-stu-id="24439-125">Examples</span></span>

<span data-ttu-id="24439-126">Следующий XML-код определяет месячный календарь дня недели, который запускает задачу в понедельник первой недели для каждого месяца года.</span><span class="sxs-lookup"><span data-stu-id="24439-126">The following XML defines a monthly day-of-week calendar that starts the task on Monday of the first week for each month of the year.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="24439-127">Требования</span><span class="sxs-lookup"><span data-stu-id="24439-127">Requirements</span></span>



| <span data-ttu-id="24439-128">Требование</span><span class="sxs-lookup"><span data-stu-id="24439-128">Requirement</span></span> | <span data-ttu-id="24439-129">Значение</span><span class="sxs-lookup"><span data-stu-id="24439-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="24439-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="24439-130">Minimum supported client</span></span><br/> | <span data-ttu-id="24439-131">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="24439-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="24439-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="24439-132">Minimum supported server</span></span><br/> | <span data-ttu-id="24439-133">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="24439-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="24439-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="24439-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24439-135">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="24439-135">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="24439-136">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="24439-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





