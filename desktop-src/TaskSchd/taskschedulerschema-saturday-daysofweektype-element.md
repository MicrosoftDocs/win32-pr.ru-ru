---
title: Суббота (Дайсофвиктипе), элемент
description: Указывает, что задача выполняется в субботу.
ms.assetid: def26a72-c143-466a-b5b0-6105078afffa
keywords:
- Элемент субботы планировщик задач
topic_type:
- apiref
api_name:
- Saturday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b5f7cb36002b2add64cdea541caa2fd28df37ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803322"
---
# <a name="saturday-daysofweektype-element"></a><span data-ttu-id="72589-104">Суббота (Дайсофвиктипе), элемент</span><span class="sxs-lookup"><span data-stu-id="72589-104">Saturday (daysOfWeekType) Element</span></span>

<span data-ttu-id="72589-105">Указывает, что задача выполняется в субботу.</span><span class="sxs-lookup"><span data-stu-id="72589-105">Specifies that the task runs on Saturday.</span></span>

``` syntax
<xs:element name="Saturday">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="72589-106">Элемент **субботы** определяется сложным типом [**дайсофвиктипе**](taskschedulerschema-daysofweektype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="72589-106">The **Saturday** element is defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="72589-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="72589-107">Parent element</span></span>



| <span data-ttu-id="72589-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="72589-108">Element</span></span>                                                                                                                  | <span data-ttu-id="72589-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="72589-109">Derived from</span></span>                                                             | <span data-ttu-id="72589-110">Описание</span><span class="sxs-lookup"><span data-stu-id="72589-110">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="72589-111">**DaysOfWeek (Монслидайофвиксчедулетипе)**</span><span class="sxs-lookup"><span data-stu-id="72589-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="72589-112">**дайсофвиктипе**</span><span class="sxs-lookup"><span data-stu-id="72589-112">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="72589-113">Указывает дни недели, в которых задача выполняется для ежемесячного расписания недели.</span><span class="sxs-lookup"><span data-stu-id="72589-113">Specifies the days of the week in which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="72589-114">**DaysOfWeek (Виклисчедулетипе)**</span><span class="sxs-lookup"><span data-stu-id="72589-114">**DaysOfWeek (weeklyScheduleType)**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [<span data-ttu-id="72589-115">**дайсофвиктипе**</span><span class="sxs-lookup"><span data-stu-id="72589-115">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="72589-116">Указывает дни недели, в которых задача выполняется для еженедельного расписания.</span><span class="sxs-lookup"><span data-stu-id="72589-116">Specifies the days of the week in which the task runs for a weekly schedule.</span></span><br/>              |



## <a name="examples"></a><span data-ttu-id="72589-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="72589-117">Examples</span></span>

<span data-ttu-id="72589-118">Следующий XML-код определяет календарь дня недели, который запускает задачу в субботу.</span><span class="sxs-lookup"><span data-stu-id="72589-118">The following XML defines a day of week calendar that starts a task on Saturday.</span></span>


```XML
<DaysOfWeek>
    <Saturday/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="72589-119">Требования</span><span class="sxs-lookup"><span data-stu-id="72589-119">Requirements</span></span>



| <span data-ttu-id="72589-120">Требование</span><span class="sxs-lookup"><span data-stu-id="72589-120">Requirement</span></span> | <span data-ttu-id="72589-121">Значение</span><span class="sxs-lookup"><span data-stu-id="72589-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="72589-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="72589-122">Minimum supported client</span></span><br/> | <span data-ttu-id="72589-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="72589-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="72589-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="72589-124">Minimum supported server</span></span><br/> | <span data-ttu-id="72589-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="72589-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="72589-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="72589-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72589-127">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="72589-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="72589-128">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="72589-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





