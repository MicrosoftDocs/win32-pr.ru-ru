---
title: Объект Тиметригжер (Windows. ApplicationModel. Background. h)
description: Объект скрипта, представляющий триггер, который запускает задачу в заданную дату и время.
ms.assetid: 3c277827-8e70-42e7-a849-773ecc997a93
keywords:
- планировщик задач триггера времени, объект
- планировщик задач объекта Тиметригжер
- Планировщик задач объекта Тиметригжер, описание
topic_type:
- apiref
api_name:
- TimeTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a8403b93e1c5292ade9f6f402b7e41994339140
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340880"
---
# <a name="timetrigger-object"></a><span data-ttu-id="d05af-106">Объект Тиметригжер</span><span class="sxs-lookup"><span data-stu-id="d05af-106">TimeTrigger object</span></span>

<span data-ttu-id="d05af-107">Объект скрипта, представляющий триггер, который запускает задачу в заданную дату и время.</span><span class="sxs-lookup"><span data-stu-id="d05af-107">Scripting object that represents a trigger that starts a task at a specific date and time.</span></span>

## <a name="members"></a><span data-ttu-id="d05af-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="d05af-108">Members</span></span>

<span data-ttu-id="d05af-109">Объект **тиметригжер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d05af-109">The **TimeTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="d05af-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="d05af-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d05af-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="d05af-111">Properties</span></span>

<span data-ttu-id="d05af-112">Объект **тиметригжер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d05af-112">The **TimeTrigger** object has these properties.</span></span>



| <span data-ttu-id="d05af-113">Свойство</span><span class="sxs-lookup"><span data-stu-id="d05af-113">Property</span></span>                                                            | <span data-ttu-id="d05af-114">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="d05af-114">Access type</span></span>           | <span data-ttu-id="d05af-115">Описание</span><span class="sxs-lookup"><span data-stu-id="d05af-115">Description</span></span>                                                                                                                                                                      |
|:--------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d05af-116">**Активировано**</span><span class="sxs-lookup"><span data-stu-id="d05af-116">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="d05af-117">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="d05af-117">Read/write</span></span><br/> | <span data-ttu-id="d05af-118">Наследуется от [**триггера**](trigger.md).</span><span class="sxs-lookup"><span data-stu-id="d05af-118">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="d05af-119">Возвращает или задает логическое значение, указывающее, включен ли триггер.</span><span class="sxs-lookup"><span data-stu-id="d05af-119">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="d05af-120">**ендбаундари**</span><span class="sxs-lookup"><span data-stu-id="d05af-120">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="d05af-121">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="d05af-121">Read/write</span></span><br/> | <span data-ttu-id="d05af-122">Наследуется от [**триггера**](trigger.md).</span><span class="sxs-lookup"><span data-stu-id="d05af-122">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="d05af-123">Возвращает или задает дату и время деактивации триггера.</span><span class="sxs-lookup"><span data-stu-id="d05af-123">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="d05af-124">Триггер не может запустить задачу после ее деактивации.</span><span class="sxs-lookup"><span data-stu-id="d05af-124">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="d05af-125">**ексекутионтимелимит**</span><span class="sxs-lookup"><span data-stu-id="d05af-125">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="d05af-126">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="d05af-126">Read/write</span></span><br/> | <span data-ttu-id="d05af-127">Наследуется от [**триггера**](trigger.md).</span><span class="sxs-lookup"><span data-stu-id="d05af-127">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="d05af-128">Возвращает или задает максимальное время, в течение которого разрешено выполнение задачи, запущенной триггером.</span><span class="sxs-lookup"><span data-stu-id="d05af-128">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                           |
| [<span data-ttu-id="d05af-129">**Удостоверения**</span><span class="sxs-lookup"><span data-stu-id="d05af-129">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="d05af-130">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="d05af-130">Read/write</span></span><br/> | <span data-ttu-id="d05af-131">Наследуется от [**триггера**](trigger.md).</span><span class="sxs-lookup"><span data-stu-id="d05af-131">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="d05af-132">Возвращает или задает идентификатор триггера.</span><span class="sxs-lookup"><span data-stu-id="d05af-132">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="d05af-133">**рандомделай**</span><span class="sxs-lookup"><span data-stu-id="d05af-133">**RandomDelay**</span></span>](dailytrigger-randomdelay.md)<br/>          | <span data-ttu-id="d05af-134">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="d05af-134">Read/write</span></span><br/> | <span data-ttu-id="d05af-135">Возвращает или задает время задержки, которое добавляется случайным образом к времени начала триггера.</span><span class="sxs-lookup"><span data-stu-id="d05af-135">Gets or sets a delay time that is randomly added to the start time of the trigger.</span></span><br/>                                                                                    |
| [<span data-ttu-id="d05af-136">**Повторение**</span><span class="sxs-lookup"><span data-stu-id="d05af-136">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="d05af-137">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="d05af-137">Read/write</span></span><br/> | <span data-ttu-id="d05af-138">Наследуется от [**триггера**](trigger.md).</span><span class="sxs-lookup"><span data-stu-id="d05af-138">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="d05af-139">Возвращает или задает частоту выполнения задачи и период повторения шаблона повторения после запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="d05af-139">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="d05af-140">**стартбаундари**</span><span class="sxs-lookup"><span data-stu-id="d05af-140">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="d05af-141">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="d05af-141">Read/write</span></span><br/> | <span data-ttu-id="d05af-142">Наследуется от [**триггера**](trigger.md).</span><span class="sxs-lookup"><span data-stu-id="d05af-142">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="d05af-143">Возвращает или задает дату и время активации триггера.</span><span class="sxs-lookup"><span data-stu-id="d05af-143">Gets or sets the date and time when the trigger is activated.</span></span> <span data-ttu-id="d05af-144">Этот элемент является обязательным.</span><span class="sxs-lookup"><span data-stu-id="d05af-144">This element is required.</span></span><br/>                                    |
| [<span data-ttu-id="d05af-145">**Тип**</span><span class="sxs-lookup"><span data-stu-id="d05af-145">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="d05af-146">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="d05af-146">Read-only</span></span><br/>  | <span data-ttu-id="d05af-147">Наследуется от [**триггера**](trigger.md).</span><span class="sxs-lookup"><span data-stu-id="d05af-147">Inherited from [**Trigger**](trigger.md).</span></span> <span data-ttu-id="d05af-148">Возвращает тип триггера.</span><span class="sxs-lookup"><span data-stu-id="d05af-148">Gets the type of the trigger.</span></span><br/>                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="d05af-149">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d05af-149">Remarks</span></span>

<span data-ttu-id="d05af-150">Элемент [**стартбаундари**](taskschedulerschema-startboundary-triggerbasetype-element.md) является обязательным элементом для триггеров времени и календаря ([**тиметригжер**](taskschedulerschema-timetrigger-triggergroup-element.md) и [**календартригжер**](taskschedulerschema-calendartrigger-triggergroup-element.md)).</span><span class="sxs-lookup"><span data-stu-id="d05af-150">The [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element is a required element for time and calendar triggers ([**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) and [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)).</span></span>

<span data-ttu-id="d05af-151">При чтении или записи XML-кода для задачи триггер простоя указывается с помощью элемента [**тиметригжер**](taskschedulerschema-timetrigger-triggergroup-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="d05af-151">When reading or writing XML for a task, an idle trigger is specified using the [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="d05af-152">Примеры</span><span class="sxs-lookup"><span data-stu-id="d05af-152">Examples</span></span>

<span data-ttu-id="d05af-153">Дополнительные сведения и примеры кода для этого объекта скрипта см. в разделе [пример триггера времени (сценарии)](time-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="d05af-153">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d05af-154">Требования</span><span class="sxs-lookup"><span data-stu-id="d05af-154">Requirements</span></span>



| <span data-ttu-id="d05af-155">Требование</span><span class="sxs-lookup"><span data-stu-id="d05af-155">Requirement</span></span> | <span data-ttu-id="d05af-156">Значение</span><span class="sxs-lookup"><span data-stu-id="d05af-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d05af-157">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d05af-157">Minimum supported client</span></span><br/> | <span data-ttu-id="d05af-158">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d05af-158">Windows Vista \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="d05af-159">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d05af-159">Minimum supported server</span></span><br/> | <span data-ttu-id="d05af-160">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d05af-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="d05af-161">Header</span><span class="sxs-lookup"><span data-stu-id="d05af-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="d05af-162"><dt>Windows. ApplicationModel. Background. h</dt></span><span class="sxs-lookup"><span data-stu-id="d05af-162"><dt>Windows.applicationmodel.background.h</dt></span></span> </dl> |
| <span data-ttu-id="d05af-163">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="d05af-163">Type library</span></span><br/>             | <dl> <span data-ttu-id="d05af-164"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d05af-164"><dt>Taskschd.tlb</dt></span></span> </dl>                          |
| <span data-ttu-id="d05af-165">DLL</span><span class="sxs-lookup"><span data-stu-id="d05af-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d05af-166"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d05af-166"><dt>Taskschd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="d05af-167">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d05af-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d05af-168">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="d05af-168">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="d05af-169">**тригжерколлектион**</span><span class="sxs-lookup"><span data-stu-id="d05af-169">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="d05af-170">**Тригжерколлектион. Create**</span><span class="sxs-lookup"><span data-stu-id="d05af-170">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





