---
title: Пятница (Дайсофвиктипе), элемент
description: Указывает, что задача выполняется в пятницу.
ms.assetid: bff85911-d354-4954-8c69-7b6f2ca312d3
keywords:
- Элемент пятницы планировщик задач
topic_type:
- apiref
api_name:
- Friday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 951142e7e925ea71ef1f833be4421351aaea3b35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136927"
---
# <a name="friday-daysofweektype-element"></a><span data-ttu-id="cbd61-104">Пятница (Дайсофвиктипе), элемент</span><span class="sxs-lookup"><span data-stu-id="cbd61-104">Friday (daysOfWeekType) Element</span></span>

<span data-ttu-id="cbd61-105">Указывает, что задача выполняется в пятницу.</span><span class="sxs-lookup"><span data-stu-id="cbd61-105">Specifies that the task runs on Friday.</span></span>

``` syntax
<xs:element name="Friday">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="cbd61-106">Элемент **пятницы** определяется сложным типом [**дайсофвиктипе**](taskschedulerschema-daysofweektype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="cbd61-106">The **Friday** element is defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="cbd61-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="cbd61-107">Parent element</span></span>



| <span data-ttu-id="cbd61-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="cbd61-108">Element</span></span>                                                                                                                  | <span data-ttu-id="cbd61-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="cbd61-109">Derived from</span></span>                                                             | <span data-ttu-id="cbd61-110">Описание</span><span class="sxs-lookup"><span data-stu-id="cbd61-110">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cbd61-111">**DaysOfWeek (Монслидайофвиксчедулетипе)**</span><span class="sxs-lookup"><span data-stu-id="cbd61-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="cbd61-112">**дайсофвиктипе**</span><span class="sxs-lookup"><span data-stu-id="cbd61-112">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="cbd61-113">Указывает дни недели, в которых задача выполняется для ежемесячного расписания недели.</span><span class="sxs-lookup"><span data-stu-id="cbd61-113">Specifies the days of the week in which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="cbd61-114">**DaysOfWeek (Виклисчедулетипе)**</span><span class="sxs-lookup"><span data-stu-id="cbd61-114">**DaysOfWeek (weeklyScheduleType)**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [<span data-ttu-id="cbd61-115">**дайсофвиктипе**</span><span class="sxs-lookup"><span data-stu-id="cbd61-115">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="cbd61-116">Указывает дни недели, в которых задача выполняется для еженедельного расписания.</span><span class="sxs-lookup"><span data-stu-id="cbd61-116">Specifies the days of the week in which the task runs for a weekly schedule.</span></span><br/>              |



## <a name="examples"></a><span data-ttu-id="cbd61-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="cbd61-117">Examples</span></span>

<span data-ttu-id="cbd61-118">Следующий XML-код определяет календарь дня недели, который запускает задачу в пятницу.</span><span class="sxs-lookup"><span data-stu-id="cbd61-118">The following XML defines a day of week calendar that starts a task on Friday.</span></span>


```XML
<DaysOfWeek>
    <Friday/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="cbd61-119">Требования</span><span class="sxs-lookup"><span data-stu-id="cbd61-119">Requirements</span></span>



| <span data-ttu-id="cbd61-120">Требование</span><span class="sxs-lookup"><span data-stu-id="cbd61-120">Requirement</span></span> | <span data-ttu-id="cbd61-121">Значение</span><span class="sxs-lookup"><span data-stu-id="cbd61-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cbd61-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cbd61-122">Minimum supported client</span></span><br/> | <span data-ttu-id="cbd61-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cbd61-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cbd61-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cbd61-124">Minimum supported server</span></span><br/> | <span data-ttu-id="cbd61-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cbd61-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cbd61-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cbd61-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbd61-127">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="cbd61-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="cbd61-128">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="cbd61-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





