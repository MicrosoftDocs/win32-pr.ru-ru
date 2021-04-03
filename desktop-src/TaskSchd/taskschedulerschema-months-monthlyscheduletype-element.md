---
title: Months (Монслисчедулетипе), элемент
description: Указывает месяцы года, в течение которых задача выполняется для ежемесячного расписания.
ms.assetid: 71c9f7ac-01fc-4837-bccf-1869df2bc24e
keywords:
- Элемент months планировщик задач
topic_type:
- apiref
api_name:
- Months
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0ed40fd2466f8962f839f39e7addd3b7e1bc33eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137026"
---
# <a name="months-monthlyscheduletype-element"></a><span data-ttu-id="6de2d-104">Months (Монслисчедулетипе), элемент</span><span class="sxs-lookup"><span data-stu-id="6de2d-104">Months (monthlyScheduleType) Element</span></span>

<span data-ttu-id="6de2d-105">Указывает месяцы года, в течение которых задача выполняется для ежемесячного расписания.</span><span class="sxs-lookup"><span data-stu-id="6de2d-105">Specifies the months of the year during which the task runs for a monthly schedule.</span></span>

``` syntax
<xs:element name="Months"
    type="monthsType"
 />
```

<span data-ttu-id="6de2d-106">Элемент **months** определяется сложным типом [**монслисчедулетипе**](taskschedulerschema-monthlyscheduletype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="6de2d-106">The **Months** element is defined by the [**monthlyScheduleType**](taskschedulerschema-monthlyscheduletype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="6de2d-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="6de2d-107">Parent element</span></span>



| <span data-ttu-id="6de2d-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="6de2d-108">Element</span></span>                                                                                    | <span data-ttu-id="6de2d-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="6de2d-109">Derived from</span></span>                                                                       | <span data-ttu-id="6de2d-110">Описание</span><span class="sxs-lookup"><span data-stu-id="6de2d-110">Description</span></span>                               |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="6de2d-111">**счедулебимонс**</span><span class="sxs-lookup"><span data-stu-id="6de2d-111">**ScheduleByMonth**</span></span>](taskschedulerschema-schedulebymonth-calendartriggertype-element.md) | [<span data-ttu-id="6de2d-112">**монслисчедулетипе**</span><span class="sxs-lookup"><span data-stu-id="6de2d-112">**monthlyScheduleType**</span></span>](taskschedulerschema-monthlyscheduletype-complextype.md) | <span data-ttu-id="6de2d-113">Указывает ежемесячное расписание.</span><span class="sxs-lookup"><span data-stu-id="6de2d-113">Specifies a monthly schedule.</span></span> <br/> |



## <a name="child-elements"></a><span data-ttu-id="6de2d-114">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="6de2d-114">Child elements</span></span>



| <span data-ttu-id="6de2d-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="6de2d-115">Element</span></span>                                                                            | <span data-ttu-id="6de2d-116">Тип</span><span class="sxs-lookup"><span data-stu-id="6de2d-116">Type</span></span> | <span data-ttu-id="6de2d-117">Описание</span><span class="sxs-lookup"><span data-stu-id="6de2d-117">Description</span></span>                                           |
|------------------------------------------------------------------------------------|------|-------------------------------------------------------|
| [<span data-ttu-id="6de2d-118">**Апрель (Монсстипе)**</span><span class="sxs-lookup"><span data-stu-id="6de2d-118">**April (monthsType)**</span></span>](taskschedulerschema-april-monthstype-element.md)         |      | <span data-ttu-id="6de2d-119">Указывает, что задача выполняется в апреле.</span><span class="sxs-lookup"><span data-stu-id="6de2d-119">Specifies that the task runs in April.</span></span><br/>     |
| [<span data-ttu-id="6de2d-120">**Август (Монсстипе)**</span><span class="sxs-lookup"><span data-stu-id="6de2d-120">**August (monthsType)**</span></span>](taskschedulerschema-august-monthstype-element.md)       |      | <span data-ttu-id="6de2d-121">Указывает, что задача выполняется в августе.</span><span class="sxs-lookup"><span data-stu-id="6de2d-121">Specifies that the task runs in August.</span></span><br/>    |
| [<span data-ttu-id="6de2d-122">**Декабрь (Монсстипе)**</span><span class="sxs-lookup"><span data-stu-id="6de2d-122">**December (monthsType)**</span></span>](taskschedulerschema-december-monthstype-element.md)   |      | <span data-ttu-id="6de2d-123">Указывает, что задача выполняется в декабре.</span><span class="sxs-lookup"><span data-stu-id="6de2d-123">Specifies that the task runs in December.</span></span><br/>  |
| [<span data-ttu-id="6de2d-124">**Февраль (Монсстипе)**</span><span class="sxs-lookup"><span data-stu-id="6de2d-124">**February (monthsType)**</span></span>](taskschedulerschema-february-monthstype-element.md)   |      | <span data-ttu-id="6de2d-125">Указывает, что задача выполняется в феврале.</span><span class="sxs-lookup"><span data-stu-id="6de2d-125">Specifies that the task runs in February.</span></span><br/>  |
| [<span data-ttu-id="6de2d-126">**Январь (Монсстипе)**</span><span class="sxs-lookup"><span data-stu-id="6de2d-126">**January (monthsType)**</span></span>](taskschedulerschema-january-monthstype-element.md)     |      | <span data-ttu-id="6de2d-127">Указывает, что задача выполняется в январе.</span><span class="sxs-lookup"><span data-stu-id="6de2d-127">Specifies that the task runs in January.</span></span><br/>   |
| [<span data-ttu-id="6de2d-128">**Июль (Монсстипе)**</span><span class="sxs-lookup"><span data-stu-id="6de2d-128">**July (monthsType)**</span></span>](taskschedulerschema-july-monthstype-element.md)           |      | <span data-ttu-id="6de2d-129">Указывает, что задача выполняется в июле.</span><span class="sxs-lookup"><span data-stu-id="6de2d-129">Specifies that the task runs in July.</span></span><br/>      |
| [<span data-ttu-id="6de2d-130">**Июнь (Монсстипе)**</span><span class="sxs-lookup"><span data-stu-id="6de2d-130">**June (monthsType)**</span></span>](taskschedulerschema-june-monthstype-element.md)           |      | <span data-ttu-id="6de2d-131">Указывает, что задача выполняется в июне.</span><span class="sxs-lookup"><span data-stu-id="6de2d-131">Specifies that the task runs in June.</span></span><br/>      |
| [<span data-ttu-id="6de2d-132">**Март (Монсстипе)**</span><span class="sxs-lookup"><span data-stu-id="6de2d-132">**March (monthsType)**</span></span>](taskschedulerschema-march-monthstype-element.md)         |      | <span data-ttu-id="6de2d-133">Указывает, что задача выполняется в марте.</span><span class="sxs-lookup"><span data-stu-id="6de2d-133">Specifies that the task runs in March.</span></span><br/>     |
| [<span data-ttu-id="6de2d-134">**Май (Монсстипе)**</span><span class="sxs-lookup"><span data-stu-id="6de2d-134">**May (monthsType)**</span></span>](taskschedulerschema-may-monthstype-element.md)             |      | <span data-ttu-id="6de2d-135">Указывает, что задача выполняется в Май.</span><span class="sxs-lookup"><span data-stu-id="6de2d-135">Specifies that the task runs in May.</span></span><br/>       |
| [<span data-ttu-id="6de2d-136">**Ноябрь (Монсстипе)**</span><span class="sxs-lookup"><span data-stu-id="6de2d-136">**November (monthsType)**</span></span>](taskschedulerschema-november-monthstype-element.md)   |      | <span data-ttu-id="6de2d-137">Указывает, что задача выполняется в ноябре.</span><span class="sxs-lookup"><span data-stu-id="6de2d-137">Specifies that the task runs in November.</span></span><br/>  |
| [<span data-ttu-id="6de2d-138">**Октябрь (Монсстипе)**</span><span class="sxs-lookup"><span data-stu-id="6de2d-138">**October (monthsType)**</span></span>](taskschedulerschema-october-monthstype-element.md)     |      | <span data-ttu-id="6de2d-139">Указывает, что задача выполняется в октябре.</span><span class="sxs-lookup"><span data-stu-id="6de2d-139">Specifies that the task runs in October.</span></span><br/>   |
| [<span data-ttu-id="6de2d-140">**Сентябрь (Монсстипе)**</span><span class="sxs-lookup"><span data-stu-id="6de2d-140">**September (monthsType)**</span></span>](taskschedulerschema-september-monthstype-element.md) |      | <span data-ttu-id="6de2d-141">Указывает, что задача выполняется в сентябре.</span><span class="sxs-lookup"><span data-stu-id="6de2d-141">Specifies that the task runs in September.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6de2d-142">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6de2d-142">Remarks</span></span>

<span data-ttu-id="6de2d-143">Для разработки сценариев месяцы расписания задаются с помощью свойства [**монслитригжер. монссофеар**](monthlytrigger-monthsofyear.md) .</span><span class="sxs-lookup"><span data-stu-id="6de2d-143">For script development, the months of the schedule are specified using the [**MonthlyTrigger.MonthsOfYear**](monthlytrigger-monthsofyear.md) property.</span></span>

<span data-ttu-id="6de2d-144">Для разработки на C++ месяцы расписания указываются с помощью свойства [**имонслитригжер:: монссофеар**](/windows/desktop/api/taskschd/nf-taskschd-imonthlytrigger-get_monthsofyear) .</span><span class="sxs-lookup"><span data-stu-id="6de2d-144">For C++ development, the months of the schedule are specified using the [**IMonthlyTrigger::MonthsOfYear**](/windows/desktop/api/taskschd/nf-taskschd-imonthlytrigger-get_monthsofyear) property.</span></span>

## <a name="examples"></a><span data-ttu-id="6de2d-145">Примеры</span><span class="sxs-lookup"><span data-stu-id="6de2d-145">Examples</span></span>

<span data-ttu-id="6de2d-146">Следующий XML-код определяет месячный календарь, который запускает задачу в первый и 15-й день каждого месяца года.</span><span class="sxs-lookup"><span data-stu-id="6de2d-146">The following XML defines a monthly calendar that starts the task on the 1st and 15th day of every month of the year.</span></span>


```XML
</ScheduleByMonth>
    <DaysOfMonth>
        <Day>1</Day>
        <Day>15</Day>
    </DaysOfMonth
    <Months>
        <January/>
        <February/>
        <March/>
        <April/>
        <May/>
        <June/>
        <July/>
        <August/>
        <September/>
        <October/>
        <November/>
        <December/>
    <Months>
</ScheduleByMonth>
```



## <a name="requirements"></a><span data-ttu-id="6de2d-147">Требования</span><span class="sxs-lookup"><span data-stu-id="6de2d-147">Requirements</span></span>



| <span data-ttu-id="6de2d-148">Требование</span><span class="sxs-lookup"><span data-stu-id="6de2d-148">Requirement</span></span> | <span data-ttu-id="6de2d-149">Значение</span><span class="sxs-lookup"><span data-stu-id="6de2d-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6de2d-150">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6de2d-150">Minimum supported client</span></span><br/> | <span data-ttu-id="6de2d-151">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6de2d-151">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6de2d-152">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6de2d-152">Minimum supported server</span></span><br/> | <span data-ttu-id="6de2d-153">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6de2d-153">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6de2d-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6de2d-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6de2d-155">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="6de2d-155">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="6de2d-156">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="6de2d-156">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





