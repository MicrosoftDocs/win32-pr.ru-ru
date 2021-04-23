---
title: Объект триггера
description: Объект скрипта, предоставляющий общие свойства, наследуемые всеми объектами триггера.
ms.assetid: dfc4cb36-8bdb-4aec-963e-5f1ec1ff85aa
keywords:
- триггеры планировщик задач, объект Trigger
- планировщик задач объекта триггера
- Планировщик задач объекта триггера, описание
topic_type:
- apiref
api_name:
- Trigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f4a7edc6eff0bb04c81ba3bff3bb86ec0455b25
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891669"
---
# <a name="trigger-object"></a><span data-ttu-id="606f2-106">Объект триггера</span><span class="sxs-lookup"><span data-stu-id="606f2-106">Trigger object</span></span>

<span data-ttu-id="606f2-107">Объект скрипта, предоставляющий общие свойства, наследуемые всеми объектами триггера.</span><span class="sxs-lookup"><span data-stu-id="606f2-107">Scripting object that provides the common properties that are inherited by all trigger objects.</span></span>

## <a name="members"></a><span data-ttu-id="606f2-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="606f2-108">Members</span></span>

<span data-ttu-id="606f2-109">Объект **триггера** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="606f2-109">The **Trigger** object has these types of members:</span></span>

-   [<span data-ttu-id="606f2-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="606f2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="606f2-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="606f2-111">Properties</span></span>

<span data-ttu-id="606f2-112">Объект **триггера** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="606f2-112">The **Trigger** object has these properties.</span></span>



| <span data-ttu-id="606f2-113">Свойство</span><span class="sxs-lookup"><span data-stu-id="606f2-113">Property</span></span>                                                            | <span data-ttu-id="606f2-114">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="606f2-114">Access type</span></span>           | <span data-ttu-id="606f2-115">Описание</span><span class="sxs-lookup"><span data-stu-id="606f2-115">Description</span></span>                                                                                                                                         |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="606f2-116">**Активировано**</span><span class="sxs-lookup"><span data-stu-id="606f2-116">**Enabled**</span></span>](trigger-enabled.md)<br/>                       | <span data-ttu-id="606f2-117">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="606f2-117">Read/write</span></span><br/> | <span data-ttu-id="606f2-118">Возвращает или задает логическое значение, указывающее, включен ли триггер.</span><span class="sxs-lookup"><span data-stu-id="606f2-118">Gets or sets a Boolean value that indicates whether the trigger is enabled.</span></span><br/>                                                              |
| [<span data-ttu-id="606f2-119">**ендбаундари**</span><span class="sxs-lookup"><span data-stu-id="606f2-119">**EndBoundary**</span></span>](trigger-endboundary.md)<br/>               | <span data-ttu-id="606f2-120">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="606f2-120">Read/write</span></span><br/> | <span data-ttu-id="606f2-121">Возвращает или задает дату и время деактивации триггера.</span><span class="sxs-lookup"><span data-stu-id="606f2-121">Gets or sets the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="606f2-122">Триггер не может запустить задачу после ее деактивации.</span><span class="sxs-lookup"><span data-stu-id="606f2-122">The trigger cannot start the task after it is deactivated.</span></span><br/>               |
| [<span data-ttu-id="606f2-123">**ексекутионтимелимит**</span><span class="sxs-lookup"><span data-stu-id="606f2-123">**ExecutionTimeLimit**</span></span>](trigger-executiontimelimit.md)<br/> | <span data-ttu-id="606f2-124">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="606f2-124">Read/write</span></span><br/> | <span data-ttu-id="606f2-125">Возвращает или задает максимальное время, в течение которого разрешено выполнение задачи, запущенной триггером.</span><span class="sxs-lookup"><span data-stu-id="606f2-125">Gets or sets the maximum amount of time that the task launched by the trigger is allowed to run.</span></span><br/>                                         |
| [<span data-ttu-id="606f2-126">**Удостоверения**</span><span class="sxs-lookup"><span data-stu-id="606f2-126">**Id**</span></span>](trigger-id.md)<br/>                                 | <span data-ttu-id="606f2-127">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="606f2-127">Read/write</span></span><br/> | <span data-ttu-id="606f2-128">Возвращает или задает идентификатор триггера.</span><span class="sxs-lookup"><span data-stu-id="606f2-128">Gets or sets the identifier for the trigger.</span></span><br/>                                                                                             |
| [<span data-ttu-id="606f2-129">**Повторение**</span><span class="sxs-lookup"><span data-stu-id="606f2-129">**Repetition**</span></span>](trigger-repetition.md)<br/>                 | <span data-ttu-id="606f2-130">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="606f2-130">Read/write</span></span><br/> | <span data-ttu-id="606f2-131">Возвращает или задает значение, указывающее, как часто выполняется задача и как долго шаблон повторения повторяется после запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="606f2-131">Gets or sets a value that indicates how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/> |
| [<span data-ttu-id="606f2-132">**стартбаундари**</span><span class="sxs-lookup"><span data-stu-id="606f2-132">**StartBoundary**</span></span>](trigger-startboundary.md)<br/>           | <span data-ttu-id="606f2-133">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="606f2-133">Read/write</span></span><br/> | <span data-ttu-id="606f2-134">Возвращает или задает дату и время активации триггера.</span><span class="sxs-lookup"><span data-stu-id="606f2-134">Gets or sets the date and time when the trigger is activated.</span></span> <span data-ttu-id="606f2-135">Триггер может запустить задачу после активации триггера.</span><span class="sxs-lookup"><span data-stu-id="606f2-135">The trigger can start the task after the trigger is activated.</span></span><br/>             |
| [<span data-ttu-id="606f2-136">**Тип**</span><span class="sxs-lookup"><span data-stu-id="606f2-136">**Type**</span></span>](trigger-type.md)<br/>                             |                       | <span data-ttu-id="606f2-137">Возвращает тип триггера.</span><span class="sxs-lookup"><span data-stu-id="606f2-137">Gets the type of the trigger.</span></span><br/>                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="606f2-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="606f2-138">Remarks</span></span>

<span data-ttu-id="606f2-139">Планировщик задач предоставляет следующие отдельные объекты для различных триггеров, которые может использовать задача.</span><span class="sxs-lookup"><span data-stu-id="606f2-139">The Task Scheduler provides the following individual objects for the different triggers that a task can use:</span></span>

-   [<span data-ttu-id="606f2-140">**буттригжер**</span><span class="sxs-lookup"><span data-stu-id="606f2-140">**BootTrigger**</span></span>](boottrigger.md)
-   [<span data-ttu-id="606f2-141">**даилитригжер**</span><span class="sxs-lookup"><span data-stu-id="606f2-141">**DailyTrigger**</span></span>](dailytrigger.md)
-   [<span data-ttu-id="606f2-142">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="606f2-142">**EventTrigger**</span></span>](eventtrigger.md)
-   [<span data-ttu-id="606f2-143">**идлетригжер**</span><span class="sxs-lookup"><span data-stu-id="606f2-143">**IdleTrigger**</span></span>](idletrigger.md)
-   [<span data-ttu-id="606f2-144">**логонтригжер**</span><span class="sxs-lookup"><span data-stu-id="606f2-144">**LogonTrigger**</span></span>](logontrigger.md)
-   [<span data-ttu-id="606f2-145">**монслидовтригжер**</span><span class="sxs-lookup"><span data-stu-id="606f2-145">**MonthlyDOWTrigger**</span></span>](monthlydowtrigger.md)
-   [<span data-ttu-id="606f2-146">**монслитригжер**</span><span class="sxs-lookup"><span data-stu-id="606f2-146">**MonthlyTrigger**</span></span>](monthlytrigger.md)
-   [<span data-ttu-id="606f2-147">**регистратионтригжер**</span><span class="sxs-lookup"><span data-stu-id="606f2-147">**RegistrationTrigger**</span></span>](registrationtrigger.md)
-   [<span data-ttu-id="606f2-148">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="606f2-148">**TimeTrigger**</span></span>](timetrigger.md)
-   [<span data-ttu-id="606f2-149">**виклитригжер**</span><span class="sxs-lookup"><span data-stu-id="606f2-149">**WeeklyTrigger**</span></span>](weeklytrigger.md)
-   [<span data-ttu-id="606f2-150">**сессионстатечанжетригжер**</span><span class="sxs-lookup"><span data-stu-id="606f2-150">**SessionStateChangeTrigger**</span></span>](sessionstatechangetrigger.md)

<span data-ttu-id="606f2-151">При чтении или записи XML триггеры задачи указываются в элементе [**Triggers**](taskschedulerschema-triggers-tasktype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="606f2-151">When reading or writing XML, the triggers of a task are specified in the [**Triggers**](taskschedulerschema-triggers-tasktype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="606f2-152">Примеры</span><span class="sxs-lookup"><span data-stu-id="606f2-152">Examples</span></span>

<span data-ttu-id="606f2-153">Дополнительные сведения и примеры кода для этого объекта скрипта см. в разделе [пример триггера времени (сценарии)](time-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="606f2-153">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="606f2-154">Требования</span><span class="sxs-lookup"><span data-stu-id="606f2-154">Requirements</span></span>



| <span data-ttu-id="606f2-155">Требование</span><span class="sxs-lookup"><span data-stu-id="606f2-155">Requirement</span></span> | <span data-ttu-id="606f2-156">Значение</span><span class="sxs-lookup"><span data-stu-id="606f2-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="606f2-157">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="606f2-157">Minimum supported client</span></span><br/> | <span data-ttu-id="606f2-158">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="606f2-158">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="606f2-159">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="606f2-159">Minimum supported server</span></span><br/> | <span data-ttu-id="606f2-160">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="606f2-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="606f2-161">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="606f2-161">Type library</span></span><br/>             | <dl> <span data-ttu-id="606f2-162"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="606f2-162"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="606f2-163">DLL</span><span class="sxs-lookup"><span data-stu-id="606f2-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="606f2-164"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="606f2-164"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="606f2-165">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="606f2-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="606f2-166">**тригжерколлектион**</span><span class="sxs-lookup"><span data-stu-id="606f2-166">**TriggerCollection**</span></span>](triggercollection.md)
</dt> </dl>

 

 





