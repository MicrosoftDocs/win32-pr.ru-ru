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
ms.openlocfilehash: 955dcc93b826b4f86bffd3371ab9907e56dfe7f35649aee603cb18716868f535
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959534"
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
| [**Основной**](taskschedulerschema-principal-principaltype-element.md) | [**принЦипалтипе**](taskschedulerschema-principaltype-complextype.md) | Указывает учетные данные безопасности для участника.<br/> |



## <a name="remarks"></a>Remarks

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
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





