---
title: Сложный тип Календартригжертипе
description: Определяет дочерние элементы и сведения о последовательности для элементов календаря.
ms.assetid: bf0d964e-aff2-4807-b086-c504f8963663
keywords:
- планировщик задач сложного типа Календартригжертипе
topic_type:
- apiref
api_name:
- calendarTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a891f60d46f8826faed1cc4b95e4c55f6efa4f7f
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734169"
---
# <a name="calendartriggertype-complex-type"></a><span data-ttu-id="3a8c2-104">Сложный тип Календартригжертипе</span><span class="sxs-lookup"><span data-stu-id="3a8c2-104">calendarTriggerType Complex Type</span></span>

<span data-ttu-id="3a8c2-105">Определяет дочерние элементы и сведения о последовательности для элементов календаря.</span><span class="sxs-lookup"><span data-stu-id="3a8c2-105">Defines the child elements and sequencing information for calendar elements.</span></span>

``` syntax
<xs:complexType name="calendarTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="RandomDelay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
                <xs:choice>
                    <xs:element name="ScheduleByDay"
                        type="dailyScheduleType"
                     />
                    <xs:element name="ScheduleByWeek"
                        type="weeklyScheduleType"
                     />
                    <xs:element name="ScheduleByMonth"
                        type="monthlyScheduleType"
                     />
                    <xs:element name="ScheduleByMonthDayOfWeek"
                        type="monthlyDayOfWeekScheduleType"
                     />
                </xs:choice>
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="3a8c2-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="3a8c2-106">Child elements</span></span>



| <span data-ttu-id="3a8c2-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="3a8c2-107">Element</span></span>                                                                                                      | <span data-ttu-id="3a8c2-108">Тип</span><span class="sxs-lookup"><span data-stu-id="3a8c2-108">Type</span></span>                                                                                                 | <span data-ttu-id="3a8c2-109">Описание</span><span class="sxs-lookup"><span data-stu-id="3a8c2-109">Description</span></span>                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3a8c2-110">**рандомделай**</span><span class="sxs-lookup"><span data-stu-id="3a8c2-110">**RandomDelay**</span></span>](taskschedulerschema-randomdelay-calendartriggertype-element.md)                           | <span data-ttu-id="3a8c2-111">длительность</span><span class="sxs-lookup"><span data-stu-id="3a8c2-111">duration</span></span>                                                                                             | <span data-ttu-id="3a8c2-112">Содержит время задержки, которое случайным образом добавляется к времени начала триггера.</span><span class="sxs-lookup"><span data-stu-id="3a8c2-112">Contains the delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="3a8c2-113">Формат этой строки — `P<days>DT<hours>H<minutes>M<seconds>S` (например, P2DT5S имеет 2 дня, 5 секунд задержки).</span><span class="sxs-lookup"><span data-stu-id="3a8c2-113">The format for this string is `P<days>DT<hours>H<minutes>M<seconds>S` (for example, P2DT5S is a 2 day, 5 second delay).</span></span><br/> |
| [<span data-ttu-id="3a8c2-114">**счедулебидай**</span><span class="sxs-lookup"><span data-stu-id="3a8c2-114">**ScheduleByDay**</span></span>](taskschedulerschema-schedulebyday-calendartriggertype-element.md)                       | [<span data-ttu-id="3a8c2-115">**даилисчедулетипе**</span><span class="sxs-lookup"><span data-stu-id="3a8c2-115">**dailyScheduleType**</span></span>](taskschedulerschema-dailyscheduletype-complextype.md)                       | <span data-ttu-id="3a8c2-116">Указывает ежедневное расписание.</span><span class="sxs-lookup"><span data-stu-id="3a8c2-116">Specifies a daily schedule.</span></span> <span data-ttu-id="3a8c2-117">Например, задача запускается каждый день, каждый второй день, каждый третий день и т. д.</span><span class="sxs-lookup"><span data-stu-id="3a8c2-117">For example, the task starts every day, every-other day, every third day, and so on.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="3a8c2-118">**счедулебимонс**</span><span class="sxs-lookup"><span data-stu-id="3a8c2-118">**ScheduleByMonth**</span></span>](taskschedulerschema-schedulebymonth-calendartriggertype-element.md)                   | [<span data-ttu-id="3a8c2-119">**монслисчедулетипе**</span><span class="sxs-lookup"><span data-stu-id="3a8c2-119">**monthlyScheduleType**</span></span>](taskschedulerschema-monthlyscheduletype-complextype.md)                   | <span data-ttu-id="3a8c2-120">Указывает ежемесячное расписание.</span><span class="sxs-lookup"><span data-stu-id="3a8c2-120">Specifies a monthly schedule.</span></span> <span data-ttu-id="3a8c2-121">Например, задача начинается в 8:00 в определенные дни месяца в определенные месяцы.</span><span class="sxs-lookup"><span data-stu-id="3a8c2-121">For example, the task starts at 8:00 AM on specific days of the month on specific months.</span></span> <br/>                                                                                                       |
| [<span data-ttu-id="3a8c2-122">**счедулебимонсдайофвик**</span><span class="sxs-lookup"><span data-stu-id="3a8c2-122">**ScheduleByMonthDayOfWeek**</span></span>](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) | [<span data-ttu-id="3a8c2-123">**монслидайофвиксчедулетипе**</span><span class="sxs-lookup"><span data-stu-id="3a8c2-123">**monthlyDayOfWeekScheduleType**</span></span>](taskschedulerschema-monthlydayofweekscheduletype-complextype.md) | <span data-ttu-id="3a8c2-124">Указывает триггер, который запускает задание в месячном расписании недели.</span><span class="sxs-lookup"><span data-stu-id="3a8c2-124">Specifies a trigger that starts a job on a monthly day-of-week schedule.</span></span> <span data-ttu-id="3a8c2-125">Например, задача запускается в определенные дни недели, недели месяца и месяцы года.</span><span class="sxs-lookup"><span data-stu-id="3a8c2-125">For example, the task starts on specific days of the week, weeks of the month, and months of the year.</span></span> <br/>                                               |
| [<span data-ttu-id="3a8c2-126">**счедулебивик**</span><span class="sxs-lookup"><span data-stu-id="3a8c2-126">**ScheduleByWeek**</span></span>](taskschedulerschema-schedulebyweek-calendartriggertype-element.md)                     | [<span data-ttu-id="3a8c2-127">**виклисчедулетипе**</span><span class="sxs-lookup"><span data-stu-id="3a8c2-127">**weeklyScheduleType**</span></span>](taskschedulerschema-weeklyscheduletype-complextype.md)                     | <span data-ttu-id="3a8c2-128">Указывает еженедельное расписание.</span><span class="sxs-lookup"><span data-stu-id="3a8c2-128">Specifies a weekly schedule.</span></span> <span data-ttu-id="3a8c2-129">Например, задача начинается в 8:00 в конкретный день недели или в конкретный день недели, каждую неделю.</span><span class="sxs-lookup"><span data-stu-id="3a8c2-129">For example, the task starts at 8:00 AM on a specific day of the week every week or on a specific day of the week every other week.</span></span> <br/>                                                              |



## <a name="remarks"></a><span data-ttu-id="3a8c2-130">Замечания</span><span class="sxs-lookup"><span data-stu-id="3a8c2-130">Remarks</span></span>

<span data-ttu-id="3a8c2-131">Помимо дочернего элемента, определенного здесь, элемент [**календартригжер**](taskschedulerschema-calendartrigger-triggergroup-element.md) также использует дочерние элементы, определенные сложным типом [**тригжербасетипе**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="3a8c2-131">In addition to the child element defined here, the [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md) element also uses the child elements defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a8c2-132">Требования</span><span class="sxs-lookup"><span data-stu-id="3a8c2-132">Requirements</span></span>



| <span data-ttu-id="3a8c2-133">Требование</span><span class="sxs-lookup"><span data-stu-id="3a8c2-133">Requirement</span></span> | <span data-ttu-id="3a8c2-134">Значение</span><span class="sxs-lookup"><span data-stu-id="3a8c2-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3a8c2-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3a8c2-135">Minimum supported client</span></span><br/> | <span data-ttu-id="3a8c2-136">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3a8c2-136">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3a8c2-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3a8c2-137">Minimum supported server</span></span><br/> | <span data-ttu-id="3a8c2-138">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3a8c2-138">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3a8c2-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3a8c2-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a8c2-140">планировщик задач сложные типы схемы</span><span class="sxs-lookup"><span data-stu-id="3a8c2-140">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="3a8c2-141">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="3a8c2-141">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





