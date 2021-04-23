---
title: Элемент повторения (Тригжербасетипе)
description: Указывает, как часто выполняется задача и как долго шаблон повторения повторяется после запуска задачи.
ms.assetid: d43c7f9a-3a7b-44a9-901b-9ad18c027b1b
keywords:
- Элемент повторения планировщик задач
topic_type:
- apiref
api_name:
- Repetition
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7ebd6f9f77998e5e975e24ff752a475e3880c0aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491670"
---
# <a name="repetition-triggerbasetype-element"></a><span data-ttu-id="4603f-104">Элемент повторения (Тригжербасетипе)</span><span class="sxs-lookup"><span data-stu-id="4603f-104">Repetition (triggerBaseType) Element</span></span>

<span data-ttu-id="4603f-105">Указывает, как часто выполняется задача и как долго шаблон повторения повторяется после запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="4603f-105">Specifies how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span>

``` syntax
<xs:element name="Repetition"
    type="repetitionType"
 />
```

<span data-ttu-id="4603f-106">Элемент **повторения** определяется сложным типом [**тригжербасетипе**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="4603f-106">The **Repetition** element is defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="4603f-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="4603f-107">Parent element</span></span>



| <span data-ttu-id="4603f-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="4603f-108">Element</span></span>                                                                                     | <span data-ttu-id="4603f-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="4603f-109">Derived from</span></span>                                                                               | <span data-ttu-id="4603f-110">Описание</span><span class="sxs-lookup"><span data-stu-id="4603f-110">Description</span></span>                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4603f-111">**буттригжер**</span><span class="sxs-lookup"><span data-stu-id="4603f-111">**BootTrigger**</span></span>](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [<span data-ttu-id="4603f-112">**буттригжертипе**</span><span class="sxs-lookup"><span data-stu-id="4603f-112">**bootTriggerType**</span></span>](taskschedulerschema-boottriggertype-complextype.md)                 | <span data-ttu-id="4603f-113">Указывает триггер, который запускает задачу при загрузке системы.</span><span class="sxs-lookup"><span data-stu-id="4603f-113">Specifies a trigger that starts a task when the system is booted.</span></span><br/>                 |
| [<span data-ttu-id="4603f-114">**календартригжер**</span><span class="sxs-lookup"><span data-stu-id="4603f-114">**CalendarTrigger**</span></span>](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [<span data-ttu-id="4603f-115">**календартригжертипе**</span><span class="sxs-lookup"><span data-stu-id="4603f-115">**calendarTriggerType**</span></span>](taskschedulerschema-calendartriggertype-complextype.md)         | <span data-ttu-id="4603f-116">Задает ежедневный, еженедельный, ежемесячный или ежемесячный триггер (DOW) в день недели.</span><span class="sxs-lookup"><span data-stu-id="4603f-116">Specifies a daily, weekly, monthly, or a monthly day-of-the-week (DOW) trigger.</span></span><br/>   |
| [<span data-ttu-id="4603f-117">**EventTrigger**</span><span class="sxs-lookup"><span data-stu-id="4603f-117">**EventTrigger**</span></span>](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [<span data-ttu-id="4603f-118">**евенттригжертипе**</span><span class="sxs-lookup"><span data-stu-id="4603f-118">**eventTriggerType**</span></span>](taskschedulerschema-eventtriggertype-complextype.md)               | <span data-ttu-id="4603f-119">Указывает триггер, который запускает задачу при возникновении системного события.</span><span class="sxs-lookup"><span data-stu-id="4603f-119">Specifies a trigger that starts a task when a system event occurs.</span></span><br/>                |
| [<span data-ttu-id="4603f-120">**идлетригжер**</span><span class="sxs-lookup"><span data-stu-id="4603f-120">**IdleTrigger**</span></span>](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [<span data-ttu-id="4603f-121">**идлетригжертипе**</span><span class="sxs-lookup"><span data-stu-id="4603f-121">**idleTriggerType**</span></span>](taskschedulerschema-idletriggertype-complextype.md)                 | <span data-ttu-id="4603f-122">Указывает триггер, который запускает задачу при переходе компьютера в состояние простоя.</span><span class="sxs-lookup"><span data-stu-id="4603f-122">Specifies a trigger that starts a task when the computer goes into an idle state.</span></span><br/> |
| [<span data-ttu-id="4603f-123">**логонтригжер**</span><span class="sxs-lookup"><span data-stu-id="4603f-123">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md)               | [<span data-ttu-id="4603f-124">**логонтригжертипе**</span><span class="sxs-lookup"><span data-stu-id="4603f-124">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md)               | <span data-ttu-id="4603f-125">Указывает триггер, который запускает задачу при входе пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="4603f-125">Specifies a trigger that starts a task when a user logs on.</span></span><br/>                       |
| [<span data-ttu-id="4603f-126">**регистратионтригжер**</span><span class="sxs-lookup"><span data-stu-id="4603f-126">**RegistrationTrigger**</span></span>](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [<span data-ttu-id="4603f-127">**регистратионтригжертипе**</span><span class="sxs-lookup"><span data-stu-id="4603f-127">**registrationTriggerType**</span></span>](taskschedulerschema-registrationtriggertype-complextype.md) | <span data-ttu-id="4603f-128">Указывает триггер, который запускает задачу при регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="4603f-128">Specifies a trigger that starts a task when the task is registered.</span></span><br/>               |
| [<span data-ttu-id="4603f-129">**TimeTrigger**</span><span class="sxs-lookup"><span data-stu-id="4603f-129">**TimeTrigger**</span></span>](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [<span data-ttu-id="4603f-130">**тиметригжертипе**</span><span class="sxs-lookup"><span data-stu-id="4603f-130">**timeTriggerType**</span></span>](taskschedulerschema-timetriggertype-complextype.md)                 | <span data-ttu-id="4603f-131">Указывает триггер, который запускает задачу при активации триггера.</span><span class="sxs-lookup"><span data-stu-id="4603f-131">Specifies a trigger that starts a task when the trigger is activated.</span></span><br/>             |



## <a name="child-elements"></a><span data-ttu-id="4603f-132">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="4603f-132">Child elements</span></span>



| <span data-ttu-id="4603f-133">Элемент</span><span class="sxs-lookup"><span data-stu-id="4603f-133">Element</span></span>                                                                                   | <span data-ttu-id="4603f-134">Тип</span><span class="sxs-lookup"><span data-stu-id="4603f-134">Type</span></span>     | <span data-ttu-id="4603f-135">Описание</span><span class="sxs-lookup"><span data-stu-id="4603f-135">Description</span></span>                                                                                                         |
|-------------------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4603f-136">**Длитель**</span><span class="sxs-lookup"><span data-stu-id="4603f-136">**Duration**</span></span>](taskschedulerschema-duration-repetitiontype-element.md)                   | <span data-ttu-id="4603f-137">длительность</span><span class="sxs-lookup"><span data-stu-id="4603f-137">duration</span></span> | <span data-ttu-id="4603f-138">Указывает, как долго шаблон повторяется.</span><span class="sxs-lookup"><span data-stu-id="4603f-138">Specifies how long the pattern is repeated.</span></span><br/>                                                              |
| [<span data-ttu-id="4603f-139">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="4603f-139">**Interval**</span></span>](taskschedulerschema-interval-repetitiontype-element.md)                   | <span data-ttu-id="4603f-140">длительность</span><span class="sxs-lookup"><span data-stu-id="4603f-140">duration</span></span> | <span data-ttu-id="4603f-141">Задает интервал времени между перезапусками задачи.</span><span class="sxs-lookup"><span data-stu-id="4603f-141">Specifies the amount of time between each restart of the task.</span></span><br/>                                           |
| [<span data-ttu-id="4603f-142">**стопатдуратионенд**</span><span class="sxs-lookup"><span data-stu-id="4603f-142">**StopAtDurationEnd**</span></span>](taskschedulerschema-stopatdurationend-repetitiontype-element.md) | <span data-ttu-id="4603f-143">Логическое</span><span class="sxs-lookup"><span data-stu-id="4603f-143">boolean</span></span>  | <span data-ttu-id="4603f-144">Указывает, что выполняющиеся экземпляры задачи останавливаются в конце шаблона повторения.</span><span class="sxs-lookup"><span data-stu-id="4603f-144">Specifies that a running instances of the task is stopped at the end of the repetition pattern duration.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="4603f-145">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4603f-145">Remarks</span></span>

<span data-ttu-id="4603f-146">Если для задачи задана длительность повторения, необходимо также указать интервал повторения.</span><span class="sxs-lookup"><span data-stu-id="4603f-146">If you specify a repetition duration for a task, you must also specify the repetition interval.</span></span>

<span data-ttu-id="4603f-147">Если зарегистрировать задачу, содержащую триггер с интервалом повтора, равный одной минуте, а длительность повторения — четыре минуты, задача будет запущена пять раз.</span><span class="sxs-lookup"><span data-stu-id="4603f-147">If you register a task that contains a trigger with a repetition interval equal to one minute and a repetition duration equal to four minutes, the task will be launched five times.</span></span> <span data-ttu-id="4603f-148">Пять повторений можно определить в следующем шаблоне.</span><span class="sxs-lookup"><span data-stu-id="4603f-148">The five repetitions can be defined by the following pattern.</span></span>

1.  <span data-ttu-id="4603f-149">Задача начинается в начале первой минуты.</span><span class="sxs-lookup"><span data-stu-id="4603f-149">A task starts at the beginning of the first minute.</span></span>
2.  <span data-ttu-id="4603f-150">Следующая задача начинается в конце первой минуты.</span><span class="sxs-lookup"><span data-stu-id="4603f-150">The next task starts at the end of the first minute.</span></span>
3.  <span data-ttu-id="4603f-151">Следующая задача начинается в конце второй минуты.</span><span class="sxs-lookup"><span data-stu-id="4603f-151">The next task starts at the end of the second minute.</span></span>
4.  <span data-ttu-id="4603f-152">Следующая задача начинается в конце третьей минуты.</span><span class="sxs-lookup"><span data-stu-id="4603f-152">The next task starts at the end of the third minute.</span></span>
5.  <span data-ttu-id="4603f-153">Следующая задача начинается в конце четвертой минуты.</span><span class="sxs-lookup"><span data-stu-id="4603f-153">The next task starts at the end of the fourth minute.</span></span>

<span data-ttu-id="4603f-154">**Windows Server 2003, Windows XP и windows 2000:** Если зарегистрировать задачу, содержащую триггер с интервалом повтора, равный одной минуте, а длительность повторения — четыре минуты, задача будет запущена четыре раза.</span><span class="sxs-lookup"><span data-stu-id="4603f-154">**Windows Server 2003, Windows XP and Windows 2000:** If you register a task that contains a trigger with a repetition interval equal to one minute and a repetition duration equal to four minutes, the task will be launched four times.</span></span>

<span data-ttu-id="4603f-155">**Windows Vista, Windows 7, Windows server 2008, Windows 8 и Windows server 2012:** Как правило, Задание длительности повтора до точно кратного интервала приводит к получению чисел, описанных выше.</span><span class="sxs-lookup"><span data-stu-id="4603f-155">**Windows Vista, Windows 7, Windows Server 2008, Windows 8 and Windows Server 2012:** Usually, setting the repetition duration to an exact multiple of the interval yields the numbers described above.</span></span> <span data-ttu-id="4603f-156">Однако при определенных условиях высокой нагрузки время ожидания истекло до того, как TaskScheduler может запустить конечный интервал задачи.</span><span class="sxs-lookup"><span data-stu-id="4603f-156">However, under certain heavy load conditions, it is possible for the duration to timeout before TaskScheduler can launch the final task interval.</span></span>

<span data-ttu-id="4603f-157">Для разработки сценариев шаблон повторения указывается с помощью свойства [**Trigger. повторения**](trigger-repetition.md) , наследуемого всеми объектами триггера.</span><span class="sxs-lookup"><span data-stu-id="4603f-157">For scripting development, the repetition pattern is specified using the [**Trigger.Repetition**](trigger-repetition.md) property that is inherited by all the trigger objects.</span></span>

<span data-ttu-id="4603f-158">Для разработки на C++ шаблон повторения указывается с помощью свойства [**итригжер:: повторение**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_repetition) , которое наследуется всеми интерфейсами триггера.</span><span class="sxs-lookup"><span data-stu-id="4603f-158">For C++ development, the repetition pattern is specified using the [**ITRigger::Repetition**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_repetition) property that is inherited by all the trigger interfaces.</span></span>

## <a name="examples"></a><span data-ttu-id="4603f-159">Примеры</span><span class="sxs-lookup"><span data-stu-id="4603f-159">Examples</span></span>

<span data-ttu-id="4603f-160">Следующий XML-код определяет элемент триггера загрузки, который указывает шаблон повторения для триггера.</span><span class="sxs-lookup"><span data-stu-id="4603f-160">The following XML defines a boot trigger element that specifies a repetition pattern for a trigger.</span></span>


```XML
<BootTrigger>
    <StartBoundary>2005-01-01T08:00:00</StartBoundary>
    <EndBounadry>2007-01-01T08:00:00</EndBoundary>
    <Enabled>true</Enabled>
    <Repetition>
        <Interval></Interval>
        <Duration></Duration>
        <StopAtDurationEnd>true</StopAtDirationEnd>
    </Repetition>
    <ExecutionTimeLimit></ExecutionTimeLimit>
    <Delay><Delay>
 </BootTrigger>
```



## <a name="requirements"></a><span data-ttu-id="4603f-161">Требования</span><span class="sxs-lookup"><span data-stu-id="4603f-161">Requirements</span></span>



| <span data-ttu-id="4603f-162">Требование</span><span class="sxs-lookup"><span data-stu-id="4603f-162">Requirement</span></span> | <span data-ttu-id="4603f-163">Значение</span><span class="sxs-lookup"><span data-stu-id="4603f-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4603f-164">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4603f-164">Minimum supported client</span></span><br/> | <span data-ttu-id="4603f-165">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4603f-165">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4603f-166">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4603f-166">Minimum supported server</span></span><br/> | <span data-ttu-id="4603f-167">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4603f-167">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4603f-168">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4603f-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4603f-169">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="4603f-169">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="4603f-170">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="4603f-170">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





