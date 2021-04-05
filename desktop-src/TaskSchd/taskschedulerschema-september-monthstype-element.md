---
title: Сентябрь (Монсстипе), элемент
description: Указывает, что задача выполняется в сентябре.
ms.assetid: b1ad2221-ca22-4808-bf20-ecf3cbb930f2
keywords:
- Сентябрь планировщик задач элементов
topic_type:
- apiref
api_name:
- September
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bdd7e18ba9ae1cc7653589710fb9529281e84ccb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989257"
---
# <a name="september-monthstype-element"></a><span data-ttu-id="fb779-104">Сентябрь (Монсстипе), элемент</span><span class="sxs-lookup"><span data-stu-id="fb779-104">September (monthsType) Element</span></span>

<span data-ttu-id="fb779-105">Указывает, что задача выполняется в сентябре.</span><span class="sxs-lookup"><span data-stu-id="fb779-105">Specifies that the task runs in September.</span></span>

``` syntax
<xs:element name="September">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="fb779-106">Элемент **сентября** определяется сложным типом [**монсстипе**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="fb779-106">The **September** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="fb779-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="fb779-107">Parent element</span></span>



| <span data-ttu-id="fb779-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="fb779-108">Element</span></span>                                                                                                          | <span data-ttu-id="fb779-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="fb779-109">Derived from</span></span>                                                     | <span data-ttu-id="fb779-110">Описание</span><span class="sxs-lookup"><span data-stu-id="fb779-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fb779-111">**Месяцы (Монслидайофвиксчедулетипе)**</span><span class="sxs-lookup"><span data-stu-id="fb779-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="fb779-112">**монсстипе**</span><span class="sxs-lookup"><span data-stu-id="fb779-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="fb779-113">Указывает месяцы года, в течение которых задача выполняется для ежемесячного расписания недели.</span><span class="sxs-lookup"><span data-stu-id="fb779-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="fb779-114">**Месяцы (Монслисчедулетипе)**</span><span class="sxs-lookup"><span data-stu-id="fb779-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="fb779-115">**монсстипе**</span><span class="sxs-lookup"><span data-stu-id="fb779-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="fb779-116">Указывает месяцы года, в течение которых задача выполняется для ежемесячного расписания.</span><span class="sxs-lookup"><span data-stu-id="fb779-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="fb779-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="fb779-117">Examples</span></span>

<span data-ttu-id="fb779-118">Следующий XML-код определяет календарь месяцев, в котором задача выполняется в сентябре.</span><span class="sxs-lookup"><span data-stu-id="fb779-118">The following XML defines a months calendar that runs the task in September.</span></span>


```XML
<Months>
    <September/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="fb779-119">Требования</span><span class="sxs-lookup"><span data-stu-id="fb779-119">Requirements</span></span>



| <span data-ttu-id="fb779-120">Требование</span><span class="sxs-lookup"><span data-stu-id="fb779-120">Requirement</span></span> | <span data-ttu-id="fb779-121">Значение</span><span class="sxs-lookup"><span data-stu-id="fb779-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fb779-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fb779-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fb779-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fb779-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fb779-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fb779-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fb779-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fb779-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fb779-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fb779-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb779-127">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="fb779-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="fb779-128">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="fb779-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





