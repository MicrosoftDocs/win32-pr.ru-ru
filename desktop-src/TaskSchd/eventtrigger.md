---
title: Объект EventTrigger (Windows. UI. XAML. h)
description: Объект скрипта, представляющий триггер, который запускает задачу при возникновении системного события.
ms.assetid: 79cb6591-0919-441f-ad7f-4eb7cf0f9591
keywords:
- планировщик задач триггеров событий, объект
- Объект EventTrigger планировщик задач
- Объект EventTrigger планировщик задач, описание
topic_type:
- apiref
api_name:
- EventTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77b80bc8336c4756dfedc041aea40f79fd5f868e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534991"
---
# <a name="eventtrigger-object"></a><span data-ttu-id="9ab5d-106">Объект EventTrigger</span><span class="sxs-lookup"><span data-stu-id="9ab5d-106">EventTrigger object</span></span>

<span data-ttu-id="9ab5d-107">Объект скрипта, представляющий триггер, который запускает задачу при возникновении системного события.</span><span class="sxs-lookup"><span data-stu-id="9ab5d-107">Scripting object that represents a trigger that starts a task when a system event occurs.</span></span>

## <a name="members"></a><span data-ttu-id="9ab5d-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="9ab5d-108">Members</span></span>

<span data-ttu-id="9ab5d-109">Объект **EventTrigger** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9ab5d-109">The **EventTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="9ab5d-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="9ab5d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9ab5d-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="9ab5d-111">Properties</span></span>

<span data-ttu-id="9ab5d-112">Объект **EventTrigger** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="9ab5d-112">The **EventTrigger** object has these properties.</span></span>



| <span data-ttu-id="9ab5d-113">Свойство</span><span class="sxs-lookup"><span data-stu-id="9ab5d-113">Property</span></span>                                                            | <span data-ttu-id="9ab5d-114">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="9ab5d-114">Access type</span></span>           | <span data-ttu-id="9ab5d-115">Описание</span><span class="sxs-lookup"><span data-stu-id="9ab5d-115">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                              |
|:--------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9ab5d-116">**Задержка**</span><span class="sxs-lookup"><span data-stu-id="9ab5d-116">**Delay**</span></span>](eventtrigger-delay.md)<br/>                      | <span data-ttu-id="9ab5d-117">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="9ab5d-117">Read/write</span></span><br/> | <span data-ttu-id="9ab5d-118">Возвращает или задает значение, указывающее промежуток времени между возникновением события и моментом запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="9ab5d-118">Gets or sets a value that indicates the amount of time between when the event occurs and when the task is started.</span></span><br/>                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="9ab5d-119">**Активировано**</span><span class="sxs-lookup"><span data-stu-id="9ab5d-119">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="9ab5d-120">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="9ab5d-120">Read/write</span></span><br/> | <span data-ttu-id="9ab5d-121">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="9ab5d-121">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="9ab5d-122">Возвращает или задает логическое значение, указывающее, включен ли триггер.</span><span class="sxs-lookup"><span data-stu-id="9ab5d-122">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                                                                                                                                                                                                             |
| [<span data-ttu-id="9ab5d-123">**ендбаундари**</span><span class="sxs-lookup"><span data-stu-id="9ab5d-123">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="9ab5d-124">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="9ab5d-124">Read/write</span></span><br/> | <span data-ttu-id="9ab5d-125">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="9ab5d-125">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="9ab5d-126">Возвращает или задает дату и время деактивации триггера.</span><span class="sxs-lookup"><span data-stu-id="9ab5d-126">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="9ab5d-127">Триггер не может запустить задачу после ее деактивации.</span><span class="sxs-lookup"><span data-stu-id="9ab5d-127">The trigger cannot start the task after it is deactivated.</span></span><br/>                                                                                                                                                                                              |
| [<span data-ttu-id="9ab5d-128">**ексекутионтимелимит**</span><span class="sxs-lookup"><span data-stu-id="9ab5d-128">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="9ab5d-129">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="9ab5d-129">Read/write</span></span><br/> | <span data-ttu-id="9ab5d-130">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="9ab5d-130">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="9ab5d-131">Возвращает или задает максимальное время, в течение которого разрешено выполнение задачи, запущенной этим триггером.</span><span class="sxs-lookup"><span data-stu-id="9ab5d-131">Gets or sets the maximum amount of time that the task launched by this trigger is allowed to run.</span></span><br/>                                                                                                                                                                                                                       |
| [<span data-ttu-id="9ab5d-132">**Удостоверения**</span><span class="sxs-lookup"><span data-stu-id="9ab5d-132">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="9ab5d-133">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="9ab5d-133">Read/write</span></span><br/> | <span data-ttu-id="9ab5d-134">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="9ab5d-134">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="9ab5d-135">Возвращает или задает идентификатор триггера.</span><span class="sxs-lookup"><span data-stu-id="9ab5d-135">Gets or sets the identifier for the trigger.</span></span><br/>                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="9ab5d-136">**Повторение**</span><span class="sxs-lookup"><span data-stu-id="9ab5d-136">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="9ab5d-137">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="9ab5d-137">Read/write</span></span><br/> | <span data-ttu-id="9ab5d-138">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="9ab5d-138">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="9ab5d-139">Возвращает или задает частоту выполнения задачи и период повторения шаблона повторения после запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="9ab5d-139">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>                                                                                                                                                                                                       |
| [<span data-ttu-id="9ab5d-140">**стартбаундари**</span><span class="sxs-lookup"><span data-stu-id="9ab5d-140">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="9ab5d-141">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="9ab5d-141">Read/write</span></span><br/> | <span data-ttu-id="9ab5d-142">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="9ab5d-142">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="9ab5d-143">Возвращает или задает дату и время активации триггера.</span><span class="sxs-lookup"><span data-stu-id="9ab5d-143">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="9ab5d-144">**Подписка**</span><span class="sxs-lookup"><span data-stu-id="9ab5d-144">**Subscription**</span></span>](eventtrigger-subscription.md)<br/>        | <span data-ttu-id="9ab5d-145">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="9ab5d-145">Read/write</span></span><br/> | <span data-ttu-id="9ab5d-146">Возвращает или задает строку запроса XPath, определяющую событие, которое вызывает срабатывание триггера.</span><span class="sxs-lookup"><span data-stu-id="9ab5d-146">Gets or sets the XPath query string that identifies the event that fires the trigger.</span></span><br/>                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="9ab5d-147">**Тип**</span><span class="sxs-lookup"><span data-stu-id="9ab5d-147">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="9ab5d-148">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ab5d-148">Read-only</span></span><br/>  | <span data-ttu-id="9ab5d-149">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="9ab5d-149">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="9ab5d-150">Возвращает тип триггера.</span><span class="sxs-lookup"><span data-stu-id="9ab5d-150">Gets the type of the trigger.</span></span><br/>                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="9ab5d-151">**валуекуериес**</span><span class="sxs-lookup"><span data-stu-id="9ab5d-151">**ValueQueries**</span></span>](eventtrigger-valuequeries.md)<br/>        | <span data-ttu-id="9ab5d-152">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="9ab5d-152">Read/write</span></span><br/> | <span data-ttu-id="9ab5d-153">Возвращает или задает коллекцию именованных запросов XPath.</span><span class="sxs-lookup"><span data-stu-id="9ab5d-153">Gets or sets a collection of named XPath queries.</span></span> <span data-ttu-id="9ab5d-154">Каждый запрос в коллекции применяется к последнему соответствующему XML-событию, возвращенному из запроса подписки, указанного в свойстве [**Subscription**](eventtrigger-subscription.md) .</span><span class="sxs-lookup"><span data-stu-id="9ab5d-154">Each query in the collection is applied to the last matching event XML that is returned from the subscription query specified in the [**Subscription**](eventtrigger-subscription.md) property.</span></span> <span data-ttu-id="9ab5d-155">Имя запроса можно использовать в качестве переменной в сообщении для действия [**шовмессажеактион**](showmessageaction.md) .</span><span class="sxs-lookup"><span data-stu-id="9ab5d-155">The name of the query can be used as a variable in the message of a [**ShowMessageAction**](showmessageaction.md) action.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9ab5d-156">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9ab5d-156">Remarks</span></span>

<span data-ttu-id="9ab5d-157">Можно создать не более 500 задач с подписками на события.</span><span class="sxs-lookup"><span data-stu-id="9ab5d-157">A maximum of 500 tasks with event subscriptions can be created.</span></span> <span data-ttu-id="9ab5d-158">Подписка на событие, которая запрашивает различные события, может использоваться для запуска задачи, которая использует то же действие в ответ на регистрируемые события.</span><span class="sxs-lookup"><span data-stu-id="9ab5d-158">An event subscription that queries for a variety of events can be used to trigger a task that uses the same action in response to the events being logged.</span></span>

<span data-ttu-id="9ab5d-159">При чтении или записи собственного XML-кода для задачи триггер события задается с помощью элемента [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="9ab5d-159">When reading or writing your own XML for a task, an event trigger is specified using the [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="9ab5d-160">Примеры</span><span class="sxs-lookup"><span data-stu-id="9ab5d-160">Examples</span></span>

<span data-ttu-id="9ab5d-161">Дополнительные сведения и пример кода для этого объекта скрипта см. в разделе [пример триггера события (создание сценариев)](/previous-versions//aa446887(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9ab5d-161">For more information and a code example for this scripting object, see [Event Trigger Example (Scripting)](/previous-versions//aa446887(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="9ab5d-162">Требования</span><span class="sxs-lookup"><span data-stu-id="9ab5d-162">Requirements</span></span>



| <span data-ttu-id="9ab5d-163">Требование</span><span class="sxs-lookup"><span data-stu-id="9ab5d-163">Requirement</span></span> | <span data-ttu-id="9ab5d-164">Значение</span><span class="sxs-lookup"><span data-stu-id="9ab5d-164">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ab5d-165">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9ab5d-165">Minimum supported client</span></span><br/> | <span data-ttu-id="9ab5d-166">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9ab5d-166">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9ab5d-167">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9ab5d-167">Minimum supported server</span></span><br/> | <span data-ttu-id="9ab5d-168">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9ab5d-168">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9ab5d-169">Header</span><span class="sxs-lookup"><span data-stu-id="9ab5d-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ab5d-170"><dt>Windows. UI. XAML. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ab5d-170"><dt>Windows.ui.xaml.h</dt></span></span> </dl> |
| <span data-ttu-id="9ab5d-171">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="9ab5d-171">Type library</span></span><br/>             | <dl> <span data-ttu-id="9ab5d-172"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9ab5d-172"><dt>Taskschd.tlb</dt></span></span> </dl>      |
| <span data-ttu-id="9ab5d-173">DLL</span><span class="sxs-lookup"><span data-stu-id="9ab5d-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ab5d-174"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ab5d-174"><dt>Taskschd.dll</dt></span></span> </dl>      |



## <a name="see-also"></a><span data-ttu-id="9ab5d-175">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9ab5d-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ab5d-176">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="9ab5d-176">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="9ab5d-177">**тригжерколлектион**</span><span class="sxs-lookup"><span data-stu-id="9ab5d-177">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="9ab5d-178">**Тригжерколлектион. Create**</span><span class="sxs-lookup"><span data-stu-id="9ab5d-178">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

