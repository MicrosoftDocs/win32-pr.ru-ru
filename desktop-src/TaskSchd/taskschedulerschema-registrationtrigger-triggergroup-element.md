---
title: Регистратионтригжер (Тригжерграуп), элемент
description: Указывает триггер, который запускает задачу при регистрации задачи.
ms.assetid: 8f028ed0-93e6-4423-be2f-9a02be99122b
keywords:
- планировщик задач триггера регистрации, XML-элемент
- планировщик задач элемента Регистратионтригжер
topic_type:
- apiref
api_name:
- RegistrationTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 90960f81d252b0b0a8d1de3ab5cc1465003467a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681983"
---
# <a name="registrationtrigger-triggergroup-element"></a><span data-ttu-id="c98ce-105">Регистратионтригжер (Тригжерграуп), элемент</span><span class="sxs-lookup"><span data-stu-id="c98ce-105">RegistrationTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="c98ce-106">Указывает триггер, который запускает задачу при регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="c98ce-106">Specifies a trigger that starts a task when the task is registered.</span></span>

``` syntax
<xs:element name="RegistrationTrigger"
    type="registrationTriggerType"
 />
```

<span data-ttu-id="c98ce-107">Элемент **регистратионтригжер** определяется сложным типом [**регистратионтригжертипе**](taskschedulerschema-registrationtriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c98ce-107">The **RegistrationTrigger** element is defined by the [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="c98ce-108">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="c98ce-108">Parent element</span></span>



| <span data-ttu-id="c98ce-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="c98ce-109">Element</span></span>                                                           | <span data-ttu-id="c98ce-110">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="c98ce-110">Derived from</span></span>                                                         | <span data-ttu-id="c98ce-111">Описание</span><span class="sxs-lookup"><span data-stu-id="c98ce-111">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="c98ce-112">**Триггеры**</span><span class="sxs-lookup"><span data-stu-id="c98ce-112">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="c98ce-113">**тригжерстипе**</span><span class="sxs-lookup"><span data-stu-id="c98ce-113">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="c98ce-114">Задает триггеры, которые запускают задачу.</span><span class="sxs-lookup"><span data-stu-id="c98ce-114">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="c98ce-115">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="c98ce-115">Child elements</span></span>



| <span data-ttu-id="c98ce-116">Элемент</span><span class="sxs-lookup"><span data-stu-id="c98ce-116">Element</span></span>                                                                                                        | <span data-ttu-id="c98ce-117">Тип</span><span class="sxs-lookup"><span data-stu-id="c98ce-117">Type</span></span>                                                                     | <span data-ttu-id="c98ce-118">Описание</span><span class="sxs-lookup"><span data-stu-id="c98ce-118">Description</span></span>                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c98ce-119">**Задержка (Регистратионтригжертипе)**</span><span class="sxs-lookup"><span data-stu-id="c98ce-119">**Delay (registrationTriggerType)**</span></span>](taskschedulerschema-delay-boottriggertype-element.md)                   | <span data-ttu-id="c98ce-120">длительность</span><span class="sxs-lookup"><span data-stu-id="c98ce-120">duration</span></span>                                                                 | <span data-ttu-id="c98ce-121">Указывает промежуток времени между регистрацией задачи и началом задачи.</span><span class="sxs-lookup"><span data-stu-id="c98ce-121">Specifies the amount of time between when the task is registered and when the task is started.</span></span><br/>                          |
| [<span data-ttu-id="c98ce-122">**Включено (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="c98ce-122">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                       | <span data-ttu-id="c98ce-123">Логическое</span><span class="sxs-lookup"><span data-stu-id="c98ce-123">boolean</span></span>                                                                  | <span data-ttu-id="c98ce-124">Указывает, что триггер включен.</span><span class="sxs-lookup"><span data-stu-id="c98ce-124">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="c98ce-125">**Ендбаундари (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="c98ce-125">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)               | <span data-ttu-id="c98ce-126">dateTime</span><span class="sxs-lookup"><span data-stu-id="c98ce-126">dateTime</span></span>                                                                 | <span data-ttu-id="c98ce-127">Указывает дату и время деактивации триггера.</span><span class="sxs-lookup"><span data-stu-id="c98ce-127">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="c98ce-128">Триггер не может запустить задачу после ее деактивации.</span><span class="sxs-lookup"><span data-stu-id="c98ce-128">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="c98ce-129">**Ексекутионтимелимит (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="c98ce-129">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | <span data-ttu-id="c98ce-130">длительность</span><span class="sxs-lookup"><span data-stu-id="c98ce-130">duration</span></span>                                                                 | <span data-ttu-id="c98ce-131">Указывает максимальное время, в течение которого задача может запускаться триггером.</span><span class="sxs-lookup"><span data-stu-id="c98ce-131">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                   |
| [<span data-ttu-id="c98ce-132">**Повторение (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="c98ce-132">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [<span data-ttu-id="c98ce-133">**репетитионтипе**</span><span class="sxs-lookup"><span data-stu-id="c98ce-133">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="c98ce-134">Указывает, как часто выполняется задача и как долго шаблон повторения повторяется после запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="c98ce-134">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="c98ce-135">**Стартбаундари (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="c98ce-135">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)           | <span data-ttu-id="c98ce-136">dateTime</span><span class="sxs-lookup"><span data-stu-id="c98ce-136">dateTime</span></span>                                                                 | <span data-ttu-id="c98ce-137">Указывает дату и время активации триггера.</span><span class="sxs-lookup"><span data-stu-id="c98ce-137">Specifies the date and time when the trigger is activated.</span></span><br/>                                                              |



## <a name="attributes"></a><span data-ttu-id="c98ce-138">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="c98ce-138">Attributes</span></span>



| <span data-ttu-id="c98ce-139">Имя</span><span class="sxs-lookup"><span data-stu-id="c98ce-139">Name</span></span> | <span data-ttu-id="c98ce-140">Тип</span><span class="sxs-lookup"><span data-stu-id="c98ce-140">Type</span></span> | <span data-ttu-id="c98ce-141">Описание</span><span class="sxs-lookup"><span data-stu-id="c98ce-141">Description</span></span>                           |
|------|------|---------------------------------------|
| <span data-ttu-id="c98ce-142">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="c98ce-142">Id</span></span>   | <span data-ttu-id="c98ce-143">ID</span><span class="sxs-lookup"><span data-stu-id="c98ce-143">ID</span></span>   | <span data-ttu-id="c98ce-144">Идентификатор триггера.</span><span class="sxs-lookup"><span data-stu-id="c98ce-144">Identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c98ce-145">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c98ce-145">Remarks</span></span>

<span data-ttu-id="c98ce-146">Для разработки сценариев триггер регистрации указывается с помощью объекта [**регистратионтригжер**](registrationtrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="c98ce-146">For scripting development, a registration trigger is specified using the [**RegistrationTrigger**](registrationtrigger.md) object.</span></span>

<span data-ttu-id="c98ce-147">Для разработки на C++ триггер регистрации указывается с помощью интерфейса [**ирегистратионтригжер**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger) .</span><span class="sxs-lookup"><span data-stu-id="c98ce-147">For C++ development, a registration trigger is specified using the [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger) interface.</span></span>

<span data-ttu-id="c98ce-148">Перечисленные выше дочерние элементы определяются сложными типами элементов [**тригжербасетипе**](taskschedulerschema-triggerbasetype-complextype.md) и [**регистратионтригжертипе**](taskschedulerschema-registrationtriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c98ce-148">The child elements listed above are defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) and [**registrationTriggerType**](taskschedulerschema-registrationtriggertype-complextype.md) complex element types.</span></span> <span data-ttu-id="c98ce-149">Эти элементы должны быть добавлены в приведенной ниже последовательности.</span><span class="sxs-lookup"><span data-stu-id="c98ce-149">These elements must be added in the sequence shown below.</span></span>

-   [<span data-ttu-id="c98ce-150">**Стартбаундари (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="c98ce-150">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="c98ce-151">**Ендбаундари (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="c98ce-151">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="c98ce-152">**Включено (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="c98ce-152">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [<span data-ttu-id="c98ce-153">**Повторение (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="c98ce-153">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [<span data-ttu-id="c98ce-154">**Ексекутионтимелимит (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="c98ce-154">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
-   [<span data-ttu-id="c98ce-155">**Задержка (Регистратионтригжертипе)**</span><span class="sxs-lookup"><span data-stu-id="c98ce-155">**Delay (registrationTriggerType)**</span></span>](taskschedulerschema-delay-boottriggertype-element.md)

## <a name="examples"></a><span data-ttu-id="c98ce-156">Примеры</span><span class="sxs-lookup"><span data-stu-id="c98ce-156">Examples</span></span>

<span data-ttu-id="c98ce-157">Полный пример XML-кода для задачи, указывающей триггер загрузки, см. в разделе [пример триггера регистрации (XML)](registration-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="c98ce-157">For a complete example of the XML for a task that specifies a boot trigger, see [Registration Trigger Example (XML)](registration-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c98ce-158">Требования</span><span class="sxs-lookup"><span data-stu-id="c98ce-158">Requirements</span></span>



| <span data-ttu-id="c98ce-159">Требование</span><span class="sxs-lookup"><span data-stu-id="c98ce-159">Requirement</span></span> | <span data-ttu-id="c98ce-160">Значение</span><span class="sxs-lookup"><span data-stu-id="c98ce-160">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c98ce-161">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c98ce-161">Minimum supported client</span></span><br/> | <span data-ttu-id="c98ce-162">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c98ce-162">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c98ce-163">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c98ce-163">Minimum supported server</span></span><br/> | <span data-ttu-id="c98ce-164">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c98ce-164">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c98ce-165">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c98ce-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c98ce-166">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="c98ce-166">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="c98ce-167">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="c98ce-167">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





