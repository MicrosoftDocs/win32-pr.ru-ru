---
title: Объект Репетитионпаттерн
description: Объект скрипта, который определяет, как часто выполняется задача и как долго шаблон повторения повторяется после запуска задачи.
ms.assetid: a4e63da7-78ab-46a9-9b55-8460355753cf
keywords:
- триггеры планировщик задач, объект шаблона повторения
- шаблон повторения планировщик задач, объект
- планировщик задач объекта Репетитионпаттерн
- Планировщик задач объекта Репетитионпаттерн, описание
topic_type:
- apiref
api_name:
- RepetitionPattern
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84b88588238c9a7e4158fe21bca8904bf6f39b51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489867"
---
# <a name="repetitionpattern-object"></a><span data-ttu-id="d633b-107">Объект Репетитионпаттерн</span><span class="sxs-lookup"><span data-stu-id="d633b-107">RepetitionPattern object</span></span>

<span data-ttu-id="d633b-108">Объект скрипта, который определяет, как часто выполняется задача и как долго шаблон повторения повторяется после запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="d633b-108">Scripting object that defines how often the task is run and how long the repetition pattern is repeated after the task is started.</span></span>

## <a name="members"></a><span data-ttu-id="d633b-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="d633b-109">Members</span></span>

<span data-ttu-id="d633b-110">Объект **репетитионпаттерн** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d633b-110">The **RepetitionPattern** object has these types of members:</span></span>

-   [<span data-ttu-id="d633b-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="d633b-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d633b-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="d633b-112">Properties</span></span>

<span data-ttu-id="d633b-113">Объект **репетитионпаттерн** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d633b-113">The **RepetitionPattern** object has these properties.</span></span>



| <span data-ttu-id="d633b-114">Свойство</span><span class="sxs-lookup"><span data-stu-id="d633b-114">Property</span></span>                                                                    | <span data-ttu-id="d633b-115">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="d633b-115">Access type</span></span>           | <span data-ttu-id="d633b-116">Описание</span><span class="sxs-lookup"><span data-stu-id="d633b-116">Description</span></span>                                                                                                                                        |
|:----------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d633b-117">**Длительность**</span><span class="sxs-lookup"><span data-stu-id="d633b-117">**Duration**</span></span>](repetitionpattern-duration.md)<br/>                   | <span data-ttu-id="d633b-118">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="d633b-118">Read/write</span></span><br/> | <span data-ttu-id="d633b-119">Возвращает или задает время, в течение которого шаблон повторяется.</span><span class="sxs-lookup"><span data-stu-id="d633b-119">Gets or sets how long the pattern is repeated.</span></span><br/>                                                                                          |
| [<span data-ttu-id="d633b-120">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="d633b-120">**Interval**</span></span>](repetitionpattern-interval.md)<br/>                   | <span data-ttu-id="d633b-121">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="d633b-121">Read/write</span></span><br/> | <span data-ttu-id="d633b-122">Возвращает или задает интервал времени между перезапусками задачи.</span><span class="sxs-lookup"><span data-stu-id="d633b-122">Gets or sets the amount of time between each restart of the task.</span></span><br/>                                                                       |
| [<span data-ttu-id="d633b-123">**стопатдуратионенд**</span><span class="sxs-lookup"><span data-stu-id="d633b-123">**StopAtDurationEnd**</span></span>](repetitionpattern-stopatdurationend.md)<br/> | <span data-ttu-id="d633b-124">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="d633b-124">Read/write</span></span><br/> | <span data-ttu-id="d633b-125">Возвращает или задает логическое значение, указывающее, останавливается ли работающий экземпляр задачи в конце шаблона повторения.</span><span class="sxs-lookup"><span data-stu-id="d633b-125">Gets or sets a Boolean value that indicates if a running instance of the task is stopped at the end of the repetition pattern duration.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d633b-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d633b-126">Remarks</span></span>

<span data-ttu-id="d633b-127">Если для задачи задана длительность повторения, необходимо также указать интервал повторения.</span><span class="sxs-lookup"><span data-stu-id="d633b-127">If you specify a repetition duration for a task, you must also specify the repetition interval.</span></span>

<span data-ttu-id="d633b-128">Если зарегистрировать задачу, содержащую триггер с интервалом повтора, равный одной минуте, а длительность повторения — четыре минуты, задача будет запущена пять раз.</span><span class="sxs-lookup"><span data-stu-id="d633b-128">If you register a task that contains a trigger with a repetition interval equal to one minute and a repetition duration equal to four minutes, the task will be launched five times.</span></span> <span data-ttu-id="d633b-129">Пять повторений можно определить в следующем шаблоне.</span><span class="sxs-lookup"><span data-stu-id="d633b-129">The five repetitions can be defined by the following pattern.</span></span>

1.  <span data-ttu-id="d633b-130">Задача начинается в начале первой минуты.</span><span class="sxs-lookup"><span data-stu-id="d633b-130">A task starts at the beginning of the first minute.</span></span>
2.  <span data-ttu-id="d633b-131">Следующая задача начинается в конце первой минуты.</span><span class="sxs-lookup"><span data-stu-id="d633b-131">The next task starts at the end of the first minute.</span></span>
3.  <span data-ttu-id="d633b-132">Следующая задача начинается в конце второй минуты.</span><span class="sxs-lookup"><span data-stu-id="d633b-132">The next task starts at the end of the second minute.</span></span>
4.  <span data-ttu-id="d633b-133">Следующая задача начинается в конце третьей минуты.</span><span class="sxs-lookup"><span data-stu-id="d633b-133">The next task starts at the end of the third minute.</span></span>
5.  <span data-ttu-id="d633b-134">Следующая задача начинается в конце четвертой минуты.</span><span class="sxs-lookup"><span data-stu-id="d633b-134">The next task starts at the end of the fourth minute.</span></span>

<span data-ttu-id="d633b-135">**Windows Server 2003, Windows XP и windows 2000:** Если зарегистрировать задачу, содержащую триггер с интервалом повтора, равный одной минуте, а длительность повторения — четыре минуты, задача будет запущена четыре раза.</span><span class="sxs-lookup"><span data-stu-id="d633b-135">**Windows Server 2003, Windows XP and Windows 2000:** If you register a task that contains a trigger with a repetition interval equal to one minute and a repetition duration equal to four minutes, the task will be launched four times.</span></span>

<span data-ttu-id="d633b-136">При чтении или записи XML для задачи шаблон повторения указывается с помощью элемента [**повторения**](taskschedulerschema-repetition-triggerbasetype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="d633b-136">When reading or writing XML for a task, the repetition pattern is specified using the [**Repetition**](taskschedulerschema-repetition-triggerbasetype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="d633b-137">Примеры</span><span class="sxs-lookup"><span data-stu-id="d633b-137">Examples</span></span>

<span data-ttu-id="d633b-138">Дополнительные сведения и примеры кода для этого свойства см. в разделе [Пример ежедневного триггера (сценарии)](daily-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="d633b-138">For more information and example code for this property, see [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d633b-139">Требования</span><span class="sxs-lookup"><span data-stu-id="d633b-139">Requirements</span></span>



| <span data-ttu-id="d633b-140">Требование</span><span class="sxs-lookup"><span data-stu-id="d633b-140">Requirement</span></span> | <span data-ttu-id="d633b-141">Значение</span><span class="sxs-lookup"><span data-stu-id="d633b-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d633b-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d633b-142">Minimum supported client</span></span><br/> | <span data-ttu-id="d633b-143">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d633b-143">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d633b-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d633b-144">Minimum supported server</span></span><br/> | <span data-ttu-id="d633b-145">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d633b-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d633b-146">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="d633b-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="d633b-147"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d633b-147"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d633b-148">DLL</span><span class="sxs-lookup"><span data-stu-id="d633b-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d633b-149"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d633b-149"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d633b-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d633b-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d633b-151">планировщик задач объекты</span><span class="sxs-lookup"><span data-stu-id="d633b-151">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="d633b-152">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="d633b-152">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





