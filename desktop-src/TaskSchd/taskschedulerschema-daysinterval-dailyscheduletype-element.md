---
title: Дайсинтервал (Даилисчедулетипе), элемент
description: Указывает интервал между днями в расписании.
ms.assetid: 495ea1c0-37eb-4b12-8241-bfc6489e33ed
keywords:
- планировщик задач элемента Дайсинтервал
topic_type:
- apiref
api_name:
- DaysInterval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 97b50581aa4825b31983a234a5eb47ff7b7b7e06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988298"
---
# <a name="daysinterval-dailyscheduletype-element"></a><span data-ttu-id="38751-104">Дайсинтервал (Даилисчедулетипе), элемент</span><span class="sxs-lookup"><span data-stu-id="38751-104">DaysInterval (dailyScheduleType) Element</span></span>

<span data-ttu-id="38751-105">Указывает интервал между днями в расписании.</span><span class="sxs-lookup"><span data-stu-id="38751-105">Specifies the interval between the days in the schedule.</span></span>

``` syntax
<xs:element name="DaysInterval"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="unsignedInt"
        >
            <xs:minInclusive
                value="1"
             />
            <xs:maxInclusive
                value="365"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="38751-106">Элемент определяется сложным типом [**даилисчедулетипе**](taskschedulerschema-dailyscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="38751-106">The element is defined by the [**dailyScheduleType**](taskschedulerschema-dailyscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="38751-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="38751-107">Parent element</span></span>



| <span data-ttu-id="38751-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="38751-108">Element</span></span>                                                                                | <span data-ttu-id="38751-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="38751-109">Derived from</span></span>                                                                   | <span data-ttu-id="38751-110">Описание</span><span class="sxs-lookup"><span data-stu-id="38751-110">Description</span></span>                            |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|----------------------------------------|
| [<span data-ttu-id="38751-111">**счедулебидай**</span><span class="sxs-lookup"><span data-stu-id="38751-111">**ScheduleByDay**</span></span>](taskschedulerschema-schedulebyday-calendartriggertype-element.md) | [<span data-ttu-id="38751-112">**даилисчедулетипе**</span><span class="sxs-lookup"><span data-stu-id="38751-112">**dailyScheduleType**</span></span>](taskschedulerschema-dailyscheduletype-complextype.md) | <span data-ttu-id="38751-113">Указывает ежедневное расписание.</span><span class="sxs-lookup"><span data-stu-id="38751-113">Specifies a daily schedule.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="38751-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="38751-114">Remarks</span></span>

<span data-ttu-id="38751-115">Для разработки скриптов интервал дней для ежедневного триггера указывается свойством [**даилитригжер. дайсинтервал**](dailytrigger-daysinterval.md) .</span><span class="sxs-lookup"><span data-stu-id="38751-115">For script development, the days interval for a daily trigger is specified by the [**DailyTrigger.DaysInterval**](dailytrigger-daysinterval.md) property.</span></span>

<span data-ttu-id="38751-116">Для разработки на C++ интервал дней для ежедневного триггера задается свойством [**идаилитригжер::D айсинтервал**](/windows/desktop/api/taskschd/nf-taskschd-idailytrigger-get_daysinterval) .</span><span class="sxs-lookup"><span data-stu-id="38751-116">For C++ development, the days interval for a daily trigger is specified by the [**IDailyTrigger::DaysInterval**](/windows/desktop/api/taskschd/nf-taskschd-idailytrigger-get_daysinterval) property.</span></span>

## <a name="examples"></a><span data-ttu-id="38751-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="38751-117">Examples</span></span>

<span data-ttu-id="38751-118">Следующий XML-код определяет ежедневный триггер календаря, который запускает задачу каждый день.</span><span class="sxs-lookup"><span data-stu-id="38751-118">The following XML defines a daily calendar trigger that starts the task every day.</span></span>


```XML
<CalendarTrigger>
    <StartBoundary>2005-01-01T00:00:00</StartBoundary>
    <EndBounadry>2007-01-01T00:00:00</EndBoundary>
    <ScheduleByDay>
        <DaysInterval>1</DaysInterval>
    </ScheduleByDay>
</CalendarTrigger>
```



<span data-ttu-id="38751-119">Полный пример кода XML для задачи, в котором указано ежедневное расписание, см. в разделе [Пример ежедневного триггера (XML)](daily-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="38751-119">For a complete example of the XML for a task that specifies a daily schedule, see [Daily Trigger Example (XML)](daily-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="38751-120">Требования</span><span class="sxs-lookup"><span data-stu-id="38751-120">Requirements</span></span>



| <span data-ttu-id="38751-121">Требование</span><span class="sxs-lookup"><span data-stu-id="38751-121">Requirement</span></span> | <span data-ttu-id="38751-122">Значение</span><span class="sxs-lookup"><span data-stu-id="38751-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="38751-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="38751-123">Minimum supported client</span></span><br/> | <span data-ttu-id="38751-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="38751-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="38751-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="38751-125">Minimum supported server</span></span><br/> | <span data-ttu-id="38751-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="38751-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="38751-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="38751-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38751-128">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="38751-128">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="38751-129">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="38751-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





