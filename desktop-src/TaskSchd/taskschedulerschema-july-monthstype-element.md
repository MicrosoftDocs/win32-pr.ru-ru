---
title: Элемент Июль (Монсстипе)
description: Указывает, что задача выполняется в июле.
ms.assetid: 6fcb06f1-0806-469c-a283-ba8f2ba2c256
keywords:
- планировщик задач элемента Июль
topic_type:
- apiref
api_name:
- July
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6901ca83792ffd98269e26dc9cf24dd575025c52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803328"
---
# <a name="july-monthstype-element"></a><span data-ttu-id="72ec7-104">Элемент Июль (Монсстипе)</span><span class="sxs-lookup"><span data-stu-id="72ec7-104">July (monthsType) Element</span></span>

<span data-ttu-id="72ec7-105">Указывает, что задача выполняется в июле.</span><span class="sxs-lookup"><span data-stu-id="72ec7-105">Specifies that the task runs in July.</span></span>

``` syntax
<xs:element name="July">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="72ec7-106">Элемент **Июль** определяется сложным типом [**монсстипе**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="72ec7-106">The **July** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="72ec7-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="72ec7-107">Parent element</span></span>



| <span data-ttu-id="72ec7-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="72ec7-108">Element</span></span>                                                                                                          | <span data-ttu-id="72ec7-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="72ec7-109">Derived from</span></span>                                                     | <span data-ttu-id="72ec7-110">Описание</span><span class="sxs-lookup"><span data-stu-id="72ec7-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="72ec7-111">**Месяцы (Монслидайофвиксчедулетипе)**</span><span class="sxs-lookup"><span data-stu-id="72ec7-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="72ec7-112">**монсстипе**</span><span class="sxs-lookup"><span data-stu-id="72ec7-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="72ec7-113">Указывает месяцы года, в течение которых задача выполняется для ежемесячного расписания недели.</span><span class="sxs-lookup"><span data-stu-id="72ec7-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="72ec7-114">**Месяцы (Монслисчедулетипе)**</span><span class="sxs-lookup"><span data-stu-id="72ec7-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="72ec7-115">**монсстипе**</span><span class="sxs-lookup"><span data-stu-id="72ec7-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="72ec7-116">Указывает месяцы года, в течение которых задача выполняется для ежемесячного расписания.</span><span class="sxs-lookup"><span data-stu-id="72ec7-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="72ec7-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="72ec7-117">Examples</span></span>

<span data-ttu-id="72ec7-118">Следующий XML-код определяет календарь месяцев, который запускает задачу в июле.</span><span class="sxs-lookup"><span data-stu-id="72ec7-118">The following XML defines a months calendar that runs the task in July.</span></span>


```XML
<Months>
    <July/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="72ec7-119">Требования</span><span class="sxs-lookup"><span data-stu-id="72ec7-119">Requirements</span></span>



| <span data-ttu-id="72ec7-120">Требование</span><span class="sxs-lookup"><span data-stu-id="72ec7-120">Requirement</span></span> | <span data-ttu-id="72ec7-121">Значение</span><span class="sxs-lookup"><span data-stu-id="72ec7-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="72ec7-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="72ec7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="72ec7-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="72ec7-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="72ec7-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="72ec7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="72ec7-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="72ec7-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="72ec7-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="72ec7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72ec7-127">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="72ec7-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="72ec7-128">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="72ec7-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





