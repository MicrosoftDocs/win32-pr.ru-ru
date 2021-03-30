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
# <a name="triggertype-property"></a>Свойство Trigger. Type

Для сценариев Возвращает тип триггера. Тип триггера определяется при создании триггера и не может быть изменен позже. Сведения о создании триггера см. в разделе [**тригжерколлектион. Create**](triggercollection-create.md).

## <a name="syntax"></a>Синтаксис


```VB
Trigger.Type As TASK_TRIGGER_TYPE2
```



## <a name="property-value"></a>Значение свойства

Одно из следующих значений перечисления типа [**\_ \_ тип2 для триггера задачи**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) .



| Значение                                                                                                                                                                                                                                                                                | Значение                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="TASK_TRIGGER_EVENT"></span><span id="task_trigger_event"></span><dl> <dt>**Задача \_ СРАБАТЫВАНИе \_ события**</dt> <dt>0</dt> </dl>                                                 | Запускает задачу при возникновении определенного события.<br/>              |
| <span id="TASK_TRIGGER_TIME"></span><span id="task_trigger_time"></span><dl> <dt>**Задача \_ \_Время активации**</dt> <dt>1</dt> </dl>                                                    | Запускает задачу в определенное время суток.<br/>                 |
| <span id="TASK_TRIGGER_DAILY"></span><span id="task_trigger_daily"></span><dl> <dt>**Задача \_ ТРИГГЕР \_ ежедневно**</dt> <dt>2</dt> </dl>                                                 | Запускает задачу ежедневно.<br/>                                     |
| <span id="TASK_TRIGGER_WEEKLY"></span><span id="task_trigger_weekly"></span><dl> <dt>**Задача \_ ТРИГГЕР \_ еженедельно**</dt> <dt>3</dt> </dl>                                              | Запускает задачу еженедельно.<br/>                                    |
| <span id="TASK_TRIGGER_MONTHLY"></span><span id="task_trigger_monthly"></span><dl> <dt>**Задача \_ ТРИГГЕР \_ ежемесячно**</dt> <dt>4</dt> </dl>                                           | Запускает задачу ежемесячно.<br/>                                   |
| <span id="TASK_TRIGGER_MONTHLYDOW"></span><span id="task_trigger_monthlydow"></span><dl> <dt>**Задача \_ ТРИГГЕР \_ монслидов**</dt> <dt>5</dt> </dl>                                  | Запускает задачу каждый месяц в конкретный день недели.<br/> |
| <span id="TASK_TRIGGER_IDLE"></span><span id="task_trigger_idle"></span><dl> <dt>**Задача \_ ЗАПУСТИТЬ \_ бездействующее**</dt> <dt>6</dt> </dl>                                                    | Запускает задачу при переходе компьютера в состояние простоя.<br/> |
| <span id="TASK_TRIGGER_REGISTRATION"></span><span id="task_trigger_registration"></span><dl> <dt>**Задача \_ \_Регистрация триггера**</dt> <dt>7</dt> </dl>                            | Запускает задачу при регистрации задачи.<br/>               |
| <span id="TASK_TRIGGER_BOOT"></span><span id="task_trigger_boot"></span><dl> <dt>**Задача \_ ЗАПУСК \_ загрузки**</dt> <dt>8</dt> </dl>                                                    | Запускает задачу при загрузке компьютера.<br/>                   |
| <span id="TASK_TRIGGER_LOGON"></span><span id="task_trigger_logon"></span><dl> <dt>**Задача \_ ЗАПУСК \_ входа**</dt> <dt>9</dt> </dl>                                                 | Запускает задачу при входе определенного пользователя в систему.<br/>              |
| <span id="TASK_TRIGGER_SESSION_STATE_CHANGE"></span><span id="task_trigger_session_state_change"></span><dl> <dt>**Задача \_ \_ \_ \_ Изменение состояния сеанса для триггера**</dt> <dt>11</dt> </dl> | Активирует задачу при изменении определенного состояния сеанса.<br/>   |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                    |
| Библиотека типов<br/>             | <dl> <dt>Тасксчд. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Тригжерколлектион. Create**](triggercollection-create.md)
</dt> <dt>

[**\_Тип 2 триггера задачи \_**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





