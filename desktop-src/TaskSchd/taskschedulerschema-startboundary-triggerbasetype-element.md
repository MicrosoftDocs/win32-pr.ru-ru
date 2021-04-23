---
title: Стартбаундари (Тригжербасетипе), элемент
description: Указывает дату и время активации триггера.
ms.assetid: 95a62ae5-4eba-49df-a25f-0d1181772833
keywords:
- планировщик задач элемента Стартбаундари
topic_type:
- apiref
api_name:
- StartBoundary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8d6adf90de2f3b199f98737996fe732f342787b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135415"
---
# <a name="startboundary-triggerbasetype-element"></a><span data-ttu-id="c0054-104">Стартбаундари (Тригжербасетипе), элемент</span><span class="sxs-lookup"><span data-stu-id="c0054-104">StartBoundary (triggerBaseType) Element</span></span>

<span data-ttu-id="c0054-105">Указывает дату и время активации триггера.</span><span class="sxs-lookup"><span data-stu-id="c0054-105">Specifies the date and time when the trigger is activated.</span></span>

``` syntax
<xs:element name="StartBoundary"
    type="dateTime"
 />
```

<span data-ttu-id="c0054-106">Элемент **стартбаундари** определяется сложным типом [**тригжербасетипе**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c0054-106">The **StartBoundary** element is defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="c0054-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="c0054-107">Parent element</span></span>



| <span data-ttu-id="c0054-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="c0054-108">Element</span></span>                                                                                     | <span data-ttu-id="c0054-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="c0054-109">Derived from</span></span>                                                                               | <span data-ttu-id="c0054-110">Описание</span><span class="sxs-lookup"><span data-stu-id="c0054-110">Description</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c0054-111">**буттригжер**</span><span class="sxs-lookup"><span data-stu-id="c0054-111">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [<span data-ttu-id="c0054-112">**буттригжертипе**</span><span class="sxs-lookup"><span data-stu-id="c0054-112">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                 | <span data-ttu-id="c0054-113">Указывает триггер, который запускает задачу при загрузке системы.</span><span class="sxs-lookup"><span data-stu-id="c0054-113">Specifies a trigger that starts a task when the system is booted.</span></span><br/>                 |
| [<span data-ttu-id="c0054-114">**календартригжер**</span><span class="sxs-lookup"><span data-stu-id="c0054-114">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [<span data-ttu-id="c0054-115">**календартригжертипе**</span><span class="sxs-lookup"><span data-stu-id="c0054-115">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)         | <span data-ttu-id="c0054-116">Задает ежедневный, еженедельный, ежемесячный или ежемесячный триггер (DOW) в день недели.</span><span class="sxs-lookup"><span data-stu-id="c0054-116">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/>   |
| [<span data-ttu-id="c0054-117">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="c0054-117">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [<span data-ttu-id="c0054-118">**евенттригжертипе**</span><span class="sxs-lookup"><span data-stu-id="c0054-118">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)               | <span data-ttu-id="c0054-119">Указывает триггер, который запускает задачу при возникновении системного события.</span><span class="sxs-lookup"><span data-stu-id="c0054-119">Specifies a trigger that starts a task when a system event occurs.</span></span><br/>                |
| [<span data-ttu-id="c0054-120">**идлетригжер**</span><span class="sxs-lookup"><span data-stu-id="c0054-120">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [<span data-ttu-id="c0054-121">**идлетригжертипе**</span><span class="sxs-lookup"><span data-stu-id="c0054-121">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                 | <span data-ttu-id="c0054-122">Указывает триггер, который запускает задачу при переходе компьютера в состояние простоя.</span><span class="sxs-lookup"><span data-stu-id="c0054-122">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span><br/> |
| [<span data-ttu-id="c0054-123">**логонтригжер**</span><span class="sxs-lookup"><span data-stu-id="c0054-123">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)               | [<span data-ttu-id="c0054-124">**логонтригжертипе**</span><span class="sxs-lookup"><span data-stu-id="c0054-124">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)               | <span data-ttu-id="c0054-125">Указывает триггер, который запускает задачу при входе пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="c0054-125">Specifies a trigger that starts a task when a user logs on.</span></span><br/>                       |
| [<span data-ttu-id="c0054-126">**регистратионтригжер**</span><span class="sxs-lookup"><span data-stu-id="c0054-126">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="c0054-127">**регистратионтригжертипе**</span><span class="sxs-lookup"><span data-stu-id="c0054-127">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="c0054-128">Указывает триггер, который запускает задачу при регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="c0054-128">Specifies a trigger that starts a task when the task is registered.</span></span><br/>               |
| [<span data-ttu-id="c0054-129">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="c0054-129">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [<span data-ttu-id="c0054-130">**тиметригжертипе**</span><span class="sxs-lookup"><span data-stu-id="c0054-130">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                 | <span data-ttu-id="c0054-131">Указывает триггер, который запускает задачу при активации триггера.</span><span class="sxs-lookup"><span data-stu-id="c0054-131">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/>             |



## <a name="remarks"></a><span data-ttu-id="c0054-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c0054-132">Remarks</span></span>

<span data-ttu-id="c0054-133">**<StartBoundary>** Элемент является обязательным элементом для триггеров времени и календаря ( [**<TimeTrigger>**](taskschedulerschema-timetrigger-triggergroup-element.md) и [**<CalendarTrigger>**](taskschedulerschema-calendartrigger-triggergroup-element.md) ).</span><span class="sxs-lookup"><span data-stu-id="c0054-133">The **<StartBoundary>** element is a required element for time and calendar triggers ([**<TimeTrigger>**](taskschedulerschema-timetrigger-triggergroup-element.md) and [**<CalendarTrigger>**](taskschedulerschema-calendartrigger-triggergroup-element.md)).</span></span>

<span data-ttu-id="c0054-134">Для разработки сценариев конечная граница указывается с помощью свойства [**Trigger. стартбаундари**](trigger-startboundary.md) , наследуемого всеми объектами триггера.</span><span class="sxs-lookup"><span data-stu-id="c0054-134">For scripting development, the end boundary is specified using the [**Trigger.StartBoundary**](trigger-startboundary.md) property that is inherited by the all trigger objects.</span></span>

<span data-ttu-id="c0054-135">Для разработки на C++ конечная граница указывается с помощью свойства [**итригжер:: стартбаундари**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_startboundary) , которое наследуется интерфейсами триггера ALL.</span><span class="sxs-lookup"><span data-stu-id="c0054-135">For C++ development, the end boundary is specified using the [**ITrigger::StartBoundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_startboundary) property that is inherited by the all trigger interfaces.</span></span>

## <a name="examples"></a><span data-ttu-id="c0054-136">Примеры</span><span class="sxs-lookup"><span data-stu-id="c0054-136">Examples</span></span>

<span data-ttu-id="c0054-137">Следующий XML-код определяет элемент триггера загрузки, который определяет начальную границу 1 января 2005:8:00 AM.</span><span class="sxs-lookup"><span data-stu-id="c0054-137">The following XML defines a boot trigger element that defines a start boundary of January 1, 2005: 8:00 AM.</span></span>


```XML
<BootTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T08:00:00</EndBoundary>
    <Enabled>true</Enabled>
    <Repetition></Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
    <Delay><Delay>
 </BootTrigger>
```



## <a name="requirements"></a><span data-ttu-id="c0054-138">Требования</span><span class="sxs-lookup"><span data-stu-id="c0054-138">Requirements</span></span>



| <span data-ttu-id="c0054-139">Требование</span><span class="sxs-lookup"><span data-stu-id="c0054-139">Requirement</span></span> | <span data-ttu-id="c0054-140">Значение</span><span class="sxs-lookup"><span data-stu-id="c0054-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c0054-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c0054-141">Minimum supported client</span></span><br/> | <span data-ttu-id="c0054-142">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c0054-142">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c0054-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c0054-143">Minimum supported server</span></span><br/> | <span data-ttu-id="c0054-144">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c0054-144">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c0054-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c0054-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0054-146">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="c0054-146">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="c0054-147">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="c0054-147">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





