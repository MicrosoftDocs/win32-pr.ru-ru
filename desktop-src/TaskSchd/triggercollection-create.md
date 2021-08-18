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
ms.openlocfilehash: a7cfc32ebff941af374d2c4bb64db8ffe064961c13840e50244f416bad477a8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001972"
---
# <a name="triggercollectioncreate-method"></a>Тригжерколлектион. Create, метод

Для создания скрипта создает новый триггер для задачи.

## <a name="syntax"></a>Синтаксис


```VB
TriggerCollection.Create( _
  ByVal type _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*тип* \[ окне\]
</dt> <dd>

Для этого параметра задается одна из следующих констант перечисления типа [**\_ \_ 2 триггера задачи**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2) .



| Значение                                                                                                                                                                                                                                                                                | Значение                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_TRIGGER_EVENT"></span><span id="task_trigger_event"></span><dl> <dt>**Задача \_ СРАБАТЫВАНИе \_ события**</dt> <dt>0</dt> </dl>                                                 | Активирует задачу при возникновении определенного события.<br/>                                                                                                               |
| <span id="TASK_TRIGGER_TIME"></span><span id="task_trigger_time"></span><dl> <dt>**Задача \_ \_Время активации**</dt> <dt>1</dt> </dl>                                                    | Запускает задачу в определенное время суток.<br/>                                                                                                                  |
| <span id="TASK_TRIGGER_DAILY"></span><span id="task_trigger_daily"></span><dl> <dt>**Задача \_ ТРИГГЕР \_ ежедневно**</dt> <dt>2</dt> </dl>                                                 | Запускает задачу ежедневно по расписанию. Например, задача начинается в определенное время каждый день, каждый второй день, каждый третий день и т. д.<br/>                |
| <span id="TASK_TRIGGER_WEEKLY"></span><span id="task_trigger_weekly"></span><dl> <dt>**Задача \_ ТРИГГЕР \_ еженедельно**</dt> <dt>3</dt> </dl>                                              | Запускает задачу по еженедельному расписанию. Например, задача начинается в 8:00 в конкретный день каждую неделю или неделю.<br/>                                   |
| <span id="TASK_TRIGGER_MONTHLY"></span><span id="task_trigger_monthly"></span><dl> <dt>**Задача \_ ТРИГГЕР \_ ежемесячно**</dt> <dt>4</dt> </dl>                                           | Запускает задачу по месячному расписанию. Например, задача запускается в определенные дни конкретного месяца.<br/>                                                    |
| <span id="TASK_TRIGGER_MONTHLYDOW"></span><span id="task_trigger_monthlydow"></span><dl> <dt>**Задача \_ ТРИГГЕР \_ монслидов**</dt> <dt>5</dt> </dl>                                  | Запускает задачу в расписании ежемесячного дня недели. Например, задача запускается в определенные дни недели, недели месяца и месяцы года.<br/> |
| <span id="TASK_TRIGGER_IDLE"></span><span id="task_trigger_idle"></span><dl> <dt>**Задача \_ ЗАПУСТИТЬ \_ бездействующее**</dt> <dt>6</dt> </dl>                                                    | Запускает задачу при переходе компьютера в состояние простоя.<br/>                                                                                                  |
| <span id="TASK_TRIGGER_REGISTRATION"></span><span id="task_trigger_registration"></span><dl> <dt>**Задача \_ \_Регистрация триггера**</dt> <dt>7</dt> </dl>                            | Активирует задачу при регистрации задачи.<br/>                                                                                                                |
| <span id="TASK_TRIGGER_BOOT"></span><span id="task_trigger_boot"></span><dl> <dt>**Задача \_ ЗАПУСК \_ загрузки**</dt> <dt>8</dt> </dl>                                                    | Запускает задачу при загрузке компьютера.<br/>                                                                                                                    |
| <span id="TASK_TRIGGER_LOGON"></span><span id="task_trigger_logon"></span><dl> <dt>**Задача \_ ЗАПУСК \_ входа**</dt> <dt>9</dt> </dl>                                                 | Запускает задачу при входе определенного пользователя в систему.<br/>                                                                                                               |
| <span id="TASK_TRIGGER_SESSION_STATE_CHANGE"></span><span id="task_trigger_session_state_change"></span><dl> <dt>**Задача \_ \_ \_ \_ Изменение состояния сеанса для триггера**</dt> <dt>11</dt> </dl> | Активирует задачу при изменении определенного состояния сеанса.<br/>                                                                                                      |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Объект [**триггера**](trigger.md) , представляющий новый триггер.

## <a name="remarks"></a>Remarks

Сведения о каждом типе триггера см. в разделе [типы триггеров](trigger-types.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                    |
| Библиотека типов<br/>             | <dl> <dt>Тасксчд. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> <dt>

[**Триггер**](trigger.md)
</dt> </dl>

 

 





