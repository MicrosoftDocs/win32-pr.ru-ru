---
title: UserId (ПринЦипалтипе), элемент
description: Указывает идентификатор пользователя, необходимый для выполнения задач, связанных с участником.
ms.assetid: 7f3c92bf-c982-4155-9391-862f674a3665
keywords:
- Элемент UserId планировщик задач
topic_type:
- apiref
api_name:
- UserId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe12f76c35238251e2ecc60f848e2f7eb4eaa681
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104416149"
---
# <a name="userid-principaltype-element"></a>UserId (ПринЦипалтипе), элемент

Указывает идентификатор пользователя, необходимый для выполнения задач, связанных с участником.

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
 />
```

Элемент **UserID** определяется сложным типом [**принЦипалтипе**](taskschedulerschema-principaltype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                  | Унаследован от                                                           | Описание                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Основного**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Указывает учетные данные безопасности для участника.<br/> |



## <a name="remarks"></a>Комментарии

Элемент **UserID** и элемент [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) используются вместе для определения пользователя, необходимого для выполнения этих задач, использующих этот участник.

Нельзя одновременно указать идентификатор пользователя и идентификатор группы. Укажите либо **идентификатор UserID** , либо элемент [**groupId**](taskschedulerschema-groupid-principaltype-element.md) , но не оба.

Для разработки сценариев идентификатор пользователя указывается с помощью свойства [**Principal. UserID**](principal-userid.md) .

Для разработки на C++ идентификатор пользователя указывается с помощью свойства [**IPrincipal:: UserID**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid) .

## <a name="examples"></a>Примеры

Следующий XML-код определяет принцип, используя идентификатор пользователя.


```XML
<Principal>
    <UserId></UserId>
    <LogonType><LogonType>
    <DisplayName></DisplayName>
 </Principal>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





