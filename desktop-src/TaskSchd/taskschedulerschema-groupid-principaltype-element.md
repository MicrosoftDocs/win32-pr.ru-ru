---
title: Элемент GroupId (ПринЦипалтипе)
description: Указывает идентификатор группы пользователей, необходимой для выполнения задач, связанных с участником.
ms.assetid: 1e576c31-79a9-42d4-b497-74412e464d60
keywords:
- Элемент GroupId планировщик задач
topic_type:
- apiref
api_name:
- GroupId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4376e7037c228ebf2d2ffdc193cc34e7f92647220251cd82f09b0b65c7f9a81c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131843"
---
# <a name="groupid-principaltype-element"></a>Элемент GroupId (ПринЦипалтипе)

Указывает идентификатор группы пользователей, необходимой для выполнения задач, связанных с участником.

``` syntax
<xs:element name="GroupId"
    type="nonEmptyString"
 />
```

Элемент **groupId** определяется сложным типом [**принЦипалтипе**](taskschedulerschema-principaltype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                  | Унаследован от                                                           | Описание                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Основной**](taskschedulerschema-principal-principaltype-element.md) | [**принЦипалтипе**](taskschedulerschema-principaltype-complextype.md) | Указывает учетные данные безопасности для участника.<br/> |



## <a name="remarks"></a>Remarks

Нельзя одновременно указать идентификатор группы и идентификатор пользователя. Укажите либо элементы [**UserID**](taskschedulerschema-userid-principaltype-element.md) , либо **groupId** , но не оба.

Для разработки скриптов идентификатор группы субъекта указывается с помощью свойства [**Principal. groupId**](principal-groupid.md) .

Для разработки на C++ идентификатор группы субъекта указывается с помощью свойства [**IPrincipal:: groupId**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_groupid) .

## <a name="examples"></a>Примеры

Полный пример XML-кода для задачи, использующей этот элемент, см. в разделе [пример триггера LOGON (XML)](logon-trigger-example--xml-.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>       |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





