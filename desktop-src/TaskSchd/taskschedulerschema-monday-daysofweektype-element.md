---
title: Понедельник (Дайсофвиктипе), элемент
description: Указывает, что задача выполняется в понедельник.
ms.assetid: 2b7ce0c1-c635-47d0-b482-5c93c0028c92
keywords:
- планировщик задач элемента понедельник
topic_type:
- apiref
api_name:
- Monday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3967db32a6ccd536e2e389e84de4eec05b333634
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492057"
---
# <a name="monday-daysofweektype-element"></a><span data-ttu-id="77603-104">Понедельник (Дайсофвиктипе), элемент</span><span class="sxs-lookup"><span data-stu-id="77603-104">Monday (daysOfWeekType) Element</span></span>

<span data-ttu-id="77603-105">Указывает, что задача выполняется в понедельник.</span><span class="sxs-lookup"><span data-stu-id="77603-105">Specifies that the task runs on Monday.</span></span>

``` syntax
<xs:element name="Monday">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="77603-106">Элемент **Monday** определяется сложным типом [**виклисчедулетипе**](taskschedulerschema-weeklyscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="77603-106">The **Monday** element is defined by the [**weeklyScheduleType**](taskschedulerschema-weeklyscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="77603-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="77603-107">Parent element</span></span>



| <span data-ttu-id="77603-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="77603-108">Element</span></span>                                                                                                                  | <span data-ttu-id="77603-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="77603-109">Derived from</span></span>                                                             | <span data-ttu-id="77603-110">Описание</span><span class="sxs-lookup"><span data-stu-id="77603-110">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="77603-111">**DaysOfWeek (Монслидайофвиксчедулетипе)**</span><span class="sxs-lookup"><span data-stu-id="77603-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="77603-112">**дайсофвиктипе**</span><span class="sxs-lookup"><span data-stu-id="77603-112">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="77603-113">Указывает дни недели, в которых задача выполняется для ежемесячного расписания недели.</span><span class="sxs-lookup"><span data-stu-id="77603-113">Specifies the days of the week in which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="77603-114">**DaysOfWeek (Виклисчедулетипе)**</span><span class="sxs-lookup"><span data-stu-id="77603-114">**DaysOfWeek (weeklyScheduleType)**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [<span data-ttu-id="77603-115">**дайсофвиктипе**</span><span class="sxs-lookup"><span data-stu-id="77603-115">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="77603-116">Указывает дни недели, в которых задача выполняется для еженедельного расписания.</span><span class="sxs-lookup"><span data-stu-id="77603-116">Specifies the days of the week in which the task runs for a weekly schedule.</span></span><br/>              |



## <a name="examples"></a><span data-ttu-id="77603-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="77603-117">Examples</span></span>

<span data-ttu-id="77603-118">Следующий XML-код определяет календарь дня недели, который запускает задачу в понедельник.</span><span class="sxs-lookup"><span data-stu-id="77603-118">The following XML defines a day of week calendar that starts a task on Monday.</span></span>


```XML
<DaysOfWeek>
    <Monday/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="77603-119">Требования</span><span class="sxs-lookup"><span data-stu-id="77603-119">Requirements</span></span>



| <span data-ttu-id="77603-120">Требование</span><span class="sxs-lookup"><span data-stu-id="77603-120">Requirement</span></span> | <span data-ttu-id="77603-121">Значение</span><span class="sxs-lookup"><span data-stu-id="77603-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="77603-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="77603-122">Minimum supported client</span></span><br/> | <span data-ttu-id="77603-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="77603-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="77603-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="77603-124">Minimum supported server</span></span><br/> | <span data-ttu-id="77603-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="77603-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="77603-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="77603-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77603-127">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="77603-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="77603-128">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="77603-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





