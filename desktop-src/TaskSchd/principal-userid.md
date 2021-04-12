---
title: Свойство Principal. UserId
description: Для сценариев Возвращает или задает идентификатор пользователя, необходимый для выполнения задач, связанных с участником.
ms.assetid: 57a34d7b-70b2-4156-b525-befecbaf070d
keywords:
- UserId, свойство планировщик задач
- Свойство UserId планировщик задач, объект Principal
- Объект Principal планировщик задач, свойство UserId
topic_type:
- apiref
api_name:
- Principal.UserId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae6fce7fcfdf235ba8a83f262161c2e0f2afc71c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136350"
---
# <a name="principaluserid-property"></a>Свойство Principal. UserId

Для сценариев Возвращает или задает идентификатор пользователя, необходимый для выполнения задач, связанных с участником.

## <a name="syntax"></a>Синтаксис


```VB
Principal.UserId As String
```



## <a name="property-value"></a>Значение свойства

Идентификатор пользователя, необходимый для выполнения задачи.

## <a name="remarks"></a>Комментарии

Не устанавливайте это свойство, если в свойстве [**groupId**](principal-groupid.md) указан идентификатор группы.

При чтении или записи XML для задачи идентификатор пользователя для субъекта указывается с помощью элемента [**UserID**](taskschedulerschema-userid-principaltype-element.md) схемы планировщик задач.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                    |
| Библиотека типов<br/>             | <dl> <dt>Тасксчд. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> <dt>

[**Основного**](principal.md)
</dt> <dt>

[**Principal. GroupId**](principal-groupid.md)
</dt> </dl>

 

 





