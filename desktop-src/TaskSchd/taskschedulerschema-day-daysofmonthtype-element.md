---
title: Day (Дайсофмонстипе), элемент
description: Указывает день месяца, в который выполняется задача.
ms.assetid: b213df09-9301-4a51-b000-edfdafbe861e
keywords:
- Элемент Day планировщик задач
topic_type:
- apiref
api_name:
- Day
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1e8e06169d2b758264f181263a5cb717977a1602
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071352"
---
# <a name="day-daysofmonthtype-element"></a><span data-ttu-id="a8483-104">Day (Дайсофмонстипе), элемент</span><span class="sxs-lookup"><span data-stu-id="a8483-104">Day (daysOfMonthType) Element</span></span>

<span data-ttu-id="a8483-105">Указывает день месяца, в который выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="a8483-105">Specifies a day of the month during which the task runs.</span></span>

``` syntax
<xs:element name="Day"
    type="dayOfMonthType"
 />
```

<span data-ttu-id="a8483-106">Элемент **Day** определяется сложным типом [**дайсофмонстипе**](taskschedulerschema-daysofmonthtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="a8483-106">The **Day** element is defined by the [**daysOfMonthType**](taskschedulerschema-daysofmonthtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="a8483-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="a8483-107">Parent element</span></span>



| <span data-ttu-id="a8483-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="a8483-108">Element</span></span>                                                                            | <span data-ttu-id="a8483-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="a8483-109">Derived from</span></span>                                                               | <span data-ttu-id="a8483-110">Описание</span><span class="sxs-lookup"><span data-stu-id="a8483-110">Description</span></span>                                                            |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="a8483-111">**DaysOfMonth**</span><span class="sxs-lookup"><span data-stu-id="a8483-111">**DaysOfMonth**</span></span>](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) | [<span data-ttu-id="a8483-112">**дайсофмонстипе**</span><span class="sxs-lookup"><span data-stu-id="a8483-112">**daysOfMonthType**</span></span>](taskschedulerschema-daysofmonthtype-complextype.md) | <span data-ttu-id="a8483-113">Указывает дни месяца, в которые выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="a8483-113">Specifies the days of the month during which the task runs.</span></span><br/> |



## <a name="examples"></a><span data-ttu-id="a8483-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="a8483-114">Examples</span></span>

<span data-ttu-id="a8483-115">Следующий XML-код определяет дни ежемесячного календаря, в которых задача выполняется в первый и 15-й день месяца.</span><span class="sxs-lookup"><span data-stu-id="a8483-115">The following XML defines the days portion of a monthly calendar that runs the task on the 1st and 15th day of the month.</span></span>


```XML
<DaysOfMonth>
    <Day>1</Day>
    <Day>15</Day>
</DaysOfMonth>
```



## <a name="requirements"></a><span data-ttu-id="a8483-116">Требования</span><span class="sxs-lookup"><span data-stu-id="a8483-116">Requirements</span></span>



| <span data-ttu-id="a8483-117">Требование</span><span class="sxs-lookup"><span data-stu-id="a8483-117">Requirement</span></span> | <span data-ttu-id="a8483-118">Значение</span><span class="sxs-lookup"><span data-stu-id="a8483-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a8483-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a8483-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a8483-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a8483-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a8483-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a8483-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a8483-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a8483-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a8483-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a8483-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8483-124">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="a8483-124">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





