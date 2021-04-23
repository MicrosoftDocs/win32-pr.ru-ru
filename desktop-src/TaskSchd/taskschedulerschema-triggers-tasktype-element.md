---
title: Элемент Triggers (taskType)
description: Задает триггеры, которые запускают задачу.
ms.assetid: 4bf8e85e-3742-433d-821f-736fb2ff7139
keywords:
- Элемент Triggers планировщик задач
topic_type:
- apiref
api_name:
- Triggers
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 06994c395fbfbc5b0c6244c9d17930bc4afac885
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803965"
---
# <a name="triggers-tasktype-element"></a><span data-ttu-id="740ea-104">Элемент Triggers (taskType)</span><span class="sxs-lookup"><span data-stu-id="740ea-104">Triggers (taskType) Element</span></span>

<span data-ttu-id="740ea-105">Задает триггеры, которые запускают задачу.</span><span class="sxs-lookup"><span data-stu-id="740ea-105">Specifies the triggers that start the task.</span></span>

``` syntax
<xs:element name="Triggers"
    type="triggersType"
 />
```

<span data-ttu-id="740ea-106">Элемент **Triggers** определяется сложным типом [**тригжерстипе**](taskschedulerschema-triggerstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="740ea-106">The **Triggers** element is defined by the [**triggersType**](taskschedulerschema-triggerstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="740ea-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="740ea-107">Parent element</span></span>



| <span data-ttu-id="740ea-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="740ea-108">Element</span></span>                                          | <span data-ttu-id="740ea-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="740ea-109">Derived from</span></span>                                                 | <span data-ttu-id="740ea-110">Описание</span><span class="sxs-lookup"><span data-stu-id="740ea-110">Description</span></span>                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="740ea-111">**Задача**</span><span class="sxs-lookup"><span data-stu-id="740ea-111">**Task**</span></span>](taskschedulerschema-task-element.md) | [<span data-ttu-id="740ea-112">**taskType**</span><span class="sxs-lookup"><span data-stu-id="740ea-112">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="740ea-113">Определяет задачу, выполняемую службой планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="740ea-113">Defines the task that is performed by the Task Scheduler service.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="740ea-114">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="740ea-114">Child elements</span></span>



| <span data-ttu-id="740ea-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="740ea-115">Element</span></span>                                                                                     | <span data-ttu-id="740ea-116">Тип</span><span class="sxs-lookup"><span data-stu-id="740ea-116">Type</span></span>                                                                                       | <span data-ttu-id="740ea-117">Описание</span><span class="sxs-lookup"><span data-stu-id="740ea-117">Description</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="740ea-118">**буттригжер**</span><span class="sxs-lookup"><span data-stu-id="740ea-118">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [<span data-ttu-id="740ea-119">**буттригжертипе**</span><span class="sxs-lookup"><span data-stu-id="740ea-119">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                 | <span data-ttu-id="740ea-120">Указывает триггер, который запускает задачу при загрузке системы.</span><span class="sxs-lookup"><span data-stu-id="740ea-120">Specifies a trigger that starts a task when the system is booted.</span></span><br/>                 |
| [<span data-ttu-id="740ea-121">**календартригжер**</span><span class="sxs-lookup"><span data-stu-id="740ea-121">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [<span data-ttu-id="740ea-122">**календартригжертипе**</span><span class="sxs-lookup"><span data-stu-id="740ea-122">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)         | <span data-ttu-id="740ea-123">Задает ежедневный, еженедельный, ежемесячный или ежемесячный триггер (DOW) в день недели.</span><span class="sxs-lookup"><span data-stu-id="740ea-123">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/>   |
| [<span data-ttu-id="740ea-124">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="740ea-124">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [<span data-ttu-id="740ea-125">**евенттригжертипе**</span><span class="sxs-lookup"><span data-stu-id="740ea-125">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)               | <span data-ttu-id="740ea-126">Указывает триггер, который запускает задачу при возникновении системного события.</span><span class="sxs-lookup"><span data-stu-id="740ea-126">Specifies a trigger that starts a task when a system event occurs.</span></span><br/>                |
| [<span data-ttu-id="740ea-127">**идлетригжер**</span><span class="sxs-lookup"><span data-stu-id="740ea-127">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [<span data-ttu-id="740ea-128">**идлетригжертипе**</span><span class="sxs-lookup"><span data-stu-id="740ea-128">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                 | <span data-ttu-id="740ea-129">Указывает триггер, который запускает задачу при переходе компьютера в состояние простоя.</span><span class="sxs-lookup"><span data-stu-id="740ea-129">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span><br/> |
| [<span data-ttu-id="740ea-130">**логонтригжер**</span><span class="sxs-lookup"><span data-stu-id="740ea-130">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)               | [<span data-ttu-id="740ea-131">**логонтригжертипе**</span><span class="sxs-lookup"><span data-stu-id="740ea-131">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)               | <span data-ttu-id="740ea-132">Указывает триггер, который запускает задачу при входе пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="740ea-132">Specifies a trigger that starts a task when a user logs on.</span></span><br/>                       |
| [<span data-ttu-id="740ea-133">**регистратионтригжер**</span><span class="sxs-lookup"><span data-stu-id="740ea-133">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="740ea-134">**регистратионтригжертипе**</span><span class="sxs-lookup"><span data-stu-id="740ea-134">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="740ea-135">Указывает триггер, который запускает задачу при регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="740ea-135">Specifies a trigger that starts a task when the task is registered.</span></span><br/>               |
| [<span data-ttu-id="740ea-136">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="740ea-136">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [<span data-ttu-id="740ea-137">**тиметригжертипе**</span><span class="sxs-lookup"><span data-stu-id="740ea-137">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                 | <span data-ttu-id="740ea-138">Указывает триггер, который запускает задачу при активации триггера.</span><span class="sxs-lookup"><span data-stu-id="740ea-138">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/>             |



## <a name="remarks"></a><span data-ttu-id="740ea-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="740ea-139">Remarks</span></span>

<span data-ttu-id="740ea-140">Перечисленные выше дочерние элементы можно добавлять в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="740ea-140">The child elements listed above can be added in any order.</span></span>

<span data-ttu-id="740ea-141">Для разработки на C++ триггеры задачи указываются с помощью [**свойства Triggers объекта итаскдефинитион**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers).</span><span class="sxs-lookup"><span data-stu-id="740ea-141">For C++ development, the triggers of a task are specified using the [**Triggers property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers).</span></span>

<span data-ttu-id="740ea-142">Для разработки сценариев триггеры задачи указываются с помощью свойства [**таскдефинитион. triggers**](taskdefinition-triggers.md) .</span><span class="sxs-lookup"><span data-stu-id="740ea-142">For scripting development, the triggers of a task are specified using the [**TaskDefinition.Triggers**](taskdefinition-triggers.md) property.</span></span>

## <a name="examples"></a><span data-ttu-id="740ea-143">Примеры</span><span class="sxs-lookup"><span data-stu-id="740ea-143">Examples</span></span>

<span data-ttu-id="740ea-144">Полный пример XML-кода для задачи, указывающей триггер, см. в разделе [пример триггера времени (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="740ea-144">For a complete example of the XML for a task that specifies a trigger, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="740ea-145">Требования</span><span class="sxs-lookup"><span data-stu-id="740ea-145">Requirements</span></span>



| <span data-ttu-id="740ea-146">Требование</span><span class="sxs-lookup"><span data-stu-id="740ea-146">Requirement</span></span> | <span data-ttu-id="740ea-147">Значение</span><span class="sxs-lookup"><span data-stu-id="740ea-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="740ea-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="740ea-148">Minimum supported client</span></span><br/> | <span data-ttu-id="740ea-149">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="740ea-149">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="740ea-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="740ea-150">Minimum supported server</span></span><br/> | <span data-ttu-id="740ea-151">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="740ea-151">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="740ea-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="740ea-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="740ea-153">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="740ea-153">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="740ea-154">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="740ea-154">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





