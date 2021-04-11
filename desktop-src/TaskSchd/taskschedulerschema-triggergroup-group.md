---
title: Группа Тригжерграуп
description: Определяет группу триггеров.
ms.assetid: e07e6999-d982-405b-adfd-2976707b999f
keywords:
- Тригжерграуп планировщик задач
topic_type:
- apiref
api_name:
- triggerGroup
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce0203cd9515808891f93223dd7b3ebaf2642103
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137674"
---
# <a name="triggergroup-group"></a>Группа Тригжерграуп

Определяет группу триггеров.

``` syntax
<xs:group name="triggerGroup">
    <xs:choice>
        <xs:element name="BootTrigger"
            type="bootTriggerType"
            minOccurs="0"
         />
        <xs:element name="RegistrationTrigger"
            type="registrationTriggerType"
            minOccurs="0"
         />
        <xs:element name="IdleTrigger"
            type="idleTriggerType"
            minOccurs="0"
         />
        <xs:element name="TimeTrigger"
            type="timeTriggerType"
            minOccurs="0"
         />
        <xs:element name="EventTrigger"
            type="eventTriggerType"
            minOccurs="0"
         />
        <xs:element name="LogonTrigger"
            type="logonTriggerType"
            minOccurs="0"
         />
        <xs:element name="SessionStateChangeTrigger"
            type="sessionStateChangeTriggerType"
            minOccurs="0"
         />
        <xs:element name="CalendarTrigger"
            type="calendarTriggerType"
            minOccurs="0"
         />
    </xs:choice>
</xs:group>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                                                 | Тип                                                                                                   | Описание                                                                                                       |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**буттригжер**](taskschedulerschema-boottrigger-triggergroup-element.md)                             | [**буттригжертипе**](taskschedulerschema-boottriggertype-complextype.md)                             | Триггер, запускающий задачу при загрузке системы.<br/>                                                |
| [**календартригжер**](taskschedulerschema-calendartrigger-triggergroup-element.md)                     | [**календартригжертипе**](taskschedulerschema-calendartriggertype-complextype.md)                     | Триггер, запускающий задачу на основе расписания ежедневного, еженедельного, ежемесячного или месячного дня недели (DOW).<br/> |
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md)                           | [**евенттригжертипе**](taskschedulerschema-eventtriggertype-complextype.md)                           | Триггер, запускающий задачу при возникновении системного события.<br/>                                               |
| [**идлетригжер**](taskschedulerschema-idletrigger-triggergroup-element.md)                             | [**идлетригжертипе**](taskschedulerschema-idletriggertype-complextype.md)                             | Триггер, запускающий задачу при переходе компьютера в состояние простоя.<br/>                                |
| [**логонтригжер**](taskschedulerschema-logontrigger-triggergroup-element.md)                           | [**логонтригжертипе**](taskschedulerschema-logontriggertype-complextype.md)                           | Триггер, запускающий задачу при входе пользователя в систему.<br/>                                                      |
| [**регистратионтригжер**](taskschedulerschema-registrationtrigger-triggergroup-element.md)             | [**регистратионтригжертипе**](taskschedulerschema-registrationtriggertype-complextype.md)             | Триггер, запускающий задачу при регистрации задачи.<br/>                                              |
| [**сессионстатечанжетригжер**](taskschedulerschema-sessionstatechangetrigger-triggergroup-element.md) | [**сессионстатечанжетригжертипе**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | Триггер, запускающий задачу при изменении состояния сеанса сервера терминалов.<br/>                             |
| [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md)                             | [**тиметригжертипе**](taskschedulerschema-timetriggertype-complextype.md)                             | Триггер, запускающий задачу при активации триггера.<br/>                                            |



## <a name="remarks"></a>Комментарии

При чтении или записи XML элементы, определенные этой группой, являются дочерними элементами элемента [**Triggers**](taskschedulerschema-triggers-tasktype-element.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





