---
title: Объект Регистратионтригжер
description: Объект скрипта, представляющий триггер, который запускает задачу при регистрации или обновлении задачи.
ms.assetid: 430ef3e0-9409-49ff-8ffb-31833938d8b2
keywords:
- триггер регистрации планировщик задач, объект
- планировщик задач объекта Регистратионтригжер
- Планировщик задач объекта Регистратионтригжер, описание
topic_type:
- apiref
api_name:
- RegistrationTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08bf84fa92b1736b2989c1920abb8f0af2c0b97c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534466"
---
# <a name="registrationtrigger-object"></a><span data-ttu-id="ecf8f-106">Объект Регистратионтригжер</span><span class="sxs-lookup"><span data-stu-id="ecf8f-106">RegistrationTrigger object</span></span>

<span data-ttu-id="ecf8f-107">Объект скрипта, представляющий триггер, который запускает задачу при регистрации или обновлении задачи.</span><span class="sxs-lookup"><span data-stu-id="ecf8f-107">Scripting object that represents a trigger that starts a task when the task is registered or updated.</span></span>

## <a name="members"></a><span data-ttu-id="ecf8f-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="ecf8f-108">Members</span></span>

<span data-ttu-id="ecf8f-109">Объект **регистратионтригжер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ecf8f-109">The **RegistrationTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="ecf8f-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="ecf8f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ecf8f-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="ecf8f-111">Properties</span></span>

<span data-ttu-id="ecf8f-112">Объект **регистратионтригжер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ecf8f-112">The **RegistrationTrigger** object has these properties.</span></span>



| <span data-ttu-id="ecf8f-113">Свойство</span><span class="sxs-lookup"><span data-stu-id="ecf8f-113">Property</span></span>                                                            | <span data-ttu-id="ecf8f-114">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="ecf8f-114">Access type</span></span>           | <span data-ttu-id="ecf8f-115">Описание</span><span class="sxs-lookup"><span data-stu-id="ecf8f-115">Description</span></span>                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ecf8f-116">**Задержка**</span><span class="sxs-lookup"><span data-stu-id="ecf8f-116">**Delay**</span></span>](registrationtrigger-delay.md)<br/>               | <span data-ttu-id="ecf8f-117">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ecf8f-117">Read/write</span></span><br/> | <span data-ttu-id="ecf8f-118">Возвращает или задает промежуток времени между регистрацией задачи и началом задачи.</span><span class="sxs-lookup"><span data-stu-id="ecf8f-118">Gets or sets the amount of time between when the task is registered and when the task is started.</span></span><br/>                                                                                |
| [<span data-ttu-id="ecf8f-119">**Активировано**</span><span class="sxs-lookup"><span data-stu-id="ecf8f-119">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="ecf8f-120">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ecf8f-120">Read/write</span></span><br/> | <span data-ttu-id="ecf8f-121">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="ecf8f-121">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="ecf8f-122">Возвращает или задает логическое значение, указывающее, включен ли триггер.</span><span class="sxs-lookup"><span data-stu-id="ecf8f-122">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                |
| [<span data-ttu-id="ecf8f-123">**ендбаундари**</span><span class="sxs-lookup"><span data-stu-id="ecf8f-123">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="ecf8f-124">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ecf8f-124">Read/write</span></span><br/> | <span data-ttu-id="ecf8f-125">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="ecf8f-125">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="ecf8f-126">Возвращает или задает дату и время деактивации триггера.</span><span class="sxs-lookup"><span data-stu-id="ecf8f-126">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="ecf8f-127">Триггер не может запустить задачу после ее деактивации.</span><span class="sxs-lookup"><span data-stu-id="ecf8f-127">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="ecf8f-128">**ексекутионтимелимит**</span><span class="sxs-lookup"><span data-stu-id="ecf8f-128">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="ecf8f-129">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ecf8f-129">Read/write</span></span><br/> | <span data-ttu-id="ecf8f-130">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="ecf8f-130">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="ecf8f-131">Возвращает или задает максимальное время, в течение которого разрешено выполнение задачи, запущенной триггером.</span><span class="sxs-lookup"><span data-stu-id="ecf8f-131">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                           |
| [<span data-ttu-id="ecf8f-132">**Удостоверения**</span><span class="sxs-lookup"><span data-stu-id="ecf8f-132">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="ecf8f-133">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ecf8f-133">Read/write</span></span><br/> | <span data-ttu-id="ecf8f-134">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="ecf8f-134">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="ecf8f-135">Возвращает или задает идентификатор триггера.</span><span class="sxs-lookup"><span data-stu-id="ecf8f-135">Gets or sets the identifier for the trigger.</span></span><br/>                                                                               |
| [<span data-ttu-id="ecf8f-136">**Повторение**</span><span class="sxs-lookup"><span data-stu-id="ecf8f-136">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="ecf8f-137">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ecf8f-137">Read/write</span></span><br/> | <span data-ttu-id="ecf8f-138">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="ecf8f-138">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="ecf8f-139">Возвращает или задает частоту выполнения задачи и период повторения шаблона повторения после запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="ecf8f-139">Gets or sets how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="ecf8f-140">**стартбаундари**</span><span class="sxs-lookup"><span data-stu-id="ecf8f-140">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="ecf8f-141">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ecf8f-141">Read/write</span></span><br/> | <span data-ttu-id="ecf8f-142">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="ecf8f-142">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="ecf8f-143">Возвращает или задает дату и время активации триггера.</span><span class="sxs-lookup"><span data-stu-id="ecf8f-143">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="ecf8f-144">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ecf8f-144">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="ecf8f-145">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="ecf8f-145">Read-only</span></span><br/>  | <span data-ttu-id="ecf8f-146">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="ecf8f-146">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="ecf8f-147">Возвращает тип триггера.</span><span class="sxs-lookup"><span data-stu-id="ecf8f-147">Gets the type of the trigger.</span></span><br/>                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="ecf8f-148">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ecf8f-148">Remarks</span></span>

<span data-ttu-id="ecf8f-149">При создании собственного XML-кода для задачи триггер регистрации указывается с помощью элемента [**регистратионтригжер**](taskschedulerschema-registrationtrigger-triggergroup-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="ecf8f-149">When creating your own XML for a task, a registration trigger is specified using the [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="ecf8f-150">Если регистрируется задача с триггером отложенной регистрации и компьютер, на котором зарегистрирована задача, завершается или перезапускается во время задержки, перед выполнением задачи Выполнение задачи не выполняется и задержка будет потеряна.</span><span class="sxs-lookup"><span data-stu-id="ecf8f-150">If a task with a delayed registration trigger is registered, and the computer that the task is registered on is shutdown or restarted during the delay, before the task runs, then the task will not run and the delay will be lost.</span></span>

## <a name="examples"></a><span data-ttu-id="ecf8f-151">Примеры</span><span class="sxs-lookup"><span data-stu-id="ecf8f-151">Examples</span></span>

<span data-ttu-id="ecf8f-152">Дополнительные сведения и пример кода для этого объекта скрипта см. в разделе [пример триггера регистрации (сценарии)](registration-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="ecf8f-152">For more information and a code example for this scripting object, see [Registration Trigger Example (Scripting)](registration-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ecf8f-153">Требования</span><span class="sxs-lookup"><span data-stu-id="ecf8f-153">Requirements</span></span>



| <span data-ttu-id="ecf8f-154">Требование</span><span class="sxs-lookup"><span data-stu-id="ecf8f-154">Requirement</span></span> | <span data-ttu-id="ecf8f-155">Значение</span><span class="sxs-lookup"><span data-stu-id="ecf8f-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ecf8f-156">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ecf8f-156">Minimum supported client</span></span><br/> | <span data-ttu-id="ecf8f-157">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ecf8f-157">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ecf8f-158">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ecf8f-158">Minimum supported server</span></span><br/> | <span data-ttu-id="ecf8f-159">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ecf8f-159">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ecf8f-160">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="ecf8f-160">Type library</span></span><br/>             | <dl> <span data-ttu-id="ecf8f-161"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ecf8f-161"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ecf8f-162">DLL</span><span class="sxs-lookup"><span data-stu-id="ecf8f-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ecf8f-163"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ecf8f-163"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecf8f-164">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ecf8f-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecf8f-165">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="ecf8f-165">**Trigger**</span></span>](trigger.md)
</dt> <dt>

[<span data-ttu-id="ecf8f-166">**тригжерколлектион**</span><span class="sxs-lookup"><span data-stu-id="ecf8f-166">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="ecf8f-167">**Тригжерколлектион. Create**</span><span class="sxs-lookup"><span data-stu-id="ecf8f-167">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





