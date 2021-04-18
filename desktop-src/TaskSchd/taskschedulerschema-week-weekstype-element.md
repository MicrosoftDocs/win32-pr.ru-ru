---
title: Week (Викстипе), элемент
description: Указывает конкретную неделю месяца.
ms.assetid: 0cec07da-e9e7-43ef-9f54-48d00114ba1f
keywords:
- Элемент Week планировщик задач
topic_type:
- apiref
api_name:
- Week
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0487aa07e1f1132c998b6cb2ba0f518a9db57ce2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682092"
---
# <a name="week-weekstype-element"></a><span data-ttu-id="c4e54-104">Week (Викстипе), элемент</span><span class="sxs-lookup"><span data-stu-id="c4e54-104">Week (weeksType) Element</span></span>

<span data-ttu-id="c4e54-105">Указывает конкретную неделю месяца.</span><span class="sxs-lookup"><span data-stu-id="c4e54-105">Specifies a specific week of the month.</span></span>

``` syntax
<xs:element name="Week"
    type="weekType"
 />
```

<span data-ttu-id="c4e54-106">Элемент **Week** определяется сложным типом [**викстипе**](taskschedulerschema-weekstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c4e54-106">The **Week** element is defined by the [**weeksType**](taskschedulerschema-weekstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="c4e54-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="c4e54-107">Parent element</span></span>



| <span data-ttu-id="c4e54-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="c4e54-108">Element</span></span>                                                                                                        | <span data-ttu-id="c4e54-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="c4e54-109">Derived from</span></span>                                                   | <span data-ttu-id="c4e54-110">Описание</span><span class="sxs-lookup"><span data-stu-id="c4e54-110">Description</span></span>                                                           |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="c4e54-111">**Weeks (Монслидайофвиксчедулетипе)**</span><span class="sxs-lookup"><span data-stu-id="c4e54-111">**Weeks (monthlyDayOfWeekScheduleType)**</span></span>](taskschedulerschema-weeks-monthlydayofweekscheduletype-element.md) | [<span data-ttu-id="c4e54-112">**викстипе**</span><span class="sxs-lookup"><span data-stu-id="c4e54-112">**weeksType**</span></span>](taskschedulerschema-weekstype-complextype.md) | <span data-ttu-id="c4e54-113">Указывает недели месяца, в которых выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="c4e54-113">Specifies the weeks of the month in which the task is run.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c4e54-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c4e54-114">Remarks</span></span>

<span data-ttu-id="c4e54-115">При указании недель месяца используйте числа 1-4 в течение первых четырех недель месяца или используйте строку Last, чтобы указать последнюю неделю месяца.</span><span class="sxs-lookup"><span data-stu-id="c4e54-115">When specifying the weeks of the month, use the numbers 1-4 for the first four weeks of the month or use the string "Last" to indicate that last week of the month.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4e54-116">Требования</span><span class="sxs-lookup"><span data-stu-id="c4e54-116">Requirements</span></span>



| <span data-ttu-id="c4e54-117">Требование</span><span class="sxs-lookup"><span data-stu-id="c4e54-117">Requirement</span></span> | <span data-ttu-id="c4e54-118">Значение</span><span class="sxs-lookup"><span data-stu-id="c4e54-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c4e54-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c4e54-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c4e54-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c4e54-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c4e54-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c4e54-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c4e54-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c4e54-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c4e54-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c4e54-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4e54-124">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="c4e54-124">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="c4e54-125">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="c4e54-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





