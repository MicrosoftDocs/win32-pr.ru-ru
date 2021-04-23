---
title: Элемент EventTrigger (Тригжерграуп)
description: Указывает триггер, который запускает задачу при возникновении системного события.
ms.assetid: 8faffc04-1ad2-499d-bcdf-bc28f64b8aa8
keywords:
- планировщик задач триггера события, элемент
- Элемент EventTrigger планировщик задач
topic_type:
- apiref
api_name:
- EventTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3cecf46250fface0f716adbf287cda3269b86f04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492072"
---
# <a name="eventtrigger-triggergroup-element"></a><span data-ttu-id="c8f70-105">Элемент EventTrigger (Тригжерграуп)</span><span class="sxs-lookup"><span data-stu-id="c8f70-105">EventTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="c8f70-106">Указывает триггер, который запускает задачу при возникновении системного события.</span><span class="sxs-lookup"><span data-stu-id="c8f70-106">Specifies a trigger that starts a task when a system event occurs.</span></span>

``` syntax
<xs:element name="EventTrigger"
    type="eventTriggerType"
 />
```

<span data-ttu-id="c8f70-107">Элемент **EventTrigger** определяется [**тригжерграуп**](taskschedulerschema-triggergroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="c8f70-107">The **EventTrigger** element is defined by the [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="c8f70-108">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="c8f70-108">Parent element</span></span>



| <span data-ttu-id="c8f70-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="c8f70-109">Element</span></span>                                                           | <span data-ttu-id="c8f70-110">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="c8f70-110">Derived from</span></span>                                                         | <span data-ttu-id="c8f70-111">Описание</span><span class="sxs-lookup"><span data-stu-id="c8f70-111">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="c8f70-112">**Триггеры**</span><span class="sxs-lookup"><span data-stu-id="c8f70-112">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="c8f70-113">**тригжерстипе**</span><span class="sxs-lookup"><span data-stu-id="c8f70-113">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="c8f70-114">Задает триггеры, которые запускают задачу.</span><span class="sxs-lookup"><span data-stu-id="c8f70-114">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="c8f70-115">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="c8f70-115">Child elements</span></span>



| <span data-ttu-id="c8f70-116">Элемент</span><span class="sxs-lookup"><span data-stu-id="c8f70-116">Element</span></span>                                                                                              | <span data-ttu-id="c8f70-117">Тип</span><span class="sxs-lookup"><span data-stu-id="c8f70-117">Type</span></span>                                                                     | <span data-ttu-id="c8f70-118">Описание</span><span class="sxs-lookup"><span data-stu-id="c8f70-118">Description</span></span>                                                                                                                        |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c8f70-119">**Задержка (Евенттригжертипе)**</span><span class="sxs-lookup"><span data-stu-id="c8f70-119">**Delay (eventTriggerType)**</span></span>](taskschedulerschema-delay-eventtriggertype-element.md)               | <span data-ttu-id="c8f70-120">длительность</span><span class="sxs-lookup"><span data-stu-id="c8f70-120">duration</span></span>                                                                 | <span data-ttu-id="c8f70-121">Указывает промежуток времени между моментом возникновения события и моментом запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="c8f70-121">Specifies the amount of time between when the event occurs and when the task is started.</span></span><br/>                                |
| [<span data-ttu-id="c8f70-122">**Включено (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="c8f70-122">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)             | <span data-ttu-id="c8f70-123">Логическое</span><span class="sxs-lookup"><span data-stu-id="c8f70-123">boolean</span></span>                                                                  | <span data-ttu-id="c8f70-124">Указывает, что триггер включен.</span><span class="sxs-lookup"><span data-stu-id="c8f70-124">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="c8f70-125">**Ендбаундари (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="c8f70-125">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)     | <span data-ttu-id="c8f70-126">dateTime</span><span class="sxs-lookup"><span data-stu-id="c8f70-126">dateTime</span></span>                                                                 | <span data-ttu-id="c8f70-127">Указывает дату и время деактивации триггера.</span><span class="sxs-lookup"><span data-stu-id="c8f70-127">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="c8f70-128">Триггер не может запустить задачу после ее деактивации.</span><span class="sxs-lookup"><span data-stu-id="c8f70-128">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="c8f70-129">**Повторение (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="c8f70-129">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)       | [<span data-ttu-id="c8f70-130">**репетитионтипе**</span><span class="sxs-lookup"><span data-stu-id="c8f70-130">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="c8f70-131">Указывает, как часто выполняется задача и как долго шаблон повторения повторяется после запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="c8f70-131">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="c8f70-132">**Стартбаундари (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="c8f70-132">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md) | <span data-ttu-id="c8f70-133">dateTime</span><span class="sxs-lookup"><span data-stu-id="c8f70-133">dateTime</span></span>                                                                 | <span data-ttu-id="c8f70-134">Указывает дату и время активации триггера.</span><span class="sxs-lookup"><span data-stu-id="c8f70-134">Specifies the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="c8f70-135">**Подписка (Евенттригжертипе)**</span><span class="sxs-lookup"><span data-stu-id="c8f70-135">**Subscription (eventTriggerType)**</span></span>](taskschedulerschema-subscription-eventtriggertype-element.md) | <span data-ttu-id="c8f70-136">строка</span><span class="sxs-lookup"><span data-stu-id="c8f70-136">string</span></span>                                                                   | <span data-ttu-id="c8f70-137">Указывает запрос XPath, определяющий событие, вызвавшее срабатывание триггера.</span><span class="sxs-lookup"><span data-stu-id="c8f70-137">Specifies the XPath query that identifies the event that fires the trigger.</span></span><br/>                                             |



## <a name="attributes"></a><span data-ttu-id="c8f70-138">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="c8f70-138">Attributes</span></span>



| <span data-ttu-id="c8f70-139">Имя</span><span class="sxs-lookup"><span data-stu-id="c8f70-139">Name</span></span> | <span data-ttu-id="c8f70-140">Тип</span><span class="sxs-lookup"><span data-stu-id="c8f70-140">Type</span></span> | <span data-ttu-id="c8f70-141">Описание</span><span class="sxs-lookup"><span data-stu-id="c8f70-141">Description</span></span>                           |
|------|------|---------------------------------------|
| <span data-ttu-id="c8f70-142">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="c8f70-142">Id</span></span>   | <span data-ttu-id="c8f70-143">ID</span><span class="sxs-lookup"><span data-stu-id="c8f70-143">ID</span></span>   | <span data-ttu-id="c8f70-144">Идентификатор триггера.</span><span class="sxs-lookup"><span data-stu-id="c8f70-144">Identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c8f70-145">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c8f70-145">Remarks</span></span>

<span data-ttu-id="c8f70-146">Можно создать не более 500 задач с подписками на события.</span><span class="sxs-lookup"><span data-stu-id="c8f70-146">A maximum of 500 tasks with event subscriptions can be created.</span></span> <span data-ttu-id="c8f70-147">Подписка на событие, которая запрашивает различные события, может использоваться для запуска задачи, которая использует то же действие в ответ на регистрируемые события.</span><span class="sxs-lookup"><span data-stu-id="c8f70-147">An event subscription that queries for a variety of events can be used to trigger a task that uses the same action in response to the events being logged.</span></span>

<span data-ttu-id="c8f70-148">Для разработки скриптов триггер события определяется объектом [**EventTrigger**](eventtrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="c8f70-148">For script development, an event trigger is defined by the [**EventTrigger**](eventtrigger.md) object.</span></span>

<span data-ttu-id="c8f70-149">Для разработки на C++ триггер события определяется интерфейсом [**иевенттригжер**](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger) .</span><span class="sxs-lookup"><span data-stu-id="c8f70-149">For C++ development, an event trigger is defined by the [**IEventTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="c8f70-150">Примеры</span><span class="sxs-lookup"><span data-stu-id="c8f70-150">Examples</span></span>

<span data-ttu-id="c8f70-151">Полный пример XML-кода для задачи, использующей триггер события, см. в разделе [пример триггера события (XML)](/previous-versions//aa446889(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c8f70-151">For a complete example of the XML for a task that uses an event trigger, see [Event Trigger Example (XML)](/previous-versions//aa446889(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="c8f70-152">Требования</span><span class="sxs-lookup"><span data-stu-id="c8f70-152">Requirements</span></span>



| <span data-ttu-id="c8f70-153">Требование</span><span class="sxs-lookup"><span data-stu-id="c8f70-153">Requirement</span></span> | <span data-ttu-id="c8f70-154">Значение</span><span class="sxs-lookup"><span data-stu-id="c8f70-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c8f70-155">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c8f70-155">Minimum supported client</span></span><br/> | <span data-ttu-id="c8f70-156">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c8f70-156">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c8f70-157">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c8f70-157">Minimum supported server</span></span><br/> | <span data-ttu-id="c8f70-158">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c8f70-158">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c8f70-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c8f70-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8f70-160">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="c8f70-160">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

