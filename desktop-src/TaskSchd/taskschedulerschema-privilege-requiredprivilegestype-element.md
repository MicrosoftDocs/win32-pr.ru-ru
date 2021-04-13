---
title: Элемент Privilege (Рекуиредпривилежестипе)
description: Указывает правую задачу для выполнения различных операций, связанных с системой, таких как завершение работы системы, загрузка драйверов устройств или изменение системного времени.
ms.assetid: d5585d1c-e121-4770-a13e-108158bc703e
keywords:
- Элемент Privilege планировщик задач
topic_type:
- apiref
api_name:
- Privilege
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 55e9263ae9d02bb384bfbe56101ea82f98c2e076
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492279"
---
# <a name="privilege-requiredprivilegestype-element"></a>Элемент Privilege (Рекуиредпривилежестипе)

Указывает правую задачу для выполнения различных операций, связанных с системой, таких как завершение работы системы, загрузка драйверов устройств или изменение системного времени.

``` syntax
<xs:element name="Privilege"
    type="privilegeType"
    maxOccurs="64"
    minOccurs="1"
 />
```

Элемент **Privilege** определяется сложным типом [**рекуиредпривилежестипе**](taskschedulerschema-requiredprivilegestype-complextype.md) .

## <a name="parent-element"></a>Родительский элемент



| Элемент                                                                                             | Унаследован от                                                                             | Описание                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**рекуиредпривилежес**](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) | [**рекуиредпривилежестипе**](taskschedulerschema-requiredprivilegestype-complextype.md) | Содержит параметры, которые планировщик задач использует для выполнения задачи.<br/> |



## <a name="remarks"></a>Комментарии

Для разработки на C++ эта информация доступна через свойство [**IPrincipal2:: рекуиредпривилеже**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege) .

## <a name="examples"></a>Примеры

Следующий XML-код определяет элемент Settings, который указывает право задачи для выполнения различных операций, связанных с системой, таких как завершение работы системы, загрузка драйверов устройств или изменение системного времени.


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
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>              |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[планировщик задач элементы схемы](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





