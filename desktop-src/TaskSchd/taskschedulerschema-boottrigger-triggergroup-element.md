---
title: Буттригжер (Тригжерграуп), элемент
description: Указывает триггер, который запускает задачу при загрузке системы.
ms.assetid: c6833547-0daf-4e8a-b8c5-b422827b1d96
keywords:
- планировщик задач триггера загрузки, XML-элемент
- планировщик задач элемента Буттригжер
topic_type:
- apiref
api_name:
- BootTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb6ccf590893e19340662fd4c47e4aa68047b29d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340950"
---
# <a name="boottrigger-triggergroup-element"></a><span data-ttu-id="ff5bb-105">Буттригжер (Тригжерграуп), элемент</span><span class="sxs-lookup"><span data-stu-id="ff5bb-105">BootTrigger (triggerGroup) Element</span></span>

<span data-ttu-id="ff5bb-106">Указывает триггер, который запускает задачу при загрузке системы.</span><span class="sxs-lookup"><span data-stu-id="ff5bb-106">Specifies a trigger that starts a task when the system is booted.</span></span>

``` syntax
<xs:element name="BootTrigger"
    type="bootTriggerType"
 />
```

<span data-ttu-id="ff5bb-107">Элемент **буттригжер** определяется сложным типом [**буттригжертипе**](taskschedulerschema-boottriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="ff5bb-107">The **BootTrigger** element is defined by the [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="ff5bb-108">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="ff5bb-108">Parent element</span></span>



| <span data-ttu-id="ff5bb-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="ff5bb-109">Element</span></span>                                                           | <span data-ttu-id="ff5bb-110">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="ff5bb-110">Derived from</span></span>                                                         | <span data-ttu-id="ff5bb-111">Описание</span><span class="sxs-lookup"><span data-stu-id="ff5bb-111">Description</span></span>                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="ff5bb-112">**Триггеры**</span><span class="sxs-lookup"><span data-stu-id="ff5bb-112">**Triggers**</span></span>](taskschedulerschema-triggers-tasktype-element.md) | [<span data-ttu-id="ff5bb-113">**тригжерстипе**</span><span class="sxs-lookup"><span data-stu-id="ff5bb-113">**triggersType**</span></span>](taskschedulerschema-triggerstype-complextype.md) | <span data-ttu-id="ff5bb-114">Задает триггеры, которые запускают задачу.</span><span class="sxs-lookup"><span data-stu-id="ff5bb-114">Specifies the triggers that start the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="ff5bb-115">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ff5bb-115">Child elements</span></span>



| <span data-ttu-id="ff5bb-116">Элемент</span><span class="sxs-lookup"><span data-stu-id="ff5bb-116">Element</span></span>                                                                                                        | <span data-ttu-id="ff5bb-117">Тип</span><span class="sxs-lookup"><span data-stu-id="ff5bb-117">Type</span></span>                                                                     | <span data-ttu-id="ff5bb-118">Описание</span><span class="sxs-lookup"><span data-stu-id="ff5bb-118">Description</span></span>                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ff5bb-119">**Задержка (Буттригжертипе)**</span><span class="sxs-lookup"><span data-stu-id="ff5bb-119">**Delay (bootTriggerType)**</span></span>](taskschedulerschema-delay-boottriggertype-element.md)                           | <span data-ttu-id="ff5bb-120">длительность</span><span class="sxs-lookup"><span data-stu-id="ff5bb-120">duration</span></span>                                                                 | <span data-ttu-id="ff5bb-121">Указывает промежуток времени между загрузкой системы и началом задачи.</span><span class="sxs-lookup"><span data-stu-id="ff5bb-121">Specifies the amount of time between when the system is booted and when the task is started.</span></span><br/>                            |
| [<span data-ttu-id="ff5bb-122">**Включено (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="ff5bb-122">**Enabled (triggerBaseType)**</span></span>](taskschedulerschema-enabled-triggerbasetype-element.md)                       | <span data-ttu-id="ff5bb-123">Логическое</span><span class="sxs-lookup"><span data-stu-id="ff5bb-123">boolean</span></span>                                                                  | <span data-ttu-id="ff5bb-124">Указывает, что триггер включен.</span><span class="sxs-lookup"><span data-stu-id="ff5bb-124">Specifies that the trigger is enabled.</span></span><br/>                                                                                  |
| [<span data-ttu-id="ff5bb-125">**Ендбаундари (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="ff5bb-125">**EndBoundary (triggerBaseType)**</span></span>](taskschedulerschema-endboundary-triggerbasetype-element.md)               | <span data-ttu-id="ff5bb-126">dateTime</span><span class="sxs-lookup"><span data-stu-id="ff5bb-126">dateTime</span></span>                                                                 | <span data-ttu-id="ff5bb-127">Указывает дату и время деактивации триггера.</span><span class="sxs-lookup"><span data-stu-id="ff5bb-127">Specifies the date and time when the trigger is deactivated.</span></span> <span data-ttu-id="ff5bb-128">Триггер не может запустить задачу после ее деактивации.</span><span class="sxs-lookup"><span data-stu-id="ff5bb-128">The trigger cannot start the task after it is deactivated.</span></span><br/> |
| [<span data-ttu-id="ff5bb-129">**Ексекутионтимелимит (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="ff5bb-129">**ExecutionTimeLimit (triggerBaseType)**</span></span>](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | <span data-ttu-id="ff5bb-130">длительность</span><span class="sxs-lookup"><span data-stu-id="ff5bb-130">duration</span></span>                                                                 | <span data-ttu-id="ff5bb-131">Указывает максимальное время, в течение которого задача может запускаться триггером.</span><span class="sxs-lookup"><span data-stu-id="ff5bb-131">Specifies the maximum amount of time in which the task can be started by the trigger.</span></span><br/>                                   |
| [<span data-ttu-id="ff5bb-132">**Повторение (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="ff5bb-132">**Repetition (triggerBaseType)**</span></span>](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [<span data-ttu-id="ff5bb-133">**репетитионтипе**</span><span class="sxs-lookup"><span data-stu-id="ff5bb-133">**repetitionType**</span></span>](taskschedulerschema-repetitiontype-complextype.md) | <span data-ttu-id="ff5bb-134">Указывает, как часто выполняется задача и как долго шаблон повторения повторяется после запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="ff5bb-134">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span><br/>          |
| [<span data-ttu-id="ff5bb-135">**Стартбаундари (Тригжербасетипе)**</span><span class="sxs-lookup"><span data-stu-id="ff5bb-135">**StartBoundary (triggerBaseType)**</span></span>](taskschedulerschema-startboundary-triggerbasetype-element.md)           | <span data-ttu-id="ff5bb-136">dateTime</span><span class="sxs-lookup"><span data-stu-id="ff5bb-136">dateTime</span></span>                                                                 | <span data-ttu-id="ff5bb-137">Указывает дату и время активации триггера.</span><span class="sxs-lookup"><span data-stu-id="ff5bb-137">Specifies the date and time when the trigger is activated.</span></span><br/>                                                              |



## <a name="attributes"></a><span data-ttu-id="ff5bb-138">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ff5bb-138">Attributes</span></span>



| <span data-ttu-id="ff5bb-139">Имя</span><span class="sxs-lookup"><span data-stu-id="ff5bb-139">Name</span></span> | <span data-ttu-id="ff5bb-140">Тип</span><span class="sxs-lookup"><span data-stu-id="ff5bb-140">Type</span></span>       | <span data-ttu-id="ff5bb-141">Описание</span><span class="sxs-lookup"><span data-stu-id="ff5bb-141">Description</span></span>                               |
|------|------------|-------------------------------------------|
| <span data-ttu-id="ff5bb-142">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="ff5bb-142">Id</span></span>   | <span data-ttu-id="ff5bb-143">**string**</span><span class="sxs-lookup"><span data-stu-id="ff5bb-143">**string**</span></span> | <span data-ttu-id="ff5bb-144">Идентификатор триггера.</span><span class="sxs-lookup"><span data-stu-id="ff5bb-144">The identifier of the trigger.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ff5bb-145">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ff5bb-145">Remarks</span></span>

<span data-ttu-id="ff5bb-146">Для разработки скриптов триггер загрузки определяется объектом [**буттригжер**](boottrigger.md) .</span><span class="sxs-lookup"><span data-stu-id="ff5bb-146">For script development, a boot trigger is defined by the [**BootTrigger**](boottrigger.md) object.</span></span>

<span data-ttu-id="ff5bb-147">Для разработки на C++ триггер загрузки определяется объектом [**ибуттригжер**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger) .</span><span class="sxs-lookup"><span data-stu-id="ff5bb-147">For C++ development, a boot trigger is defined by the [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger) object.</span></span>

## <a name="examples"></a><span data-ttu-id="ff5bb-148">Примеры</span><span class="sxs-lookup"><span data-stu-id="ff5bb-148">Examples</span></span>

<span data-ttu-id="ff5bb-149">Полный пример XML-кода для задачи, указывающей триггер загрузки, см. в разделе [Пример загрузочного триггера (XML)](boot-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="ff5bb-149">For a complete example of the XML for a task that specifies a boot trigger, see [Boot Trigger Example (XML)](boot-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ff5bb-150">Требования</span><span class="sxs-lookup"><span data-stu-id="ff5bb-150">Requirements</span></span>



| <span data-ttu-id="ff5bb-151">Требование</span><span class="sxs-lookup"><span data-stu-id="ff5bb-151">Requirement</span></span> | <span data-ttu-id="ff5bb-152">Значение</span><span class="sxs-lookup"><span data-stu-id="ff5bb-152">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ff5bb-153">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ff5bb-153">Minimum supported client</span></span><br/> | <span data-ttu-id="ff5bb-154">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ff5bb-154">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ff5bb-155">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ff5bb-155">Minimum supported server</span></span><br/> | <span data-ttu-id="ff5bb-156">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ff5bb-156">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ff5bb-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ff5bb-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff5bb-158">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="ff5bb-158">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="ff5bb-159">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="ff5bb-159">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





