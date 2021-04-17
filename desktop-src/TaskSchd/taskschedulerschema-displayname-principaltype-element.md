---
title: Элемент DisplayName (ПринЦипалтипе)
description: Указывает имя участника, отображаемого в пользовательском интерфейсе планировщик задач.
ms.assetid: a8640cc9-fc16-4e73-9f0c-1ebff338fb84
keywords:
- Элемент DisplayName планировщик задач
topic_type:
- apiref
api_name:
- DisplayName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e8ef310869ea8558bca231e866ddeefc0dc35944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535501"
---
# <a name="displayname-principaltype-element"></a>Элемент DisplayName (ПринЦипалтипе)

Указывает имя участника, отображаемого в пользовательском интерфейсе планировщик задач.

``` syntax
<xs:element name="DisplayName"
    type="string"
 />
```

Элемент **DisplayName** определяется сложным типом [**принЦипалтипе**](taskschedulerschema-principaltype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                  | Унаследован от                                                           | Описание                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Основного**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Указывает учетные данные безопасности для участника.<br/> |



## <a name="remarks"></a>Комментарии

Для разработки сценариев отображаемое имя участника указывается с помощью свойства [**Principal. DisplayName**](principal-displayname.md) .

Для разработки на C++ отображаемое имя участника указывается с помощью свойства [**IPrincipal::D исплайнаме**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_displayname) .

## <a name="examples"></a>Примеры

Следующий XML-код определяет, используя идентификатор группы и отображаемое имя.


```XML
<Principal>
    <GroupId></GroupId>
    <DisplayName></DisplayName>
 </Principal>
```



Следующий код XML определяет субъект, используя идентификатор пользователя и отображаемое имя.


```XML
<Principal>
    <UserId></UserId>
    <LogonType></LogonType>
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

 

 





