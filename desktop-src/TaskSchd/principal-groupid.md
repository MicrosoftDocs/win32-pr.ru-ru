---
title: Свойство Principal. GroupId
description: Для создания скриптов Возвращает или задает идентификатор группы пользователей, необходимой для выполнения задач, связанных с участником.
ms.assetid: be0b7cd1-0e17-4aa5-af8e-880c95b3e7dc
keywords:
- Свойство GroupId планировщик задач
- Свойство GroupId планировщик задач, объект Principal
- Объект Principal планировщик задач, свойство GroupId
topic_type:
- apiref
api_name:
- Principal.GroupId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc7b5acd17d32b0123723fe53f91e390c37f42d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681991"
---
# <a name="principalgroupid-property"></a>Свойство Principal. GroupId

Для создания скриптов Возвращает или задает идентификатор группы пользователей, необходимой для выполнения задач, связанных с участником.

## <a name="syntax"></a>Синтаксис


```VB
Principal.GroupId As String
```



## <a name="property-value"></a>Значение свойства

Идентификатор группы пользователей, связанной с этим участником.

## <a name="remarks"></a>Комментарии

Не устанавливайте это свойство, если в свойстве [**UserID**](principal-userid.md) указан идентификатор пользователя.

При чтении или записи XML-кода для задачи идентификатор группы участника указывается в элементе [**groupId**](taskschedulerschema-groupid-principaltype-element.md) схемы планировщик задач.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                          |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                    |
| Библиотека типов<br/>             | <dl> <dt>Тасксчд. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**UserId**](principal-userid.md)
</dt> <dt>

[**Основного**](principal.md)
</dt> <dt>

[Планировщик заданий](task-scheduler-start-page.md)
</dt> </dl>

 

 





