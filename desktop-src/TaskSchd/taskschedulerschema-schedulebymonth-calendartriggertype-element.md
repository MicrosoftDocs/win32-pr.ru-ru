---
title: Счедулебимонс (Календартригжертипе), элемент
description: Указывает ежемесячное расписание.
ms.assetid: 3a23f4d0-bdaf-4f2a-81c6-8652a0849fc8
keywords:
- планировщик задач элемента Счедулебимонс
topic_type:
- apiref
api_name:
- ScheduleByMonth
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6fda84a1cd4373f7988fa66a5ad70c97dd371d4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137019"
---
# <a name="schedulebymonth-calendartriggertype-element"></a><span data-ttu-id="508a5-104">Счедулебимонс (Календартригжертипе), элемент</span><span class="sxs-lookup"><span data-stu-id="508a5-104">ScheduleByMonth (calendarTriggerType) Element</span></span>

<span data-ttu-id="508a5-105">Указывает ежемесячное расписание.</span><span class="sxs-lookup"><span data-stu-id="508a5-105">Specifies a monthly schedule.</span></span> <span data-ttu-id="508a5-106">Например, задача начинается в 8:00 в определенные дни месяца в определенные месяцы.</span><span class="sxs-lookup"><span data-stu-id="508a5-106">For example, the task starts at 8:00 AM on specific days of the month on specific months.</span></span>

``` syntax
<xs:element name="ScheduleByMonth"
    type="monthlyScheduleType"
 />
```

<span data-ttu-id="508a5-107">Элемент **счедулебимонс** определяется сложным типом [**календартригжертипе**](taskschedulerschema-calendartriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="508a5-107">The **ScheduleByMonth** element is defined by the [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="508a5-108">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="508a5-108">Parent element</span></span>



| <span data-ttu-id="508a5-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="508a5-109">Element</span></span>                                                                             | <span data-ttu-id="508a5-110">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="508a5-110">Derived from</span></span>                                                                       | <span data-ttu-id="508a5-111">Описание</span><span class="sxs-lookup"><span data-stu-id="508a5-111">Description</span></span>                                                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="508a5-112">**календартригжер**</span><span class="sxs-lookup"><span data-stu-id="508a5-112">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md) | [<span data-ttu-id="508a5-113">**календартригжертипе**</span><span class="sxs-lookup"><span data-stu-id="508a5-113">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md) | <span data-ttu-id="508a5-114">Задает ежедневный, еженедельный, ежемесячный или ежемесячный триггер (DOW) в день недели.</span><span class="sxs-lookup"><span data-stu-id="508a5-114">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="508a5-115">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="508a5-115">Child elements</span></span>



| <span data-ttu-id="508a5-116">Элемент</span><span class="sxs-lookup"><span data-stu-id="508a5-116">Element</span></span>                                                                                                  | <span data-ttu-id="508a5-117">Тип</span><span class="sxs-lookup"><span data-stu-id="508a5-117">Type</span></span>                                                                       | <span data-ttu-id="508a5-118">Описание</span><span class="sxs-lookup"><span data-stu-id="508a5-118">Description</span></span>                                                             |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="508a5-119">**DaysOfMonth (Монслисчедулетипе)**</span><span class="sxs-lookup"><span data-stu-id="508a5-119">**DaysOfMonth (monthlyScheduleType)**</span></span>](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) | [<span data-ttu-id="508a5-120">**дайсофмонстипе**</span><span class="sxs-lookup"><span data-stu-id="508a5-120">**daysOfMonthType**</span></span>](taskschedulerschema-daysofmonthtype-complextype.md) | <span data-ttu-id="508a5-121">Указывает дни месяца, в которые выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="508a5-121">Specifies the days of the month during which the task runs.</span></span><br/>  |
| [<span data-ttu-id="508a5-122">**Месяцы (Монслисчедулетипе)**</span><span class="sxs-lookup"><span data-stu-id="508a5-122">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)           | [<span data-ttu-id="508a5-123">**монсстипе**</span><span class="sxs-lookup"><span data-stu-id="508a5-123">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md)           | <span data-ttu-id="508a5-124">Указывает месяцы года, в течение которых выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="508a5-124">Specifies the months of the year during which the task runs.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="508a5-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="508a5-125">Remarks</span></span>

<span data-ttu-id="508a5-126">Время дня, когда начинается задача, задается элементом [**стартбаундари**](taskschedulerschema-startboundary-triggerbasetype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="508a5-126">The time of day that the task is started is set by the [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element.</span></span>

<span data-ttu-id="508a5-127">Для разработки скриптов ежемесячный триггер указывается с помощью объекта [**монслитригжер**](monthlytrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="508a5-127">For script development, a monthly trigger is specified using the [**MonthlyTrigger**](monthlytrigger.md) object.</span></span>

<span data-ttu-id="508a5-128">Для разработки на C++ ежемесячный триггер указывается с помощью интерфейса [**имонслитригжер**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger) .</span><span class="sxs-lookup"><span data-stu-id="508a5-128">For C++ development, a monthly trigger is specified using the [**IMonthlyTrigger**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger) interface.</span></span>

<span data-ttu-id="508a5-129">Перечисленные ниже дочерние элементы определяются сложными типами элементов [**монслисчедулетипе**](taskschedulerschema-monthlyscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="508a5-129">The child elements listed below are defined by the [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) complex element types.</span></span>

## <a name="examples"></a><span data-ttu-id="508a5-130">Примеры</span><span class="sxs-lookup"><span data-stu-id="508a5-130">Examples</span></span>

<span data-ttu-id="508a5-131">Следующий XML-код определяет месячный триггер календаря, который запускает задачу (в 8:00 AM) на первый и 15-й день каждого месяца года.</span><span class="sxs-lookup"><span data-stu-id="508a5-131">The following XML defines a monthly calendar trigger that starts a task ( at 8:00 AM) on the 1st and 15th day of every month of the year.</span></span>


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByMonth>
        <DaysOfMonth>
            <Day>1</Day>
            <Day>15</Day>
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
        </Months>
    </ScheduleByMonth>
</CalendarTrigger>
```



## <a name="requirements"></a><span data-ttu-id="508a5-132">Требования</span><span class="sxs-lookup"><span data-stu-id="508a5-132">Requirements</span></span>



| <span data-ttu-id="508a5-133">Требование</span><span class="sxs-lookup"><span data-stu-id="508a5-133">Requirement</span></span> | <span data-ttu-id="508a5-134">Значение</span><span class="sxs-lookup"><span data-stu-id="508a5-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="508a5-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="508a5-135">Minimum supported client</span></span><br/> | <span data-ttu-id="508a5-136">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="508a5-136">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="508a5-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="508a5-137">Minimum supported server</span></span><br/> | <span data-ttu-id="508a5-138">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="508a5-138">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="508a5-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="508a5-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="508a5-140">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="508a5-140">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="508a5-141">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="508a5-141">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





