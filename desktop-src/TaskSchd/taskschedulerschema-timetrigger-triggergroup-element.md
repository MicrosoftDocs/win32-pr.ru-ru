---
title: Тиметригжер (Тригжерграуп), элемент
description: Указывает триггер, который запускает задачу при активации триггера.
ms.assetid: bb467f36-47cd-4db4-97c4-60c09937caac
keywords:
- планировщик задач элемента Тиметригжер
topic_type:
- apiref
api_name:
- TimeTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 83d3b0a63a8be70af7eba4edb90e49db71892f5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492054"
---
# <a name="timetrigger-triggergroup-element"></a><span data-ttu-id="e78fc-104">Тиметригжер (Тригжерграуп), элемент</span><span class="sxs-lookup"><span data-stu-id="e78fc-104">TimeTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="e78fc-105">Указывает триггер, который запускает задачу при активации триггера.</span><span class="sxs-lookup"><span data-stu-id="e78fc-105">Specifies a trigger that starts a task when the trigger is activated.</span></span>

``` syntax
<xs:element name="TimeTrigger"
    type="timeTriggerType"
 />
```

<span data-ttu-id="e78fc-106">Элемент **тиметригжер** определяется параметром [**тригжерграуп**](taskschedulerschema-triggergroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="e78fc-106">The **TimeTrigger** element is defined by the [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="e78fc-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="e78fc-107">Parent element</span></span>



| <span data-ttu-id="e78fc-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="e78fc-108">Element</span></span>                                                           | <span data-ttu-id="e78fc-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="e78fc-109">Derived from</span></span>                                                         | <span data-ttu-id="e78fc-110">Описание</span><span class="sxs-lookup"><span data-stu-id="e78fc-110">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="e78fc-111">**Триггеры**</span><span class="sxs-lookup"><span data-stu-id="e78fc-111">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="e78fc-112">**тригжерстипе**</span><span class="sxs-lookup"><span data-stu-id="e78fc-112">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="e78fc-113">Задает триггеры, которые запускают задачу.</span><span class="sxs-lookup"><span data-stu-id="e78fc-113">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="e78fc-114">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="e78fc-114">Child elements</span></span>



| <span data-ttu-id="e78fc-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="e78fc-115">Element</span></span>                                                                                                        | <span data-ttu-id="e78fc-116">Тип</span><span class="sxs-lookup"><span data-stu-id="e78fc-116">Type</span></span>                                                                     | <span data-ttu-id="e78fc-117">Описание</span><span class="sxs-lookup"><span data-stu-id="e78fc-117">Description</span></span>                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e78fc-118">**Включено (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="e78fc-118">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                       | <span data-ttu-id="e78fc-119">Логическое</span><span class="sxs-lookup"><span data-stu-id="e78fc-119">boolean</span></span>                                                                  | <span data-ttu-id="e78fc-120">Указывает, что триггер включен.</span><span class="sxs-lookup"><span data-stu-id="e78fc-120">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="e78fc-121">**Ендбаундари (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="e78fc-121">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)               | <span data-ttu-id="e78fc-122">dateTime</span><span class="sxs-lookup"><span data-stu-id="e78fc-122">dateTime</span></span>                                                                 | <span data-ttu-id="e78fc-123">Указывает дату и время деактивации триггера.</span><span class="sxs-lookup"><span data-stu-id="e78fc-123">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="e78fc-124">Триггер не может запустить задачу после ее деактивации.</span><span class="sxs-lookup"><span data-stu-id="e78fc-124">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="e78fc-125">**Ексекутионтимелимит (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="e78fc-125">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | <span data-ttu-id="e78fc-126">длительность</span><span class="sxs-lookup"><span data-stu-id="e78fc-126">duration</span></span>                                                                 | <span data-ttu-id="e78fc-127">Указывает максимальное время, в течение которого задача может запускаться триггером.</span><span class="sxs-lookup"><span data-stu-id="e78fc-127">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                   |
| [<span data-ttu-id="e78fc-128">**Повторение (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="e78fc-128">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [<span data-ttu-id="e78fc-129">**репетитионтипе**</span><span class="sxs-lookup"><span data-stu-id="e78fc-129">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="e78fc-130">Указывает, как часто выполняется задача и как долго шаблон повторения повторяется после запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="e78fc-130">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="e78fc-131">**Стартбаундари (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="e78fc-131">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)           | <span data-ttu-id="e78fc-132">dateTime</span><span class="sxs-lookup"><span data-stu-id="e78fc-132">dateTime</span></span>                                                                 | <span data-ttu-id="e78fc-133">Указывает дату и время активации триггера.</span><span class="sxs-lookup"><span data-stu-id="e78fc-133">Specifies the date and time when the trigger is activated.</span></span> <span data-ttu-id="e78fc-134">Этот элемент является обязательным.</span><span class="sxs-lookup"><span data-stu-id="e78fc-134">This element is required.</span></span><br/>                                    |



## <a name="attributes"></a><span data-ttu-id="e78fc-135">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e78fc-135">Attributes</span></span>



| <span data-ttu-id="e78fc-136">Имя</span><span class="sxs-lookup"><span data-stu-id="e78fc-136">Name</span></span> | <span data-ttu-id="e78fc-137">Тип</span><span class="sxs-lookup"><span data-stu-id="e78fc-137">Type</span></span>       | <span data-ttu-id="e78fc-138">Описание</span><span class="sxs-lookup"><span data-stu-id="e78fc-138">Description</span></span>                               |
|------|------------|-------------------------------------------|
| <span data-ttu-id="e78fc-139">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="e78fc-139">Id</span></span>   | <span data-ttu-id="e78fc-140">**string**</span><span class="sxs-lookup"><span data-stu-id="e78fc-140">**string**</span></span> | <span data-ttu-id="e78fc-141">Идентификатор триггера.</span><span class="sxs-lookup"><span data-stu-id="e78fc-141">The identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e78fc-142">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e78fc-142">Remarks</span></span>

<span data-ttu-id="e78fc-143">Элемент [**стартбаундари**](taskschedulerschema-startboundary-triggerbasetype-element.md) является обязательным элементом для триггеров времени и календаря (**тиметригжер** и [**календартригжер**](taskschedulerschema-calendartrigger-triggergroup-element.md)).</span><span class="sxs-lookup"><span data-stu-id="e78fc-143">The [**StartBoundary**](taskschedulerschema-startboundary-triggerbasetype-element.md) element is a required element for time and calendar triggers (**TimeTrigger** and [**CalendarTrigger**](taskschedulerschema-calendartrigger-triggergroup-element.md)).</span></span>

<span data-ttu-id="e78fc-144">Для разработки сценариев триггер времени указывается с помощью объекта [**тиметригжер**](timetrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="e78fc-144">For scripting development, a time trigger is specified using the [**TimeTrigger**](timetrigger.md) object.</span></span>

<span data-ttu-id="e78fc-145">Для разработки на C++ триггер времени указывается с помощью интерфейса [**итиметригжер**](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger) .</span><span class="sxs-lookup"><span data-stu-id="e78fc-145">For C++ development, a time trigger is specified using the [**ITimeTrigger**](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger) interface.</span></span>

<span data-ttu-id="e78fc-146">Перечисленные выше дочерние элементы определяются сложными типами элементов [**тригжербасетипе**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="e78fc-146">The child elements listed above are defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex element types.</span></span> <span data-ttu-id="e78fc-147">Эти элементы должны быть добавлены в приведенной ниже последовательности.</span><span class="sxs-lookup"><span data-stu-id="e78fc-147">These elements must be added in the sequence shown below.</span></span>

-   [<span data-ttu-id="e78fc-148">**Стартбаундари (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="e78fc-148">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="e78fc-149">**Ендбаундари (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="e78fc-149">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="e78fc-150">**Включено (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="e78fc-150">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [<span data-ttu-id="e78fc-151">**Повторение (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="e78fc-151">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [<span data-ttu-id="e78fc-152">**Ексекутионтимелимит (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="e78fc-152">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)

## <a name="examples"></a><span data-ttu-id="e78fc-153">Примеры</span><span class="sxs-lookup"><span data-stu-id="e78fc-153">Examples</span></span>

<span data-ttu-id="e78fc-154">Полный пример XML-кода для задачи, указывающей триггер времени, см. в разделе [пример триггера времени (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="e78fc-154">For a complete example of the XML for a task that specifies a time trigger, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e78fc-155">Требования</span><span class="sxs-lookup"><span data-stu-id="e78fc-155">Requirements</span></span>



| <span data-ttu-id="e78fc-156">Требование</span><span class="sxs-lookup"><span data-stu-id="e78fc-156">Requirement</span></span> | <span data-ttu-id="e78fc-157">Значение</span><span class="sxs-lookup"><span data-stu-id="e78fc-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e78fc-158">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e78fc-158">Minimum supported client</span></span><br/> | <span data-ttu-id="e78fc-159">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e78fc-159">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e78fc-160">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e78fc-160">Minimum supported server</span></span><br/> | <span data-ttu-id="e78fc-161">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e78fc-161">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e78fc-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e78fc-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e78fc-163">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="e78fc-163">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





