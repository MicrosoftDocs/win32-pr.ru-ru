---
title: Элемент Task
description: Определяет задачу, выполняемую службой планировщик задач.
ms.assetid: 103a332a-8620-4e0c-81b5-4782d85fc391
keywords:
- планировщик задач элемента Task
topic_type:
- apiref
api_name:
- Task
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 38bac482f8546028d21db913e31dc4152f19f599
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891609"
---
# <a name="task-element"></a>Элемент Task

Определяет задачу, выполняемую службой планировщик задач.

``` syntax
<xs:element name="Task"
    type="taskType"
>
    <xs:key name="PrincipalKey">
        <xs:selector
            xpath="td:Principals/td:Principal"
         />
        <xs:field
            xpath="@id"
         />
    </xs:key>
    <xs:keyref name="ContextKeyRef">
        <xs:selector
            xpath="td:Actions"
         />
        <xs:field
            xpath="@Context"
         />
    </xs:keyref>
    <xs:unique name="UniqueId">
        <xs:selector
            xpath="td:Principals/td:Principal|td:Triggers/td:BootTrigger|td:Triggers/td:RegistrationTrigger|td:Triggers/td:IdleTrigger|td:Triggers/td:TimeTrigger|td:Triggers/td:EventTrigger|td:Triggers/td:LogonTrigger|td:Triggers/td:SessionStateChangeTrigger|td:Triggers/td:CalendarTrigger|td:Actions/td:Exec|td:Actions/td:ComHandler|td:Actions/td:SendEmail"
         />
        <xs:field
            xpath="@id"
         />
    </xs:unique>
</xs:element>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                           | Тип                                                                                 | Описание                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**Действия**](taskschedulerschema-actions-tasktype-element.md)                   | [**актионстипе**](taskschedulerschema-actionstype-complextype.md)                   | Указывает действия, выполняемые задачей.<br/>                                                                             |
| [**Data**](taskschedulerschema-data-tasktype-element.md)                         | [**Заданий**](taskschedulerschema-datatype-complextype.md)                         | Указывает дополнительные данные, связанные с задачей, но не используемые службой планировщик задач в противном случае.<br/>         |
| [**Субъекты**](taskschedulerschema-principals-tasktype-element.md)             | [**принЦипалстипе**](taskschedulerschema-principalstype-complextype.md)             | Указывает контексты безопасности, которые могут использоваться для выполнения задачи.<br/>                                                        |
| [**регистратионинфо**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**регистратионинфотипе**](taskschedulerschema-registrationinfotype-complextype.md) | Указывает административную информацию о задаче, например автора задачи и дату регистрации задачи.<br/> |
| [**Параметры**](taskschedulerschema-settings-tasktype-element.md)                 | [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md)                 | Задает параметры, которые планировщик задач использует для выполнения задачи.<br/>                                                 |
| [**Триггеры**](taskschedulerschema-triggers-tasktype-element.md)                 | [**тригжерстипе**](taskschedulerschema-triggerstype-complextype.md)                 | Задает триггеры, которые запускают задачу.<br/>                                                                              |



## <a name="remarks"></a>Комментарии

Сведения о разработке с + + см. в разделе [**итаскдефинитион**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition).

Сведения о разработке сценариев см. в разделе [**таскдефинитион**](taskdefinition.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





