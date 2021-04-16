---
title: Элемент Delay (Евенттригжертипе)
description: Указывает промежуток времени между моментом возникновения события и моментом запуска задачи.
ms.assetid: b38bebc7-9818-41f0-a277-cb0e63c28d86
keywords:
- планировщик задач элемента Delay
topic_type:
- apiref
api_name:
- Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: de1117ff4f7e0f823b1b213721521e1b526125bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672905"
---
# <a name="delay-eventtriggertype-element"></a><span data-ttu-id="ce409-104">Элемент Delay (Евенттригжертипе)</span><span class="sxs-lookup"><span data-stu-id="ce409-104">Delay (eventTriggerType) Element</span></span>

<span data-ttu-id="ce409-105">Указывает промежуток времени между моментом возникновения события и моментом запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="ce409-105">Specifies the amount of time between when the event occurs and when the task is started.</span></span> <span data-ttu-id="ce409-106">Формат этой строки — Пнинмндтнхнмнс, где Нью-то число лет, nM — это количество месяцев, а — число дней, равное, т. е. в качестве разделителя даты и времени, nH — это количество часов, а в качестве значения nS — количество секунд (например, PT5M указывает 5 минут, а P1M4DT2H5M — один месяц, четыре дня, два часа и пять минут).</span><span class="sxs-lookup"><span data-stu-id="ce409-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="ce409-107">Дополнительные сведения о типе длительности см. в разделе <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="ce409-107">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

<span data-ttu-id="ce409-108">Элемент **delay** определяется сложным типом [**евенттригжертипе**](taskschedulerschema-eventtriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="ce409-108">The **Delay** element is defined by the [**eventTriggerType**](taskschedulerschema-eventtriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="ce409-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="ce409-109">Parent element</span></span>



| <span data-ttu-id="ce409-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="ce409-110">Element</span></span>                                                                       | <span data-ttu-id="ce409-111">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="ce409-111">Derived from</span></span>                                                                 | <span data-ttu-id="ce409-112">Описание</span><span class="sxs-lookup"><span data-stu-id="ce409-112">Description</span></span>                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="ce409-113">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="ce409-113">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md) | [<span data-ttu-id="ce409-114">**евенттригжертипе**</span><span class="sxs-lookup"><span data-stu-id="ce409-114">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md) | <span data-ttu-id="ce409-115">Указывает триггер, который запускает задачу при возникновении системного события.</span><span class="sxs-lookup"><span data-stu-id="ce409-115">Specifies a trigger that starts a task when a system event occurs.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ce409-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ce409-116">Remarks</span></span>

<span data-ttu-id="ce409-117">Для разработки скриптов задержка триггера события задается свойством [**EventTrigger. Delay**](eventtrigger-delay.md) .</span><span class="sxs-lookup"><span data-stu-id="ce409-117">For script development, the event trigger delay is specified by the [**EventTrigger.Delay**](eventtrigger-delay.md) property.</span></span>

<span data-ttu-id="ce409-118">Для разработки на C++ задержка триггера события задается свойством [**иевенттригжер::D елай**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_delay) .</span><span class="sxs-lookup"><span data-stu-id="ce409-118">For C++ development, the event trigger delay is specified by the [**IEventTrigger::Delay**](/windows/desktop/api/taskschd/nf-taskschd-ieventtrigger-get_delay) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce409-119">Требования</span><span class="sxs-lookup"><span data-stu-id="ce409-119">Requirements</span></span>



| <span data-ttu-id="ce409-120">Требование</span><span class="sxs-lookup"><span data-stu-id="ce409-120">Requirement</span></span> | <span data-ttu-id="ce409-121">Значение</span><span class="sxs-lookup"><span data-stu-id="ce409-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ce409-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ce409-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ce409-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ce409-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ce409-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ce409-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ce409-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ce409-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ce409-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ce409-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce409-127">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="ce409-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="ce409-128">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="ce409-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





