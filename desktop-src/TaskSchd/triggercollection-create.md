---
title: Тригжерколлектион. Create, метод
description: Для создания скрипта создает новый триггер для задачи.
ms.assetid: 3d7dc811-0d83-475f-8a6e-87e59dae0113
keywords:
- триггеры планировщик задач, создание
- планировщик задач метода Create
- Создание планировщик задач метода, объект Тригжерколлектион
- Планировщик задач объекта Тригжерколлектион, метод Create
topic_type:
- apiref
api_name:
- TriggerCollection.Create
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad0f1c5dd8bef3d81a8e9b5859bc2bbd8c969bf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672583"
---
# <a name="triggercollectioncreate-method"></a><span data-ttu-id="cc6d1-107">Тригжерколлектион. Create, метод</span><span class="sxs-lookup"><span data-stu-id="cc6d1-107">TriggerCollection.Create method</span></span>

<span data-ttu-id="cc6d1-108">Для создания скрипта создает новый триггер для задачи.</span><span class="sxs-lookup"><span data-stu-id="cc6d1-108">For scripting, creates a new trigger for the task.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc6d1-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cc6d1-109">Syntax</span></span>


```VB
TriggerCollection.Create( _
  ByVal type _
)
```



## <a name="parameters"></a><span data-ttu-id="cc6d1-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="cc6d1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc6d1-111">*тип* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cc6d1-111">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc6d1-112">Для этого параметра задается одна из следующих констант перечисления типа [**\_ \_ 2 триггера задачи**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) .</span><span class="sxs-lookup"><span data-stu-id="cc6d1-112">This parameter is set to one of the following [**TASK\_TRIGGER\_TYPE2**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) enumeration constants.</span></span>



| <span data-ttu-id="cc6d1-113">Значение</span><span class="sxs-lookup"><span data-stu-id="cc6d1-113">Value</span></span>                                                                                                                                                                                                                                                                                | <span data-ttu-id="cc6d1-114">Значение</span><span class="sxs-lookup"><span data-stu-id="cc6d1-114">Meaning</span></span>                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_TRIGGER_EVENT"></span><span id="task_trigger_event"></span><dl> <span data-ttu-id="cc6d1-115"><dt>**Задача \_ СРАБАТЫВАНИе \_ события**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="cc6d1-115"><dt>**TASK\_TRIGGER\_EVENT**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="cc6d1-116">Активирует задачу при возникновении определенного события.</span><span class="sxs-lookup"><span data-stu-id="cc6d1-116">Triggers the task when a specific event occurs.</span></span><br/>                                                                                                               |
| <span id="TASK_TRIGGER_TIME"></span><span id="task_trigger_time"></span><dl> <span data-ttu-id="cc6d1-117"><dt>**Задача \_ \_Время активации**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="cc6d1-117"><dt>**TASK\_TRIGGER\_TIME**</dt> <dt>1</dt></span></span> </dl>                                                    | <span data-ttu-id="cc6d1-118">Запускает задачу в определенное время суток.</span><span class="sxs-lookup"><span data-stu-id="cc6d1-118">Triggers the task at a specific time of day.</span></span><br/>                                                                                                                  |
| <span id="TASK_TRIGGER_DAILY"></span><span id="task_trigger_daily"></span><dl> <span data-ttu-id="cc6d1-119"><dt>**Задача \_ ТРИГГЕР \_ ежедневно**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="cc6d1-119"><dt>**TASK\_TRIGGER\_DAILY**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="cc6d1-120">Запускает задачу ежедневно по расписанию.</span><span class="sxs-lookup"><span data-stu-id="cc6d1-120">Triggers the task on a daily schedule.</span></span> <span data-ttu-id="cc6d1-121">Например, задача начинается в определенное время каждый день, каждый второй день, каждый третий день и т. д.</span><span class="sxs-lookup"><span data-stu-id="cc6d1-121">For example, the task starts at a specific time every day, every-other day, every third day, and so on.</span></span><br/>                |
| <span id="TASK_TRIGGER_WEEKLY"></span><span id="task_trigger_weekly"></span><dl> <span data-ttu-id="cc6d1-122"><dt>**Задача \_ ТРИГГЕР \_ еженедельно**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="cc6d1-122"><dt>**TASK\_TRIGGER\_WEEKLY**</dt> <dt>3</dt></span></span> </dl>                                              | <span data-ttu-id="cc6d1-123">Запускает задачу по еженедельному расписанию.</span><span class="sxs-lookup"><span data-stu-id="cc6d1-123">Triggers the task on a weekly schedule.</span></span> <span data-ttu-id="cc6d1-124">Например, задача начинается в 8:00 в конкретный день каждую неделю или неделю.</span><span class="sxs-lookup"><span data-stu-id="cc6d1-124">For example, the task starts at 8:00 AM on a specific day every week or other week.</span></span><br/>                                   |
| <span id="TASK_TRIGGER_MONTHLY"></span><span id="task_trigger_monthly"></span><dl> <span data-ttu-id="cc6d1-125"><dt>**Задача \_ ТРИГГЕР \_ ежемесячно**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="cc6d1-125"><dt>**TASK\_TRIGGER\_MONTHLY**</dt> <dt>4</dt></span></span> </dl>                                           | <span data-ttu-id="cc6d1-126">Запускает задачу по месячному расписанию.</span><span class="sxs-lookup"><span data-stu-id="cc6d1-126">Triggers the task on a monthly schedule.</span></span> <span data-ttu-id="cc6d1-127">Например, задача запускается в определенные дни конкретного месяца.</span><span class="sxs-lookup"><span data-stu-id="cc6d1-127">For example, the task starts on specific days of specific months.</span></span><br/>                                                    |
| <span id="TASK_TRIGGER_MONTHLYDOW"></span><span id="task_trigger_monthlydow"></span><dl> <span data-ttu-id="cc6d1-128"><dt>**Задача \_ ТРИГГЕР \_ монслидов**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="cc6d1-128"><dt>**TASK\_TRIGGER\_MONTHLYDOW**</dt> <dt>5</dt></span></span> </dl>                                  | <span data-ttu-id="cc6d1-129">Запускает задачу в расписании ежемесячного дня недели.</span><span class="sxs-lookup"><span data-stu-id="cc6d1-129">Triggers the task on a monthly day-of-week schedule.</span></span> <span data-ttu-id="cc6d1-130">Например, задача запускается в определенные дни недели, недели месяца и месяцы года.</span><span class="sxs-lookup"><span data-stu-id="cc6d1-130">For example, the task starts on a specific days of the week, weeks of the month, and months of the year.</span></span><br/> |
| <span id="TASK_TRIGGER_IDLE"></span><span id="task_trigger_idle"></span><dl> <span data-ttu-id="cc6d1-131"><dt>**Задача \_ ЗАПУСТИТЬ \_ бездействующее**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="cc6d1-131"><dt>**TASK\_TRIGGER\_IDLE**</dt> <dt>6</dt></span></span> </dl>                                                    | <span data-ttu-id="cc6d1-132">Запускает задачу при переходе компьютера в состояние простоя.</span><span class="sxs-lookup"><span data-stu-id="cc6d1-132">Triggers the task when the computer goes into an idle state.</span></span><br/>                                                                                                  |
| <span id="TASK_TRIGGER_REGISTRATION"></span><span id="task_trigger_registration"></span><dl> <span data-ttu-id="cc6d1-133"><dt>**Задача \_ \_Регистрация триггера**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="cc6d1-133"><dt>**TASK\_TRIGGER\_REGISTRATION**</dt> <dt>7</dt></span></span> </dl>                            | <span data-ttu-id="cc6d1-134">Активирует задачу при регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="cc6d1-134">Triggers the task when the task is registered.</span></span><br/>                                                                                                                |
| <span id="TASK_TRIGGER_BOOT"></span><span id="task_trigger_boot"></span><dl> <span data-ttu-id="cc6d1-135"><dt>**Задача \_ ЗАПУСК \_ загрузки**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="cc6d1-135"><dt>**TASK\_TRIGGER\_BOOT**</dt> <dt>8</dt></span></span> </dl>                                                    | <span data-ttu-id="cc6d1-136">Запускает задачу при загрузке компьютера.</span><span class="sxs-lookup"><span data-stu-id="cc6d1-136">Triggers the task when the computer boots.</span></span><br/>                                                                                                                    |
| <span id="TASK_TRIGGER_LOGON"></span><span id="task_trigger_logon"></span><dl> <span data-ttu-id="cc6d1-137"><dt>**Задача \_ ЗАПУСК \_ входа**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="cc6d1-137"><dt>**TASK\_TRIGGER\_LOGON**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="cc6d1-138">Запускает задачу при входе определенного пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="cc6d1-138">Triggers the task when a specific user logs on.</span></span><br/>                                                                                                               |
| <span id="TASK_TRIGGER_SESSION_STATE_CHANGE"></span><span id="task_trigger_session_state_change"></span><dl> <span data-ttu-id="cc6d1-139"><dt>**Задача \_ \_ \_ \_ Изменение состояния сеанса для триггера**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="cc6d1-139"><dt>**TASK\_TRIGGER\_SESSION\_STATE\_CHANGE**</dt> <dt>11</dt></span></span> </dl> | <span data-ttu-id="cc6d1-140">Активирует задачу при изменении определенного состояния сеанса.</span><span class="sxs-lookup"><span data-stu-id="cc6d1-140">Triggers the task when a specific session state changes.</span></span><br/>                                                                                                      |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc6d1-141">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cc6d1-141">Return value</span></span>

<span data-ttu-id="cc6d1-142">Объект [**триггера**](trigger.md) , представляющий новый триггер.</span><span class="sxs-lookup"><span data-stu-id="cc6d1-142">A [**Trigger**](trigger.md) object that represents the new trigger.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc6d1-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cc6d1-143">Remarks</span></span>

<span data-ttu-id="cc6d1-144">Сведения о каждом типе триггера см. в разделе [типы триггеров](trigger-types.md).</span><span class="sxs-lookup"><span data-stu-id="cc6d1-144">For information about each trigger type see [Trigger Types](trigger-types.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cc6d1-145">Требования</span><span class="sxs-lookup"><span data-stu-id="cc6d1-145">Requirements</span></span>



| <span data-ttu-id="cc6d1-146">Требование</span><span class="sxs-lookup"><span data-stu-id="cc6d1-146">Requirement</span></span> | <span data-ttu-id="cc6d1-147">Значение</span><span class="sxs-lookup"><span data-stu-id="cc6d1-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc6d1-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cc6d1-148">Minimum supported client</span></span><br/> | <span data-ttu-id="cc6d1-149">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cc6d1-149">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="cc6d1-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cc6d1-150">Minimum supported server</span></span><br/> | <span data-ttu-id="cc6d1-151">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cc6d1-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cc6d1-152">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="cc6d1-152">Type library</span></span><br/>             | <dl> <span data-ttu-id="cc6d1-153"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="cc6d1-153"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="cc6d1-154">DLL</span><span class="sxs-lookup"><span data-stu-id="cc6d1-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc6d1-155"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc6d1-155"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc6d1-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cc6d1-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc6d1-157">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="cc6d1-157">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="cc6d1-158">**Необходимость**</span><span class="sxs-lookup"><span data-stu-id="cc6d1-158">**Trigger**</span></span>](trigger.md)
</dt> </dl>

 

 





