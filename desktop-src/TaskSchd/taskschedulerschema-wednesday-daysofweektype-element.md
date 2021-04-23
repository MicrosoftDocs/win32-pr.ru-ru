---
title: Среда (Дайсофвиктипе), элемент
description: Указывает, что задача выполняется в среду.
ms.assetid: 6d4f52e2-4390-4f9d-bab8-813bd0851582
keywords:
- Элемент среды планировщик задач
topic_type:
- apiref
api_name:
- Wednesday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3f9d8c60cb7cea818cc0b096e99e97e8f1490d47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534868"
---
# <a name="wednesday-daysofweektype-element"></a><span data-ttu-id="bba43-104">Среда (Дайсофвиктипе), элемент</span><span class="sxs-lookup"><span data-stu-id="bba43-104">Wednesday (daysOfWeekType) Element</span></span>

<span data-ttu-id="bba43-105">Указывает, что задача выполняется в среду.</span><span class="sxs-lookup"><span data-stu-id="bba43-105">Specifies that the task runs on Wednesday.</span></span>

``` syntax
<xs:element name="Wednesday">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="bba43-106">Элемент **среды** определяется сложным типом [**дайсофвиктипе**](taskschedulerschema-daysofweektype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="bba43-106">The **Wednesday** element is defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="bba43-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="bba43-107">Parent element</span></span>



| <span data-ttu-id="bba43-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="bba43-108">Element</span></span>                                                                                                                  | <span data-ttu-id="bba43-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="bba43-109">Derived from</span></span>                                                             | <span data-ttu-id="bba43-110">Описание</span><span class="sxs-lookup"><span data-stu-id="bba43-110">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bba43-111">**DaysOfWeek (Монслидайофвиксчедулетипе)**</span><span class="sxs-lookup"><span data-stu-id="bba43-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="bba43-112">**дайсофвиктипе**</span><span class="sxs-lookup"><span data-stu-id="bba43-112">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="bba43-113">Указывает дни недели, в которых задача выполняется для ежемесячного расписания недели.</span><span class="sxs-lookup"><span data-stu-id="bba43-113">Specifies the days of the week in which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="bba43-114">**DaysOfWeek (Виклисчедулетипе)**</span><span class="sxs-lookup"><span data-stu-id="bba43-114">**DaysOfWeek (weeklyScheduleType)**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [<span data-ttu-id="bba43-115">**дайсофвиктипе**</span><span class="sxs-lookup"><span data-stu-id="bba43-115">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="bba43-116">Указывает дни недели, в которых задача выполняется для еженедельного расписания.</span><span class="sxs-lookup"><span data-stu-id="bba43-116">Specifies the days of the week in which the task runs for a weekly schedule.</span></span><br/>              |



## <a name="examples"></a><span data-ttu-id="bba43-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="bba43-117">Examples</span></span>

<span data-ttu-id="bba43-118">Следующий XML-код определяет календарь дня недели, который запускает задачу в среду.</span><span class="sxs-lookup"><span data-stu-id="bba43-118">The following XML defines a day of week calendar that starts a task on Wednesday.</span></span>


```XML
<DaysOfWeek>
    <Wednesday/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="bba43-119">Требования</span><span class="sxs-lookup"><span data-stu-id="bba43-119">Requirements</span></span>



| <span data-ttu-id="bba43-120">Требование</span><span class="sxs-lookup"><span data-stu-id="bba43-120">Requirement</span></span> | <span data-ttu-id="bba43-121">Значение</span><span class="sxs-lookup"><span data-stu-id="bba43-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bba43-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bba43-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bba43-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bba43-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bba43-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bba43-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bba43-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bba43-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bba43-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bba43-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bba43-127">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="bba43-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="bba43-128">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="bba43-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





