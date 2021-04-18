---
title: Элемент вторника (Дайсофвиктипе)
description: Указывает, что задача выполняется во вторник.
ms.assetid: 588608e9-33f9-405d-8b4b-35f11ab403db
keywords:
- Элемент вторника планировщик задач
topic_type:
- apiref
api_name:
- Tuesday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5ed48803d0cad5dae409202869c600e7e7a60643
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672897"
---
# <a name="tuesday-daysofweektype-element"></a><span data-ttu-id="eb40f-104">Элемент вторника (Дайсофвиктипе)</span><span class="sxs-lookup"><span data-stu-id="eb40f-104">Tuesday (daysOfWeekType) Element</span></span>

<span data-ttu-id="eb40f-105">Указывает, что задача выполняется во вторник.</span><span class="sxs-lookup"><span data-stu-id="eb40f-105">Specifies that the task runs on Tuesday.</span></span>

``` syntax
<xs:element name="Tuesday">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="eb40f-106">Элемент **вторника** определяется сложным типом [**дайсофвиктипе**](taskschedulerschema-daysofweektype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="eb40f-106">The **Tuesday** element is defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="eb40f-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="eb40f-107">Parent element</span></span>



| <span data-ttu-id="eb40f-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="eb40f-108">Element</span></span>                                                                                                                  | <span data-ttu-id="eb40f-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="eb40f-109">Derived from</span></span>                                                             | <span data-ttu-id="eb40f-110">Описание</span><span class="sxs-lookup"><span data-stu-id="eb40f-110">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eb40f-111">**DaysOfWeek (Монслидайофвиксчедулетипе)**</span><span class="sxs-lookup"><span data-stu-id="eb40f-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="eb40f-112">**дайсофвиктипе**</span><span class="sxs-lookup"><span data-stu-id="eb40f-112">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="eb40f-113">Указывает дни недели, в которых задача выполняется для ежемесячного расписания недели.</span><span class="sxs-lookup"><span data-stu-id="eb40f-113">Specifies the days of the week in which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="eb40f-114">**DaysOfWeek (Виклисчедулетипе)**</span><span class="sxs-lookup"><span data-stu-id="eb40f-114">**DaysOfWeek (weeklyScheduleType)**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [<span data-ttu-id="eb40f-115">**дайсофвиктипе**</span><span class="sxs-lookup"><span data-stu-id="eb40f-115">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="eb40f-116">Указывает дни недели, в которых задача выполняется для еженедельного расписания.</span><span class="sxs-lookup"><span data-stu-id="eb40f-116">Specifies the days of the week in which the task runs for a weekly schedule.</span></span><br/>              |



## <a name="examples"></a><span data-ttu-id="eb40f-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="eb40f-117">Examples</span></span>

<span data-ttu-id="eb40f-118">Следующий XML-код определяет календарь дня недели, который запускает задачу во вторник.</span><span class="sxs-lookup"><span data-stu-id="eb40f-118">The following XML defines a day of week calendar that starts a task on Tuesday.</span></span>


```XML
<DaysOfWeek>
    <Tuesday/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="eb40f-119">Требования</span><span class="sxs-lookup"><span data-stu-id="eb40f-119">Requirements</span></span>



| <span data-ttu-id="eb40f-120">Требование</span><span class="sxs-lookup"><span data-stu-id="eb40f-120">Requirement</span></span> | <span data-ttu-id="eb40f-121">Значение</span><span class="sxs-lookup"><span data-stu-id="eb40f-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="eb40f-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eb40f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="eb40f-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eb40f-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="eb40f-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eb40f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="eb40f-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="eb40f-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="eb40f-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eb40f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb40f-127">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="eb40f-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="eb40f-128">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="eb40f-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





