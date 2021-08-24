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
ms.openlocfilehash: 0242700b2f22050741d9de175b7dae532cc5ef4bb2097fadb23799ce3b2f82b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118356346"
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
| [**Скрытая копия**](taskschedulerschema-bcc-sendemailtype-element.md)                   | **строка**                                                                   | Указывает адреса электронной почты, используемые в строке СК сообщения электронной почты.<br/>               |
| [**Текст**](taskschedulerschema-body-sendemailtype-element.md)                 | **строка**                                                                   | Задает текст в тексте сообщения электронной почты.<br/>                                  |
| [**Кому**](taskschedulerschema-cc-sendemailtype-element.md)                     | **строка**                                                                   | Указывает адреса электронной почты, используемые в строке CC сообщения электронной почты.<br/>                |
| [**Исходный тип**](taskschedulerschema-from-sendemailtype-element.md)                 | **строка**                                                                   | Указывает адрес электронной почты отправителя.<br/>                                            |
| [**хеадерфиелдс**](taskschedulerschema-headerfields-sendemailtype-element.md) | [**хеадерфиелдстипе**](taskschedulerschema-headerfieldstype-complextype.md) | Задает поля заголовка и их значения, используемые в заголовке сообщения электронной почты.<br/> |
| [**ReplyTo**](taskschedulerschema-replyto-sendemailtype-element.md)           | **строка**                                                                   | Указывает адреса электронной почты, на которые вы ответили в сообщении электронной почты.<br/>               |
| [**Сервер**](taskschedulerschema-server-sendemailtype-element.md)             | [**нонемптистринг**](taskschedulerschema-nonemptystring-simpletype.md)      | Указывает сервер электронной почты, используемый для отправки сообщения электронной почты. <br/>                           |
| [**Тема**](taskschedulerschema-subject-sendemailtype-element.md)           | **строка**                                                                   | Указывает тему сообщения электронной почты.<br/>                                           |
| [**Кому**](taskschedulerschema-to-sendemailtype-element.md)                     | **строка**                                                                   | Указывает адреса электронной почты, на которые будет отправлено сообщение электронной почты.<br/>                        |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



 

 





