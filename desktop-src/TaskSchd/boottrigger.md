---
title: Объект Буттригжер
description: Объект скрипта, представляющий триггер, который запускает задачу при загрузке системы.
ms.assetid: 9d5a7cf6-2e1d-44ae-bb45-66424770d61b
keywords:
- планировщик задач триггера загрузки, объект
- планировщик задач объекта Буттригжер
- Планировщик задач объекта Буттригжер, описание
topic_type:
- apiref
api_name:
- BootTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 346a4bc7b20606f59c26b131590b92593d40d07e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493134"
---
# <a name="boottrigger-object"></a><span data-ttu-id="0a13e-106">Объект Буттригжер</span><span class="sxs-lookup"><span data-stu-id="0a13e-106">BootTrigger object</span></span>

<span data-ttu-id="0a13e-107">Объект скрипта, представляющий триггер, который запускает задачу при загрузке системы.</span><span class="sxs-lookup"><span data-stu-id="0a13e-107">Scripting object that represents a trigger that starts a task when the system is booted.</span></span>

## <a name="members"></a><span data-ttu-id="0a13e-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="0a13e-108">Members</span></span>

<span data-ttu-id="0a13e-109">Объект **буттригжер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0a13e-109">The **BootTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="0a13e-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="0a13e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0a13e-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="0a13e-111">Properties</span></span>

<span data-ttu-id="0a13e-112">Объект **буттригжер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0a13e-112">The **BootTrigger** object has these properties.</span></span>



| <span data-ttu-id="0a13e-113">Свойство</span><span class="sxs-lookup"><span data-stu-id="0a13e-113">Property</span></span>                                                            | <span data-ttu-id="0a13e-114">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="0a13e-114">Access type</span></span>           | <span data-ttu-id="0a13e-115">Описание</span><span class="sxs-lookup"><span data-stu-id="0a13e-115">Description</span></span>                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0a13e-116">**Задержка**</span><span class="sxs-lookup"><span data-stu-id="0a13e-116">**Delay**</span></span>](boottrigger-delay.md)<br/>                       |                       | <span data-ttu-id="0a13e-117">Возвращает или задает значение, указывающее промежуток времени между загрузкой системы и началом задачи.</span><span class="sxs-lookup"><span data-stu-id="0a13e-117">Gets or sets a value that indicates the amount of time between when the system is booted and when the task is started.</span></span><br/>                                                           |
| [<span data-ttu-id="0a13e-118">**Активировано**</span><span class="sxs-lookup"><span data-stu-id="0a13e-118">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="0a13e-119">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="0a13e-119">Read/write</span></span><br/> | <span data-ttu-id="0a13e-120">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="0a13e-120">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="0a13e-121">Возвращает или задает логическое значение, указывающее, включен ли триггер.</span><span class="sxs-lookup"><span data-stu-id="0a13e-121">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="0a13e-122">**ендбаундари**</span><span class="sxs-lookup"><span data-stu-id="0a13e-122">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="0a13e-123">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="0a13e-123">Read/write</span></span><br/> | <span data-ttu-id="0a13e-124">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="0a13e-124">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="0a13e-125">Возвращает или задает дату и время деактивации триггера.</span><span class="sxs-lookup"><span data-stu-id="0a13e-125">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="0a13e-126">Триггер не может запустить задачу после ее деактивации.</span><span class="sxs-lookup"><span data-stu-id="0a13e-126">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="0a13e-127">**ексекутионтимелимит**</span><span class="sxs-lookup"><span data-stu-id="0a13e-127">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="0a13e-128">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="0a13e-128">Read/write</span></span><br/> | <span data-ttu-id="0a13e-129">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="0a13e-129">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="0a13e-130">Возвращает или задает максимальное время, в течение которого разрешено выполнение задачи, запущенной триггером.</span><span class="sxs-lookup"><span data-stu-id="0a13e-130">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                           |
| [<span data-ttu-id="0a13e-131">**Удостоверения**</span><span class="sxs-lookup"><span data-stu-id="0a13e-131">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="0a13e-132">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="0a13e-132">Read/write</span></span><br/> | <span data-ttu-id="0a13e-133">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="0a13e-133">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="0a13e-134">Возвращает или задает идентификатор триггера.</span><span class="sxs-lookup"><span data-stu-id="0a13e-134">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="0a13e-135">**Повторение**</span><span class="sxs-lookup"><span data-stu-id="0a13e-135">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="0a13e-136">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="0a13e-136">Read/write</span></span><br/> | <span data-ttu-id="0a13e-137">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="0a13e-137">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="0a13e-138">Возвращает или задает частоту выполнения задачи и период повторения шаблона повторения после запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="0a13e-138">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="0a13e-139">**стартбаундари**</span><span class="sxs-lookup"><span data-stu-id="0a13e-139">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="0a13e-140">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="0a13e-140">Read/write</span></span><br/> | <span data-ttu-id="0a13e-141">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="0a13e-141">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="0a13e-142">Возвращает или задает дату и время активации триггера.</span><span class="sxs-lookup"><span data-stu-id="0a13e-142">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="0a13e-143">**Тип**</span><span class="sxs-lookup"><span data-stu-id="0a13e-143">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="0a13e-144">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="0a13e-144">Read-only</span></span><br/>  | <span data-ttu-id="0a13e-145">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="0a13e-145">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="0a13e-146">Возвращает тип триггера.</span><span class="sxs-lookup"><span data-stu-id="0a13e-146">Gets the type of the trigger.</span></span><br/>                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="0a13e-147">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0a13e-147">Remarks</span></span>

<span data-ttu-id="0a13e-148">Служба планировщик задач запускается при загрузке операционной системы, а задачи триггера загрузки настроены на запуск при запуске службы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="0a13e-148">The Task Scheduler service is started when the operating system is booted, and boot trigger tasks are set to start when the Task Scheduler service starts.</span></span>

<span data-ttu-id="0a13e-149">Только член группы "Администраторы" может создать задачу с триггером загрузки.</span><span class="sxs-lookup"><span data-stu-id="0a13e-149">Only a member of the Administrators group can create a task with a boot trigger.</span></span>

<span data-ttu-id="0a13e-150">При создании собственного XML-кода для задачи триггер загрузки указывается с помощью элемента [**буттригжер**](taskschedulerschema-boottrigger-triggergroup-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="0a13e-150">When creating your own XML for a task, a boot trigger is specified using the [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="0a13e-151">Примеры</span><span class="sxs-lookup"><span data-stu-id="0a13e-151">Examples</span></span>

<span data-ttu-id="0a13e-152">Дополнительные сведения и примеры кода для этого объекта скрипта см. в разделе [Пример загрузочного триггера (сценарии)](boot-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="0a13e-152">For more information and example code for this scripting object, see [Boot Trigger Example (Scripting)](boot-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0a13e-153">Требования</span><span class="sxs-lookup"><span data-stu-id="0a13e-153">Requirements</span></span>



| <span data-ttu-id="0a13e-154">Требование</span><span class="sxs-lookup"><span data-stu-id="0a13e-154">Requirement</span></span> | <span data-ttu-id="0a13e-155">Значение</span><span class="sxs-lookup"><span data-stu-id="0a13e-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a13e-156">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0a13e-156">Minimum supported client</span></span><br/> | <span data-ttu-id="0a13e-157">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0a13e-157">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="0a13e-158">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0a13e-158">Minimum supported server</span></span><br/> | <span data-ttu-id="0a13e-159">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0a13e-159">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0a13e-160">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="0a13e-160">Type library</span></span><br/>             | <dl> <span data-ttu-id="0a13e-161"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0a13e-161"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0a13e-162">DLL</span><span class="sxs-lookup"><span data-stu-id="0a13e-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a13e-163"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a13e-163"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a13e-164">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0a13e-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a13e-165">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="0a13e-165">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="0a13e-166">**тригжерколлектион**</span><span class="sxs-lookup"><span data-stu-id="0a13e-166">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="0a13e-167">**Тригжерколлектион. Create**</span><span class="sxs-lookup"><span data-stu-id="0a13e-167">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





