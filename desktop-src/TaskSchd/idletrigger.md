---
title: Объект Идлетригжер
description: Объект скрипта, представляющий триггер, который запускает задачу при возникновении условия простоя.
ms.assetid: 627d83cf-27bd-47ce-a647-fa1e9af5263e
keywords:
- планировщик задач триггера бездействия, объект
- планировщик задач объекта Идлетригжер
- Планировщик задач объекта Идлетригжер, описание
topic_type:
- apiref
api_name:
- IdleTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e72288827fec34257bf4f54a152031ef37068790
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682098"
---
# <a name="idletrigger-object"></a><span data-ttu-id="79da1-106">Объект Идлетригжер</span><span class="sxs-lookup"><span data-stu-id="79da1-106">IdleTrigger object</span></span>

<span data-ttu-id="79da1-107">Объект скрипта, представляющий триггер, который запускает задачу при возникновении условия простоя.</span><span class="sxs-lookup"><span data-stu-id="79da1-107">Scripting object that represents a trigger that starts a task when an idle condition occurs.</span></span> <span data-ttu-id="79da1-108">Сведения об условиях простоя см. в разделе [условия простоя задачи](task-idle-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="79da1-108">For information about idle conditions, see [Task Idle Conditions](task-idle-conditions.md).</span></span>

## <a name="members"></a><span data-ttu-id="79da1-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="79da1-109">Members</span></span>

<span data-ttu-id="79da1-110">Объект **идлетригжер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="79da1-110">The **IdleTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="79da1-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="79da1-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="79da1-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="79da1-112">Properties</span></span>

<span data-ttu-id="79da1-113">Объект **идлетригжер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="79da1-113">The **IdleTrigger** object has these properties.</span></span>



| <span data-ttu-id="79da1-114">Свойство</span><span class="sxs-lookup"><span data-stu-id="79da1-114">Property</span></span>                                                            | <span data-ttu-id="79da1-115">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="79da1-115">Access type</span></span>           | <span data-ttu-id="79da1-116">Описание</span><span class="sxs-lookup"><span data-stu-id="79da1-116">Description</span></span>                                                                                                                                                                                               |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="79da1-117">**Активировано**</span><span class="sxs-lookup"><span data-stu-id="79da1-117">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="79da1-118">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="79da1-118">Read/write</span></span><br/> | <span data-ttu-id="79da1-119">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="79da1-119">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="79da1-120">Возвращает или задает логическое значение, указывающее, включен ли триггер.</span><span class="sxs-lookup"><span data-stu-id="79da1-120">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                              |
| [<span data-ttu-id="79da1-121">ендбаундари</span><span class="sxs-lookup"><span data-stu-id="79da1-121">EndBoundary</span></span>](trigger-endboundary.md)<br/>                   | <span data-ttu-id="79da1-122">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="79da1-122">Read/write</span></span><br/> | <span data-ttu-id="79da1-123">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="79da1-123">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="79da1-124">Возвращает или задает дату и время деактивации триггера.</span><span class="sxs-lookup"><span data-stu-id="79da1-124">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="79da1-125">Триггер не может запустить задачу после ее деактивации.</span><span class="sxs-lookup"><span data-stu-id="79da1-125">The trigger cannot start the task after it is deactivated.</span></span><br/>               |
| [<span data-ttu-id="79da1-126">**ексекутионтимелимит**</span><span class="sxs-lookup"><span data-stu-id="79da1-126">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="79da1-127">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="79da1-127">Read/write</span></span><br/> | <span data-ttu-id="79da1-128">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="79da1-128">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="79da1-129">Возвращает или задает максимальное время, в течение которого задача может запускаться триггером.</span><span class="sxs-lookup"><span data-stu-id="79da1-129">Gets or sets the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                                 |
| [<span data-ttu-id="79da1-130">**Удостоверения**</span><span class="sxs-lookup"><span data-stu-id="79da1-130">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="79da1-131">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="79da1-131">Read/write</span></span><br/> | <span data-ttu-id="79da1-132">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="79da1-132">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="79da1-133">Возвращает или задает идентификатор триггера.</span><span class="sxs-lookup"><span data-stu-id="79da1-133">Gets or sets the identifier for the trigger.</span></span><br/>                                                                                             |
| [<span data-ttu-id="79da1-134">**Повторение**</span><span class="sxs-lookup"><span data-stu-id="79da1-134">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="79da1-135">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="79da1-135">Read/write</span></span><br/> | <span data-ttu-id="79da1-136">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="79da1-136">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="79da1-137">Возвращает или задает значение, указывающее, как часто выполняется задача и как долго шаблон повторения повторяется после запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="79da1-137">Gets or sets a value that indicates how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |
| [<span data-ttu-id="79da1-138">**стартбаундари**</span><span class="sxs-lookup"><span data-stu-id="79da1-138">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="79da1-139">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="79da1-139">Read/write</span></span><br/> | <span data-ttu-id="79da1-140">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="79da1-140">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="79da1-141">Возвращает или задает дату и время активации триггера.</span><span class="sxs-lookup"><span data-stu-id="79da1-141">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                                            |
| [<span data-ttu-id="79da1-142">**Тип**</span><span class="sxs-lookup"><span data-stu-id="79da1-142">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="79da1-143">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="79da1-143">Read-only</span></span><br/>  | <span data-ttu-id="79da1-144">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="79da1-144">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="79da1-145">Возвращает тип триггера.</span><span class="sxs-lookup"><span data-stu-id="79da1-145">Gets the type of the trigger.</span></span><br/>                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="79da1-146">Комментарии</span><span class="sxs-lookup"><span data-stu-id="79da1-146">Remarks</span></span>

<span data-ttu-id="79da1-147">Триггер простоя активирует действие задачи, только если компьютер переходит в состояние простоя после начальной границы триггера.</span><span class="sxs-lookup"><span data-stu-id="79da1-147">An idle trigger will only trigger a task action if the computer goes into an idle state after the start boundary of the trigger.</span></span>

<span data-ttu-id="79da1-148">При чтении или записи XML-кода для задачи триггер простоя указывается с помощью элемента [**идлетригжер**](taskschedulerschema-idletrigger-triggergroup-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="79da1-148">When reading or writing XML for a task, an idle trigger is specified using the [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="79da1-149">Если задача запускается триггером Idle, свойство [**идлесеттингс. ваиттимеаут**](idlesettings-waittimeout.md) игнорируется.</span><span class="sxs-lookup"><span data-stu-id="79da1-149">If a task is triggered by an idle trigger, then the [**IdleSettings.WaitTimeout**](idlesettings-waittimeout.md) property is ignored.</span></span>

<span data-ttu-id="79da1-150">Если исходный экземпляр задачи с триггером Idle все еще выполняется, задача запускается только один раз без повторений, даже если в свойстве [**повторения**](trigger-repetition.md) определено несколько повторений.</span><span class="sxs-lookup"><span data-stu-id="79da1-150">If the initial instance of a task with an idle trigger is still running, then the task is only launched once with no repetitions, even if multiple repetition is defined in the [**Repetition**](trigger-repetition.md) property.</span></span> <span data-ttu-id="79da1-151">Такое поведение не происходит, если задача останавливается сама по себе.</span><span class="sxs-lookup"><span data-stu-id="79da1-151">This behavior does not occur if the task stops by itself.</span></span>

## <a name="requirements"></a><span data-ttu-id="79da1-152">Требования</span><span class="sxs-lookup"><span data-stu-id="79da1-152">Requirements</span></span>



| <span data-ttu-id="79da1-153">Требование</span><span class="sxs-lookup"><span data-stu-id="79da1-153">Requirement</span></span> | <span data-ttu-id="79da1-154">Значение</span><span class="sxs-lookup"><span data-stu-id="79da1-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="79da1-155">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="79da1-155">Minimum supported client</span></span><br/> | <span data-ttu-id="79da1-156">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="79da1-156">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="79da1-157">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="79da1-157">Minimum supported server</span></span><br/> | <span data-ttu-id="79da1-158">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="79da1-158">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="79da1-159">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="79da1-159">Type library</span></span><br/>             | <dl> <span data-ttu-id="79da1-160"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="79da1-160"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="79da1-161">DLL</span><span class="sxs-lookup"><span data-stu-id="79da1-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79da1-162"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79da1-162"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79da1-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="79da1-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79da1-164">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="79da1-164">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="79da1-165">планировщик задач объекты</span><span class="sxs-lookup"><span data-stu-id="79da1-165">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="79da1-166">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="79da1-166">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





