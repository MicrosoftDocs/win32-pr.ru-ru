---
title: Апрель (Монсстипе), элемент
description: Указывает, что задача выполняется в апреле.
ms.assetid: b642e142-0acc-4b88-a86a-5d539613ead6
keywords:
- Элемент April планировщик задач
topic_type:
- apiref
api_name:
- April
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ecde82e5091adf51c2e42b682e36dba6d45e85c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137370"
---
# <a name="april-monthstype-element"></a><span data-ttu-id="534a8-104">Апрель (Монсстипе), элемент</span><span class="sxs-lookup"><span data-stu-id="534a8-104">April (monthsType) Element</span></span>

<span data-ttu-id="534a8-105">Указывает, что задача выполняется в апреле.</span><span class="sxs-lookup"><span data-stu-id="534a8-105">Specifies that the task runs in April.</span></span>

``` syntax
<xs:element name="April">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="534a8-106">Элемент **April** определяется сложным типом [**монсстипе**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="534a8-106">The **April** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="534a8-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="534a8-107">Parent element</span></span>



| <span data-ttu-id="534a8-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="534a8-108">Element</span></span>                                                                                                          | <span data-ttu-id="534a8-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="534a8-109">Derived from</span></span>                                                     | <span data-ttu-id="534a8-110">Описание</span><span class="sxs-lookup"><span data-stu-id="534a8-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="534a8-111">**Месяцы (Монслидайофвиксчедулетипе)**</span><span class="sxs-lookup"><span data-stu-id="534a8-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="534a8-112">**монсстипе**</span><span class="sxs-lookup"><span data-stu-id="534a8-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="534a8-113">Указывает месяцы года, в течение которых задача выполняется для ежемесячного расписания.</span><span class="sxs-lookup"><span data-stu-id="534a8-113">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |
| [<span data-ttu-id="534a8-114">**Месяцы (Монслисчедулетипе)**</span><span class="sxs-lookup"><span data-stu-id="534a8-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="534a8-115">**монсстипе**</span><span class="sxs-lookup"><span data-stu-id="534a8-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="534a8-116">Указывает месяцы года, в течение которых задача выполняется для ежемесячного расписания недели.</span><span class="sxs-lookup"><span data-stu-id="534a8-116">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |



## <a name="examples"></a><span data-ttu-id="534a8-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="534a8-117">Examples</span></span>

<span data-ttu-id="534a8-118">Следующий XML-код определяет календарь месяцев, в котором выполняется задача в апреле.</span><span class="sxs-lookup"><span data-stu-id="534a8-118">The following XML defines a months calendar that runs the task in April.</span></span>


```XML
<Months>
    <April/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="534a8-119">Требования</span><span class="sxs-lookup"><span data-stu-id="534a8-119">Requirements</span></span>



| <span data-ttu-id="534a8-120">Требование</span><span class="sxs-lookup"><span data-stu-id="534a8-120">Requirement</span></span> | <span data-ttu-id="534a8-121">Значение</span><span class="sxs-lookup"><span data-stu-id="534a8-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="534a8-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="534a8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="534a8-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="534a8-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="534a8-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="534a8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="534a8-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="534a8-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="534a8-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="534a8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="534a8-127">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="534a8-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="534a8-128">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="534a8-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





