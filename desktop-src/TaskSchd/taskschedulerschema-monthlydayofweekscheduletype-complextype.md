---
title: Сложный тип Монслидайофвиксчедулетипе
description: Определяет дочерние элементы и сведения о последовательности для элемента Счедулебимонсдайофвик.
ms.assetid: fb4e5ba3-592b-47a4-bedf-5181d2b7a50f
keywords:
- планировщик задач сложного типа Монслидайофвиксчедулетипе
topic_type:
- apiref
api_name:
- monthlyDayOfWeekScheduleType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 782715aed5cbf59a98e996bfa18fdd7c1022227a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672784"
---
# <a name="monthlydayofweekscheduletype-complex-type"></a><span data-ttu-id="d7137-104">Сложный тип Монслидайофвиксчедулетипе</span><span class="sxs-lookup"><span data-stu-id="d7137-104">monthlyDayOfWeekScheduleType Complex Type</span></span>

<span data-ttu-id="d7137-105">Определяет дочерние элементы и сведения о последовательности для элемента [**счедулебимонсдайофвик**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d7137-105">Defines the child elements and sequencing information for the [**ScheduleByMonthDayOfWeek**](taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) element.</span></span>

``` syntax
<xs:complexType name="monthlyDayOfWeekScheduleType">
    <xs:all>
        <xs:element name="Weeks"
            type="weeksType"
            minOccurs="0"
         />
        <xs:element name="DaysOfWeek"
            type="daysOfWeekType"
         />
        <xs:element name="Months"
            type="monthsType"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="d7137-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="d7137-106">Child elements</span></span>



| <span data-ttu-id="d7137-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="d7137-107">Element</span></span>                                                                                   | <span data-ttu-id="d7137-108">Тип</span><span class="sxs-lookup"><span data-stu-id="d7137-108">Type</span></span>                                                                     | <span data-ttu-id="d7137-109">Описание</span><span class="sxs-lookup"><span data-stu-id="d7137-109">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="d7137-110">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="d7137-110">**DaysOfWeek**</span></span>](taskschedulerschema-daysofweek-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="d7137-111">**дайсофвиктипе**</span><span class="sxs-lookup"><span data-stu-id="d7137-111">**daysOfWeekType**</span></span>](taskschedulerschema-daysofweektype-complextype.md) | <span data-ttu-id="d7137-112">Указывает дни недели, в которые выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="d7137-112">Specifies the days of the week during which the task runs.</span></span><br/>   |
| [<span data-ttu-id="d7137-113">**Месяц**</span><span class="sxs-lookup"><span data-stu-id="d7137-113">**Months**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md)         | [<span data-ttu-id="d7137-114">**монсстипе**</span><span class="sxs-lookup"><span data-stu-id="d7137-114">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md)         | <span data-ttu-id="d7137-115">Указывает месяцы года, в течение которых выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="d7137-115">Specifies the months of the year during which the task runs.</span></span><br/> |
| [<span data-ttu-id="d7137-116">**Недели**</span><span class="sxs-lookup"><span data-stu-id="d7137-116">**Weeks**</span></span>](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md)           | [<span data-ttu-id="d7137-117">**викстипе**</span><span class="sxs-lookup"><span data-stu-id="d7137-117">**weeksType**</span></span>](taskschedulerschema-weekstype-complextype.md)           | <span data-ttu-id="d7137-118">Указывает недели месяца, в течение которых выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="d7137-118">Specifies the weeks of the month during which the task runs.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="d7137-119">Требования</span><span class="sxs-lookup"><span data-stu-id="d7137-119">Requirements</span></span>



| <span data-ttu-id="d7137-120">Требование</span><span class="sxs-lookup"><span data-stu-id="d7137-120">Requirement</span></span> | <span data-ttu-id="d7137-121">Значение</span><span class="sxs-lookup"><span data-stu-id="d7137-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d7137-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d7137-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d7137-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d7137-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d7137-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d7137-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d7137-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d7137-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d7137-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d7137-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7137-127">планировщик задач сложные типы схемы</span><span class="sxs-lookup"><span data-stu-id="d7137-127">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="d7137-128">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="d7137-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





