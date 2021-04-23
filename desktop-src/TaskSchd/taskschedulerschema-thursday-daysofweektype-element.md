---
title: Четверг (Дайсофвиктипе), элемент
description: Указывает, что задача выполняется в четверг.
ms.assetid: 01d0e7e8-7135-4f43-9d8f-b50c002b93bc
keywords:
- Элемент "четверг" планировщик задач
topic_type:
- apiref
api_name:
- Thursday
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 12b1fb602411a9e4562a044b044e43de4800f239
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672775"
---
# <a name="thursday-daysofweektype-element"></a><span data-ttu-id="ae890-104">Четверг (Дайсофвиктипе), элемент</span><span class="sxs-lookup"><span data-stu-id="ae890-104">Thursday (daysOfWeekType) Element</span></span>

<span data-ttu-id="ae890-105">Указывает, что задача выполняется в четверг.</span><span class="sxs-lookup"><span data-stu-id="ae890-105">Specifies that the task runs on Thursday.</span></span>

``` syntax
<xs:element name="Thursday">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="ae890-106">Элемент " **четверг** " определяется сложным типом [**дайсофвиктипе**](taskschedulerschema-daysofweektype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="ae890-106">The **Thursday** element is defined by the [**daysOfWeekType**](taskschedulerschema-daysofweektype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="ae890-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="ae890-107">Parent element</span></span>



| <span data-ttu-id="ae890-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="ae890-108">Element</span></span>                                                                                                                  | <span data-ttu-id="ae890-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="ae890-109">Derived from</span></span>                                                             | <span data-ttu-id="ae890-110">Описание</span><span class="sxs-lookup"><span data-stu-id="ae890-110">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ae890-111">**DaysOfWeek (Монслидайофвиксчедулетипе)**</span><span class="sxs-lookup"><span data-stu-id="ae890-111">**DaysOfWeek (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="ae890-112">**дайсофвиктипе**</span><span class="sxs-lookup"><span data-stu-id="ae890-112">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="ae890-113">Указывает дни недели, в которых задача выполняется для ежемесячного расписания недели.</span><span class="sxs-lookup"><span data-stu-id="ae890-113">Specifies the days of the week in which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="ae890-114">**DaysOfWeek (Виклисчедулетипе)**</span><span class="sxs-lookup"><span data-stu-id="ae890-114">**DaysOfWeek (weeklyScheduleType)**</span></span>](taskschedulerschema-daysofweek-weeklyscheduletype-element.md)                     | [<span data-ttu-id="ae890-115">**дайсофвиктипе**</span><span class="sxs-lookup"><span data-stu-id="ae890-115">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="ae890-116">Указывает дни недели, в которых задача выполняется для еженедельного расписания.</span><span class="sxs-lookup"><span data-stu-id="ae890-116">Specifies the days of the week in which the task runs for a weekly schedule.</span></span><br/>              |



## <a name="examples"></a><span data-ttu-id="ae890-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="ae890-117">Examples</span></span>

<span data-ttu-id="ae890-118">Следующий XML-код определяет календарь дня недели, который запускает задачу в четверг.</span><span class="sxs-lookup"><span data-stu-id="ae890-118">The following XML defines a day of week calendar that starts a task on Thursday.</span></span>


```XML
<DaysOfWeek>
    <Thursday/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="ae890-119">Требования</span><span class="sxs-lookup"><span data-stu-id="ae890-119">Requirements</span></span>



| <span data-ttu-id="ae890-120">Требование</span><span class="sxs-lookup"><span data-stu-id="ae890-120">Requirement</span></span> | <span data-ttu-id="ae890-121">Значение</span><span class="sxs-lookup"><span data-stu-id="ae890-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ae890-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ae890-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ae890-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ae890-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ae890-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ae890-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ae890-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ae890-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ae890-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ae890-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae890-127">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="ae890-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="ae890-128">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="ae890-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





