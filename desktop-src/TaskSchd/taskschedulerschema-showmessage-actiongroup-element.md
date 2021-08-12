---
title: ShowMessage (actionGroup), элемент
description: Представляет действие, показывающее окно сообщения.
ms.assetid: 33c6e437-b993-4b5e-b75a-fb3fda9b24df
keywords:
- планировщик задач элемента ShowMessage
topic_type:
- apiref
api_name:
- ShowMessage
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 474bc44550408591616d3a8d2c6c3c69a5a0d073c90297c60b4a831627c996e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611302"
---
# <a name="showmessage-actiongroup-element"></a>ShowMessage (actionGroup), элемент

Представляет действие, показывающее окно сообщения.

``` syntax
<xs:element name="ShowMessage"
    type="showMessageType"
 />
```

Элемент **ShowMessage** определяется параметром [**actionGroup**](taskschedulerschema-actiongroup-group.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                    | Унаследован от                                                       | Описание                                            |
|----------------------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [**Действия (taskType)**](taskschedulerschema-actions-tasktype-element.md) | [**актионстипе**](taskschedulerschema-actionstype-complextype.md) | Содержит действия, выполняемые задачей.<br/> |



## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                            | Тип           | Описание                                                               |
|--------------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| [**Текст**](taskschedulerschema-body-showmessagetype-element.md)   | нонемптистринг | Задает текст, отображаемый в тексте окна сообщения. <br/> |
| [**Заголовок**](taskschedulerschema-title-showmessagetype-element.md) | нонемптистринг | Задает заголовок окна сообщения. <br/>                       |



## <a name="remarks"></a>Remarks

Для разработки сценариев действие окна сообщения указывается с помощью объекта [**шовмессажеактион**](showmessageaction.md) .

Для разработки на C++ действие окна сообщения указывается с помощью интерфейса [**ишовмессажеактион**](/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction) .

**Windows 8 и Windows Server 2012:** Этот элемент был удален. для отображения сообщения в сеансе пользователя можно использовать иексекактион с функцией Windows scripting [**MsgBox**](/previous-versions/sfw6660x(v=vs.80)) .

## <a name="examples"></a>Примеры

Полный пример XML-кода для задачи, использующей действие окна сообщения, см. в разделе [Пример сообщения (XML)](/previous-versions//aa381917(v=vs.85)).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                 |
| Поддержка конца сервера<br/>    | Windows Server 2008 R2<br/>                    |



 

