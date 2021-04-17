---
title: Константы планировщик задач и ошибки успеха (WinError. h)
description: При возникновении ошибки API-интерфейсы планировщик задач могут возвращать один из следующих кодов ошибок как значение HRESULT.
ms.assetid: 54278bbd-7dca-438e-a771-5fcb08c4aa68
keywords:
- Планировщик задач планировщик задач, ссылки, ошибки и константы успеха
topic_type:
- apiref
api_name:
- SCHED_S_TASK_READY
- SCHED_S_TASK_RUNNING
- SCHED_S_TASK_DISABLED
- SCHED_S_TASK_HAS_NOT_RUN
- SCHED_S_TASK_NO_MORE_RUNS
- SCHED_S_TASK_NOT_SCHEDULED
- SCHED_S_TASK_TERMINATED
- SCHED_S_TASK_NO_VALID_TRIGGERS
- SCHED_S_EVENT_TRIGGER
- SCHED_E_TRIGGER_NOT_FOUND
- SCHED_E_TASK_NOT_READY
- SCHED_E_TASK_NOT_RUNNING
- SCHED_E_SERVICE_NOT_INSTALLED
- SCHED_E_CANNOT_OPEN_TASK
- SCHED_E_INVALID_TASK
- SCHED_E_ACCOUNT_INFORMATION_NOT_SET
- SCHED_E_ACCOUNT_NAME_NOT_FOUND
- SCHED_E_ACCOUNT_DBASE_CORRUPT
- SCHED_E_NO_SECURITY_SERVICES
- SCHED_E_UNKNOWN_OBJECT_VERSION
- SCHED_E_UNSUPPORTED_ACCOUNT_OPTION
- SCHED_E_SERVICE_NOT_RUNNING
- SCHED_E_UNEXPECTEDNODE
- SCHED_E_NAMESPACE
- SCHED_E_INVALIDVALUE
- SCHED_E_MISSINGNODE
- SCHED_E_MALFORMEDXML
- SCHED_S_SOME_TRIGGERS_FAILED
- SCHED_S_BATCH_LOGON_PROBLEM
- SCHED_E_TOO_MANY_NODES
- SCHED_E_PAST_END_BOUNDARY
- SCHED_E_ALREADY_RUNNING
- SCHED_E_USER_NOT_LOGGED_ON
- SCHED_E_INVALID_TASK_HASH
- SCHED_E_SERVICE_NOT_AVAILABLE
- SCHED_E_SERVICE_TOO_BUSY
- SCHED_E_TASK_ATTEMPTED
- SCHED_S_TASK_QUEUED
- SCHED_E_TASK_DISABLED
- SCHED_E_TASK_NOT_V1_COMPAT
- SCHED_E_START_ON_DEMAND
api_location:
- WinError.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: a1d0347938020ca8937f2764e3b2c62a38fc9273
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674965"
---
# <a name="task-scheduler-error-and-success-constants"></a><span data-ttu-id="4e490-104">планировщик задач константы ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="4e490-104">Task Scheduler Error and Success Constants</span></span>

<span data-ttu-id="4e490-105">При возникновении ошибки API-интерфейсы планировщик задач могут возвращать один из следующих кодов ошибок как значение **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4e490-105">If an error occurs, the Task Scheduler APIs can return one of the following error codes as an **HRESULT** value.</span></span>

<span data-ttu-id="4e490-106">Константы, начинающиеся с SCHED \_ S, \_ являются константами успеха, а константы, которые начинаются с sched \_ E \_ , являются константами ошибок.</span><span class="sxs-lookup"><span data-stu-id="4e490-106">The constants that begin with SCHED\_S\_ are success constants, and the constants that begin with SCHED\_E\_ are error constants.</span></span>

```cpp
  HRESULT phrStatus;
  hr = pITask->GetStatus(&phrStatus);
  
  // Release the ITask interface.
  pITask->Release();
    
  switch(phrStatus)
  {
  case SCHED_S_TASK_READY:
       wprintf(L"  SCHED_S_TASK_READY\n");
       break;
  case SCHED_S_TASK_RUNNING:
       wprintf(L"  SCHED_S_TASK_RUNNING\n");
       break;

  //...
  }
```

<span data-ttu-id="4e490-107">Пример [кода C/C++: получение состояния задачи](c-c-code-example-retrieving-task-status.md).</span><span class="sxs-lookup"><span data-stu-id="4e490-107">Example from [C/C++ Code Example: Retrieving Task Status](c-c-code-example-retrieving-task-status.md).</span></span>

> [!Note]  
> <span data-ttu-id="4e490-108">Некоторые планировщик задач API могут возвращать системные и сетевые коды ошибок (например, 64).</span><span class="sxs-lookup"><span data-stu-id="4e490-108">Some Task Scheduler APIs can return system and network error codes (64 for example).</span></span> <span data-ttu-id="4e490-109">Определение этих типов кодов ошибок можно проверить с помощью команды **net helpmsg** в окне командной строки.</span><span class="sxs-lookup"><span data-stu-id="4e490-109">You can check the definition of these types of error codes by using the **net helpmsg** command in the command prompt window.</span></span> <span data-ttu-id="4e490-110">Например, команда **net helpmsg 64** возвращает сообщение: указанное сетевое имя больше недоступно.</span><span class="sxs-lookup"><span data-stu-id="4e490-110">For example, the command **net helpmsg 64** returns the message: The specified network name is no longer available.</span></span>

 

<span data-ttu-id="4e490-111">Дополнительные сведения о событиях и сообщениях об ошибках см. в разделе [события и ошибки в центре сообщений](https://www.microsoft.com/technet/support/ee/ee_advanced.aspx).</span><span class="sxs-lookup"><span data-stu-id="4e490-111">For more information about events and error messages, see [Events and Errors Message Center](https://www.microsoft.com/technet/support/ee/ee_advanced.aspx).</span></span>

<dl> <dt>

<span data-ttu-id="4e490-112"><span id="SCHED_S_TASK_READY"></span><span id="sched_s_task_ready"></span>**Задача "SCHED \_ S" \_ \_ готова**</span><span class="sxs-lookup"><span data-stu-id="4e490-112"><span id="SCHED_S_TASK_READY"></span><span id="sched_s_task_ready"></span>**SCHED\_S\_TASK\_READY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e490-113">0x00041300</span><span class="sxs-lookup"><span data-stu-id="4e490-113">0x00041300</span></span>
</dt> <dt>



<span data-ttu-id="4e490-114">Задача готова к выполнению в следующее запланированное время.</span><span class="sxs-lookup"><span data-stu-id="4e490-114">The task is ready to run at its next scheduled time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e490-115"><span id="SCHED_S_TASK_RUNNING"></span><span id="sched_s_task_running"></span>**\_ \_ выполнение задачи "запланировать S" \_**</span><span class="sxs-lookup"><span data-stu-id="4e490-115"><span id="SCHED_S_TASK_RUNNING"></span><span id="sched_s_task_running"></span>**SCHED\_S\_TASK\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e490-116">0x00041301</span><span class="sxs-lookup"><span data-stu-id="4e490-116">0x00041301</span></span>
</dt> <dt>



<span data-ttu-id="4e490-117">Задача выполняется в данный момент.</span><span class="sxs-lookup"><span data-stu-id="4e490-117">The task is currently running.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e490-118"><span id="SCHED_S_TASK_DISABLED"></span><span id="sched_s_task_disabled"></span>**Задача "SCHED \_ S" \_ \_ отключена**</span><span class="sxs-lookup"><span data-stu-id="4e490-118"><span id="SCHED_S_TASK_DISABLED"></span><span id="sched_s_task_disabled"></span>**SCHED\_S\_TASK\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e490-119">0x00041302</span><span class="sxs-lookup"><span data-stu-id="4e490-119">0x00041302</span></span>
</dt> <dt>



<span data-ttu-id="4e490-120">Задача не будет выполняться в запланированное время, так как она была отключена.</span><span class="sxs-lookup"><span data-stu-id="4e490-120">The task will not run at the scheduled times because it has been disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e490-121"><span id="SCHED_S_TASK_HAS_NOT_RUN"></span><span id="sched_s_task_has_not_run"></span>**\_задача sched \_ S \_ \_ не \_ выполнена**</span><span class="sxs-lookup"><span data-stu-id="4e490-121"><span id="SCHED_S_TASK_HAS_NOT_RUN"></span><span id="sched_s_task_has_not_run"></span>**SCHED\_S\_TASK\_HAS\_NOT\_RUN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e490-122">0x00041303</span><span class="sxs-lookup"><span data-stu-id="4e490-122">0x00041303</span></span>
</dt> <dt>



<span data-ttu-id="4e490-123">Задача еще не выполнена.</span><span class="sxs-lookup"><span data-stu-id="4e490-123">The task has not yet run.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e490-124"><span id="SCHED_S_TASK_NO_MORE_RUNS"></span><span id="sched_s_task_no_more_runs"></span>**\_выполнение задачи "sched S" \_ \_ больше не \_ \_ выполняется**</span><span class="sxs-lookup"><span data-stu-id="4e490-124"><span id="SCHED_S_TASK_NO_MORE_RUNS"></span><span id="sched_s_task_no_more_runs"></span>**SCHED\_S\_TASK\_NO\_MORE\_RUNS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e490-125">0x00041304</span><span class="sxs-lookup"><span data-stu-id="4e490-125">0x00041304</span></span>
</dt> <dt>



<span data-ttu-id="4e490-126">Для этой задачи больше нет запланированных запусков.</span><span class="sxs-lookup"><span data-stu-id="4e490-126">There are no more runs scheduled for this task.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e490-127"><span id="SCHED_S_TASK_NOT_SCHEDULED"></span><span id="sched_s_task_not_scheduled"></span>**\_ \_ \_ не \_ запланированная задача "sched S"**</span><span class="sxs-lookup"><span data-stu-id="4e490-127"><span id="SCHED_S_TASK_NOT_SCHEDULED"></span><span id="sched_s_task_not_scheduled"></span>**SCHED\_S\_TASK\_NOT\_SCHEDULED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e490-128">0x00041305</span><span class="sxs-lookup"><span data-stu-id="4e490-128">0x00041305</span></span>
</dt> <dt>



<span data-ttu-id="4e490-129">Не задано одно или несколько свойств, необходимых для выполнения этой задачи по расписанию.</span><span class="sxs-lookup"><span data-stu-id="4e490-129">One or more of the properties that are needed to run this task on a schedule have not been set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e490-130"><span id="SCHED_S_TASK_TERMINATED"></span><span id="sched_s_task_terminated"></span>**Задача "запланировать \_ S" \_ \_ прервана**</span><span class="sxs-lookup"><span data-stu-id="4e490-130"><span id="SCHED_S_TASK_TERMINATED"></span><span id="sched_s_task_terminated"></span>**SCHED\_S\_TASK\_TERMINATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e490-131">0x00041306</span><span class="sxs-lookup"><span data-stu-id="4e490-131">0x00041306</span></span>
</dt> <dt>



<span data-ttu-id="4e490-132">Последнее выполнение задачи было прервано пользователем.</span><span class="sxs-lookup"><span data-stu-id="4e490-132">The last run of the task was terminated by the user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e490-133"><span id="SCHED_S_TASK_NO_VALID_TRIGGERS"></span><span id="sched_s_task_no_valid_triggers"></span>**\_ \_ \_ нет \_ допустимых \_ триггеров для задачи sched S**</span><span class="sxs-lookup"><span data-stu-id="4e490-133"><span id="SCHED_S_TASK_NO_VALID_TRIGGERS"></span><span id="sched_s_task_no_valid_triggers"></span>**SCHED\_S\_TASK\_NO\_VALID\_TRIGGERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e490-134">0x00041307</span><span class="sxs-lookup"><span data-stu-id="4e490-134">0x00041307</span></span>
</dt> <dt>



<span data-ttu-id="4e490-135">Либо задача не имеет триггеров, либо существующие триггеры отключены или не заданы.</span><span class="sxs-lookup"><span data-stu-id="4e490-135">Either the task has no triggers or the existing triggers are disabled or not set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e490-136"><span id="SCHED_S_EVENT_TRIGGER"></span><span id="sched_s_event_trigger"></span>**событие "SCHED \_ S" \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4e490-136"><span id="SCHED_S_EVENT_TRIGGER"></span><span id="sched_s_event_trigger"></span>**SCHED\_S\_EVENT\_TRIGGER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e490-137">0x00041308</span><span class="sxs-lookup"><span data-stu-id="4e490-137">0x00041308</span></span>
</dt> <dt>



<span data-ttu-id="4e490-138">Триггеры событий не имеют значения времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="4e490-138">Event triggers do not have set run times.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e490-139"><span id="SCHED_E_TRIGGER_NOT_FOUND"></span><span id="sched_e_trigger_not_found"></span>**\_ \_ \_ не \_ найден триггер sched E**</span><span class="sxs-lookup"><span data-stu-id="4e490-139"><span id="SCHED_E_TRIGGER_NOT_FOUND"></span><span id="sched_e_trigger_not_found"></span>**SCHED\_E\_TRIGGER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e490-140">0x80041309</span><span class="sxs-lookup"><span data-stu-id="4e490-140">0x80041309</span></span>
</dt> <dt>



<span data-ttu-id="4e490-141">Триггер задачи не найден.</span><span class="sxs-lookup"><span data-stu-id="4e490-141">A task's trigger is not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e490-142"><span id="SCHED_E_TASK_NOT_READY"></span><span id="sched_e_task_not_ready"></span>**Задача "SCHED \_ E" \_ \_ не \_ готова**</span><span class="sxs-lookup"><span data-stu-id="4e490-142"><span id="SCHED_E_TASK_NOT_READY"></span><span id="sched_e_task_not_ready"></span>**SCHED\_E\_TASK\_NOT\_READY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e490-143">0x8004130A</span><span class="sxs-lookup"><span data-stu-id="4e490-143">0x8004130A</span></span>
</dt> <dt>



<span data-ttu-id="4e490-144">Не задано одно или несколько свойств, необходимых для выполнения этой задачи.</span><span class="sxs-lookup"><span data-stu-id="4e490-144">One or more of the properties required to run this task have not been set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e490-145"><span id="SCHED_E_TASK_NOT_RUNNING"></span><span id="sched_e_task_not_running"></span>**\_задача sched \_ E \_ не \_ запущена**</span><span class="sxs-lookup"><span data-stu-id="4e490-145"><span id="SCHED_E_TASK_NOT_RUNNING"></span><span id="sched_e_task_not_running"></span>**SCHED\_E\_TASK\_NOT\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e490-146">0x8004130B</span><span class="sxs-lookup"><span data-stu-id="4e490-146">0x8004130B</span></span>
</dt> <dt>



<span data-ttu-id="4e490-147">Выполняющийся экземпляр задачи отсутствует.</span><span class="sxs-lookup"><span data-stu-id="4e490-147">There is no running instance of the task.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e490-148"><span id="SCHED_E_SERVICE_NOT_INSTALLED"></span><span id="sched_e_service_not_installed"></span>**\_ \_ \_ не \_ установлена служба sched E**</span><span class="sxs-lookup"><span data-stu-id="4e490-148"><span id="SCHED_E_SERVICE_NOT_INSTALLED"></span><span id="sched_e_service_not_installed"></span>**SCHED\_E\_SERVICE\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e490-149">0x8004130C</span><span class="sxs-lookup"><span data-stu-id="4e490-149">0x8004130C</span></span>
</dt> <dt>



<span data-ttu-id="4e490-150">На этом компьютере не установлена служба планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="4e490-150">The Task Scheduler service is not installed on this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e490-151"><span id="SCHED_E_CANNOT_OPEN_TASK"></span><span id="sched_e_cannot_open_task"></span>**\_ \_ не удается \_ открыть \_ задачу sched E**</span><span class="sxs-lookup"><span data-stu-id="4e490-151"><span id="SCHED_E_CANNOT_OPEN_TASK"></span><span id="sched_e_cannot_open_task"></span>**SCHED\_E\_CANNOT\_OPEN\_TASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e490-152">0x8004130D</span><span class="sxs-lookup"><span data-stu-id="4e490-152">0x8004130D</span></span>
</dt> <dt>



<span data-ttu-id="4e490-153">Не удалось открыть объект задачи.</span><span class="sxs-lookup"><span data-stu-id="4e490-153">The task object could not be opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e490-154"><span id="SCHED_E_INVALID_TASK"></span><span id="sched_e_invalid_task"></span>**SCHED \_ \_ недопустимую \_ задачу**</span><span class="sxs-lookup"><span data-stu-id="4e490-154"><span id="SCHED_E_INVALID_TASK"></span><span id="sched_e_invalid_task"></span>**SCHED\_E\_INVALID\_TASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e490-155">0x8004130E</span><span class="sxs-lookup"><span data-stu-id="4e490-155">0x8004130E</span></span>
</dt> <dt>



<span data-ttu-id="4e490-156">Объект либо является недопустимым объектом Task, либо не является объектом Task.</span><span class="sxs-lookup"><span data-stu-id="4e490-156">The object is either an invalid task object or is not a task object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e490-157"><span id="SCHED_E_ACCOUNT_INFORMATION_NOT_SET"></span><span id="sched_e_account_information_not_set"></span>**\_ \_ \_ \_ не заданы сведения об учетной записи "sched E" \_**</span><span class="sxs-lookup"><span data-stu-id="4e490-157"><span id="SCHED_E_ACCOUNT_INFORMATION_NOT_SET"></span><span id="sched_e_account_information_not_set"></span>**SCHED\_E\_ACCOUNT\_INFORMATION\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e490-158">0x8004130F</span><span class="sxs-lookup"><span data-stu-id="4e490-158">0x8004130F</span></span>
</dt> <dt>



<span data-ttu-id="4e490-159">Не удалось найти сведения об учетной записи в планировщик задач базе данных безопасности для указанной задачи.</span><span class="sxs-lookup"><span data-stu-id="4e490-159">No account information could be found in the Task Scheduler security database for the task indicated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e490-160"><span id="SCHED_E_ACCOUNT_NAME_NOT_FOUND"></span><span id="sched_e_account_name_not_found"></span>**\_ \_ \_ \_ не найдено имя учетной записи "sched E \_ "**</span><span class="sxs-lookup"><span data-stu-id="4e490-160"><span id="SCHED_E_ACCOUNT_NAME_NOT_FOUND"></span><span id="sched_e_account_name_not_found"></span>**SCHED\_E\_ACCOUNT\_NAME\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e490-161">0x80041310</span><span class="sxs-lookup"><span data-stu-id="4e490-161">0x80041310</span></span>
</dt> <dt>



<span data-ttu-id="4e490-162">Не удалось установить существование указанной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="4e490-162">Unable to establish existence of the account specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e490-163"><span id="SCHED_E_ACCOUNT_DBASE_CORRUPT"></span><span id="sched_e_account_dbase_corrupt"></span>**\_ \_ повреждение dBASE учетной записи \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4e490-163"><span id="SCHED_E_ACCOUNT_DBASE_CORRUPT"></span><span id="sched_e_account_dbase_corrupt"></span>**SCHED\_E\_ACCOUNT\_DBASE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e490-164">0x80041311</span><span class="sxs-lookup"><span data-stu-id="4e490-164">0x80041311</span></span>
</dt> <dt>



<span data-ttu-id="4e490-165">В базе данных безопасности планировщик задач обнаружено повреждение; база данных была сброшена.</span><span class="sxs-lookup"><span data-stu-id="4e490-165">Corruption was detected in the Task Scheduler security database; the database has been reset.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e490-166"><span id="SCHED_E_NO_SECURITY_SERVICES"></span><span id="sched_e_no_security_services"></span>**SCHED \_ E \_ нет \_ \_ служб безопасности**</span><span class="sxs-lookup"><span data-stu-id="4e490-166"><span id="SCHED_E_NO_SECURITY_SERVICES"></span><span id="sched_e_no_security_services"></span>**SCHED\_E\_NO\_SECURITY\_SERVICES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e490-167">0x80041312</span><span class="sxs-lookup"><span data-stu-id="4e490-167">0x80041312</span></span>
</dt> <dt>



<span data-ttu-id="4e490-168">Планировщик задач службы безопасности доступны только в Windows NT.</span><span class="sxs-lookup"><span data-stu-id="4e490-168">Task Scheduler security services are available only on Windows NT.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e490-169"><span id="SCHED_E_UNKNOWN_OBJECT_VERSION"></span><span id="sched_e_unknown_object_version"></span>**SCHED \_ \_ неизвестная \_ \_ версия объекта**</span><span class="sxs-lookup"><span data-stu-id="4e490-169"><span id="SCHED_E_UNKNOWN_OBJECT_VERSION"></span><span id="sched_e_unknown_object_version"></span>**SCHED\_E\_UNKNOWN\_OBJECT\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e490-170">0x80041313</span><span class="sxs-lookup"><span data-stu-id="4e490-170">0x80041313</span></span>
</dt> <dt>



<span data-ttu-id="4e490-171">Версия объекта задачи либо не поддерживается, либо недопустима.</span><span class="sxs-lookup"><span data-stu-id="4e490-171">The task object version is either unsupported or invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e490-172"><span id="SCHED_E_UNSUPPORTED_ACCOUNT_OPTION"></span><span id="sched_e_unsupported_account_option"></span>**SCHED \_ \_ неподдерживаемый \_ параметр учетной записи \_**</span><span class="sxs-lookup"><span data-stu-id="4e490-172"><span id="SCHED_E_UNSUPPORTED_ACCOUNT_OPTION"></span><span id="sched_e_unsupported_account_option"></span>**SCHED\_E\_UNSUPPORTED\_ACCOUNT\_OPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e490-173">0x80041314</span><span class="sxs-lookup"><span data-stu-id="4e490-173">0x80041314</span></span>
</dt> <dt>



<span data-ttu-id="4e490-174">В задаче настроено неподдерживаемое сочетание параметров учетной записи и параметров времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="4e490-174">The task has been configured with an unsupported combination of account settings and run time options.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e490-175"><span id="SCHED_E_SERVICE_NOT_RUNNING"></span><span id="sched_e_service_not_running"></span>**\_Служба sched \_ E \_ не \_ запущена**</span><span class="sxs-lookup"><span data-stu-id="4e490-175"><span id="SCHED_E_SERVICE_NOT_RUNNING"></span><span id="sched_e_service_not_running"></span>**SCHED\_E\_SERVICE\_NOT\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e490-176">0x80041315</span><span class="sxs-lookup"><span data-stu-id="4e490-176">0x80041315</span></span>
</dt> <dt>



<span data-ttu-id="4e490-177">Служба планировщик задач не запущена.</span><span class="sxs-lookup"><span data-stu-id="4e490-177">The Task Scheduler Service is not running.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e490-178"><span id="SCHED_E_UNEXPECTEDNODE"></span><span id="sched_e_unexpectednode"></span>**SCHED \_ E \_ унекспектедноде**</span><span class="sxs-lookup"><span data-stu-id="4e490-178"><span id="SCHED_E_UNEXPECTEDNODE"></span><span id="sched_e_unexpectednode"></span>**SCHED\_E\_UNEXPECTEDNODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e490-179">0x80041316</span><span class="sxs-lookup"><span data-stu-id="4e490-179">0x80041316</span></span>
</dt> <dt>



<span data-ttu-id="4e490-180">XML-код задачи содержит непредвиденный узел.</span><span class="sxs-lookup"><span data-stu-id="4e490-180">The task XML contains an unexpected node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e490-181"><span id="SCHED_E_NAMESPACE"></span><span id="sched_e_namespace"></span>**\_ \_ пространство имен "sched"**</span><span class="sxs-lookup"><span data-stu-id="4e490-181"><span id="SCHED_E_NAMESPACE"></span><span id="sched_e_namespace"></span>**SCHED\_E\_NAMESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e490-182">0x80041317</span><span class="sxs-lookup"><span data-stu-id="4e490-182">0x80041317</span></span>
</dt> <dt>



<span data-ttu-id="4e490-183">XML-код задачи содержит элемент или атрибут из непредвиденного пространства имен.</span><span class="sxs-lookup"><span data-stu-id="4e490-183">The task XML contains an element or attribute from an unexpected namespace.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e490-184"><span id="SCHED_E_INVALIDVALUE"></span><span id="sched_e_invalidvalue"></span>**SCHED \_ E \_ инвалидвалуе**</span><span class="sxs-lookup"><span data-stu-id="4e490-184"><span id="SCHED_E_INVALIDVALUE"></span><span id="sched_e_invalidvalue"></span>**SCHED\_E\_INVALIDVALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e490-185">0x80041318</span><span class="sxs-lookup"><span data-stu-id="4e490-185">0x80041318</span></span>
</dt> <dt>



<span data-ttu-id="4e490-186">XML-код задачи содержит значение, которое неправильно отформатировано или выходит за пределы диапазона.</span><span class="sxs-lookup"><span data-stu-id="4e490-186">The task XML contains a value which is incorrectly formatted or out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e490-187"><span id="SCHED_E_MISSINGNODE"></span><span id="sched_e_missingnode"></span>**SCHED \_ E \_ миссингноде**</span><span class="sxs-lookup"><span data-stu-id="4e490-187"><span id="SCHED_E_MISSINGNODE"></span><span id="sched_e_missingnode"></span>**SCHED\_E\_MISSINGNODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e490-188">0x80041319</span><span class="sxs-lookup"><span data-stu-id="4e490-188">0x80041319</span></span>
</dt> <dt>



<span data-ttu-id="4e490-189">В XML-коде задачи отсутствует обязательный элемент или атрибут.</span><span class="sxs-lookup"><span data-stu-id="4e490-189">The task XML is missing a required element or attribute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e490-190"><span id="SCHED_E_MALFORMEDXML"></span><span id="sched_e_malformedxml"></span>**SCHED \_ E \_ малформедксмл**</span><span class="sxs-lookup"><span data-stu-id="4e490-190"><span id="SCHED_E_MALFORMEDXML"></span><span id="sched_e_malformedxml"></span>**SCHED\_E\_MALFORMEDXML**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e490-191">0x8004131A</span><span class="sxs-lookup"><span data-stu-id="4e490-191">0x8004131A</span></span>
</dt> <dt>



<span data-ttu-id="4e490-192">XML-код задачи имеет неправильный формат.</span><span class="sxs-lookup"><span data-stu-id="4e490-192">The task XML is malformed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e490-193"><span id="SCHED_S_SOME_TRIGGERS_FAILED"></span><span id="sched_s_some_triggers_failed"></span>**не удалось запланировать \_ \_ некоторые \_ Триггеры \_**</span><span class="sxs-lookup"><span data-stu-id="4e490-193"><span id="SCHED_S_SOME_TRIGGERS_FAILED"></span><span id="sched_s_some_triggers_failed"></span>**SCHED\_S\_SOME\_TRIGGERS\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e490-194">0x0004131B</span><span class="sxs-lookup"><span data-stu-id="4e490-194">0x0004131B</span></span>
</dt> <dt>



<span data-ttu-id="4e490-195">Задача зарегистрирована, но не все указанные триггеры будут запускать задачу.</span><span class="sxs-lookup"><span data-stu-id="4e490-195">The task is registered, but not all specified triggers will start the task.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e490-196"><span id="SCHED_S_BATCH_LOGON_PROBLEM"></span><span id="sched_s_batch_logon_problem"></span>**\_ \_ Ошибка пакетного \_ входа sched S \_**</span><span class="sxs-lookup"><span data-stu-id="4e490-196"><span id="SCHED_S_BATCH_LOGON_PROBLEM"></span><span id="sched_s_batch_logon_problem"></span>**SCHED\_S\_BATCH\_LOGON\_PROBLEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e490-197">0x0004131C</span><span class="sxs-lookup"><span data-stu-id="4e490-197">0x0004131C</span></span>
</dt> <dt>



<span data-ttu-id="4e490-198">Задача зарегистрирована, но может не запуститься.</span><span class="sxs-lookup"><span data-stu-id="4e490-198">The task is registered, but may fail to start.</span></span> <span data-ttu-id="4e490-199">Для участника задачи необходимо включить привилегию пакетного входа.</span><span class="sxs-lookup"><span data-stu-id="4e490-199">Batch logon privilege needs to be enabled for the task principal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e490-200"><span id="SCHED_E_TOO_MANY_NODES"></span><span id="sched_e_too_many_nodes"></span>**SCHED \_ \_ слишком \_ много \_ узлов**</span><span class="sxs-lookup"><span data-stu-id="4e490-200"><span id="SCHED_E_TOO_MANY_NODES"></span><span id="sched_e_too_many_nodes"></span>**SCHED\_E\_TOO\_MANY\_NODES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e490-201">0x8004131D</span><span class="sxs-lookup"><span data-stu-id="4e490-201">0x8004131D</span></span>
</dt> <dt>



<span data-ttu-id="4e490-202">XML-код задачи содержит слишком много узлов одного типа.</span><span class="sxs-lookup"><span data-stu-id="4e490-202">The task XML contains too many nodes of the same type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e490-203"><span id="SCHED_E_PAST_END_BOUNDARY"></span><span id="sched_e_past_end_boundary"></span>**запланировать \_ \_ границу по прошедшему \_ краю \_**</span><span class="sxs-lookup"><span data-stu-id="4e490-203"><span id="SCHED_E_PAST_END_BOUNDARY"></span><span id="sched_e_past_end_boundary"></span>**SCHED\_E\_PAST\_END\_BOUNDARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e490-204">0x8004131E</span><span class="sxs-lookup"><span data-stu-id="4e490-204">0x8004131E</span></span>
</dt> <dt>



<span data-ttu-id="4e490-205">Задача не может быть запущена после границ конечной точки триггера.</span><span class="sxs-lookup"><span data-stu-id="4e490-205">The task cannot be started after the trigger end boundary.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e490-206"><span id="SCHED_E_ALREADY_RUNNING"></span><span id="sched_e_already_running"></span>**SCHED \_ E \_ уже \_ запущено**</span><span class="sxs-lookup"><span data-stu-id="4e490-206"><span id="SCHED_E_ALREADY_RUNNING"></span><span id="sched_e_already_running"></span>**SCHED\_E\_ALREADY\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e490-207">0x8004131F</span><span class="sxs-lookup"><span data-stu-id="4e490-207">0x8004131F</span></span>
</dt> <dt>



<span data-ttu-id="4e490-208">Экземпляр этой задачи уже запущен.</span><span class="sxs-lookup"><span data-stu-id="4e490-208">An instance of this task is already running.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e490-209"><span id="SCHED_E_USER_NOT_LOGGED_ON"></span><span id="sched_e_user_not_logged_on"></span>**\_ \_ \_ не \_ зарегистрировано пользователь sched \_ E**</span><span class="sxs-lookup"><span data-stu-id="4e490-209"><span id="SCHED_E_USER_NOT_LOGGED_ON"></span><span id="sched_e_user_not_logged_on"></span>**SCHED\_E\_USER\_NOT\_LOGGED\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e490-210">0x80041320</span><span class="sxs-lookup"><span data-stu-id="4e490-210">0x80041320</span></span>
</dt> <dt>



<span data-ttu-id="4e490-211">Задача не будет запущена, так как пользователь не вошел в систему.</span><span class="sxs-lookup"><span data-stu-id="4e490-211">The task will not run because the user is not logged on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e490-212"><span id="SCHED_E_INVALID_TASK_HASH"></span><span id="sched_e_invalid_task_hash"></span>**SCHED \_ \_ Недопустимый \_ \_ хэш задачи**</span><span class="sxs-lookup"><span data-stu-id="4e490-212"><span id="SCHED_E_INVALID_TASK_HASH"></span><span id="sched_e_invalid_task_hash"></span>**SCHED\_E\_INVALID\_TASK\_HASH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e490-213">0x80041321</span><span class="sxs-lookup"><span data-stu-id="4e490-213">0x80041321</span></span>
</dt> <dt>



<span data-ttu-id="4e490-214">Изображение задачи повреждено или было незаконно изменено.</span><span class="sxs-lookup"><span data-stu-id="4e490-214">The task image is corrupt or has been tampered with.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e490-215"><span id="SCHED_E_SERVICE_NOT_AVAILABLE"></span><span id="sched_e_service_not_available"></span>**\_Служба sched \_ E \_ \_ недоступна**</span><span class="sxs-lookup"><span data-stu-id="4e490-215"><span id="SCHED_E_SERVICE_NOT_AVAILABLE"></span><span id="sched_e_service_not_available"></span>**SCHED\_E\_SERVICE\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e490-216">0x80041322</span><span class="sxs-lookup"><span data-stu-id="4e490-216">0x80041322</span></span>
</dt> <dt>



<span data-ttu-id="4e490-217">Служба планировщик задач недоступна.</span><span class="sxs-lookup"><span data-stu-id="4e490-217">The Task Scheduler service is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e490-218"><span id="SCHED_E_SERVICE_TOO_BUSY"></span><span id="sched_e_service_too_busy"></span>**\_ \_ \_ слишком \_ занятая служба sched E**</span><span class="sxs-lookup"><span data-stu-id="4e490-218"><span id="SCHED_E_SERVICE_TOO_BUSY"></span><span id="sched_e_service_too_busy"></span>**SCHED\_E\_SERVICE\_TOO\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e490-219">0x80041323</span><span class="sxs-lookup"><span data-stu-id="4e490-219">0x80041323</span></span>
</dt> <dt>



<span data-ttu-id="4e490-220">Служба планировщик задач слишком занята, чтобы обрабатывал ваш запрос.</span><span class="sxs-lookup"><span data-stu-id="4e490-220">The Task Scheduler service is too busy to handle your request.</span></span> <span data-ttu-id="4e490-221">Повторите попытку позже.</span><span class="sxs-lookup"><span data-stu-id="4e490-221">Please try again later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e490-222"><span id="SCHED_E_TASK_ATTEMPTED"></span><span id="sched_e_task_attempted"></span>**\_ \_ \_ предпринята попыток задачи sched E**</span><span class="sxs-lookup"><span data-stu-id="4e490-222"><span id="SCHED_E_TASK_ATTEMPTED"></span><span id="sched_e_task_attempted"></span>**SCHED\_E\_TASK\_ATTEMPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e490-223">0x80041324</span><span class="sxs-lookup"><span data-stu-id="4e490-223">0x80041324</span></span>
</dt> <dt>



<span data-ttu-id="4e490-224">Служба планировщик задача попыталась выполнить задачу, но задача не была выполнена из-за одного из ограничений в определении задачи.</span><span class="sxs-lookup"><span data-stu-id="4e490-224">The Task Scheduler service attempted to run the task, but the task did not run due to one of the constraints in the task definition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e490-225"><span id="SCHED_S_TASK_QUEUED"></span><span id="sched_s_task_queued"></span>**Задача "SCHED \_ S" \_ \_ поставлена в очередь**</span><span class="sxs-lookup"><span data-stu-id="4e490-225"><span id="SCHED_S_TASK_QUEUED"></span><span id="sched_s_task_queued"></span>**SCHED\_S\_TASK\_QUEUED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e490-226">0x00041325</span><span class="sxs-lookup"><span data-stu-id="4e490-226">0x00041325</span></span>
</dt> <dt>



<span data-ttu-id="4e490-227">Служба планировщик задач запросила выполнение задачи.</span><span class="sxs-lookup"><span data-stu-id="4e490-227">The Task Scheduler service has asked the task to run.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e490-228"><span id="SCHED_E_TASK_DISABLED"></span><span id="sched_e_task_disabled"></span>**Задача "SCHED \_ E" \_ \_ отключена**</span><span class="sxs-lookup"><span data-stu-id="4e490-228"><span id="SCHED_E_TASK_DISABLED"></span><span id="sched_e_task_disabled"></span>**SCHED\_E\_TASK\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e490-229">0x80041326</span><span class="sxs-lookup"><span data-stu-id="4e490-229">0x80041326</span></span>
</dt> <dt>



<span data-ttu-id="4e490-230">Задача отключена.</span><span class="sxs-lookup"><span data-stu-id="4e490-230">The task is disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e490-231"><span id="SCHED_E_TASK_NOT_V1_COMPAT"></span><span id="sched_e_task_not_v1_compat"></span>**\_ \_ \_ Не \_ \_ высовместимость задачи "sched E"**</span><span class="sxs-lookup"><span data-stu-id="4e490-231"><span id="SCHED_E_TASK_NOT_V1_COMPAT"></span><span id="sched_e_task_not_v1_compat"></span>**SCHED\_E\_TASK\_NOT\_V1\_COMPAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e490-232">0x80041327</span><span class="sxs-lookup"><span data-stu-id="4e490-232">0x80041327</span></span>
</dt> <dt>



<span data-ttu-id="4e490-233">У задачи есть свойства, несовместимые с более ранними версиями Windows.</span><span class="sxs-lookup"><span data-stu-id="4e490-233">The task has properties that are not compatible with earlier versions of Windows.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4e490-234"><span id="SCHED_E_START_ON_DEMAND"></span><span id="sched_e_start_on_demand"></span>**SCHED \_ E \_ Начало \_ по \_ запросу**</span><span class="sxs-lookup"><span data-stu-id="4e490-234"><span id="SCHED_E_START_ON_DEMAND"></span><span id="sched_e_start_on_demand"></span>**SCHED\_E\_START\_ON\_DEMAND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e490-235">0x80041328</span><span class="sxs-lookup"><span data-stu-id="4e490-235">0x80041328</span></span>
</dt> <dt>



<span data-ttu-id="4e490-236">Параметры задачи не позволяют запускать задачу по требованию.</span><span class="sxs-lookup"><span data-stu-id="4e490-236">The task settings do not allow the task to start on demand.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4e490-237">Требования</span><span class="sxs-lookup"><span data-stu-id="4e490-237">Requirements</span></span>



| <span data-ttu-id="4e490-238">Требование</span><span class="sxs-lookup"><span data-stu-id="4e490-238">Requirement</span></span> | <span data-ttu-id="4e490-239">Значение</span><span class="sxs-lookup"><span data-stu-id="4e490-239">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4e490-240">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4e490-240">Minimum supported client</span></span><br/> | <span data-ttu-id="4e490-241">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4e490-241">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4e490-242">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4e490-242">Minimum supported server</span></span><br/> | <span data-ttu-id="4e490-243">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4e490-243">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4e490-244">Header</span><span class="sxs-lookup"><span data-stu-id="4e490-244">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e490-245"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e490-245"><dt>WinError.h</dt></span></span> </dl> |



 

 





