---
title: Свойство Trigger. Type
description: Для сценариев Возвращает тип триггера.
ms.assetid: 346e6b02-c89e-4644-aa19-2bbf3d0fb3c3
keywords:
- Тип свойства планировщик задач
- Свойство Type планировщик задач, объект Trigger
- Планировщик задач объекта триггера, свойство Type
topic_type:
- apiref
api_name:
- Trigger.Type
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba2cef2d6ae33ceeac028e10a0f545afbc0a0ec8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801744"
---
# <a name="triggertype-property"></a><span data-ttu-id="d1c60-106">Свойство Trigger. Type</span><span class="sxs-lookup"><span data-stu-id="d1c60-106">Trigger.Type property</span></span>

<span data-ttu-id="d1c60-107">Для сценариев Возвращает тип триггера.</span><span class="sxs-lookup"><span data-stu-id="d1c60-107">For scripting, gets the type of the trigger.</span></span> <span data-ttu-id="d1c60-108">Тип триггера определяется при создании триггера и не может быть изменен позже.</span><span class="sxs-lookup"><span data-stu-id="d1c60-108">The trigger type is defined when the trigger is created and cannot be changed later.</span></span> <span data-ttu-id="d1c60-109">Сведения о создании триггера см. в разделе [**тригжерколлектион. Create**](triggercollection-create.md).</span><span class="sxs-lookup"><span data-stu-id="d1c60-109">For information on creating a trigger, see [**TriggerCollection.Create**](triggercollection-create.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d1c60-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d1c60-110">Syntax</span></span>


```VB
Trigger.Type As TASK_TRIGGER_TYPE2
```



## <a name="property-value"></a><span data-ttu-id="d1c60-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d1c60-111">Property value</span></span>

<span data-ttu-id="d1c60-112">Одно из следующих значений перечисления типа [**\_ \_ тип2 для триггера задачи**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) .</span><span class="sxs-lookup"><span data-stu-id="d1c60-112">One of the following [**TASK\_TRIGGER\_TYPE2**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) enumeration values.</span></span>



| <span data-ttu-id="d1c60-113">Значение</span><span class="sxs-lookup"><span data-stu-id="d1c60-113">Value</span></span>                                                                                                                                                                                                                                                                                | <span data-ttu-id="d1c60-114">Значение</span><span class="sxs-lookup"><span data-stu-id="d1c60-114">Meaning</span></span>                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="TASK_TRIGGER_EVENT"></span><span id="task_trigger_event"></span><dl> <span data-ttu-id="d1c60-115"><dt>**Задача \_ СРАБАТЫВАНИе \_ события**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d1c60-115"><dt>**TASK\_TRIGGER\_EVENT**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="d1c60-116">Запускает задачу при возникновении определенного события.</span><span class="sxs-lookup"><span data-stu-id="d1c60-116">Starts the task when a specific event occurs.</span></span><br/>              |
| <span id="TASK_TRIGGER_TIME"></span><span id="task_trigger_time"></span><dl> <span data-ttu-id="d1c60-117"><dt>**Задача \_ \_Время активации**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="d1c60-117"><dt>**TASK\_TRIGGER\_TIME**</dt> <dt>1</dt></span></span> </dl>                                                    | <span data-ttu-id="d1c60-118">Запускает задачу в определенное время суток.</span><span class="sxs-lookup"><span data-stu-id="d1c60-118">Starts the task at a specific time of day.</span></span><br/>                 |
| <span id="TASK_TRIGGER_DAILY"></span><span id="task_trigger_daily"></span><dl> <span data-ttu-id="d1c60-119"><dt>**Задача \_ ТРИГГЕР \_ ежедневно**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="d1c60-119"><dt>**TASK\_TRIGGER\_DAILY**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="d1c60-120">Запускает задачу ежедневно.</span><span class="sxs-lookup"><span data-stu-id="d1c60-120">Starts the task daily.</span></span><br/>                                     |
| <span id="TASK_TRIGGER_WEEKLY"></span><span id="task_trigger_weekly"></span><dl> <span data-ttu-id="d1c60-121"><dt>**Задача \_ ТРИГГЕР \_ еженедельно**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="d1c60-121"><dt>**TASK\_TRIGGER\_WEEKLY**</dt> <dt>3</dt></span></span> </dl>                                              | <span data-ttu-id="d1c60-122">Запускает задачу еженедельно.</span><span class="sxs-lookup"><span data-stu-id="d1c60-122">Starts the task weekly.</span></span><br/>                                    |
| <span id="TASK_TRIGGER_MONTHLY"></span><span id="task_trigger_monthly"></span><dl> <span data-ttu-id="d1c60-123"><dt>**Задача \_ ТРИГГЕР \_ ежемесячно**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="d1c60-123"><dt>**TASK\_TRIGGER\_MONTHLY**</dt> <dt>4</dt></span></span> </dl>                                           | <span data-ttu-id="d1c60-124">Запускает задачу ежемесячно.</span><span class="sxs-lookup"><span data-stu-id="d1c60-124">Starts the task monthly.</span></span><br/>                                   |
| <span id="TASK_TRIGGER_MONTHLYDOW"></span><span id="task_trigger_monthlydow"></span><dl> <span data-ttu-id="d1c60-125"><dt>**Задача \_ ТРИГГЕР \_ монслидов**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="d1c60-125"><dt>**TASK\_TRIGGER\_MONTHLYDOW**</dt> <dt>5</dt></span></span> </dl>                                  | <span data-ttu-id="d1c60-126">Запускает задачу каждый месяц в конкретный день недели.</span><span class="sxs-lookup"><span data-stu-id="d1c60-126">Starts the task every month on a specific day of the week.</span></span><br/> |
| <span id="TASK_TRIGGER_IDLE"></span><span id="task_trigger_idle"></span><dl> <span data-ttu-id="d1c60-127"><dt>**Задача \_ ЗАПУСТИТЬ \_ бездействующее**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="d1c60-127"><dt>**TASK\_TRIGGER\_IDLE**</dt> <dt>6</dt></span></span> </dl>                                                    | <span data-ttu-id="d1c60-128">Запускает задачу при переходе компьютера в состояние простоя.</span><span class="sxs-lookup"><span data-stu-id="d1c60-128">Starts the task when the computer goes into an idle state.</span></span><br/> |
| <span id="TASK_TRIGGER_REGISTRATION"></span><span id="task_trigger_registration"></span><dl> <span data-ttu-id="d1c60-129"><dt>**Задача \_ \_Регистрация триггера**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="d1c60-129"><dt>**TASK\_TRIGGER\_REGISTRATION**</dt> <dt>7</dt></span></span> </dl>                            | <span data-ttu-id="d1c60-130">Запускает задачу при регистрации задачи.</span><span class="sxs-lookup"><span data-stu-id="d1c60-130">Starts the task when the task is registered.</span></span><br/>               |
| <span id="TASK_TRIGGER_BOOT"></span><span id="task_trigger_boot"></span><dl> <span data-ttu-id="d1c60-131"><dt>**Задача \_ ЗАПУСК \_ загрузки**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="d1c60-131"><dt>**TASK\_TRIGGER\_BOOT**</dt> <dt>8</dt></span></span> </dl>                                                    | <span data-ttu-id="d1c60-132">Запускает задачу при загрузке компьютера.</span><span class="sxs-lookup"><span data-stu-id="d1c60-132">Starts the task when the computer boots.</span></span><br/>                   |
| <span id="TASK_TRIGGER_LOGON"></span><span id="task_trigger_logon"></span><dl> <span data-ttu-id="d1c60-133"><dt>**Задача \_ ЗАПУСК \_ входа**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="d1c60-133"><dt>**TASK\_TRIGGER\_LOGON**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="d1c60-134">Запускает задачу при входе определенного пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="d1c60-134">Starts the task when a specific user logs on.</span></span><br/>              |
| <span id="TASK_TRIGGER_SESSION_STATE_CHANGE"></span><span id="task_trigger_session_state_change"></span><dl> <span data-ttu-id="d1c60-135"><dt>**Задача \_ \_ \_ \_ Изменение состояния сеанса для триггера**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="d1c60-135"><dt>**TASK\_TRIGGER\_SESSION\_STATE\_CHANGE**</dt> <dt>11</dt></span></span> </dl> | <span data-ttu-id="d1c60-136">Активирует задачу при изменении определенного состояния сеанса.</span><span class="sxs-lookup"><span data-stu-id="d1c60-136">Triggers the task when a specific session state changes.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="d1c60-137">Требования</span><span class="sxs-lookup"><span data-stu-id="d1c60-137">Requirements</span></span>



| <span data-ttu-id="d1c60-138">Требование</span><span class="sxs-lookup"><span data-stu-id="d1c60-138">Requirement</span></span> | <span data-ttu-id="d1c60-139">Значение</span><span class="sxs-lookup"><span data-stu-id="d1c60-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1c60-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d1c60-140">Minimum supported client</span></span><br/> | <span data-ttu-id="d1c60-141">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d1c60-141">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d1c60-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d1c60-142">Minimum supported server</span></span><br/> | <span data-ttu-id="d1c60-143">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d1c60-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d1c60-144">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="d1c60-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="d1c60-145"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d1c60-145"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d1c60-146">DLL</span><span class="sxs-lookup"><span data-stu-id="d1c60-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1c60-147"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1c60-147"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1c60-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d1c60-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1c60-149">**Тригжерколлектион. Create**</span><span class="sxs-lookup"><span data-stu-id="d1c60-149">**TriggerCollection.Create**</span></span>](triggercollection-create.md)
</dt> <dt>

[<span data-ttu-id="d1c60-150">**\_Тип 2 триггера задачи \_**</span><span class="sxs-lookup"><span data-stu-id="d1c60-150">**TASK\_TRIGGER\_TYPE2**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2)
</dt> <dt>

[<span data-ttu-id="d1c60-151">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="d1c60-151">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





