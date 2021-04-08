---
title: Элемент SendEmail (actionGroup)
description: Представляет действие, которое отправляет сообщение электронной почты.
ms.assetid: 83416b02-8327-47b3-9dfc-1bf5b9365728
keywords:
- планировщик задач элемента SendEmail
topic_type:
- apiref
api_name:
- SendEmail
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81f6f3437521dea2c5cf6e157ad7997718632081
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989107"
---
# <a name="sendemail-actiongroup-element"></a>Элемент SendEmail (actionGroup)

Представляет действие, которое отправляет сообщение электронной почты.

``` syntax
<xs:element name="SendEmail"
    type="sendEmailType"
 />
```

Элемент **SendEmail** определяется параметром [**actionGroup**](taskschedulerschema-actiongroup-group.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                         | Унаследован от                                                       | Описание                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [**Действия**](taskschedulerschema-actions-tasktype-element.md) | [**актионстипе**](taskschedulerschema-actionstype-complextype.md) | Содержит действия, выполняемые задачей.<br/> |



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



## <a name="remarks"></a>Комментарии

Сведения о разработке на языке C++ см. в разделе интерфейс [**иемаилактион**](/windows/win32/api/taskschd/nn-taskschd-iemailaction) .

Сведения о разработке сценариев см. в разделе объект [**емаилактион**](emailaction.md) .

**Windows 8 и Windows Server 2012:** Этот элемент был удален. Используйте Иексекактион с командлетом PowerShell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) в качестве обходного пути.

## <a name="examples"></a>Примеры

Полный пример XML-кода для задачи, указывающей действие электронной почты, см. в разделе [пример триггера события (XML)](/previous-versions//aa446889(v=vs.85)).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                 |
| Поддержка конца сервера<br/>    | Windows Server 2008 R2<br/>                    |



 

