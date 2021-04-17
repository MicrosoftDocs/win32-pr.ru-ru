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
# <a name="task-scheduler-error-and-success-constants"></a>планировщик задач константы ошибок и успешности

При возникновении ошибки API-интерфейсы планировщик задач могут возвращать один из следующих кодов ошибок как значение **HRESULT** .

Константы, начинающиеся с SCHED \_ S, \_ являются константами успеха, а константы, которые начинаются с sched \_ E \_ , являются константами ошибок.

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

Пример [кода C/C++: получение состояния задачи](c-c-code-example-retrieving-task-status.md).

> [!Note]  
> Некоторые планировщик задач API могут возвращать системные и сетевые коды ошибок (например, 64). Определение этих типов кодов ошибок можно проверить с помощью команды **net helpmsg** в окне командной строки. Например, команда **net helpmsg 64** возвращает сообщение: указанное сетевое имя больше недоступно.

 

Дополнительные сведения о событиях и сообщениях об ошибках см. в разделе [события и ошибки в центре сообщений](https://www.microsoft.com/technet/support/ee/ee_advanced.aspx).

<dl> <dt>

<span id="SCHED_S_TASK_READY"></span><span id="sched_s_task_ready"></span>**Задача "SCHED \_ S" \_ \_ готова**
</dt> <dd> <dl> <dt>

0x00041300
</dt> <dt>



Задача готова к выполнению в следующее запланированное время.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_RUNNING"></span><span id="sched_s_task_running"></span>**\_ \_ выполнение задачи "запланировать S" \_**
</dt> <dd> <dl> <dt>

0x00041301
</dt> <dt>



Задача выполняется в данный момент.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_DISABLED"></span><span id="sched_s_task_disabled"></span>**Задача "SCHED \_ S" \_ \_ отключена**
</dt> <dd> <dl> <dt>

0x00041302
</dt> <dt>



Задача не будет выполняться в запланированное время, так как она была отключена.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_HAS_NOT_RUN"></span><span id="sched_s_task_has_not_run"></span>**\_задача sched \_ S \_ \_ не \_ выполнена**
</dt> <dd> <dl> <dt>

0x00041303
</dt> <dt>



Задача еще не выполнена.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_NO_MORE_RUNS"></span><span id="sched_s_task_no_more_runs"></span>**\_выполнение задачи "sched S" \_ \_ больше не \_ \_ выполняется**
</dt> <dd> <dl> <dt>

0x00041304
</dt> <dt>



Для этой задачи больше нет запланированных запусков.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_NOT_SCHEDULED"></span><span id="sched_s_task_not_scheduled"></span>**\_ \_ \_ не \_ запланированная задача "sched S"**
</dt> <dd> <dl> <dt>

0x00041305
</dt> <dt>



Не задано одно или несколько свойств, необходимых для выполнения этой задачи по расписанию.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_TERMINATED"></span><span id="sched_s_task_terminated"></span>**Задача "запланировать \_ S" \_ \_ прервана**
</dt> <dd> <dl> <dt>

0x00041306
</dt> <dt>



Последнее выполнение задачи было прервано пользователем.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_NO_VALID_TRIGGERS"></span><span id="sched_s_task_no_valid_triggers"></span>**\_ \_ \_ нет \_ допустимых \_ триггеров для задачи sched S**
</dt> <dd> <dl> <dt>

0x00041307
</dt> <dt>



Либо задача не имеет триггеров, либо существующие триггеры отключены или не заданы.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_EVENT_TRIGGER"></span><span id="sched_s_event_trigger"></span>**событие "SCHED \_ S" \_ \_**
</dt> <dd> <dl> <dt>

0x00041308
</dt> <dt>



Триггеры событий не имеют значения времени выполнения.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TRIGGER_NOT_FOUND"></span><span id="sched_e_trigger_not_found"></span>**\_ \_ \_ не \_ найден триггер sched E**
</dt> <dd> <dl> <dt>

0x80041309
</dt> <dt>



Триггер задачи не найден.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TASK_NOT_READY"></span><span id="sched_e_task_not_ready"></span>**Задача "SCHED \_ E" \_ \_ не \_ готова**
</dt> <dd> <dl> <dt>

0x8004130A
</dt> <dt>



Не задано одно или несколько свойств, необходимых для выполнения этой задачи.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TASK_NOT_RUNNING"></span><span id="sched_e_task_not_running"></span>**\_задача sched \_ E \_ не \_ запущена**
</dt> <dd> <dl> <dt>

0x8004130B
</dt> <dt>



Выполняющийся экземпляр задачи отсутствует.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_SERVICE_NOT_INSTALLED"></span><span id="sched_e_service_not_installed"></span>**\_ \_ \_ не \_ установлена служба sched E**
</dt> <dd> <dl> <dt>

0x8004130C
</dt> <dt>



На этом компьютере не установлена служба планировщик задач.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_CANNOT_OPEN_TASK"></span><span id="sched_e_cannot_open_task"></span>**\_ \_ не удается \_ открыть \_ задачу sched E**
</dt> <dd> <dl> <dt>

0x8004130D
</dt> <dt>



Не удалось открыть объект задачи.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_INVALID_TASK"></span><span id="sched_e_invalid_task"></span>**SCHED \_ \_ недопустимую \_ задачу**
</dt> <dd> <dl> <dt>

0x8004130E
</dt> <dt>



Объект либо является недопустимым объектом Task, либо не является объектом Task.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_ACCOUNT_INFORMATION_NOT_SET"></span><span id="sched_e_account_information_not_set"></span>**\_ \_ \_ \_ не заданы сведения об учетной записи "sched E" \_**
</dt> <dd> <dl> <dt>

0x8004130F
</dt> <dt>



Не удалось найти сведения об учетной записи в планировщик задач базе данных безопасности для указанной задачи.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_ACCOUNT_NAME_NOT_FOUND"></span><span id="sched_e_account_name_not_found"></span>**\_ \_ \_ \_ не найдено имя учетной записи "sched E \_ "**
</dt> <dd> <dl> <dt>

0x80041310
</dt> <dt>



Не удалось установить существование указанной учетной записи.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_ACCOUNT_DBASE_CORRUPT"></span><span id="sched_e_account_dbase_corrupt"></span>**\_ \_ повреждение dBASE учетной записи \_ \_**
</dt> <dd> <dl> <dt>

0x80041311
</dt> <dt>



В базе данных безопасности планировщик задач обнаружено повреждение; база данных была сброшена.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_NO_SECURITY_SERVICES"></span><span id="sched_e_no_security_services"></span>**SCHED \_ E \_ нет \_ \_ служб безопасности**
</dt> <dd> <dl> <dt>

0x80041312
</dt> <dt>



Планировщик задач службы безопасности доступны только в Windows NT.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_UNKNOWN_OBJECT_VERSION"></span><span id="sched_e_unknown_object_version"></span>**SCHED \_ \_ неизвестная \_ \_ версия объекта**
</dt> <dd> <dl> <dt>

0x80041313
</dt> <dt>



Версия объекта задачи либо не поддерживается, либо недопустима.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_UNSUPPORTED_ACCOUNT_OPTION"></span><span id="sched_e_unsupported_account_option"></span>**SCHED \_ \_ неподдерживаемый \_ параметр учетной записи \_**
</dt> <dd> <dl> <dt>

0x80041314
</dt> <dt>



В задаче настроено неподдерживаемое сочетание параметров учетной записи и параметров времени выполнения.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_SERVICE_NOT_RUNNING"></span><span id="sched_e_service_not_running"></span>**\_Служба sched \_ E \_ не \_ запущена**
</dt> <dd> <dl> <dt>

0x80041315
</dt> <dt>



Служба планировщик задач не запущена.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_UNEXPECTEDNODE"></span><span id="sched_e_unexpectednode"></span>**SCHED \_ E \_ унекспектедноде**
</dt> <dd> <dl> <dt>

0x80041316
</dt> <dt>



XML-код задачи содержит непредвиденный узел.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_NAMESPACE"></span><span id="sched_e_namespace"></span>**\_ \_ пространство имен "sched"**
</dt> <dd> <dl> <dt>

0x80041317
</dt> <dt>



XML-код задачи содержит элемент или атрибут из непредвиденного пространства имен.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_INVALIDVALUE"></span><span id="sched_e_invalidvalue"></span>**SCHED \_ E \_ инвалидвалуе**
</dt> <dd> <dl> <dt>

0x80041318
</dt> <dt>



XML-код задачи содержит значение, которое неправильно отформатировано или выходит за пределы диапазона.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_MISSINGNODE"></span><span id="sched_e_missingnode"></span>**SCHED \_ E \_ миссингноде**
</dt> <dd> <dl> <dt>

0x80041319
</dt> <dt>



В XML-коде задачи отсутствует обязательный элемент или атрибут.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_MALFORMEDXML"></span><span id="sched_e_malformedxml"></span>**SCHED \_ E \_ малформедксмл**
</dt> <dd> <dl> <dt>

0x8004131A
</dt> <dt>



XML-код задачи имеет неправильный формат.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_SOME_TRIGGERS_FAILED"></span><span id="sched_s_some_triggers_failed"></span>**не удалось запланировать \_ \_ некоторые \_ Триггеры \_**
</dt> <dd> <dl> <dt>

0x0004131B
</dt> <dt>



Задача зарегистрирована, но не все указанные триггеры будут запускать задачу.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_BATCH_LOGON_PROBLEM"></span><span id="sched_s_batch_logon_problem"></span>**\_ \_ Ошибка пакетного \_ входа sched S \_**
</dt> <dd> <dl> <dt>

0x0004131C
</dt> <dt>



Задача зарегистрирована, но может не запуститься. Для участника задачи необходимо включить привилегию пакетного входа.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TOO_MANY_NODES"></span><span id="sched_e_too_many_nodes"></span>**SCHED \_ \_ слишком \_ много \_ узлов**
</dt> <dd> <dl> <dt>

0x8004131D
</dt> <dt>



XML-код задачи содержит слишком много узлов одного типа.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_PAST_END_BOUNDARY"></span><span id="sched_e_past_end_boundary"></span>**запланировать \_ \_ границу по прошедшему \_ краю \_**
</dt> <dd> <dl> <dt>

0x8004131E
</dt> <dt>



Задача не может быть запущена после границ конечной точки триггера.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_ALREADY_RUNNING"></span><span id="sched_e_already_running"></span>**SCHED \_ E \_ уже \_ запущено**
</dt> <dd> <dl> <dt>

0x8004131F
</dt> <dt>



Экземпляр этой задачи уже запущен.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_USER_NOT_LOGGED_ON"></span><span id="sched_e_user_not_logged_on"></span>**\_ \_ \_ не \_ зарегистрировано пользователь sched \_ E**
</dt> <dd> <dl> <dt>

0x80041320
</dt> <dt>



Задача не будет запущена, так как пользователь не вошел в систему.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_INVALID_TASK_HASH"></span><span id="sched_e_invalid_task_hash"></span>**SCHED \_ \_ Недопустимый \_ \_ хэш задачи**
</dt> <dd> <dl> <dt>

0x80041321
</dt> <dt>



Изображение задачи повреждено или было незаконно изменено.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_SERVICE_NOT_AVAILABLE"></span><span id="sched_e_service_not_available"></span>**\_Служба sched \_ E \_ \_ недоступна**
</dt> <dd> <dl> <dt>

0x80041322
</dt> <dt>



Служба планировщик задач недоступна.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_SERVICE_TOO_BUSY"></span><span id="sched_e_service_too_busy"></span>**\_ \_ \_ слишком \_ занятая служба sched E**
</dt> <dd> <dl> <dt>

0x80041323
</dt> <dt>



Служба планировщик задач слишком занята, чтобы обрабатывал ваш запрос. Повторите попытку позже.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TASK_ATTEMPTED"></span><span id="sched_e_task_attempted"></span>**\_ \_ \_ предпринята попыток задачи sched E**
</dt> <dd> <dl> <dt>

0x80041324
</dt> <dt>



Служба планировщик задача попыталась выполнить задачу, но задача не была выполнена из-за одного из ограничений в определении задачи.


</dt> </dl> </dd> <dt>

<span id="SCHED_S_TASK_QUEUED"></span><span id="sched_s_task_queued"></span>**Задача "SCHED \_ S" \_ \_ поставлена в очередь**
</dt> <dd> <dl> <dt>

0x00041325
</dt> <dt>



Служба планировщик задач запросила выполнение задачи.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TASK_DISABLED"></span><span id="sched_e_task_disabled"></span>**Задача "SCHED \_ E" \_ \_ отключена**
</dt> <dd> <dl> <dt>

0x80041326
</dt> <dt>



Задача отключена.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_TASK_NOT_V1_COMPAT"></span><span id="sched_e_task_not_v1_compat"></span>**\_ \_ \_ Не \_ \_ высовместимость задачи "sched E"**
</dt> <dd> <dl> <dt>

0x80041327
</dt> <dt>



У задачи есть свойства, несовместимые с более ранними версиями Windows.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_START_ON_DEMAND"></span><span id="sched_e_start_on_demand"></span>**SCHED \_ E \_ Начало \_ по \_ запросу**
</dt> <dd> <dl> <dt>

0x80041328
</dt> <dt>



Параметры задачи не позволяют запускать задачу по требованию.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                  |
| Header<br/>                   | <dl> <dt>WinError. h</dt> </dl> |



 

 





