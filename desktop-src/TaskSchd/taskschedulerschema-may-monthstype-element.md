---
title: Май (Монсстипе), элемент
description: Указывает, что задача выполняется в Май.
ms.assetid: 1fcc3eb7-6500-4ba3-b146-14d169d9b445
keywords:
- Элемент может планировщик задач
topic_type:
- apiref
api_name:
- May
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d3f0c107124aa2c87672f63a469857f3795e13c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672777"
---
# <a name="may-monthstype-element"></a><span data-ttu-id="4a70b-104">Май (Монсстипе), элемент</span><span class="sxs-lookup"><span data-stu-id="4a70b-104">May (monthsType) Element</span></span>

<span data-ttu-id="4a70b-105">Указывает, что задача выполняется в Май.</span><span class="sxs-lookup"><span data-stu-id="4a70b-105">Specifies that the task runs in May.</span></span>

``` syntax
<xs:element name="May">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="4a70b-106">Элемент " **Май** " определяется сложным типом [**монсстипе**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="4a70b-106">The **May** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="4a70b-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="4a70b-107">Parent element</span></span>



| <span data-ttu-id="4a70b-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="4a70b-108">Element</span></span>                                                                                                          | <span data-ttu-id="4a70b-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="4a70b-109">Derived from</span></span>                                                     | <span data-ttu-id="4a70b-110">Описание</span><span class="sxs-lookup"><span data-stu-id="4a70b-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4a70b-111">**Месяцы (Монслидайофвиксчедулетипе)**</span><span class="sxs-lookup"><span data-stu-id="4a70b-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="4a70b-112">**монсстипе**</span><span class="sxs-lookup"><span data-stu-id="4a70b-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="4a70b-113">Указывает месяцы года, в течение которых задача выполняется для ежемесячного расписания недели.</span><span class="sxs-lookup"><span data-stu-id="4a70b-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="4a70b-114">**Месяцы (Монслисчедулетипе)**</span><span class="sxs-lookup"><span data-stu-id="4a70b-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="4a70b-115">**монсстипе**</span><span class="sxs-lookup"><span data-stu-id="4a70b-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="4a70b-116">Указывает месяцы года, в течение которых задача выполняется для ежемесячного расписания.</span><span class="sxs-lookup"><span data-stu-id="4a70b-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="4a70b-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="4a70b-117">Examples</span></span>

<span data-ttu-id="4a70b-118">Следующий XML-код определяет календарь месяцев, в котором выполняется задача в мае.</span><span class="sxs-lookup"><span data-stu-id="4a70b-118">The following XML defines a months calendar that runs the task in May.</span></span>


```XML
<Months>
    <May/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="4a70b-119">Требования</span><span class="sxs-lookup"><span data-stu-id="4a70b-119">Requirements</span></span>



| <span data-ttu-id="4a70b-120">Требование</span><span class="sxs-lookup"><span data-stu-id="4a70b-120">Requirement</span></span> | <span data-ttu-id="4a70b-121">Значение</span><span class="sxs-lookup"><span data-stu-id="4a70b-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4a70b-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4a70b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4a70b-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4a70b-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4a70b-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4a70b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4a70b-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4a70b-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4a70b-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4a70b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a70b-127">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="4a70b-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="4a70b-128">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="4a70b-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





