---
title: Рекуиредпривилежес (Рекуиредпривилежестипе), элемент
description: Указывает привилегии, необходимые для задачи.
ms.assetid: 7b615af8-76f9-498c-aa2d-7da02d64992f
keywords:
- планировщик задач элемента Рекуиредпривилежес
topic_type:
- apiref
api_name:
- RequiredPrivileges
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e395a61aace07dccb27eab04d9c0299115c25f16d84cd42e3d607435478f8060
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611491"
---
# <a name="requiredprivileges-requiredprivilegestype-element"></a>Рекуиредпривилежес (Рекуиредпривилежестипе), элемент

Указывает привилегии, необходимые для задачи.

``` syntax
<xs:element name="RequiredPrivileges"
    type="requiredPrivilegesType"
    minOccurs="0"
 />
```

Элемент **рекуиредпривилежес** определяется сложным типом [**рекуиредпривилежестипе**](taskschedulerschema-requiredprivilegestype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                                  | Унаследован от                                                           | Описание                                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Субъект (ПринЦипалтипе)**](taskschedulerschema-principal-principaltype-element.md) | [**принЦипалтипе**](taskschedulerschema-principaltype-complextype.md) | Указывает учетные данные безопасности для участника.<br/> |



## <a name="remarks"></a>Remarks

Для разработки на C++ эта информация доступна через свойство [**IPrincipal2:: рекуиредпривилеже**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege) .

## <a name="examples"></a>Примеры

Следующий XML-код определяет, используя идентификатор группы и необходимые привилегии.


```XML
<Principal>
    <RequiredPrivileges>
        <Privilege>SeCreateTokenPrivilege</Privilege>
    </RequiredPrivileges>
</Principal>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>              |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





