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
ms.openlocfilehash: 74ae14f6e22245e49b2c2d0136fd297b35c9c5ed1f5126cc0914e97f42c8488f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611005"
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



## <a name="remarks"></a>Remarks

При чтении или записи XML элементы, определенные этой группой, являются дочерними элементами элемента [**Triggers**](taskschedulerschema-triggers-tasktype-element.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





