---
title: Ноябрь (Монсстипе), элемент
description: Указывает, что задача выполняется в ноябре.
ms.assetid: 45f8c47b-3884-4f18-8275-f29f82ee32e2
keywords:
- Ноябрьский элемент планировщик задач
topic_type:
- apiref
api_name:
- November
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 295b63a4ff4dad1ec07504bb43c4a471d4389159
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681946"
---
# <a name="november-monthstype-element"></a><span data-ttu-id="a8aad-104">Ноябрь (Монсстипе), элемент</span><span class="sxs-lookup"><span data-stu-id="a8aad-104">November (monthsType) Element</span></span>

<span data-ttu-id="a8aad-105">Указывает, что задача выполняется в ноябре.</span><span class="sxs-lookup"><span data-stu-id="a8aad-105">Specifies that the task runs in November.</span></span>

``` syntax
<xs:element name="November">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="a8aad-106">Элемент **Ноябрь** определяется сложным типом [**монсстипе**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="a8aad-106">The **November** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="a8aad-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="a8aad-107">Parent element</span></span>



| <span data-ttu-id="a8aad-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="a8aad-108">Element</span></span>                                                                                                          | <span data-ttu-id="a8aad-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="a8aad-109">Derived from</span></span>                                                     | <span data-ttu-id="a8aad-110">Описание</span><span class="sxs-lookup"><span data-stu-id="a8aad-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a8aad-111">**Месяцы (Монслидайофвиксчедулетипе)**</span><span class="sxs-lookup"><span data-stu-id="a8aad-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="a8aad-112">**монсстипе**</span><span class="sxs-lookup"><span data-stu-id="a8aad-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="a8aad-113">Указывает месяцы года, в течение которых задача выполняется для ежемесячного расписания недели.</span><span class="sxs-lookup"><span data-stu-id="a8aad-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="a8aad-114">**Месяцы (Монслисчедулетипе)**</span><span class="sxs-lookup"><span data-stu-id="a8aad-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="a8aad-115">**монсстипе**</span><span class="sxs-lookup"><span data-stu-id="a8aad-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="a8aad-116">Указывает месяцы года, в течение которых задача выполняется для ежемесячного расписания.</span><span class="sxs-lookup"><span data-stu-id="a8aad-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="a8aad-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="a8aad-117">Examples</span></span>

<span data-ttu-id="a8aad-118">Следующий XML-код определяет календарь месяцев, который запускает задачу в ноябре.</span><span class="sxs-lookup"><span data-stu-id="a8aad-118">The following XML defines a months calendar that runs the task in November.</span></span>


```XML
<Months>
    <November/>
</DaysOfWeek>
```



## <a name="requirements"></a><span data-ttu-id="a8aad-119">Требования</span><span class="sxs-lookup"><span data-stu-id="a8aad-119">Requirements</span></span>



| <span data-ttu-id="a8aad-120">Требование</span><span class="sxs-lookup"><span data-stu-id="a8aad-120">Requirement</span></span> | <span data-ttu-id="a8aad-121">Значение</span><span class="sxs-lookup"><span data-stu-id="a8aad-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a8aad-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a8aad-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a8aad-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a8aad-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a8aad-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a8aad-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a8aad-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a8aad-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a8aad-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a8aad-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8aad-127">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="a8aad-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="a8aad-128">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="a8aad-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





