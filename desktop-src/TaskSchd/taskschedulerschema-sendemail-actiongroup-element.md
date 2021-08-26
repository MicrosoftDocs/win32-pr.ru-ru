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
ms.openlocfilehash: 1b42a8e63f3b64ef2a66a74300036bbf8ade24a7e0ee5c68b3d1d599f00a04b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099854"
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
| [**Скрытая копия**](taskschedulerschema-bcc-sendemailtype-element.md)                   | **строка**                                                                   | Указывает адреса электронной почты, используемые в строке СК сообщения электронной почты.<br/>               |
| [**Текст**](taskschedulerschema-body-sendemailtype-element.md)                 | **строка**                                                                   | Задает текст в тексте сообщения электронной почты.<br/>                                  |
| [**Кому**](taskschedulerschema-cc-sendemailtype-element.md)                     | **строка**                                                                   | Указывает адреса электронной почты, используемые в строке CC сообщения электронной почты.<br/>                |
| [**Исходный тип**](taskschedulerschema-from-sendemailtype-element.md)                 | **строка**                                                                   | Указывает адрес электронной почты отправителя.<br/>                                            |
| [**хеадерфиелдс**](taskschedulerschema-headerfields-sendemailtype-element.md) | [**хеадерфиелдстипе**](taskschedulerschema-headerfieldstype-complextype.md) | Задает поля заголовка и их значения, используемые в заголовке сообщения электронной почты.<br/> |
| [**ReplyTo**](taskschedulerschema-replyto-sendemailtype-element.md)           | **строка**                                                                   | Указывает адреса электронной почты, на которые вы ответили в сообщении электронной почты.<br/>               |
| [**Сервер**](taskschedulerschema-server-sendemailtype-element.md)             | [**нонемптистринг**](taskschedulerschema-nonemptystring-simpletype.md)      | Указывает сервер электронной почты, используемый для отправки сообщения электронной почты. <br/>                           |
| [**Тема**](taskschedulerschema-subject-sendemailtype-element.md)           | **строка**                                                                   | Указывает тему сообщения электронной почты.<br/>                                           |
| [**Кому**](taskschedulerschema-to-sendemailtype-element.md)                     | **строка**                                                                   | Указывает адреса электронной почты, на которые будет отправлено сообщение электронной почты.<br/>                        |



## <a name="remarks"></a>Remarks

Сведения о разработке на языке C++ см. в разделе интерфейс [**иемаилактион**](/windows/win32/api/taskschd/nn-taskschd-iemailaction) .

Сведения о разработке сценариев см. в разделе объект [**емаилактион**](emailaction.md) .

**Windows 8 и Windows Server 2012:** Этот элемент был удален. Используйте Иексекактион с командлетом PowerShell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) в качестве обходного пути.

## <a name="examples"></a>Примеры

Полный пример XML-кода для задачи, указывающей действие электронной почты, см. в разделе [пример триггера события (XML)](/previous-versions//aa446889(v=vs.85)).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                 |
| Поддержка конца сервера<br/>    | Windows Server 2008 R2<br/>                    |



 

