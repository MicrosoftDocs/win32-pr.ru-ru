---
title: Сложный тип Сендемаилтипе
description: Определяет тип действия, используемого для указания того, что при выполнении задачи будет отправлено сообщение электронной почты. Этот тип определяет все элементы, используемые для моделирования сообщения электронной почты.
ms.assetid: e384971f-e7e4-4206-9d15-9555dfcbac2f
keywords:
- планировщик задач сложного типа Сендемаилтипе
topic_type:
- apiref
api_name:
- sendEmailType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 959e0b8f03223eb23b7a7bec69ba9b2aeea66447
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672900"
---
# <a name="sendemailtype-complex-type"></a>Сложный тип Сендемаилтипе

Определяет тип действия, используемого для указания того, что при выполнении задачи будет отправлено сообщение электронной почты. Этот тип определяет все элементы, используемые для моделирования сообщения электронной почты.

``` syntax
<xs:complexType name="sendEmailType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="Server"
                    type="nonEmptyString"
                 />
                <xs:element name="Subject"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="To"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="Cc"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="Bcc"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="ReplyTo"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="From"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="HeaderFields"
                    type="headerFieldsType"
                    minOccurs="0"
                 />
                <xs:element name="Body"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="Attachments"
                    type="attachmentsType"
                    minOccurs="0"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                        | Тип                                                                         | Описание                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**Вложения**](taskschedulerschema-attachments-sendemailtype-element.md)   | [**аттачментстипе**](taskschedulerschema-attachmentstype-complextype.md)   | Указывает список вложений в сообщении электронной почты.<br/>                                 |
| [**Скрытая копия**](taskschedulerschema-bcc-sendemailtype-element.md)                   | **string**                                                                   | Указывает адреса электронной почты, используемые в строке СК сообщения электронной почты.<br/>               |
| [**Текст**](taskschedulerschema-body-sendemailtype-element.md)                 | **string**                                                                   | Задает текст в тексте сообщения электронной почты.<br/>                                  |
| [**Кому**](taskschedulerschema-cc-sendemailtype-element.md)                     | **string**                                                                   | Указывает адреса электронной почты, используемые в строке CC сообщения электронной почты.<br/>                |
| [**Исходный тип**](taskschedulerschema-from-sendemailtype-element.md)                 | **string**                                                                   | Указывает адрес электронной почты отправителя.<br/>                                            |
| [**хеадерфиелдс**](taskschedulerschema-headerfields-sendemailtype-element.md) | [**хеадерфиелдстипе**](taskschedulerschema-headerfieldstype-complextype.md) | Задает поля заголовка и их значения, используемые в заголовке сообщения электронной почты.<br/> |
| [**ReplyTo**](taskschedulerschema-replyto-sendemailtype-element.md)           | **string**                                                                   | Указывает адреса электронной почты, на которые вы ответили в сообщении электронной почты.<br/>               |
| [**Сервером**](taskschedulerschema-server-sendemailtype-element.md)             | [**нонемптистринг**](taskschedulerschema-nonemptystring-simpletype.md)      | Указывает сервер электронной почты, используемый для отправки сообщения электронной почты. <br/>                           |
| [**Субъект**](taskschedulerschema-subject-sendemailtype-element.md)           | **string**                                                                   | Указывает тему сообщения электронной почты.<br/>                                           |
| [**Кому**](taskschedulerschema-to-sendemailtype-element.md)                     | **string**                                                                   | Указывает адреса электронной почты, на которые будет отправлено сообщение электронной почты.<br/>                        |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



 

 





