---
title: Логонтригжер (Тригжерграуп), элемент
description: Указывает триггер, который запускает задачу при входе пользователя в систему.
ms.assetid: c3edee50-e053-4813-a1b2-bf1e7b575ff7
keywords:
- триггер LOGON, XML-элемент
- планировщик задач элемента Логонтригжер
topic_type:
- apiref
api_name:
- LogonTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c89d0e593277f1c854850017412b49c22d8ac436
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340545"
---
# <a name="logontrigger-triggergroup-element"></a><span data-ttu-id="f3039-105">Логонтригжер (Тригжерграуп), элемент</span><span class="sxs-lookup"><span data-stu-id="f3039-105">LogonTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="f3039-106">Указывает триггер, который запускает задачу при входе пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="f3039-106">Specifies a trigger that starts a task when a user logs on.</span></span>

``` syntax
<xs:element name="LogonTrigger"
    type="logonTriggerType"
 />
```

<span data-ttu-id="f3039-107">Элемент **логонтригжер** определяется параметром [**тригжерграуп**](taskschedulerschema-triggergroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="f3039-107">The **LogonTrigger** element is defined by the [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="f3039-108">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="f3039-108">Parent element</span></span>



| <span data-ttu-id="f3039-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="f3039-109">Element</span></span>                                                           | <span data-ttu-id="f3039-110">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="f3039-110">Derived from</span></span>                                                         | <span data-ttu-id="f3039-111">Описание</span><span class="sxs-lookup"><span data-stu-id="f3039-111">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="f3039-112">**Триггеры**</span><span class="sxs-lookup"><span data-stu-id="f3039-112">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="f3039-113">**тригжерстипе**</span><span class="sxs-lookup"><span data-stu-id="f3039-113">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="f3039-114">Задает триггеры, которые запускают задачу.</span><span class="sxs-lookup"><span data-stu-id="f3039-114">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="f3039-115">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="f3039-115">Child elements</span></span>



| <span data-ttu-id="f3039-116">Элемент</span><span class="sxs-lookup"><span data-stu-id="f3039-116">Element</span></span>                                                                                                        | <span data-ttu-id="f3039-117">Тип</span><span class="sxs-lookup"><span data-stu-id="f3039-117">Type</span></span>                                                                     | <span data-ttu-id="f3039-118">Описание</span><span class="sxs-lookup"><span data-stu-id="f3039-118">Description</span></span>                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f3039-119">**Задержка (Логонтригжертипе)**</span><span class="sxs-lookup"><span data-stu-id="f3039-119">**Delay (logonTriggerType)**</span></span>](taskschedulerschema-delay-logontriggertype-element.md)                         | <span data-ttu-id="f3039-120">длительность</span><span class="sxs-lookup"><span data-stu-id="f3039-120">duration</span></span>                                                                 | <span data-ttu-id="f3039-121">Промежуток времени между входом пользователя в систему и запуском задачи.</span><span class="sxs-lookup"><span data-stu-id="f3039-121">Amount of time between when the user logs on and when the task is started.</span></span><br/>                                              |
| [<span data-ttu-id="f3039-122">**Включено (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="f3039-122">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                       | <span data-ttu-id="f3039-123">Логическое</span><span class="sxs-lookup"><span data-stu-id="f3039-123">boolean</span></span>                                                                  | <span data-ttu-id="f3039-124">Указывает, что триггер включен.</span><span class="sxs-lookup"><span data-stu-id="f3039-124">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="f3039-125">**Ендбаундари (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="f3039-125">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)               | <span data-ttu-id="f3039-126">dateTime</span><span class="sxs-lookup"><span data-stu-id="f3039-126">dateTime</span></span>                                                                 | <span data-ttu-id="f3039-127">Указывает дату и время деактивации триггера.</span><span class="sxs-lookup"><span data-stu-id="f3039-127">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="f3039-128">Триггер не может запустить задачу после ее деактивации.</span><span class="sxs-lookup"><span data-stu-id="f3039-128">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="f3039-129">**Ексекутионтимелимит (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="f3039-129">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | <span data-ttu-id="f3039-130">длительность</span><span class="sxs-lookup"><span data-stu-id="f3039-130">duration</span></span>                                                                 | <span data-ttu-id="f3039-131">Указывает максимальное время, в течение которого задача может запускаться триггером.</span><span class="sxs-lookup"><span data-stu-id="f3039-131">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                   |
| [<span data-ttu-id="f3039-132">**Повторение (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="f3039-132">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [<span data-ttu-id="f3039-133">**репетитионтипе**</span><span class="sxs-lookup"><span data-stu-id="f3039-133">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="f3039-134">Указывает, как часто выполняется задача и как долго шаблон повторения повторяется после запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="f3039-134">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="f3039-135">**Стартбаундари (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="f3039-135">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)           | <span data-ttu-id="f3039-136">dateTime</span><span class="sxs-lookup"><span data-stu-id="f3039-136">dateTime</span></span>                                                                 | <span data-ttu-id="f3039-137">Указывает дату и время активации триггера.</span><span class="sxs-lookup"><span data-stu-id="f3039-137">Specifies the date and time when the trigger is activated.</span></span><br/>                                                              |
| [<span data-ttu-id="f3039-138">**UserId (Логонтригжертипе)**</span><span class="sxs-lookup"><span data-stu-id="f3039-138">**UserId (logonTriggerType)**</span></span>](taskschedulerschema-userid-logontriggertype-element.md)                       | <span data-ttu-id="f3039-139">строка</span><span class="sxs-lookup"><span data-stu-id="f3039-139">string</span></span>                                                                   | <span data-ttu-id="f3039-140">Идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="f3039-140">Identifier of the user.</span></span> <span data-ttu-id="f3039-141">Задача запускается, когда пользователь входит в систему на компьютере.</span><span class="sxs-lookup"><span data-stu-id="f3039-141">The task is started when this user logs onto the computer.</span></span><br/>                                      |



## <a name="remarks"></a><span data-ttu-id="f3039-142">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f3039-142">Remarks</span></span>

<span data-ttu-id="f3039-143">Для разработки сценариев триггер входа задается с помощью объекта [**логонтригжер**](logontrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="f3039-143">For scripting development, a logon trigger is specified using the [**LogonTrigger**](logontrigger.md) object.</span></span>

<span data-ttu-id="f3039-144">Для разработки на C++ триггер входа указывается с помощью интерфейса [**илогонтригжер**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger) .</span><span class="sxs-lookup"><span data-stu-id="f3039-144">For C++ development, a logon trigger is specified using the [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger) interface.</span></span>

<span data-ttu-id="f3039-145">Перечисленные выше дочерние элементы определяются сложными типами элементов [**тригжербасетипе**](taskschedulerschema-triggerbasetype-complextype.md) и [**логонтригжертипе**](taskschedulerschema-logontriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f3039-145">The child elements listed above are defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) and [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) complex element types.</span></span> <span data-ttu-id="f3039-146">Эти элементы должны быть добавлены в приведенной ниже последовательности.</span><span class="sxs-lookup"><span data-stu-id="f3039-146">These elements must be added in the sequence shown below.</span></span>

-   [<span data-ttu-id="f3039-147">**Стартбаундари (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="f3039-147">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="f3039-148">**Ендбаундари (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="f3039-148">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="f3039-149">**Включено (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="f3039-149">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [<span data-ttu-id="f3039-150">**Повторение (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="f3039-150">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [<span data-ttu-id="f3039-151">**Ексекутионтимелимит (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="f3039-151">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
-   [<span data-ttu-id="f3039-152">**UserId (Логонтригжертипе)**</span><span class="sxs-lookup"><span data-stu-id="f3039-152">**UserId (logonTriggerType)**</span></span>](taskschedulerschema-userid-logontriggertype-element.md)
-   [<span data-ttu-id="f3039-153">**Задержка (Логонтригжертипе)**</span><span class="sxs-lookup"><span data-stu-id="f3039-153">**Delay (logonTriggerType)**</span></span>](taskschedulerschema-delay-logontriggertype-element.md)

### <a name="attributes"></a><span data-ttu-id="f3039-154">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="f3039-154">Attributes</span></span>

<span data-ttu-id="f3039-155">Приведенный ниже атрибут определяется сложными типами элементов [**тригжербасетипе**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f3039-155">The attribute listed below is defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex element types.</span></span>

-   <span data-ttu-id="f3039-156">ID: Идентификатор триггера.</span><span class="sxs-lookup"><span data-stu-id="f3039-156">Id: Identifier of the trigger.</span></span>

## <a name="examples"></a><span data-ttu-id="f3039-157">Примеры</span><span class="sxs-lookup"><span data-stu-id="f3039-157">Examples</span></span>

<span data-ttu-id="f3039-158">Полный пример XML-кода для задачи, использующей триггер входа, см. в разделе [пример триггера LOGON (XML)](logon-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="f3039-158">For a complete example of the XML for a task that uses a logon trigger, see [Logon Trigger Example (XML)](logon-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f3039-159">Требования</span><span class="sxs-lookup"><span data-stu-id="f3039-159">Requirements</span></span>



| <span data-ttu-id="f3039-160">Требование</span><span class="sxs-lookup"><span data-stu-id="f3039-160">Requirement</span></span> | <span data-ttu-id="f3039-161">Значение</span><span class="sxs-lookup"><span data-stu-id="f3039-161">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f3039-162">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f3039-162">Minimum supported client</span></span><br/> | <span data-ttu-id="f3039-163">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f3039-163">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f3039-164">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f3039-164">Minimum supported server</span></span><br/> | <span data-ttu-id="f3039-165">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f3039-165">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f3039-166">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f3039-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3039-167">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="f3039-167">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





