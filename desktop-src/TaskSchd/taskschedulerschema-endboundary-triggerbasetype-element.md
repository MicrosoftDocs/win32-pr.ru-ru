---
title: Ендбаундари (Тригжербасетипе), элемент
description: Указывает дату и время деактивации триггера. Триггер не может запустить задачу после ее деактивации.
ms.assetid: 84731c0b-3fb8-44dd-be1a-67547add1f9e
keywords:
- планировщик задач элемента Ендбаундари
topic_type:
- apiref
api_name:
- EndBoundary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d687655498301595c1ab888fcc179ec0694f0aef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681791"
---
# <a name="endboundary-triggerbasetype-element"></a><span data-ttu-id="6a9d4-105">Ендбаундари (Тригжербасетипе), элемент</span><span class="sxs-lookup"><span data-stu-id="6a9d4-105">EndBoundary (triggerBaseType) Element</span></span>

<span data-ttu-id="6a9d4-106">Указывает дату и время деактивации триггера.</span><span class="sxs-lookup"><span data-stu-id="6a9d4-106">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="6a9d4-107">Триггер не может запустить задачу после ее деактивации.</span><span class="sxs-lookup"><span data-stu-id="6a9d4-107">The trigger cannot start the task after it is deactivated.</span></span>

``` syntax
<xs:element name="EndBoundary"
    type="dateTime"
 />
```

<span data-ttu-id="6a9d4-108">Элемент **ендбаундари** определяется сложным типом [**тригжербасетипе**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="6a9d4-108">The **EndBoundary** element is defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="6a9d4-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="6a9d4-109">Parent element</span></span>



| <span data-ttu-id="6a9d4-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="6a9d4-110">Element</span></span>                                                                                     | <span data-ttu-id="6a9d4-111">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="6a9d4-111">Derived from</span></span>                                                                               | <span data-ttu-id="6a9d4-112">Описание</span><span class="sxs-lookup"><span data-stu-id="6a9d4-112">Description</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6a9d4-113">**буттригжер**</span><span class="sxs-lookup"><span data-stu-id="6a9d4-113">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [<span data-ttu-id="6a9d4-114">**буттригжертипе**</span><span class="sxs-lookup"><span data-stu-id="6a9d4-114">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                 | <span data-ttu-id="6a9d4-115">Указывает триггер, который запускает задачу при загрузке системы.</span><span class="sxs-lookup"><span data-stu-id="6a9d4-115">Specifies a trigger that starts a task when the system is booted.</span></span><br/>                 |
| [<span data-ttu-id="6a9d4-116">**календартригжер**</span><span class="sxs-lookup"><span data-stu-id="6a9d4-116">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [<span data-ttu-id="6a9d4-117">**календартригжертипе**</span><span class="sxs-lookup"><span data-stu-id="6a9d4-117">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)         | <span data-ttu-id="6a9d4-118">Задает ежедневный, еженедельный, ежемесячный или ежемесячный триггер (DOW) в день недели.</span><span class="sxs-lookup"><span data-stu-id="6a9d4-118">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/>   |
| [<span data-ttu-id="6a9d4-119">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="6a9d4-119">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [<span data-ttu-id="6a9d4-120">**евенттригжертипе**</span><span class="sxs-lookup"><span data-stu-id="6a9d4-120">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)               | <span data-ttu-id="6a9d4-121">Указывает триггер, который запускает задачу при возникновении системного события.</span><span class="sxs-lookup"><span data-stu-id="6a9d4-121">Specifies a trigger that starts a task when a system event occurs.</span></span><br/>                |
| [<span data-ttu-id="6a9d4-122">**идлетригжер**</span><span class="sxs-lookup"><span data-stu-id="6a9d4-122">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [<span data-ttu-id="6a9d4-123">**идлетригжертипе**</span><span class="sxs-lookup"><span data-stu-id="6a9d4-123">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                 | <span data-ttu-id="6a9d4-124">Указывает триггер, который запускает задачу при переходе компьютера в состояние простоя.</span><span class="sxs-lookup"><span data-stu-id="6a9d4-124">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span><br/> |
| [<span data-ttu-id="6a9d4-125">**логонтригжер**</span><span class="sxs-lookup"><span data-stu-id="6a9d4-125">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)               | [<span data-ttu-id="6a9d4-126">**логонтригжертипе**</span><span class="sxs-lookup"><span data-stu-id="6a9d4-126">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)               | <span data-ttu-id="6a9d4-127">Указывает триггер, который запускает задачу при входе пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="6a9d4-127">Specifies a trigger that starts a task when a user logs on.</span></span><br/>                       |
| [<span data-ttu-id="6a9d4-128">**регистратионтригжер**</span><span class="sxs-lookup"><span data-stu-id="6a9d4-128">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="6a9d4-129">**регистратионтригжертипе**</span><span class="sxs-lookup"><span data-stu-id="6a9d4-129">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="6a9d4-130">Указывает триггер, который запускает задачу при регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="6a9d4-130">Specifies a trigger that starts a task when the task is registered.</span></span><br/>               |
| [<span data-ttu-id="6a9d4-131">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="6a9d4-131">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [<span data-ttu-id="6a9d4-132">**тиметригжертипе**</span><span class="sxs-lookup"><span data-stu-id="6a9d4-132">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                 | <span data-ttu-id="6a9d4-133">Указывает триггер, который запускает задачу при активации триггера.</span><span class="sxs-lookup"><span data-stu-id="6a9d4-133">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/>             |



## <a name="remarks"></a><span data-ttu-id="6a9d4-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6a9d4-134">Remarks</span></span>

<span data-ttu-id="6a9d4-135">Для разработки сценариев конечная граница указывается с помощью свойства [**Trigger. ендбаундари**](trigger-endboundary.md) , наследуемого всеми объектами триггера.</span><span class="sxs-lookup"><span data-stu-id="6a9d4-135">For scripting development, the end boundary is specified using the [**Trigger.EndBoundary**](trigger-endboundary.md) property that is inherited by the all trigger objects.</span></span>

<span data-ttu-id="6a9d4-136">Для разработки на C++ конечная граница указывается с помощью свойства [**итригжер:: ендбаундари**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_endboundary) , которое наследуется интерфейсами триггера ALL.</span><span class="sxs-lookup"><span data-stu-id="6a9d4-136">For C++ development, the end boundary is specified using the [**ITrigger::EndBoundary**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_endboundary) property that is inherited by the all trigger interfaces.</span></span>

## <a name="examples"></a><span data-ttu-id="6a9d4-137">Примеры</span><span class="sxs-lookup"><span data-stu-id="6a9d4-137">Examples</span></span>

<span data-ttu-id="6a9d4-138">Следующий XML-код определяет элемент триггера Boot, определяющий конечную границу 1 января 2007:8:00 AM.</span><span class="sxs-lookup"><span data-stu-id="6a9d4-138">The following XML defines a boot trigger element that defines an end boundary of January 1, 2007: 8:00 AM.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="6a9d4-139">Требования</span><span class="sxs-lookup"><span data-stu-id="6a9d4-139">Requirements</span></span>



| <span data-ttu-id="6a9d4-140">Требование</span><span class="sxs-lookup"><span data-stu-id="6a9d4-140">Requirement</span></span> | <span data-ttu-id="6a9d4-141">Значение</span><span class="sxs-lookup"><span data-stu-id="6a9d4-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6a9d4-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6a9d4-142">Minimum supported client</span></span><br/> | <span data-ttu-id="6a9d4-143">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6a9d4-143">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6a9d4-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6a9d4-144">Minimum supported server</span></span><br/> | <span data-ttu-id="6a9d4-145">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6a9d4-145">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6a9d4-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6a9d4-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a9d4-147">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="6a9d4-147">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="6a9d4-148">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="6a9d4-148">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





