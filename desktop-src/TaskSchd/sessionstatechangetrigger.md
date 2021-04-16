---
title: Объект Сессионстатечанжетригжер
description: Объект скрипта, который активирует задачи для подключения консоли или отключения, удаленного подключения или отключения, а также для блокировки или разблокировки рабочей станцией.
ms.assetid: ea450b8a-81cc-4d24-b850-78c967dcc5b8
keywords:
- планировщик задач объекта Сессионстатечанжетригжер
- Планировщик задач объекта Сессионстатечанжетригжер, описание
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f55d41f495c714fe2e1798c79cc4f24b99987a49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672557"
---
# <a name="sessionstatechangetrigger-object"></a><span data-ttu-id="35355-105">Объект Сессионстатечанжетригжер</span><span class="sxs-lookup"><span data-stu-id="35355-105">SessionStateChangeTrigger object</span></span>

<span data-ttu-id="35355-106">Объект скрипта, который активирует задачи для подключения консоли или отключения, удаленного подключения или отключения, а также для блокировки или разблокировки рабочей станцией.</span><span class="sxs-lookup"><span data-stu-id="35355-106">Scripting object that triggers tasks for console connect or disconnect, remote connect or disconnect, or workstation lock or unlock notifications.</span></span>

## <a name="members"></a><span data-ttu-id="35355-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="35355-107">Members</span></span>

<span data-ttu-id="35355-108">Объект **сессионстатечанжетригжер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="35355-108">The **SessionStateChangeTrigger** object has these types of members:</span></span>

-   [<span data-ttu-id="35355-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="35355-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="35355-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="35355-110">Properties</span></span>

<span data-ttu-id="35355-111">Объект **сессионстатечанжетригжер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="35355-111">The **SessionStateChangeTrigger** object has these properties.</span></span>



| <span data-ttu-id="35355-112">Свойство</span><span class="sxs-lookup"><span data-stu-id="35355-112">Property</span></span>                                                                | <span data-ttu-id="35355-113">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="35355-113">Access type</span></span>           | <span data-ttu-id="35355-114">Описание</span><span class="sxs-lookup"><span data-stu-id="35355-114">Description</span></span>                                                                                                                                                                                               |
|:------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="35355-115">**Задержка**</span><span class="sxs-lookup"><span data-stu-id="35355-115">**Delay**</span></span>](sessionstatechangetrigger-delay.md)<br/>             | <span data-ttu-id="35355-116">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="35355-116">Read/write</span></span><br/> | <span data-ttu-id="35355-117">Возвращает или задает значение, указывающее, как долго происходит задержка перед запуском задачи после обнаружения изменения состояния сеанса сервера терминалов.</span><span class="sxs-lookup"><span data-stu-id="35355-117">Gets or sets a value that indicates how long of a delay takes place before a task is started after a Terminal Server session state change is detected.</span></span><br/>                                         |
| [<span data-ttu-id="35355-118">**Активировано**</span><span class="sxs-lookup"><span data-stu-id="35355-118">**Enabled**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_enabled)<br/>                          | <span data-ttu-id="35355-119">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="35355-119">Read/write</span></span><br/> | <span data-ttu-id="35355-120">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="35355-120">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="35355-121">Возвращает или задает логическое значение, указывающее, включен ли триггер.</span><span class="sxs-lookup"><span data-stu-id="35355-121">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                              |
| [<span data-ttu-id="35355-122">**ендбаундари**</span><span class="sxs-lookup"><span data-stu-id="35355-122">**EndBoundary**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_endboundary)<br/>                  | <span data-ttu-id="35355-123">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="35355-123">Read/write</span></span><br/> | <span data-ttu-id="35355-124">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="35355-124">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="35355-125">Возвращает или задает дату и время деактивации триггера.</span><span class="sxs-lookup"><span data-stu-id="35355-125">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="35355-126">Триггер не может запустить задачу после ее деактивации.</span><span class="sxs-lookup"><span data-stu-id="35355-126">The trigger cannot start the task after it is deactivated.</span></span><br/>               |
| [<span data-ttu-id="35355-127">**ексекутионтимелимит**</span><span class="sxs-lookup"><span data-stu-id="35355-127">**ExecutionTimeLimit**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_executiontimelimit)<br/>    | <span data-ttu-id="35355-128">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="35355-128">Read/write</span></span><br/> | <span data-ttu-id="35355-129">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="35355-129">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="35355-130">Возвращает или задает максимальное время, в течение которого задача может запускаться триггером.</span><span class="sxs-lookup"><span data-stu-id="35355-130">Gets or sets the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                                 |
| [<span data-ttu-id="35355-131">**Удостоверения**</span><span class="sxs-lookup"><span data-stu-id="35355-131">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                    | <span data-ttu-id="35355-132">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="35355-132">Read/write</span></span><br/> | <span data-ttu-id="35355-133">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="35355-133">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="35355-134">Возвращает или задает идентификатор триггера.</span><span class="sxs-lookup"><span data-stu-id="35355-134">Gets or sets the identifier for the trigger.</span></span><br/>                                                                                             |
| [<span data-ttu-id="35355-135">**Повторение**</span><span class="sxs-lookup"><span data-stu-id="35355-135">**Repetition**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_repetition)<br/>                    | <span data-ttu-id="35355-136">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="35355-136">Read/write</span></span><br/> | <span data-ttu-id="35355-137">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="35355-137">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="35355-138">Возвращает или задает значение, указывающее, как часто выполняется задача и как долго шаблон повторения повторяется после запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="35355-138">Gets or sets a value that indicates how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |
| [<span data-ttu-id="35355-139">**стартбаундари**</span><span class="sxs-lookup"><span data-stu-id="35355-139">**StartBoundary**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_startboundary)<br/>              | <span data-ttu-id="35355-140">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="35355-140">Read/write</span></span><br/> | <span data-ttu-id="35355-141">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="35355-141">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="35355-142">Возвращает или задает дату и время активации триггера.</span><span class="sxs-lookup"><span data-stu-id="35355-142">Gets or sets the date and time when the trigger is activated.</span></span><br/>                                                                            |
| [<span data-ttu-id="35355-143">**StateChange**</span><span class="sxs-lookup"><span data-stu-id="35355-143">**StateChange**</span></span>](sessionstatechangetrigger-statechange.md)<br/> | <span data-ttu-id="35355-144">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="35355-144">Read/write</span></span><br/> | <span data-ttu-id="35355-145">Возвращает или задает тип изменения сеанса сервера терминалов, запускающего запуск задачи.</span><span class="sxs-lookup"><span data-stu-id="35355-145">Gets or sets the kind of Terminal Server session change that would trigger a task launch.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="35355-146">**Тип**</span><span class="sxs-lookup"><span data-stu-id="35355-146">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                                | <span data-ttu-id="35355-147">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="35355-147">Read-only</span></span><br/>  | <span data-ttu-id="35355-148">Наследуется от объекта [**триггера**](trigger.md) .</span><span class="sxs-lookup"><span data-stu-id="35355-148">Inherited from the [**Trigger**](trigger.md) object.</span></span> <span data-ttu-id="35355-149">Возвращает тип триггера.</span><span class="sxs-lookup"><span data-stu-id="35355-149">Gets the type of the trigger.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="35355-150">**UserId**</span><span class="sxs-lookup"><span data-stu-id="35355-150">**UserId**</span></span>](sessionstatechangetrigger-userid.md)<br/>           | <span data-ttu-id="35355-151">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="35355-151">Read/write</span></span><br/> | <span data-ttu-id="35355-152">Возвращает или задает пользователя для сеанса сервера терминалов.</span><span class="sxs-lookup"><span data-stu-id="35355-152">Gets or sets the user for the Terminal Server session.</span></span> <span data-ttu-id="35355-153">При обнаружении изменения состояния сеанса для этого пользователя запускается задача.</span><span class="sxs-lookup"><span data-stu-id="35355-153">When a session state change is detected for this user, a task is started.</span></span><br/>                                                               |



 

## <a name="remarks"></a><span data-ttu-id="35355-154">Комментарии</span><span class="sxs-lookup"><span data-stu-id="35355-154">Remarks</span></span>

<span data-ttu-id="35355-155">При чтении или записи собственного XML-кода для задачи триггер изменения состояния сеанса задается с помощью элемента [**сессионстатечанжетригжер**](taskschedulerschema-sessionstatechangetrigger-triggergroup-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="35355-155">When reading or writing your own XML for a task, a session state change trigger is specified using the [**SessionStateChangeTrigger**](taskschedulerschema-sessionstatechangetrigger-triggergroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="35355-156">Требования</span><span class="sxs-lookup"><span data-stu-id="35355-156">Requirements</span></span>



| <span data-ttu-id="35355-157">Требование</span><span class="sxs-lookup"><span data-stu-id="35355-157">Requirement</span></span> | <span data-ttu-id="35355-158">Значение</span><span class="sxs-lookup"><span data-stu-id="35355-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35355-159">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="35355-159">Minimum supported client</span></span><br/> | <span data-ttu-id="35355-160">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="35355-160">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="35355-161">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="35355-161">Minimum supported server</span></span><br/> | <span data-ttu-id="35355-162">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="35355-162">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="35355-163">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="35355-163">Type library</span></span><br/>             | <dl> <span data-ttu-id="35355-164"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="35355-164"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="35355-165">DLL</span><span class="sxs-lookup"><span data-stu-id="35355-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35355-166"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35355-166"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35355-167">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="35355-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35355-168">**тригжерколлектион**</span><span class="sxs-lookup"><span data-stu-id="35355-168">**TriggerCollection**</span></span>](triggercollection.md)
</dt> <dt>

[<span data-ttu-id="35355-169">**Тригжерколлектион. Create**</span><span class="sxs-lookup"><span data-stu-id="35355-169">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> </dl>

 

 





