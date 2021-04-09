---
title: Сложный тип Регистратионинфотипе
description: Определяет дочерние элементы и сведения о последовательности для элемента Регистратионинфо.
ms.assetid: 855eb0a4-6037-4868-ae09-6c9f01d91545
keywords:
- планировщик задач сложного типа Регистратионинфотипе
topic_type:
- apiref
api_name:
- registrationInfoType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe98a06daf84ec753c26903cc09787cec65c8d10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988948"
---
# <a name="registrationinfotype-complex-type"></a>Сложный тип Регистратионинфотипе

Определяет дочерние элементы и сведения о последовательности для элемента [**регистратионинфо**](taskschedulerschema-registrationinfo-tasktype-element.md) .

``` syntax
<xs:complexType name="registrationInfoType">
    <xs:all>
        <xs:element name="URI"
            type="anyURI"
            minOccurs="0"
         />
        <xs:element name="SecurityDescriptor"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Source"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Date"
            type="dateTime"
            minOccurs="0"
         />
        <xs:element name="Author"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Version"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Description"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Documentation"
            type="string"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                                           | Тип     | Описание                                                                                                        |
|---------------------------------------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------|
| [**Автор**](taskschedulerschema-author-registrationinfotype-element.md)                         | строка   | Указывает автора задачи.<br/>                                                                       |
| [**Дата**](taskschedulerschema-date-registrationinfotype-element.md)                             | dateTime | Указывает дату и время регистрации задачи.<br/>                                                |
| [**Описание**](taskschedulerschema-description-registrationinfotype-element.md)               | строка   | Указание описания задачи.<br/>                                                                  |
| [**Документация**](taskschedulerschema-documentation-registrationinfotype-element.md)           | строка   | Указывает любую дополнительную документацию для задачи.<br/>                                                    |
| [**SecurityDescriptor**](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) | строка   | Указывает дескриптор безопасности задачи.<br/>                                                          |
| [**Источника**](taskschedulerschema-source-registrationinfotype-element.md)                         | строка   | Указывает, откуда поступила задача. Например, из компонента, службы, приложения или пользователя.<br/> |
| [**URI**](taskschedulerschema-uri-registrationinfotype-element.md)                               | anyURI   | Указывает универсальный код ресурса (URI) задачи.<br/>                                                                          |
| [**Версия**](taskschedulerschema-version-registrationinfotype-element.md)                       | строка   | Указывает номер версии задачи.<br/>                                                               |



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

 

 





