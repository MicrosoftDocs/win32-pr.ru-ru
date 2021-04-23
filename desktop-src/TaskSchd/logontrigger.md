---
title: Объект Логонтригжер
description: Объект скрипта, представляющий триггер, который запускает задачу при входе пользователя в систему.
ms.assetid: 1a1c10ce-4273-490a-a732-a8d39773203b
keywords:
- триггер входа планировщик задач, объект
- планировщик задач объекта Логонтригжер
- Планировщик задач объекта Логонтригжер, описание
topic_type:
- apiref
api_name:
- LogonTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b9c4b2031b39a6dfd483b039023ad9114271b21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988953"
---
# <a name="logontrigger-object"></a><span data-ttu-id="70c21-106">Объект Логонтригжер</span><span class="sxs-lookup"><span data-stu-id="70c21-106">LogonTrigger object</span></span>

<span data-ttu-id="70c21-107">Объект скрипта, представляющий триггер, который запускает задачу при входе пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="70c21-107">Scripting object that represents a trigger that starts a task when a user logs on.</span></span> <span data-ttu-id="70c21-108">При запуске службы планировщик задач выполняется перечисление всех вошедших в систему пользователей и выполняются все задачи, зарегистрированные с помощью триггеров входа, соответствующих вошедшему в систему пользователю.</span><span class="sxs-lookup"><span data-stu-id="70c21-108">When the Task Scheduler service starts, all logged-on users are enumerated and any tasks registered with logon triggers that match the logged on user are run.</span></span>

## <a name="members"></a><span data-ttu-id="70c21-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="70c21-109">Members</span></span>

<span data-ttu-id="70c21-110">Объект **логонтригжер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="70c21-110">The **LogonTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="70c21-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="70c21-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="70c21-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="70c21-112">Properties</span></span>

<span data-ttu-id="70c21-113">Объект **логонтригжер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="70c21-113">The **LogonTrigger** object has these properties.</span></span>



| <span data-ttu-id="70c21-114">Свойство</span><span class="sxs-lookup"><span data-stu-id="70c21-114">Property</span></span>                                                            | <span data-ttu-id="70c21-115">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="70c21-115">Access type</span></span>           | <span data-ttu-id="70c21-116">Описание</span><span class="sxs-lookup"><span data-stu-id="70c21-116">Description</span></span>                                                                                                                                                                                               |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="70c21-117">**Задержка**</span><span class="sxs-lookup"><span data-stu-id="70c21-117">**Delay**</span></span>](logontrigger-delay.md)<br/>                      | <span data-ttu-id="70c21-118">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="70c21-118">Read/write</span></span><br/> | <span data-ttu-id="70c21-119">Возвращает или задает значение, указывающее промежуток времени между входом пользователя в систему и запуском задания.</span><span class="sxs-lookup"><span data-stu-id="70c21-119">Gets or sets a value that indicates the amount of time between when the user logs on and when the job is started.</span></span><br/>                                                                              |
| [<span data-ttu-id="70c21-120">**Активировано**</span><span class="sxs-lookup"><span data-stu-id="70c21-120">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="70c21-121">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="70c21-121">Read/write</span></span><br/> | <span data-ttu-id="70c21-122">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="70c21-122">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="70c21-123">Возвращает или задает логическое значение, указывающее, включен ли триггер.</span><span class="sxs-lookup"><span data-stu-id="70c21-123">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                              |
| [<span data-ttu-id="70c21-124">**ендбаундари**</span><span class="sxs-lookup"><span data-stu-id="70c21-124">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="70c21-125">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="70c21-125">Read/write</span></span><br/> | <span data-ttu-id="70c21-126">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="70c21-126">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="70c21-127">Возвращает или задает дату и время деактивации триггера.</span><span class="sxs-lookup"><span data-stu-id="70c21-127">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="70c21-128">Триггер не может запустить задачу после ее деактивации.</span><span class="sxs-lookup"><span data-stu-id="70c21-128">The trigger cannot start the task after it is deactivated.</span></span><br/>               |
| [<span data-ttu-id="70c21-129">**ексекутионтимелимит**</span><span class="sxs-lookup"><span data-stu-id="70c21-129">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="70c21-130">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="70c21-130">Read/write</span></span><br/> | <span data-ttu-id="70c21-131">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="70c21-131">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="70c21-132">Возвращает или задает максимальное время, в течение которого разрешено выполнение задачи, запущенной триггером.</span><span class="sxs-lookup"><span data-stu-id="70c21-132">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                                         |
| [<span data-ttu-id="70c21-133">**Удостоверения**</span><span class="sxs-lookup"><span data-stu-id="70c21-133">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | <span data-ttu-id="70c21-134">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="70c21-134">Read/write</span></span><br/> | <span data-ttu-id="70c21-135">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="70c21-135">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="70c21-136">Возвращает или задает идентификатор триггера.</span><span class="sxs-lookup"><span data-stu-id="70c21-136">Gets or sets the identifier for the trigger.</span></span><br/>                                                                                             |
| [<span data-ttu-id="70c21-137">**Повторение**</span><span class="sxs-lookup"><span data-stu-id="70c21-137">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="70c21-138">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="70c21-138">Read/write</span></span><br/> | <span data-ttu-id="70c21-139">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="70c21-139">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="70c21-140">Возвращает или задает значение, указывающее, как часто выполняется задача и как долго шаблон повторения повторяется после запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="70c21-140">Gets or sets a value that indicates how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |
| [<span data-ttu-id="70c21-141">**стартбаундари**</span><span class="sxs-lookup"><span data-stu-id="70c21-141">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="70c21-142">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="70c21-142">Read/write</span></span><br/> | <span data-ttu-id="70c21-143">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="70c21-143">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="70c21-144">Возвращает или задает дату и время активации триггера.</span><span class="sxs-lookup"><span data-stu-id="70c21-144">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                                            |
| [<span data-ttu-id="70c21-145">**Тип**</span><span class="sxs-lookup"><span data-stu-id="70c21-145">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | <span data-ttu-id="70c21-146">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="70c21-146">Read-only</span></span><br/>  | <span data-ttu-id="70c21-147">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="70c21-147">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="70c21-148">Возвращает тип триггера.</span><span class="sxs-lookup"><span data-stu-id="70c21-148">Gets the type of the trigger.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="70c21-149">**UserId**</span><span class="sxs-lookup"><span data-stu-id="70c21-149">**UserId**</span></span>](logontrigger-userid.md)<br/>                    | <span data-ttu-id="70c21-150">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="70c21-150">Read/write</span></span><br/> | <span data-ttu-id="70c21-151">Возвращает или задает идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="70c21-151">Gets or sets the identifier of the user.</span></span><br/>                                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="70c21-152">Комментарии</span><span class="sxs-lookup"><span data-stu-id="70c21-152">Remarks</span></span>

<span data-ttu-id="70c21-153">Если требуется активировать задачу при входе любого члена группы на компьютер, а не при входе определенного пользователя в систему, не присваивайте свойству [**логонтригжер. UserID**](logontrigger-userid.md) значение.</span><span class="sxs-lookup"><span data-stu-id="70c21-153">If you want a task to be triggered when any member of a group logs on to the computer rather than when a specific user logs on, then do not assign a value to the [**LogonTrigger.UserId**](logontrigger-userid.md) property.</span></span> <span data-ttu-id="70c21-154">Вместо этого создайте триггер LOGON с пустым свойством **логонтригжер. UserID** и назначьте участнику значение для задачи с помощью свойства [**Principal. groupId**](principal-groupid.md) .</span><span class="sxs-lookup"><span data-stu-id="70c21-154">Instead, create a logon trigger with an empty **LogonTrigger.UserId** property and assign a value to the principal for the task using the [**Principal.GroupId**](principal-groupid.md) property.</span></span>

<span data-ttu-id="70c21-155">При чтении или записи XML-кода для задачи триггер входа задается с помощью элемента [**логонтригжер**](taskschedulerschema-logontrigger-triggergroup-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="70c21-155">When reading or writing XML for a task, a logon trigger is specified using the [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="70c21-156">Примеры</span><span class="sxs-lookup"><span data-stu-id="70c21-156">Examples</span></span>

<span data-ttu-id="70c21-157">Дополнительные сведения и примеры кода для этого объекта скрипта см. в разделе [пример триггера входа (сценарии)](logon-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="70c21-157">For more information and example code for this scripting object, see [Logon Trigger Example (Scripting)](logon-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="70c21-158">Требования</span><span class="sxs-lookup"><span data-stu-id="70c21-158">Requirements</span></span>



| <span data-ttu-id="70c21-159">Требование</span><span class="sxs-lookup"><span data-stu-id="70c21-159">Requirement</span></span> | <span data-ttu-id="70c21-160">Значение</span><span class="sxs-lookup"><span data-stu-id="70c21-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="70c21-161">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="70c21-161">Minimum supported client</span></span><br/> | <span data-ttu-id="70c21-162">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="70c21-162">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="70c21-163">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="70c21-163">Minimum supported server</span></span><br/> | <span data-ttu-id="70c21-164">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="70c21-164">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="70c21-165">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="70c21-165">Type library</span></span><br/>             | <dl> <span data-ttu-id="70c21-166"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="70c21-166"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="70c21-167">DLL</span><span class="sxs-lookup"><span data-stu-id="70c21-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70c21-168"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70c21-168"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70c21-169">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="70c21-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70c21-170">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="70c21-170">**Trigger**</span></span>](trigger.md)
</dt> </dl>

 

 





