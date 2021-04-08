---
title: Элемент августе (Монсстипе)
description: Указывает, что задача выполняется в августе.
ms.assetid: cd7e528c-d482-4bb4-a31f-fccdb19a441b
keywords:
- планировщик задач элемента августе
topic_type:
- apiref
api_name:
- August
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4978ebd8f22da6e157461791c4c2000fce9db6ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892209"
---
# <a name="august-monthstype-element"></a><span data-ttu-id="fc774-104">Элемент августе (Монсстипе)</span><span class="sxs-lookup"><span data-stu-id="fc774-104">August (monthsType) Element</span></span>

<span data-ttu-id="fc774-105">Указывает, что задача выполняется в августе.</span><span class="sxs-lookup"><span data-stu-id="fc774-105">Specifies that the task runs in August.</span></span>

``` syntax
<xs:element name="August">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="fc774-106">Элемент **августе** определяется сложным типом [**монсстипе**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="fc774-106">The **August** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="fc774-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="fc774-107">Parent element</span></span>



| <span data-ttu-id="fc774-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="fc774-108">Element</span></span>                                                                                                          | <span data-ttu-id="fc774-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="fc774-109">Derived from</span></span>                                                     | <span data-ttu-id="fc774-110">Описание</span><span class="sxs-lookup"><span data-stu-id="fc774-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fc774-111">**Месяцы (Монслидайофвиксчедулетипе)**</span><span class="sxs-lookup"><span data-stu-id="fc774-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="fc774-112">**монсстипе**</span><span class="sxs-lookup"><span data-stu-id="fc774-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="fc774-113">Указывает месяцы года, в течение которых задача выполняется для ежемесячного расписания недели.</span><span class="sxs-lookup"><span data-stu-id="fc774-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="fc774-114">**Месяцы (Монслисчедулетипе)**</span><span class="sxs-lookup"><span data-stu-id="fc774-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="fc774-115">**монсстипе**</span><span class="sxs-lookup"><span data-stu-id="fc774-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="fc774-116">Указывает месяцы года, в течение которых задача выполняется для ежемесячного расписания.</span><span class="sxs-lookup"><span data-stu-id="fc774-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="fc774-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="fc774-117">Examples</span></span>

<span data-ttu-id="fc774-118">Следующий XML-код определяет календарь месяцев, в котором выполняется задача в августе.</span><span class="sxs-lookup"><span data-stu-id="fc774-118">The following XML defines a months calendar that runs the task in August.</span></span>


```XML
<Months>
    <August/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="fc774-119">Требования</span><span class="sxs-lookup"><span data-stu-id="fc774-119">Requirements</span></span>



| <span data-ttu-id="fc774-120">Требование</span><span class="sxs-lookup"><span data-stu-id="fc774-120">Requirement</span></span> | <span data-ttu-id="fc774-121">Значение</span><span class="sxs-lookup"><span data-stu-id="fc774-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fc774-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fc774-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fc774-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fc774-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fc774-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fc774-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fc774-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fc774-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fc774-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fc774-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc774-127">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="fc774-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="fc774-128">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="fc774-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





