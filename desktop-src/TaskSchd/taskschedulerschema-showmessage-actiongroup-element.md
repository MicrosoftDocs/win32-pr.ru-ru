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
ms.openlocfilehash: a1344aadfa5fe67e411048bac2a83330ea704c50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340495"
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



## <a name="remarks"></a>Комментарии

Для разработки сценариев действие окна сообщения указывается с помощью объекта [**шовмессажеактион**](showmessageaction.md) .

Для разработки на C++ действие окна сообщения указывается с помощью интерфейса [**ишовмессажеактион**](/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction) .

**Windows 8 и Windows Server 2012:** Этот элемент был удален. Для отображения сообщения в сеансе пользователя можно использовать Иексекактион с функцией Windows Scripting [**MsgBox**](/previous-versions/sfw6660x(v=vs.80)) .

## <a name="examples"></a>Примеры

Полный пример XML-кода для задачи, использующей действие окна сообщения, см. в разделе [Пример сообщения (XML)](/previous-versions//aa381917(v=vs.85)).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                 |
| Поддержка конца сервера<br/>    | Windows Server 2008 R2<br/>                    |



 

