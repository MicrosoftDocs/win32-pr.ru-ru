---
title: Идлетригжер (Тригжерграуп), элемент
description: Указывает триггер, который запускает задачу при переходе компьютера в состояние простоя.
ms.assetid: c3e317b5-d1a7-46de-ace5-e066452583d3
keywords:
- триггер Idle, XML-элемент
- планировщик задач элемента Идлетригжер
topic_type:
- apiref
api_name:
- IdleTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 221d272145670b9514cde5ffbe8b02e5ddcd6e0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071298"
---
# <a name="idletrigger-triggergroup-element"></a><span data-ttu-id="3f3dd-105">Идлетригжер (Тригжерграуп), элемент</span><span class="sxs-lookup"><span data-stu-id="3f3dd-105">IdleTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="3f3dd-106">Указывает триггер, который запускает задачу при переходе компьютера в состояние простоя.</span><span class="sxs-lookup"><span data-stu-id="3f3dd-106">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span> <span data-ttu-id="3f3dd-107">Сведения об условиях простоя см. в разделе [условия простоя задачи](task-idle-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="3f3dd-107">For information about idle conditions, see [Task Idle Conditions](task-idle-conditions.md).</span></span>

``` syntax
<xs:element name="IdleTrigger"
    type="idleTriggerType"
 />
```

<span data-ttu-id="3f3dd-108">Элемент **идлетригжер** определяется параметром [**тригжерграуп**](taskschedulerschema-triggergroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="3f3dd-108">The **IdleTrigger** element is defined by the [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="3f3dd-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="3f3dd-109">Parent element</span></span>



| <span data-ttu-id="3f3dd-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="3f3dd-110">Element</span></span>                                                           | <span data-ttu-id="3f3dd-111">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="3f3dd-111">Derived from</span></span>                                                         | <span data-ttu-id="3f3dd-112">Описание</span><span class="sxs-lookup"><span data-stu-id="3f3dd-112">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="3f3dd-113">**Триггеры**</span><span class="sxs-lookup"><span data-stu-id="3f3dd-113">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="3f3dd-114">**тригжерстипе**</span><span class="sxs-lookup"><span data-stu-id="3f3dd-114">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="3f3dd-115">Задает триггеры, которые запускают задачу.</span><span class="sxs-lookup"><span data-stu-id="3f3dd-115">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="3f3dd-116">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="3f3dd-116">Child elements</span></span>



| <span data-ttu-id="3f3dd-117">Элемент</span><span class="sxs-lookup"><span data-stu-id="3f3dd-117">Element</span></span>                                                                                                        | <span data-ttu-id="3f3dd-118">Тип</span><span class="sxs-lookup"><span data-stu-id="3f3dd-118">Type</span></span>                                                                     | <span data-ttu-id="3f3dd-119">Описание</span><span class="sxs-lookup"><span data-stu-id="3f3dd-119">Description</span></span>                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3f3dd-120">**Включено (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="3f3dd-120">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                       | <span data-ttu-id="3f3dd-121">Логическое</span><span class="sxs-lookup"><span data-stu-id="3f3dd-121">boolean</span></span>                                                                  | <span data-ttu-id="3f3dd-122">Указывает, что триггер включен.</span><span class="sxs-lookup"><span data-stu-id="3f3dd-122">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="3f3dd-123">**Ендбаундари (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="3f3dd-123">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)               | <span data-ttu-id="3f3dd-124">dateTime</span><span class="sxs-lookup"><span data-stu-id="3f3dd-124">dateTime</span></span>                                                                 | <span data-ttu-id="3f3dd-125">Указывает дату и время деактивации триггера.</span><span class="sxs-lookup"><span data-stu-id="3f3dd-125">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="3f3dd-126">Триггер не может запустить задачу после ее деактивации.</span><span class="sxs-lookup"><span data-stu-id="3f3dd-126">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="3f3dd-127">**Ексекутионтимелимит (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="3f3dd-127">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | <span data-ttu-id="3f3dd-128">длительность</span><span class="sxs-lookup"><span data-stu-id="3f3dd-128">duration</span></span>                                                                 | <span data-ttu-id="3f3dd-129">Указывает максимальное время, в течение которого задача может запускаться триггером.</span><span class="sxs-lookup"><span data-stu-id="3f3dd-129">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                   |
| [<span data-ttu-id="3f3dd-130">**Повторение (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="3f3dd-130">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [<span data-ttu-id="3f3dd-131">**репетитионтипе**</span><span class="sxs-lookup"><span data-stu-id="3f3dd-131">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="3f3dd-132">Указывает, как часто выполняется задача и как долго шаблон повторения повторяется после запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="3f3dd-132">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="3f3dd-133">**Стартбаундари (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="3f3dd-133">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)           | <span data-ttu-id="3f3dd-134">dateTime</span><span class="sxs-lookup"><span data-stu-id="3f3dd-134">dateTime</span></span>                                                                 | <span data-ttu-id="3f3dd-135">Указывает дату и время активации триггера.</span><span class="sxs-lookup"><span data-stu-id="3f3dd-135">Specifies the date and time when the trigger is activated.</span></span><br/>                                                              |



## <a name="attributes"></a><span data-ttu-id="3f3dd-136">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="3f3dd-136">Attributes</span></span>



| <span data-ttu-id="3f3dd-137">Имя</span><span class="sxs-lookup"><span data-stu-id="3f3dd-137">Name</span></span> | <span data-ttu-id="3f3dd-138">Тип</span><span class="sxs-lookup"><span data-stu-id="3f3dd-138">Type</span></span>   | <span data-ttu-id="3f3dd-139">Описание</span><span class="sxs-lookup"><span data-stu-id="3f3dd-139">Description</span></span>                               |
|------|--------|-------------------------------------------|
| <span data-ttu-id="3f3dd-140">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="3f3dd-140">Id</span></span>   | <span data-ttu-id="3f3dd-141">строка</span><span class="sxs-lookup"><span data-stu-id="3f3dd-141">string</span></span> | <span data-ttu-id="3f3dd-142">Идентификатор триггера.</span><span class="sxs-lookup"><span data-stu-id="3f3dd-142">The identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3f3dd-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3f3dd-143">Remarks</span></span>

<span data-ttu-id="3f3dd-144">Для разработки сценариев триггер простоя указывается с помощью объекта [**идлетригжер**](idletrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="3f3dd-144">For scripting development, an idle trigger is specified using the [**IdleTrigger**](idletrigger.md) object.</span></span>

<span data-ttu-id="3f3dd-145">Для разработки на C++ триггер простоя указывается с помощью интерфейса [**иидлетригжер**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger) .</span><span class="sxs-lookup"><span data-stu-id="3f3dd-145">For C++ development, an idle trigger is specified using the [**IIdleTrigger**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger) interface.</span></span>

<span data-ttu-id="3f3dd-146">Перечисленные выше дочерние элементы определяются сложными типами элементов [**тригжербасетипе**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="3f3dd-146">The child elements listed above are defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex element types.</span></span> <span data-ttu-id="3f3dd-147">Эти элементы должны быть добавлены в приведенной ниже последовательности.</span><span class="sxs-lookup"><span data-stu-id="3f3dd-147">These elements must be added in the sequence shown below.</span></span>

-   [<span data-ttu-id="3f3dd-148">**Стартбаундари (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="3f3dd-148">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="3f3dd-149">**Ендбаундари (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="3f3dd-149">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [<span data-ttu-id="3f3dd-150">**Включено (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="3f3dd-150">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [<span data-ttu-id="3f3dd-151">**Повторение (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="3f3dd-151">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [<span data-ttu-id="3f3dd-152">**Ексекутионтимелимит (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="3f3dd-152">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)

## <a name="examples"></a><span data-ttu-id="3f3dd-153">Примеры</span><span class="sxs-lookup"><span data-stu-id="3f3dd-153">Examples</span></span>

<span data-ttu-id="3f3dd-154">Следующий XML-код определяет триггер простоя.</span><span class="sxs-lookup"><span data-stu-id="3f3dd-154">The following XML defines an idle trigger.</span></span>


```XML
<IdleTrigger>
    <StartBoundary>2005-01-01T00:08:00</StartBoundary>
    <EndBounadry>2007-01-01T00:08:00</EndBoundary>
    <Enabled></Enabled>
    <Repetition></Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
</IdleTrigger>
```



## <a name="requirements"></a><span data-ttu-id="3f3dd-155">Требования</span><span class="sxs-lookup"><span data-stu-id="3f3dd-155">Requirements</span></span>



| <span data-ttu-id="3f3dd-156">Требование</span><span class="sxs-lookup"><span data-stu-id="3f3dd-156">Requirement</span></span> | <span data-ttu-id="3f3dd-157">Значение</span><span class="sxs-lookup"><span data-stu-id="3f3dd-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3f3dd-158">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3f3dd-158">Minimum supported client</span></span><br/> | <span data-ttu-id="3f3dd-159">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3f3dd-159">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3f3dd-160">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3f3dd-160">Minimum supported server</span></span><br/> | <span data-ttu-id="3f3dd-161">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3f3dd-161">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3f3dd-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3f3dd-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f3dd-163">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="3f3dd-163">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="3f3dd-164">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="3f3dd-164">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

