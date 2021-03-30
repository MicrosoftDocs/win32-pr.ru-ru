---
title: Элемент Triggers (taskType)
description: Задает триггеры, которые запускают задачу.
ms.assetid: 4bf8e85e-3742-433d-821f-736fb2ff7139
keywords:
- Элемент Triggers планировщик задач
topic_type:
- apiref
api_name:
- Triggers
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 06994c395fbfbc5b0c6244c9d17930bc4afac885
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803965"
---
# <a name="triggers-tasktype-element"></a>Элемент Triggers (taskType)

Задает триггеры, которые запускают задачу.

``` syntax
<xs:element name="Triggers"
    type="triggersType"
 />
```

Элемент **Triggers** определяется сложным типом [**тригжерстипе**](taskschedulerschema-triggerstype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                          | Унаследован от                                                 | Описание                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [**Задача**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Определяет задачу, выполняемую службой планировщик задач.<br/> |



## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                                     | Тип                                                                                       | Описание                                                                                  |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**буттригжер**](taskschedulerschema-boottrigger-triggergroup-element.md)                 | [**буттригжертипе**](taskschedulerschema-boottriggertype-complextype.md)                 | Указывает триггер, который запускает задачу при загрузке системы.<br/>                 |
| [**календартригжер**](taskschedulerschema-calendartrigger-triggergroup-element.md)         | [**календартригжертипе**](taskschedulerschema-calendartriggertype-complextype.md)         | Задает ежедневный, еженедельный, ежемесячный или ежемесячный триггер (DOW) в день недели.<br/>   |
| [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md)               | [**евенттригжертипе**](taskschedulerschema-eventtriggertype-complextype.md)               | Указывает триггер, который запускает задачу при возникновении системного события.<br/>                |
| [**идлетригжер**](taskschedulerschema-idletrigger-triggergroup-element.md)                 | [**идлетригжертипе**](taskschedulerschema-idletriggertype-complextype.md)                 | Указывает триггер, который запускает задачу при переходе компьютера в состояние простоя.<br/> |
| [**логонтригжер**](taskschedulerschema-logontrigger-triggergroup-element.md)               | [**логонтригжертипе**](taskschedulerschema-logontriggertype-complextype.md)               | Указывает триггер, который запускает задачу при входе пользователя в систему.<br/>                       |
| [**регистратионтригжер**](taskschedulerschema-registrationtrigger-triggergroup-element.md) | [**регистратионтригжертипе**](taskschedulerschema-registrationtriggertype-complextype.md) | Указывает триггер, который запускает задачу при регистрации задачи.<br/>               |
| [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md)                 | [**тиметригжертипе**](taskschedulerschema-timetriggertype-complextype.md)                 | Указывает триггер, который запускает задачу при активации триггера.<br/>             |



## <a name="remarks"></a>Комментарии

Перечисленные выше дочерние элементы можно добавлять в любом порядке.

Для разработки на C++ триггеры задачи указываются с помощью [**свойства Triggers объекта итаскдефинитион**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_triggers).

Для разработки сценариев триггеры задачи указываются с помощью свойства [**таскдефинитион. triggers**](taskdefinition-triggers.md) .

## <a name="examples"></a>Примеры

Полный пример XML-кода для задачи, указывающей триггер, см. в разделе [пример триггера времени (XML)](time-trigger-example--xml-.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





