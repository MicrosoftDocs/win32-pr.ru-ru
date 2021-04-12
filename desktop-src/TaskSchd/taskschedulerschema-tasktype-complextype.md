---
title: Сложный тип taskType (планировщик задач)
description: Определяет дочерние элементы и сведения о последовательности для элемента Task.
ms.assetid: 622b2bf4-c7e0-403c-bd6c-99b687c1d439
keywords:
- планировщик задач сложного типа taskType
topic_type:
- apiref
api_name:
- taskType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0e86174920c28614f6c871e3f0bb0bc322243009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491667"
---
# <a name="tasktype-complex-type"></a>Сложный тип taskType

Определяет дочерние элементы и сведения о последовательности для элемента [**Task**](taskschedulerschema-task-element.md) .

``` syntax
<xs:complexType name="taskType">
    <xs:all>
        <xs:element name="RegistrationInfo"
            type="registrationInfoType"
            minOccurs="0"
         />
        <xs:element name="Triggers"
            type="triggersType"
            minOccurs="0"
         />
        <xs:element name="Settings"
            type="settingsType"
            minOccurs="0"
         />
        <xs:element name="Data"
            type="dataType"
            minOccurs="0"
         />
        <xs:element name="Principals"
            type="principalsType"
            minOccurs="0"
         />
        <xs:element name="Actions"
            type="actionsType"
         />
    </xs:all>
    <xs:attribute name="version"
        type="versionType"
        use="optional"
        fixed="1.3"
     />
</xs:complexType>
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



## <a name="attributes"></a>Атрибуты



| Имя    | Тип                                                              | Description                                   |
|---------|-------------------------------------------------------------------|-----------------------------------------------|
| version | [**версионтипе**](taskschedulerschema-versiontype-simpletype.md) | Указывает версию задачи.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач сложные типы схемы](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





