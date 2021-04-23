---
title: Воскресенье (Дайсофвиктипе), элемент
description: Указывает, что задача выполняется в воскресенье.
ms.assetid: 856db869-2273-4bb8-88c8-c126bb16c87b
keywords:
- Воскресенье элемента планировщик задач
topic_type:
- apiref
api_name:
- Sunday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 40efba31b392da5959853feeb1cae567cee25cc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137014"
---
# <a name="sunday-daysofweektype-element"></a><span data-ttu-id="743c4-104">Воскресенье (Дайсофвиктипе), элемент</span><span class="sxs-lookup"><span data-stu-id="743c4-104">Sunday (daysOfWeekType) Element</span></span>

<span data-ttu-id="743c4-105">Указывает, что задача выполняется в воскресенье.</span><span class="sxs-lookup"><span data-stu-id="743c4-105">Specifies that the task runs on Sunday.</span></span>

``` syntax
<xs:element name="Sunday">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="743c4-106">Элемент **Sunday** определяется сложным типом [**дайсофвиктипе**](taskschedulerschema-daysofweektype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="743c4-106">The **Sunday** element is defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="743c4-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="743c4-107">Parent element</span></span>



| <span data-ttu-id="743c4-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="743c4-108">Element</span></span>                                                                                                                  | <span data-ttu-id="743c4-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="743c4-109">Derived from</span></span>                                                             | <span data-ttu-id="743c4-110">Описание</span><span class="sxs-lookup"><span data-stu-id="743c4-110">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="743c4-111">**DaysOfWeek (Монслидайофвиксчедулетипе)**</span><span class="sxs-lookup"><span data-stu-id="743c4-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="743c4-112">**дайсофвиктипе**</span><span class="sxs-lookup"><span data-stu-id="743c4-112">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="743c4-113">Указывает дни недели, в которых задача выполняется для ежемесячного расписания недели.</span><span class="sxs-lookup"><span data-stu-id="743c4-113">Specifies the days of the week in which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="743c4-114">**DaysOfWeek (Виклисчедулетипе)**</span><span class="sxs-lookup"><span data-stu-id="743c4-114">**DaysOfWeek (weeklyScheduleType)**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [<span data-ttu-id="743c4-115">**дайсофвиктипе**</span><span class="sxs-lookup"><span data-stu-id="743c4-115">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="743c4-116">Указывает дни недели, в которых задача выполняется для еженедельного расписания.</span><span class="sxs-lookup"><span data-stu-id="743c4-116">Specifies the days of the week in which the task runs for a weekly schedule.</span></span><br/>              |



## <a name="examples"></a><span data-ttu-id="743c4-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="743c4-117">Examples</span></span>

<span data-ttu-id="743c4-118">Следующий XML-код определяет календарь дня недели, который запускает задачу в воскресенье.</span><span class="sxs-lookup"><span data-stu-id="743c4-118">The following XML defines a day of week calendar that starts a task on Sunday.</span></span>


```XML
<DaysOfWeek>
    <Sunday/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="743c4-119">Требования</span><span class="sxs-lookup"><span data-stu-id="743c4-119">Requirements</span></span>



| <span data-ttu-id="743c4-120">Требование</span><span class="sxs-lookup"><span data-stu-id="743c4-120">Requirement</span></span> | <span data-ttu-id="743c4-121">Значение</span><span class="sxs-lookup"><span data-stu-id="743c4-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="743c4-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="743c4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="743c4-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="743c4-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="743c4-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="743c4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="743c4-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="743c4-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="743c4-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="743c4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="743c4-127">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="743c4-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="743c4-128">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="743c4-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





