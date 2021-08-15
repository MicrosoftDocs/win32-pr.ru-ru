---
title: Сложный тип ПринЦипалтипе
description: Определяет атрибут, дочерние элементы и сведения о последовательности для элемента Principal.
ms.assetid: 0f39d0a7-c9c9-402f-afe1-4378466ac1b6
keywords:
- планировщик задач сложного типа ПринЦипалтипе
topic_type:
- apiref
api_name:
- principalType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e6b2d7e71642ab0294f6e930eef40c5841aa5832fcc3a8d1c45aef2d7e80bbda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611916"
---
# <a name="principaltype-complex-type"></a>Сложный тип ПринЦипалтипе

Определяет атрибут, дочерние элементы и сведения о последовательности для элемента [**Principal**](taskschedulerschema-principal-principaltype-element.md) .

``` syntax
<xs:complexType name="principalType">
    <xs:all>
        <xs:element name="UserId"
            type="nonEmptyString"
            minOccurs="0"
         />
        <xs:element name="LogonType"
            type="logonType"
            minOccurs="0"
            maxOccurs="1"
         />
        <xs:element name="GroupId"
            type="nonEmptyString"
            minOccurs="0"
         />
        <xs:element name="DisplayName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="RunLevel"
            type="runLevelType"
            minOccurs="0"
         />
        <xs:element name="ProcessTokenSidType"
            type="processTokenSidType"
            minOccurs="0"
            maxOccurs="1"
         />
        <xs:element name="RequiredPrivileges"
            type="requiredPrivilegesType"
            minOccurs="0"
         />
    </xs:all>
    <xs:attribute name="id"
        type="ID"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                                             | Тип                                                                                     | Описание                                                                                                                 |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**DisplayName**](taskschedulerschema-displayname-principaltype-element.md)                        | строка                                                                                   | Указывает имя участника, который отображается в планировщик задач пользовательском интерфейсе.<br/>                 |
| [**Идентификатор**](taskschedulerschema-groupid-principaltype-element.md)                                | [**нонемптистринг**](taskschedulerschema-nonemptystring-simpletype.md)                  | Указывает идентификатор группы пользователей, необходимой для выполнения задач, связанных с участником.<br/> |
| [**LogonType**](taskschedulerschema-logontype-principaltype-element.md)                            | [**logonType**](taskschedulerschema-logontype-simpletype.md)                            | Указывает метод входа в систему безопасности, необходимый для выполнения задач, связанных с участником.<br/>        |
| [**процесстокенсидтипе**](taskschedulerschema-processtokensidtype-principaltype-element.md)        | [**процесстокенсидтипе**](taskschedulerschema-processtokensidtype-simpletype.md)        | Указывает типы идентификаторов безопасности процесса (SID), которые могут использоваться задачами.<br/>                              |
| [**рекуиредпривилежес**](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) | [**рекуиредпривилежестипе**](taskschedulerschema-requiredprivilegestype-complextype.md) | Указывает необходимые привилегии для выполнения задачи.<br/>                                                               |
| [**RunLevel**](taskschedulerschema-runlevel-principaltype-element.md)                              | [**рунлевелтипе**](taskschedulerschema-runleveltype-simpletype.md)                      | Указывает уровень разрешений, в котором будет выполняться задача.<br/>                                                     |
| [**UserId**](taskschedulerschema-userid-principaltype-element.md)                                  | [**нонемптистринг**](taskschedulerschema-nonemptystring-simpletype.md)                  | Указывает идентификатор пользователя, необходимый для выполнения задач, связанных с участником.<br/>              |



## <a name="attributes"></a>Атрибуты



| Имя | Тип | Описание                                           |
|------|------|-------------------------------------------------------|
| идентификатор   | ID   | Указывает идентификатор участника.<br/> |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>              |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач сложные типы схемы](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





