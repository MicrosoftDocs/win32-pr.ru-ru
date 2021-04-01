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
ms.openlocfilehash: 080a408f65ac7a36ada1751bbd5cb95395cf0b35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071887"
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
| [**Основного**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Указывает учетные данные безопасности для участника.<br/> |



## <a name="remarks"></a>Комментарии

Нельзя одновременно указать идентификатор группы и идентификатор пользователя. Укажите либо элементы [**UserID**](taskschedulerschema-userid-principaltype-element.md) , либо **groupId** , но не оба.

Для разработки скриптов идентификатор группы субъекта указывается с помощью свойства [**Principal. groupId**](principal-groupid.md) .

Для разработки на C++ идентификатор группы субъекта указывается с помощью свойства [**IPrincipal:: groupId**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_groupid) .

## <a name="examples"></a>Примеры

Полный пример XML-кода для задачи, использующей этот элемент, см. в разделе [пример триггера LOGON (XML)](logon-trigger-example--xml-.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





