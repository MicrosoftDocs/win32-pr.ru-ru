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
ms.openlocfilehash: 9501184f3316e464aa26f42d51e0b4c27eccaeb72d447faa91edaa33b0b4774c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060032"
---
# <a name="principaluserid-property"></a>Свойство Principal. UserId

Для сценариев Возвращает или задает идентификатор пользователя, необходимый для выполнения задач, связанных с участником.

## <a name="syntax"></a>Синтаксис


```VB
Principal.UserId As String
```



## <a name="property-value"></a>Значение свойства

Идентификатор пользователя, необходимый для выполнения задачи.

## <a name="remarks"></a>Remarks

Не устанавливайте это свойство, если в свойстве [**groupId**](principal-groupid.md) указан идентификатор группы.

При чтении или записи XML для задачи идентификатор пользователя для субъекта указывается с помощью элемента [**UserID**](taskschedulerschema-userid-principaltype-element.md) схемы планировщик задач.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                    |
| Библиотека типов<br/>             | <dl> <dt>Тасксчд. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> <dt>

[**Основной**](principal.md)
</dt> <dt>

[**Principal. GroupId**](principal-groupid.md)
</dt> </dl>

 

 





