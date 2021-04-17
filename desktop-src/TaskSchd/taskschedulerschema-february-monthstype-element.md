---
title: Элемент Февраль (Монсстипе)
description: Указывает, что задача выполняется в феврале.
ms.assetid: 871449f8-fa3a-4e1f-be36-bc5c98125721
keywords:
- планировщик задач февраля
topic_type:
- apiref
api_name:
- February
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 727751964bfb9a752eb1190f8c7d3a86de2a9413
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672847"
---
# <a name="february-monthstype-element"></a><span data-ttu-id="743da-104">Элемент Февраль (Монсстипе)</span><span class="sxs-lookup"><span data-stu-id="743da-104">February (monthsType) Element</span></span>

<span data-ttu-id="743da-105">Указывает, что задача выполняется в феврале.</span><span class="sxs-lookup"><span data-stu-id="743da-105">Specifies that the task runs in February.</span></span>

``` syntax
<xs:element name="February">
    <xs:complexType />
</xs:element>
```

<span data-ttu-id="743da-106">Элемент **Февраль** определяется сложным типом [**монсстипе**](taskschedulerschema-monthstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="743da-106">The **February** element is defined by the [**monthsType**](taskschedulerschema-monthstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="743da-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="743da-107">Parent element</span></span>



| <span data-ttu-id="743da-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="743da-108">Element</span></span>                                                                                                          | <span data-ttu-id="743da-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="743da-109">Derived from</span></span>                                                     | <span data-ttu-id="743da-110">Описание</span><span class="sxs-lookup"><span data-stu-id="743da-110">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="743da-111">**Месяцы (Монслидайофвиксчедулетипе)**</span><span class="sxs-lookup"><span data-stu-id="743da-111">**Months (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-months-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="743da-112">**монсстипе**</span><span class="sxs-lookup"><span data-stu-id="743da-112">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="743da-113">Указывает месяцы года, в течение которых задача выполняется для ежемесячного расписания недели.</span><span class="sxs-lookup"><span data-stu-id="743da-113">Specifies the months of the year during which the task runs for a monthly day-of-week schedule.</span></span><br/> |
| [<span data-ttu-id="743da-114">**Месяцы (Монслисчедулетипе)**</span><span class="sxs-lookup"><span data-stu-id="743da-114">**Months (monthlyScheduleType)**</span></span>](taskschedulerschema-months-monthlyscheduletype-element.md)                   | [<span data-ttu-id="743da-115">**монсстипе**</span><span class="sxs-lookup"><span data-stu-id="743da-115">**monthsType**</span></span>](taskschedulerschema-monthstype-complextype.md) | <span data-ttu-id="743da-116">Указывает месяцы года, в течение которых задача выполняется для ежемесячного расписания.</span><span class="sxs-lookup"><span data-stu-id="743da-116">Specifies the months of the year during which the task runs for a monthly schedule.</span></span><br/>             |



## <a name="examples"></a><span data-ttu-id="743da-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="743da-117">Examples</span></span>

<span data-ttu-id="743da-118">Следующий XML-код определяет календарь месяцев, который запускает задачу в феврале.</span><span class="sxs-lookup"><span data-stu-id="743da-118">The following XML defines a months calendar that runs the task in February.</span></span>


```XML
<Months>
    <February/>
</Months>
```



## <a name="requirements"></a><span data-ttu-id="743da-119">Требования</span><span class="sxs-lookup"><span data-stu-id="743da-119">Requirements</span></span>



| <span data-ttu-id="743da-120">Требование</span><span class="sxs-lookup"><span data-stu-id="743da-120">Requirement</span></span> | <span data-ttu-id="743da-121">Значение</span><span class="sxs-lookup"><span data-stu-id="743da-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="743da-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="743da-122">Minimum supported client</span></span><br/> | <span data-ttu-id="743da-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="743da-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="743da-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="743da-124">Minimum supported server</span></span><br/> | <span data-ttu-id="743da-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="743da-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="743da-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="743da-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="743da-127">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="743da-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="743da-128">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="743da-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





