---
title: Виксинтервал (Виклисчедулетипе), элемент
description: Указывает интервал между неделями в расписании.
ms.assetid: 6cbf1e7e-a695-4012-97fd-fe3360c362c4
keywords:
- планировщик задач элемента Виксинтервал
topic_type:
- apiref
api_name:
- WeeksInterval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 747ca4b73ff18bdb3e29d8b909d72b8d2367d89b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415976"
---
# <a name="weeksinterval-weeklyscheduletype-element"></a><span data-ttu-id="12985-104">Виксинтервал (Виклисчедулетипе), элемент</span><span class="sxs-lookup"><span data-stu-id="12985-104">WeeksInterval (weeklyScheduleType) Element</span></span>

<span data-ttu-id="12985-105">Указывает интервал между неделями в расписании.</span><span class="sxs-lookup"><span data-stu-id="12985-105">Specifies the interval between the weeks in the schedule.</span></span>

``` syntax
<xs:element name="WeeksInterval"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="unsignedByte"
        >
            <xs:minInclusive
                value="1"
             />
            <xs:maxInclusive
                value="52"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="12985-106">Элемент определяется сложным типом [**виклисчедулетипе**](taskschedulerschema-weeklyscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="12985-106">The element is defined by the [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="12985-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="12985-107">Parent element</span></span>



| <span data-ttu-id="12985-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="12985-108">Element</span></span>                                                                                  | <span data-ttu-id="12985-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="12985-109">Derived from</span></span>                                                                     | <span data-ttu-id="12985-110">Описание</span><span class="sxs-lookup"><span data-stu-id="12985-110">Description</span></span>                             |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="12985-111">**счедулебивик**</span><span class="sxs-lookup"><span data-stu-id="12985-111">**ScheduleByWeek**</span></span>](taskschedulerschema-schedulebyweek-calendartriggertype-element.md) | [<span data-ttu-id="12985-112">**виклисчедулетипе**</span><span class="sxs-lookup"><span data-stu-id="12985-112">**weeklyScheduleType**</span></span>](taskschedulerschema-weeklyscheduletype-complextype.md) | <span data-ttu-id="12985-113">Указывает еженедельное расписание.</span><span class="sxs-lookup"><span data-stu-id="12985-113">Specifies a weekly schedule.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="12985-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="12985-114">Remarks</span></span>

<span data-ttu-id="12985-115">Для разработки сценариев еженедельный интервал указывается с помощью свойства [**виклитригжер. виксинтервал**](weeklytrigger-weeksinterval.md) .</span><span class="sxs-lookup"><span data-stu-id="12985-115">For scripting development, the weekly interval is specified using the [**WeeklyTrigger.WeeksInterval**](weeklytrigger-weeksinterval.md) property.</span></span>

<span data-ttu-id="12985-116">Для разработки на C++ еженедельный интервал задается с помощью свойства [**ивиклитригжер:: виксинтервал**](/windows/desktop/api/taskschd/nf-taskschd-iweeklytrigger-get_weeksinterval) .</span><span class="sxs-lookup"><span data-stu-id="12985-116">For C++ development, the weekly interval is specified using the [**IWeeklyTrigger::WeeksInterval**](/windows/desktop/api/taskschd/nf-taskschd-iweeklytrigger-get_weeksinterval) property.</span></span>

## <a name="examples"></a><span data-ttu-id="12985-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="12985-117">Examples</span></span>

<span data-ttu-id="12985-118">Следующий XML-код определяет еженедельный календарный триггер, который запускает задачу с понедельника по пятницу (в 8:00 AM) каждую неделю.</span><span class="sxs-lookup"><span data-stu-id="12985-118">The following XML defines a weekly calendar trigger that starts a task Monday through Friday ( at 8:00 AM) every week.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="12985-119">Требования</span><span class="sxs-lookup"><span data-stu-id="12985-119">Requirements</span></span>



| <span data-ttu-id="12985-120">Требование</span><span class="sxs-lookup"><span data-stu-id="12985-120">Requirement</span></span> | <span data-ttu-id="12985-121">Значение</span><span class="sxs-lookup"><span data-stu-id="12985-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="12985-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="12985-122">Minimum supported client</span></span><br/> | <span data-ttu-id="12985-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="12985-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="12985-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="12985-124">Minimum supported server</span></span><br/> | <span data-ttu-id="12985-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="12985-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="12985-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="12985-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12985-127">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="12985-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="12985-128">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="12985-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





